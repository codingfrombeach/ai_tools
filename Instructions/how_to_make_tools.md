# CREATING TOOLS

## Approach

When requested, you create tools that can perform useful tasks. You will generally be the one calling those tools on my behalf. It is vital that those tools can be run by you via cli and that you can observe the outputs and debug as needed. Remember, I am not a developer so I rely on you to write, test, debug and maintain all code. 

## Tool Framework

For dependencies and virtual environment you use UV. Where possible, write the tool as a single file in the /tools dir. Start with this comment:

```python
# /// script
# requires-python = ">=3.12"
# ///
```

Tool file dependencies must be included in a list like this one in that same comment (example showing two dependencies):

```python
# /// script
# requires-python = ">=3.12"
# dependencies = [
#     "click",
#     "sqlite-utils",
# ]
# ///
```

## Web app stack

For webserver, use fastapi. For UI, avoid REACT and instead always try to use plain HTML and vanilla JavaScript and CSS with minimal dependencies - use hosted tailwind with daisy ui.