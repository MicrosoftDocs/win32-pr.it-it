---
description: 'Il metodo GetBuffer recupera un esempio di supporto che contiene un buffer. Questo metodo implementa il metodo IMemAllocator:: GetBuffer.'
ms.assetid: 81694b9c-b325-47c8-94e4-f54d1329a684
title: Metodo CBaseAllocator. GetBuffer (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f965885d4a7a12e09c8875f71032ce2fded61bd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331814"
---
# <a name="cbaseallocatorgetbuffer-method"></a><span data-ttu-id="92475-104">CBaseAllocator. GetBuffer, metodo</span><span class="sxs-lookup"><span data-stu-id="92475-104">CBaseAllocator.GetBuffer method</span></span>

<span data-ttu-id="92475-105">Il `GetBuffer` metodo recupera un esempio di supporto che contiene un buffer.</span><span class="sxs-lookup"><span data-stu-id="92475-105">The `GetBuffer` method retrieves a media sample that contains a buffer.</span></span> <span data-ttu-id="92475-106">Questo metodo implementa il metodo [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) .</span><span class="sxs-lookup"><span data-stu-id="92475-106">This method implements the [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="92475-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="92475-107">Syntax</span></span>


```C++
HRESULT GetBuffer(
   IMediaSample   **ppBuffer,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime,
   DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="92475-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="92475-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92475-109">*ppBuffer*</span><span class="sxs-lookup"><span data-stu-id="92475-109">*ppBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="92475-110">Riceve un puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del buffer.</span><span class="sxs-lookup"><span data-stu-id="92475-110">Receives a pointer to the buffer's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span> <span data-ttu-id="92475-111">Il chiamante deve rilasciare l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="92475-111">The caller must release the interface.</span></span>

</dd> <dt>

<span data-ttu-id="92475-112">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="92475-112">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="92475-113">Puntatore all'ora di inizio dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="92475-113">Pointer to the start time of the sample.</span></span>

</dd> <dt>

<span data-ttu-id="92475-114">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="92475-114">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="92475-115">Puntatore all'ora di fine dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="92475-115">Pointer to the end time of the sample.</span></span>

</dd> <dt>

<span data-ttu-id="92475-116">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="92475-116">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="92475-117">Combinazione bit per bit di zero o più flag.</span><span class="sxs-lookup"><span data-stu-id="92475-117">Bitwise combination of zero or more flags.</span></span> <span data-ttu-id="92475-118">La classe base supporta il flag seguente.</span><span class="sxs-lookup"><span data-stu-id="92475-118">The base class supports the following flag.</span></span>



| <span data-ttu-id="92475-119">Valore</span><span class="sxs-lookup"><span data-stu-id="92475-119">Value</span></span>                                                                                                                                                          | <span data-ttu-id="92475-120">Significato</span><span class="sxs-lookup"><span data-stu-id="92475-120">Meaning</span></span>                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="AM_GBF_NOWAIT"></span><span id="am_gbf_nowait"></span><dl> <span data-ttu-id="92475-121"><dt>**AM \_ GBF \_ nowait**</dt></span><span class="sxs-lookup"><span data-stu-id="92475-121"><dt>**AM\_GBF\_NOWAIT**</dt></span></span> </dl> | <span data-ttu-id="92475-122">Non attendere che un buffer diventi disponibile.</span><span class="sxs-lookup"><span data-stu-id="92475-122">Do not wait for a buffer to become available.</span></span> <br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92475-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="92475-123">Return value</span></span>

<span data-ttu-id="92475-124">Restituisce uno dei seguenti valori **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="92475-124">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="92475-125">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="92475-125">Return code</span></span>                                                                                           | <span data-ttu-id="92475-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="92475-126">Description</span></span>                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="92475-127"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="92475-127"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="92475-128">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="92475-128">Success.</span></span><br/>                     |
| <dl> <span data-ttu-id="92475-129"><dt>**non è stato \_ \_ eseguito il \_ commit di VFW E**</dt></span><span class="sxs-lookup"><span data-stu-id="92475-129"><dt>**VFW\_E\_NOT\_COMMITTED**</dt></span></span> </dl> | <span data-ttu-id="92475-130">Non è stato eseguito il commit dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="92475-130">Allocator was not committed.</span></span><br/> |
| <dl> <span data-ttu-id="92475-131"><dt>**TIMEOUT di VFW \_ E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="92475-131"><dt>**VFW\_E\_TIMEOUT**</dt></span></span> </dl>        | <span data-ttu-id="92475-132">Timeout.</span><span class="sxs-lookup"><span data-stu-id="92475-132">Timed out.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="92475-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="92475-133">Remarks</span></span>

<span data-ttu-id="92475-134">A meno che il chiamante non specifichi il flag **\_ GBF \_ nowait** in *dwFlags*, questo metodo si blocca fino a quando non è disponibile l'esempio successivo.</span><span class="sxs-lookup"><span data-stu-id="92475-134">Unless the caller specifies the **AM\_GBF\_NOWAIT** flag in *dwFlags*, this method blocks until the next sample is available.</span></span>

<span data-ttu-id="92475-135">L'esempio di supporto recuperato ha un puntatore valido al buffer allocato.</span><span class="sxs-lookup"><span data-stu-id="92475-135">The retrieved media sample has a valid pointer to the allocated buffer.</span></span> <span data-ttu-id="92475-136">Il chiamante è responsabile dell'impostazione di qualsiasi altra proprietà nell'esempio, ad esempio i timestamp, i tempi dei supporti o la proprietà del punto di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="92475-136">The caller is responsible for setting any other properties on the sample, such as the time stamps, the media times, or the sync-point property.</span></span> <span data-ttu-id="92475-137">Per ulteriori informazioni, vedere [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample).</span><span class="sxs-lookup"><span data-stu-id="92475-137">For more information, see [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample).</span></span>

<span data-ttu-id="92475-138">Nella classe di base, i parametri *pStartTime* e *pEndTime* vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="92475-138">In the base class, the *pStartTime* and *pEndTime* parameters are ignored.</span></span> <span data-ttu-id="92475-139">Le classi derivate possono usare questi valori.</span><span class="sxs-lookup"><span data-stu-id="92475-139">Derived classes can use these values.</span></span> <span data-ttu-id="92475-140">Ad esempio, l'allocatore per il filtro [renderer video](video-renderer-filter.md) utilizza questi valori per sincronizzare il cambio tra superfici di DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="92475-140">For example, the allocator for the [Video Renderer](video-renderer-filter.md) filter uses these values to synchronize switching between DirectDraw surfaces.</span></span>

<span data-ttu-id="92475-141">Se il metodo deve attendere un campione, incrementa il numero di oggetti in attesa ([**CBaseAllocator:: m \_ lCount**](cbaseallocator-m-lcount.md)) e chiama [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) Function sul semaforo ([**CBaseAllocator:: m \_ hSem**](cbaseallocator-m-hsem.md)).</span><span class="sxs-lookup"><span data-stu-id="92475-141">If the method needs to wait on a sample, it increments the count of waiting objects ([**CBaseAllocator::m\_lCount**](cbaseallocator-m-lcount.md)) and the calls [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) function on the semaphore ([**CBaseAllocator::m\_hSem**](cbaseallocator-m-hsem.md)).</span></span> <span data-ttu-id="92475-142">Quando un campione diventa disponibile, viene chiamato il metodo [**CBaseAllocator:: ReleaseBuffer**](cbaseallocator-releasebuffer.md) sull'allocatore, che aumenta il numero di semafori per **m \_ lCount** (rilasciando quindi i thread in attesa) e imposta **m \_ lCount** su zero.</span><span class="sxs-lookup"><span data-stu-id="92475-142">When a sample becomes available, it calls the [**CBaseAllocator::ReleaseBuffer**](cbaseallocator-releasebuffer.md) method on the allocator, which increases the semaphore count by **m\_lCount** (thereby releasing the waiting threads) and sets **m\_lCount** back to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="92475-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="92475-143">Requirements</span></span>



| <span data-ttu-id="92475-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="92475-144">Requirement</span></span> | <span data-ttu-id="92475-145">Valore</span><span class="sxs-lookup"><span data-stu-id="92475-145">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92475-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="92475-146">Header</span></span><br/>  | <dl> <span data-ttu-id="92475-147"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="92475-147"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="92475-148">Libreria</span><span class="sxs-lookup"><span data-stu-id="92475-148">Library</span></span><br/> | <dl> <span data-ttu-id="92475-149"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="92475-149"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92475-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="92475-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92475-151">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="92475-151">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

