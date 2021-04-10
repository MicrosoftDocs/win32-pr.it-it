---
description: Modalità Run-Time MPEG-2 demux
ms.assetid: b0d0c725-9220-43a5-af1c-d3c5c72e1ef3
title: Modalità Run-Time MPEG-2 demux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6e4e7a1dea0bfeccd60d8680a31b99cc10271ee
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125217"
---
# <a name="mpeg-2-demux-run-time-modes"></a><span data-ttu-id="80d1a-103">Modalità Run-Time MPEG-2 demux</span><span class="sxs-lookup"><span data-stu-id="80d1a-103">MPEG-2 Demux Run-Time Modes</span></span>

<span data-ttu-id="80d1a-104">Il [Demultiplexer MPEG-2](mpeg-2-demultiplexer.md) ("demux") può funzionare in modalità push o pull.</span><span class="sxs-lookup"><span data-stu-id="80d1a-104">The [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) ("demux") can operate in push mode or pull mode.</span></span> <span data-ttu-id="80d1a-105">In modalità push, i dati provengono da un'origine live, ad esempio una trasmissione di rete.</span><span class="sxs-lookup"><span data-stu-id="80d1a-105">In push mode, the data comes from a live source, such as a network broadcast.</span></span> <span data-ttu-id="80d1a-106">In modalità pull i dati provengono da un file locale.</span><span class="sxs-lookup"><span data-stu-id="80d1a-106">In pull mode, the data comes from a local file.</span></span>

-   <span data-ttu-id="80d1a-107">La modalità pull è disponibile in Windows XP e versioni successive per solo i flussi di programma.</span><span class="sxs-lookup"><span data-stu-id="80d1a-107">Pull mode is available in Windows XP and later, for program streams only.</span></span> <span data-ttu-id="80d1a-108">Nelle piattaforme di livello inferiore, usare il filtro con [separatore MPEG-2](mpeg-2-splitter.md) .</span><span class="sxs-lookup"><span data-stu-id="80d1a-108">On down-level platforms, use the [MPEG-2 Splitter](mpeg-2-splitter.md) filter.</span></span>
-   <span data-ttu-id="80d1a-109">La modalità push è disponibile in tutte le piattaforme, sia per i flussi di programma che per i flussi di trasporto.</span><span class="sxs-lookup"><span data-stu-id="80d1a-109">Push mode is available on all platforms, for both program streams and transport streams.</span></span>

<span data-ttu-id="80d1a-110">Il demux supporta pertanto tre modalità possibili: i flussi di programma in modalità pull, i flussi di programma in modalità push e i flussi di trasporto in modalità push.</span><span class="sxs-lookup"><span data-stu-id="80d1a-110">The demux therefore supports three possible modes: Program streams in pull mode, program streams in push mode, and transport streams in push mode.</span></span> <span data-ttu-id="80d1a-111">Il demux determina la modalità da usare in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="80d1a-111">The demux determines which mode to use at run time.</span></span> <span data-ttu-id="80d1a-112">La modalità viene determinata quando il pin di input si connette o quando viene configurato il primo pin di output, a seconda di quale evento si verifica per primo:</span><span class="sxs-lookup"><span data-stu-id="80d1a-112">The mode is determined when the input pin connects, or when the first output pin is configured, whichever happens first:</span></span>

-   <span data-ttu-id="80d1a-113">Quando il pin di input si connette: in Windows XP e versioni successive, demux esegue una query sul filtro upstream per l'interfaccia [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) . Se il filtro upstream espone tale interfaccia, demux si configura per i flussi di programma in modalità pull.</span><span class="sxs-lookup"><span data-stu-id="80d1a-113">When the input pin connects: On Windows XP and later, the demux queries the upstream filter for the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface; if the upstream filter exposes that interface, the demux configures itself for program streams in pull mode.</span></span> <span data-ttu-id="80d1a-114">In caso contrario, demux usa la modalità push e il tipo di supporto determina il tipo di flusso (flusso del programma o flusso di trasporto).</span><span class="sxs-lookup"><span data-stu-id="80d1a-114">Otherwise, the demux uses push mode, and the media type determines the stream type (program stream or transport stream).</span></span> <span data-ttu-id="80d1a-115">Per un elenco di tipi di input, vedere [**tipi di supporti Demultiplexer MPEG-2**](mpeg-2-demultiplexer-media-types.md) .</span><span class="sxs-lookup"><span data-stu-id="80d1a-115">See [**MPEG-2 Demultiplexer Media Types**](mpeg-2-demultiplexer-media-types.md) for a list of input types.</span></span>
-   <span data-ttu-id="80d1a-116">Quando viene configurato il primo pin di output: se si crea un pin di output e lo si esegue una query per [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap), demux si configura per i flussi di trasporto in modalità push.</span><span class="sxs-lookup"><span data-stu-id="80d1a-116">When the first output pin is configured: If you create an output pin and query it for [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap), the demux configures itself for transport streams in push mode.</span></span> <span data-ttu-id="80d1a-117">Se si esegue una query sul pin per [**IMPEG2StreamIdMap**](/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap), demux si configura per i flussi di programma, anche in modalità push.</span><span class="sxs-lookup"><span data-stu-id="80d1a-117">If you query the pin for [**IMPEG2StreamIdMap**](/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap), the demux configures itself for program streams, also in push mode.</span></span> <span data-ttu-id="80d1a-118">Tutte le query successive per l'altra interfaccia hanno esito negativo, perché demux non può funzionare contemporaneamente in due modalità.</span><span class="sxs-lookup"><span data-stu-id="80d1a-118">Any subsequent queries for the other interface fail, because the demux cannot operate in two modes at once.</span></span>

<span data-ttu-id="80d1a-119">Una volta che il demux è stato configurato per una particolare modalità, rimane in tale modalità.</span><span class="sxs-lookup"><span data-stu-id="80d1a-119">Once the demux has configured itself for a particular mode, it remains in that mode.</span></span> <span data-ttu-id="80d1a-120">Per utilizzare una modalità diversa, è necessario creare una nuova istanza di demux.</span><span class="sxs-lookup"><span data-stu-id="80d1a-120">To use a different mode, you must create a new instance of the demux.</span></span>

## <a name="related-topics"></a><span data-ttu-id="80d1a-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="80d1a-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80d1a-122">Uso del Demultiplexer MPEG-2</span><span class="sxs-lookup"><span data-stu-id="80d1a-122">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



