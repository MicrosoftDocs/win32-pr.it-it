---
description: Una traduzione aggiunge un valore a uno o più dei quattro componenti del colore. Nella tabella seguente vengono fornite le voci della matrice di colori che rappresentano le traduzioni.
ms.assetid: a0d89989-9b98-42fb-8d87-206581e3c91e
title: Conversione di colori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c769a24c02e977c3e32ff913852d4b6b8d54441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104569655"
---
# <a name="translating-colors"></a>Conversione di colori

Una traduzione aggiunge un valore a uno o più dei quattro componenti del colore. Nella tabella seguente vengono fornite le voci della matrice di colori che rappresentano le traduzioni.



| Componente da tradurre | Voce matrice |
|----------------------------|--------------|
| Red                        | \[4 \] \[ 0\]   |
| Green                      | \[4 \] \[ 1\]   |
| Blu                       | \[4 \] \[ 2\]   |
| Alfa                      | \[4 \] \[ 3\]   |



 

Nell'esempio seguente viene costruito un oggetto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) dal file ColorBars.bmp. Il codice aggiunge quindi 0,75 al componente rosso di ogni pixel nell'immagine. L'immagine originale viene disegnata insieme all'immagine trasformata.


```
Image            image(L"ColorBars.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f,  0.0f, 0.0f, 0.0f, 0.0f,
   0.0f,  1.0f, 0.0f, 0.0f, 0.0f,
   0.0f,  0.0f, 1.0f, 0.0f, 0.0f,
   0.0f,  0.0f, 0.0f, 1.0f, 0.0f,
   0.75f, 0.0f, 0.0f, 0.0f, 1.0f};
   
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



Nell'illustrazione seguente viene mostrata l'immagine originale a sinistra e l'immagine trasformata a destra.

![illustrazione che mostra quattro barre colorate, quindi le stesse barre con colori diversi](images/colortrans2.png)

Nella tabella seguente sono elencati i vettori di colore per le quattro barre prima e dopo la traduzione rossa. Si noti che poiché il valore massimo per un componente colore è 1, il componente rosso nella seconda riga non cambia. Analogamente, il valore minimo per un componente colore è 0.



| Originale           | Convertito      |
|--------------------|-----------------|
| Nero (0, 0, 0, 1) | (0.75, 0, 0, 1) |
| Rosso (1, 0, 0, 1)   | (1, 0, 0, 1)    |
| Verde (0, 1, 0, 1) | (0.75, 1, 0, 1) |
| Blu (0, 0, 1, 1)  | (0.75, 0, 1, 1) |



 

 

 



