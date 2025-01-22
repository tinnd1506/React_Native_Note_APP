# Note App 

## Main Components

### Root Layout (`_layout.tsx`)
- Sets up stack navigation with routes:
  - Home (`index`)
  - Note Details (`notes/[id]`)
  - 404 Page (`+not-found`)

### Home Screen (`index.tsx`)
- Displays list of notes using FlatList
- Each note is rendered as a card with:
  - Title
  - Preview text
- Implements navigation to note details screen
- Uses custom styles for dark theme

### Note Details (`notes/[id].tsx`)
- Displays full content of a selected note
- Uses dynamic routing with note ID parameter

### 404 Handling (`+not-found.tsx`)
- Displays when invalid route is accessed
- Provides link back to home screen
- Uses themed components for consistent styling

## Component Relationships

```mermaid
graph TD
    A[_layout.tsx] --> B[index.tsx]
    A --> C[notes/[id].tsx]
    A --> D[+not-found.tsx]
    B --> C
```

## Styling Approach
- Uses StyleSheet for component-specific styles
- Implements dark theme through background colors
- Maintains consistent spacing and typography
- Uses themed components for text and views

## Navigation Flow
1. Home screen displays note list
2. Tapping a note navigates to details view
3. Invalid routes show 404 page
4. 404 page provides return to home
