HTML
<!-- index.html -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Overflow Demonstration & Layout Fixing</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>CSS Overflow & Layout Fixing</h1>
        <p>Demonstrating visible, hidden, auto, and scroll overflow behaviors.</p>
    </header>

    <main class="container">
        <!-- 1. overflow: visible -->
        <section class="overflow-section">
            <h2>1. <code>overflow: visible</code> (Default)</h2>
            <p>Content overflows outside the container boundaries without clipping.</p>
            <div class="box box-visible">
                <p>This is a long paragraph of text designed to test container boundaries. When overflow is set to visible, the text spills out of the fixed-height box and overlaps whatever is placed directly below it, which can break the layout if not handled properly.</p>
            </div>
        </section>

        <!-- 2. overflow: hidden -->
        <section class="overflow-section">
            <h2>2. <code>overflow: hidden</code></h2>
            <p>Overflowing content is clipped and hidden from view.</p>
            <div class="box box-hidden">
                <p>This is a long paragraph of text designed to test container boundaries. When overflow is set to hidden, any content that exceeds the fixed height of the box is cleanly clipped at the bottom border and cannot be scrolled or seen by the user.</p>
            </div>
        </section>

        <!-- 3. overflow: scroll -->
        <section class="overflow-section">
            <h2>3. <code>overflow: scroll</code></h2>
            <p>Scrollbars are always rendered to allow viewing hidden content.</p>
            <div class="box box-scroll">
                <p>This is a long paragraph of text designed to test container boundaries. When overflow is set to scroll, scrollbars appear on the box regardless of whether the content actually overflows, allowing users to scroll up and down within the fixed container.</p>
            </div>
        </section>

        <!-- 4. overflow: auto -->
        <section class="overflow-section">
            <h2>4. <code>overflow: auto</code></h2>
            <p>Scrollbars appear dynamically only when content exceeds the container size.</p>
            <div class="box box-auto">
                <p>This is a long paragraph of text designed to test container boundaries. When overflow is set to auto, scrollbars appear only when the content overflows the fixed height. If the content fits inside, no scrollbars are shown, making it the cleanest and most common solution for scrollable panels.</p>
            </div>
        </section>
    </main>

    <footer>
        <p>&copy; 2026 falak siddiqui. All rights reserved.</p>
    </footer>
</body>
</html>
CSS
/* style.css */
body {
    font-family: Arial, sans-serif;
    background-color: #f8fafc;
    color: #334155;
    margin: 0;
    padding: 0;
    line-height: 1.6;
}

header {
    background-color: #0f172a;
    color: #ffffff;
    text-align: center;
    padding: 2rem 1rem;
}

header h1 {
    margin-bottom: 0.5rem;
}

header p {
    color: #94a3b8;
    margin: 0;
}

.container {
    max-width: 700px;
    margin: 2rem auto;
    padding: 0 1rem;
    display: flex;
    flex-direction: column;
    gap: 2rem;
}

.overflow-section {
    background-color: #ffffff;
    border: 1px solid #e2e8f0;
    border-radius: 10px;
    padding: 1.5rem;
    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
}

.overflow-section h2 {
    font-size: 1.1rem;
    color: #0f172a;
    margin-top: 0;
    margin-bottom: 0.3rem;
}

.overflow-section > p {
    font-size: 0.9rem;
    color: #64748b;
    margin-bottom: 1rem;
}

/* Base Fixed-Height Box */
.box {
    height: 100px;
    background-color: #f1f5f9;
    border: 2px dashed #cbd5e1;
    border-radius: 6px;
    padding: 12px;
}

.box p {
    margin: 0;
    color: #334155;
    font-size: 0.95rem;
}

/* 1. Visible */
.box-visible {
    overflow: visible;
}

/* 2. Hidden */
.box-hidden {
    overflow: hidden;
}

/* 3. Scroll */
.box-scroll {
    overflow: scroll;
}

/* 4. Auto */
.box-auto {
    overflow: auto;
}

footer {
    text-align: center;
    padding: 1.5rem;
    color: #64748b;
    font-size: 0.875rem;
    border-top: 1px solid #e2e8f0;
    margin-top: 2rem;
}
Markdown
# Overflow Values Explanation & Layout Fix

1. **`overflow: visible`**: The default behavior. Overflowing content spills outside the box boundaries and can overlap adjacent layout elements.
2. **`overflow: hidden`**: Clips overflowing content cleanly at the box boundary. Any text or images beyond the fixed height are completely hidden from view.
3. **`overflow: scroll`**: Forces horizontal or vertical scrollbars to render on the container at all times, regardless of whether the content actually exceeds the height.
4. **`overflow: auto`**: Dynamically checks content height. Scrollbars appear only when content overflows, providing a clean user interface.
5. **Layout Fix**: When elements overflow unexpectedly (such as long text or floated items breaking o
