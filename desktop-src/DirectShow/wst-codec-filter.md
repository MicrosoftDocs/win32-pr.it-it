---
description: Filtro codec WST
ms.assetid: 0a06acbf-b842-4ab6-bcf9-d2d006301d83
title: Filtro codec WST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338db987986a5f4706c144907d122eec3a0615a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349796"
---
# <a name="wst-codec-filter"></a><span data-ttu-id="95789-103">Filtro codec WST</span><span class="sxs-lookup"><span data-stu-id="95789-103">WST Codec Filter</span></span>

> [!IMPORTANT]
> <span data-ttu-id="95789-104">Questo componente è stato rimosso da Windows Vista e dai sistemi operativi successivi.</span><span class="sxs-lookup"><span data-stu-id="95789-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="95789-105">È disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="95789-105">It is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

 

<span data-ttu-id="95789-106">A partire da Windows Vista, questo filtro viene sostituito dal filtro VBICodec, documentato nella documentazione relativa alle tecnologie Microsoft TV.</span><span class="sxs-lookup"><span data-stu-id="95789-106">Starting in Windows Vista, this filter is replaced by the VBICodec filter, which is documented in the Microsoft TV Technologies documentation.</span></span>

<span data-ttu-id="95789-107">Il televideo (WST) è lo standard europeo per la trasmissione dei dati tramite VBI nei segnali TV analoghi di PAL.</span><span class="sxs-lookup"><span data-stu-id="95789-107">World Standard Teletext (WST) is the European standard for data transmission using VBI on PAL analog television signals.</span></span> <span data-ttu-id="95789-108">La didascalia e i servizi dati vengono forniti utilizzando questo standard.</span><span class="sxs-lookup"><span data-stu-id="95789-108">Both captioning and data services are provided using this standard.</span></span> <span data-ttu-id="95789-109">Il codec WST è un filtro in modalità kernel che riceve esempi di VBI non elaborati e, facoltativamente, gli esempi di televideo decodificati dal filtro di acquisizione tramite il filtro del [convertitore Tee/Sink-to-sink](tee-sink-to-sink-converter.md) .</span><span class="sxs-lookup"><span data-stu-id="95789-109">The WST Codec is a kernel-mode filter that receives raw VBI samples and, optionally, decoded Teletext samples from the Capture Filter via the [Tee/Sink-to-Sink Converter](tee-sink-to-sink-converter.md) filter.</span></span> <span data-ttu-id="95789-110">Questo codec decodifica e/o duplica i dati di televideo decodificati e con errori in diretta per il filtro del [decodificatore WST](wst-decoder-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="95789-110">This codec decodes and/or duplicates the decoded and forward-error-corrected Teletext data for the [WST Decoder](wst-decoder-filter.md) filter.</span></span> <span data-ttu-id="95789-111">Il codec WST corrisponde al filtro del decodificatore CC per le trasmissioni NTSC.</span><span class="sxs-lookup"><span data-stu-id="95789-111">The WST Codec corresponds to the CC Decoder filter for NTSC transmissions.</span></span> <span data-ttu-id="95789-112">Il decodificatore WST corrisponde al [decodificatore della riga 21](line-21-decoder-filter.md) per NTSC; Questi filtri creano le bitmap inviate al mixer overlay o al renderer di mixaggio video.</span><span class="sxs-lookup"><span data-stu-id="95789-112">The WST Decoder corresponds to the [Line 21 Decoder](line-21-decoder-filter.md) for NTSC; these filters create the bitmaps that are sent to the Overlay Mixer or the Video Mixing Renderer.</span></span>

<span data-ttu-id="95789-113">Questo filtro ha due pin di input, VBI e HWCC.</span><span class="sxs-lookup"><span data-stu-id="95789-113">This filter has two input pins, VBI and HWCC.</span></span> <span data-ttu-id="95789-114">Il pin VBI viene usato per i dati VBI non elaborati e il pin HWCC viene usato quando la decodifica VBI viene eseguita nell'hardware dal filtro di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="95789-114">The VBI pin is used for raw VBI data, and the HWCC pin is used when the VBI decoding is performed in hardware by the capture filter.</span></span> <span data-ttu-id="95789-115">Quando i dati vengono ricevuti sul pin HWCC, il codec WST funziona in modalità "pass-through" e invia i dati direttamente al decodificatore WST senza elaborarli in alcun modo.</span><span class="sxs-lookup"><span data-stu-id="95789-115">When the data is received on the HWCC pin, the WST Codec operates in "pass-through" mode, and sends the data directly to the WST Decoder without processing it in any way.</span></span> <span data-ttu-id="95789-116">Se il filtro di acquisizione espone un pin HWCC, deve essere connesso direttamente al pin corrispondente nel codec WST.</span><span class="sxs-lookup"><span data-stu-id="95789-116">If the capture filter exposes an HWCC pin, it must be connected directly to the corresponding pin on the WST Codec.</span></span>

<span data-ttu-id="95789-117">Il filtro codec WST viene visualizzato nella categoria di filtro "WDM Streaming VBI codecs" (**am \_ KSCATEGORY \_ VBICODEC**).</span><span class="sxs-lookup"><span data-stu-id="95789-117">The WST Codec filter appears in the "WDM Streaming VBI Codecs" filter category (**AM\_KSCATEGORY\_VBICODEC**).</span></span>

<span data-ttu-id="95789-118">Poiché si tratta di un filtro in modalità kernel, le applicazioni non possono crearlo direttamente tramite **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="95789-118">Because this is a kernel-mode filter, applications cannot create it directly using **CoCreateInstance**.</span></span> <span data-ttu-id="95789-119">Usare invece l' [enumeratore di dispositivo di sistema](system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="95789-119">Instead, use the [System Device Enumerator](system-device-enumerator.md).</span></span> <span data-ttu-id="95789-120">Per ulteriori informazioni, vedere [creazione di filtri Kernel-Mode](creating-kernel-mode-filters.md).</span><span class="sxs-lookup"><span data-stu-id="95789-120">For more information, see [Creating Kernel-Mode Filters](creating-kernel-mode-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="95789-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="95789-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95789-122">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="95789-122">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="95789-123">Visualizzazione del televideo standard internazionale</span><span class="sxs-lookup"><span data-stu-id="95789-123">Viewing World Standard Teletext</span></span>](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



