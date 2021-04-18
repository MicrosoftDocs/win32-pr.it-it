---
description: Informazioni sui motori di rendering
ms.assetid: 80299b1a-09bf-4660-95d3-41a2b0074745
title: Informazioni sui motori di rendering
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70fe3a9956bee0d167de9e6618187bfd1f2a6e39
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522234"
---
# <a name="about-the-render-engines"></a><span data-ttu-id="37e40-103">Informazioni sui motori di rendering</span><span class="sxs-lookup"><span data-stu-id="37e40-103">About the Render Engines</span></span>

<span data-ttu-id="37e40-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="37e40-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="37e40-105">Questo articolo descrive come [DirectShow editing Services](directshow-editing-services.md) (des) esegue il rendering di un progetto di modifica video.</span><span class="sxs-lookup"><span data-stu-id="37e40-105">This article describes how [DirectShow Editing Services](directshow-editing-services.md) (DES) renders a video editing project.</span></span>

<span data-ttu-id="37e40-106">In DES un progetto viene rappresentato come sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="37e40-106">In DES, a project is represented as a timeline.</span></span> <span data-ttu-id="37e40-107">La sequenza temporale è utile perché semplifica le attività più comuni nella modifica dei video, ad esempio la ridisposizione delle clip di origine e l'aggiunta di effetti video.</span><span class="sxs-lookup"><span data-stu-id="37e40-107">The timeline is useful because it simplifies the most common tasks in video editing, such as rearranging source clips and adding video effects.</span></span> <span data-ttu-id="37e40-108">L'architettura del flusso DirectShow, d'altra parte, richiede un grafico di filtro.</span><span class="sxs-lookup"><span data-stu-id="37e40-108">The DirectShow stream architecture, on the other hand, requires a filter graph.</span></span> <span data-ttu-id="37e40-109">Quindi, per eseguire il rendering del progetto, è necessario tradurre una sequenza temporale in un grafico a filtro.</span><span class="sxs-lookup"><span data-stu-id="37e40-109">Thus, to render your project, you must translate a timeline into a filter graph.</span></span> <span data-ttu-id="37e40-110">Il componente che esegue questa operazione è denominato *motore di rendering*.</span><span class="sxs-lookup"><span data-stu-id="37e40-110">The component that does this is called a *render engine*.</span></span> <span data-ttu-id="37e40-111">DirectShow fornisce due motori di rendering:</span><span class="sxs-lookup"><span data-stu-id="37e40-111">DirectShow provides two render engines:</span></span>

-   <span data-ttu-id="37e40-112">Motore di rendering di base: compila un grafico di filtro che recapita output non compresso.</span><span class="sxs-lookup"><span data-stu-id="37e40-112">Basic render engine: Builds a filter graph that delivers uncompressed output.</span></span>
-   <span data-ttu-id="37e40-113">Motore di rendering intelligente: compila un grafico di filtro che recapita l'output compresso.</span><span class="sxs-lookup"><span data-stu-id="37e40-113">Smart render engine: Builds a filter graph that delivers compressed output.</span></span>

<span data-ttu-id="37e40-114">Il motore di rendering intelligente utilizza la ricompressione intelligente per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="37e40-114">The smart render engine uses smart recompression to improve performance.</span></span> <span data-ttu-id="37e40-115">Con la ricompressione intelligente, i file di origine vengono ricompressi solo quando il formato di file originale è diverso dal formato di output finale.</span><span class="sxs-lookup"><span data-stu-id="37e40-115">With smart recompression, source files are recompressed only when the original file format differs from the final output format.</span></span> <span data-ttu-id="37e40-116">Se i formati corrispondono, l'origine non viene mai decompressa.</span><span class="sxs-lookup"><span data-stu-id="37e40-116">If the formats match, the source is never decompressed.</span></span> <span data-ttu-id="37e40-117">La ricompressione intelligente è supportata solo per la compressione video, non per la compressione audio.</span><span class="sxs-lookup"><span data-stu-id="37e40-117">Smart recompression is supported only for video compression, not for audio compression.</span></span>

<span data-ttu-id="37e40-118">Per l'anteprima, usare il motore di rendering di base.</span><span class="sxs-lookup"><span data-stu-id="37e40-118">For preview, use the basic render engine.</span></span> <span data-ttu-id="37e40-119">Il motore di rendering intelligente può anche essere visualizzato in anteprima, ma meno efficiente perché deve decomprimere il flusso compresso.</span><span class="sxs-lookup"><span data-stu-id="37e40-119">The smart render engine can also preview, but less efficiently because it has to decompress the compressed stream.</span></span> <span data-ttu-id="37e40-120">Per la scrittura di file, usare il motore di rendering intelligente se si desidera la ricompressione intelligente.</span><span class="sxs-lookup"><span data-stu-id="37e40-120">For writing files, use the smart render engine if you want smart recompression.</span></span> <span data-ttu-id="37e40-121">In caso contrario, usare il motore di rendering di base.</span><span class="sxs-lookup"><span data-stu-id="37e40-121">Otherwise, use the basic render engine.</span></span> <span data-ttu-id="37e40-122">La ricompressione intelligente può ridurre notevolmente il tempo necessario per la scrittura del file.</span><span class="sxs-lookup"><span data-stu-id="37e40-122">Smart recompression can greatly reduce the time it takes to write the file.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="37e40-123">Non usare il motore di rendering intelligente per leggere o scrivere file di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="37e40-123">Do not use the smart render engine to read or write Windows Media files.</span></span>

 

> [!IMPORTANT]
> <span data-ttu-id="37e40-124">Entrambi i motori di rendering creano una finestra invisibile che elabora i messaggi.</span><span class="sxs-lookup"><span data-stu-id="37e40-124">Both render engines create an invisible window that processes messages.</span></span> <span data-ttu-id="37e40-125">Il thread che crea il motore di rendering deve disporre di un ciclo di messaggi per inviare i messaggi.</span><span class="sxs-lookup"><span data-stu-id="37e40-125">The thread that creates the render engine must have a message loop, to dispatch messages.</span></span> <span data-ttu-id="37e40-126">Inoltre, il thread non deve uscire finché non vengono rilasciati il motore di rendering e il gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="37e40-126">Also, that thread must not exit until the Render Engine and the Filter Graph Manager are released.</span></span> <span data-ttu-id="37e40-127">In caso contrario, l'applicazione potrebbe verificarsi un deadlock.</span><span class="sxs-lookup"><span data-stu-id="37e40-127">Otherwise, the application might deadlock.</span></span>

 

<span data-ttu-id="37e40-128">Creazione del grafico di filtro</span><span class="sxs-lookup"><span data-stu-id="37e40-128">Constructing the Filter Graph</span></span>

<span data-ttu-id="37e40-129">Il grafico a filtro è compilato in due fasi.</span><span class="sxs-lookup"><span data-stu-id="37e40-129">The filter graph is built in two stages.</span></span> <span data-ttu-id="37e40-130">Nella prima fase, il motore di rendering costruisce un "front-end", ovvero un grafico a filtro parziale.</span><span class="sxs-lookup"><span data-stu-id="37e40-130">In the first stage, the render engine constructs a "front end," which is a partial filter graph.</span></span> <span data-ttu-id="37e40-131">Il diagramma seguente illustra un tipico front-end:</span><span class="sxs-lookup"><span data-stu-id="37e40-131">The following diagram illustrates a typical front end:</span></span>

![front-end del grafico filtro](images/rendeng1.png)

<span data-ttu-id="37e40-133">I sottosistemi contengono diversi filtri specializzati, che vengono assemblati automaticamente dal motore di rendering.</span><span class="sxs-lookup"><span data-stu-id="37e40-133">The subsystems contain various specialized filters, which the render engine assembles automatically.</span></span> <span data-ttu-id="37e40-134">Il front-end contiene un pin di output per ogni gruppo nella sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="37e40-134">The front end contains one output pin for each group in the timeline.</span></span> <span data-ttu-id="37e40-135">I pin di output restituiscono dati non compressi se si usa il motore di rendering di base o i dati compressi se si usa il motore di rendering intelligente.</span><span class="sxs-lookup"><span data-stu-id="37e40-135">The output pins deliver uncompressed data if you use the basic render engine, or compressed data if you use the smart render engine.</span></span>

<span data-ttu-id="37e40-136">Nel secondo passaggio, i pin di output sono connessi ai filtri di rendering.</span><span class="sxs-lookup"><span data-stu-id="37e40-136">In the second step, the output pins are connected to rendering filters.</span></span> <span data-ttu-id="37e40-137">Per l'anteprima, i filtri di rendering sono renderer video e audio.</span><span class="sxs-lookup"><span data-stu-id="37e40-137">For preview, the rendering filters are video and audio renderers.</span></span> <span data-ttu-id="37e40-138">Per la scrittura di file, i filtri di rendering sono filtri multiplexer (MUX) e filtri di file writer.</span><span class="sxs-lookup"><span data-stu-id="37e40-138">For file writing, the rendering filters are multiplexer (mux) filters and file-writer filters.</span></span>

![completamento del grafico di filtro](images/rendeng2.png)

## <a name="related-topics"></a><span data-ttu-id="37e40-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="37e40-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37e40-141">Visualizzazione in anteprima di un progetto</span><span class="sxs-lookup"><span data-stu-id="37e40-141">Previewing a Project</span></span>](previewing-a-project.md)
</dt> <dt>

[<span data-ttu-id="37e40-142">Scrittura di un progetto in un file</span><span class="sxs-lookup"><span data-stu-id="37e40-142">Writing a Project to a File</span></span>](writing-a-project-to-a-file.md)
</dt> </dl>

 

 



