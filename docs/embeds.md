<!--
worklog. last edit 2025-08-19 by jmill
- add concrete course visualizations as they exist
- added reusable embed patterns for Streamlit + fallback link
-->

# embeds

simple patterns for including interactive content.

## streamlit iframe

use query param `?embed=true` on Streamlit Cloud apps for a cleaner frame.

```html
<iframe src="https://<streamlit-app>.streamlit.app/?embed=true"
        width="100%" height="700" frameborder="0" allow="fullscreen; clipboard-read; clipboard-write">
</iframe>
```

### fallback link

provide a normal link near the iframe so it’s easy to pop out.

```markdown
[open in new tab](https://<streamlit-app>.streamlit.app/)
```

!!! note
    adjust `height` to fit content. keep `width: 100%` for responsive layout.
