---
description: Architettura di servizi di modifica DirectShow
ms.assetid: ba6cc3f1-9130-4197-8501-c2d0a088e847
title: Architettura di servizi di modifica DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c6059eebe9228e61d3de9677972eedfcb51c62
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303779"
---
# <a name="directshow-editing-services-architecture"></a><span data-ttu-id="76282-103">Architettura di servizi di modifica DirectShow</span><span class="sxs-lookup"><span data-stu-id="76282-103">DirectShow Editing Services Architecture</span></span>

<span data-ttu-id="76282-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="76282-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="76282-105">Nella figura seguente è illustrata l'architettura dei [servizi di modifica DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="76282-105">The following illustration shows the architecture of [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

![architettura di servizi di modifica DirectShow](images/architecture.png)

-   <span data-ttu-id="76282-107">Sequenza temporale: rappresenta una produzione video come raccolta di clip di origine, transizioni ed effetti, organizzati in un set di tracce nidificate.</span><span class="sxs-lookup"><span data-stu-id="76282-107">Timeline: Represents a video production as a collection of source clips, transitions, and effects, organized into a set of nested tracks.</span></span> <span data-ttu-id="76282-108">Per ulteriori informazioni, vedere [il modello di sequenza temporale](the-timeline-model.md).</span><span class="sxs-lookup"><span data-stu-id="76282-108">For more information, see [The Timeline Model](the-timeline-model.md).</span></span>
-   <span data-ttu-id="76282-109">Parser XML: analizza la sequenza temporale e genera un file di output oppure legge un file di input e genera una sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="76282-109">XML Parser: Parses the timeline and generates an output file, or reads an input file and generates a timeline.</span></span> <span data-ttu-id="76282-110">DES supporta un formato di persistenza basato su XML.</span><span class="sxs-lookup"><span data-stu-id="76282-110">DES supports an XML-based persistence format.</span></span>
-   <span data-ttu-id="76282-111">Motore di rendering: converte la sequenza temporale in un modulo di cui è possibile eseguire il rendering come flussi multimediali.</span><span class="sxs-lookup"><span data-stu-id="76282-111">Render engine: Translates the timeline into a form that can be rendered as streaming media.</span></span> <span data-ttu-id="76282-112">Per impostazione predefinita, il motore di rendering genera un grafico di filtro DirectShow (vedere la sezione successiva).</span><span class="sxs-lookup"><span data-stu-id="76282-112">By default, the render engine produces a DirectShow filter graph (see next section).</span></span>
-   <span data-ttu-id="76282-113">Media Locator: mantiene una cache di posizioni di elementi multimediali.</span><span class="sxs-lookup"><span data-stu-id="76282-113">Media locator: Maintains a cache of locations of media elements.</span></span> <span data-ttu-id="76282-114">Quando un tentativo di apertura di un elemento multimediale ha esito negativo, DES usa la cache per individuare l'elemento, in base a una cronologia di apertura riuscita.</span><span class="sxs-lookup"><span data-stu-id="76282-114">When an attempt to open a media element fails, DES uses the cache to locate the element, based on a history of successful opens.</span></span>

<span data-ttu-id="76282-115">La sequenza temporale è una descrizione astratta di un progetto di modifica video.</span><span class="sxs-lookup"><span data-stu-id="76282-115">The timeline is an abstract description of a video editing project.</span></span> <span data-ttu-id="76282-116">Specifica le clip di origine utilizzate nel progetto, le ore di inizio e di fine, gli effetti e le transizioni e così via.</span><span class="sxs-lookup"><span data-stu-id="76282-116">It specifies the source clips used in the project, start and stop times, effects and transitions, and so forth.</span></span> <span data-ttu-id="76282-117">Tuttavia, la sequenza temporale non esegue il rendering dei flussi video e audio.</span><span class="sxs-lookup"><span data-stu-id="76282-117">The timeline does not render the video and audio streams, however.</span></span> <span data-ttu-id="76282-118">Al contrario, il motore di rendering converte la sequenza temporale in un grafico di filtro, sia per l'anteprima che per l'output del file.</span><span class="sxs-lookup"><span data-stu-id="76282-118">Instead, the render engine translates the timeline into a filter graph, for either preview or file output.</span></span> <span data-ttu-id="76282-119">Un'applicazione modifica la sequenza temporale anziché modificare direttamente il grafico del filtro, operazione complessa e soggetta a errori.</span><span class="sxs-lookup"><span data-stu-id="76282-119">An application manipulates the timeline rather than directly manipulating the filter graph, which would be cumbersome and error prone.</span></span>

<span data-ttu-id="76282-120">Nella tabella seguente sono elencate le attività principali eseguite da una tipica applicazione di modifica video, insieme alle interfacce che supportano ogni attività.</span><span class="sxs-lookup"><span data-stu-id="76282-120">The following table lists the main tasks that a typical video editing application performs, along with the interfaces that support each task.</span></span> <span data-ttu-id="76282-121">Le sezioni successive descrivono queste attività e le interfacce in modo più dettagliato.</span><span class="sxs-lookup"><span data-stu-id="76282-121">Later sections describe these tasks and the interfaces in more detail.</span></span>



| <span data-ttu-id="76282-122">Attività</span><span class="sxs-lookup"><span data-stu-id="76282-122">Task</span></span>                                     | <span data-ttu-id="76282-123">Interfaccia/e</span><span class="sxs-lookup"><span data-stu-id="76282-123">Interface(s)</span></span>                                                                             |
|------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="76282-124">Creare o modificare una sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="76282-124">Construct or modify a timeline.</span></span>          | <span data-ttu-id="76282-125">[**IAMTimeline**](iamtimeline.md) e altre interfacce **IAMTimelineXXXX**</span><span class="sxs-lookup"><span data-stu-id="76282-125">[**IAMTimeline**](iamtimeline.md) and the other **IAMTimelineXXXX** interfaces</span></span>          |
| <span data-ttu-id="76282-126">Salvare e caricare i file di progetto.</span><span class="sxs-lookup"><span data-stu-id="76282-126">Save and load project files.</span></span>             | [<span data-ttu-id="76282-127">**IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="76282-127">**IXml2Dex**</span></span>](ixml2dex.md)                                                             |
| <span data-ttu-id="76282-128">Visualizzare in anteprima un progetto o scriverlo in un file.</span><span class="sxs-lookup"><span data-stu-id="76282-128">Preview a project or write it to a file.</span></span> | <span data-ttu-id="76282-129">[**IRenderEngine**](irenderengine.md), [ **ISmartRenderEngine**](ismartrenderengine.md)</span><span class="sxs-lookup"><span data-stu-id="76282-129">[**IRenderEngine**](irenderengine.md), [**ISmartRenderEngine**](ismartrenderengine.md)</span></span> |



 

<span data-ttu-id="76282-130">Inoltre, un'applicazione può eseguire alcune o tutte le attività secondarie riportate di seguito.</span><span class="sxs-lookup"><span data-stu-id="76282-130">In addition, an application might perform some or all of the following secondary tasks.</span></span>



| <span data-ttu-id="76282-131">Attività</span><span class="sxs-lookup"><span data-stu-id="76282-131">Task</span></span>                                                                                           | <span data-ttu-id="76282-132">Interfaccia/e</span><span class="sxs-lookup"><span data-stu-id="76282-132">Interface(s)</span></span>                                                                 |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="76282-133">Ottenere informazioni sui file multimediali.</span><span class="sxs-lookup"><span data-stu-id="76282-133">Obtain information about media files.</span></span> <span data-ttu-id="76282-134">(Numero di flussi, formato e durata di ogni flusso).</span><span class="sxs-lookup"><span data-stu-id="76282-134">(Number of streams; format and duration of each stream.)</span></span> | [<span data-ttu-id="76282-135">**IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="76282-135">**IMediaDet**</span></span>](imediadet.md)                                               |
| <span data-ttu-id="76282-136">Impostare le proprietà per transizioni ed effetti.</span><span class="sxs-lookup"><span data-stu-id="76282-136">Set properties on transitions and effects.</span></span>                                                     | [<span data-ttu-id="76282-137">**IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="76282-137">**IPropertySetter**</span></span>](ipropertysetter.md)                                   |
| <span data-ttu-id="76282-138">Ricevere una notifica quando si verificano errori durante il rendering.</span><span class="sxs-lookup"><span data-stu-id="76282-138">Receive notification when errors occur during rendering.</span></span>                                       | <span data-ttu-id="76282-139">[**IAMSetErrorLog**](iamseterrorlog.md), [ **IAMErrorLog**](iamerrorlog.md)</span><span class="sxs-lookup"><span data-stu-id="76282-139">[**IAMSetErrorLog**](iamseterrorlog.md), [**IAMErrorLog**](iamerrorlog.md)</span></span> |
| <span data-ttu-id="76282-140">Recuperare i frame del poster.</span><span class="sxs-lookup"><span data-stu-id="76282-140">Retrieve poster frames.</span></span>                                                                        | <span data-ttu-id="76282-141">[**IMediaDet**](imediadet.md), [ **ISampleGrabber**](isamplegrabber.md)</span><span class="sxs-lookup"><span data-stu-id="76282-141">[**IMediaDet**](imediadet.md), [**ISampleGrabber**](isamplegrabber.md)</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="76282-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="76282-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76282-143">Introduzione con i servizi di modifica DirectShow</span><span class="sxs-lookup"><span data-stu-id="76282-143">Getting Started with DirectShow Editing Services</span></span>](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



