# Class Schedule Manager



## Overview

Class Schedule Manager is a robust desktop application for educational institutions to visualize, manage, and resolve conflicts in classroom schedules. Built with Python and Tkinter, this tool helps administrators and department schedulers efficiently manage room assignments and class times to minimize scheduling conflicts.

## Features

- **Visual Schedule Interface**: Intuitive drag-and-drop calendar view of class schedules by room
- **Conflict Detection**: Automatic identification and highlighting of scheduling conflicts
- **Conflict Resolution**: Tools to quickly resolve overlapping class schedules
- **Room Management**: View and edit schedules by building and room
- **Search Functionality**: Find courses quickly with instant search
- **Drag-and-Drop Editing**: Easily modify class times and days by dragging
- **Multi-Day Classes**: Support for classes that meet on multiple days of the week
- **Data Persistence**: Save schedule changes to Excel files
- **User-Friendly Interface**: Clean and intuitive design for educational administrators


## Requirements

- Python 3.6+
- Required Python packages:
  - pandas
  - tkinter (usually included with Python)
  - numpy

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/class-schedule-manager.git
   cd class-schedule-manager
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the application:
   ```bash
   python schedule_manager.py
   ```

## Usage Guide

### Loading a Schedule

1. Launch the application
2. Click "Load Schedule File" and select an Excel file with your class data
3. The file should contain columns for: Subject, Number, Section, Title, Days, Start, End, Bldg, Room

### Viewing Room Schedules

- **From Conflict List**: Double-click any conflict in the list to view that room's schedule
- **Manual Selection**: Enter building and room number in the input fields and click "Show Schedule"

### Managing Conflicts

1. Red-highlighted classes indicate scheduling conflicts
2. Double-click any class block to edit its details
3. Drag classes to new times or days to resolve conflicts
4. Right-click on a class to open the edit dialog

### Editing Classes

- **Drag and Drop**: Move classes by clicking and dragging
  - Vertical drag: Change class time
  - Horizontal drag: Move class to a different day
- **Edit Dialog**: Double-click or right-click a class to open detailed editing options
- **Conflict Resolution**: Use the "Resolve Conflicts" button in the edit dialog to manage overlapping classes

### Searching for Classes

1. Type a course code or title in the search box
2. Select a course from the results list
3. The application will display the relevant room schedule with that course highlighted

### Saving Changes

- Click "Save Changes" to update the current file
- Click "Save As New File" to create a new Excel file with your changes

## Data Format

The application expects an Excel file with the following columns:
- **Subject**: Department code (e.g., "MATH", "ENGL")
- **Number**: Course number (e.g., "101", "4250")
- **Section**: Section identifier (e.g., "001", "A")
- **Title**: Course title
- **Days**: Days of the week (U=Sunday, M=Monday, T=Tuesday, W=Wednesday, R=Thursday, F=Friday, S=Saturday)
- **Start**: Start time in HH:MM format
- **End**: End time in HH:MM format
- **Bldg**: Building identifier
- **Room**: Room number

## Features in Detail

### Conflict Detection

The system automatically:
- Identifies overlapping class times in the same room
- Highlights conflicting classes in red
- Shows a conflict counter badge with the number of overlaps
- Maintains a comprehensive list of all conflicts by room

### Day Representation

- **U**: Sunday
- **M**: Monday
- **T**: Tuesday
- **W**: Wednesday
- **R**: Thursday
- **F**: Friday
- **S**: Saturday

Classes that meet on multiple days use combined characters (e.g., "MWF" for Monday, Wednesday, Friday).

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request


## Acknowledgments

- Developed to streamline academic scheduling processes
- Inspired by the challenges faced by university department schedulers
