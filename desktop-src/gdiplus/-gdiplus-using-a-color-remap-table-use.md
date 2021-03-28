---
description: Il rimapping è il processo di conversione dei colori in un'immagine in base a una tabella di modifica del mapping dei colori. La tabella di modifica del mapping dei colori è una matrice di strutture mappate. Ogni struttura della mappa colori nella matrice ha un membro oldColor e un membro newColor.
ms.assetid: 2b56ccd5-b9f3-4c5e-8a0b-4b3d1f2b7122
title: Uso di una tabella di rimappatura dei colori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1c07bc0a67a02ea07aeaa3931e661af5665e33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129055"
---
# <a name="using-a-color-remap-table"></a>Uso di una tabella di rimappatura dei colori

Il rimapping è il processo di conversione dei colori in un'immagine in base a una tabella di modifica del mapping dei colori. La tabella di modifica del mapping dei colori è una matrice di strutture [**mappate**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) . Ogni struttura della **mappa colori** nella matrice ha un membro **oldColor** e un membro **NewColor** .

Quando GDI+ disegna un'immagine, ogni pixel dell'immagine viene confrontato con la matrice dei colori precedenti. Se il colore di un pixel corrisponde a un colore precedente, il colore viene modificato nel nuovo colore corrispondente. I colori vengono modificati solo per il rendering: i valori dei colori dell'immagine stessa (archiviati in un' [**immagine**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) o in un oggetto [**bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) ) non vengono modificati.

Per tracciare un'immagine rimappata, inizializzare una matrice di strutture della [**mappa colori**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) . Passare l'indirizzo della matrice al metodo [**ImageAttributes:: SetRemapTable**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setremaptable) di un oggetto [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) , quindi passare l'indirizzo dell'oggetto **ImageAttributes** al metodo [DrawImage Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) di un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .

Nell'esempio seguente viene creato un oggetto [**immagine**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) dal file RemapInput.bmp. Il codice consente di creare una tabella di modifica del mapping dei colori costituita da una singola struttura della [**mappa colori**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) . Il membro **oldColor** della struttura **mappa colori** è rosso e il membro **NewColor** è blu. L'immagine viene disegnata una volta senza modificarne il mapping e una volta con il mapping. Il processo di modifica del mapping modifica tutti i pixel rossi in blu.


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



Nell'illustrazione seguente viene mostrata l'immagine originale a sinistra e l'immagine rimappata a destra.

![illustrazione che mostra due versioni di un'immagine multicolore; l'area rossa nella prima versione è blu nella seconda versione](images/colortrans7.png)

 

 



