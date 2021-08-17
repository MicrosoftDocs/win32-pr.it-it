---
description: Il remapping è il processo di conversione dei colori in un'immagine in base a una tabella di modifica del mapping dei colori. La tabella di modifica del mapping dei colori è una matrice di strutture ColorMap. Ogni struttura ColorMap nella matrice ha un membro oldColor e un membro newColor.
ms.assetid: 2b56ccd5-b9f3-4c5e-8a0b-4b3d1f2b7122
title: Uso di una tabella di rimappatura dei colori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a00f36c493bbdc696fa672b2899d4d7c6d3231a9e40c0e4162b5113d78a67164
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036299"
---
# <a name="using-a-color-remap-table"></a>Uso di una tabella di rimappatura dei colori

Il remapping è il processo di conversione dei colori in un'immagine in base a una tabella di modifica del mapping dei colori. La tabella di modifica del mapping dei colori è una matrice [**di strutture ColorMap.**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) Ogni **struttura ColorMap** nella matrice ha un **membro oldColor** e un **membro newColor.**

Quando GDI+ disegna un'immagine, ogni pixel dell'immagine viene confrontato con la matrice di colori vecchi. Se il colore di un pixel corrisponde a un colore precedente, il colore viene modificato nel nuovo colore corrispondente. I colori vengono modificati solo per il rendering. I valori dei colori dell'immagine stessa (archiviati in un [**oggetto Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) o [**Bitmap)**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) non vengono modificati.

Per disegnare un'immagine nuovamente mappata, inizializzare una matrice di [**strutture ColorMap.**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) Passare l'indirizzo di tale matrice al metodo [**ImageAttributes::SetRemapTable**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setremaptable) di un [**oggetto ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) e quindi passare l'indirizzo dell'oggetto **ImageAttributes** al metodo [DrawImage Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) di un [**oggetto Graphics.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)

Nell'esempio seguente viene creato [**un oggetto Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) dal file RemapInput.bmp. Il codice crea una tabella di modifica del mapping dei colori costituita da una singola [**struttura ColorMap.**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) Il **membro oldColor** della **struttura ColorMap** è rosso e il **membro newColor** è blu. L'immagine viene disegnata una volta senza modificare il mapping e una volta con il nuovo mapping. Il processo di modifica del mapping modifica tutti i pixel rossi in blu.


```
Image            image(L"RemapInput.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();
ColorMap         colorMap[1];

colorMap[0].oldColor = Color(255, 255, 0, 0);  // opaque red
colorMap[0].newColor = Color(255, 0, 0, 255);  // opaque blue

imageAttributes.SetRemapTable(1, colorMap, ColorAdjustTypeBitmap);

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



La figura seguente mostra l'immagine originale a sinistra e l'immagine mappata a destra.

![figura che mostra due versioni di un'immagine multicolore; l'area rossa nella prima versione è blu nella seconda versione](images/colortrans7.png)

 

 



