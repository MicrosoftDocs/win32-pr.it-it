---
title: Informazioni sul ritaglio e sul ridimensionamento di immagini GDI+
description: È possibile usare il metodo DrawImage della classe Graphics per creare e posizionare le immagini.
ms.assetid: 81d20adc-0481-4b1b-80aa-ae218fdecd84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b44a13b5cee632e6ceafe327f94eca48edd93dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131354"
---
# <a name="about-cropping-and-scaling-gdi-images"></a>Informazioni sul ritaglio e sul ridimensionamento di immagini GDI+

È possibile usare il metodo [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) della classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) per creare e posizionare le immagini. DrawImage è un metodo di overload, quindi è possibile fornire gli argomenti in diversi modi. Una variante del metodo [**Graphics::D rawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) riceve l'indirizzo di un oggetto [**immagine**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) e un riferimento a un oggetto [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) . Il rettangolo specifica la destinazione per l'operazione di disegno. ovvero specifica il rettangolo in cui verrà disegnata l'immagine. Se le dimensioni del rettangolo di destinazione sono diverse da quelle dell'immagine originale, l'immagine viene ridimensionata in modo da adattarsi al rettangolo di destinazione. Nell'esempio seguente viene disegnata la stessa immagine tre volte: una volta senza scalabilità, una volta con un'espansione e una volta con una compressione.


```
Bitmap myBitmap(L"Spiral.png");
Rect expansionRect(80, 10, 2 * myBitmap.GetWidth(), myBitmap.GetHeight());
Rect compressionRect(210, 10, myBitmap.GetWidth() / 2, 
   myBitmap.GetHeight() / 2);

myGraphics.DrawImage(&myBitmap, 10, 10);
myGraphics.DrawImage(&myBitmap, expansionRect);
myGraphics.DrawImage(&myBitmap, compressionRect);
```



Il codice precedente, insieme a un determinato file Spiral.png, ha prodotto l'output seguente.

![illustrazione che mostra tre versioni di un'immagine: normale, estesa e compattata a metà delle dimensioni originali](images/aboutgdip03-art06.png)

Alcune varianti della [**grafica::D Metodo rawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) hanno un parametro source-Rectangle, oltre a un parametro Destination-Rectangle. Il rettangolo di origine specifica la parte dell'immagine originale che verrà disegnata. Il rettangolo di destinazione specifica il punto in cui verrà disegnata la parte dell'immagine. Se le dimensioni del rettangolo di destinazione sono diverse dalla dimensione del rettangolo di origine, l'immagine viene ridimensionata in modo da adattarsi al rettangolo di destinazione.

Nell'esempio seguente viene costruito un oggetto [**bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) dal file Runner.jpg. L'intera immagine viene disegnata senza alcun ridimensionamento in corrispondenza di (0, 0). Una piccola parte dell'immagine viene disegnata due volte: una volta con una compressione e una volta con un'espansione.


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



Nella figura seguente viene illustrata l'immagine non ridimensionata e le parti di immagine compresse ed espanse.

![screenshot che mostra un'immagine, una parte dell'immagine compressa e quindi la stessa parte espansa](images/aboutgdip03-art07.png)

 

 



