# Einops-implementation
# README

## Overview
This project implements a custom `rearrange()` function, inspired by the functionality of `einops`. The goal was to build a system that allows intuitive and flexible tensor rearrangement based on string patterns representing input and output axes. The function supports axis grouping, ellipsis (`...`), and nested structures, among other features.

The focus of the assignment was to understand pattern-based tensor reshaping and develop a clear, well-structured, and testable implementation.

## Design Approach

### Refactoring and Structure
- The initial implementation contained long, mixed-responsibility functions combining pattern parsing, axis parsing, batch handling, and rearrangement logic.
- This was refactored into smaller, clearly defined helper functions, each focused on a specific task. This significantly improved maintainability, readability, and debugging.
- The main function now delegates tasks to these helpers, making the codebase easier to extend and test.

### Parsing and Rearrangement Logic
- Attention given to correctly parse and expand ellipsis (`...`), which represent variable numbers of axes.
- A robust parser was implemented to extract input and output axis specifications, including support for nested and grouped elements.
- The axis-matching logic ensures that tensor dimensions are correctly aligned between input and output patterns.

### Error Handling and Tests
- Proper error checks and exceptions were added for invalid pattern specifications, mismatched axes, and unsupported configurations.
- Negative tests were included to validate these edge cases.
- All functions include type annotations and clearly written docstrings for better understanding.

## Challenges Faced
- Correct handling of ellipsis and their expansion based on remaining tensor axes.
- Dealing with nested pattern complexity and maintaining axis order across transformations.
- Simplifying the original monolithic code structure without losing functionality.
- Designing reusable components that generalize across different tensor shapes and patterns.

## Running the Code and Tests
1. Open the Colab notebook and run the cells sequentially.
2. The primary function to test is `rearrange(tensor, pattern)`.
3. At the end of the notebook, a set of test cases is provided:
   - Run the positive tests to verify the correctness of the implementation.
   - Run the negative tests to ensure proper error handling.

## Link to the Colab Notebook 
https://colab.research.google.com/drive/1ItaBxQIijixXYsFAMM08ENvk9wW5Gewz?usp=sharing
