---
description: 'Il metodo seproperties specifica il numero di buffer da allocare e le dimensioni di ogni buffer. Questo metodo implementa il metodo IMemAllocator:: SetValue.'
ms.assetid: f53c22a4-c01d-4d2f-81f0-bedf8f2ae5f0
title: Metodo CBaseAllocator. seproperties (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 000da3ee359ad727e3af972fc4aa6d0dbbb9133e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331800"
---
# <a name="cbaseallocatorsetproperties-method"></a><span data-ttu-id="1fd22-104">Metodo CBaseAllocator. seproperties</span><span class="sxs-lookup"><span data-stu-id="1fd22-104">CBaseAllocator.SetProperties method</span></span>

<span data-ttu-id="1fd22-105">Il `SetProperties` metodo specifica il numero di buffer da allocare e le dimensioni di ogni buffer.</span><span class="sxs-lookup"><span data-stu-id="1fd22-105">The `SetProperties` method specifies the number of buffers to allocate and the size of each buffer.</span></span> <span data-ttu-id="1fd22-106">Questo metodo implementa il metodo [**IMemAllocator::**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) SetValue.</span><span class="sxs-lookup"><span data-stu-id="1fd22-106">This method implements the [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fd22-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1fd22-107">Syntax</span></span>


```C++
HRESULT SetProperties(
   ALLOCATOR_PROPERTIES *pRequest,
   ALLOCATOR_PROPERTIES *pActual
);
```



## <a name="parameters"></a><span data-ttu-id="1fd22-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1fd22-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fd22-109">*pRequest*</span><span class="sxs-lookup"><span data-stu-id="1fd22-109">*pRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="1fd22-110">Puntatore a una struttura di [**\_ proprietà dell'allocatore**](/windows/win32/api/strmif/ns-strmif-allocator_properties) che contiene i requisiti del buffer.</span><span class="sxs-lookup"><span data-stu-id="1fd22-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the buffer requirements.</span></span>

</dd> <dt>

<span data-ttu-id="1fd22-111">*pActual*</span><span class="sxs-lookup"><span data-stu-id="1fd22-111">*pActual*</span></span> 
</dt> <dd>

<span data-ttu-id="1fd22-112">Puntatore a una struttura di **\_ proprietà dell'allocatore** che riceve le proprietà effettive del buffer.</span><span class="sxs-lookup"><span data-stu-id="1fd22-112">Pointer to an **ALLOCATOR\_PROPERTIES** structure that receives the actual buffer properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fd22-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1fd22-113">Return value</span></span>

<span data-ttu-id="1fd22-114">Restituisce uno dei seguenti valori **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1fd22-114">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="1fd22-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="1fd22-115">Return code</span></span>                                                                                                 | <span data-ttu-id="1fd22-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1fd22-116">Description</span></span>                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="1fd22-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1fd22-117"><dt>**S\_OK**</dt></span></span> </dl>                        | <span data-ttu-id="1fd22-118">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="1fd22-118">Success.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="1fd22-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="1fd22-119"><dt>**E\_POINTER**</dt></span></span> </dl>                   | <span data-ttu-id="1fd22-120">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="1fd22-120">**NULL** pointer argument.</span></span><br/>                                 |
| <dl> <span data-ttu-id="1fd22-121"><dt>**è \_ \_ già stato \_ eseguito il commit di VFW**</dt></span><span class="sxs-lookup"><span data-stu-id="1fd22-121"><dt>**VFW\_E\_ALREADY\_COMMITTED**</dt></span></span> </dl>   | <span data-ttu-id="1fd22-122">Non è possibile modificare la memoria allocata mentre il filtro è attivo.</span><span class="sxs-lookup"><span data-stu-id="1fd22-122">Cannot change allocated memory while the filter is active.</span></span><br/> |
| <dl> <span data-ttu-id="1fd22-123"><dt>**VFW \_ E \_ BADALIGN**</dt></span><span class="sxs-lookup"><span data-stu-id="1fd22-123"><dt>**VFW\_E\_BADALIGN**</dt></span></span> </dl>             | <span data-ttu-id="1fd22-124">È stato specificato un allineamento non valido.</span><span class="sxs-lookup"><span data-stu-id="1fd22-124">An invalid alignment was specified.</span></span><br/>                        |
| <dl> <span data-ttu-id="1fd22-125"><dt>**\_buffer VFW E in \_ \_ attesa**</dt></span><span class="sxs-lookup"><span data-stu-id="1fd22-125"><dt>**VFW\_E\_BUFFERS\_OUTSTANDING**</dt></span></span> </dl> | <span data-ttu-id="1fd22-126">Uno o più buffer sono ancora attivi.</span><span class="sxs-lookup"><span data-stu-id="1fd22-126">One or more buffers are still active.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="1fd22-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="1fd22-127">Remarks</span></span>

<span data-ttu-id="1fd22-128">Questo metodo specifica i requisiti del buffer, ma non alloca i buffer.</span><span class="sxs-lookup"><span data-stu-id="1fd22-128">This method specifies the buffer requirements, but does not allocate any buffers.</span></span> <span data-ttu-id="1fd22-129">Chiamare il metodo [**CBaseAllocator:: commit**](cbaseallocator-commit.md) per allocare i buffer.</span><span class="sxs-lookup"><span data-stu-id="1fd22-129">Call the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method to allocate buffers.</span></span>

<span data-ttu-id="1fd22-130">Il chiamante alloca due strutture delle proprietà dell'ALLOCAtore \_ .</span><span class="sxs-lookup"><span data-stu-id="1fd22-130">The caller allocates two ALLOCATOR\_PROPERTIES structures.</span></span> <span data-ttu-id="1fd22-131">Il parametro *pRequest* contiene i requisiti del buffer del chiamante, inclusi il numero di buffer e le dimensioni di ogni buffer.</span><span class="sxs-lookup"><span data-stu-id="1fd22-131">The *pRequest* parameter contains the caller's buffer requirements, including the number of buffers and the size of each buffer.</span></span> <span data-ttu-id="1fd22-132">Quando il metodo viene restituito, il parametro *pActual* contiene le proprietà del buffer effettive, impostate dall'allocatore.</span><span class="sxs-lookup"><span data-stu-id="1fd22-132">When the method returns, the *pActual* parameter contains the actual buffer properties, as set by the allocator.</span></span> <span data-ttu-id="1fd22-133">Nella classe di base, supponendo che il metodo abbia esito positivo, le proprietà effettive corrispondono sempre alle proprietà richieste.</span><span class="sxs-lookup"><span data-stu-id="1fd22-133">In the base class, assuming that the method succeeds, the actual properties always match the requested properties.</span></span> <span data-ttu-id="1fd22-134">Le classi derivate potrebbero ignorare questo comportamento.</span><span class="sxs-lookup"><span data-stu-id="1fd22-134">Derived classes might override this behavior.</span></span>

<span data-ttu-id="1fd22-135">L'allocatore non deve essere sottoposta a commit e non deve avere buffer in attesa.</span><span class="sxs-lookup"><span data-stu-id="1fd22-135">The allocator must not be committed, and must not have outstanding buffers.</span></span> <span data-ttu-id="1fd22-136">Nella classe di base, l'allineamento deve essere uguale a 1.</span><span class="sxs-lookup"><span data-stu-id="1fd22-136">In the base class, the alignment must equal 1.</span></span> <span data-ttu-id="1fd22-137">La classe [**CMemAllocator**](cmemallocator.md) esegue l'override di questo requisito.</span><span class="sxs-lookup"><span data-stu-id="1fd22-137">The [**CMemAllocator**](cmemallocator.md) class overrides this requirement.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fd22-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1fd22-138">Requirements</span></span>



| <span data-ttu-id="1fd22-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fd22-139">Requirement</span></span> | <span data-ttu-id="1fd22-140">Valore</span><span class="sxs-lookup"><span data-stu-id="1fd22-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fd22-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1fd22-141">Header</span></span><br/>  | <dl> <span data-ttu-id="1fd22-142"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1fd22-142"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1fd22-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="1fd22-143">Library</span></span><br/> | <dl> <span data-ttu-id="1fd22-144"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1fd22-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fd22-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1fd22-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fd22-146">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="1fd22-146">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




