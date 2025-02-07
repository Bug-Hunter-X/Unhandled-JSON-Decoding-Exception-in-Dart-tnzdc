# Unhandled JSON Decoding Exception in Dart

This repository demonstrates a common error in Dart applications involving asynchronous HTTP requests and JSON decoding. The `bug.dart` file contains code that makes an HTTP request, decodes the JSON response, and lacks proper error handling for JSON decoding exceptions.  The `bugSolution.dart` file provides a corrected version with robust error handling.

## Problem

The original code fails to handle `FormatException` that can occur if the server returns malformed JSON. This can lead to unexpected app crashes. 

## Solution

The solution adds a `try-catch` block specifically around the `jsonDecode` call. This allows the app to gracefully handle invalid JSON responses, preventing crashes and providing informative error messages.