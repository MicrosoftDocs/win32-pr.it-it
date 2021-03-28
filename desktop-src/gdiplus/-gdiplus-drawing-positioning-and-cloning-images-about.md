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
# <a name="drawing-positioning-and-cloning-images"></a><span data-ttu-id="80a29-103">Disegno, posizionamento e clonazione delle immagini</span><span class="sxs-lookup"><span data-stu-id="80a29-103">Drawing, Positioning, and Cloning Images</span></span>

<span data-ttu-id="80a29-104">È possibile usare la classe [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) per caricare e visualizzare immagini raster (bitmap) e immagini vettoriali (Metafile).</span><span class="sxs-lookup"><span data-stu-id="80a29-104">You can use the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class to load and display raster images (bitmaps) and vector images (metafiles).</span></span> <span data-ttu-id="80a29-105">Per visualizzare un'immagine, sono necessari un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e un oggetto **Image** .</span><span class="sxs-lookup"><span data-stu-id="80a29-105">To display an image, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and an **Image** object.</span></span> <span data-ttu-id="80a29-106">L'oggetto **Graphics** fornisce il metodo [**Graphics::D rawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) , che riceve l'indirizzo dell'oggetto **Image** come argomento.</span><span class="sxs-lookup"><span data-stu-id="80a29-106">The **Graphics** object provides the [**Graphics::DrawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) method, which receives the address of the **Image** object as an argument.</span></span>

<span data-ttu-id="80a29-107">Nell'esempio seguente viene creato un oggetto [**immagine**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) dal file Climber.jpg e quindi viene visualizzata l'immagine.</span><span class="sxs-lookup"><span data-stu-id="80a29-107">The following example constructs an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file Climber.jpg and then displays the image.</span></span> <span data-ttu-id="80a29-108">Il punto di destinazione per l'angolo superiore sinistro dell'immagine, (10, 10), viene specificato nel secondo e terzo parametro del metodo [**Graphics::D rawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) .</span><span class="sxs-lookup"><span data-stu-id="80a29-108">The destination point for the upper-left corner of the image, (10, 10), is specified in the second and third parameters of the [**Graphics::DrawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) method.</span></span>


```
Image myImage(L"Climber.jpg");
myGraphics.DrawImage(&myImage, 10, 10);
```



<span data-ttu-id="80a29-109">Il codice precedente, insieme a un determinato file Climber.jpg, ha prodotto l'output seguente.</span><span class="sxs-lookup"><span data-stu-id="80a29-109">The preceding code, along with a particular file, Climber.jpg, produced the following output.</span></span>

![Screenshot di una finestra contenente una foto](images/aboutgdip03-art04.png)

<span data-ttu-id="80a29-111">È possibile costruire oggetti [**immagine**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) da un'ampia gamma di formati di file grafici: BMP, gif, JPEG, EXIF, PNG, TIFF, WMF, EMF e Icon.</span><span class="sxs-lookup"><span data-stu-id="80a29-111">You can construct [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) objects from a variety of graphics file formats: BMP, GIF, JPEG, Exif, PNG, TIFF, WMF, EMF, and ICON.</span></span>

<span data-ttu-id="80a29-112">Nell'esempio seguente vengono costruiti oggetti [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) da un'ampia gamma di tipi di file, quindi vengono visualizzate le immagini.</span><span class="sxs-lookup"><span data-stu-id="80a29-112">The following example constructs [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) objects from a variety of file types and then displays the images.</span></span>


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



<span data-ttu-id="80a29-113">La [**classe Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) fornisce un [**Metodo Image:: Clone**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-image-clone) che è possibile usare per creare una copia di un' **immagine**, un [**metafile**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-metafile)o un oggetto [**bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) esistente.</span><span class="sxs-lookup"><span data-stu-id="80a29-113">The [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class provides a [**Image::Clone**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-image-clone) method that you can use to make a copy of an existing **Image**, [**Metafile**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-metafile), or [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object.</span></span> <span data-ttu-id="80a29-114">Il metodo [Clone](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-bitmap-clone(inconstrectf__inpixelformat)) viene sottomesso a overload nella classe **bitmap** e una delle varianti dispone di un parametro source-Rectangle che è possibile usare per specificare la porzione dell'immagine originale che si vuole copiare.</span><span class="sxs-lookup"><span data-stu-id="80a29-114">The [Clone](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-bitmap-clone(inconstrectf__inpixelformat)) method is overloaded in the **Bitmap** class, and one of the variations has a source-rectangle parameter that you can use to specify the portion of the original image that you want to copy.</span></span> <span data-ttu-id="80a29-115">Nell'esempio seguente viene creato un oggetto **bitmap** clonando la metà superiore di un oggetto **bitmap** esistente.</span><span class="sxs-lookup"><span data-stu-id="80a29-115">The following example creates a **Bitmap** object by cloning the top half of an existing **Bitmap** object.</span></span> <span data-ttu-id="80a29-116">Vengono quindi visualizzate entrambe le immagini.</span><span class="sxs-lookup"><span data-stu-id="80a29-116">Then both images are displayed.</span></span>


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



<span data-ttu-id="80a29-117">Il codice precedente, insieme a un determinato file Spiral.png, ha prodotto l'output seguente.</span><span class="sxs-lookup"><span data-stu-id="80a29-117">The preceding code, along with a particular file, Spiral.png, produced the following output.</span></span>

![illustrazione di un'immagine, seguita dalla metà superiore dell'immagine originale](images/aboutgdip03-art05.png)

 

 
