---
description: La rotazione in uno spazio di colore a quattro dimensioni è difficile da visualizzare.
ms.assetid: 099f76a3-2da3-4f2b-8f8d-557d144451dc
title: Rotazione di colori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea322179bd4a46021d181abedd1797d6bdda7cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879173"
---
# <a name="rotating-colors"></a>Rotazione di colori

La rotazione in uno spazio di colore a quattro dimensioni è difficile da visualizzare. È possibile semplificare la visualizzazione della rotazione accettando che uno dei componenti del colore sia fisso. Si supponga di accettare di tenere il componente alfa fisso a 1 (completamente opaco). Sarà quindi possibile visualizzare uno spazio colore tridimensionale con assi rossi, verdi e blu, come illustrato nella figura seguente.

![illustrazione di una visualizzazione prospettica di uno spazio colore tridimensionale con assi con etichetta rosso, verde e blu](images/recoloring03.png)

Un colore può essere considerato come un punto nello spazio 3D. Ad esempio, il punto (1, 0, 0) nello spazio rappresenta il colore rosso e il punto (0, 1, 0) nello spazio rappresenta il colore verde.

Nella figura seguente viene illustrato il significato della rotazione del colore (1, 0, 0) tramite un angolo di 60 gradi nel piano Red-Green. La rotazione in un piano parallelo al piano di Red-Green può essere considerata come rotazione sull'asse blu.

![illustrazione che mostra il punto (1, 0, 0) ruotato di 60 gradi a (0,5, 0,866, 0)](images/recoloring04.png)

Nella figura seguente viene illustrato come inizializzare una matrice di colori per eseguire rotazioni su ognuno dei tre assi delle coordinate (rosso, verde, blu).

![illustrazione che mostra le matrici di colore che eseguono rotazioni su ognuno dei tre assi delle coordinate](images/recoloring05.png)

Nell'esempio seguente viene accettata un'immagine che corrisponde a un solo colore (1, 0, 0,6) e viene applicata una rotazione di 60 gradi sull'asse blu. L'angolo della rotazione viene eliminato in un piano parallelo al piano di Red-Green.


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



Nell'illustrazione seguente viene mostrata l'immagine originale a sinistra e l'immagine ruotata a colori a destra.

![illustrazione che mostra i rettangoli riempiti con l'immagine originale (violetto rosso) e l'immagine ruotata a colori (verde acqua)](images/colortrans5.png)

La rotazione dei colori eseguita nell'esempio di codice precedente può essere visualizzata come indicato di seguito.

![illustrazione che mostra uno spazio colore 3D e il punto (1, 0, 0,6) ruotato di 60 gradi a (0,5, 0,866, 0,6)](images/recoloring06.png)

 

 



