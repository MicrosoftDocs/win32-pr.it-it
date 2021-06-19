---
description: Informazioni sull'uso di immagini, bitmap e metafile. GDI+ di Windows fornisce la classe Image per l'uso di immagini raster (bitmap) e immagini vettoriali (metafile).
ms.assetid: 57e3bf33-5490-4f4a-addf-356ef8f1aeed
title: Uso di immagini, bitmap e metafile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d0603c8a428c45feac8cdeb47a46b61dc5e3bd
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395536"
---
# <a name="using-images-bitmaps-and-metafiles"></a><span data-ttu-id="37d30-104">Uso di immagini, bitmap e metafile</span><span class="sxs-lookup"><span data-stu-id="37d30-104">Using Images, Bitmaps, and Metafiles</span></span>

<span data-ttu-id="37d30-105">GDI+ di Windows fornisce la [**classe Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) per l'uso di immagini raster (bitmap) e immagini vettoriali (metafile).</span><span class="sxs-lookup"><span data-stu-id="37d30-105">Windows GDI+ provides the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class for working with raster images (bitmaps) and vector images (metafiles).</span></span> <span data-ttu-id="37d30-106">La [**classe Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) e la classe [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) ereditano entrambe dalla **classe** Image.</span><span class="sxs-lookup"><span data-stu-id="37d30-106">The [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) class and the [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) class both inherit from the **Image** class.</span></span> <span data-ttu-id="37d30-107">La **classe Bitmap** si espande sulle funzionalità della classe **Image** fornendo metodi aggiuntivi per il caricamento, il salvataggio e la modifica delle immagini raster.</span><span class="sxs-lookup"><span data-stu-id="37d30-107">The **Bitmap** class expands on the capabilities of the **Image** class by providing additional methods for loading, saving, and manipulating raster images.</span></span> <span data-ttu-id="37d30-108">La **classe Metafile** si espande sulle funzionalità della classe **Image** fornendo metodi aggiuntivi per la registrazione e l'analisi delle immagini vettoriali.</span><span class="sxs-lookup"><span data-stu-id="37d30-108">The **Metafile** class expands on the capabilities of the **Image** class by providing additional methods for recording and examining vector images.</span></span>

<span data-ttu-id="37d30-109">Negli argomenti seguenti vengono fornite informazioni più [**dettagliate sulle**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)classi [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image), Bitmap e [**Metafile:**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile)</span><span class="sxs-lookup"><span data-stu-id="37d30-109">The following topics cover the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image), [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap), and [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) classes in more detail:</span></span>

-   [<span data-ttu-id="37d30-110">Caricamento e visualizzazione di bitmap</span><span class="sxs-lookup"><span data-stu-id="37d30-110">Loading and Displaying Bitmaps</span></span>](-gdiplus-loading-and-displaying-bitmaps-use.md)
-   [<span data-ttu-id="37d30-111">Caricamento e visualizzazione di metafile</span><span class="sxs-lookup"><span data-stu-id="37d30-111">Loading and Displaying Metafiles</span></span>](-gdiplus-loading-and-displaying-metafiles-use.md)
-   [<span data-ttu-id="37d30-112">Registrazione di metafile</span><span class="sxs-lookup"><span data-stu-id="37d30-112">Recording Metafiles</span></span>](-gdiplus-recording-metafiles-use.md)
-   [<span data-ttu-id="37d30-113">Ritaglio e ridimensionamento delle immagini</span><span class="sxs-lookup"><span data-stu-id="37d30-113">Cropping and Scaling Images</span></span>](-gdiplus-cropping-and-scaling-images-use.md)
-   [<span data-ttu-id="37d30-114">Rotazione, riflessione e inclinazione delle immagini</span><span class="sxs-lookup"><span data-stu-id="37d30-114">Rotating, Reflecting, and Skewing Images</span></span>](-gdiplus-rotating-reflecting-and-skewing-images-use.md)
-   [<span data-ttu-id="37d30-115">Uso della modalità di interpolazione per controllare la qualità dell'immagine durante il ridimensionamento</span><span class="sxs-lookup"><span data-stu-id="37d30-115">Using Interpolation Mode to Control Image Quality During Scaling</span></span>](-gdiplus-using-interpolation-mode-to-control-image-quality-during-scaling-use.md)
-   [<span data-ttu-id="37d30-116">Creazione di immagini di anteprima</span><span class="sxs-lookup"><span data-stu-id="37d30-116">Creating Thumbnail Images</span></span>](-gdiplus-creating-thumbnail-images-use.md)
-   [<span data-ttu-id="37d30-117">Uso di una bitmap memorizzata nella cache per migliorare le prestazioni</span><span class="sxs-lookup"><span data-stu-id="37d30-117">Using a Cached Bitmap to Improve Performance</span></span>](-gdiplus-using-a-cached-bitmap-to-improve-performance-use.md)
-   [<span data-ttu-id="37d30-118">Miglioramento delle prestazioni evitando il ridimensionamento automatico</span><span class="sxs-lookup"><span data-stu-id="37d30-118">Improving Performance by Avoiding Automatic Scaling</span></span>](-gdiplus-improving-performance-by-avoiding-automatic-scaling-use.md)
-   [<span data-ttu-id="37d30-119">Lettura e scrittura di metadati</span><span class="sxs-lookup"><span data-stu-id="37d30-119">Reading and Writing Metadata</span></span>](-gdiplus-reading-and-writing-metadata-use.md)

 

 



