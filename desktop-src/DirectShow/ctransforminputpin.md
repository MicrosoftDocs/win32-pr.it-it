---
description: La classe CTransformInputPin implementa un pin di input usato dalla classe CTransformFilter.
ms.assetid: 032da1bb-448d-48ea-ab3d-f721d790637f
title: Classe CTransformInputPin (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6cbfad0a33384249ab474d6376ffc110294bca6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333309"
---
# <a name="ctransforminputpin-class"></a><span data-ttu-id="f1699-103">Classe CTransformInputPin</span><span class="sxs-lookup"><span data-stu-id="f1699-103">CTransformInputPin class</span></span>

![gerarchia di classi ctransforminputpin](images/tfrm01.png)

<span data-ttu-id="f1699-105">La `CTransformInputPin` classe implementa un pin di input usato dalla classe [**CTransformFilter**](ctransformfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="f1699-105">The `CTransformInputPin` class implements an input pin that is used by the [**CTransformFilter**](ctransformfilter.md) class.</span></span>

<span data-ttu-id="f1699-106">In genere, non è necessario derivare da questa classe.</span><span class="sxs-lookup"><span data-stu-id="f1699-106">Typically, you do not need to derive from this class.</span></span> <span data-ttu-id="f1699-107">La maggior parte dei metodi di questa classe chiama i metodi corrispondenti sulla classe **CTransformFilter** , che è possibile sottoscrivere.</span><span class="sxs-lookup"><span data-stu-id="f1699-107">Most of the methods in this class call corresponding methods on the **CTransformFilter** class, which you can override.</span></span> <span data-ttu-id="f1699-108">Se si deriva da questa classe, è necessario eseguire l'override del metodo [**CTransformFilter:: GetPin**](ctransformfilter-getpin.md) del filtro per creare istanze della classe derivata.</span><span class="sxs-lookup"><span data-stu-id="f1699-108">If you derive from this class, you must override the filter's [**CTransformFilter::GetPin**](ctransformfilter-getpin.md) method to create instances of your derived class.</span></span>



| <span data-ttu-id="f1699-109">Variabili membro protette</span><span class="sxs-lookup"><span data-stu-id="f1699-109">Protected Member Variables</span></span>                                           | <span data-ttu-id="f1699-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1699-110">Description</span></span>                                                                            |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="f1699-111">**\_pTransformFilter m**</span><span class="sxs-lookup"><span data-stu-id="f1699-111">**m\_pTransformFilter**</span></span>](ctransforminputpin-m-ptransformfilter.md) | <span data-ttu-id="f1699-112">Puntatore al filtro proprietario.</span><span class="sxs-lookup"><span data-stu-id="f1699-112">Pointer to the owning filter.</span></span>                                                          |
| <span data-ttu-id="f1699-113">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="f1699-113">Public Methods</span></span>                                                       | <span data-ttu-id="f1699-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1699-114">Description</span></span>                                                                            |
| [<span data-ttu-id="f1699-115">**CTransformInputPin**</span><span class="sxs-lookup"><span data-stu-id="f1699-115">**CTransformInputPin**</span></span>](ctransforminputpin-ctransforminputpin.md)  | <span data-ttu-id="f1699-116">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="f1699-116">Constructor method.</span></span>                                                                    |
| [<span data-ttu-id="f1699-117">**CheckConnect**</span><span class="sxs-lookup"><span data-stu-id="f1699-117">**CheckConnect**</span></span>](ctransforminputpin-checkconnect.md)              | <span data-ttu-id="f1699-118">Determina se una connessione pin è adatta.</span><span class="sxs-lookup"><span data-stu-id="f1699-118">Determines whether a pin connection is suitable.</span></span>                                       |
| [<span data-ttu-id="f1699-119">**BreakConnect**</span><span class="sxs-lookup"><span data-stu-id="f1699-119">**BreakConnect**</span></span>](ctransforminputpin-breakconnect.md)              | <span data-ttu-id="f1699-120">Rilascia il pin da una connessione.</span><span class="sxs-lookup"><span data-stu-id="f1699-120">Releases the pin from a connection.</span></span>                                                    |
| [<span data-ttu-id="f1699-121">**CompleteConnect**</span><span class="sxs-lookup"><span data-stu-id="f1699-121">**CompleteConnect**</span></span>](ctransforminputpin-completeconnect.md)        | <span data-ttu-id="f1699-122">Completa una connessione a un altro pin.</span><span class="sxs-lookup"><span data-stu-id="f1699-122">Completes a connection to another pin.</span></span>                                                 |
| [<span data-ttu-id="f1699-123">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="f1699-123">**CheckMediaType**</span></span>](ctransforminputpin-checkmediatype.md)          | <span data-ttu-id="f1699-124">Determina se il pin accetta un tipo di supporto specifico.</span><span class="sxs-lookup"><span data-stu-id="f1699-124">Determines if the pin accepts a specific media type.</span></span>                                   |
| [<span data-ttu-id="f1699-125">**SetMediaType**</span><span class="sxs-lookup"><span data-stu-id="f1699-125">**SetMediaType**</span></span>](ctransforminputpin-setmediatype.md)              | <span data-ttu-id="f1699-126">Imposta il tipo di supporto per la connessione.</span><span class="sxs-lookup"><span data-stu-id="f1699-126">Sets the media type for the connection.</span></span>                                                |
| [<span data-ttu-id="f1699-127">**CheckStreaming**</span><span class="sxs-lookup"><span data-stu-id="f1699-127">**CheckStreaming**</span></span>](ctransforminputpin-checkstreaming.md)          | <span data-ttu-id="f1699-128">Determina se il pin può accettare esempi.</span><span class="sxs-lookup"><span data-stu-id="f1699-128">Determines whether the pin can accept samples.</span></span> <span data-ttu-id="f1699-129">Virtuale.</span><span class="sxs-lookup"><span data-stu-id="f1699-129">Virtual.</span></span>                                |
| [<span data-ttu-id="f1699-130">**CurrentMediaType**</span><span class="sxs-lookup"><span data-stu-id="f1699-130">**CurrentMediaType**</span></span>](ctransforminputpin-currentmediatype.md)      | <span data-ttu-id="f1699-131">Recupera il tipo di supporto per la connessione al pin corrente.</span><span class="sxs-lookup"><span data-stu-id="f1699-131">Retrieves the media type for the current pin connection.</span></span>                               |
| <span data-ttu-id="f1699-132">Metodi IPin</span><span class="sxs-lookup"><span data-stu-id="f1699-132">IPin Methods</span></span>                                                         | <span data-ttu-id="f1699-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1699-133">Description</span></span>                                                                            |
| [<span data-ttu-id="f1699-134">**QueryId**</span><span class="sxs-lookup"><span data-stu-id="f1699-134">**QueryId**</span></span>](ctransforminputpin-queryid.md)                        | <span data-ttu-id="f1699-135">Recupera un identificatore per il PIN.</span><span class="sxs-lookup"><span data-stu-id="f1699-135">Retrieves an identifier for the pin.</span></span>                                                   |
| [<span data-ttu-id="f1699-136">**EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="f1699-136">**EndOfStream**</span></span>](ctransforminputpin-endofstream.md)                | <span data-ttu-id="f1699-137">Notifica al pin che non sono previsti dati aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="f1699-137">Notifies the pin that no additional data is expected.</span></span>                                  |
| [<span data-ttu-id="f1699-138">**BeginFlush**</span><span class="sxs-lookup"><span data-stu-id="f1699-138">**BeginFlush**</span></span>](ctransforminputpin-beginflush.md)                  | <span data-ttu-id="f1699-139">Avvia un'operazione di svuotamento.</span><span class="sxs-lookup"><span data-stu-id="f1699-139">Begins a flush operation.</span></span>                                                              |
| [<span data-ttu-id="f1699-140">**EndFlush**</span><span class="sxs-lookup"><span data-stu-id="f1699-140">**EndFlush**</span></span>](ctransforminputpin-endflush.md)                      | <span data-ttu-id="f1699-141">Termina un'operazione di svuotamento.</span><span class="sxs-lookup"><span data-stu-id="f1699-141">Ends a flush operation.</span></span>                                                                |
| [<span data-ttu-id="f1699-142">**NewSegment**</span><span class="sxs-lookup"><span data-stu-id="f1699-142">**NewSegment**</span></span>](ctransforminputpin-newsegment.md)                  | <span data-ttu-id="f1699-143">Notifica al pin che gli esempi di supporti ricevuti dopo questa chiamata vengono raggruppati come segmento.</span><span class="sxs-lookup"><span data-stu-id="f1699-143">Notifies the pin that media samples received after this call are grouped as a segment.</span></span> |
| <span data-ttu-id="f1699-144">Metodi IMemInputPin</span><span class="sxs-lookup"><span data-stu-id="f1699-144">IMemInputPin Methods</span></span>                                                 | <span data-ttu-id="f1699-145">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1699-145">Description</span></span>                                                                            |
| [<span data-ttu-id="f1699-146">**Ricevere**</span><span class="sxs-lookup"><span data-stu-id="f1699-146">**Receive**</span></span>](ctransforminputpin-receive.md)                        | <span data-ttu-id="f1699-147">Riceve il campione multimediale successivo nel flusso.</span><span class="sxs-lookup"><span data-stu-id="f1699-147">Receives the next media sample in the stream.</span></span>                                          |



 

## <a name="requirements"></a><span data-ttu-id="f1699-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1699-148">Requirements</span></span>



| <span data-ttu-id="f1699-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1699-149">Requirement</span></span> | <span data-ttu-id="f1699-150">Valore</span><span class="sxs-lookup"><span data-stu-id="f1699-150">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1699-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f1699-151">Header</span></span><br/>  | <dl> <span data-ttu-id="f1699-152"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1699-152"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f1699-153">Libreria</span><span class="sxs-lookup"><span data-stu-id="f1699-153">Library</span></span><br/> | <dl> <span data-ttu-id="f1699-154"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f1699-154"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




