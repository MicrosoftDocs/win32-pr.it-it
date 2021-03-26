---
description: Il taglio aumenta o diminuisce un componente colore di un importo proporzionale a un altro componente colore.
ms.assetid: 12f83f35-33f1-4ac9-b45d-f8700e54053a
title: Colori di taglio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d632fded9f2b4d1e4682ae9f8ffbfedee85a46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131331"
---
# <a name="shearing-colors"></a>Colori di taglio

Il taglio aumenta o diminuisce un componente colore di un importo proporzionale a un altro componente colore. Si consideri, ad esempio, la trasformazione in cui il componente rosso viene aumentato di una metà del valore del componente blu. In tale trasformazione, il colore (0,2, 0,5, 1) diventerà (0,7, 0,5, 1). Il nuovo componente rosso è 0,2 + (1/2) (1) = 0,7.

Nell'esempio seguente viene costruito un oggetto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) dal file ColorBars4.bmp. Il codice applica quindi la trasformazione di taglio descritta nel paragrafo precedente a ogni pixel nell'immagine.


```
Image            image(L"ColorBars4.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.5f, 0.0f, 1.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 0.0f, 1.0f, 0.0f,
   0.0f, 0.0f, 0.0f, 0.0f, 1.0f};
   
imageAttributes.SetColorMatrix(
   &colorMatrix, 
   ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
   
graphics.DrawImage(&image, 10, 10, width, height);

graphics.DrawImage(
   &image, 
   Rect(150, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



Nell'illustrazione seguente viene mostrata l'immagine originale a sinistra e l'immagine tranciata a destra.

![illustrazione che mostra quattro barre colorate, quindi le stesse barre con colori diversi](images/colortrans6.png)

Nella tabella seguente vengono illustrati i vettori di colore per le quattro barre prima e dopo la trasformazione di taglio.



| Originale           | Tranciati            |
|--------------------|--------------------|
| (0, 0, 1, 1)       | (0.5, 0, 1, 1)     |
| (0.5, 1, 0.5, 1)   | (0.75, 1, 0.5, 1)  |
| (1, 1, 0, 1)       | (1, 1, 0, 1)       |
| (0.4, 0.4, 0.4, 1) | (0.6, 0.4, 0.4, 1) |



 

 

 



