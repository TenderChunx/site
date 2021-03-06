---
layout: page
title: Designer
namespace: Freesewing\Themes\Core
tags: [class docs]
permalink: /docs/core/classdocs/themes/core/designer
---
## Description 

The [`Designer`](designer) theme is a theme specifically for pattern designers.

It specifically adds a number of things to the pattern:

- Debug output for points: Place a marker on each point, hovering shows point info in browser console.
- Debug output for paths: Connect bezier control points with their origin.
- It optionally marks points listed in the `markPoints` request parameter.

## Example 

{% include coreClassdocsFigure.html
    description="You will need to open this in its own window to see the hover effect on points"
    params="service=draft&pattern=AaronAshirt&theme=Designer"
%}

## Public methods

### themePattern

```php?start_inline=1
void themePattern(
    \Freesewing\Pattern $pattern
)
```

This is where, as a theme designer, you theme the [`Pattern`](../../patterns/core/pattern) object.

This [`Designer`](designer) theme overrides [`Theme::themePattern`](theme#themepattern) to
add the extra debug info that is useful for pattern designers.

#### Typical use
{:.no_toc}
Called by the service classes after the pattern is drafted/sampled, but before it's rendered.

#### Parameters
{:.no_toc}

- [`Pattern`](../../patterns/core/pattern) `$pattern` : The pattern object to theme.

## See also

The [`Theme`](theme) parent class.

{% include classFooter.html %}
* TOC - Do not remove this line
{:toc}
