---
description: Una trasformazione globale è una trasformazione che viene applicata a ogni elemento disegnato da un determinato oggetto Graphics.
ms.assetid: 9f744c2a-f1f3-4a7e-ab0c-37aa1df01623
title: Trasformazioni globali e locali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2682fef6a6236b9da7ec0ec1e5ab5484ad9f90d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104557708"
---
# <a name="global-and-local-transformations"></a>Trasformazioni globali e locali

Una trasformazione globale è una trasformazione che viene applicata a ogni elemento disegnato da un determinato oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Per creare una trasformazione globale, costruire un oggetto **Graphics** , quindi chiamare il metodo [**Graphics:: setransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settransform) . Il metodo **Graphics:: setransform** modifica un oggetto [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) associato all'oggetto **Graphics** . La trasformazione archiviata nell'oggetto **matrice** viene chiamata *trasformazione globale*. La trasformazione mondiale può essere una semplice trasformazione affine o una complessa sequenza di trasformazioni affini, ma indipendentemente dalla complessità, la trasformazione globale è archiviata in un singolo oggetto **Matrix** .

La classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fornisce diversi metodi per la creazione di una trasformazione globale composita: [**Graphics:: MultiplyTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-multiplytransform), [**Graphics:: RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform), [**Graphics:: ScaleTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-scaletransform)e [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform). Nell'esempio seguente viene disegnata un'ellisse due volte: una volta prima di creare una trasformazione globale e una volta dopo. La trasformazione viene innanzitutto ridimensionata in base a un fattore di 0,5 nella direzione y, quindi converte 50 unità nella direzione x e quindi ruota di 30 gradi.


```
myGraphics.DrawEllipse(&myPen, 0, 0, 100, 50);
myGraphics.ScaleTransform(1.0f, 0.5f);
myGraphics.TranslateTransform(50.0f, 0.0f, MatrixOrderAppend);
myGraphics.RotateTransform(30.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myPen, 0, 0, 100, 50);
```



Nella figura seguente vengono illustrati l'ellisse originale e l'ellisse trasformata.

![Screenshot di una finestra che contiene due ellissi sovrapposti; uno è più piccolo e ruotato](images/aboutgdip05-art14.png)

> [!Note]  
> Nell'esempio precedente, l'ellisse viene ruotata sull'origine del sistema di coordinate, che si trova nell'angolo superiore sinistro dell'area client. Questo produce un risultato diverso rispetto alla rotazione dell'ellisse sul proprio centro.

 

Una trasformazione locale è una trasformazione che si applica a un elemento specifico da disegnare. Un oggetto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) , ad esempio, dispone di un metodo [**GraphicsPath:: Transform**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-transform) che consente di trasformare i punti dati di tale percorso. Nell'esempio seguente viene disegnato un rettangolo senza trasformazione e un percorso con una trasformazione di rotazione. (Si supponga che non esista alcuna trasformazione globale).


```
 
Matrix myMatrix;
myMatrix.Rotate(45.0f);
myGraphicsPath.Transform(&myMatrix);
myGraphics.DrawRectangle(&myPen, 10, 10, 100, 50);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



È possibile combinare la trasformazione globale con le trasformazioni locali per ottenere una serie di risultati. È ad esempio possibile utilizzare la trasformazione mondo per modificare il sistema di coordinate e utilizzare le trasformazioni locali per ruotare e ridimensionare gli oggetti disegnati nel nuovo sistema di coordinate.

Si supponga di volere un sistema di coordinate con origine 200 pixel dal bordo sinistro dell'area client e 150 pixel dalla parte superiore dell'area client. Si supponga inoltre che l'unità di misura sia il pixel, con l'asse x che punta verso destra e l'asse y che punta verso l'alto. Il sistema di coordinate predefinito ha l'asse y che punta verso il basso ed è quindi necessario eseguire una reflection sull'asse orizzontale. Nella figura seguente viene illustrata la matrice di tale Reflection.

![illustrazione che mostra una matrice tre per tre](images/aboutgdip05-art15.png)

Si supponga quindi che sia necessario eseguire una traduzione 200 unità a destra e 150 unità in basso.

Nell'esempio seguente viene stabilito il sistema di coordinate appena descritto impostando la trasformazione globale di un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .


```
Matrix myMatrix(1.0f, 0.0f, 0.0f, -1.0f, 0.0f, 0.0f);
myGraphics.SetTransform(&myMatrix);
myGraphics.TranslateTransform(200.0f, 150.0f, MatrixOrderAppend);
```



Il codice seguente (inserito dopo il codice nell'esempio precedente) crea un percorso costituito da un singolo rettangolo con l'angolo inferiore sinistro all'origine del nuovo sistema di coordinate. Il rettangolo viene compilato una volta senza alcuna trasformazione locale e una volta con una trasformazione locale. La trasformazione locale è costituita da un ridimensionamento orizzontale di un fattore 2 seguito da una rotazione di 30 gradi.


```
// Create the path.
GraphicsPath myGraphicsPath;
Rect myRect(0, 0, 60, 60);
myGraphicsPath.AddRectangle(myRect);

// Fill the path on the new coordinate system.
// No local transformation
myGraphics.FillPath(&mySolidBrush1, &myGraphicsPath);

// Transform the path.
Matrix myPathMatrix;
myPathMatrix.Scale(2, 1);
myPathMatrix.Rotate(30, MatrixOrderAppend);
myGraphicsPath.Transform(&myPathMatrix);

// Fill the transformed path on the new coordinate system.
myGraphics.FillPath(&mySolidBrush2, &myGraphicsPath);
```



Nella figura seguente vengono illustrati il nuovo sistema di coordinate e i due rettangoli.

![Screenshot di un asse x e y e un quadrato blu sovrapposto a una semitrasparente rectagle ruotata intorno all'angolo inferiore sinistro](images/aboutgdip05-art16.png)

 

 



