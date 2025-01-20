# Unhandled Exception During Asynchronous Network Request in Dart

This repository demonstrates a common error in Dart asynchronous programming: not properly handling exceptions that can occur during network requests. The `bug.dart` file shows the problematic code, while `bugSolution.dart` provides a more robust solution.

## Problem
The original code lacks comprehensive exception handling, potentially leading to unexpected crashes or silent failures.  The `try-catch` block is present but `rethrow` allows for the exception to propagate up the call stack which helps the programmer better handle it.

## Solution
The solution involves using Futures to manage asynchronous operations gracefully. The `try-catch` block handles exceptions during network requests and logs error messages.  The `rethrow` statement permits higher-level error handling mechanisms to take action (e.g., displaying an error message to the user or retrying the request).