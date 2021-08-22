---
description: Una trasformazione di ridimensionamento moltiplica uno o più dei quattro componenti di colore per un numero. Le voci della matrice di colori che rappresentano il ridimensionamento sono riportate nella tabella seguente.
ms.assetid: 08347831-7100-4220-a83b-693bb7b98ccb
title: Ridimensionamento dei colori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7877db07ff1a11dcb985f8b0ca8ec3cc017f25fe45f00e989c9108891f8ff1ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036369"
---
# <a name="scaling-colors"></a>Ridimensionamento dei colori

Una trasformazione di ridimensionamento moltiplica uno o più dei quattro componenti di colore per un numero. Le voci della matrice di colori che rappresentano il ridimensionamento sono riportate nella tabella seguente.



| Componente da ridimensionare | Immissione matrice |
|------------------------|--------------|
| Red                    | \[0 \] \[ 0\]   |
| Green                  | \[1 \] \[ 1\]   |
| Blu                   | \[2 \] \[ 2\]   |
| Alfa                  | \[3 \] \[ 3\]   |



 

L'esempio seguente costruisce un [**oggetto Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) dal file ColorBars2.bmp. Il codice ridimensiona quindi il componente blu di ogni pixel nell'immagine di un fattore di 2. L'immagine originale viene disegnata insieme all'immagine trasformata.


```
Image            image(L"ColorBars2.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 2.0f, 0.0f, 0.0f,
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



La figura seguente mostra l'immagine originale a sinistra e l'immagine ridimensionata a destra.

![Mostra quattro barre colorate e quindi le stesse barre con colori diversi.](images/colortrans3.png)

La tabella seguente mostra i vettori di colore per le quattro barre prima e dopo il ridimensionamento blu. Si noti che il componente blu nella quarta barra dei colori è passato da 0,8 a 0,6. Questo perché GDI+ mantiene solo la parte frazionaria del risultato. Ad esempio, (2)(0,8) = 1,6 e la parte frazionaria di 1,6 è 0,6. Mantenendo solo la parte frazionaria si garantisce che il risultato sia sempre nell'intervallo \[ 0, 1 \] .



| Originale           | Scala             |
|--------------------|--------------------|
| (0.4, 0.4, 0.4, 1) | (0.4, 0.4, 0.8, 1) |
| (0.4, 0.2, 0.2, 1) | (0.4, 0.2, 0.4, 1) |
| (0.2, 0.4, 0.2, 1) | (0.2, 0.4, 0.4, 1) |
| (0.4, 0.4, 0.8, 1) | (0.4, 0.4, 0.6, 1) |



 

L'esempio seguente costruisce un [**oggetto Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) dal file ColorBars2.bmp. Il codice ridimensiona quindi i componenti rosso, verde e blu di ogni pixel nell'immagine. I componenti rossi vengono ridimensionati del 25%, i componenti verdi vengono ridimensionati del 35% e i componenti blu vengono ridimensionati del 50%.


```
Image            image(L"ColorBars.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   0.75f, 0.0f,  0.0f, 0.0f, 0.0f,
   0.0f,  0.65f, 0.0f, 0.0f, 0.0f,
   0.0f,  0.0f,  0.5f, 0.0f, 0.0f,
   0.0f,  0.0f,  0.0f, 1.0f, 0.0f,
   0.0f,  0.0f,  0.0f, 0.0f, 1.0f};
   
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



La figura seguente mostra l'immagine originale a sinistra e l'immagine ridimensionata a destra.

![illustrazione che mostra quattro barre colorate, quindi quelle con colori diversi](images/colortrans4.png)

La tabella seguente mostra i vettori di colore per le quattro barre prima e dopo il ridimensionamento rosso, verde e blu.



| Originale           | Scala               |
|--------------------|----------------------|
| (0.6, 0.6, 0.6, 1) | (0.45, 0.39, 0.3, 1) |
| (0, 1, 1, 1)       | (0, 0.65, 0.5, 1)    |
| (1, 1, 0, 1)       | (0.75, 0.65, 0, 1)   |
| (1, 0, 1, 1)       | (0.75, 0, 0.5, 1)    |



 

 

 



