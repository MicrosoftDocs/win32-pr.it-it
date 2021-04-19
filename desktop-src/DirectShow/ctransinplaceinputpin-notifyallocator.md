---
description: 'Il metodo NotifyAllocator specifica un allocatore per la connessione. Questo metodo implementa il metodo IMemInputPin:: NotifyAllocator.'
ms.assetid: adc1c5b6-99da-4140-b644-7b98f6b8bad4
title: Metodo CTransInPlaceInputPin. NotifyAllocator (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 74578243ce780e09d7435f9dd4b70bd9497e1e97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326189"
---
# <a name="ctransinplaceinputpinnotifyallocator-method"></a><span data-ttu-id="31813-104">CTransInPlaceInputPin. NotifyAllocator, metodo</span><span class="sxs-lookup"><span data-stu-id="31813-104">CTransInPlaceInputPin.NotifyAllocator method</span></span>

<span data-ttu-id="31813-105">Il `NotifyAllocator` metodo specifica un allocatore per la connessione.</span><span class="sxs-lookup"><span data-stu-id="31813-105">The `NotifyAllocator` method specifies an allocator for the connection.</span></span> <span data-ttu-id="31813-106">Questo metodo implementa il metodo [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) .</span><span class="sxs-lookup"><span data-stu-id="31813-106">This method implements the [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="31813-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="31813-107">Syntax</span></span>


```C++
HRESULT NotifyAllocator(
   IMemAllocator *pAllocator,
   BOOL          bReadOnly
);
```



## <a name="parameters"></a><span data-ttu-id="31813-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="31813-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31813-109">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="31813-109">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="31813-110">Puntatore all'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="31813-110">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="31813-111">*bReadOnly*</span><span class="sxs-lookup"><span data-stu-id="31813-111">*bReadOnly*</span></span> 
</dt> <dd>

<span data-ttu-id="31813-112">Flag che specifica se gli esempi di questo allocatore sono di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="31813-112">Flag that specifies whether samples from this allocator are read-only.</span></span> <span data-ttu-id="31813-113">Se **true**, gli esempi sono di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="31813-113">If **TRUE**, samples are read-only.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31813-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="31813-114">Return value</span></span>

<span data-ttu-id="31813-115">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="31813-115">Returns an **HRESULT** value.</span></span> <span data-ttu-id="31813-116">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="31813-116">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="31813-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="31813-117">Return code</span></span>                                                                               | <span data-ttu-id="31813-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31813-118">Description</span></span>                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="31813-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="31813-119"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="31813-120">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="31813-120">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="31813-121"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="31813-121"><dt>**E\_FAIL**</dt></span></span> </dl>    | <span data-ttu-id="31813-122">Errore</span><span class="sxs-lookup"><span data-stu-id="31813-122">Failure</span></span><br/>                   |
| <dl> <span data-ttu-id="31813-123"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="31813-123"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="31813-124">Argomento puntatore **null**</span><span class="sxs-lookup"><span data-stu-id="31813-124">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="31813-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="31813-125">Remarks</span></span>

<span data-ttu-id="31813-126">Il filtro tenta di utilizzare lo stesso allocatore per entrambe le connessioni pin.</span><span class="sxs-lookup"><span data-stu-id="31813-126">The filter attempts to use the same allocator for both pin connections.</span></span>

-   <span data-ttu-id="31813-127">Se il pin di output non è connesso, il pin di input accetta automaticamente l'allocatore.</span><span class="sxs-lookup"><span data-stu-id="31813-127">If the output pin is not connected, the input pin automatically accepts the allocator.</span></span> <span data-ttu-id="31813-128">Quando il pin di output è connesso, il filtro riconnetterà il pin di input.</span><span class="sxs-lookup"><span data-stu-id="31813-128">When the output pin is connected, the filter will reconnect the input pin.</span></span> <span data-ttu-id="31813-129">A questo punto, il filtro proverà a usare un solo allocatore.</span><span class="sxs-lookup"><span data-stu-id="31813-129">At that point, the filter will try again to use a single allocator.</span></span>
-   <span data-ttu-id="31813-130">Se il pin di output è connesso, il pin di input accetta l'allocatore.</span><span class="sxs-lookup"><span data-stu-id="31813-130">If the output pin is connected, the input pin accepts the allocator.</span></span> <span data-ttu-id="31813-131">Il pin di output usa anche lo stesso allocatore.</span><span class="sxs-lookup"><span data-stu-id="31813-131">The output pin also uses the same allocator.</span></span> <span data-ttu-id="31813-132">Chiama `NotifyAllocator` sul pin di input downstream.</span><span class="sxs-lookup"><span data-stu-id="31813-132">It calls `NotifyAllocator` on the downstream input pin.</span></span>

<span data-ttu-id="31813-133">Il caso precedente presenta la seguente eccezione:</span><span class="sxs-lookup"><span data-stu-id="31813-133">The previous case has the following exception:</span></span>

-   <span data-ttu-id="31813-134">Se l'allocatore proposto è di sola lettura (ovvero il parametro *bReadOnly* è **true**) e il filtro deve modificare gli esempi, il filtro deve usare due allocatori diversi.</span><span class="sxs-lookup"><span data-stu-id="31813-134">If the proposed allocator is read-only (that is, the *bReadOnly* parameter is **TRUE**) and the filter needs to modify the samples, then the filter must use two different allocators.</span></span> <span data-ttu-id="31813-135">In questo caso, se il filtro upstream sta proponendo di usare l'allocatore del filtro downstream, il metodo restituisce E ha \_ esito negativo.</span><span class="sxs-lookup"><span data-stu-id="31813-135">In this case, if the upstream filter is proposing to use the downstream filter's allocator, the method returns E\_FAIL.</span></span>

## <a name="requirements"></a><span data-ttu-id="31813-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31813-136">Requirements</span></span>



| <span data-ttu-id="31813-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="31813-137">Requirement</span></span> | <span data-ttu-id="31813-138">Valore</span><span class="sxs-lookup"><span data-stu-id="31813-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31813-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="31813-139">Header</span></span><br/>  | <dl> <span data-ttu-id="31813-140"><dt>Transip. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="31813-140"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="31813-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="31813-141">Library</span></span><br/> | <dl> <span data-ttu-id="31813-142"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="31813-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31813-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="31813-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31813-144">**Classe CTransInPlaceInputPin**</span><span class="sxs-lookup"><span data-stu-id="31813-144">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




