---
description: Windows GDI+ fornisce la classe di immagini per l'utilizzo di immagini raster (bitmap) e di immagini vettoriali (Metafile).
ms.assetid: 57e3bf33-5490-4f4a-addf-356ef8f1aeed
title: Utilizzo di immagini, bitmap e metafile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 445b37caa488fa4b83bcfb7792eb83f6ee1e6e75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049856"
---
# <a name="using-images-bitmaps-and-metafiles"></a><span data-ttu-id="a42c3-103">Utilizzo di immagini, bitmap e metafile</span><span class="sxs-lookup"><span data-stu-id="a42c3-103">Using Images, Bitmaps, and Metafiles</span></span>

<span data-ttu-id="a42c3-104">Windows GDI+ [**fornisce la classe di immagini per**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) l'utilizzo di immagini raster (bitmap) e di immagini vettoriali (Metafile).</span><span class="sxs-lookup"><span data-stu-id="a42c3-104">Windows GDI+ provides the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class for working with raster images (bitmaps) and vector images (metafiles).</span></span> <span data-ttu-id="a42c3-105">La classe [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) e la classe [**metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) ereditano entrambe dalla classe **Image** .</span><span class="sxs-lookup"><span data-stu-id="a42c3-105">The [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) class and the [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) class both inherit from the **Image** class.</span></span> <span data-ttu-id="a42c3-106">La classe **bitmap** si espande sulle funzionalità della classe **Image** fornendo metodi aggiuntivi per il caricamento, il salvataggio e la modifica di immagini raster.</span><span class="sxs-lookup"><span data-stu-id="a42c3-106">The **Bitmap** class expands on the capabilities of the **Image** class by providing additional methods for loading, saving, and manipulating raster images.</span></span> <span data-ttu-id="a42c3-107">La classe **metafile** espande le funzionalità della classe **Image** fornendo metodi aggiuntivi per la registrazione e l'analisi di immagini vettoriali.</span><span class="sxs-lookup"><span data-stu-id="a42c3-107">The **Metafile** class expands on the capabilities of the **Image** class by providing additional methods for recording and examining vector images.</span></span>

<span data-ttu-id="a42c3-108">Negli argomenti seguenti vengono [**illustrate**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image)in modo più dettagliato le classi Image, [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)e [**metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) :</span><span class="sxs-lookup"><span data-stu-id="a42c3-108">The following topics cover the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image), [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap), and [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) classes in more detail:</span></span>

-   [<span data-ttu-id="a42c3-109">Caricamento e visualizzazione di bitmap</span><span class="sxs-lookup"><span data-stu-id="a42c3-109">Loading and Displaying Bitmaps</span></span>](-gdiplus-loading-and-displaying-bitmaps-use.md)
-   [<span data-ttu-id="a42c3-110">Caricamento e visualizzazione di metafile</span><span class="sxs-lookup"><span data-stu-id="a42c3-110">Loading and Displaying Metafiles</span></span>](-gdiplus-loading-and-displaying-metafiles-use.md)
-   [<span data-ttu-id="a42c3-111">Registrazione di metafile</span><span class="sxs-lookup"><span data-stu-id="a42c3-111">Recording Metafiles</span></span>](-gdiplus-recording-metafiles-use.md)
-   [<span data-ttu-id="a42c3-112">Ritaglio e ridimensionamento di immagini</span><span class="sxs-lookup"><span data-stu-id="a42c3-112">Cropping and Scaling Images</span></span>](-gdiplus-cropping-and-scaling-images-use.md)
-   [<span data-ttu-id="a42c3-113">Rotazione, Reflection e inclinazione di immagini</span><span class="sxs-lookup"><span data-stu-id="a42c3-113">Rotating, Reflecting, and Skewing Images</span></span>](-gdiplus-rotating-reflecting-and-skewing-images-use.md)
-   [<span data-ttu-id="a42c3-114">Uso della modalità di interpolazione per controllare la qualità dell'immagine durante il ridimensionamento</span><span class="sxs-lookup"><span data-stu-id="a42c3-114">Using Interpolation Mode to Control Image Quality During Scaling</span></span>](-gdiplus-using-interpolation-mode-to-control-image-quality-during-scaling-use.md)
-   [<span data-ttu-id="a42c3-115">Creazione di immagini di anteprima</span><span class="sxs-lookup"><span data-stu-id="a42c3-115">Creating Thumbnail Images</span></span>](-gdiplus-creating-thumbnail-images-use.md)
-   [<span data-ttu-id="a42c3-116">Utilizzo di una bitmap memorizzata nella cache per migliorare le prestazioni</span><span class="sxs-lookup"><span data-stu-id="a42c3-116">Using a Cached Bitmap to Improve Performance</span></span>](-gdiplus-using-a-cached-bitmap-to-improve-performance-use.md)
-   [<span data-ttu-id="a42c3-117">Miglioramento delle prestazioni evitando il ridimensionamento automatico</span><span class="sxs-lookup"><span data-stu-id="a42c3-117">Improving Performance by Avoiding Automatic Scaling</span></span>](-gdiplus-improving-performance-by-avoiding-automatic-scaling-use.md)
-   [<span data-ttu-id="a42c3-118">Lettura e scrittura di metadati</span><span class="sxs-lookup"><span data-stu-id="a42c3-118">Reading and Writing Metadata</span></span>](-gdiplus-reading-and-writing-metadata-use.md)

 

 



