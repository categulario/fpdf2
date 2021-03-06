# Shapes #

The following code snippets show examples of rendering various shapes.

## Lines ##

Draw a thin plain orange line:
```python
from fpdf import FPDF

pdf = FPDF()
pdf.add_page()
pdf.set_line_width(0.5)
pdf.set_draw_color(r=255, g=128, b=0)
pdf.line(x1=50, y1=50, x2=150, y2=100)
pdf.output("orange_plain_line.pdf")
```

Draw a dashed light blue line:
```python
from fpdf import FPDF

pdf = FPDF()
pdf.add_page()
pdf.set_line_width(0.5)
pdf.set_draw_color(r=0, g=128, b=255)
pdf.dashed_line(x1=50, y1=50, x2=150, y2=100, dash_length=2, space_length=3)
pdf.output("blue_dashed_line.pdf")
```

## Ellipse ##

Draw a circle filled in grey with a pink outline:
```python
from fpdf import FPDF

pdf = FPDF()
pdf.add_page()
pdf.set_line_width(2)
pdf.set_draw_color(r=230, g=30, b=180)
pdf.set_fill_color(240)
pdf.ellipse(x=50, y=50, w=50, h=50, style="FD")
pdf.output("circle.pdf")
```

## Rectangle ##

Draw nested squares:
```python
from fpdf import FPDF

pdf = FPDF()
pdf.add_page()
for i in range(15):
    pdf.set_fill_color(255 - 15*i)
    pdf.rect(x=5+5*i, y=5+5*i, w=200-10*i, h=200-10*i, style="FD")
pdf.output("squares.pdf")
```
