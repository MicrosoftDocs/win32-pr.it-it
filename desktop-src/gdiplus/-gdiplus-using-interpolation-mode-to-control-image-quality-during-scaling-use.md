---
description: La modalità di interpolazione di un oggetto Graphics influisce sul modo in cui Windows GDI+ ridimensiona (estende e compatta) le immagini.
ms.assetid: 3aeead47-78da-4ab3-9126-2fbe9e341e48
title: Uso della modalità di interpolazione per controllare la qualità dell'immagine durante il ridimensionamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34a829f2edf2f341f50bee771d909f7c4eef98e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977530"
---
# <a name="using-interpolation-mode-to-control-image-quality-during-scaling"></a>Uso della modalità di interpolazione per controllare la qualità dell'immagine durante il ridimensionamento

La modalità di interpolazione di un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) influisce sul modo in cui Windows GDI+ ridimensiona (estende e compatta) le immagini. L'enumerazione [**InterpolationMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) in Gdiplusenums. h definisce diverse modalità di interpolazione, alcune delle quali sono mostrate nell'elenco seguente:

-   InterpolationModeNearestNeighbor
-   InterpolationModeBilinear
-   InterpolationModeHighQualityBilinear
-   InterpolationModeBicubic
-   InterpolationModeHighQualityBicubic

Per estendere un'immagine, è necessario eseguire il mapping di ogni pixel nell'immagine originale a un gruppo di pixel nell'immagine più grande. Per compattare un'immagine, è necessario eseguire il mapping dei gruppi di pixel nell'immagine originale a singoli pixel nell'immagine più piccola. L'efficacia degli algoritmi che eseguono questi mapping determina la qualità di un'immagine ridimensionata. Gli algoritmi che producono immagini con scalabilità di qualità superiore tendono a richiedere più tempo di elaborazione. Nell'elenco precedente InterpolationModeNearestNeighbor è la modalità di qualità più bassa e InterpolationModeHighQualityBicubic è la modalità di qualità più elevata.

Per impostare la modalità di interpolazione, passare uno dei membri dell'enumerazione [**InterpolationMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) al metodo **SetInterpolationMode** di un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .

Nell'esempio seguente viene disegnata un'immagine, quindi viene compattata l'immagine con tre diverse modalità di interpolazione:


```
Image image(L"GrapeBunch.bmp");
UINT width = image.GetWidth();
UINT height = image.GetHeight();
// Draw the image with no shrinking or stretching.
graphics.DrawImage(
   &image,
   Rect(10, 10, width, height),  // destination rectangle  
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
// Shrink the image using low-quality interpolation. 
graphics.SetInterpolationMode(InterpolationModeNearestNeighbor);
graphics.DrawImage(
   &image,
   Rect(10, 250, 0.6*width, 0.6*height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
// Shrink the image using medium-quality interpolation.
graphics.SetInterpolationMode(InterpolationModeHighQualityBilinear);
graphics.DrawImage(
   &image,
   Rect(150, 250, 0.6 * width, 0.6 * height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
// Shrink the image using high-quality interpolation.
graphics.SetInterpolationMode(InterpolationModeHighQualityBicubic);
graphics.DrawImage(
   &image,
   Rect(290, 250, 0.6 * width, 0.6 * height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
```



La figura seguente illustra l'immagine originale e le tre immagini più piccole.

![illustrazione che mostra un'immagine originale di grandi dimensioni e le tre immagini più piccole di qualità variabile](images/grapes1.png)

 

 



