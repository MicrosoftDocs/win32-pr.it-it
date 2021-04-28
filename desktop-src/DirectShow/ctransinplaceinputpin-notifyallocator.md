---
description: 'Metodo CTransInPlaceInputPin.NotifyAllocator : il metodo NotifyAllocator specifica un allocatore per la connessione. Questo metodo implementa il metodo IMemInputPin::NotifyAllocator.'
ms.assetid: adc1c5b6-99da-4140-b644-7b98f6b8bad4
title: Metodo CTransInPlaceInputPin.NotifyAllocator (Transip.h)
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
ms.openlocfilehash: ca15be5dc1893a393e6052832cc7522f27355eeb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094749"
---
# <a name="ctransinplaceinputpinnotifyallocator-method"></a><span data-ttu-id="efd66-104">Metodo CTransInPlaceInputPin.NotifyAllocator</span><span class="sxs-lookup"><span data-stu-id="efd66-104">CTransInPlaceInputPin.NotifyAllocator method</span></span>

<span data-ttu-id="efd66-105">Il `NotifyAllocator` metodo specifica un allocatore per la connessione.</span><span class="sxs-lookup"><span data-stu-id="efd66-105">The `NotifyAllocator` method specifies an allocator for the connection.</span></span> <span data-ttu-id="efd66-106">Questo metodo implementa il [**metodo IMemInputPin::NotifyAllocator.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator)</span><span class="sxs-lookup"><span data-stu-id="efd66-106">This method implements the [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="efd66-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="efd66-107">Syntax</span></span>


```C++
HRESULT NotifyAllocator(
   IMemAllocator *pAllocator,
   BOOL          bReadOnly
);
```



## <a name="parameters"></a><span data-ttu-id="efd66-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="efd66-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efd66-109">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="efd66-109">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="efd66-110">Puntatore all'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="efd66-110">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="efd66-111">*bReadOnly*</span><span class="sxs-lookup"><span data-stu-id="efd66-111">*bReadOnly*</span></span> 
</dt> <dd>

<span data-ttu-id="efd66-112">Flag che specifica se i campioni di questo allocatore sono di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="efd66-112">Flag that specifies whether samples from this allocator are read-only.</span></span> <span data-ttu-id="efd66-113">Se **TRUE,** gli esempi sono di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="efd66-113">If **TRUE**, samples are read-only.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efd66-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="efd66-114">Return value</span></span>

<span data-ttu-id="efd66-115">Restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="efd66-115">Returns an **HRESULT** value.</span></span> <span data-ttu-id="efd66-116">I valori possibili includono quelli illustrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="efd66-116">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="efd66-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="efd66-117">Return code</span></span>                                                                               | <span data-ttu-id="efd66-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="efd66-118">Description</span></span>                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="efd66-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="efd66-119"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="efd66-120">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="efd66-120">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="efd66-121"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="efd66-121"><dt>**E\_FAIL**</dt></span></span> </dl>    | <span data-ttu-id="efd66-122">Operazioni non riuscite</span><span class="sxs-lookup"><span data-stu-id="efd66-122">Failure</span></span><br/>                   |
| <dl> <span data-ttu-id="efd66-123"><dt>**PUNTATORE \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="efd66-123"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="efd66-124">**Argomento puntatore NULL**</span><span class="sxs-lookup"><span data-stu-id="efd66-124">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="efd66-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="efd66-125">Remarks</span></span>

<span data-ttu-id="efd66-126">Il filtro tenta di usare lo stesso allocatore per entrambe le connessioni pin.</span><span class="sxs-lookup"><span data-stu-id="efd66-126">The filter attempts to use the same allocator for both pin connections.</span></span>

-   <span data-ttu-id="efd66-127">Se il pin di output non è connesso, il pin di input accetta automaticamente l'allocatore.</span><span class="sxs-lookup"><span data-stu-id="efd66-127">If the output pin is not connected, the input pin automatically accepts the allocator.</span></span> <span data-ttu-id="efd66-128">Quando il pin di output è connesso, il filtro riconnetterà il pin di input.</span><span class="sxs-lookup"><span data-stu-id="efd66-128">When the output pin is connected, the filter will reconnect the input pin.</span></span> <span data-ttu-id="efd66-129">A questo punto, il filtro tenterà di nuovo di usare un singolo allocatore.</span><span class="sxs-lookup"><span data-stu-id="efd66-129">At that point, the filter will try again to use a single allocator.</span></span>
-   <span data-ttu-id="efd66-130">Se il pin di output è connesso, il pin di input accetta l'allocatore.</span><span class="sxs-lookup"><span data-stu-id="efd66-130">If the output pin is connected, the input pin accepts the allocator.</span></span> <span data-ttu-id="efd66-131">Il pin di output usa anche lo stesso allocatore.</span><span class="sxs-lookup"><span data-stu-id="efd66-131">The output pin also uses the same allocator.</span></span> <span data-ttu-id="efd66-132">Chiama sul `NotifyAllocator` pin di input downstream.</span><span class="sxs-lookup"><span data-stu-id="efd66-132">It calls `NotifyAllocator` on the downstream input pin.</span></span>

<span data-ttu-id="efd66-133">Il caso precedente presenta l'eccezione seguente:</span><span class="sxs-lookup"><span data-stu-id="efd66-133">The previous case has the following exception:</span></span>

-   <span data-ttu-id="efd66-134">Se l'allocatore proposto è di sola lettura, ovvero il parametro *bReadOnly* è **TRUE** e il filtro deve modificare gli esempi, il filtro deve usare due allocatori diversi.</span><span class="sxs-lookup"><span data-stu-id="efd66-134">If the proposed allocator is read-only (that is, the *bReadOnly* parameter is **TRUE**) and the filter needs to modify the samples, then the filter must use two different allocators.</span></span> <span data-ttu-id="efd66-135">In questo caso, se il filtro upstream propone di usare l'allocatore del filtro downstream, il metodo restituisce E \_ FAIL.</span><span class="sxs-lookup"><span data-stu-id="efd66-135">In this case, if the upstream filter is proposing to use the downstream filter's allocator, the method returns E\_FAIL.</span></span>

## <a name="requirements"></a><span data-ttu-id="efd66-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="efd66-136">Requirements</span></span>



| <span data-ttu-id="efd66-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="efd66-137">Requirement</span></span> | <span data-ttu-id="efd66-138">Valore</span><span class="sxs-lookup"><span data-stu-id="efd66-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efd66-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="efd66-139">Header</span></span><br/>  | <dl> <span data-ttu-id="efd66-140"><dt>Transip.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="efd66-140"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="efd66-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="efd66-141">Library</span></span><br/> | <dl> <span data-ttu-id="efd66-142"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="efd66-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efd66-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="efd66-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efd66-144">**Classe CTransInPlaceInputPin**</span><span class="sxs-lookup"><span data-stu-id="efd66-144">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




