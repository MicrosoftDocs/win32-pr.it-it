---
description: È possibile usare la classe Image per caricare e visualizzare immagini raster (bitmap) e immagini vettoriali (Metafile).
ms.assetid: 0ad2a132-6db6-4099-81a2-10e1cd1b1f61
title: Disegno, posizionamento e clonazione delle immagini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa265a8f75cbfcaf0ff614ded4466482e5b986b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227081"
---
# <a name="drawing-positioning-and-cloning-images"></a>Disegno, posizionamento e clonazione delle immagini

È possibile usare la classe [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) per caricare e visualizzare immagini raster (bitmap) e immagini vettoriali (Metafile). Per visualizzare un'immagine, sono necessari un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e un oggetto **Image** . L'oggetto **Graphics** fornisce il metodo [**Graphics::D rawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) , che riceve l'indirizzo dell'oggetto **Image** come argomento.

Nell'esempio seguente viene creato un oggetto [**immagine**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) dal file Climber.jpg e quindi viene visualizzata l'immagine. Il punto di destinazione per l'angolo superiore sinistro dell'immagine, (10, 10), viene specificato nel secondo e terzo parametro del metodo [**Graphics::D rawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) .


```
Image myImage(L"Climber.jpg");
myGraphics.DrawImage(&myImage, 10, 10);
```



Il codice precedente, insieme a un determinato file Climber.jpg, ha prodotto l'output seguente.

![Screenshot di una finestra contenente una foto](images/aboutgdip03-art04.png)

È possibile costruire oggetti [**immagine**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) da un'ampia gamma di formati di file grafici: BMP, gif, JPEG, EXIF, PNG, TIFF, WMF, EMF e Icon.

Nell'esempio seguente vengono costruiti oggetti [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) da un'ampia gamma di tipi di file, quindi vengono visualizzate le immagini.


```
Image myBMP(L"SpaceCadet.bmp");
Image myEMF(L"Metafile1.emf");
Image myGIF(L"Soda.gif");
Image myJPEG(L"Mango.jpg");
Image myPNG(L"Flowers.png");
Image myTIFF(L"MS.tif");

myGraphics.DrawImage(&myBMP, 10, 10);
myGraphics.DrawImage(&myEMF, 220, 10);
myGraphics.DrawImage(&myGIF, 320, 10);
myGraphics.DrawImage(&myJPEG, 380, 10);
myGraphics.DrawImage(&myPNG, 150, 200);
myGraphics.DrawImage(&myTIFF, 300, 200);
```



La [**classe Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) fornisce un [**Metodo Image:: Clone**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-image-clone) che è possibile usare per creare una copia di un' **immagine**, un [**metafile**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-metafile)o un oggetto [**bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) esistente. Il metodo [Clone](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-bitmap-clone(inconstrectf__inpixelformat)) viene sottomesso a overload nella classe **bitmap** e una delle varianti dispone di un parametro source-Rectangle che è possibile usare per specificare la porzione dell'immagine originale che si vuole copiare. Nell'esempio seguente viene creato un oggetto **bitmap** clonando la metà superiore di un oggetto **bitmap** esistente. Vengono quindi visualizzate entrambe le immagini.


```
Bitmap* originalBitmap = new Bitmap(L"Spiral.png");
RectF sourceRect(
   0.0f,
   0.0f, 
   (REAL)(originalBitmap->GetWidth()), 
   (REAL)(originalBitmap->GetHeight())/2.0f);

Bitmap* secondBitmap = originalBitmap->Clone(sourceRect, PixelFormatDontCare);

myGraphics.DrawImage(originalBitmap, 10, 10);
myGraphics.DrawImage(secondBitmap, 100, 10);
```



Il codice precedente, insieme a un determinato file Spiral.png, ha prodotto l'output seguente.

![illustrazione di un'immagine, seguita dalla metà superiore dell'immagine originale](images/aboutgdip03-art05.png)

 

 
