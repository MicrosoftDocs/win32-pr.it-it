---
description: La classe CTransformOutputPin implementa un pin di output usato dalla classe CTransformFilter.
ms.assetid: 76f9a981-8f0d-45d4-b901-c5ec5b5ac9ee
title: Classe CTransformOutputPin (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c55c57fbec0a8441b80398370542d94b2b70c1ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332985"
---
# <a name="ctransformoutputpin-class"></a><span data-ttu-id="cf36b-103">Classe CTransformOutputPin</span><span class="sxs-lookup"><span data-stu-id="cf36b-103">CTransformOutputPin class</span></span>

![gerarchia di classi ctransformoutputpin](images/tfrm02.png)

<span data-ttu-id="cf36b-105">La `CTransformOutputPin` classe implementa un pin di output usato dalla classe [**CTransformFilter**](ctransformfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="cf36b-105">The `CTransformOutputPin` class implements an output pin that is used by the [**CTransformFilter**](ctransformfilter.md) class.</span></span>

<span data-ttu-id="cf36b-106">In genere, non è necessario derivare da questa classe.</span><span class="sxs-lookup"><span data-stu-id="cf36b-106">Typically, you do not need to derive from this class.</span></span> <span data-ttu-id="cf36b-107">La maggior parte dei metodi di questa classe chiama i metodi corrispondenti sulla classe **CTransformFilter** , che è possibile sottoscrivere.</span><span class="sxs-lookup"><span data-stu-id="cf36b-107">Most of the methods in this class call corresponding methods on the **CTransformFilter** class, which you can override.</span></span> <span data-ttu-id="cf36b-108">Se si deriva da questa classe, è necessario eseguire l'override del metodo [**CTransformFilter:: GetPin**](ctransformfilter-getpin.md) del filtro per creare istanze della classe derivata.</span><span class="sxs-lookup"><span data-stu-id="cf36b-108">If you derive from this class, you must override the filter's [**CTransformFilter::GetPin**](ctransformfilter-getpin.md) method to create instances of your derived class.</span></span>

<span data-ttu-id="cf36b-109">Questa classe espone le interfacce **IMediaSeeking** e **IMediaPosition** tramite l'oggetto [**CPosPassThru**](cpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="cf36b-109">This class exposes the **IMediaSeeking** and **IMediaPosition** interfaces through the [**CPosPassThru**](cpospassthru.md) object.</span></span> <span data-ttu-id="cf36b-110">Passa tutte le richieste Seek al filtro successivo upstream.</span><span class="sxs-lookup"><span data-stu-id="cf36b-110">It passes all seek requests to the next filter upstream.</span></span>



| <span data-ttu-id="cf36b-111">Variabili membro protette</span><span class="sxs-lookup"><span data-stu-id="cf36b-111">Protected Member Variables</span></span>                                               | <span data-ttu-id="cf36b-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf36b-112">Description</span></span>                                              |
|--------------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="cf36b-113">**\_pTransformFilter m**</span><span class="sxs-lookup"><span data-stu-id="cf36b-113">**m\_pTransformFilter**</span></span>](ctransformoutputpin-m-ptransformfilter.md)    | <span data-ttu-id="cf36b-114">Puntatore al filtro proprietario.</span><span class="sxs-lookup"><span data-stu-id="cf36b-114">Pointer to the owning filter.</span></span>                            |
| <span data-ttu-id="cf36b-115">Variabili membro pubblico</span><span class="sxs-lookup"><span data-stu-id="cf36b-115">Public Member Variables</span></span>                                                  | <span data-ttu-id="cf36b-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf36b-116">Description</span></span>                                              |
| [<span data-ttu-id="cf36b-117">**\_pPosition m**</span><span class="sxs-lookup"><span data-stu-id="cf36b-117">**m\_pPosition**</span></span>](ctransformoutputpin-m-pposition.md)                  | <span data-ttu-id="cf36b-118">Oggetto helper per passare i comandi Seek upstream.</span><span class="sxs-lookup"><span data-stu-id="cf36b-118">Helper object to pass seek commands upstream.</span></span>            |
| <span data-ttu-id="cf36b-119">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="cf36b-119">Public Methods</span></span>                                                           | <span data-ttu-id="cf36b-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf36b-120">Description</span></span>                                              |
| [<span data-ttu-id="cf36b-121">**CTransformOutputPin**</span><span class="sxs-lookup"><span data-stu-id="cf36b-121">**CTransformOutputPin**</span></span>](ctransformoutputpin-ctransformoutputpin.md)   | <span data-ttu-id="cf36b-122">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="cf36b-122">Constructor method.</span></span>                                      |
| [<span data-ttu-id="cf36b-123">**~ CTransformOutputPin**</span><span class="sxs-lookup"><span data-stu-id="cf36b-123">**~CTransformOutputPin**</span></span>](ctransformoutputpin--ctransformoutputpin.md) | <span data-ttu-id="cf36b-124">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="cf36b-124">Destructor method.</span></span>                                       |
| [<span data-ttu-id="cf36b-125">**CheckConnect**</span><span class="sxs-lookup"><span data-stu-id="cf36b-125">**CheckConnect**</span></span>](ctransformoutputpin-checkconnect.md)                 | <span data-ttu-id="cf36b-126">Determina se una connessione pin è adatta.</span><span class="sxs-lookup"><span data-stu-id="cf36b-126">Determines whether a pin connection is suitable.</span></span>         |
| [<span data-ttu-id="cf36b-127">**BreakConnect**</span><span class="sxs-lookup"><span data-stu-id="cf36b-127">**BreakConnect**</span></span>](ctransformoutputpin-breakconnect.md)                 | <span data-ttu-id="cf36b-128">Rilascia il pin da una connessione.</span><span class="sxs-lookup"><span data-stu-id="cf36b-128">Releases the pin from a connection.</span></span>                      |
| [<span data-ttu-id="cf36b-129">**CompleteConnect**</span><span class="sxs-lookup"><span data-stu-id="cf36b-129">**CompleteConnect**</span></span>](ctransformoutputpin-completeconnect.md)           | <span data-ttu-id="cf36b-130">Completa una connessione a un altro pin.</span><span class="sxs-lookup"><span data-stu-id="cf36b-130">Completes a connection to another pin.</span></span>                   |
| [<span data-ttu-id="cf36b-131">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="cf36b-131">**CheckMediaType**</span></span>](ctransformoutputpin-checkmediatype.md)             | <span data-ttu-id="cf36b-132">Determina se il pin accetta un tipo di supporto specifico.</span><span class="sxs-lookup"><span data-stu-id="cf36b-132">Determines if the pin accepts a specific media type.</span></span>     |
| [<span data-ttu-id="cf36b-133">**SetMediaType**</span><span class="sxs-lookup"><span data-stu-id="cf36b-133">**SetMediaType**</span></span>](ctransformoutputpin-setmediatype.md)                 | <span data-ttu-id="cf36b-134">Imposta il tipo di supporto per la connessione.</span><span class="sxs-lookup"><span data-stu-id="cf36b-134">Sets the media type for the connection.</span></span>                  |
| [<span data-ttu-id="cf36b-135">**DecideBufferSize**</span><span class="sxs-lookup"><span data-stu-id="cf36b-135">**DecideBufferSize**</span></span>](ctransformoutputpin-decidebuffersize.md)         | <span data-ttu-id="cf36b-136">Imposta i requisiti del buffer.</span><span class="sxs-lookup"><span data-stu-id="cf36b-136">Sets the buffer requirements.</span></span>                            |
| [<span data-ttu-id="cf36b-137">**GetMediaType**</span><span class="sxs-lookup"><span data-stu-id="cf36b-137">**GetMediaType**</span></span>](ctransformoutputpin-getmediatype.md)                 | <span data-ttu-id="cf36b-138">Recupera un tipo di supporto preferito, in base al valore di indice.</span><span class="sxs-lookup"><span data-stu-id="cf36b-138">Retrieves a preferred media type, by index value.</span></span>        |
| [<span data-ttu-id="cf36b-139">**CurrentMediaType**</span><span class="sxs-lookup"><span data-stu-id="cf36b-139">**CurrentMediaType**</span></span>](ctransformoutputpin-currentmediatype.md)         | <span data-ttu-id="cf36b-140">Recupera il tipo di supporto per la connessione al pin corrente.</span><span class="sxs-lookup"><span data-stu-id="cf36b-140">Retrieves the media type for the current pin connection.</span></span> |
| <span data-ttu-id="cf36b-141">Metodi IPin</span><span class="sxs-lookup"><span data-stu-id="cf36b-141">IPin Methods</span></span>                                                             | <span data-ttu-id="cf36b-142">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf36b-142">Description</span></span>                                              |
| [<span data-ttu-id="cf36b-143">**QueryId**</span><span class="sxs-lookup"><span data-stu-id="cf36b-143">**QueryId**</span></span>](ctransformoutputpin-queryid.md)                           | <span data-ttu-id="cf36b-144">Recupera un identificatore per il PIN.</span><span class="sxs-lookup"><span data-stu-id="cf36b-144">Retrieves an identifier for the pin.</span></span>                     |
| <span data-ttu-id="cf36b-145">Metodi IQualityControl</span><span class="sxs-lookup"><span data-stu-id="cf36b-145">IQualityControl Methods</span></span>                                                  | <span data-ttu-id="cf36b-146">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf36b-146">Description</span></span>                                              |
| [<span data-ttu-id="cf36b-147">**Notifica**</span><span class="sxs-lookup"><span data-stu-id="cf36b-147">**Notify**</span></span>](ctransformoutputpin-notify.md)                             | <span data-ttu-id="cf36b-148">Notifica al pin che è richiesta una modifica di qualità.</span><span class="sxs-lookup"><span data-stu-id="cf36b-148">Notifies the pin that a quality change is requested.</span></span>     |



 

## <a name="requirements"></a><span data-ttu-id="cf36b-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cf36b-149">Requirements</span></span>



| <span data-ttu-id="cf36b-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf36b-150">Requirement</span></span> | <span data-ttu-id="cf36b-151">Valore</span><span class="sxs-lookup"><span data-stu-id="cf36b-151">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf36b-152">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cf36b-152">Header</span></span><br/>  | <dl> <span data-ttu-id="cf36b-153"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cf36b-153"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cf36b-154">Libreria</span><span class="sxs-lookup"><span data-stu-id="cf36b-154">Library</span></span><br/> | <dl> <span data-ttu-id="cf36b-155"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cf36b-155"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




