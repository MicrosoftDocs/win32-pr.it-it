---
description: "Il metodo senotify imposta o rimuove un callback nell'allocatore. L'allocatore chiama il metodo di callback ogni volta che viene chiamato il metodo IMemAllocator:: ReleaseBuffer dell'allocatore."
ms.assetid: ef9a6c66-d392-4130-b4fc-9eb6aecb6cbf
title: Metodo CBaseAllocator. senotify (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetNotify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d8269112325d470cae59cff6e615f04fbdfab91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331802"
---
# <a name="cbaseallocatorsetnotify-method"></a><span data-ttu-id="6b0ae-104">Metodo CBaseAllocator. senotify</span><span class="sxs-lookup"><span data-stu-id="6b0ae-104">CBaseAllocator.SetNotify method</span></span>

<span data-ttu-id="6b0ae-105">\[[**Senotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) può essere modificato o non disponibile nelle versioni successive.\]</span><span class="sxs-lookup"><span data-stu-id="6b0ae-105">\[[**SetNotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="6b0ae-106">Il `SetNotify` metodo imposta o rimuove un callback nell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="6b0ae-106">The `SetNotify` method sets or removes a callback on the allocator.</span></span> <span data-ttu-id="6b0ae-107">L'allocatore chiama il metodo di callback ogni volta che viene chiamato il metodo [**IMemAllocator:: ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="6b0ae-107">The allocator calls the callback method whenever the allocator's [**IMemAllocator::ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) method is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b0ae-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6b0ae-108">Syntax</span></span>


```C++
HRESULT SetNotify(
   IMemAllocatorNotifyCallbackTemp *pNotify
);
```



## <a name="parameters"></a><span data-ttu-id="6b0ae-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6b0ae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b0ae-110">*pNotify*</span><span class="sxs-lookup"><span data-stu-id="6b0ae-110">*pNotify*</span></span> 
</dt> <dd>

<span data-ttu-id="6b0ae-111">Puntatore all'interfaccia [**IMemAllocatorNotifyCallbackTemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatornotifycallbacktemp) che verrà utilizzata per il callback.</span><span class="sxs-lookup"><span data-stu-id="6b0ae-111">Pointer to the [**IMemAllocatorNotifyCallbackTemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatornotifycallbacktemp) interface that will be used for the callback.</span></span> <span data-ttu-id="6b0ae-112">Il chiamante deve implementare l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6b0ae-112">The caller must implement the interface.</span></span> <span data-ttu-id="6b0ae-113">Usare il valore **null** per rimuovere il callback.</span><span class="sxs-lookup"><span data-stu-id="6b0ae-113">Use the value **NULL** to remove the callback.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b0ae-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6b0ae-114">Return value</span></span>

<span data-ttu-id="6b0ae-115">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6b0ae-115">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b0ae-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="6b0ae-116">Remarks</span></span>

<span data-ttu-id="6b0ae-117">Questo metodo implementa il metodo [**IMemAllocatorCallbackTemp:: senotify**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-setnotify) .</span><span class="sxs-lookup"><span data-stu-id="6b0ae-117">This method implements the [**IMemAllocatorCallbackTemp::SetNotify**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-setnotify) method.</span></span> <span data-ttu-id="6b0ae-118">L'allocatore non espone l'interfaccia [**IMemAllocatorCallbackTemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatorcallbacktemp) , a meno che il flag *fEnableReleaseCallback* non sia impostato su **true** nel costruttore [**CBaseAllocator**](cbaseallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="6b0ae-118">The allocator does not expose the [**IMemAllocatorCallbackTemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatorcallbacktemp) interface unless the *fEnableReleaseCallback* flag is set to **TRUE** in the [**CBaseAllocator**](cbaseallocator.md) constructor.</span></span>

<span data-ttu-id="6b0ae-119">Questo metodo imposta la variabile membro [**CBaseAllocator:: m \_ pNotify**](cbaseallocator-m-pnotify.md) uguale a *pNotify* e incrementa il conteggio dei riferimenti nell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6b0ae-119">This method sets the [**CBaseAllocator::m\_pNotify**](cbaseallocator-m-pnotify.md) member variable equal to *pNotify* and increments the reference count on the interface.</span></span> <span data-ttu-id="6b0ae-120">Se *m \_ pNotify* è diverso da **null**, il metodo **ReleaseBuffer** dell'allocatore chiama [**IMemAllocatorNotifyCallbackTemp:: NotifyRelease**](/windows/desktop/api/Strmif/nf-strmif-imemallocatornotifycallbacktemp-notifyrelease).</span><span class="sxs-lookup"><span data-stu-id="6b0ae-120">If *m\_pNotify* is non-**NULL**, the allocator's **ReleaseBuffer** method calls [**IMemAllocatorNotifyCallbackTemp::NotifyRelease**](/windows/desktop/api/Strmif/nf-strmif-imemallocatornotifycallbacktemp-notifyrelease).</span></span> <span data-ttu-id="6b0ae-121">Per informazioni sull'implementazione del callback, vedere la sezione Osservazioni in questo metodo.</span><span class="sxs-lookup"><span data-stu-id="6b0ae-121">See the Remarks section in that method for information about implementing the callback.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b0ae-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b0ae-122">Requirements</span></span>



| <span data-ttu-id="6b0ae-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b0ae-123">Requirement</span></span> | <span data-ttu-id="6b0ae-124">Valore</span><span class="sxs-lookup"><span data-stu-id="6b0ae-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b0ae-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6b0ae-125">Header</span></span><br/>  | <dl> <span data-ttu-id="6b0ae-126"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6b0ae-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6b0ae-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="6b0ae-127">Library</span></span><br/> | <dl> <span data-ttu-id="6b0ae-128"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6b0ae-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b0ae-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b0ae-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b0ae-130">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="6b0ae-130">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




