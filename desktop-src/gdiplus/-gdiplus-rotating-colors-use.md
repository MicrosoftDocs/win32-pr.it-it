---
description: La rotazione in uno spazio colori quattrodimensionale è difficile da visualizzare.
ms.assetid: 099f76a3-2da3-4f2b-8f8d-557d144451dc
title: Rotazione dei colori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fc09a84c4c51181c672c549369783ac476fa1d3c79f1598c1c29ca14604429d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036429"
---
# <a name="rotating-colors"></a>Rotazione dei colori

La rotazione in uno spazio colori quattrodimensionale è difficile da visualizzare. È possibile semplificare la visualizzazione della rotazione accettando di mantenere fisso uno dei componenti di colore. Si supponga di accettare di mantenere il componente alfa fisso su 1 (completamente opaco). È quindi possibile visualizzare uno spazio colori tridimensionale con assi rosso, verde e blu, come illustrato nella figura seguente.

![illustrazione di una vista prospettica di uno spazio colori tridimensionale con assi con etichetta rosso, verde e blu](images/recoloring03.png)

Un colore può essere pensato come un punto nello spazio 3D. Ad esempio, il punto (1, 0, 0) nello spazio rappresenta il colore rosso e il punto (0, 1, 0) nello spazio rappresenta il colore verde.

La figura seguente mostra cosa significa ruotare il colore (1, 0, 0) in un angolo di 60 gradi nel piano Red-Green verticale. La rotazione in un piano parallelo al Red-Green può essere pensata come rotazione intorno all'asse blu.

![illustrazione che mostra il punto (1, 0, 0) ruotato da 60 gradi a (0,5, 0,866, 0)](images/recoloring04.png)

Nella figura seguente viene illustrato come inizializzare una matrice di colori per eseguire rotazioni su ognuno dei tre assi delle coordinate (rosso, verde, blu).

![illustrazione che mostra matrici di colori che eseguono rotazioni su ognuno dei tre assi delle coordinate](images/recoloring05.png)

Nell'esempio seguente viene accettata un'immagine con un solo colore (1, 0, 0,6) e viene applicata una rotazione di 60 gradi intorno all'asse blu. L'angolo della rotazione si trova in un piano parallelo al piano Red-Green rotazione.


```
Image            image(L"RotationInput.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();
REAL             degrees = 60;
REAL             pi = acos(-1);  // the angle whose cosine is -1.
REAL             r = degrees * pi / 180;  // degrees to radians

ColorMatrix colorMatrix = {
   cos(r),  sin(r), 0.0f, 0.0f, 0.0f,
   -sin(r), cos(r), 0.0f, 0.0f, 0.0f,
   0.0f,    0.0f,   1.0f, 0.0f, 0.0f,
   0.0f,    0.0f,   0.0f, 1.0f, 0.0f,
   0.0f,    0.0f,   0.0f, 0.0f, 1.0f};
   
imageAttributes.SetColorMatrix(
   &colorMatrix, 
   ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
   
graphics.DrawImage(&image, 10, 10, width, height);

graphics.DrawImage(
   &image, 
   Rect(130, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



La figura seguente mostra l'immagine originale a sinistra e l'immagine ruotata a colori a destra.

![illustrazione che mostra rettangoli riempiti con l'immagine originale (rosso bianco) e l'immagine ruotata a colori (verde acqua)](images/colortrans5.png)

La rotazione dei colori eseguita nell'esempio di codice precedente può essere mostrata come segue.

![illustrazione che mostra uno spazio colore 3D e il punto (1, 0, 0,6) ruotato da 60 gradi a (0,5, 0,866, 0,6)](images/recoloring06.png)

 

 



