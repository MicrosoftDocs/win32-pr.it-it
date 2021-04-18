---
description: 'Il metodo NotifyAllocator specifica un allocatore per la connessione. Questo metodo implementa il metodo IMemInputPin:: NotifyAllocator.'
ms.assetid: 16167bd5-2d33-4329-87ec-6a6c578e0060
title: Metodo CBaseInputPin. NotifyAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce5bc3cfe165b1adb6b5b970ca43d31c8ace98f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330701"
---
# <a name="cbaseinputpinnotifyallocator-method"></a><span data-ttu-id="e9f3d-104">CBaseInputPin. NotifyAllocator, metodo</span><span class="sxs-lookup"><span data-stu-id="e9f3d-104">CBaseInputPin.NotifyAllocator method</span></span>

<span data-ttu-id="e9f3d-105">Il `NotifyAllocator` metodo specifica un allocatore per la connessione.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-105">The `NotifyAllocator` method specifies an allocator for the connection.</span></span> <span data-ttu-id="e9f3d-106">Questo metodo implementa il metodo [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) .</span><span class="sxs-lookup"><span data-stu-id="e9f3d-106">This method implements the [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9f3d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9f3d-107">Syntax</span></span>


```C++
HRESULT NotifyAllocator(
   IMemAllocator *pAllocator,
   BOOL          bReadOnly
);
```



## <a name="parameters"></a><span data-ttu-id="e9f3d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e9f3d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9f3d-109">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="e9f3d-109">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="e9f3d-110">Puntatore all'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-110">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="e9f3d-111">*bReadOnly*</span><span class="sxs-lookup"><span data-stu-id="e9f3d-111">*bReadOnly*</span></span> 
</dt> <dd>

<span data-ttu-id="e9f3d-112">Flag che specifica se gli esempi di questo allocatore sono di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-112">Flag that specifies whether samples from this allocator are read-only.</span></span> <span data-ttu-id="e9f3d-113">Se **true**, gli esempi sono di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-113">If **TRUE**, samples are read-only.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9f3d-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e9f3d-114">Return value</span></span>

<span data-ttu-id="e9f3d-115">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-115">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9f3d-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9f3d-116">Remarks</span></span>

<span data-ttu-id="e9f3d-117">Durante la connessione del PIN, il pin di output sceglie un allocatore e chiama questo metodo per inviare una notifica al pin di input.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-117">During the pin connection, the output pin chooses an allocator and calls this method to notify the input pin.</span></span> <span data-ttu-id="e9f3d-118">Il pin di output può usare l'allocatore proposto dal pin di input nel metodo [**IMemInputPin:: Getallocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) oppure può fornire il proprio allocatore.</span><span class="sxs-lookup"><span data-stu-id="e9f3d-118">The output pin can use the allocator that the input pin proposed in the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method, or it can provide its own allocator.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9f3d-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9f3d-119">Requirements</span></span>



| <span data-ttu-id="e9f3d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9f3d-120">Requirement</span></span> | <span data-ttu-id="e9f3d-121">Valore</span><span class="sxs-lookup"><span data-stu-id="e9f3d-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9f3d-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e9f3d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e9f3d-123"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9f3d-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e9f3d-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="e9f3d-124">Library</span></span><br/> | <dl> <span data-ttu-id="e9f3d-125"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e9f3d-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9f3d-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9f3d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9f3d-127">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="e9f3d-127">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




