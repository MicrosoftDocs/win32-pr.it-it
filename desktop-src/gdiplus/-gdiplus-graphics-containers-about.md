---
description: Lo stato graphics &\# 8212; area di ridimensionamento, trasformazioni e impostazioni di qualità &\# 8212; è archiviato in un oggetto Graphics.
ms.assetid: 98b9fa12-02e7-42bf-9cbd-03ee696188f6
title: Contenitori di oggetti Graphics
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab8bf6469d0835137be1bb76b7727fd961bba16b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104565515"
---
# <a name="graphics-containers"></a>Contenitori di oggetti Graphics

Lo stato della grafica, ovvero area di ridimensionamento, trasformazioni e impostazioni di qualità, viene archiviato in un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Windows GDI+ consente di sostituire temporaneamente o aumentare parte dello stato in un oggetto **Graphics** utilizzando un contenitore. Per avviare un contenitore, chiamare il metodo [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) di un oggetto **Graphics** e terminare un contenitore chiamando il metodo [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) . In between **Graphics:: BeginContainer** e **Graphics:: EndContainer** tutte le modifiche di stato apportate all'oggetto **Graphics** appartengono al contenitore e non sovrascrivono lo stato esistente dell'oggetto **Graphics** .

Nell'esempio seguente viene creato un contenitore all'interno di un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . La trasformazione globale dell'oggetto **Graphics** è una traduzione 200 unità a destra e la trasformazione globale del contenitore è una conversione 100 unità inattive.


```
myGraphics.TranslateTransform(200.0f, 0.0f);

myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.TranslateTransform(0.0f, 100.0f);
   myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50);
myGraphics.EndContainer(myGraphicsContainer);

myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50);
```



Si noti che nell'esempio precedente, l'istruzione `myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50)` eseguita tra le chiamate a [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) e [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) produce un rettangolo diverso dalla stessa istruzione effettuata dopo la chiamata a **Graphics:: EndContainer**. Solo la traduzione orizzontale si applica alla chiamata **DrawRectangle** effettuata all'esterno del contenitore. Entrambe le trasformazioni, ovvero la traduzione orizzontale di 200 unità e la conversione verticale di 100 unità, si applicano alla [**grafica::D chiamata rawrectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) effettuata all'interno del contenitore. Nella figura seguente sono illustrati i due rettangoli.

![Screenshot di una finestra con due rettangoli disegnati con una penna blu, uno posizionato sopra l'altro](images/aboutgdip05-art17.png)

I contenitori possono essere annidati all'interno dei contenitori. Nell'esempio seguente viene creato un contenitore in un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e un altro contenitore all'interno del primo contenitore. La trasformazione globale dell'oggetto **Graphics** è una conversione di unità 100 nella direzione x e 80 unità nella direzione y. La trasformazione globale del primo contenitore è una rotazione di 30 gradi. La trasformazione globale del secondo contenitore è una scala per un fattore 2 nella direzione x. Viene eseguita una chiamata al metodo [**Graphics::D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) all'interno del secondo contenitore.


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



La figura seguente mostra l'ellisse.

![Screenshot di una finestra che contiene un'ellisse blu ruotata con il relativo centro contrassegnato come (100, 80)](images/aboutgdip05-art18.png)

Si noti che tutte e tre le trasformazioni si applicano alla [**grafica::D chiamata rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) effettuata nel secondo contenitore (più interno). Si noti anche l'ordine delle trasformazioni: prima scala, quindi ruota, quindi trasla. La trasformazione più interna viene applicata per prima e la trasformazione più esterna viene applicata per ultima.

È possibile impostare qualsiasi proprietà di un oggetto [**grafico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) all'interno di un contenitore (tra le chiamate a [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) e [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)). È ad esempio possibile impostare un'area di ridimensionamento all'interno di un contenitore. Qualsiasi disegno eseguito all'interno del contenitore sarà limitato all'area di visualizzazione del contenitore e sarà limitato anche alle aree di visualizzazione di qualsiasi contenitore esterno e all'area di visualizzazione dell'oggetto **Graphics** stesso.

Le proprietà discusse finora, ovvero la trasformazione mondiale e l'area di visualizzazione, vengono combinate dai contenitori annidati. Le altre proprietà vengono temporaneamente sostituite da un contenitore annidato. Se, ad esempio, si imposta la modalità di smussatura su SmoothingModeAntiAlias all'interno di un contenitore, qualsiasi metodo di disegno chiamato all'interno del contenitore utilizzerà la modalità di smussamento AntiAlias, ma i metodi di disegno chiamati dopo [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) utilizzeranno la modalità di smussamento che era presente prima della chiamata a [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).

Per un altro esempio di combinazione delle trasformazioni internazionali di un oggetto [**grafico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e di un contenitore, si supponga di voler creare un occhio e posizionarlo in varie posizioni in una sequenza di visi. Nell'esempio seguente viene disegnato un occhio centrato sull'origine del sistema di coordinate.


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



Nella figura seguente vengono illustrati l'occhio e gli assi delle coordinate.

![illustrazione che mostra un occhio composto da tre ellissi: uno per la struttura, Iris e la pupilla](images/aboutgdip05-art19.png)

La funzione DrawEye, definita nell'esempio precedente, riceve l'indirizzo di un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e crea immediatamente un contenitore all'interno dell'oggetto **Graphics** . Questo contenitore isola il codice che chiama la funzione DrawEye dalle impostazioni delle proprietà effettuate durante l'esecuzione della funzione DrawEye. Ad esempio, il codice nella funzione DrawEye imposta l'area di visualizzazione dell'oggetto **Graphics** , ma quando DrawEye restituisce il controllo alla routine chiamante, l'area di ridimensionamento sarà così com'era prima della chiamata a DrawEye.

Nell'esempio seguente vengono disegnati tre ellissi (visi), ognuno con un occhio all'interno.


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



Nella figura seguente sono illustrati i tre ellissi.

![Screenshot di una finestra con tre ellissi, ognuno dei quali contiene un occhio a una dimensione e una rotazione diverse](images/aboutgdip05-art20.png)

Nell'esempio precedente, tutti i puntini di sospensione vengono disegnati con la chiamata `DrawEllipse(&myBlackPen, -40, -60, 80, 120)` , che disegna un'ellisse centrata sull'origine del sistema di coordinate. I puntini di sospensione vengono spostati dall'angolo superiore sinistro dell'area client impostando la trasformazione globale dell'oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . L'istruzione fa in modo che la prima ellisse si trovi al centro (100, 100). L'istruzione fa in modo che il centro della seconda ellisse sia 100 unità a destra del centro della prima ellisse. Analogamente, il centro della terza ellisse è 100 unità a destra del centro della seconda ellisse.

I contenitori nell'esempio precedente vengono usati per trasformare l'occhio rispetto al centro di una determinata ellisse. Il primo occhio viene disegnato al centro dell'ellisse senza trasformazione, quindi la chiamata DrawEye non si trova all'interno di un contenitore. Il secondo occhio è ruotato di 40 gradi e ha disegnato 30 unità al di sopra del centro dell'ellisse, quindi la funzione DrawEye e i metodi che impostano la trasformazione vengono chiamati all'interno di un contenitore. Il terzo occhio viene allungato e ruotato e disegnato al centro dell'ellisse. Come nel secondo occhio, la funzione DrawEye e i metodi che impostano la trasformazione vengono chiamati all'interno di un contenitore.

 

 
