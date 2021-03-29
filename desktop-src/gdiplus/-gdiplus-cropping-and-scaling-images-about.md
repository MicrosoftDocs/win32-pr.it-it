---
title: Informazioni sul ritaglio e sul ridimensionamento di immagini GDI+
description: È possibile usare il metodo DrawImage della classe Graphics per creare e posizionare le immagini.
ms.assetid: 81d20adc-0481-4b1b-80aa-ae218fdecd84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b44a13b5cee632e6ceafe327f94eca48edd93dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131354"
---
# <a name="about-cropping-and-scaling-gdi-images"></a><span data-ttu-id="7ec9a-103">Informazioni sul ritaglio e sul ridimensionamento di immagini GDI+</span><span class="sxs-lookup"><span data-stu-id="7ec9a-103">About cropping and scaling GDI+ images</span></span>

<span data-ttu-id="7ec9a-104">È possibile usare il metodo [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) della classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) per creare e posizionare le immagini.</span><span class="sxs-lookup"><span data-stu-id="7ec9a-104">You can use the [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to draw and position images.</span></span> <span data-ttu-id="7ec9a-105">DrawImage è un metodo di overload, quindi è possibile fornire gli argomenti in diversi modi.</span><span class="sxs-lookup"><span data-stu-id="7ec9a-105">DrawImage is an overloaded method, so there are several ways you can supply it with arguments.</span></span> <span data-ttu-id="7ec9a-106">Una variante del metodo [**Graphics::D rawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) riceve l'indirizzo di un oggetto [**immagine**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) e un riferimento a un oggetto [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) .</span><span class="sxs-lookup"><span data-stu-id="7ec9a-106">One variation of the [**Graphics::DrawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) method receives the address of an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object and a reference to a [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) object.</span></span> <span data-ttu-id="7ec9a-107">Il rettangolo specifica la destinazione per l'operazione di disegno. ovvero specifica il rettangolo in cui verrà disegnata l'immagine.</span><span class="sxs-lookup"><span data-stu-id="7ec9a-107">The rectangle specifies the destination for the drawing operation; that is, it specifies the rectangle in which the image will be drawn.</span></span> <span data-ttu-id="7ec9a-108">Se le dimensioni del rettangolo di destinazione sono diverse da quelle dell'immagine originale, l'immagine viene ridimensionata in modo da adattarsi al rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7ec9a-108">If the size of the destination rectangle is different from the size of the original image, the image is scaled to fit the destination rectangle.</span></span> <span data-ttu-id="7ec9a-109">Nell'esempio seguente viene disegnata la stessa immagine tre volte: una volta senza scalabilità, una volta con un'espansione e una volta con una compressione.</span><span class="sxs-lookup"><span data-stu-id="7ec9a-109">The following example draws the same image three times: once with no scaling, once with an expansion, and once with a compression.</span></span>


```
Bitmap myBitmap(L"Spiral.png");
Rect expansionRect(80, 10, 2 * myBitmap.GetWidth(), myBitmap.GetHeight());
Rect compressionRect(210, 10, myBitmap.GetWidth() / 2, 
   myBitmap.GetHeight() / 2);

myGraphics.DrawImage(&myBitmap, 10, 10);
myGraphics.DrawImage(&myBitmap, expansionRect);
myGraphics.DrawImage(&myBitmap, compressionRect);
```



<span data-ttu-id="7ec9a-110">Il codice precedente, insieme a un determinato file Spiral.png, ha prodotto l'output seguente.</span><span class="sxs-lookup"><span data-stu-id="7ec9a-110">The preceding code, along with a particular file, Spiral.png, produced the following output.</span></span>

![illustrazione che mostra tre versioni di un'immagine: normale, estesa e compattata a metà delle dimensioni originali](images/aboutgdip03-art06.png)

<span data-ttu-id="7ec9a-112">Alcune varianti della [**grafica::D Metodo rawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) hanno un parametro source-Rectangle, oltre a un parametro Destination-Rectangle.</span><span class="sxs-lookup"><span data-stu-id="7ec9a-112">Some variations of the [**Graphics::DrawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) method have a source-rectangle parameter as well as a destination-rectangle parameter.</span></span> <span data-ttu-id="7ec9a-113">Il rettangolo di origine specifica la parte dell'immagine originale che verrà disegnata.</span><span class="sxs-lookup"><span data-stu-id="7ec9a-113">The source rectangle specifies the portion of the original image that will be drawn.</span></span> <span data-ttu-id="7ec9a-114">Il rettangolo di destinazione specifica il punto in cui verrà disegnata la parte dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="7ec9a-114">The destination rectangle specifies where that portion of the image will be drawn.</span></span> <span data-ttu-id="7ec9a-115">Se le dimensioni del rettangolo di destinazione sono diverse dalla dimensione del rettangolo di origine, l'immagine viene ridimensionata in modo da adattarsi al rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7ec9a-115">If the size of the destination rectangle is different from the size of the source rectangle, the image is scaled to fit the destination rectangle.</span></span>

<span data-ttu-id="7ec9a-116">Nell'esempio seguente viene costruito un oggetto [**bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) dal file Runner.jpg.</span><span class="sxs-lookup"><span data-stu-id="7ec9a-116">The following example constructs a [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object from the file Runner.jpg.</span></span> <span data-ttu-id="7ec9a-117">L'intera immagine viene disegnata senza alcun ridimensionamento in corrispondenza di (0, 0).</span><span class="sxs-lookup"><span data-stu-id="7ec9a-117">The entire image is drawn with no scaling at (0, 0).</span></span> <span data-ttu-id="7ec9a-118">Una piccola parte dell'immagine viene disegnata due volte: una volta con una compressione e una volta con un'espansione.</span><span class="sxs-lookup"><span data-stu-id="7ec9a-118">Then a small portion of the image is drawn twice: once with a compression and once with an expansion.</span></span>


```
Bitmap myBitmap(L"Runner.jpg"); 

// The rectangle (in myBitmap) with upper-left corner (80, 70), 
// width 80, and height 45, encloses one of the runner's hands.

// Small destination rectangle for compressed hand.
Rect destRect1(200, 10, 20, 16);

// Large destination rectangle for expanded hand.
Rect destRect2(200, 40, 200, 160);

// Draw the original image at (0, 0).
myGraphics.DrawImage(&myBitmap, 0, 0);

// Draw the compressed hand.
myGraphics.DrawImage(
   &myBitmap, destRect1, 80, 70, 80, 45, UnitPixel);

// Draw the expanded hand. 
myGraphics.DrawImage(
   &myBitmap, destRect2, 80, 70, 80, 45, UnitPixel);
```



<span data-ttu-id="7ec9a-119">Nella figura seguente viene illustrata l'immagine non ridimensionata e le parti di immagine compresse ed espanse.</span><span class="sxs-lookup"><span data-stu-id="7ec9a-119">The following illustration shows the unscaled image, and the compressed and expanded image portions.</span></span>

![screenshot che mostra un'immagine, una parte dell'immagine compressa e quindi la stessa parte espansa](images/aboutgdip03-art07.png)

 

 



