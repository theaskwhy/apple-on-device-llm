---
name: apple-on-device-llm
description: Use when you want to run Apple's free on-device language model (Foundation Models framework, Apple Intelligence Macs) from the command line for short private text tasks such as hooks, captions or summaries.
---

# Apple On-Device LLM from the Terminal

Run Apple's local model with a tiny Swift script — free, offline, private. Needs a Mac with Apple Intelligence and a macOS version that includes the Foundation Models framework. By The Ask Why Company.

## Script (fm.swift)
```swift
import Foundation
import FoundationModels
let prompt = try! String(contentsOfFile: CommandLine.arguments[1], encoding: .utf8)
let sem = DispatchSemaphore(value: 0)
Task {
  let model = SystemLanguageModel.default
  guard case .available = model.availability else { print("UNAVAILABLE: \(model.availability)"); sem.signal(); return }
  do { let s = LanguageModelSession(); let r = try await s.respond(to: prompt); print(r.content) }
  catch { print("ERROR: \(error)") }
  sem.signal()
}
sem.wait()
```
Run: `swift fm.swift prompt.txt`

## Tips
- Small context window: send short prompts; batch long jobs (e.g. 6 items per call) and append outputs to one file.
- Good for: hooks, captions, rewrites, short classification. Not for long research or facts that must be current.
- Ask for plain output and "no made-up facts or numbers"; review before use.
