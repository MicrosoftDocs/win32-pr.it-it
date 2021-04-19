---
description: In questa sezione vengono descritte le nuove funzionalità aggiunte ai contatori delle prestazioni per ogni versione.
ms.assetid: 14bdae6c-9dcd-401e-8c43-5391e00cf7e3
title: Novità (contatori delle prestazioni)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f0c1189a185351eabae438a01c6f111952f164e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312104"
---
# <a name="whats-new-with-performance-counters"></a><span data-ttu-id="a952e-103">Novità dei contatori delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="a952e-103">What's New with Performance Counters</span></span>

<span data-ttu-id="a952e-104">In questa sezione vengono descritte le nuove funzionalità aggiunte ai contatori delle prestazioni per ogni versione.</span><span class="sxs-lookup"><span data-stu-id="a952e-104">This section describes the new features that were added to Performance Counters for each release.</span></span>

## <a name="windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="a952e-105">Windows 7 e Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a952e-105">Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="a952e-106">Lo strumento [CTRPP](ctrpp.md) è stato modificato per migliorare e semplificare la generazione di codice.</span><span class="sxs-lookup"><span data-stu-id="a952e-106">The [CTRPP](ctrpp.md) tool was changed to improve and simplify code generation.</span></span> <span data-ttu-id="a952e-107">Lo strumento ora genera solo un file di intestazione e di risorse.</span><span class="sxs-lookup"><span data-stu-id="a952e-107">The tool now generates only a header and resource file.</span></span> <span data-ttu-id="a952e-108">Se si vuole un comportamento di generazione del codice obsoleto (non consigliato), è possibile usare il nuovo `-legacy` argomento.</span><span class="sxs-lookup"><span data-stu-id="a952e-108">If you want to old code generation behavior (not recommended), you can use the new `-legacy` argument.</span></span>

- <span data-ttu-id="a952e-109">È ora necessario specificare i nuovi `-o` `-rc` argomenti e che specificano rispettivamente il nome e il percorso del file di intestazione e di risorse.</span><span class="sxs-lookup"><span data-stu-id="a952e-109">You must now specify the new `-o` and `-rc` arguments that specify the name and location of the header and resource file, respectively.</span></span>
- <span data-ttu-id="a952e-110">È possibile usare il nuovo `-prefix` argomento facoltativo per specificare una stringa da aggiungere all'inizio delle variabili globali e delle funzioni definite nel file di intestazione generato.</span><span class="sxs-lookup"><span data-stu-id="a952e-110">You can use the optional new `-prefix` argument to specify a string to add to the beginning of global variables and functions defined in the generated header file.</span></span>
- <span data-ttu-id="a952e-111">Se è necessario aggiornare il manifesto dei contatori, l'utilizzo della nuova generazione del codice elimina la necessità di eseguire il merge dell'implementazione di callback precedente con il nuovo codice generato poiché i callback non sono più inclusi nel codice generato.</span><span class="sxs-lookup"><span data-stu-id="a952e-111">If you have to update your counters manifest, using the new code generation eliminates the need to merge your previous callback implementation with the new generated code since the callbacks are no longer included in the generated code.</span></span>

<span data-ttu-id="a952e-112">`symbol`È disponibile un nuovo attributo per gli elementi manifesto seguenti:</span><span class="sxs-lookup"><span data-stu-id="a952e-112">A new `symbol` attribute is available for the following manifest elements:</span></span>

- [<span data-ttu-id="a952e-113">provider</span><span class="sxs-lookup"><span data-stu-id="a952e-113">provider</span></span>](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element)
- [<span data-ttu-id="a952e-114">counterSet</span><span class="sxs-lookup"><span data-stu-id="a952e-114">counterSet</span></span>](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element)
- [<span data-ttu-id="a952e-115">Counter</span><span class="sxs-lookup"><span data-stu-id="a952e-115">counter</span></span>](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element)

<span data-ttu-id="a952e-116">L' `symbol` attributo è obbligatorio per il [provider](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) e il contatore e è facoltativo per il [contatore](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element). [](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element)</span><span class="sxs-lookup"><span data-stu-id="a952e-116">The `symbol` attribute is required for [provider](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) and [counterSet](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element), and is optional for [counter](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element).</span></span> <span data-ttu-id="a952e-117">L'attributo consente di fornire un nome simbolico che è possibile utilizzare per fare riferimento a ogni elemento quando si chiamano le funzioni del provider (ad esempio, è possibile utilizzare il nome simbolico dell'insieme di contatori quando si chiama [PerfCreateInstance](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)).</span><span class="sxs-lookup"><span data-stu-id="a952e-117">The attribute lets you provide a symbolic name that you can use to reference each element when calling the provider functions (for example, you can use the counter set symbolic name when calling [PerfCreateInstance](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)).</span></span>

## <a name="windows-vista"></a><span data-ttu-id="a952e-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a952e-118">Windows Vista</span></span>

<span data-ttu-id="a952e-119">L'architettura dei contatori delle prestazioni per fornire i dati del contatore è stata modificata completamente per questa versione.</span><span class="sxs-lookup"><span data-stu-id="a952e-119">The Performance Counters architecture for providing counter data was completely changed for this release.</span></span>

<span data-ttu-id="a952e-120">In precedenza è stato usato un file INI per definire i dati del contatore ed è stata implementata una DLL di prestazioni che è stata eseguita nel processo del consumer per fornire i dati quando un consumer lo ha richiesto.</span><span class="sxs-lookup"><span data-stu-id="a952e-120">Previously, you used an INI file to define your counter data and you implemented a performance DLL which ran in the consumer's process to provide the data when a consumer requested it.</span></span> <span data-ttu-id="a952e-121">Questa architettura è deprecata e non è consigliata per il nuovo codice a causa di problemi significativi relativi a prestazioni e affidabilità.</span><span class="sxs-lookup"><span data-stu-id="a952e-121">This architecture is deprecated and is not recommended for new code due to significant performance and reliability issues.</span></span>

<span data-ttu-id="a952e-122">La nuova architettura usa un manifesto per definire i dati del contatore ed esegue il codice nel processo del provider per fornire i dati quando un consumer lo richiede.</span><span class="sxs-lookup"><span data-stu-id="a952e-122">The new architecture uses a manifest to define the counter data and runs code in the provider's process to provide the data when a consumer requests it.</span></span> <span data-ttu-id="a952e-123">Per ulteriori informazioni, vedere la pagina relativa alla [fornitura di dati del contatore con la versione 2,0](providing-counter-data-using-version-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="a952e-123">For additional details, see [Providing Counter Data Using Version 2.0](providing-counter-data-using-version-2-0.md).</span></span>

<span data-ttu-id="a952e-124">Per questa versione sono state aggiunte le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="a952e-124">The following functions were added for this release:</span></span>

- [<span data-ttu-id="a952e-125">ControlCallback</span><span class="sxs-lookup"><span data-stu-id="a952e-125">ControlCallback</span></span>](/windows/desktop/api/Perflib/nc-perflib-perflibrequest)
- [<span data-ttu-id="a952e-126">PerfCreateInstance</span><span class="sxs-lookup"><span data-stu-id="a952e-126">PerfCreateInstance</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)
- [<span data-ttu-id="a952e-127">PerfDeleteInstance</span><span class="sxs-lookup"><span data-stu-id="a952e-127">PerfDeleteInstance</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance)
- [<span data-ttu-id="a952e-128">PerfQueryInstance</span><span class="sxs-lookup"><span data-stu-id="a952e-128">PerfQueryInstance</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfqueryinstance)
- [<span data-ttu-id="a952e-129">PerfSetCounterSetInfo</span><span class="sxs-lookup"><span data-stu-id="a952e-129">PerfSetCounterSetInfo</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo)
- [<span data-ttu-id="a952e-130">PerfSetULongCounterValue</span><span class="sxs-lookup"><span data-stu-id="a952e-130">PerfSetULongCounterValue</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
- [<span data-ttu-id="a952e-131">PerfSetULongLongCounterValue</span><span class="sxs-lookup"><span data-stu-id="a952e-131">PerfSetULongLongCounterValue</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
- [<span data-ttu-id="a952e-132">PerfSetCounterRefValue</span><span class="sxs-lookup"><span data-stu-id="a952e-132">PerfSetCounterRefValue</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)
- [<span data-ttu-id="a952e-133">PerfStartProvider</span><span class="sxs-lookup"><span data-stu-id="a952e-133">PerfStartProvider</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider)
- [<span data-ttu-id="a952e-134">PerfStopProvider</span><span class="sxs-lookup"><span data-stu-id="a952e-134">PerfStopProvider</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider)

<span data-ttu-id="a952e-135">Per questa versione sono state aggiunte le strutture seguenti:</span><span class="sxs-lookup"><span data-stu-id="a952e-135">The following structures were added for this release:</span></span>

- [<span data-ttu-id="a952e-136">\_identità contatore \_ prestazioni</span><span class="sxs-lookup"><span data-stu-id="a952e-136">PERF\_COUNTER\_IDENTITY</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identity)
- [<span data-ttu-id="a952e-137">\_informazioni contatore \_ prestazioni</span><span class="sxs-lookup"><span data-stu-id="a952e-137">PERF\_COUNTER\_INFO</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_info)
- [<span data-ttu-id="a952e-138">informazioni sul contatore delle prestazioni \_ \_</span><span class="sxs-lookup"><span data-stu-id="a952e-138">PERF\_COUNTERSET\_INFO</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_info)
- [<span data-ttu-id="a952e-139">istanza del contatore delle prestazioni \_ \_</span><span class="sxs-lookup"><span data-stu-id="a952e-139">PERF\_COUNTERSET\_INSTANCE</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_instance)

<span data-ttu-id="a952e-140">Per un elenco degli elementi XML usati nel manifesto per definire i contatori, vedere [schema dei contatori delle prestazioni](performance-counters-schema.md).</span><span class="sxs-lookup"><span data-stu-id="a952e-140">For a list of the XML elements that you use in your manifest to define your counters, see [Performance Counters Schema](performance-counters-schema.md).</span></span>

<span data-ttu-id="a952e-141">Per informazioni sullo strumento di pre-elaborazione CTRPP che analizza il manifesto e genera il codice usato come punto di partenza per il provider, vedere [CTRPP](ctrpp.md).</span><span class="sxs-lookup"><span data-stu-id="a952e-141">For information on the CTRPP pre-processor tool that parses your manifest and generates the code that you use as the starting point for your provider, see [CTRPP](ctrpp.md).</span></span>
