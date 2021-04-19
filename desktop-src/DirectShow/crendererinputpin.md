---
description: La classe CBaseRendererInputPin implementa un pin di input per la classe CBaseRenderer. Eccetto laddove indicato, i metodi di questa classe delegano ai metodi corrispondenti sulla classe CBaseRenderer.
ms.assetid: da3e6aba-c2cc-4fd4-b382-fc4bc7fef774
title: Classe CRendererInputPin (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ec48b31170b2233f211e7e72de81d8792ae9160
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333172"
---
# <a name="crendererinputpin-class"></a><span data-ttu-id="da7a0-104">Classe CRendererInputPin</span><span class="sxs-lookup"><span data-stu-id="da7a0-104">CRendererInputPin class</span></span>

![crendererinput gerarchia di classi pin](images/rbase01.png)

<span data-ttu-id="da7a0-106">La classe **CBaseRendererInputPin** implementa un pin di input per la classe [**CBaseRenderer**](cbaserenderer.md) .</span><span class="sxs-lookup"><span data-stu-id="da7a0-106">The **CBaseRendererInputPin** class implements an input pin for the [**CBaseRenderer**](cbaserenderer.md) class.</span></span> <span data-ttu-id="da7a0-107">Eccetto laddove indicato, i metodi di questa classe delegano ai metodi corrispondenti sulla classe **CBaseRenderer** .</span><span class="sxs-lookup"><span data-stu-id="da7a0-107">Except where noted, the methods in this class delegate to corresponding methods on the **CBaseRenderer** class.</span></span>



| <span data-ttu-id="da7a0-108">Variabili membro protette</span><span class="sxs-lookup"><span data-stu-id="da7a0-108">Protected Member Variables</span></span>                                       | <span data-ttu-id="da7a0-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da7a0-109">Description</span></span>                                                                            |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="da7a0-110">**\_pRenderer m**</span><span class="sxs-lookup"><span data-stu-id="da7a0-110">**m\_pRenderer**</span></span>](crendererinputpin-m-prenderer.md)            | <span data-ttu-id="da7a0-111">Puntatore al filtro.</span><span class="sxs-lookup"><span data-stu-id="da7a0-111">Pointer to the filter.</span></span>                                                                 |
| <span data-ttu-id="da7a0-112">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="da7a0-112">Public Methods</span></span>                                                   | <span data-ttu-id="da7a0-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da7a0-113">Description</span></span>                                                                            |
| [<span data-ttu-id="da7a0-114">**CRendererInputPin**</span><span class="sxs-lookup"><span data-stu-id="da7a0-114">**CRendererInputPin**</span></span>](crendererinputpin-crendererinputpin.md) | <span data-ttu-id="da7a0-115">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="da7a0-115">Constructor method.</span></span>                                                                    |
| [<span data-ttu-id="da7a0-116">**BreakConnect**</span><span class="sxs-lookup"><span data-stu-id="da7a0-116">**BreakConnect**</span></span>](crendererinputpin-breakconnect.md)           | <span data-ttu-id="da7a0-117">Aggiunge codice personalizzato quando si interrompe una connessione.</span><span class="sxs-lookup"><span data-stu-id="da7a0-117">Adds customized code upon breaking a connection.</span></span>                                       |
| [<span data-ttu-id="da7a0-118">**CompleteConnect**</span><span class="sxs-lookup"><span data-stu-id="da7a0-118">**CompleteConnect**</span></span>](crendererinputpin-completeconnect.md)     | <span data-ttu-id="da7a0-119">Completa la connessione.</span><span class="sxs-lookup"><span data-stu-id="da7a0-119">Completes the connection.</span></span>                                                              |
| [<span data-ttu-id="da7a0-120">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="da7a0-120">**CheckMediaType**</span></span>](crendererinputpin-checkmediatype.md)       | <span data-ttu-id="da7a0-121">Determina se il pin può supportare un tipo di supporto specifico.</span><span class="sxs-lookup"><span data-stu-id="da7a0-121">Determines if the pin can support a specific media type.</span></span>                               |
| [<span data-ttu-id="da7a0-122">**Attivo**</span><span class="sxs-lookup"><span data-stu-id="da7a0-122">**Active**</span></span>](crendererinputpin-active.md)                       | <span data-ttu-id="da7a0-123">Passa il pin alla modalità attiva (in pausa o in esecuzione).</span><span class="sxs-lookup"><span data-stu-id="da7a0-123">Switches the pin to the active (paused or running) mode.</span></span>                               |
| [<span data-ttu-id="da7a0-124">**Inattivo**</span><span class="sxs-lookup"><span data-stu-id="da7a0-124">**Inactive**</span></span>](crendererinputpin-inactive.md)                   | <span data-ttu-id="da7a0-125">Passa il pin a uno stato inattivo e rilascia la memoria dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="da7a0-125">Switches the pin to an inactive state and releases the memory of the allocator.</span></span>        |
| [<span data-ttu-id="da7a0-126">**SetMediaType**</span><span class="sxs-lookup"><span data-stu-id="da7a0-126">**SetMediaType**</span></span>](crendererinputpin-setmediatype.md)           | <span data-ttu-id="da7a0-127">Imposta il tipo di supporto del PIN.</span><span class="sxs-lookup"><span data-stu-id="da7a0-127">Sets the media type of the pin.</span></span>                                                        |
| [<span data-ttu-id="da7a0-128">**Allocatore**</span><span class="sxs-lookup"><span data-stu-id="da7a0-128">**Allocator**</span></span>](crendererinputpin-allocator.md)                 | <span data-ttu-id="da7a0-129">Recupera un puntatore all'allocatore di memoria predefinito.</span><span class="sxs-lookup"><span data-stu-id="da7a0-129">Retrieves a pointer to the default memory allocator.</span></span>                                   |
| <span data-ttu-id="da7a0-130">Metodi IPin</span><span class="sxs-lookup"><span data-stu-id="da7a0-130">IPin Methods</span></span>                                                     | <span data-ttu-id="da7a0-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da7a0-131">Description</span></span>                                                                            |
| [<span data-ttu-id="da7a0-132">**QueryId**</span><span class="sxs-lookup"><span data-stu-id="da7a0-132">**QueryId**</span></span>](crendererinputpin-queryid.md)                     | <span data-ttu-id="da7a0-133">Recupera un identificatore per il PIN.</span><span class="sxs-lookup"><span data-stu-id="da7a0-133">Retrieves an identifier for the pin.</span></span>                                                   |
| [<span data-ttu-id="da7a0-134">**EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="da7a0-134">**EndOfStream**</span></span>](crendererinputpin-endofstream.md)             | <span data-ttu-id="da7a0-135">Informa il pin che non sono previsti dati aggiuntivi fino a quando non viene emesso un nuovo comando di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="da7a0-135">Informs the pin that no additional data is expected until a new run command is issued.</span></span> |
| [<span data-ttu-id="da7a0-136">**BeginFlush**</span><span class="sxs-lookup"><span data-stu-id="da7a0-136">**BeginFlush**</span></span>](crendererinputpin-beginflush.md)               | <span data-ttu-id="da7a0-137">Informa il pin per iniziare un'operazione di svuotamento.</span><span class="sxs-lookup"><span data-stu-id="da7a0-137">Informs the pin to begin a flush operation.</span></span>                                            |
| [<span data-ttu-id="da7a0-138">**EndFlush**</span><span class="sxs-lookup"><span data-stu-id="da7a0-138">**EndFlush**</span></span>](crendererinputpin-endflush.md)                   | <span data-ttu-id="da7a0-139">Informa il pin per terminare un'operazione di svuotamento.</span><span class="sxs-lookup"><span data-stu-id="da7a0-139">Informs the pin to end a flush operation.</span></span>                                              |
| <span data-ttu-id="da7a0-140">Metodi IMemInputPin</span><span class="sxs-lookup"><span data-stu-id="da7a0-140">IMemInputPin Methods</span></span>                                             | <span data-ttu-id="da7a0-141">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da7a0-141">Description</span></span>                                                                            |
| [<span data-ttu-id="da7a0-142">**Ricevere**</span><span class="sxs-lookup"><span data-stu-id="da7a0-142">**Receive**</span></span>](crendererinputpin-receive.md)                     | <span data-ttu-id="da7a0-143">Recupera il blocco di dati successivo dal flusso.</span><span class="sxs-lookup"><span data-stu-id="da7a0-143">Retrieves the next block of data from the stream.</span></span>                                      |



 

## <a name="requirements"></a><span data-ttu-id="da7a0-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da7a0-144">Requirements</span></span>



| <span data-ttu-id="da7a0-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="da7a0-145">Requirement</span></span> | <span data-ttu-id="da7a0-146">Valore</span><span class="sxs-lookup"><span data-stu-id="da7a0-146">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da7a0-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="da7a0-147">Header</span></span><br/>  | <dl> <span data-ttu-id="da7a0-148"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="da7a0-148"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="da7a0-149">Libreria</span><span class="sxs-lookup"><span data-stu-id="da7a0-149">Library</span></span><br/> | <dl> <span data-ttu-id="da7a0-150"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="da7a0-150"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




