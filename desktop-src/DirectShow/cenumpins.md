---
description: La classe CEnumPins implementa un enumeratore per i pin.
ms.assetid: 8729f294-c76d-404f-9f51-7565470eced8
title: Classe CEnumPins (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dde02c31ed0ef72e6df36a6cf0364b7f184304e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329832"
---
# <a name="cenumpins-class"></a><span data-ttu-id="1f085-103">Classe CEnumPins</span><span class="sxs-lookup"><span data-stu-id="1f085-103">CEnumPins class</span></span>

![gerarchia di classi cenumpins](images/filter03.png)

<span data-ttu-id="1f085-105">La `CEnumPins` classe implementa un enumeratore per i pin.</span><span class="sxs-lookup"><span data-stu-id="1f085-105">The `CEnumPins` class implements an enumerator for pins.</span></span>

<span data-ttu-id="1f085-106">Questa classe implementa l'interfaccia [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) .</span><span class="sxs-lookup"><span data-stu-id="1f085-106">This class implements the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface.</span></span> <span data-ttu-id="1f085-107">Chiama i metodi [**CBaseFilter**](cbasefilter.md) seguenti:</span><span class="sxs-lookup"><span data-stu-id="1f085-107">It calls the following [**CBaseFilter**](cbasefilter.md) methods:</span></span>

-   <span data-ttu-id="1f085-108">[**CBaseFilter:: GetPin**](cbasefilter-getpin.md): Recupera un pin sul filtro, a cui fa riferimento un indice in base zero.</span><span class="sxs-lookup"><span data-stu-id="1f085-108">[**CBaseFilter::GetPin**](cbasefilter-getpin.md): Retrieves a pin on the filter, referenced by a zero-based index.</span></span>
-   <span data-ttu-id="1f085-109">[**CBaseFilter:: GetPinCount**](cbasefilter-getpincount.md): Recupera il numero totale di pin sul filtro.</span><span class="sxs-lookup"><span data-stu-id="1f085-109">[**CBaseFilter::GetPinCount**](cbasefilter-getpincount.md): Retrieves the total number of pins on the filter.</span></span>
-   <span data-ttu-id="1f085-110">[**CBaseFilter:: GetPinVersion**](cbasefilter-getpinversion.md): determina se i pin sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="1f085-110">[**CBaseFilter::GetPinVersion**](cbasefilter-getpinversion.md): Determines whether the pins have changed.</span></span>

<span data-ttu-id="1f085-111">Se il filtro crea o Elimina in modo dinamico i pin, incrementa la versione del PIN ogni volta che i pin cambiano.</span><span class="sxs-lookup"><span data-stu-id="1f085-111">If the filter dynamically creates or destroys pins, it increments the pin version whenever the pins change.</span></span> <span data-ttu-id="1f085-112">Se il numero di versione viene modificato, l'oggetto enumeratore non viene più sincronizzato con il filtro.</span><span class="sxs-lookup"><span data-stu-id="1f085-112">If the version number changes, the enumerator object is no longer synchronized with the filter.</span></span> <span data-ttu-id="1f085-113">Una volta che l'enumeratore non è sincronizzato, i metodi in `CEnumPins` restituiscono la \_ \_ sincronizzazione di VFW E enum \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1f085-113">Once the enumerator is out of sync, the methods in `CEnumPins` return VFW\_E\_ENUM\_OUT\_OF\_SYNC.</span></span> <span data-ttu-id="1f085-114">Chiamare il metodo [**CEnumPins:: Reset**](cenumpins-reset.md) per risincronizzare l'enumeratore.</span><span class="sxs-lookup"><span data-stu-id="1f085-114">Call the [**CEnumPins::Reset**](cenumpins-reset.md) method to resynchronize the enumerator.</span></span>



| <span data-ttu-id="1f085-115">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="1f085-115">Public Methods</span></span>                             | <span data-ttu-id="1f085-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f085-116">Description</span></span>                                                     |
|--------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="1f085-117">**CEnumPins**</span><span class="sxs-lookup"><span data-stu-id="1f085-117">**CEnumPins**</span></span>](cenumpins-cenumpins.md)   | <span data-ttu-id="1f085-118">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="1f085-118">Constructor method.</span></span>                                             |
| [<span data-ttu-id="1f085-119">**~ CEnumPins**</span><span class="sxs-lookup"><span data-stu-id="1f085-119">**~CEnumPins**</span></span>](cenumpins--cenumpins.md) | <span data-ttu-id="1f085-120">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="1f085-120">Destructor method.</span></span> <span data-ttu-id="1f085-121">Virtuale.</span><span class="sxs-lookup"><span data-stu-id="1f085-121">Virtual.</span></span>                                     |
| <span data-ttu-id="1f085-122">Metodi IEnumPins</span><span class="sxs-lookup"><span data-stu-id="1f085-122">IEnumPins Methods</span></span>                          | <span data-ttu-id="1f085-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f085-123">Description</span></span>                                                     |
| [<span data-ttu-id="1f085-124">**Clone**</span><span class="sxs-lookup"><span data-stu-id="1f085-124">**Clone**</span></span>](cenumpins-clone.md)           | <span data-ttu-id="1f085-125">Crea una copia dell'enumeratore con lo stesso stato di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="1f085-125">Makes a copy of the enumerator with the same enumeration state.</span></span> |
| [<span data-ttu-id="1f085-126">**Avanti**</span><span class="sxs-lookup"><span data-stu-id="1f085-126">**Next**</span></span>](cenumpins-next.md)             | <span data-ttu-id="1f085-127">Recupera un numero specificato di pin.</span><span class="sxs-lookup"><span data-stu-id="1f085-127">Retrieves a specified number of pins.</span></span>                           |
| [<span data-ttu-id="1f085-128">**Reset**</span><span class="sxs-lookup"><span data-stu-id="1f085-128">**Reset**</span></span>](cenumpins-reset.md)           | <span data-ttu-id="1f085-129">Riporta all'inizio la sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="1f085-129">Resets the enumeration sequence to the beginning.</span></span>               |
| [<span data-ttu-id="1f085-130">**Ignora**</span><span class="sxs-lookup"><span data-stu-id="1f085-130">**Skip**</span></span>](cenumpins-skip.md)             | <span data-ttu-id="1f085-131">Ignora un numero specificato di pin.</span><span class="sxs-lookup"><span data-stu-id="1f085-131">Skips over a specified number of pins.</span></span>                          |



 

## <a name="requirements"></a><span data-ttu-id="1f085-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f085-132">Requirements</span></span>



| <span data-ttu-id="1f085-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f085-133">Requirement</span></span> | <span data-ttu-id="1f085-134">Valore</span><span class="sxs-lookup"><span data-stu-id="1f085-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f085-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1f085-135">Header</span></span><br/>  | <dl> <span data-ttu-id="1f085-136"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1f085-136"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1f085-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="1f085-137">Library</span></span><br/> | <dl> <span data-ttu-id="1f085-138"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1f085-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




