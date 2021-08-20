---
description: La classe Graphics è il centro della Windows GDI+. Per disegnare qualsiasi elemento, crea un oggetto Graphics, ne imposta le proprietà e chiama i relativi metodi ( DrawLine, DrawImage, DrawString e simili).
ms.assetid: 7d70f9fe-c0b2-4d65-815d-483d06df96ad
title: Stato di un oggetto Graphics
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f68a2ba754aadc1f7d2572dcbc2ac40d08d7fe95d382ce60511cd72d441bb80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977331"
---
# <a name="the-state-of-a-graphics-object"></a>Stato di un oggetto Graphics

La [**classe Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) è alla base della Windows GDI+. Per disegnare qualsiasi elemento, crea un **oggetto Graphics,** ne imposta le proprietà e chiama i relativi metodi ( [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)), [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))e simili).

L'esempio seguente costruisce un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e un oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) e quindi chiama il [**metodo Graphics::D rawRectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) dell'oggetto **Graphics:**


```
HDC          hdc;
PAINTSTRUCT  ps;

hdc = BeginPaint(hWnd, &ps);
{
   Graphics graphics(hdc);
   Pen pen(Color(255, 0, 0, 255));  // opaque blue
   graphics.DrawRectangle(&pen, 10, 10, 200, 100);
}
EndPaint(hWnd, &ps);
```



Nel codice precedente il metodo [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) restituisce un handle a un contesto di dispositivo e tale handle viene passato al [**costruttore Graphics.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Un contesto di dispositivo è una struttura (gestita da Windows) che contiene informazioni sul dispositivo di visualizzazione specifico in uso.

## <a name="graphics-state"></a>Stato grafica

Un [**oggetto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) non fornisce metodi di disegno, ad esempio [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) [e DrawRectangle.](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) Un **oggetto Graphics** mantiene anche lo stato grafico, che può essere suddiviso nelle categorie seguenti:

-   Collegamento a un contesto di dispositivo
-   Impostazioni di qualità
-   Trasformazioni
-   Area di ritaglio

### <a name="device-context"></a>Contesto di dispositivo

I programmatori di applicazioni non devono pensare all'interazione tra un [**oggetto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e il relativo contesto di dispositivo. Questa interazione viene gestita da GDI+ in background.

### <a name="quality-settings"></a>Qualità Impostazioni

Un [**oggetto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) ha diverse proprietà che influiscono sulla qualità degli elementi disegnati sullo schermo. È possibile visualizzare e modificare queste proprietà chiamando i metodi get e set. Ad esempio, è possibile chiamare il [**metodo Graphics::SetTextRenderingHint**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) per specificare il tipo di anti-aliasing (se presente) applicato al testo. Altri metodi set che influenzano la qualità sono [**Graphics::SetSmoothingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode), [**Graphics::SetCompositingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingmode), [**Graphics::SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality)e [**Graphics::SetInterpolationMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setinterpolationmode).

L'esempio seguente disegna due puntini di sospensione, una con la modalità smoothing impostata su [****SmoothingModeAntiAlias***](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) e una con la modalità di smussamento impostata su [****SmoothingModeHighSpeed****](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode):


```
Graphics graphics(hdc);
Pen pen(Color(255, 0, 255, 0));  // opaque green

graphics.SetSmoothingMode(SmoothingModeAntiAlias);
graphics.DrawEllipse(&pen, 0, 0, 200, 100);
graphics.SetSmoothingMode(SmoothingModeHighSpeed);
graphics.DrawEllipse(&pen, 0, 150, 200, 100);
```



### <a name="transformations"></a>Trasformazioni

Un [**oggetto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) mantiene due trasformazioni (world e page) che vengono applicate a tutti gli elementi disegnati da tale oggetto **Graphics.** Qualsiasi trasformazione affine può essere archiviata nella trasformazione globale. Le trasformazioni affine includono il ridimensionamento, la rotazione, la riflessione, l'inclinazione e la traduzione. La trasformazione della pagina può essere usata per il ridimensionamento e per la modifica delle unità (ad esempio, da pixel a pollici). Per altre informazioni sulle trasformazioni, vedere [Sistemi di coordinate e trasformazioni.](-gdiplus-coordinate-systems-and-transformations-about.md)

Nell'esempio seguente vengono impostate le trasformazioni globale e di pagina di un [**oggetto Graphics.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) La trasformazione globale è impostata su una rotazione di 30 gradi. La trasformazione della pagina viene impostata in modo che le coordinate passate al secondo [**oggetto Graphics::D rawEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) siano considerate come millimetri anziché pixel. Il codice esegue due chiamate identiche al **metodo Graphics::D rawEllipse.** La trasformazione globale viene applicata alla prima chiamata **Graphics::D rawEllipse** ed entrambe le trasformazioni (world e page) vengono applicate alla seconda chiamata **Graphics::D rawEllipse.**


```
Graphics graphics(hdc);
Pen pen(Color(255, 255, 0, 0));

graphics.ResetTransform();
graphics.RotateTransform(30.0f);            // World transformation
graphics.DrawEllipse(&pen, 30, 0, 50, 25);
graphics.SetPageUnit(UnitMillimeter);       // Page transformation
graphics.DrawEllipse(&pen, 30, 0, 50, 25);
```



La figura seguente mostra i due puntini di sospensione. Si noti che la rotazione di 30 gradi riguarda l'origine del sistema di coordinate (angolo superiore sinistro dell'area client), non i centri dei puntini di sospensione. Si noti anche che lo spessore della penna di 1 indica 1 pixel per la prima ellisse e 1 millimetro per la seconda ellisse.

![screenshot di una finestra contenente un'ellisse piccola e sottile e un'ellisse grande e più spesso](images/graphicsascon1.png)

 

### <a name="clipping-region"></a>Area di ritaglio

Un [**oggetto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) mantiene un'area di ritaglio che si applica a tutti gli elementi disegnati da tale **oggetto** Graphics. Puoi impostare l'area di ritaglio chiamando il [metodo SetClip.](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode))

L'esempio seguente crea un'area a forma di segno più formando l'unione di due rettangoli. Tale area è designata come area di ritaglio di un [**oggetto Graphics.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Il codice disegna quindi due linee limitate all'interno dell'area di ritaglio.


```
Graphics graphics(hdc);
Pen pen(Color(255, 255, 0, 0), 5);  // opaque red, width 5
SolidBrush brush(Color(255, 180, 255, 255));  // opaque aqua

// Create a plus-shaped region by forming the union of two rectangles.
Region region(Rect(50, 0, 50, 150));
region.Union(Rect(0, 50, 150, 50));
graphics.FillRegion(&brush, &region);

// Set the clipping region.
graphics.SetClip(&region);

// Draw two clipped lines.
graphics.DrawLine(&pen, 0, 30, 150, 160);
graphics.DrawLine(&pen, 40, 20, 190, 150);
```



La figura seguente mostra le linee ritagliate.

![illustrazione che mostra una forma colorata attraversata da due linee rosse diagonali](images/graphicsascon2.png)

 

 
