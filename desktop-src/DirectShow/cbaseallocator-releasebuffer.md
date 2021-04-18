---
description: "Il metodo ReleaseBuffer restituisce un esempio di supporto all'elenco di esempi di supporti disponibili. Questo metodo implementa il metodo IMemAllocator:: ReleaseBuffer."
ms.assetid: 35e4e426-044c-4e57-af13-2fddf8501db7
title: Metodo CBaseAllocator. ReleaseBuffer (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.ReleaseBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e339f3a8186e845e28261633806a61b1b15c281
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331804"
---
# <a name="cbaseallocatorreleasebuffer-method"></a><span data-ttu-id="67c32-104">CBaseAllocator. ReleaseBuffer, metodo</span><span class="sxs-lookup"><span data-stu-id="67c32-104">CBaseAllocator.ReleaseBuffer method</span></span>

<span data-ttu-id="67c32-105">Il `ReleaseBuffer` metodo restituisce un esempio di supporto all'elenco di esempi di supporti disponibili.</span><span class="sxs-lookup"><span data-stu-id="67c32-105">The `ReleaseBuffer` method returns a media sample to the list of free media samples.</span></span> <span data-ttu-id="67c32-106">Questo metodo implementa il metodo [**IMemAllocator:: ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) .</span><span class="sxs-lookup"><span data-stu-id="67c32-106">This method implements the [**IMemAllocator::ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="67c32-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="67c32-107">Syntax</span></span>


```C++
HRESULT ReleaseBuffer(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="67c32-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="67c32-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67c32-109">*pSample*</span><span class="sxs-lookup"><span data-stu-id="67c32-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="67c32-110">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'oggetto di esempio multimediale.</span><span class="sxs-lookup"><span data-stu-id="67c32-110">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the media sample object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67c32-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="67c32-111">Return value</span></span>

<span data-ttu-id="67c32-112">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="67c32-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="67c32-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="67c32-113">Remarks</span></span>

<span data-ttu-id="67c32-114">Quando il conteggio dei riferimenti di un campione multimediale raggiunge zero, l'esempio chiama **ReleaseBuffer** con se stesso come parametro.</span><span class="sxs-lookup"><span data-stu-id="67c32-114">When a media sample's reference count reaches zero, the sample calls **ReleaseBuffer** with itself as the parameter.</span></span> <span data-ttu-id="67c32-115">Questo metodo esegue le azioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="67c32-115">This method performs the following actions.</span></span>

-   <span data-ttu-id="67c32-116">Restituisce l'esempio di supporto all'elenco di disponibilità ([**CBaseAllocator:: m \_ lFree**](cbaseallocator-m-lfree.md)).</span><span class="sxs-lookup"><span data-stu-id="67c32-116">Returns the media sample to the free list ([**CBaseAllocator::m\_lFree**](cbaseallocator-m-lfree.md)).</span></span>
-   <span data-ttu-id="67c32-117">Chiama il metodo [**CBaseAllocator:: NotifySample**](cbaseallocator-notifysample.md) , che rilascia tutti i thread bloccati sulle chiamate al metodo [**CBaseAllocator:: GetBuffer**](cbaseallocator-getbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="67c32-117">Calls the [**CBaseAllocator::NotifySample**](cbaseallocator-notifysample.md) method, which releases any threads that are blocked on calls to the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method.</span></span>
-   <span data-ttu-id="67c32-118">Se il metodo [**CBaseAllocator:: senotify**](cbaseallocator-setnotify.md) è stato chiamato in precedenza, chiama il metodo **IMemAllocatorNotifyCallbackTemp:: NotifyRelease** .</span><span class="sxs-lookup"><span data-stu-id="67c32-118">If the [**CBaseAllocator::SetNotify**](cbaseallocator-setnotify.md) method was called previously, calls the **IMemAllocatorNotifyCallbackTemp::NotifyRelease** method.</span></span>
-   <span data-ttu-id="67c32-119">Quando viene rilasciato l'ultimo esempio, se è presente una chiamata a [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) in sospeso, chiama il metodo [**CBaseAllocator:: Free**](cbaseallocator-free.md) per rilasciare la memoria del buffer.</span><span class="sxs-lookup"><span data-stu-id="67c32-119">When the last sample is released, if there is a pending [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) call, calls the [**CBaseAllocator::Free**](cbaseallocator-free.md) method to release the buffer memory.</span></span> <span data-ttu-id="67c32-120">Nella classe di base, **Free** è un metodo virtuale puro.</span><span class="sxs-lookup"><span data-stu-id="67c32-120">(In the base class, **Free** is a pure virtual method.)</span></span>

## <a name="requirements"></a><span data-ttu-id="67c32-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="67c32-121">Requirements</span></span>



| <span data-ttu-id="67c32-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="67c32-122">Requirement</span></span> | <span data-ttu-id="67c32-123">Valore</span><span class="sxs-lookup"><span data-stu-id="67c32-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67c32-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="67c32-124">Header</span></span><br/>  | <dl> <span data-ttu-id="67c32-125"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="67c32-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="67c32-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="67c32-126">Library</span></span><br/> | <dl> <span data-ttu-id="67c32-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="67c32-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67c32-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="67c32-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67c32-129">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="67c32-129">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




