---
description: Passaggio 1.
ms.assetid: 4b2d3add-0430-480b-ad5f-bb1aa19fef21
title: Passaggio 1. Scegliere una classe di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4679873e78e75b350335b5294db63579fd41f36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883121"
---
# <a name="step-1-choose-a-base-class"></a><span data-ttu-id="acaac-104">Passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="acaac-104">Step 1.</span></span> <span data-ttu-id="acaac-105">Scegliere una classe di base</span><span class="sxs-lookup"><span data-stu-id="acaac-105">Choose a Base Class</span></span>

<span data-ttu-id="acaac-106">Questo è il passaggio 1 dell'esercitazione [scrittura dei filtri di trasformazione](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="acaac-106">This is step 1 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="acaac-107">Supponendo che si decida di scrivere un filtro e non un DMO, il primo passaggio consiste nella scelta della classe di base da usare.</span><span class="sxs-lookup"><span data-stu-id="acaac-107">Assuming that you decide to write a filter and not a DMO, the first step is choosing which base class to use.</span></span> <span data-ttu-id="acaac-108">Le classi seguenti sono appropriate per i filtri di trasformazione:</span><span class="sxs-lookup"><span data-stu-id="acaac-108">The following classes are appropriate for transform filters:</span></span>

-   <span data-ttu-id="acaac-109">[**CTransformFilter**](ctransformfilter.md) è progettato per i filtri di trasformazione che usano buffer di input e output distinti.</span><span class="sxs-lookup"><span data-stu-id="acaac-109">[**CTransformFilter**](ctransformfilter.md) is designed for transform filters that use separate input and output buffers.</span></span> <span data-ttu-id="acaac-110">Questo tipo di filtro viene talvolta definito filtro di copia/trasformazione.</span><span class="sxs-lookup"><span data-stu-id="acaac-110">This kind of filter is sometimes called a copy-transform filter.</span></span> <span data-ttu-id="acaac-111">Quando un filtro di copia-trasformazione riceve un esempio di input, scrive nuovi dati in un esempio di output e recapita l'esempio di output al filtro successivo.</span><span class="sxs-lookup"><span data-stu-id="acaac-111">When a copy-transform filter receives an input sample, it writes new data to an output sample and delivers the output sample to the next filter.</span></span>
-   <span data-ttu-id="acaac-112">[**CTransInPlaceFilter**](ctransinplacefilter.md) è progettato per i filtri che modificano i dati nel buffer originale, detti anche filtri trans-on-Place.</span><span class="sxs-lookup"><span data-stu-id="acaac-112">[**CTransInPlaceFilter**](ctransinplacefilter.md) is designed for filters that modify data in the original buffer, also called trans-in-place filters.</span></span> <span data-ttu-id="acaac-113">Quando un filtro Trans-on-Place riceve un esempio, modifica i dati all'interno dell'esempio e recapita lo stesso campione downstream.</span><span class="sxs-lookup"><span data-stu-id="acaac-113">When a trans-in-place filter receives a sample, it changes the data inside that sample and delivers the same sample downstream.</span></span> <span data-ttu-id="acaac-114">Il pin di input e il pin di output del filtro si connettono sempre con i tipi di supporto corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="acaac-114">The filter's input pin and output pin always connect with matching media types.</span></span>
-   <span data-ttu-id="acaac-115">[**CVideoTransformFilter**](cvideotransformfilter.md) è progettato principalmente per i decodificatori video.</span><span class="sxs-lookup"><span data-stu-id="acaac-115">[**CVideoTransformFilter**](cvideotransformfilter.md) is designed primarily for video decoders.</span></span> <span data-ttu-id="acaac-116">Deriva da **CTransformFilter**, ma include funzionalità per l'eliminazione di frame se il renderer downstream si trova dietro.</span><span class="sxs-lookup"><span data-stu-id="acaac-116">It derives from **CTransformFilter**, but includes functionality for dropping frames if the downstream renderer falls behind.</span></span>
-   <span data-ttu-id="acaac-117">[**CBaseFilter**](cbasefilter.md) è una classe di filtro generica.</span><span class="sxs-lookup"><span data-stu-id="acaac-117">[**CBaseFilter**](cbasefilter.md) is a generic filter class.</span></span> <span data-ttu-id="acaac-118">Tutte le altre classi in questo elenco derivano da **CBaseFilter**.</span><span class="sxs-lookup"><span data-stu-id="acaac-118">The other classes in this list all derive from **CBaseFilter**.</span></span> <span data-ttu-id="acaac-119">Se nessuno di essi è adatto, è possibile eseguire il fallback su questa classe.</span><span class="sxs-lookup"><span data-stu-id="acaac-119">If none of them is suitable, you can fall back on this class.</span></span> <span data-ttu-id="acaac-120">Tuttavia, questa classe richiede anche il maggior numero di lavoro da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="acaac-120">However, this class also requires the most work on your part.</span></span>
-   <span data-ttu-id="acaac-121">\[! Importante\]</span><span class="sxs-lookup"><span data-stu-id="acaac-121">\[!Important\]</span></span>  
    > <span data-ttu-id="acaac-122">Le trasformazioni video sul posto possono avere un notevole effetto sulle prestazioni di rendering.</span><span class="sxs-lookup"><span data-stu-id="acaac-122">In-place video transforms can have a serious impact on rendering performance.</span></span> <span data-ttu-id="acaac-123">Le trasformazioni sul posto richiedono operazioni di lettura-modifica-scrittura nel buffer.</span><span class="sxs-lookup"><span data-stu-id="acaac-123">In-place transforms require read-modify-write operations on the buffer.</span></span> <span data-ttu-id="acaac-124">Se la memoria si trova in una scheda grafica, le operazioni di lettura sono significativamente più lente.</span><span class="sxs-lookup"><span data-stu-id="acaac-124">If the memory resides on a graphics card, read operations are significantly slower.</span></span> <span data-ttu-id="acaac-125">Inoltre, anche una trasformazione copia può causare operazioni di lettura indesiderate se non viene implementata con attenzione.</span><span class="sxs-lookup"><span data-stu-id="acaac-125">Moreover, even a copy transform can cause unintended read operations if you do not implement it carefully.</span></span> <span data-ttu-id="acaac-126">Pertanto, è consigliabile eseguire sempre il test delle prestazioni se si scrive una trasformazione video.</span><span class="sxs-lookup"><span data-stu-id="acaac-126">Therefore, you should always do performance testing if you write a video transform.</span></span>

     

<span data-ttu-id="acaac-127">Per il codificatore RLE di esempio, la scelta migliore è **CTransformFilter** o **CVideoTransformFilter**.</span><span class="sxs-lookup"><span data-stu-id="acaac-127">For the example RLE encoder, the best choice is either **CTransformFilter** or **CVideoTransformFilter**.</span></span> <span data-ttu-id="acaac-128">Infatti, le differenze tra di esse sono in gran parte interne, pertanto è facile eseguire la conversione da una all'altra.</span><span class="sxs-lookup"><span data-stu-id="acaac-128">In fact, the differences between them are largely internal, so it is easy to convert from one to the other.</span></span> <span data-ttu-id="acaac-129">Poiché i tipi di supporto devono essere diversi nei due pin, la classe **CTransInPlaceFilter** non è appropriata per questo filtro.</span><span class="sxs-lookup"><span data-stu-id="acaac-129">Because the media types must be different on the two pins, the **CTransInPlaceFilter** class is not appropriate for this filter.</span></span> <span data-ttu-id="acaac-130">In questo esempio verrà usato **CTransformFilter**.</span><span class="sxs-lookup"><span data-stu-id="acaac-130">This example will use **CTransformFilter**.</span></span>

<span data-ttu-id="acaac-131">Successivo: [passaggio 2. Dichiarare la classe filter](step-2--declare-the-filter-class.md).</span><span class="sxs-lookup"><span data-stu-id="acaac-131">Next: [Step 2. Declare the Filter Class](step-2--declare-the-filter-class.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="acaac-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="acaac-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acaac-133">Scrittura di filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="acaac-133">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



