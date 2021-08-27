---
description: Windows GDI+ fornisce contenitori che è possibile usare per sostituire o aumentare temporaneamente parte dello stato in un oggetto Graphics.
ms.assetid: f3fce8ef-903a-4b9d-b76c-562739d02eb3
title: Contenitori di oggetti Graphics annidati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d88b3a768e5b156eb5d28410ad69d58227e9660618764ca4b084b5e35662b839
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114981"
---
# <a name="nested-graphics-containers"></a>Contenitori di oggetti Graphics annidati

Windows GDI+ fornisce contenitori che è possibile usare per sostituire o aumentare temporaneamente parte dello stato in un [**oggetto**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Graphics. Per creare un contenitore, chiamare il [**metodo Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) di un **oggetto Graphics.** È possibile chiamare **Ripetutamente Graphics::BeginContainer** per formare contenitori annidati.

## <a name="transformations-in-nested-containers"></a>Trasformazioni in contenitori annidati

L'esempio seguente crea un [**oggetto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e un contenitore all'interno di tale **oggetto Graphics.** La trasformazione globale **dell'oggetto Graphics** è una traslazione di 100 unità nella direzione x e di 80 unità nella direzione y. La trasformazione globale del contenitore è una rotazione di 30 gradi. Il codice effettua la chiamata


```
DrawRectangle(&pen, -60, -30, 120, 60)
```



Due volte. La prima chiamata a [**Graphics::D rawRectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) si trova *all'interno del contenitore*; ciò significa che la chiamata è tra le chiamate a [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) [**e Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer). La seconda chiamata a **Graphics::D rawRectangle** è dopo la chiamata a **Graphics::EndContainer.**


```
Graphics           graphics(hdc);
Pen                pen(Color(255, 255, 0, 0));
GraphicsContainer  graphicsContainer;

graphics.TranslateTransform(100.0f, 80.0f);

graphicsContainer = graphics.BeginContainer();
   graphics.RotateTransform(30.0f);
   graphics.DrawRectangle(&pen, -60, -30, 120, 60);
graphics.EndContainer(graphicsContainer);

graphics.DrawRectangle(&pen, -60, -30, 120, 60);
```



Nel codice precedente, il rettangolo disegnato dall'interno del contenitore viene trasformato prima dalla trasformazione globale del contenitore (rotazione) e quindi dalla trasformazione globale dell'oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) (traslazione). Il rettangolo disegnato dall'esterno del contenitore viene trasformato solo dalla trasformazione globale **dell'oggetto Graphics** (traslazione). La figura seguente mostra i due rettangoli.

![screenshot di una finestra con due rettangoli rossi centrati sullo stesso punto, ma con rotazioni diverse](images/nestedcontainers1.png)

 

## <a name="clipping-in-nested-containers"></a>Ritaglio in contenitori annidati

L'esempio seguente illustra come i contenitori annidati gestiscono le aree di ritaglio. Il codice crea un [**oggetto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e un contenitore all'interno di tale **oggetto Graphics.** L'area di ritaglio **dell'oggetto Graphics** è un rettangolo e l'area di ritaglio del contenitore è un'ellisse. Il codice effettua due chiamate al [**metodo Graphics::D rawLine.**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) La prima chiamata a **Graphics::D rawLine** si trova all'interno del contenitore e la seconda chiamata **a Graphics::D rawLine** si trova all'esterno del contenitore (dopo la chiamata a [**Graphics::EndContainer).**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) La prima riga viene ritagliata in base all'intersezione delle due aree di ritaglio. La seconda riga viene ritagliata solo dall'area di ritaglio rettangolare **dell'oggetto** Graphics.


```
Graphics           graphics(hdc);
GraphicsContainer  graphicsContainer;
Pen                redPen(Color(255, 255, 0, 0), 2);
Pen                bluePen(Color(255, 0, 0, 255), 2);
SolidBrush         aquaBrush(Color(255, 180, 255, 255));
SolidBrush         greenBrush(Color(255, 150, 250, 130));

graphics.SetClip(Rect(50, 65, 150, 120));
graphics.FillRectangle(&aquaBrush, 50, 65, 150, 120);

graphicsContainer = graphics.BeginContainer();
   // Create a path that consists of a single ellipse.
   GraphicsPath path;
   path.AddEllipse(75, 50, 100, 150);

  // Construct a region based on the path.
   Region region(&path);
   graphics.FillRegion(&greenBrush, &region);

   graphics.SetClip(&region);
   graphics.DrawLine(&redPen, 50, 0, 350, 300);
graphics.EndContainer(graphicsContainer);

graphics.DrawLine(&bluePen, 70, 0, 370, 300);
```



La figura seguente mostra le due linee ritagliate.

![illustrazione di un'ellisse all'interno di un rettangolo, con una linea ritagliata dall'ellisse e l'altra dal rettangolo](images/nestedcontainers2.png)

Come illustrato nei due esempi precedenti, le trasformazioni e le aree di ritaglio sono cumulative in contenitori annidati. Se si impostano le trasformazioni world del contenitore e dell'oggetto [**Graphics,**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) entrambe le trasformazioni verranno applicate agli elementi disegnati dall'interno del contenitore. La trasformazione del contenitore verrà applicata per prima e la trasformazione **dell'oggetto Graphics** verrà applicata per seconda. Se si impostano le aree di ritaglio del contenitore e dell'oggetto **Graphics,** gli elementi disegnati dall'interno del contenitore verranno ritagliati dall'intersezione delle due aree di ritaglio.

## <a name="quality-settings-in-nested-containers"></a>Qualità Impostazioni nei contenitori annidati

Le impostazioni di qualità ( [**SmoothingMode,**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) [**TextRenderingHint**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)e simili) nei contenitori annidati non sono cumulative; al contrario, le impostazioni di qualità del contenitore sostituiscono temporaneamente le impostazioni di qualità di un [**oggetto**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Graphics. Quando si crea un nuovo contenitore, le impostazioni di qualità per tale contenitore vengono impostate su valori predefiniti. Si supponga, ad esempio, di avere un oggetto **Graphics** con una modalità di [smussamento ****SmoothingModeAntiAlias****.](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) Quando si crea un contenitore, la modalità di smussamento all'interno del contenitore è la modalità di smussamento predefinita. È possibile impostare la modalità di smussamento del contenitore e tutti gli elementi estratti dall'interno del contenitore verranno disegnati in base alla modalità impostata. Gli elementi disegnati dopo la chiamata a [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) verranno disegnati in base alla modalità di smussamento ([****SmoothingModeAntiAlias****](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)) attivata prima della chiamata a [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).

## <a name="several-layers-of-nested-containers"></a>Diversi livelli di contenitori annidati

Non si è limitati a un solo contenitore in un [**oggetto**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Graphics. È possibile creare una sequenza di contenitori, ognuno annidato nel precedente, e specificare le impostazioni di trasformazione globale, area di ritaglio e qualità di ognuno di questi contenitori annidati. Se si chiama un metodo di disegno dall'interno del contenitore più interno, le trasformazioni verranno applicate in ordine, a partire dal contenitore più interno e terminando con il contenitore più esterno. Gli elementi disegnati dall'interno del contenitore più interno verranno ritagliati in base all'intersezione di tutte le aree di ritaglio.

L'esempio seguente crea un [**oggetto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e imposta l'hint per il rendering del testo su [****TextRenderingHintAntiAlias****.](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint) Il codice crea due contenitori, uno annidato all'interno dell'altro. L'hint per il rendering del testo del contenitore esterno è impostato su [****TextRenderingHintSingleBitPerPixel***](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)e l'hint per il rendering del testo del contenitore interno è impostato su [****TextRenderingHintAntiAlias****.](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint) Il codice disegna tre stringhe: una dal contenitore interno, una dal contenitore esterno e una **dall'oggetto Graphics** stesso.


```
Graphics graphics(hdc);
GraphicsContainer innerContainer;
GraphicsContainer outerContainer;
SolidBrush brush(Color(255, 0, 0, 255));
FontFamily fontFamily(L"Times New Roman");
Font font(&fontFamily, 36, FontStyleRegular, UnitPixel);

graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);

outerContainer = graphics.BeginContainer();

   graphics.SetTextRenderingHint(TextRenderingHintSingleBitPerPixel);

   innerContainer = graphics.BeginContainer();
      graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
      graphics.DrawString(L"Inner Container", 15, &font,
         PointF(20, 10), &brush);
   graphics.EndContainer(innerContainer);

   graphics.DrawString(L"Outer Container", 15, &font, PointF(20, 50), &brush);

graphics.EndContainer(outerContainer);

graphics.DrawString(L"Graphics Object", 15, &font, PointF(20, 90), &brush);
```



La figura seguente mostra le tre stringhe. Le stringhe disegnate dal contenitore interno e [**dall'oggetto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) vengono smussate dall'antialiasing. La stringa disegnata dal contenitore esterno non viene smussata dall'antialiasing a causa dell'impostazione TextRenderingHintSingleBitPerPixel.

![illustrazione di un rettangolo contenente la stessa stringa in alcuni casi; solo i caratteri nella prima e nell'ultima riga sono uniformi](images/nestedcontainers3.png)

 

 
