---
description: Windows GDI+ fornisce le classi di immagini e bitmap per l'archiviazione e la manipolazione delle immagini.
ms.assetid: fcd7f3d9-8bad-44f8-8c9c-c2f5df4a7241
title: Uso di una matrice di colori per trasformare un singolo colore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db56d0a64c36c08a5415d76e3fb184158d473268
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104557846"
---
# <a name="using-a-color-matrix-to-transform-a-single-color"></a>Uso di una matrice di colori per trasformare un singolo colore

Windows GDI+ fornisce le classi di [**Immagini**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) e [**bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) per l'archiviazione e la manipolazione delle immagini. Gli oggetti **Image** e **bitmap** memorizzano il colore di ogni pixel come numero a 32 bit: 8 bit per colore rosso, verde, blu e alfa. Ognuno dei quattro componenti è un numero compreso tra 0 e 255, 0 che rappresenta nessuna intensità e 255 che rappresenta l'intensità completa. Il componente alfa specifica la trasparenza del colore: 0 è completamente trasparente e 255 è completamente opaco.

Un vettore di colore è una tupla con 4 elementi del form (rosso, verde, blu, alfa). Ad esempio, il vettore di colore (0, 255, 0, 255) rappresenta un colore opaco che non ha rosso o blu, ma ha un verde a intensità piena.

Un'altra convenzione per la rappresentazione dei colori usa il numero 1 per l'intensità massima e il numero 0 per l'intensità minima. Usando tale convenzione, il colore descritto nel paragrafo precedente verrebbe rappresentato dal vettore (0, 1, 0, 1). GDI+ utilizza la convenzione di 1 come intensità completa durante le trasformazioni dei colori.

È possibile applicare trasformazioni lineari (rotazione, ridimensionamento e così via) ai vettori colori moltiplicando per una matrice 4 × 4. Tuttavia, non è possibile utilizzare una matrice 4 × 4 per eseguire una conversione (non lineare). Se si aggiunge una quinta coordinata fittizia, ad esempio il numero 1, a ogni vettore di colore, è possibile utilizzare una matrice di 5 × 5 per applicare qualsiasi combinazione di trasformazioni e traduzioni lineari. Una trasformazione costituita da una trasformazione lineare seguita da una traduzione è detta trasformazione affine. Una matrice di 5 × 5 che rappresenta una trasformazione affine è detta matrice omogenea per una trasformazione con 4 spazi. L'elemento nella quinta riga e nella quinta colonna di una matrice omogenea 5 × 5 deve essere 1 e tutte le altre voci della quinta colonna devono essere pari a 0.

Si supponga, ad esempio, di voler iniziare con il colore (0,2, 0,0, 0,4, 1,0) e applicare le trasformazioni seguenti:

1.  Raddoppiare il componente rosso
2.  Aggiungere 0,2 ai componenti rosso, verde e blu

La moltiplicazione di matrici seguente eseguirà la coppia di trasformazioni nell'ordine elencato.

![illustrazione che mostra una matrice 5x1 di numeri moltiplicata per una matrice 5x5 per creare una nuova matrice 5x1](images/recoloring01.png)

Gli elementi di una matrice di colori sono indicizzati (in base zero) per riga e quindi colonna. Ad esempio, la voce della quinta riga e della terza colonna della matrice M è indicata da M \[ 4 \] \[ 2 \] .

La matrice di identità 5 × 5 (mostrata nella figura seguente) presenta 1S sulla diagonale e sugli zeri in qualsiasi altra posizione. Se si moltiplica un vettore di colore per la matrice di identità, il vettore di colore non cambia. Un modo pratico per formare la matrice di una trasformazione colore consiste nell'iniziare con la matrice di identità e apportare una piccola modifica che produce la trasformazione desiderata.

![illustrazione che mostra una matrice di identità 5x5; 1S in alto a sinistra e in basso a destra diagonale e 0 in qualsiasi altra posizione](images/recoloring02.png)

Per una descrizione più dettagliata delle matrici e delle trasformazioni, vedere [sistemi di coordinate e trasformazioni](-gdiplus-coordinate-systems-and-transformations-about.md).

Nell'esempio seguente viene accettata un'immagine che corrisponde a un solo colore (0,2, 0,0, 0,4, 1,0) e viene applicata la trasformazione descritta nei paragrafi precedenti.


```
Image            image(L"InputColor.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   2.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 1.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 0.0f, 1.0f, 0.0f,
   0.2f, 0.2f, 0.2f, 0.0f, 1.0f};
   
imageAttributes.SetColorMatrix(
   &colorMatrix, 
   ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
   
graphics.DrawImage(&image, 10, 10);

graphics.DrawImage(
   &image, 
   Rect(120, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



Nell'illustrazione seguente viene mostrata l'immagine originale a sinistra e l'immagine trasformata a destra.

![illustrazione che mostra un rettangolo riempito da un colore a tinta unita scuro e quindi uno riempito con un colore a tinta unita più chiaro ](images/colortrans1.png)

Il codice nell'esempio precedente usa i passaggi seguenti per eseguire la ricolorazione:

1.  Inizializzare una struttura [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) .
2.  Creare un oggetto [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) e passare l'indirizzo della struttura [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) al metodo [**ImageAttributes:: SetColorMatrix**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix) dell'oggetto **ImageAttributes** .
3.  Passare l'indirizzo dell'oggetto [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) al metodo [DrawImage Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) di un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .

 

 



