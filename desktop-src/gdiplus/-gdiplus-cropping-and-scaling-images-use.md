---
title: Ritaglio e ridimensionamento di GDI+ immagini
description: La classe Graphics fornisce diversi metodi DrawImage, alcuni dei quali hanno parametri del rettangolo di origine e di destinazione che è possibile usare per ritagliare e ridimensionare le immagini.
ms.assetid: cad64615-d8e6-4c03-a6c7-c98267a8f159
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3684089ddab4ba963a79b80aafa67e94f94d988de5aa7d7d9f65ad31e48bcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118067551"
---
# <a name="cropping-and-scaling-gdi-images"></a>Ritaglio e ridimensionamento di GDI+ immagini

La [**classe Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fornisce diversi metodi **DrawImage,** alcuni dei quali hanno parametri del rettangolo di origine e di destinazione che è possibile usare per ritagliare e ridimensionare le immagini.

Nell'esempio seguente viene costruito un [**oggetto Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) dal file Apple.gif. Il codice disegna l'intera immagine apple nelle dimensioni originali. Il codice chiama quindi il **metodo DrawImage** di un [**oggetto Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) per disegnare una parte dell'immagine apple in un rettangolo di destinazione più grande dell'immagine apple originale.

Il **metodo DrawImage** determina quale parte della apple disegnare esaminando il rettangolo di origine, specificato dal terzo, quarto, quinto e sesto argomento. In questo caso, la apple viene ritagliata al 75% della larghezza e al 75% dell'altezza.

Il **metodo DrawImage** determina la posizione in cui disegnare la apple ritagliata e la sua estensione osservando il rettangolo di destinazione, specificato dal secondo argomento. In questo caso, il rettangolo di destinazione è più ampio del 30% e più alto del 30% rispetto all'immagine originale.


```
Image image(L"Apple.gif");
UINT width = image.GetWidth();
UINT height = image.GetHeight();
// Make the destination rectangle 30 percent wider and
// 30 percent taller than the original image.
// Put the upper-left corner of the destination
// rectangle at (150, 20).
Rect destinationRect(150, 20, 1.3 * width, 1.3 * height);
// Draw the image unaltered with its upper-left corner at (0, 0).
graphics.DrawImage(&image, 0, 0);
// Draw a portion of the image. Scale that portion of the image
// so that it fills the destination rectangle.
graphics.DrawImage(
   &image,
   destinationRect,
   0, 0,              // upper-left corner of source rectangle
   0.75 * width,      // width of source rectangle
   0.75 * height,     // height of source rectangle
   UnitPixel);
```



La figura seguente mostra la apple originale e la apple ritagliata in scala.

![illustrazione che mostra una apple, quindi una parte ingrandita della apple originale](images/cropscale1.png)

 

 



