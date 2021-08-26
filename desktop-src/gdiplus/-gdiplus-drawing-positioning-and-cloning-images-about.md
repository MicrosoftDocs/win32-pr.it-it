---
description: È possibile usare la classe Image per caricare e visualizzare immagini raster (bitmap) e immagini vettoriali (metafile).
ms.assetid: 0ad2a132-6db6-4099-81a2-10e1cd1b1f61
title: Disegno, posizionamento e clonazione delle immagini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e37e53ce3937d4f10b91a92e64feec57c6b39e718e7b551e4e4130569d4dd90d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015151"
---
# <a name="drawing-positioning-and-cloning-images"></a>Disegno, posizionamento e clonazione delle immagini

È possibile usare la [**classe Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) per caricare e visualizzare immagini raster (bitmap) e immagini vettoriali (metafile). Per visualizzare un'immagine, sono necessari un [**oggetto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e un **oggetto Image.** **L'oggetto Graphics** fornisce il [**metodo Graphics::D rawImage,**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) che riceve l'indirizzo dell'oggetto **Image** come argomento.

L'esempio seguente costruisce un [**oggetto Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) dal file Climber.jpg e quindi visualizza l'immagine. Il punto di destinazione per l'angolo superiore sinistro dell'immagine (10, 10) viene specificato nel secondo e nel terzo parametro del metodo [**Graphics::D rawImage.**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint))


```
Image myImage(L"Climber.jpg");
myGraphics.DrawImage(&myImage, 10, 10);
```



Il codice precedente, insieme a un file specifico, Climber.jpg, ha prodotto l'output seguente.

![Screenshot di una finestra contenente una foto](images/aboutgdip03-art04.png)

È possibile costruire oggetti [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) da un'ampia gamma di formati di file grafici: BMP, GIF, JPEG, Exif, PNG, TIFF, WMF, EMF e ICON.

L'esempio seguente costruisce [**oggetti Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) da diversi tipi di file e quindi visualizza le immagini.


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



La [**classe Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) fornisce un metodo [**Image::Clone**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-image-clone) che è possibile usare per creare una copia di un oggetto **Image,** [**Metafile**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-metafile)o [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) esistente. Il [metodo Clone](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-bitmap-clone(inconstrectf__inpixelformat)) viene sottoposto a overload nella classe **Bitmap** e una delle varianti ha un parametro del rettangolo di origine che è possibile usare per specificare la parte dell'immagine originale da copiare. Nell'esempio seguente viene creato un **oggetto Bitmap** clonando la metà superiore di un oggetto **Bitmap** esistente. Vengono quindi visualizzate entrambe le immagini.


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



Il codice precedente, insieme a un file specifico, Spiral.png, ha prodotto l'output seguente.

![illustrazione di un'immagine, seguita dalla metà superiore dell'immagine orignale](images/aboutgdip03-art05.png)

 

 
