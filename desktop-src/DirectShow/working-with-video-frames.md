---
description: Utilizzo di fotogrammi video
ms.assetid: a5ad74dd-abfd-4810-a512-42e4b98a6c59
title: Utilizzo di fotogrammi video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ead597fac5a28befc9c9868485840d03b46e5185
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313392"
---
# <a name="working-with-video-frames"></a><span data-ttu-id="958c8-103">Utilizzo di fotogrammi video</span><span class="sxs-lookup"><span data-stu-id="958c8-103">Working with Video Frames</span></span>

<span data-ttu-id="958c8-104">Il video non compresso è una sequenza di bitmap riprodotte in rapida successione, in genere con una frequenza di circa 30 fotogrammi al secondo.</span><span class="sxs-lookup"><span data-stu-id="958c8-104">Uncompressed video is a sequence of bitmaps played in rapid succession, typically at a rate of about 30 frames per second.</span></span> <span data-ttu-id="958c8-105">Poiché la maggior parte dei video entra in un grafico con filtro DirectShow in un formato compresso, il flusso video passa in genere a un decodificatore per la decompressione.</span><span class="sxs-lookup"><span data-stu-id="958c8-105">Because most video enters a DirectShow filter graph in a compressed format, the video stream generally goes through a decoder for decompression.</span></span> <span data-ttu-id="958c8-106">Molti decodificatori restituiscono dati in formato YUV e lasciano la conversione finale a RGB per l'hardware video appena prima del rendering.</span><span class="sxs-lookup"><span data-stu-id="958c8-106">Many decoders output data in a YUV format and leave the final conversion to RGB for the video hardware just prior to rendering.</span></span> <span data-ttu-id="958c8-107">Se un decodificatore usa l'accelerazione video DirectX, l'hardware video esegue operazioni aggiuntive per decodificare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="958c8-107">If a decoder uses DirectX Video Acceleration, the video hardware performs additional work to decode the image.</span></span> <span data-ttu-id="958c8-108">Pertanto, la decompressione finale delle bitmap potrebbe non essere eseguita fino a quando i dati non raggiungono l'hardware del video.</span><span class="sxs-lookup"><span data-stu-id="958c8-108">Thus, final decompression of the bitmaps may not be performed until the data reaches the video hardware.</span></span>

<span data-ttu-id="958c8-109">Tuttavia, per eseguire molti tipi di analisi video, elaborazione o modifica, è spesso necessario lavorare su bitmap non compresse in un tipo di formato RGB o YUV prima che vengano sottoposti a rendering o scritti nel file.</span><span class="sxs-lookup"><span data-stu-id="958c8-109">But to perform many types of video analysis, processing, or editing, it is often necessary to work on uncompressed bitmaps in some type of RGB or YUV format before they are rendered or written to file.</span></span> <span data-ttu-id="958c8-110">Questa operazione viene in genere eseguita in un filtro di trasformazione basato sulla classe di base [**CTransformFilter**](ctransformfilter.md) , in particolare nel metodo **Transform** .</span><span class="sxs-lookup"><span data-stu-id="958c8-110">This work is typically done within a transform filter based on the [**CTransformFilter**](ctransformfilter.md) base class, specifically in the **Transform** method.</span></span> <span data-ttu-id="958c8-111">Questo metodo riceve un puntatore a un oggetto [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) che incapsula i dati video.</span><span class="sxs-lookup"><span data-stu-id="958c8-111">This method receives a pointer to an [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) object that encapsulates the video data.</span></span> <span data-ttu-id="958c8-112">Il metodo **IMediaSample:: Getpointer** restituisce un puntatore al primo byte dei dati non elaborati.</span><span class="sxs-lookup"><span data-stu-id="958c8-112">The **IMediaSample::GetPointer** method returns a pointer to the first byte of the raw data.</span></span> <span data-ttu-id="958c8-113">Per i frame non compressi, i dati sono costituiti da pixel a cui è possibile accedere o che possono essere modificati direttamente dal filtro.</span><span class="sxs-lookup"><span data-stu-id="958c8-113">For uncompressed frames, this data consists of pixels that can be accessed or modified directly by the filter.</span></span> <span data-ttu-id="958c8-114">Nelle sezioni seguenti vengono fornite informazioni complementari che consentono di utilizzare in modo efficace i dati DIB.</span><span class="sxs-lookup"><span data-stu-id="958c8-114">The following sections provide background information that will help you work effectively with DIB data in this manner.</span></span>

> [!Note]  
> <span data-ttu-id="958c8-115">È anche possibile modificare i bit usando le funzioni GDI, GDI+, DirectDraw o Direct3D, ma queste tecniche esulano dall'ambito di questo articolo.</span><span class="sxs-lookup"><span data-stu-id="958c8-115">You can also modify the bits by using GDI, GDI+, DirectDraw or Direct3D functions, but these techniques are beyond the scope of this article.</span></span>

 

<span data-ttu-id="958c8-116">Questa sezione contiene i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="958c8-116">This section contains the following topics:</span></span>

-   [<span data-ttu-id="958c8-117">Top-down rispetto a Bottom-Up</span><span class="sxs-lookup"><span data-stu-id="958c8-117">Top-Down vs. Bottom-Up DIBs</span></span>](top-down-vs--bottom-up-dibs.md)
-   [<span data-ttu-id="958c8-118">Uso di RGB a 16 bit</span><span class="sxs-lookup"><span data-stu-id="958c8-118">Working with 16-bit RGB</span></span>](working-with-16-bit-rgb.md)

 

 



