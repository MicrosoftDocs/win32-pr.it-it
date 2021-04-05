---
description: Gli oggetti WMContainer forniscono il controllo di basso livello sull'analisi e la scrittura di un file di formato Advanced Systems (ASF).
ms.assetid: 258ea139-581f-4b94-9655-43ecf1e77f10
title: Componenti ASF WMContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d7d1c1b76683cfe01dc0970ab1c077580215d2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967637"
---
# <a name="wmcontainer-asf-components"></a><span data-ttu-id="bc656-103">Componenti ASF WMContainer</span><span class="sxs-lookup"><span data-stu-id="bc656-103">WMContainer ASF Components</span></span>

<span data-ttu-id="bc656-104">Gli oggetti WMContainer forniscono il controllo di basso livello sull'analisi e la scrittura di un file di formato Advanced Systems (ASF).</span><span class="sxs-lookup"><span data-stu-id="bc656-104">The WMContainer objects provide low-level control over parsing and writing an Advanced Systems Format (ASF) file.</span></span>

<span data-ttu-id="bc656-105">I [componenti ASF del livello pipeline](pipeline-layer-asf-components.md) utilizzano internamente gli oggetti WMContainer.</span><span class="sxs-lookup"><span data-stu-id="bc656-105">The [Pipeline Layer ASF Components](pipeline-layer-asf-components.md) use the WMContainer objects internally.</span></span> <span data-ttu-id="bc656-106">La maggior parte delle applicazioni deve usare i componenti della pipeline, anziché usare gli oggetti WMContainer.</span><span class="sxs-lookup"><span data-stu-id="bc656-106">Most applications should use the pipeline components, rather than using WMContainer objects.</span></span> <span data-ttu-id="bc656-107">Utilizzare WMContainer solo se è necessario un controllo di basso livello sull'analisi e la scrittura di un file ASF.</span><span class="sxs-lookup"><span data-stu-id="bc656-107">Use WMContainer only if you require low-level control over parsing and writing an ASF file.</span></span>

<span data-ttu-id="bc656-108">Il livello WMContainer include gli oggetti seguenti:</span><span class="sxs-lookup"><span data-stu-id="bc656-108">The WMContainer layer includes the following objects:</span></span>

-   [<span data-ttu-id="bc656-109">Profilo ASF</span><span class="sxs-lookup"><span data-stu-id="bc656-109">ASF Profile</span></span>](asf-profile.md)
-   [<span data-ttu-id="bc656-110">Oggetto ContentInfo ASF</span><span class="sxs-lookup"><span data-stu-id="bc656-110">ASF ContentInfo Object</span></span>](asf-contentinfo-object.md)
-   [<span data-ttu-id="bc656-111">Barra di divisione ASF</span><span class="sxs-lookup"><span data-stu-id="bc656-111">ASF Splitter</span></span>](asf-splitter.md)
-   [<span data-ttu-id="bc656-112">Multiplexer ASF</span><span class="sxs-lookup"><span data-stu-id="bc656-112">ASF Multiplexer</span></span>](asf-multiplexer.md)
-   [<span data-ttu-id="bc656-113">Indicizzatore ASF</span><span class="sxs-lookup"><span data-stu-id="bc656-113">ASF Indexer</span></span>](asf-index-object.md)

<span data-ttu-id="bc656-114">Negli argomenti seguenti sono contenute istruzioni dettagliate sull'utilizzo di WMContainer per la lettura o la scrittura di file ASF.</span><span class="sxs-lookup"><span data-stu-id="bc656-114">The following topics contain step-by-step instructions about using WMContainer to read or write ASF files.</span></span>

-   [<span data-ttu-id="bc656-115">Esercitazione: lettura di un file ASF usando oggetti WMContainer</span><span class="sxs-lookup"><span data-stu-id="bc656-115">Tutorial: Reading an ASF File by Using WMContainer Objects</span></span>](tutorial--reading-an-asf-file.md)
-   [<span data-ttu-id="bc656-116">Esercitazione: copia di flussi ASF usando oggetti WMContainer</span><span class="sxs-lookup"><span data-stu-id="bc656-116">Tutorial: Copying ASF Streams by Using WMContainer Objects</span></span>](tutorial--copying-asf-streams-from-one-file-to-another.md)
-   [<span data-ttu-id="bc656-117">Esercitazione: scrittura di un file WMA usando oggetti WMContainer</span><span class="sxs-lookup"><span data-stu-id="bc656-117">Tutorial: Writing a WMA File by Using WMContainer Objects</span></span>](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)

## <a name="about-wm-container"></a><span data-ttu-id="bc656-118">Informazioni sul contenitore WM</span><span class="sxs-lookup"><span data-stu-id="bc656-118">About WM Container</span></span>

<span data-ttu-id="bc656-119">Gli oggetti WMContainer interagiscono direttamente con gli oggetti file ASF.</span><span class="sxs-lookup"><span data-stu-id="bc656-119">The WMContainer objects interact directly with ASF file objects.</span></span> <span data-ttu-id="bc656-120">Il diagramma seguente mostra la struttura dei file ASF e gli oggetti WMContainer corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="bc656-120">The following diagram shows the ASF file structure and the corresponding WMContainer objects.</span></span>

![diagramma che illustra la struttura dei file ASF e gli oggetti di Media Foundation corrispondenti](images/asf-components01.png)

<span data-ttu-id="bc656-122">Ad eccezione della barra di divisione e del multiplexer, ognuno di questi oggetti supporta sia l'analisi (lettura) che la scrittura dei file ASF.</span><span class="sxs-lookup"><span data-stu-id="bc656-122">Except for the splitter and multiplexer, each of these objects supports both parsing (reading) and writing ASF files.</span></span> <span data-ttu-id="bc656-123">La barra di divisione viene utilizzata solo per la lettura dei file ASF.</span><span class="sxs-lookup"><span data-stu-id="bc656-123">The splitter is used only for reading ASF files.</span></span> <span data-ttu-id="bc656-124">Multiplexer viene usato solo per la creazione di nuovi file ASF.</span><span class="sxs-lookup"><span data-stu-id="bc656-124">The multiplexer is used only for authoring new ASF files.</span></span>

<span data-ttu-id="bc656-125">Tutte le operazioni eseguite dagli oggetti WMContainer sono sincrone, ovvero bloccano il thread chiamante.</span><span class="sxs-lookup"><span data-stu-id="bc656-125">All operations performed by WMContainer objects are synchronous, meaning they block the calling thread.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc656-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bc656-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc656-127">Supporto ASF in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bc656-127">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



