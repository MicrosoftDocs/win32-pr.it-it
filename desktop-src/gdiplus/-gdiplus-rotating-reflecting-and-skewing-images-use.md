---
description: È possibile ruotare, riflettere e inclinare un'immagine specificando punti di destinazione per gli angoli superiore sinistro, superiore destro e inferiore sinistro dell'immagine originale.
ms.assetid: 1e982d84-8749-451b-89a8-81440fcee439
title: Rotazione, Reflection e inclinazione di immagini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5637cb8be0290d96a164042086e997bc878c0227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967198"
---
# <a name="rotating-reflecting-and-skewing-images"></a>Rotazione, Reflection e inclinazione di immagini

È possibile ruotare, riflettere e inclinare un'immagine specificando punti di destinazione per gli angoli superiore sinistro, superiore destro e inferiore sinistro dell'immagine originale. I tre punti di destinazione determinano una trasformazione affine che esegue il mapping dell'immagine rettangolare originale a un parallelogramma. L'angolo inferiore destro dell'immagine originale viene mappato al quarto angolo del parallelogramma, che viene calcolato dai tre punti di destinazione specificati.

Si supponga, ad esempio, che l'immagine originale sia un rettangolo con angolo superiore sinistro in corrispondenza di (0, 0), angolo superiore destro in corrispondenza di (100, 0) e angolo inferiore sinistro in (0, 50). Si supponga ora di eseguire il mapping di questi tre punti ai punti di destinazione come indicato di seguito.



| Punto originale       | Punto di destinazione |
|----------------------|-------------------|
| Superiore sinistro (0,0)    | (200, 20)         |
| In alto a destra (100, 0) | (110, 100)        |
| In basso a sinistra (0, 50)   | (250, 30)         |



 

La figura seguente mostra l'immagine originale e l'immagine mappata al parallelogramma. L'immagine originale è stata inclinata, riflessa, ruotata e convertita. L'asse x lungo il bordo superiore dell'immagine originale viene mappato alla riga che esegue fino a (200, 20) e (110, 100). L'asse y lungo il bordo sinistro dell'immagine originale viene mappato alla riga che esegue fino a (200, 20) e (250, 30).

![illustrazione che mostra strisce colorate all'origine degli assi delle coordinate e le stesse strisce inclinate e in una posizione, una rotazione e una dimensione diverse](images/stripes1.png)

Nell'esempio seguente vengono generate le immagini mostrate nella figura precedente.


```
Point destinationPoints[] = {
   Point(200, 20),   // destination for upper-left point of original
   Point(110, 100),  // destination for upper-right point of original
   Point(250, 30)};  // destination for lower-left point of original
Image image(L"Stripes.bmp");
// Draw the image unaltered with its upper-left corner at (0, 0).
graphics.DrawImage(&image, 0, 0);
// Draw the image mapped to the parallelogram.
graphics.DrawImage(&image, destinationPoints, 3); 
```



Nella figura seguente viene illustrata una trasformazione simile applicata a un'immagine fotografica.

![illustrazione che mostra la stessa foto due volte. il secondo è invertito, inclinato e ha dimensioni, rotazione e posizione diverse](images/transformedclimber.png)

Nella figura seguente viene illustrata una trasformazione simile applicata a un metafile.

![illustrazione che mostra le forme e il testo, quindi ancora una volta invertita, asimmetrica e con posizioni, rotazione e dimensioni diverse](images/transformedmetafile.png)

 

 



