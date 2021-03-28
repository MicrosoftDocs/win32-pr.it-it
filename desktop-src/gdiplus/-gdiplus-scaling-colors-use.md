---
description: Una trasformazione di ridimensionamento moltiplica uno o più dei quattro componenti colore per numero. Nella tabella seguente vengono fornite le voci della matrice di colori che rappresentano il ridimensionamento.
ms.assetid: 08347831-7100-4220-a83b-693bb7b98ccb
title: Ridimensionamento di colori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 370155306f7b1a177358d7cf28d329ebb0d75f8c
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104234416"
---
# <a name="scaling-colors"></a>Ridimensionamento di colori

Una trasformazione di ridimensionamento moltiplica uno o più dei quattro componenti colore per numero. Nella tabella seguente vengono fornite le voci della matrice di colori che rappresentano il ridimensionamento.



| Componente da ridimensionare | Voce matrice |
|------------------------|--------------|
| Red                    | \[0 \] \[ 0\]   |
| Green                  | \[1 \] \[ 1\]   |
| Blu                   | \[2 \] \[ 2\]   |
| Alfa                  | \[3 \] \[ 3\]   |



 

Nell'esempio seguente viene costruito un oggetto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) dal file ColorBars2.bmp. Quindi il codice ridimensiona il componente blu di ogni pixel nell'immagine per un fattore di 2. L'immagine originale viene disegnata insieme all'immagine trasformata.


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



Nell'illustrazione seguente viene mostrata l'immagine originale a sinistra e l'immagine ridimensionata a destra.

![Mostra quattro barre colorate, quindi le stesse barre con colori diversi.](images/colortrans3.png)

La tabella seguente mostra i vettori di colore per le quattro barre prima e dopo il ridimensionamento blu. Si noti che il componente blu nella quarta barra dei colori è stato compreso tra 0,8 e 0,6. Ciò è dovuto al fatto che GDI+ mantiene solo la parte frazionaria del risultato. Ad esempio, (2) (0.8) = 1,6 e la parte frazionaria di 1,6 è 0,6. La conservazione solo della parte frazionaria garantisce che il risultato sia sempre nell'intervallo \[ compreso tra 0 e 1 \] .



| Originale           | Ridimensionato             |
|--------------------|--------------------|
| (0.4, 0.4, 0.4, 1) | (0.4, 0.4, 0.8, 1) |
| (0.4, 0.2, 0.2, 1) | (0.4, 0.2, 0.4, 1) |
| (0.2, 0.4, 0.2, 1) | (0.2, 0.4, 0.4, 1) |
| (0.4, 0.4, 0.8, 1) | (0.4, 0.4, 0.6, 1) |



 

Nell'esempio seguente viene costruito un oggetto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) dal file ColorBars2.bmp. Il codice Ridimensiona quindi i componenti rosso, verde e blu di ogni pixel nell'immagine. I componenti rossi vengono ridimensionati fino al 25%, i componenti verdi vengono ridimensionati fino al 35% e i componenti blu vengono ridimensionati fino al 50%.


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



Nell'illustrazione seguente viene mostrata l'immagine originale a sinistra e l'immagine ridimensionata a destra.

![illustrazione che mostra quattro barre colorate, quindi le barre con colori diversi](images/colortrans4.png)

La tabella seguente mostra i vettori di colore per le quattro barre prima e dopo il ridimensionamento rosso, verde e blu.



| Originale           | Ridimensionato               |
|--------------------|----------------------|
| (0.6, 0.6, 0.6, 1) | (0.45, 0.39, 0.3, 1) |
| (0, 1, 1, 1)       | (0, 0.65, 0.5, 1)    |
| (1, 1, 0, 1)       | (0.75, 0.65, 0, 1)   |
| (1, 0, 1, 1)       | (0.75, 0, 0.5, 1)    |



 

 

 



