# Tags Manager

A lightweight, single-file web application for managing and organizing text tags. All data is stored locally in your browser using localStorage.

## Features

### Adding Tags
- Paste text into the left panel
- Text is split by commas (,) or periods (.)
- Click "Save Tags" to store them
- Preview shows what will be saved before committing
- Duplicate tags increment the count instead of creating duplicates

### Viewing Tags
- Tags display with a count badge showing frequency
- Sort options:
  - **Popular** - Most used tags first
  - **Newest** - Recently added/updated first
  - **Longest** - Longest text first
  - **Shortest** - Shortest text first

### Tag Actions
| Action | Result |
|--------|--------|
| Single click | Toggle selection |
| Double click | Edit tag inline |
| Click copy icon | Copy tag to clipboard |
| Click X icon | Delete tag (with undo) |

### Inline Editing
- Double-click any tag to edit its text
- Press **Enter** to save changes
- Press **Escape** to cancel
- If renamed to an existing tag, counts are merged

### Multi-Select & Bulk Actions
- Click tags to select/deselect them (purple highlight)
- When tags are selected, bulk action bar appears:
  - **X button** - Clear selection
  - **Copy All** - Copy all selected tags to clipboard
  - **Similar** - Find similar tags (splits words and searches)
  - **Delete** - Delete all selected tags
- Press **Escape** to deselect all

### Advanced Search
- Search bar supports multiple word search
- Type a word and press **Space** or **Enter** to add it as a search tag
- Each search word becomes a removable chip (click X to remove)
- Press **Backspace** when input is empty to remove the last search word
- Results prioritize:
  1. Exact matches
  2. Tags matching more search words
  3. Tags matching fewer search words

### Similar Tags
- Select one or more tags
- Click "Similar" button
- Words from selected tags are extracted and added to search
- Helps find related tags quickly

### Undo Delete
- When you delete a tag, an "Undo" button appears
- Click to restore the deleted tag
- Toast disappears when you perform another action (typing, clicking, searching)

### Data Management
- **Clear** button removes all saved tags (with confirmation)
- All data stored in browser localStorage
- Works offline, no server required

## Deployment

This is a single HTML file that can be:
- Opened directly in a browser
- Hosted on GitHub Pages
- Deployed to any static hosting service

## Tech Stack

- Vanilla HTML, CSS, JavaScript
- No dependencies or build process
- localStorage for persistence
