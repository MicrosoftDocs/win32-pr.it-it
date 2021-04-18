---
description: Uso della barra di divisione MPEG-2
ms.assetid: a08e079c-41be-475a-9e88-ee46d17fe938
title: Uso della barra di divisione MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60505ef242c2ed9c1eab3031a005a2582b99608
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314385"
---
# <a name="using-the-mpeg-2-splitter"></a><span data-ttu-id="caa0a-103">Uso della barra di divisione MPEG-2</span><span class="sxs-lookup"><span data-stu-id="caa0a-103">Using the MPEG-2 Splitter</span></span>

> [!Note]  
> <span data-ttu-id="caa0a-104">A partire da Microsoft® Windows® XP, il filtro della barra di divisione MPEG-2 è deprecato.</span><span class="sxs-lookup"><span data-stu-id="caa0a-104">Starting in Microsoft® Windows® XP, the MPEG-2 Splitter filter is deprecated.</span></span> <span data-ttu-id="caa0a-105">Usare invece [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) .</span><span class="sxs-lookup"><span data-stu-id="caa0a-105">Use the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) instead.</span></span>

 

<span data-ttu-id="caa0a-106">Il filtro Splitter MPEG-2 supporta la riproduzione in modalità pull dei flussi di programma MPEG-2 che contengono almeno uno dei tipi di flusso seguenti.</span><span class="sxs-lookup"><span data-stu-id="caa0a-106">The MPEG-2 Splitter filter supports pull-mode playback of MPEG-2 program streams that contain at least one of the following stream types.</span></span>

-   <span data-ttu-id="caa0a-107">Video MPEG-2</span><span class="sxs-lookup"><span data-stu-id="caa0a-107">MPEG-2 video</span></span>
-   <span data-ttu-id="caa0a-108">Audio MPEG-2</span><span class="sxs-lookup"><span data-stu-id="caa0a-108">MPEG-2 audio</span></span>
-   <span data-ttu-id="caa0a-109">Audio Dolby AC-3 codificato come definito per DVD-Video</span><span class="sxs-lookup"><span data-stu-id="caa0a-109">Dolby AC-3 audio encoded as defined for DVD-Video</span></span>
-   <span data-ttu-id="caa0a-110">LPCM (Linear Pulse Code modulata) audio codificato come definito per DVD-Video</span><span class="sxs-lookup"><span data-stu-id="caa0a-110">LPCM (Linear Pulse Code Modulated) audio encoded as defined for DVD-Video</span></span>

<span data-ttu-id="caa0a-111">Per un elenco dei tipi di supporto supportati dal separatore MPEG-2, vedere tipi di supporto per la [barra di divisione MPEG-2](mpeg-2-splitter-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="caa0a-111">For a list of media types that the MPEG-2 Splitter supports, see [MPEG-2 Splitter Media Types](mpeg-2-splitter-media-types.md).</span></span>

<span data-ttu-id="caa0a-112">Il separatore MPEG-2 non analizza i flussi di trasporto.</span><span class="sxs-lookup"><span data-stu-id="caa0a-112">The MPEG-2 Splitter does not parse transport streams.</span></span> <span data-ttu-id="caa0a-113">Usare il filtro di demultiplexing MPEG-2 per i flussi di trasporto (solo modalità push).</span><span class="sxs-lookup"><span data-stu-id="caa0a-113">Use the MPEG-2 Demultiplexer filter for transport streams (push mode only).</span></span>

<span data-ttu-id="caa0a-114">**Timestamp**</span><span class="sxs-lookup"><span data-stu-id="caa0a-114">**Time Stamps**</span></span>

<span data-ttu-id="caa0a-115">Quando si esegue la riproduzione dei flussi di programma MPEG-2, il filtro con separatore MPEG-2 considera il primo riferimento all'orologio di sistema rilevato come origine dell'ora di qualsiasi flusso.</span><span class="sxs-lookup"><span data-stu-id="caa0a-115">When playing back MPEG-2 program streams, the MPEG-2 Splitter filter treats the first system clock reference it encounters as the time origin of any stream.</span></span> <span data-ttu-id="caa0a-116">Questo comportamento è diverso dal [separatore di flusso MPEG-1](mpeg-1-stream-splitter-filter.md), che usa i timestamp di presentazione.</span><span class="sxs-lookup"><span data-stu-id="caa0a-116">This differs from the [MPEG-1 Stream Splitter](mpeg-1-stream-splitter-filter.md), which uses presentation time stamps.</span></span> <span data-ttu-id="caa0a-117">Il metodo [**IAMParse:: GetParseTime**](/previous-versions/windows/desktop/api/Amparse/nf-amparse-iamparse-getparsetime) restituisce il tempo di clock del sistema di flusso (probabilmente stimato) per i dati elaborati.</span><span class="sxs-lookup"><span data-stu-id="caa0a-117">The [**IAMParse::GetParseTime**](/previous-versions/windows/desktop/api/Amparse/nf-amparse-iamparse-getparsetime) method returns the (possibly estimated) stream system clock time for the data it has processed.</span></span>

<span data-ttu-id="caa0a-118">Se il filtro della barra di divisione MPEG-2 rileva un campione di input con il set di proprietà di discontinuità (la proprietà discontinuità può essere impostata tramite [**IMediaSample:: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) o [**IMediaSample2:: seproperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties)) ignora i dati fino a quando non trova il primo pacchetto nei dati e ne modifica i timestamp in modo che il riferimento all'orologio di sistema (SCR) per il pacchetto venga considerato identico all'ora di SCR prima della discontinuità.</span><span class="sxs-lookup"><span data-stu-id="caa0a-118">If the MPEG-2 splitter filter encounters an input sample with the discontinuity property set (the discontinuity property can be set by using [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) or [**IMediaSample2::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties)), it skips data until it finds the first pack in the data and adjusts its time stamps so that the system clock reference (SCR) for that pack is considered identical to the SCR time before the discontinuity.</span></span> <span data-ttu-id="caa0a-119">Se il clock SCR viene visualizzato per tornare indietro o per andare avanti di più di un secondo, quindi, in linea con la specifica MPEG-2 Program Stream, viene trattato anche come una discontinuità di clock e la discrepanza di clock apparente viene sottratta dai timestamp passati ai filtri downstream.</span><span class="sxs-lookup"><span data-stu-id="caa0a-119">If the SCR clock appears either to jump backward or to jump forward by more than a second, then (in line with the MPEG-2 program stream specification), this is also treated as a clock discontinuity and the apparent clock discrepancy is subtracted from the time stamps passed to downstream filters.</span></span>

<span data-ttu-id="caa0a-120">**Selezione flusso**</span><span class="sxs-lookup"><span data-stu-id="caa0a-120">**Stream Selection**</span></span>

<span data-ttu-id="caa0a-121">Quando si esegue la riproduzione del flusso di programma MPEG-2, vengono scelti il primo flusso video e il primo flusso audio trovato attraversando il flusso del programma.</span><span class="sxs-lookup"><span data-stu-id="caa0a-121">When playing back the MPEG-2 program stream, the first video stream and first audio stream found traversing the program stream are chosen.</span></span> <span data-ttu-id="caa0a-122">Sono supportati fino a un pin audio e un pin di output video.</span><span class="sxs-lookup"><span data-stu-id="caa0a-122">Up to one audio and one video output pin are supported.</span></span> <span data-ttu-id="caa0a-123">Tramite l'interfaccia [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect) , è possibile selezionare flussi diversi dello stesso tipo fino al numero specificato dal limite audio nell'intestazione di sistema.</span><span class="sxs-lookup"><span data-stu-id="caa0a-123">Through the [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect) interface, different streams of the same type can be selected up to the number specified by the audio limit in the system header.</span></span> <span data-ttu-id="caa0a-124">Per l'audio MPEG-2, attualmente si presuppone che i flussi formino un intervallo contiguo a partire dal flusso 0xC0.</span><span class="sxs-lookup"><span data-stu-id="caa0a-124">For MPEG-2 audio, it is currently assumed the streams form a contiguous range starting at stream 0xC0.</span></span>

<span data-ttu-id="caa0a-125">**Interfacce supportate**</span><span class="sxs-lookup"><span data-stu-id="caa0a-125">**Supported Interfaces**</span></span>

<span data-ttu-id="caa0a-126">Il filtro separatore MPEG-2 supporta le interfacce seguenti.</span><span class="sxs-lookup"><span data-stu-id="caa0a-126">The MPEG-2 splitter filter supports the following interfaces.</span></span>

-   <span data-ttu-id="caa0a-127">[**IAMParse**](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse).</span><span class="sxs-lookup"><span data-stu-id="caa0a-127">[**IAMParse**](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse).</span></span> <span data-ttu-id="caa0a-128">Solo flusso di programma MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="caa0a-128">MPEG-2 program stream only.</span></span>
-   <span data-ttu-id="caa0a-129">[**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect).</span><span class="sxs-lookup"><span data-stu-id="caa0a-129">[**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect).</span></span> <span data-ttu-id="caa0a-130">Solo flusso di programma MPEG-2, solo flussi audio.</span><span class="sxs-lookup"><span data-stu-id="caa0a-130">MPEG-2 program stream only, audio streams only.</span></span>
-   <span data-ttu-id="caa0a-131">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking).</span><span class="sxs-lookup"><span data-stu-id="caa0a-131">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking).</span></span> <span data-ttu-id="caa0a-132">Include la ricerca in modalità byte.</span><span class="sxs-lookup"><span data-stu-id="caa0a-132">Includes byte mode seeking.</span></span>

## <a name="related-topics"></a><span data-ttu-id="caa0a-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="caa0a-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="caa0a-134">Supporto MPEG-2 in DirectShow</span><span class="sxs-lookup"><span data-stu-id="caa0a-134">MPEG-2 Support in DirectShow</span></span>](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 



