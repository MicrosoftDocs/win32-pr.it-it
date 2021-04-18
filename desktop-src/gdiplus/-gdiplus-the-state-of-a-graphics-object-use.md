---
description: La classe Graphics è il nucleo di Windows GDI+. Per creare qualsiasi elemento, è necessario creare un oggetto graphics, impostarne le proprietà e chiamarne i metodi (DrawLine, DrawImage, DrawString e like).
ms.assetid: 7d70f9fe-c0b2-4d65-815d-483d06df96ad
title: Stato di un oggetto Graphics
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 661733f944b08633b5df84eed3ac488e612d9e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550413"
---
# <a name="the-state-of-a-graphics-object"></a>Stato di un oggetto Graphics

La classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) è il nucleo di Windows GDI+. Per creare qualsiasi elemento, è necessario creare un oggetto **Graphics** , impostarne le proprietà e chiamarne i metodi ( [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)), [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))e like).

L'esempio seguente crea un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e un oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) , quindi chiama il metodo [**Graphics::D rawrectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) dell'oggetto **Graphics** :


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



Nel codice precedente, il metodo [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) restituisce un handle a un contesto di dispositivo e tale handle viene passato al costruttore [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Un contesto di dispositivo è una struttura (gestita da Windows) che include informazioni sul dispositivo di visualizzazione specifico usato.

## <a name="graphics-state"></a>Stato grafica

Un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) non fornisce metodi di disegno, ad esempio [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) e [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)). Un oggetto **Graphics** gestisce anche lo stato della grafica, che può essere suddiviso nelle categorie seguenti:

-   Collegamento a un contesto di dispositivo
-   Impostazioni qualità
-   Trasformazioni
-   Area di visualizzazione

### <a name="device-context"></a>Contesto di dispositivo

In qualità di programmatore di applicazioni, non è necessario pensare all'interazione tra un oggetto [**grafico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e il relativo contesto di dispositivo. Questa interazione viene gestita da GDI+ dietro le quinte.

### <a name="quality-settings"></a>Impostazioni qualità

Un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) dispone di diverse proprietà che influiscono sulla qualità degli elementi disegnati sullo schermo. Per visualizzare e modificare queste proprietà, è possibile chiamare i metodi get e set. Ad esempio, è possibile chiamare il metodo [**Graphics:: SetTextRenderingHint**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) per specificare il tipo di anti-aliasing, se presente, applicato al testo. Altri metodi set che influenzano la qualità sono [**Graphics:: SetSmoothingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode), [**Graphics:: SetCompositingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingmode), [**Graphics:: SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality)e [**Graphics:: SetInterpolationMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setinterpolationmode).

Nell'esempio seguente vengono disegnati due ellissi, uno con la modalità di smussatura impostata su [* * * * SmoothingModeAntiAlias * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) * * e uno con la modalità di smussatura impostata su [* * * * SmoothingModeHighSpeed * * * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode):


```
Graphics graphics(hdc);
Pen pen(Color(255, 0, 255, 0));  // opaque green

graphics.SetSmoothingMode(SmoothingModeAntiAlias);
graphics.DrawEllipse(&pen, 0, 0, 200, 100);
graphics.SetSmoothingMode(SmoothingModeHighSpeed);
graphics.DrawEllipse(&pen, 0, 150, 200, 100);
```



### <a name="transformations"></a>Trasformazioni

Un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) gestisce due trasformazioni (mondo e pagina) che vengono applicate a tutti gli elementi disegnati da tale oggetto **grafico** . Qualsiasi trasformazione affine può essere archiviata nella trasformazione globale. Le trasformazioni affini includono il ridimensionamento, la rotazione, la reflection, la distorsione e la conversione. La trasformazione pagina può essere utilizzata per la scalabilità e per la modifica delle unità, ad esempio da pixel a pollici. Per ulteriori informazioni sulle trasformazioni, vedere [sistemi di coordinate e trasformazioni](-gdiplus-coordinate-systems-and-transformations-about.md).

Nell'esempio seguente vengono impostate le trasformazioni globali e di pagina di un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . La trasformazione globale è impostata su una rotazione di 30 gradi. La trasformazione pagina viene impostata in modo che le coordinate passate alla seconda [**grafica::D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) verranno considerate millimetri anziché pixel. Il codice effettua due chiamate identiche all'oggetto **Graphics::D Metodo rawellipse** . La trasformazione globale viene applicata alla prima **grafica::D chiamata rawellipse** e entrambe le trasformazioni (mondo e pagina) vengono applicate alla seconda **grafica::D chiamata rawellipse** .


```
Graphics graphics(hdc);
Pen pen(Color(255, 255, 0, 0));

graphics.ResetTransform();
graphics.RotateTransform(30.0f);            // World transformation
graphics.DrawEllipse(&pen, 30, 0, 50, 25);
graphics.SetPageUnit(UnitMillimeter);       // Page transformation
graphics.DrawEllipse(&pen, 30, 0, 50, 25);
```



Nella figura seguente sono illustrati i due ellissi. Si noti che la rotazione di 30 gradi riguarda l'origine del sistema di coordinate (angolo superiore sinistro dell'area client), non dei centri dei puntini di sospensione. Si noti inoltre che la larghezza della penna di 1 indica 1 pixel per la prima ellisse e 1 millimetro per la seconda ellisse.

![Screenshot di una finestra contenente una piccola ellisse, un'ellisse sottile e un'ellisse grande e più spessa](images/graphicsascon1.png)

 

### <a name="clipping-region"></a>Area di visualizzazione

Un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) mantiene un'area di ridimensionamento che si applica a tutti gli elementi disegnati da tale oggetto **grafico** . È possibile impostare l'area di ridimensionamento chiamando il metodo [seclip](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) .

Nell'esempio seguente viene creata un'area con più forme formando l'Unione di due rettangoli. Tale area viene designata come area di visualizzazione di un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Il codice disegna quindi due righe limitate all'interno dell'area di visualizzazione.


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



Nella figura seguente sono illustrate le linee ritagliate.

![illustrazione che mostra una forma colorata incrociata da due linee rosse diagonali](images/graphicsascon2.png)

 

 
