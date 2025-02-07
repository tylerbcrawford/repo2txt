# Product Context: repo2txt

## Purpose
repo2txt is a Python tool designed to streamline the process of preparing codebase training data for GPT-style Models (LLMs). Its primary purpose is to make it easier to pass an entire codebase to GPT models by compiling all repository assets into a single, comprehensive document.

## Problems Solved
1. **Code Organization for LLMs**: Makes it easier to feed entire codebases to LLMs by consolidating all files into a single document
2. **Repository Documentation**: Provides a complete view of a repository's structure and contents
3. **Training Data Preparation**: Simplifies the process of preparing code-based training data for LLMs

## Core Functionality
1. **Directory Tree Generation**: Creates a hierarchical view of the repository structure
2. **Content Compilation**: Combines all file contents into a single document
3. **Flexible Output**: Supports both .txt and .docx output formats
4. **Customizable Filtering**: Allows ignoring specific files, types, and directories

## Target Users
- AI/ML Engineers working with code-based LLM training
- Developers needing to share codebase context with LLMs
- Teams requiring comprehensive repository documentation

## Success Criteria
1. Successfully generates complete repository documentation
2. Maintains proper file organization and hierarchy
3. Provides flexible configuration options
4. Handles various file types and structures effectively
5. Produces clean, well-formatted output files