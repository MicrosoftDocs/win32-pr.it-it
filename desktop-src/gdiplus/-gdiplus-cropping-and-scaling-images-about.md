---
title: Informazioni sul ritaglio e sul ridimensionamento di immagini GDI+
description: È possibile usare il metodo DrawImage della classe Graphics per disegnare e posizionare le immagini.
ms.assetid: 81d20adc-0481-4b1b-80aa-ae218fdecd84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9e69adb7f817c36b955ed313290cf0b762c279b4296e06ad52aa6175ff2c467
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036839"
---
# <a name="about-cropping-and-scaling-gdi-images"></a>Informazioni sul ritaglio e sul ridimensionamento di immagini GDI+

È possibile usare il [metodo DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) della [**classe Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) per disegnare e posizionare le immagini. DrawImage è un metodo di overload, quindi è possibile specificarlo in diversi modi con argomenti. Una variante del [**metodo Graphics::D rawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) riceve l'indirizzo di un oggetto [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) e un riferimento a un [**oggetto Rect.**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) Il rettangolo specifica la destinazione per l'operazione di disegno. ovvero specifica il rettangolo in cui verrà disegnata l'immagine. Se le dimensioni del rettangolo di destinazione sono diverse dalle dimensioni dell'immagine originale, l'immagine viene ridimensionata in base al rettangolo di destinazione. L'esempio seguente disegna la stessa immagine tre volte: una volta senza ridimensionamento, una con un'espansione e una volta con una compressione.


```
Bitmap myBitmap(L"Spiral.png");
Rect expansionRect(80, 10, 2 * myBitmap.GetWidth(), myBitmap.GetHeight());
Rect compressionRect(210, 10, myBitmap.GetWidth() / 2, 
   myBitmap.GetHeight() / 2);

myGraphics.DrawImage(&myBitmap, 10, 10);
myGraphics.DrawImage(&myBitmap, expansionRect);
myGraphics.DrawImage(&myBitmap, compressionRect);
```



Il codice precedente, insieme a un file specifico, Spiral.png, ha prodotto l'output seguente.

![Figura che mostra tre versioni di un'immagine: normale, estesa e ridotta a metà delle dimensioni originali](images/aboutgdip03-art06.png)

Alcune varianti del [**metodo Graphics::D rawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) hanno un parametro del rettangolo di origine e un parametro del rettangolo di destinazione. Il rettangolo di origine specifica la parte dell'immagine originale che verrà disegnata. Il rettangolo di destinazione specifica dove verrà disegnata la parte dell'immagine. Se le dimensioni del rettangolo di destinazione sono diverse dalle dimensioni del rettangolo di origine, l'immagine viene ridimensionata in base al rettangolo di destinazione.

Nell'esempio seguente viene creato un [**oggetto Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) dal file Runner.jpg. L'intera immagine viene disegnata senza ridimensionamento (0, 0). Quindi una piccola parte dell'immagine viene disegnata due volte: una con una compressione e una volta con un'espansione.


```
Bitmap myBitmap(L"Runner.jpg"); 

// The rectangle (in myBitmap) with upper-left corner (80, 70), 
// width 80, and height 45, encloses one of the runner's hands.

// Small destination rectangle for compressed hand.
Rect destRect1(200, 10, 20, 16);

// Large destination rectangle for expanded hand.
Rect destRect2(200, 40, 200, 160);

// Draw the original image at (0, 0).
myGraphics.DrawImage(&myBitmap, 0, 0);

// Draw the compressed hand.
myGraphics.DrawImage(
   &myBitmap, destRect1, 80, 70, 80, 45, UnitPixel);

// Draw the expanded hand. 
myGraphics.DrawImage(
   &myBitmap, destRect2, 80, 70, 80, 45, UnitPixel);
```



La figura seguente mostra l'immagine non ridimensionata e le parti dell'immagine compressa ed espansa.

![Screenshot che mostra un'immagine, quindi una parte dell'immagine compressa e quindi la stessa parte espansa](images/aboutgdip03-art07.png)

 

 



