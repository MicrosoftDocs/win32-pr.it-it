---
description: Il metodo pause sospende il filtro. Questo metodo implementa il metodo IMediaFilter::P ause.
ms.assetid: cfb7d532-6c00-49a1-a48d-4dadaca39a0f
title: Metodo CBaseFilter. pause (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 43a90e78084f2320d0df7da806b6138571c9a5bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332077"
---
# <a name="cbasefilterpause-method"></a><span data-ttu-id="a2e8b-104">CBaseFilter. pause (metodo)</span><span class="sxs-lookup"><span data-stu-id="a2e8b-104">CBaseFilter.Pause method</span></span>

<span data-ttu-id="a2e8b-105">Il `Pause` metodo sospende il filtro.</span><span class="sxs-lookup"><span data-stu-id="a2e8b-105">The `Pause` method pauses the filter.</span></span> <span data-ttu-id="a2e8b-106">Questo metodo implementa il metodo [**IMediaFilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) .</span><span class="sxs-lookup"><span data-stu-id="a2e8b-106">This method implements the [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2e8b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a2e8b-107">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="a2e8b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a2e8b-108">Parameters</span></span>

<span data-ttu-id="a2e8b-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a2e8b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a2e8b-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a2e8b-110">Return value</span></span>

<span data-ttu-id="a2e8b-111">Restituisce \_ OK se ha esito positivo o un valore **HRESULT** che indica la ragione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="a2e8b-111">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2e8b-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="a2e8b-112">Remarks</span></span>

<span data-ttu-id="a2e8b-113">Questo metodo chiama il metodo [**CBasePin:: Active**](cbasepin-active.md) su ognuno dei pin connessi del filtro.</span><span class="sxs-lookup"><span data-stu-id="a2e8b-113">This method calls the [**CBasePin::Active**](cbasepin-active.md) method on each of the filter's connected pins.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2e8b-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a2e8b-114">Requirements</span></span>



| <span data-ttu-id="a2e8b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2e8b-115">Requirement</span></span> | <span data-ttu-id="a2e8b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a2e8b-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2e8b-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a2e8b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a2e8b-118"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a2e8b-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a2e8b-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="a2e8b-119">Library</span></span><br/> | <dl> <span data-ttu-id="a2e8b-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a2e8b-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2e8b-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a2e8b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2e8b-122">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="a2e8b-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




