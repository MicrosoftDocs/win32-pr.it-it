---
description: Nuovi segmenti
ms.assetid: 6c470b38-481f-4e52-93b8-eb6b343dcefc
title: Nuovi segmenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5438cb3b457ed8ea0f77bd2ac1dcc5d6d2c72698
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303736"
---
# <a name="new-segments"></a><span data-ttu-id="24f71-103">Nuovi segmenti</span><span class="sxs-lookup"><span data-stu-id="24f71-103">New Segments</span></span>

<span data-ttu-id="24f71-104">Un *segmento* è un gruppo di esempi di supporti che condividono un'ora di inizio, un'ora di arresto e una velocità di riproduzione comuni.</span><span class="sxs-lookup"><span data-stu-id="24f71-104">A *segment* is a group of media samples that share a common start time, stop time, and playback rate.</span></span> <span data-ttu-id="24f71-105">Il metodo [**Ipin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) segnala l'inizio di un nuovo segmento.</span><span class="sxs-lookup"><span data-stu-id="24f71-105">The [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method signals the start of a new segment.</span></span> <span data-ttu-id="24f71-106">Fornisce un modo per un filtro di origine per informare i filtri downstream che sono state modificate le informazioni relative a ora e frequenza.</span><span class="sxs-lookup"><span data-stu-id="24f71-106">It provides a way for a source filter to inform downstream filters that the time and rate information has changed.</span></span> <span data-ttu-id="24f71-107">Se, ad esempio, il filtro di origine cerca un nuovo punto nel flusso, viene chiamato **NewSegment** con la nuova ora di inizio.</span><span class="sxs-lookup"><span data-stu-id="24f71-107">For example, if the source filter seeks to a new point in the stream, it calls **NewSegment** with the new start time.</span></span>

<span data-ttu-id="24f71-108">Alcuni filtri downstream utilizzano le informazioni sul segmento quando elaborano gli esempi.</span><span class="sxs-lookup"><span data-stu-id="24f71-108">Some downstream filters use the segment information when they process samples.</span></span> <span data-ttu-id="24f71-109">Ad esempio, in un formato che usa la compressione interframe, se l'ora di arresto si trova su un frame differenziale, il filtro di origine potrebbe dover inviare campioni aggiuntivi dopo l'ora di arresto.</span><span class="sxs-lookup"><span data-stu-id="24f71-109">For example, in a format that uses interframe compression, if the stop time falls on a delta frame, the source filter may need to send additional samples after the stop time.</span></span> <span data-ttu-id="24f71-110">Ciò consente al decodificatore di decodificare il frame Delta finale.</span><span class="sxs-lookup"><span data-stu-id="24f71-110">This enables the decoder to decode the final delta frame.</span></span> <span data-ttu-id="24f71-111">Per determinare il fotogramma finale corretto, il decodificatore fa riferimento all'ora di arresto del segmento.</span><span class="sxs-lookup"><span data-stu-id="24f71-111">To determine the correct final frame, the decoder refers to the segment stop time.</span></span> <span data-ttu-id="24f71-112">Come altro esempio, i renderer audio usano la frequenza dei segmenti insieme alla frequenza di campionamento audio per generare l'output audio corretto.</span><span class="sxs-lookup"><span data-stu-id="24f71-112">As another example, audio renderers use the segment rate along with the audio sampling rate to generate the correct audio output.</span></span>

<span data-ttu-id="24f71-113">Nel modello push, il filtro di origine avvia la chiamata **NewSegment** .</span><span class="sxs-lookup"><span data-stu-id="24f71-113">In the push model, the source filter initiates the **NewSegment** call.</span></span> <span data-ttu-id="24f71-114">Nel modello pull questa operazione viene eseguita dal filtro del parser.</span><span class="sxs-lookup"><span data-stu-id="24f71-114">In the pull model, this is done by the parser filter.</span></span> <span data-ttu-id="24f71-115">In entrambi i casi, il filtro chiama **NewSegment** sul pin di input downstream, che propaga la chiamata al filtro successivo, finché la chiamata non raggiunge il renderer.</span><span class="sxs-lookup"><span data-stu-id="24f71-115">In either case, the filter calls **NewSegment** on the downstream input pin, which propagates the call to the next filter, until the call reaches the renderer.</span></span> <span data-ttu-id="24f71-116">I filtri devono serializzare le chiamate **NewSegment** con altre chiamate di streaming, ad esempio [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive).</span><span class="sxs-lookup"><span data-stu-id="24f71-116">Filters must serialize **NewSegment** calls with other streaming calls, such as [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive).</span></span>

<span data-ttu-id="24f71-117">Il flusso temporale viene reimpostato su zero dopo ogni nuovo segmento.</span><span class="sxs-lookup"><span data-stu-id="24f71-117">Stream time resets to zero after each new segment.</span></span> <span data-ttu-id="24f71-118">Timestamp per gli esempi recapitati dopo l'inizio del segmento da zero.</span><span class="sxs-lookup"><span data-stu-id="24f71-118">Time stamps on samples delivered after the segment start from zero.</span></span>

 

 



