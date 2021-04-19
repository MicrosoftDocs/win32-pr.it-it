---
description: 'Il metodo Stop arresta il filtro. Questo metodo implementa il metodo IMediaFilter:: stop.'
ms.assetid: 68d77f9a-95a2-4a71-bbe1-28be76fbc538
title: Metodo CBaseFilter. Stop (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b4c4893edcf02fa18da3dc207a49f87c91b2a9ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328172"
---
# <a name="cbasefilterstop-method"></a><span data-ttu-id="cdcf3-104">Metodo CBaseFilter. Stop</span><span class="sxs-lookup"><span data-stu-id="cdcf3-104">CBaseFilter.Stop method</span></span>

<span data-ttu-id="cdcf3-105">Il `Stop` metodo interrompe il filtro.</span><span class="sxs-lookup"><span data-stu-id="cdcf3-105">The `Stop` method stops the filter.</span></span> <span data-ttu-id="cdcf3-106">Questo metodo implementa il metodo [**IMediaFilter:: Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .</span><span class="sxs-lookup"><span data-stu-id="cdcf3-106">This method implements the [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdcf3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cdcf3-107">Syntax</span></span>


```C++
HRESULT Stop();
```



## <a name="parameters"></a><span data-ttu-id="cdcf3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="cdcf3-108">Parameters</span></span>

<span data-ttu-id="cdcf3-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="cdcf3-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cdcf3-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cdcf3-110">Return value</span></span>

<span data-ttu-id="cdcf3-111">Restituisce \_ OK se ha esito positivo o un valore **HRESULT** che indica la ragione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="cdcf3-111">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdcf3-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="cdcf3-112">Remarks</span></span>

<span data-ttu-id="cdcf3-113">Questo metodo chiama il metodo [**CBasePin:: inactive**](cbasepin-inactive.md) su ognuno dei pin connessi del filtro.</span><span class="sxs-lookup"><span data-stu-id="cdcf3-113">This method calls the [**CBasePin::Inactive**](cbasepin-inactive.md) method on each of the filter's connected pins.</span></span> <span data-ttu-id="cdcf3-114">Imposta anche lo stato del filtro sullo stato \_ arrestato.</span><span class="sxs-lookup"><span data-stu-id="cdcf3-114">It also sets the filter's state to State\_Stopped.</span></span>

<span data-ttu-id="cdcf3-115">Quando il filtro si interrompe, deve rifiutare esempi da upstream, interrompere la distribuzione di campioni a valle, arrestare i thread di lavoro e liberare le risorse usate per lo streaming.</span><span class="sxs-lookup"><span data-stu-id="cdcf3-115">When the filter stops, it should reject samples from upstream, stop delivering samples downstream, shut down worker threads, and free any resources that it used for streaming.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdcf3-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cdcf3-116">Requirements</span></span>



| <span data-ttu-id="cdcf3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdcf3-117">Requirement</span></span> | <span data-ttu-id="cdcf3-118">Valore</span><span class="sxs-lookup"><span data-stu-id="cdcf3-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdcf3-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cdcf3-119">Header</span></span><br/>  | <dl> <span data-ttu-id="cdcf3-120"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cdcf3-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cdcf3-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="cdcf3-121">Library</span></span><br/> | <dl> <span data-ttu-id="cdcf3-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cdcf3-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdcf3-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cdcf3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdcf3-124">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="cdcf3-124">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




