---
description: Comportamento demux Clock
ms.assetid: c8a067f7-4e4c-4f25-b26c-f6bb048060b0
title: Comportamento demux Clock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9065e6da51acb5387ca06bf921d5cdc91c567843
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104048999"
---
# <a name="demux-clock-behavior"></a><span data-ttu-id="a81d8-103">Comportamento demux Clock</span><span class="sxs-lookup"><span data-stu-id="a81d8-103">Demux Clock Behavior</span></span>

<span data-ttu-id="a81d8-104">In modalità push, il Demultiplexer MPEG-2 (demux) espone l'interfaccia [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) .</span><span class="sxs-lookup"><span data-stu-id="a81d8-104">In push mode, the MPEG-2 Demultiplexer (demux) exposes the [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface.</span></span> <span data-ttu-id="a81d8-105">Funge da origine live, quindi verrà scelto come clock di riferimento del grafico per impostazione predefinita. Per ulteriori informazioni, vedere [Live Sources](live-sources.md) .</span><span class="sxs-lookup"><span data-stu-id="a81d8-105">It acts as a live source, so it will be chosen as the graph reference clock by default; see [Live Sources](live-sources.md) for more information.</span></span>

-   <span data-ttu-id="a81d8-106">Per i flussi di trasporto, il demux sincronizza l'orologio con il flusso di PCR che corrisponde al flusso audio o video più recentemente mappato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a81d8-106">For transport streams, the demux synchronizes its clock to the PCR stream that corresponds to the audio or video stream most recently mapped by the application.</span></span> <span data-ttu-id="a81d8-107">Internamente, demux tiene traccia delle tabelle PAT e PMT.</span><span class="sxs-lookup"><span data-stu-id="a81d8-107">Internally, the demux tracks the PAT and PMT tables.</span></span> <span data-ttu-id="a81d8-108">Quando l'applicazione esegue il mapping di un PID del flusso elementare a un pin di output, demux Cerca il flusso di PCR per tale PID e usa tale flusso di PCR.</span><span class="sxs-lookup"><span data-stu-id="a81d8-108">When the application maps an elementary stream PID to an output pin, the demux looks up the PCR stream for that PID and uses that PCR stream.</span></span> <span data-ttu-id="a81d8-109">Attualmente non è possibile specificare direttamente il PID PCR per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a81d8-109">(Currently, there is not way for the application to specify the PCR PID directly.)</span></span>
-   <span data-ttu-id="a81d8-110">Per i flussi di programma, demux sincronizza l'orologio con il flusso SCR.</span><span class="sxs-lookup"><span data-stu-id="a81d8-110">For program streams, the demux synchronizes its clock to the SCR stream.</span></span>

<span data-ttu-id="a81d8-111">La sincronizzazione dell'orologio del filtro per il flusso PCR o SCR impedisce l'overflow o l'underflow dei dati, cosa che può verificarsi se il clock del grafico varia dal clock del flusso.</span><span class="sxs-lookup"><span data-stu-id="a81d8-111">Synchronizing the filter clock to the PCR or SCR stream prevents data overflow or underflow, which could result if the graph clock varied from the stream clock.</span></span> <span data-ttu-id="a81d8-112">Il demux converte anche i valori dei PTS di PES in orari di riferimento DirectShow e usa questi valori per contrassegnare il timestamp degli esempi di supporti.</span><span class="sxs-lookup"><span data-stu-id="a81d8-112">The demux also translates PES PTS values into DirectShow reference times, and uses these values to time stamp the media samples.</span></span> <span data-ttu-id="a81d8-113">Gli indicatori di data e ora si applicano al limite del frame successivo. non vi è alcuna garanzia che il limite del frame verrà allineato all'inizio dell'esempio di supporto.</span><span class="sxs-lookup"><span data-stu-id="a81d8-113">The time stamps apply to the next frame boundary; there is no guarantee that the frame boundary will align with the start of the media sample.</span></span>

<span data-ttu-id="a81d8-114">Il demux garantisce che i timestamp aumentino in modo progressivo.</span><span class="sxs-lookup"><span data-stu-id="a81d8-114">The demux guarantees that the time stamps increase monotonically.</span></span> <span data-ttu-id="a81d8-115">Ciò significa, ad esempio, che se un flusso di trasporto include un segmento, ad esempio un annuncio commerciale creato con un clock diverso da quello del programma principale, il demux modificherà i timestamp di presentazione per nascondere la discontinuità temporale dai filtri downstream.</span><span class="sxs-lookup"><span data-stu-id="a81d8-115">This means, for example, that if a transport stream includes a segment such as a commercial that was created with a different clock than the main program, the demux will adjust the presentation time stamps to hide the time discontinuity from downstream filters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a81d8-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a81d8-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a81d8-117">Uso del Demultiplexer MPEG-2</span><span class="sxs-lookup"><span data-stu-id="a81d8-117">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



