---
title: Ritaglio e ridimensionamento di immagini GDI+
description: La classe Graphics fornisce diversi metodi DrawImage, alcuni dei quali hanno parametri di origine e di destinazione rettangolari che è possibile usare per ritagliare e ridimensionare le immagini.
ms.assetid: cad64615-d8e6-4c03-a6c7-c98267a8f159
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18c70a7b4f7aa0374602326ab856a01bbadc0047
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987880"
---
# <a name="cropping-and-scaling-gdi-images"></a>Ritaglio e ridimensionamento di immagini GDI+

La classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fornisce diversi metodi **DrawImage** , alcuni dei quali hanno parametri di origine e di destinazione rettangolari che è possibile usare per ritagliare e ridimensionare le immagini.

Nell'esempio seguente viene costruito un oggetto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) dal file Apple.gif. Il codice disegna l'intera immagine Apple nelle dimensioni originali. Il codice chiama quindi il metodo **DrawImage** di un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) per creare una parte dell'immagine Apple in un rettangolo di destinazione più grande dell'immagine Apple originale.

Il metodo **DrawImage** determina la parte della mela da creare osservando il rettangolo di origine, specificato dal terzo, dal quarto, dal quinto e dal sesto argomento. In questo caso, la mela viene ritagliata al 75% della larghezza e il 75% dell'altezza.

Il metodo **DrawImage** determina la posizione in cui creare la mela ritagliata e la dimensione della mela ritagliata esaminando il rettangolo di destinazione, specificato dal secondo argomento. In questo caso, il rettangolo di destinazione è più grande del 30% e il 30% più alto rispetto all'immagine originale.


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



La figura seguente mostra l'Apple originale e l'Apple ritagliata e ridimensionata.

![illustrazione che mostra una mela, quindi una parte ingrandita della mela originale](images/cropscale1.png)

 

 



