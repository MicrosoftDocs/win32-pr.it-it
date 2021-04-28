---
description: 'Metodo CBaseOutputPin.DecideBufferSize: il metodo DecideBufferSize imposta i requisiti del buffer.'
ms.assetid: 1f7a3424-18ba-4a10-b09f-947ee8585ffa
title: Metodo CBaseOutputPin.DecideBufferSize (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7a76f058e2f9c07a344453db87046704e26280a1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099529"
---
# <a name="cbaseoutputpindecidebuffersize-method"></a><span data-ttu-id="89c4f-103">Metodo CBaseOutputPin.DecideBufferSize</span><span class="sxs-lookup"><span data-stu-id="89c4f-103">CBaseOutputPin.DecideBufferSize method</span></span>

<span data-ttu-id="89c4f-104">Il `DecideBufferSize` metodo imposta i requisiti del buffer.</span><span class="sxs-lookup"><span data-stu-id="89c4f-104">The `DecideBufferSize` method sets the buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="89c4f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89c4f-105">Syntax</span></span>


```C++
virtual HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="89c4f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="89c4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89c4f-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="89c4f-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="89c4f-108">Puntatore all'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="89c4f-108">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="89c4f-109">*ppropInputRequest*</span><span class="sxs-lookup"><span data-stu-id="89c4f-109">*ppropInputRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="89c4f-110">Puntatore a una [**struttura ALLOCATOR \_ PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) che contiene i requisiti del buffer del pin di input.</span><span class="sxs-lookup"><span data-stu-id="89c4f-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the input pin's buffer requirements.</span></span> <span data-ttu-id="89c4f-111">Se il pin di input non ha requisiti, il chiamante deve azzerare i membri di questa struttura prima di chiamare il metodo .</span><span class="sxs-lookup"><span data-stu-id="89c4f-111">If the input pin does not have any requirements, the caller should zero out the members of this structure before calling the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89c4f-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="89c4f-112">Return value</span></span>

<span data-ttu-id="89c4f-113">Restituisce S OK in caso di esito positivo o un \_ **valore HRESULT** che indica la causa dell'errore.</span><span class="sxs-lookup"><span data-stu-id="89c4f-113">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="89c4f-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="89c4f-114">Remarks</span></span>

<span data-ttu-id="89c4f-115">Eseguire l'override di questo metodo nella classe derivata.</span><span class="sxs-lookup"><span data-stu-id="89c4f-115">Override this method in your derived class.</span></span> <span data-ttu-id="89c4f-116">Chiamare il [**metodo IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) per specificare i requisiti del buffer.</span><span class="sxs-lookup"><span data-stu-id="89c4f-116">Call the [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) method to specify your buffer requirements.</span></span> <span data-ttu-id="89c4f-117">In genere, la classe derivata rispetta i requisiti del buffer del pin di input, ma non è necessario.</span><span class="sxs-lookup"><span data-stu-id="89c4f-117">Typically, the derived class will honor the input pin's buffer requirements, but it is not required to.</span></span>

## <a name="requirements"></a><span data-ttu-id="89c4f-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89c4f-118">Requirements</span></span>



| <span data-ttu-id="89c4f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="89c4f-119">Requirement</span></span> | <span data-ttu-id="89c4f-120">Valore</span><span class="sxs-lookup"><span data-stu-id="89c4f-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89c4f-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="89c4f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="89c4f-122"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="89c4f-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="89c4f-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="89c4f-123">Library</span></span><br/> | <dl> <span data-ttu-id="89c4f-124"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="89c4f-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89c4f-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89c4f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89c4f-126">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="89c4f-126">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




