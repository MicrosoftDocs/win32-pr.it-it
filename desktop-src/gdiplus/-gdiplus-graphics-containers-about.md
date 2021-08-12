---
description: Lo stato della &8212; l'area di ritaglio, le trasformazioni e le impostazioni \# di qualità &8212; viene archiviato in un \# oggetto Graphics.
ms.assetid: 98b9fa12-02e7-42bf-9cbd-03ee696188f6
title: Contenitori di oggetti Graphics
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26af00a17f793a1f3ce587963343556b8c4ad685f930b707bd81de1008d610ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118248670"
---
# <a name="graphics-containers"></a>Contenitori di oggetti Graphics

Lo stato della grafica, ovvero l'area di ritaglio, le trasformazioni e le impostazioni di qualità, viene archiviato in un [**oggetto**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Graphics. Windows GDI+ consente di sostituire o aumentare temporaneamente parte dello stato in un **oggetto Graphics** usando un contenitore. Si avvia un contenitore chiamando il [**metodo Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) di un oggetto **Graphics** e si termina un contenitore chiamando il [**metodo Graphics::EndContainer.**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) Tra **Graphics::BeginContainer** e **Graphics::EndContainer,** tutte le modifiche di stato apportate all'oggetto **Graphics** appartengono al contenitore e non sovrascrivono lo stato esistente dell'oggetto **Graphics.**

L'esempio seguente crea un contenitore all'interno di [**un oggetto**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Graphics. La trasformazione globale **dell'oggetto Graphics** è una traslazione di 200 unità a destra e la trasformazione globale del contenitore è una traslazione di 100 unità verso il basso.


```
myGraphics.TranslateTransform(200.0f, 0.0f);

myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.TranslateTransform(0.0f, 100.0f);
   myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50);
myGraphics.EndContainer(myGraphicsContainer);

myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50);
```



Si noti che nell'esempio precedente l'istruzione effettuata tra le chiamate `myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50)` a [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) e [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) produce un rettangolo diverso rispetto alla stessa istruzione effettuata dopo la chiamata a **Graphics::EndContainer**. Solo la traslazione orizzontale si applica **alla chiamata DrawRectangle** effettuata all'esterno del contenitore. Entrambe le trasformazioni, ovvero la traslazione orizzontale di 200 unità e la traslazione verticale di 100 unità, si applicano alla chiamata [**Graphics::D rawRectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) effettuata all'interno del contenitore. La figura seguente mostra i due rettangoli.

![screenshot di una finestra con due rettangoli disegnati con una penna blu, uno posizionato sopra l'altro](images/aboutgdip05-art17.png)

I contenitori possono essere annidati all'interno di contenitori. L'esempio seguente crea un contenitore all'interno [**di un oggetto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e un altro contenitore all'interno del primo contenitore. La trasformazione globale **dell'oggetto Graphics** è una traslazione di 100 unità nella direzione x e di 80 unità nella direzione y. La trasformazione globale del primo contenitore è una rotazione di 30 gradi. La trasformazione globale del secondo contenitore è un ridimensionamento di un fattore di 2 nella direzione x. Una chiamata al metodo [**Graphics::D rawEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) viene effettuata all'interno del secondo contenitore.


```
myGraphics.TranslateTransform(100.0f, 80.0f, MatrixOrderAppend);

container1 = myGraphics.BeginContainer();
   myGraphics.RotateTransform(30.0f, MatrixOrderAppend);

   container2 = myGraphics.BeginContainer();
      myGraphics.ScaleTransform(2.0f, 1.0f);
      myGraphics.DrawEllipse(&myPen, -30, -20, 60, 40);
   myGraphics.EndContainer(container2);

myGraphics.EndContainer(container1);
```



La figura seguente mostra i puntini di sospensione.

![Screenshot di una finestra che contiene un'ellisse blu ruotata con il centro etichettato come (100,80)](images/aboutgdip05-art18.png)

Si noti che tutte e tre le trasformazioni si applicano alla chiamata [**Graphics::D rawEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) eseguita nel secondo contenitore (più interno). Si noti anche l'ordine delle trasformazioni: prima ridimensionare, quindi ruotare e infine traslare. La trasformazione più interna viene applicata per prima e la trasformazione più esterna viene applicata per ultima.

Qualsiasi proprietà di un [**oggetto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) può essere impostata all'interno di un contenitore (tra le chiamate a [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) [**e Graphics::EndContainer).**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) Ad esempio, un'area di ritaglio può essere impostata all'interno di un contenitore. Qualsiasi disegno eseguito all'interno del contenitore sarà limitato all'area di ritaglio del contenitore e sarà limitato anche alle aree di ritaglio di tutti i contenitori esterni e all'area di ritaglio dell'oggetto **Graphics** stesso.

Le proprietà descritte finora, ovvero la trasformazione globale e l'area di ritaglio, sono combinate da contenitori annidati. Altre proprietà vengono temporaneamente sostituite da un contenitore annidato. Ad esempio, se si imposta la modalità di smussamento su SmoothingModeAntiAlias all'interno di un contenitore, tutti i metodi di disegno chiamati all'interno di tale contenitore useranno la modalità di smussamento antialias, mentre i metodi di disegno chiamati dopo [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) useranno la modalità di smussamento attivata prima della chiamata a [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).

Per un altro esempio di combinazione delle trasformazioni del mondo di un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e di un contenitore, si supponga di voler disegnare un occhio e posizionarlo in diverse posizioni su una sequenza di visi. L'esempio seguente disegna un occhio centrato in corrispondenza dell'origine del sistema di coordinate.


```
void DrawEye(Graphics* pGraphics)
{
   GraphicsContainer eyeContainer;
   
   eyeContainer = pGraphics->BeginContainer();

      Pen myBlackPen(Color(255, 0, 0, 0));
      SolidBrush myGreenBrush(Color(255, 0, 128, 0));
      SolidBrush myBlackBrush(Color(255, 0, 0, 0));

      GraphicsPath myTopPath;
      myTopPath.AddEllipse(-30, -50, 60, 60);

      GraphicsPath myBottomPath;
      myBottomPath.AddEllipse(-30, -10, 60, 60);

      Region myTopRegion(&myTopPath);
      Region myBottomRegion(&myBottomPath);

      // Draw the outline of the eye.
      // The outline of the eye consists of two ellipses.
      // The top ellipse is clipped by the bottom ellipse, and
      // the bottom ellipse is clipped by the top ellipse.
      pGraphics->SetClip(&myTopRegion);
      pGraphics->DrawPath(&myBlackPen, &myBottomPath);
      pGraphics->SetClip(&myBottomRegion);
      pGraphics->DrawPath(&myBlackPen, &myTopPath);

      // Fill the iris.
      // The iris is clipped by the bottom ellipse.
      pGraphics->FillEllipse(&myGreenBrush, -10, -15, 20, 22);

      // Fill the pupil.
      pGraphics->FillEllipse(&myBlackBrush, -3, -7, 6, 9);

   pGraphics->EndContainer(eyeContainer);
}
```



La figura seguente mostra gli assi dell'occhio e delle coordinate.

![illustrazione che mostra un occhio composto da tre puntini di sospensione: uno per il contorno, l'iris e la sfumatura](images/aboutgdip05-art19.png)

La funzione DrawEye, definita nell'esempio precedente, riceve l'indirizzo di un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e crea immediatamente un contenitore all'interno di **tale oggetto Graphics.** Questo contenitore isola qualsiasi codice che chiama la funzione DrawEye dalle impostazioni delle proprietà effettuate durante l'esecuzione della funzione DrawEye. Ad esempio, il codice nella funzione DrawEye imposta l'area di ritaglio dell'oggetto **Graphics,** ma quando DrawEye restituisce il controllo alla routine chiamante, l'area di ritaglio sarà come prima della chiamata a DrawEye.

L'esempio seguente disegna tre puntini di sospensione (visi), ognuno con un occhio all'interno.


```
// Draw an ellipse with center at (100, 100).
myGraphics.TranslateTransform(100.0f, 100.0f);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Draw the eye at the center of the ellipse.
DrawEye(&myGraphics);

// Draw an ellipse with center at 200, 100.
myGraphics.TranslateTransform(100.0f, 0.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Rotate the eye 40 degrees, and draw it 30 units above
// the center of the ellipse.
myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.RotateTransform(-40.0f);
   myGraphics.TranslateTransform(0.0f, -30.0f, MatrixOrderAppend);
   DrawEye(&myGraphics);
myGraphics.EndContainer(myGraphicsContainer);

// Draw a ellipse with center at (300.0f, 100.0f).
myGraphics.TranslateTransform(100.0f, 0.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Stretch and rotate the eye, and draw it at the 
// center of the ellipse.
myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.ScaleTransform(2.0f, 1.5f);
   myGraphics.RotateTransform(45.0f, MatrixOrderAppend);
   DrawEye(&myGraphics);
myGraphics.EndContainer(myGraphicsContainer);
```



La figura seguente mostra i tre puntini di sospensione.

![Screenshot di una finestra con tre puntini di sospensione, ognuno dei quali contiene un occhio con dimensioni e rotazione diverse](images/aboutgdip05-art20.png)

Nell'esempio precedente, tutte le ellissi vengono disegnate con la chiamata , che disegna un'ellisse centrata in `DrawEllipse(&myBlackPen, -40, -60, 80, 120)` corrispondenza dell'origine del sistema di coordinate. I puntini di sospensione vengono spostati dall'angolo superiore sinistro dell'area client impostando la trasformazione globale [**dell'oggetto**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Graphics. L'istruzione fa sì che la prima ellisse sia centrata su (100, 100). L'istruzione fa sì che il centro della seconda ellisse sia 100 unità a destra del centro della prima ellisse. Analogamente, il centro della terza ellisse è 100 unità a destra del centro della seconda ellisse.

I contenitori nell'esempio precedente vengono usati per trasformare l'occhio rispetto al centro di una determinata ellisse. Il primo occhio viene disegnato al centro dell'ellisse senza alcuna trasformazione, quindi la chiamata DrawEye non si trova all'interno di un contenitore. Il secondo occhio viene ruotato di 40 gradi e disegnato 30 unità sopra il centro dell'ellisse, quindi la funzione DrawEye e i metodi che impostano la trasformazione vengono chiamati all'interno di un contenitore. Il terzo occhio viene allungato, ruotato e disegnato al centro dell'ellisse. Come per il secondo occhio, la funzione DrawEye e i metodi che impostano la trasformazione vengono chiamati all'interno di un contenitore.

 

 
