def badge(label, value, color, path="badge.svg"):
    w1, w2 = 8 * len(label) + 20, 8 * len(value) + 20
    svg = f"""<svg xmlns="http://www.w3.org/2000/svg" width="{w1 + w2}" height="28">
  <rect width="{w1}" height="28" rx="4" fill="#24292F"/>
  <rect x="{w1}" width="{w2}" height="28" rx="4" fill="{color}"/>
  <g fill="#fff" font-family="Verdana,sans-serif" font-size="12" text-anchor="middle">
    <text x="{w1 / 2}" y="18">{label}</text>
    <text x="{w1 + w2 / 2}" y="18">{value}</text>
  </g>
</svg>"""
    open(path, "w").write(svg)

badge("palette", "neon night", "#7B2FF7")# SVG-badge-generator
