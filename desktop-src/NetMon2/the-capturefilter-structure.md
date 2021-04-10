---
description: In Network Monitor il filtro di acquisizione viene definito dalla struttura CAPTUREFILTER.
ms.assetid: 03cd35f2-4da5-4ef6-b73f-0bf6e0e33135
title: Struttura CAPTUREFILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3962ef9828ce13a1d03c58e4d7744d2854624858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966763"
---
# <a name="the-capturefilter-structure"></a><span data-ttu-id="bbf0f-103">Struttura CAPTUREFILTER</span><span class="sxs-lookup"><span data-stu-id="bbf0f-103">The CAPTUREFILTER Structure</span></span>

<span data-ttu-id="bbf0f-104">In Network Monitor il [filtro di acquisizione](capture-filters.md) viene definito dalla struttura [**capturefilter**](capturefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="bbf0f-104">In Network Monitor, the [capture filter](capture-filters.md) is defined by the [**CAPTUREFILTER**](capturefilter.md) structure.</span></span> <span data-ttu-id="bbf0f-105">L'assenza o la combinazione di flag, valori ed espressioni determina quali frame verranno passati o eliminati dal driver Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="bbf0f-105">The absence or combination of flags, values, and expressions determines which frames will be passed on or dropped by the Network Monitor driver.</span></span> <span data-ttu-id="bbf0f-106">Nella figura seguente sono illustrate le tre aree dell'analisi del filtro di acquisizione: ETYPE/SAP, Address e pattern match.</span><span class="sxs-lookup"><span data-stu-id="bbf0f-106">The following illustration shows the three areas of the capture filter analysis: Etype/SAP, address, and pattern match.</span></span>

![tre aree dell'analisi del filtro di acquisizione](images/capfilter.png)

<span data-ttu-id="bbf0f-108">La tabella seguente elenca la funzione di ogni elemento filtro di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="bbf0f-108">The following table lists the function of each capture filter element.</span></span>



| <span data-ttu-id="bbf0f-109">Filter - elemento</span><span class="sxs-lookup"><span data-stu-id="bbf0f-109">Filter element</span></span>                                       | <span data-ttu-id="bbf0f-110">Azione</span><span class="sxs-lookup"><span data-stu-id="bbf0f-110">Action</span></span>                                                                                                                                                                                                       |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bbf0f-111">ETYPE/SAP</span><span class="sxs-lookup"><span data-stu-id="bbf0f-111">Etype/SAP</span></span>](writing-etypesap-filter-portion.md)     | <span data-ttu-id="bbf0f-112">Valuta le impostazioni di ETYPE/SAP.</span><span class="sxs-lookup"><span data-stu-id="bbf0f-112">Evaluates Etype/SAP settings.</span></span> <span data-ttu-id="bbf0f-113">La combinazione di flag determina i tipi o i valori di impostazione inclusi o esclusi.</span><span class="sxs-lookup"><span data-stu-id="bbf0f-113">The combination of flags determines which setting types or values are included or excluded.</span></span>                                                                                    |
| [<span data-ttu-id="bbf0f-114">Indirizzo</span><span class="sxs-lookup"><span data-stu-id="bbf0f-114">Address</span></span>](writing-addresstable-filter-portion.md)   | <span data-ttu-id="bbf0f-115">Valuta gli indirizzi di origine e di destinazione e le coppie di indirizzi.</span><span class="sxs-lookup"><span data-stu-id="bbf0f-115">Evaluates source and destination addresses and address pairs.</span></span> <span data-ttu-id="bbf0f-116">Diverse combinazioni di flag determinano quali valori singoli o combinazioni di coppie di indirizzi sono inclusi o esclusi.</span><span class="sxs-lookup"><span data-stu-id="bbf0f-116">Different combinations of flags determine which individual values or combinations of address pairs are included or excluded.</span></span>                   |
| [<span data-ttu-id="bbf0f-117">Corrispondenza criterio</span><span class="sxs-lookup"><span data-stu-id="bbf0f-117">Pattern Match</span></span>](writing-the-patternmatch-filter.md) | <span data-ttu-id="bbf0f-118">Definisce le corrispondenze di modelli complessi all'interno di un frame.</span><span class="sxs-lookup"><span data-stu-id="bbf0f-118">Defines complex pattern matches within a frame.</span></span> <span data-ttu-id="bbf0f-119">I flag vengono forniti per diversi tipi e offset.</span><span class="sxs-lookup"><span data-stu-id="bbf0f-119">Flags are provided for different types and offsets.</span></span> <span data-ttu-id="bbf0f-120">È possibile combinare le corrispondenze dei modelli con le istruzioni operatore AND o OR logiche.</span><span class="sxs-lookup"><span data-stu-id="bbf0f-120">You can combine pattern matches with logical AND or OR operator statements.</span></span>                              |
| [<span data-ttu-id="bbf0f-121">Ritaglio</span><span class="sxs-lookup"><span data-stu-id="bbf0f-121">Clipping</span></span>](clipping-a-frame.md)                     | <span data-ttu-id="bbf0f-122">Consente di riagganciare i frame in un modo specificato da diversi valori di byte.</span><span class="sxs-lookup"><span data-stu-id="bbf0f-122">Clips frames in a manner specified by various byte values.</span></span> <span data-ttu-id="bbf0f-123">È possibile utilizzare solo questo elemento per ritagliare tutti i frame o utilizzarlo con altri elementi di filtro di acquisizione. ad esempio, per trovare e quindi ritagliare un singolo frame.</span><span class="sxs-lookup"><span data-stu-id="bbf0f-123">You can use only this element to clip all frames or use it with other capture filter elements; for example, to find and then clip a single frame.</span></span> |
| [<span data-ttu-id="bbf0f-124">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="bbf0f-124">**Trigger**</span></span>](trigger.md)                           | <span data-ttu-id="bbf0f-125">Questo elemento del filtro di acquisizione è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="bbf0f-125">This capture filter element is obsolete.</span></span> <span data-ttu-id="bbf0f-126">I trigger non fanno più parte di un filtro di acquisizione. sono ora contenute nei propri tag BLOB, che vengono specificati separatamente.</span><span class="sxs-lookup"><span data-stu-id="bbf0f-126">Triggers are no longer part of a capture filter; they are now contained in their own BLOB tags, which are specified separately.</span></span>                                     |



 

<span data-ttu-id="bbf0f-127">Un frame viene valutato rispetto a tutte e tre le parti del filtro di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="bbf0f-127">A frame is evaluated against all three portions of the capture filter.</span></span> <span data-ttu-id="bbf0f-128">Pertanto, un frame trasmesso correttamente deve superare ogni elemento.</span><span class="sxs-lookup"><span data-stu-id="bbf0f-128">Therefore, a successfully transmitted frame must pass each element.</span></span> <span data-ttu-id="bbf0f-129">Tenere presente che il driver Network Monitor valuta l'assenza di uno dei tre elementi come **true**.</span><span class="sxs-lookup"><span data-stu-id="bbf0f-129">Be aware that the Network Monitor driver evaluates the absence of any of the three elements as **TRUE**.</span></span> <span data-ttu-id="bbf0f-130">Il driver, ad esempio, valuta l'assenza di una sezione ETYPE/SAP "tutti i frame con qualsiasi valore ETYPE/SAP sono validi".</span><span class="sxs-lookup"><span data-stu-id="bbf0f-130">For example, the driver evaluates the absence of an Etype/SAP section as "ALL frames with the ANY Etype/SAP value are valid."</span></span>

 

 



