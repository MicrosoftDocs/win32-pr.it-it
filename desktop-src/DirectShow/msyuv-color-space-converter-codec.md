---
description: MSYUV è un codec di convertitore dello spazio colore da YUV a RGB.
ms.assetid: 77b00937-ac63-4b23-b546-c0896b3c57ba
title: Codec MSYUV Color Space Converter
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 838e7cd749042b2fb97adaf0b2b4cd0378a81c07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332635"
---
# <a name="msyuv-color-space-converter-codec"></a><span data-ttu-id="6fb81-103">Codec MSYUV Color Space Converter</span><span class="sxs-lookup"><span data-stu-id="6fb81-103">MSYUV Color Space Converter Codec</span></span>

<span data-ttu-id="6fb81-104">MSYUV è un codec di convertitore dello spazio colore da YUV a RGB.</span><span class="sxs-lookup"><span data-stu-id="6fb81-104">MSYUV is a YUV-to-RGB color space converter codec.</span></span> <span data-ttu-id="6fb81-105">Consente la riproduzione dei dati di origine video in formati YUV nei client la cui scheda video non può essere usata per le conversioni da YUV a RGB nell'hardware.</span><span class="sxs-lookup"><span data-stu-id="6fb81-105">It enables playback of video source data in YUV formats on clients whose video display adapter cannot be used for YUV-to-RGB conversions in hardware.</span></span> <span data-ttu-id="6fb81-106">Il codec partecipa ai grafici dei filtri tramite il filtro del wrapper di [decompressione AVI](avi-decompressor-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="6fb81-106">The codec participates in filter graphs through the [AVI Decompressor](avi-decompressor-filter.md) wrapper filter.</span></span>

<span data-ttu-id="6fb81-107">Le videocamere digitali per la comunicazione con 1394 o le interfacce USB possono produrre dati di immagini in diversi formati YUV.</span><span class="sxs-lookup"><span data-stu-id="6fb81-107">Digital conferencing cameras with 1394 or USB interfaces can produce image data in various YUV formats.</span></span> <span data-ttu-id="6fb81-108">Se l'hardware di visualizzazione non supporta la conversione da YUV a RGB a bordo o se non è possibile usare la funzionalità di conversione hardware per altri motivi, i dati dell'immagine YUV devono essere convertiti in formato RGB prima di essere inviati al renderer video.</span><span class="sxs-lookup"><span data-stu-id="6fb81-108">If the display hardware does not support on-board YUV-to-RGB conversion, or if the hardware conversion capability cannot be used for some other reason, then the YUV image data must be converted to RGB format before it is sent to the Video Renderer.</span></span>

<span data-ttu-id="6fb81-109">A causa del requisito del [renderer video](video-renderer-filter.md)per un tipo di input RGB al momento della connessione, questo filtro può essere inserito in un grafico a Monte dal renderer video durante la creazione automatica del grafo.</span><span class="sxs-lookup"><span data-stu-id="6fb81-109">Because of the [Video Renderer](video-renderer-filter.md)'s requirement for an RGB input type at connection time, this filter might be inserted into a graph upstream from the Video Renderer during automatic graph building.</span></span> <span data-ttu-id="6fb81-110">In particolare, se il generatore di grafici rileva un formato YUV nel tipo di supporto del PIN di output del filtro upstream, il generatore di grafi inserirà il decompressore AVI, che caricherà il codec MSYUV e lo configurerà inizialmente per eseguire la conversione in RGB.</span><span class="sxs-lookup"><span data-stu-id="6fb81-110">Specifically, if the Graph Builder detects a YUV format in the media type of the upstream filter's output pin, the Graph Builder will insert the AVI Decompressor, which will then load the MSYUV codec and configure it initially to perform the conversion to RGB.</span></span> <span data-ttu-id="6fb81-111">Dopo la prima transizione del grafico a uno stato di esecuzione o di sospensione, il filtro renderer video può rilevare se la scheda video è in grado di eseguire la conversione nell'hardware.</span><span class="sxs-lookup"><span data-stu-id="6fb81-111">After the graph first transitions to a run or paused state, the Video Renderer filter can detect whether the video display adapter can perform the conversion in hardware.</span></span> <span data-ttu-id="6fb81-112">In caso contrario, il decompressore AVI riceve una notifica e riconfigura MSYUV per il funzionamento in modalità pass-through, che fa in modo che il codec ignori la conversione e copi i dati dell'immagine YUV direttamente su una superficie sovrapposta DirectDraw nella memoria video.</span><span class="sxs-lookup"><span data-stu-id="6fb81-112">If it can, then the AVI Decompressor is notified and it reconfigures MSYUV to operate in "pass-through mode," which causes the codec to skip the conversion and copy the YUV image data directly onto a DirectDraw overlay surface in video memory.</span></span>

<span data-ttu-id="6fb81-113">Poiché i renderer di mixaggio video (VMR-7 e VMR-9) non utilizzano mai GDI, non richiedono un tipo RGB al momento della connessione e il convertitore dello spazio colori MSYUV non viene mai inserito prima del VMR in un grafico.</span><span class="sxs-lookup"><span data-stu-id="6fb81-113">Because the Video Mixing Renderers (VMR-7 and VMR-9) never use GDI, they do not require an RGB type at connect time, and the MSYUV Color Space Converter is never inserted before the VMR in a graph.</span></span>

<span data-ttu-id="6fb81-114">MSYUV converte i formati YUV compressi in RGB, come illustrato nell'elenco seguente:</span><span class="sxs-lookup"><span data-stu-id="6fb81-114">MSYUV converts packed YUV formats to RGB, as shown in the following list:</span></span>

-   <span data-ttu-id="6fb81-115">Formati di input: UYVY, YUY2, YVYU</span><span class="sxs-lookup"><span data-stu-id="6fb81-115">Input formats: UYVY, YUY2, YVYU</span></span>
-   <span data-ttu-id="6fb81-116">Formati di output: RGB 8, RGB 16, RGB 24, RGB 32</span><span class="sxs-lookup"><span data-stu-id="6fb81-116">Output formats: RGB 8, RGB 16, RGB 24, RGB 32</span></span>

<span data-ttu-id="6fb81-117">Il codec MSYUV Color Space Converter è un codec di Gestione compressione video (VCM).</span><span class="sxs-lookup"><span data-stu-id="6fb81-117">The MSYUV Color Space Converter Codec is a Video Compression Manager (VCM) codec.</span></span> <span data-ttu-id="6fb81-118">Viene usato in DirectShow tramite il filtro di [decompressione AVI](avi-decompressor-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="6fb81-118">It is used in DirectShow through the [AVI Decompressor](avi-decompressor-filter.md) filter.</span></span> <span data-ttu-id="6fb81-119">Per un convertitore di colori più generico, usare il [**convertitore di colori DSP**](../medfound/colorconverter.md).</span><span class="sxs-lookup"><span data-stu-id="6fb81-119">For a more general-purpose color converter, use the [**Color Converter DSP**](../medfound/colorconverter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6fb81-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6fb81-120">Requirements</span></span>



| <span data-ttu-id="6fb81-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fb81-121">Requirement</span></span> | <span data-ttu-id="6fb81-122">Valore</span><span class="sxs-lookup"><span data-stu-id="6fb81-122">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6fb81-123">DLL</span><span class="sxs-lookup"><span data-stu-id="6fb81-123">DLL</span></span><br/> | <dl> <span data-ttu-id="6fb81-124"><dt>Msyuv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fb81-124"><dt>Msyuv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fb81-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6fb81-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fb81-126">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="6fb81-126">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 
