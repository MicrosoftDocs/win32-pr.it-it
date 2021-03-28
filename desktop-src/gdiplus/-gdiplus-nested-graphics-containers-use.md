---
description: In Windows GDI+ sono disponibili contenitori che è possibile utilizzare per sostituire temporaneamente o aumentare parte dello stato in un oggetto Graphics.
ms.assetid: f3fce8ef-903a-4b9d-b76c-562739d02eb3
title: Contenitori di oggetti Graphics annidati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29f9d9feac3494b423d844cb1e3da359af33eaec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967202"
---
# <a name="nested-graphics-containers"></a>Contenitori di oggetti Graphics annidati

In Windows GDI+ sono disponibili contenitori che è possibile utilizzare per sostituire temporaneamente o aumentare parte dello stato in un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Per creare un contenitore, chiamare il metodo [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) di un oggetto **Graphics** . È possibile chiamare **Graphics:: BeginContainer** ripetutamente per creare contenitori nidificati.

## <a name="transformations-in-nested-containers"></a>Trasformazioni nei contenitori annidati

Nell'esempio seguente vengono creati un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e un contenitore all'interno dell'oggetto **Graphics** . La trasformazione globale dell'oggetto **Graphics** è una conversione di unità 100 nella direzione x e 80 unità nella direzione y. La trasformazione globale del contenitore è una rotazione di 30 gradi. Il codice effettua la chiamata


```
DrawRectangle(&pen, -60, -30, 120, 60)
```



doppio. La prima chiamata a [**Graphics::D rawrectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) si trova *all'interno del contenitore*; ovvero la chiamata è tra le chiamate a [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) e [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer). La seconda chiamata a **Graphics::D rawrectangle** è successiva alla chiamata a **Graphics:: EndContainer**.


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



Nel codice precedente, il rettangolo disegnato dall'interno del contenitore viene trasformato prima dalla trasformazione globale del contenitore (rotazione), quindi dalla trasformazione globale dell'oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) (Translation). Il rettangolo disegnato dall'esterno del contenitore viene trasformato solo dalla trasformazione globale dell'oggetto **Graphics** (Translation). Nella figura seguente sono illustrati i due rettangoli.

![Screenshot di una finestra con due rettangoli rossi centrati nello stesso punto, ma con rotazioni diverse](images/nestedcontainers1.png)

 

## <a name="clipping-in-nested-containers"></a>Ritaglio in contenitori annidati

Nell'esempio seguente viene illustrato il modo in cui i contenitori nidificati gestiscono le aree di ritaglio. Il codice crea un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e un contenitore all'interno dell'oggetto **Graphics** . L'area di visualizzazione dell'oggetto **Graphics** è un rettangolo e l'area di visualizzazione del contenitore è un'ellisse. Il codice effettua due chiamate al metodo [**Graphics::D rawline**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) . La prima chiamata a **Graphics::D rawline** si trova all'interno del contenitore e la seconda chiamata a **Graphics::D rawline** è esterna al contenitore (dopo la chiamata a [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)). La prima riga viene ritagliata dall'intersezione delle due aree di ritaglio. La seconda riga viene troncata solo dall'area di ridimensionamento rettangolare dell'oggetto **Graphics** .


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



Nella figura seguente sono illustrate le due righe ritagliate.

![illustrazione di un'ellisse all'interno di un rettangolo, con una riga ritagliata dall'ellisse e l'altra dal rettangolo](images/nestedcontainers2.png)

Come illustrato nei due esempi precedenti, le trasformazioni e le aree di ridimensionamento sono cumulative nei contenitori nidificati. Se si impostano le trasformazioni globali del contenitore e dell'oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , entrambe le trasformazioni verranno applicate agli elementi disegnati dall'interno del contenitore. La trasformazione del contenitore verrà applicata per prima e la trasformazione dell'oggetto **Graphics** verrà applicata secondo. Se si impostano le aree di visualizzazione del contenitore e l'oggetto **Graphics** , gli elementi disegnati dall'interno del contenitore verranno ritagliati dall'intersezione delle due aree di ridimensionamento.

## <a name="quality-settings-in-nested-containers"></a>Impostazioni di qualità nei contenitori annidati

Le impostazioni di qualità ( [**SmoothingMode**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode), [**TextRenderingHint**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)e like) nei contenitori annidati non sono cumulative. piuttosto, le impostazioni di qualità del contenitore sostituiscono temporaneamente le impostazioni di qualità di un oggetto [**grafico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Quando si crea un nuovo contenitore, le impostazioni di qualità per il contenitore sono impostate sui valori predefiniti. Si supponga, ad esempio, di avere un oggetto **Graphics** con una modalità di smussatura di * * * [* SmoothingModeAntiAlias * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)* *. Quando si crea un contenitore, la modalità di smussatura all'interno del contenitore è la modalità di smussatura predefinita. È possibile impostare la modalità di smussatura del contenitore e tutti gli elementi disegnati dall'interno del contenitore verranno disegnati in base alla modalità impostata. Gli elementi disegnati dopo la chiamata a [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) verranno disegnati in base alla modalità di smussamento ([* * * * SmoothingModeAntiAlias * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)* *) che era presente prima della chiamata a [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).

## <a name="several-layers-of-nested-containers"></a>Diversi livelli di contenitori annidati

Non si è limitati a un contenitore in un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . È possibile creare una sequenza di contenitori, ognuno nidificato nell'oggetto precedente, ed è possibile specificare la trasformazione globale, l'area di ridimensionamento e le impostazioni di qualità di ognuno di questi contenitori annidati. Se si chiama un metodo Drawing dall'interno del contenitore più interno, le trasformazioni verranno applicate in ordine, a partire dal contenitore più interno e terminando con il contenitore più esterno. Gli elementi disegnati dall'interno del contenitore più interno verranno ritagliati dall'intersezione di tutte le aree di ridimensionamento.

Nell'esempio seguente viene creato un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e ne viene impostato l'hint per il rendering del testo su * * * [* TextRenderingHintAntiAlias * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)* *. Il codice crea due contenitori, uno annidato all'interno dell'altro. L'hint per il rendering del testo del contenitore esterno è impostato su [* * * * TextRenderingHintSingleBitPerPixel * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)* * e l'hint per il rendering del testo del contenitore interno è impostato su [* * * * TextRenderingHintAntiAlias * * * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint). Il codice disegna tre stringhe: una dal contenitore interno, una dal contenitore esterno e una dall'oggetto **Graphics** stesso.


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



Nella figura seguente sono illustrate le tre stringhe. Le stringhe disegnate dal contenitore interno e dall'oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) sono smussate mediante l'anti-aliasing. La stringa disegnata dal contenitore esterno non è smussata mediante l'anti-aliasing a causa dell'impostazione TextRenderingHintSingleBitPerPixel.

![illustrazione di un rettangolo contenente la stessa stringa. solo i caratteri nella prima e nell'ultima riga sono uniformi](images/nestedcontainers3.png)

 

 
