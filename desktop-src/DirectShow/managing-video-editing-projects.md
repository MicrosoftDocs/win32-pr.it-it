---
description: Gestione dei progetti di modifica video
ms.assetid: f8d74807-562f-429b-93a1-e65d0f15163b
title: Gestione dei progetti di modifica video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 491cfcb9a6e94874d2cae43567b61666bbd43cd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303852"
---
# <a name="managing-video-editing-projects"></a><span data-ttu-id="86e7d-103">Gestione dei progetti di modifica video</span><span class="sxs-lookup"><span data-stu-id="86e7d-103">Managing Video Editing Projects</span></span>

<span data-ttu-id="86e7d-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="86e7d-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="86e7d-105">I suggerimenti seguenti consentono di gestire i progetti in [servizi di modifica DirectShow](directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="86e7d-105">The following tips will help you to manage projects in [DirectShow Editing Services](directshow-editing-services.md).</span></span>

<span data-ttu-id="86e7d-106">Modifiche alla sequenza temporale</span><span class="sxs-lookup"><span data-stu-id="86e7d-106">Changes to the Timeline</span></span>

-   <span data-ttu-id="86e7d-107">Se si modifica la sequenza temporale dopo aver compilato il grafico del filtro, chiamare di nuovo [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) per ricompilare il front-end.</span><span class="sxs-lookup"><span data-stu-id="86e7d-107">If you change the timeline after you build the filter graph, call [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) again to rebuild the front end.</span></span> <span data-ttu-id="86e7d-108">In genere, ciò non influisce sul resto del grafo.</span><span class="sxs-lookup"><span data-stu-id="86e7d-108">Usually, this does not affect the rest of the graph.</span></span> <span data-ttu-id="86e7d-109">In alcuni casi, tuttavia, il motore di rendering deve eliminare l'intero grafico prima di ricompilare il front-end.</span><span class="sxs-lookup"><span data-stu-id="86e7d-109">Occasionally, however, the render engine needs to delete the entire graph before it rebuilds the front end.</span></span> <span data-ttu-id="86e7d-110">Questa situazione si verifica, ad esempio, se si aggiunge o si rimuove un gruppo. Il metodo **ConnectFrontEnd** restituisce \_ un avviso \_ OUTPUTRESET per segnalare che il grafo è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="86e7d-110">(For example, this happens if you add or remove a group.) The **ConnectFrontEnd** method returns S\_WARN\_OUTPUTRESET to signal that it deleted the graph.</span></span> <span data-ttu-id="86e7d-111">In tal caso, l'applicazione deve ricompilare la sezione di rendering del grafico.</span><span class="sxs-lookup"><span data-stu-id="86e7d-111">If this happens, your application must rebuild the rendering section of the graph.</span></span>
-   <span data-ttu-id="86e7d-112">Per rimuovere completamente tutti gli oggetti dalla sequenza temporale, chiamare il metodo [**IAMTimeline:: ClearAllGroups**](iamtimeline-clearallgroups.md) .</span><span class="sxs-lookup"><span data-stu-id="86e7d-112">To remove all objects completely from the timeline, call the [**IAMTimeline::ClearAllGroups**](iamtimeline-clearallgroups.md) method.</span></span>

<span data-ttu-id="86e7d-113">**Pulizia**</span><span class="sxs-lookup"><span data-stu-id="86e7d-113">**Cleanup**</span></span>

-   <span data-ttu-id="86e7d-114">Al termine dell'utilizzo di un motore di rendering, chiamare il metodo [**IRenderEngine:: ScrapIt**](irenderengine-scrapit.md) .</span><span class="sxs-lookup"><span data-stu-id="86e7d-114">When you are finished using a render engine, call the [**IRenderEngine::ScrapIt**](irenderengine-scrapit.md) method.</span></span> <span data-ttu-id="86e7d-115">Come per qualsiasi oggetto COM, assicurarsi di rilasciare ogni puntatore a interfaccia al termine dell'uso.</span><span class="sxs-lookup"><span data-stu-id="86e7d-115">As with any COM object, be sure to release every interface pointer when you are finished using it.</span></span>
-   <span data-ttu-id="86e7d-116">Il motore di rendering non mantiene un conteggio dei riferimenti nella sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="86e7d-116">The render engine does not keep a reference count on the timeline.</span></span> <span data-ttu-id="86e7d-117">Non rilasciare la sequenza temporale prima di procedere con l'uso e chiamare sempre **ScrapIt** sul motore di rendering.</span><span class="sxs-lookup"><span data-stu-id="86e7d-117">Do not release the timeline before you are done using it, and always call **ScrapIt** on the render engine first.</span></span>
-   <span data-ttu-id="86e7d-118">Se si rilasciano tutti i riferimenti a una sequenza temporale, non usare alcuno degli oggetti in tale sequenza temporale, anche se sono presenti conteggi dei riferimenti su di essi.</span><span class="sxs-lookup"><span data-stu-id="86e7d-118">If you release all references to a timeline, do not use any of the objects in that timeline, even if you are holding reference counts on them.</span></span>

<span data-ttu-id="86e7d-119">**Più istanze della sequenza temporale**</span><span class="sxs-lookup"><span data-stu-id="86e7d-119">**Multiple Timeline Instances**</span></span>

-   <span data-ttu-id="86e7d-120">Non spostare oggetti sequenza temporale tra sequenze temporali.</span><span class="sxs-lookup"><span data-stu-id="86e7d-120">Do not move timeline objects between timelines.</span></span> <span data-ttu-id="86e7d-121">Ogni oggetto in una sequenza temporale deve essere creato da tale sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="86e7d-121">Every object in a timeline must be created by that timeline.</span></span> <span data-ttu-id="86e7d-122">La sequenza temporale include una cache interna con informazioni sugli oggetti creati; lo stato di avanzamento degli oggetti Timeline può compromettere la cache.</span><span class="sxs-lookup"><span data-stu-id="86e7d-122">The timeline holds an internal cache with information about the objects that it creates; moving timeline objects can disrupt the cache.</span></span>
-   <span data-ttu-id="86e7d-123">Non usare mai la stessa istanza di un motore di rendering con più di una sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="86e7d-123">Never use the same instance of a render engine with more than one timeline.</span></span> <span data-ttu-id="86e7d-124">Il motore di rendering include una cache con informazioni sulla sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="86e7d-124">The render engine holds a cache with information about the timeline.</span></span> <span data-ttu-id="86e7d-125">Più sequenze temporali comprometteranno la cache e causeranno risultati imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="86e7d-125">Multiple timelines will disrupt the cache and cause unpredictable results.</span></span> <span data-ttu-id="86e7d-126">Se sono necessarie due sequenze temporali attive, creare istanze separate dei motori di rendering per ogni sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="86e7d-126">If you need two active timelines, make separate instances of render engines for each timeline.</span></span>
-   <span data-ttu-id="86e7d-127">Una sequenza temporale può usare più di un motore di rendering, ma non nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="86e7d-127">A timeline can use more than one render engine, but not at the same time.</span></span> <span data-ttu-id="86e7d-128">Eliminare il motore di rendering precedente prima di utilizzare un altro motore di rendering.</span><span class="sxs-lookup"><span data-stu-id="86e7d-128">Delete the old render engine before using another render engine.</span></span> <span data-ttu-id="86e7d-129">Questa operazione viene eseguita in genere quando si passa dall'utilizzo del motore di rendering di base per l'anteprima al motore di rendering intelligente per la scrittura di file.</span><span class="sxs-lookup"><span data-stu-id="86e7d-129">(You would typically do this when you switch from using the basic render engine for preview to the smart render engine for file writing.)</span></span>

<span data-ttu-id="86e7d-130">**Persistenza**</span><span class="sxs-lookup"><span data-stu-id="86e7d-130">**Persistence**</span></span>

-   <span data-ttu-id="86e7d-131">Il grafico del filtro non è permanente quando si salva il progetto in un file XML.</span><span class="sxs-lookup"><span data-stu-id="86e7d-131">The filter graph is not persistent when you save the project to an XML file.</span></span> <span data-ttu-id="86e7d-132">Pertanto, si perderanno tutte le informazioni relative al ricompressione intelligente, al formato di compressione o ai parametri di compressione.</span><span class="sxs-lookup"><span data-stu-id="86e7d-132">Therefore, you lose any information relating to smart recompression, compression format, or compression parameters.</span></span> <span data-ttu-id="86e7d-133">Al termine del caricamento di un progetto, l'applicazione deve ripristinare questi parametri.</span><span class="sxs-lookup"><span data-stu-id="86e7d-133">It is up to the application to restore these parameters after it loads a project.</span></span>

## <a name="related-topics"></a><span data-ttu-id="86e7d-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="86e7d-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86e7d-135">Uso dei servizi di modifica DirectShow</span><span class="sxs-lookup"><span data-stu-id="86e7d-135">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



