---
description: Il metodo Stop arresta il filtro.
ms.assetid: 80eac207-5db3-4b06-bbae-eca72e37d09d
title: Metodo CBaseRenderer. Stop (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ddd8194bbf76c4a4311aa90335f94d1e7548a356
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332995"
---
# <a name="cbaserendererstop-method"></a><span data-ttu-id="14178-103">Metodo CBaseRenderer. Stop</span><span class="sxs-lookup"><span data-stu-id="14178-103">CBaseRenderer.Stop method</span></span>

<span data-ttu-id="14178-104">Il `Stop` metodo interrompe il filtro.</span><span class="sxs-lookup"><span data-stu-id="14178-104">The `Stop` method stops the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="14178-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="14178-105">Syntax</span></span>


```C++
HRESULT Stop();
```



## <a name="parameters"></a><span data-ttu-id="14178-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="14178-106">Parameters</span></span>

<span data-ttu-id="14178-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="14178-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="14178-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="14178-108">Return value</span></span>

<span data-ttu-id="14178-109">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="14178-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="14178-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="14178-110">Remarks</span></span>

<span data-ttu-id="14178-111">Questo metodo esegue l'override del metodo [**CBaseFilter:: Stop**](cbasefilter-stop.md) .</span><span class="sxs-lookup"><span data-stu-id="14178-111">This method overrides the [**CBaseFilter::Stop**](cbasefilter-stop.md) method.</span></span> <span data-ttu-id="14178-112">Esegue le azioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="14178-112">It performs the following actions:</span></span>

-   <span data-ttu-id="14178-113">Chiama [**CBaseFilter:: Stop**](cbasefilter-stop.md).</span><span class="sxs-lookup"><span data-stu-id="14178-113">Calls [**CBaseFilter::Stop**](cbasefilter-stop.md).</span></span>
-   <span data-ttu-id="14178-114">Decommit dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="14178-114">Decommits the allocator.</span></span> <span data-ttu-id="14178-115">(Vedere [**IMemAllocator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit)).</span><span class="sxs-lookup"><span data-stu-id="14178-115">(See [**IMemAllocator::Decommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit).)</span></span>
-   <span data-ttu-id="14178-116">Annulla qualsiasi rendering pianificato e rilascia il thread di streaming.</span><span class="sxs-lookup"><span data-stu-id="14178-116">Cancels any scheduled rendering and releases the streaming thread.</span></span>
-   <span data-ttu-id="14178-117">Attende il completamento di qualsiasi chiamata di **ricezione** in sospeso.</span><span class="sxs-lookup"><span data-stu-id="14178-117">Waits for any pending **Receive** call to complete.</span></span>

## <a name="requirements"></a><span data-ttu-id="14178-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14178-118">Requirements</span></span>



| <span data-ttu-id="14178-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="14178-119">Requirement</span></span> | <span data-ttu-id="14178-120">Valore</span><span class="sxs-lookup"><span data-stu-id="14178-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14178-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="14178-121">Header</span></span><br/>  | <dl> <span data-ttu-id="14178-122"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="14178-122"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="14178-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="14178-123">Library</span></span><br/> | <dl> <span data-ttu-id="14178-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="14178-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14178-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14178-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14178-126">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="14178-126">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




