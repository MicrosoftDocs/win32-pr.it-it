---
description: Il metodo seproperties specifica il numero di buffer da allocare e le dimensioni di ogni buffer.
ms.assetid: 01f63379-1d66-4a72-b87c-de55504b0bb4
title: Metodo CMemAllocator. seproperties (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8505916245cca81fdd84132e4523fe9dd03b971b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328845"
---
# <a name="cmemallocatorsetproperties-method"></a><span data-ttu-id="fc667-103">Metodo CMemAllocator. seproperties</span><span class="sxs-lookup"><span data-stu-id="fc667-103">CMemAllocator.SetProperties method</span></span>

<span data-ttu-id="fc667-104">Il `SetProperties` metodo specifica il numero di buffer da allocare e le dimensioni di ogni buffer.</span><span class="sxs-lookup"><span data-stu-id="fc667-104">The `SetProperties` method specifies the number of buffers to allocate and the size of each buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc667-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc667-105">Syntax</span></span>


```C++
HRESULT SetProperties(
   ALLOCATOR_PROPERTIES *pRequest,
   ALLOCATOR_PROPERTIES *pActual
);
```



## <a name="parameters"></a><span data-ttu-id="fc667-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fc667-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc667-107">*pRequest*</span><span class="sxs-lookup"><span data-stu-id="fc667-107">*pRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="fc667-108">Puntatore a una struttura di [**\_ proprietà dell'allocatore**](/windows/win32/api/strmif/ns-strmif-allocator_properties) che contiene i requisiti del buffer.</span><span class="sxs-lookup"><span data-stu-id="fc667-108">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the buffer requirements.</span></span>

</dd> <dt>

<span data-ttu-id="fc667-109">*pActual*</span><span class="sxs-lookup"><span data-stu-id="fc667-109">*pActual*</span></span> 
</dt> <dd>

<span data-ttu-id="fc667-110">Puntatore a una struttura di **\_ proprietà dell'allocatore** che riceve le proprietà effettive del buffer.</span><span class="sxs-lookup"><span data-stu-id="fc667-110">Pointer to an **ALLOCATOR\_PROPERTIES** structure that receives the actual buffer properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc667-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fc667-111">Return value</span></span>

<span data-ttu-id="fc667-112">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="fc667-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="fc667-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="fc667-113">Return code</span></span>                                                                                                 | <span data-ttu-id="fc667-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fc667-114">Description</span></span>                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="fc667-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fc667-115"><dt>**S\_OK**</dt></span></span> </dl>                        | <span data-ttu-id="fc667-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="fc667-116">Success.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="fc667-117"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="fc667-117"><dt>**E\_POINTER**</dt></span></span> </dl>                   | <span data-ttu-id="fc667-118">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="fc667-118">**NULL** pointer argument.</span></span><br/>                                 |
| <dl> <span data-ttu-id="fc667-119"><dt>**è \_ \_ già stato \_ eseguito il commit di VFW**</dt></span><span class="sxs-lookup"><span data-stu-id="fc667-119"><dt>**VFW\_E\_ALREADY\_COMMITTED**</dt></span></span> </dl>   | <span data-ttu-id="fc667-120">Non è possibile modificare la memoria allocata mentre il filtro è attivo.</span><span class="sxs-lookup"><span data-stu-id="fc667-120">Cannot change allocated memory while the filter is active.</span></span><br/> |
| <dl> <span data-ttu-id="fc667-121"><dt>**VFW \_ E \_ BADALIGN**</dt></span><span class="sxs-lookup"><span data-stu-id="fc667-121"><dt>**VFW\_E\_BADALIGN**</dt></span></span> </dl>             | <span data-ttu-id="fc667-122">È stato specificato un allineamento non valido.</span><span class="sxs-lookup"><span data-stu-id="fc667-122">An invalid alignment was specified.</span></span><br/>                        |
| <dl> <span data-ttu-id="fc667-123"><dt>**\_buffer VFW E in \_ \_ attesa**</dt></span><span class="sxs-lookup"><span data-stu-id="fc667-123"><dt>**VFW\_E\_BUFFERS\_OUTSTANDING**</dt></span></span> </dl> | <span data-ttu-id="fc667-124">Uno o più buffer sono ancora attivi.</span><span class="sxs-lookup"><span data-stu-id="fc667-124">One or more buffers are still active.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="fc667-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc667-125">Remarks</span></span>

<span data-ttu-id="fc667-126">Questo metodo esegue l'override del metodo [**CBaseAllocator::**](cbaseallocator-setproperties.md) SetValue.</span><span class="sxs-lookup"><span data-stu-id="fc667-126">This method overrides the [**CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) method.</span></span>

<span data-ttu-id="fc667-127">L'allineamento del buffer, specificato dal membro **cbAlign** della struttura **delle \_ proprietà dell'allocatore** , deve essere una potenza pari di due.</span><span class="sxs-lookup"><span data-stu-id="fc667-127">The buffer alignment, specified by the **cbAlign** member of the **ALLOCATOR\_PROPERTIES** structure, must be an even power of two.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc667-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc667-128">Requirements</span></span>



| <span data-ttu-id="fc667-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc667-129">Requirement</span></span> | <span data-ttu-id="fc667-130">Valore</span><span class="sxs-lookup"><span data-stu-id="fc667-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc667-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fc667-131">Header</span></span><br/>  | <dl> <span data-ttu-id="fc667-132"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fc667-132"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fc667-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="fc667-133">Library</span></span><br/> | <dl> <span data-ttu-id="fc667-134"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="fc667-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc667-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc667-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc667-136">**Classe CMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="fc667-136">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




