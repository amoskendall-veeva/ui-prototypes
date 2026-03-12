# Process Monitor UI Styling & Layout Guidelines

This guide defines the specific UI patterns, components, and styling used in the **Process Monitor** (Drill Down) interface. It builds upon the core Vault styles but adds advanced data navigation and visualization patterns.

## Specialized CSS Variables

In addition to standard Vault variables, Process Monitor uses:

```css
:root {
    /* Specialized Context Colors */
    --tp-bar-bg: #f0f6ff;        /* Time Period Bar */
    --info-banner-bg: #fffbe6;   /* Info/Alert Banners */
    --info-banner-border: #f0e68c;
    --graph-step-stroke: #b0b0b0;
    --graph-hover-bg: #f0f6ff;
}
```

## Navigation & Layout Patterns

### 1. Section Tabs
Used to switch between high-level views (Overview, Process Graph, Records).
- **Idle State**: `text-[#666] border-b-2 border-transparent px-4 py-2.5`.
- **Active State**: `text-[var(--veeva-blue)] border-b-2 border-[var(--veeva-blue)] font-semibold`.
- **Hover**: `text-[var(--text-main)]`.

### 2. Time Period Bar
A sticky control bar for navigating time-based data buckets.
- **Background**: `bg-[#f0f6ff] border-b`.
- **Selector Button**: `border-[#b0c4de] bg-white font-semibold text-[13px] px-2.5 py-1 rounded`.
- **Navigation Controls**: Small gray-bordered buttons for "Older" and "Newer".

### 3. Info Banners (Smart Alerts)
Used for contextual feedback (e.g., when jumping between time periods).
- **Background**: `bg-[#fffbe6] border-b border-[#f0e68c] text-[13px]`.
- **Links**: `text-[var(--veeva-blue)] underline`.

---

## Data Grid & Advanced Filtering

### 1. Header Filter Dropdowns
Shadowed popovers triggered from column headers.
- **Container**: `absolute bg-white border shadow-lg rounded-[4px] p-[10px] w-[220px] z-20`.
- **Inputs**: Small 12px inputs and selects with `border-[#ccc]`.
- **Actions**: "Clear" (text button) and "Apply" (standard primary button).

### 2. Vertical Filter Summary
A collapsible summary list shown above the grid.
- **Toggle**: `text-[13px]` with a rotating caret.
- **Rows**: `flex flex-col gap-[2px] pl-4 py-1`.
- **Chip Style**: Bold label followed by value, with a light-gray "X" (`filter-remove`) for deletion.

---

## Visualization Components

### 1. Dashboard Summary Cards
High-level metric cards shown at the top of the workspace.
- **Header**: `bg-[#e3edfc] font-bold text-[14px] border-b`.
- **Metric Content**: Large bold numbers (`20px`) with small bold labels (`12px text-gray-500`).

### 2. Process Graph (SVG)
Flow-based visualization of variants.
- **Steps**: White boxes with `stroke-[#b0b0b0]` and `rx="6"`.
- **Labels**: `text-[12px] font-semibold`.
- **Arrows**: `stroke-[#999]` with arrowhead markers.
- **Hovercards**: `absolute shadow-xl border rounded-[6px] p-4 bg-white z-40`.

### 3. Configuration Sidebar
Used for complex parameters that affect the entire dashboard.
- **Groupings**: Uppercase labels in `text-gray-500 text-[12px]`.
- **Spaced Elements**: 24px vertical gap (`gap-6`) between parameter blocks.
- **Controls**: Standard 13px radio buttons and checkboxes.
