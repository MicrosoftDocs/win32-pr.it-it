---
description: Per visualizzare un'immagine raster (bitmap) sullo schermo, sono necessari un oggetto immagine e un oggetto Graphics.
ms.assetid: 8c1a26d9-b640-4f38-8276-10c4464525f2
title: Caricamento e visualizzazione di bitmap
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: ab2405462db5017215893d50d93dc0b228633cfb
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/20/2021
ms.locfileid: "104982843"
---
# <a name="loading-and-displaying-bitmaps"></a><span data-ttu-id="33385-103">Caricamento e visualizzazione di bitmap</span><span class="sxs-lookup"><span data-stu-id="33385-103">Loading and displaying bitmaps</span></span>

<span data-ttu-id="33385-104">Vedere anche l' [app di esempio GDI+ visualizzatore WIC](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus).</span><span class="sxs-lookup"><span data-stu-id="33385-104">Also see the [WIC Viewer GDI+ sample app](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus).</span></span>

<span data-ttu-id="33385-105">Per visualizzare un'immagine raster (bitmap) sullo schermo, sono necessari un oggetto [**immagine**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="33385-105">To display a raster image (bitmap) on the screen, you need an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="33385-106">Passare il nome di un file (o un puntatore a un flusso) a un costruttore di **immagine** .</span><span class="sxs-lookup"><span data-stu-id="33385-106">Pass the name of a file (or a pointer to a stream) to an **Image** constructor.</span></span> <span data-ttu-id="33385-107">Dopo aver creato un oggetto **immagine** , passare l'indirizzo dell'oggetto **immagine** al metodo **DrawImage** di un oggetto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="33385-107">After you have created an **Image** object, pass the address of that **Image** object to the **DrawImage** method of a **Graphics** object.</span></span>

<span data-ttu-id="33385-108">Nell'esempio seguente viene creato un oggetto [**immagine**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) da un file JPEG, quindi viene disegnata l'immagine con l'angolo superiore sinistro in (60, 10):</span><span class="sxs-lookup"><span data-stu-id="33385-108">The following example creates an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from a JPEG file and then draws the image with its upper-left corner at (60, 10):</span></span>

```cpp
Image image(L"Grapes.jpg");
graphics.DrawImage(&image, 60, 10);
```

<span data-ttu-id="33385-109">Nella figura seguente viene illustrata l'immagine disegnata nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="33385-109">The following illustration shows the image drawn at the specified location.</span></span>

![<span data-ttu-id="33385-110">Screenshot di una finestra che contiene un'immagine, con un callout per il punto di origine</span><span class="sxs-lookup"><span data-stu-id="33385-110">screen shot of a window that contains an image, with a callout for the origin point</span></span> ](images/imageposition1.png)

<span data-ttu-id="33385-111">La classe [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) fornisce metodi di base per il caricamento e la visualizzazione di immagini raster e vettoriali.</span><span class="sxs-lookup"><span data-stu-id="33385-111">The [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class provides basic methods for loading and displaying raster images and vector images.</span></span> <span data-ttu-id="33385-112">La classe [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) , che eredita dalla classe **Image** , fornisce metodi più specializzati per il caricamento, la visualizzazione e la manipolazione delle immagini raster.</span><span class="sxs-lookup"><span data-stu-id="33385-112">The [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) class, which inherits from the **Image** class, provides more specialized methods for loading, displaying, and manipulating raster images.</span></span> <span data-ttu-id="33385-113">È ad esempio possibile costruire un oggetto **bitmap** da un handle di icona (HICON).</span><span class="sxs-lookup"><span data-stu-id="33385-113">For example, you can construct a **Bitmap** object from an icon handle (HICON).</span></span>

<span data-ttu-id="33385-114">Nell'esempio seguente viene ottenuto un handle per un'icona e quindi viene utilizzato tale handle per costruire un oggetto [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) .</span><span class="sxs-lookup"><span data-stu-id="33385-114">The following example obtains a handle to an icon and then uses that handle to construct a [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object.</span></span> <span data-ttu-id="33385-115">Il codice Visualizza l'icona passando l'indirizzo dell'oggetto **bitmap** al metodo **DrawImage** di un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="33385-115">The code displays the icon by passing the address of the **Bitmap** object to the **DrawImage** method of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>

```cpp
HICON hIcon = LoadIcon(NULL, IDI_APPLICATION);
Bitmap bitmap(hIcon);
graphics.DrawImage(&bitmap, 10, 10);
```

## <a name="see-also"></a><span data-ttu-id="33385-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33385-116">See also</span></span>

[<span data-ttu-id="33385-117">App di esempio GDI+ visualizzatore WIC</span><span class="sxs-lookup"><span data-stu-id="33385-117">WIC Viewer GDI+ sample app</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus)
