# GUI Implementation Plan for repo2txt

## Overview
This document outlines the plan to add a graphical user interface to repo2txt with new features including clipboard functionality and token counting.

## Core Features to Implement

### 1. Basic GUI Framework
- Use tkinter for the main GUI framework
- Create a main window with proper layout and styling
- Implement responsive design for resizing

### 2. File/Directory Selection
- Add "Select Repository" button with directory picker dialog
- Display selected directory path
- Add validation for selected directory
- Show current working directory as default

### 3. Output Configuration
- Add output format selection (.txt/.docx)
- Add output file location picker
- Include default output name suggestion
- Add output file validation

### 4. New Features

#### Clipboard Integration
- Add "Copy to Clipboard" button
- Use pyperclip library for clipboard operations
- Include error handling for large content
- Add copy confirmation feedback

#### Token Counter
- Integrate tiktoken library for token counting
- Add real-time token count display
- Show token counts for:
  * Directory structure
  * File contents
  * Total repository
- Include token count in output file

## Technical Requirements

### Dependencies to Add
```
tkinter  # GUI framework
pyperclip  # Clipboard functionality
tiktoken  # Token counting
```

### New Files to Create

1. `src/repo2txt/gui.py`
   - Main GUI implementation
   - Window and widget setup
   - Event handlers
   - Integration with existing functionality

2. `src/repo2txt/utils/token_counter.py`
   - Token counting implementation
   - Different counting strategies
   - Caching mechanism for performance

3. `src/repo2txt/utils/clipboard_manager.py`
   - Clipboard operations
   - Large content handling
   - Error management

### Modifications to Existing Files

1. `repo2txt.py`
   - Add GUI launch option
   - Integrate token counting
   - Add clipboard functionality
   - Maintain CLI compatibility

2. `config.json`
   - Add GUI-specific configurations
   - Token counter settings
   - Clipboard size limits
   - UI preferences

## Implementation Steps

1. Setup Phase
   - Add new dependencies to requirements.txt
   - Create new directory structure
   - Update documentation

2. Core GUI Development
   - Implement basic window and layout
   - Add file/directory selection
   - Create output configuration options

3. New Features Integration
   - Implement clipboard functionality
   - Add token counting system
   - Create progress indicators

4. Testing and Refinement
   - Test with various repository sizes
   - Verify token counting accuracy
   - Ensure clipboard handling for large repos
   - Test GUI responsiveness

## Code Structure

```python
# gui.py structure
class Repo2TxtGUI:
    def __init__(self):
        self.window = tk.Tk()
        self.setup_ui()
        
    def setup_ui(self):
        # Create and arrange widgets
        self.create_directory_selector()
        self.create_output_config()
        self.create_clipboard_button()
        self.create_token_counter()
        
    def create_directory_selector(self):
        # Directory selection implementation
        
    def create_output_config(self):
        # Output configuration implementation
        
    def create_clipboard_button(self):
        # Clipboard functionality implementation
        
    def create_token_counter(self):
        # Token counter implementation
```

## Future Enhancements
1. Preview pane for directory tree
2. Save/load configuration profiles
3. Dark/light theme support
4. Recent projects list
5. Search functionality
6. Custom filtering interface

## Notes
- Maintain backwards compatibility with CLI
- Ensure proper error handling
- Consider memory usage for large repositories
- Add proper logging for debugging
- Include user feedback mechanisms