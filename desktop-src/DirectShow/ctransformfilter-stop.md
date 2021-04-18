---
description: 'Arresta il filtro. Questo metodo implementa il metodo IMediaFilter:: stop.'
ms.assetid: e95537d6-b3ec-49a4-aa28-333d69eff3bb
title: Metodo CTransformFilter. Stop (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2a7f7ea0f80095cd63f9708f12a42146260f2f8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331122"
---
# <a name="ctransformfilterstop-method"></a><span data-ttu-id="b7b38-104">Metodo CTransformFilter. Stop</span><span class="sxs-lookup"><span data-stu-id="b7b38-104">CTransformFilter.Stop method</span></span>

<span data-ttu-id="b7b38-105">Arresta il filtro.</span><span class="sxs-lookup"><span data-stu-id="b7b38-105">Stops the filter.</span></span> <span data-ttu-id="b7b38-106">Questo metodo implementa il metodo [**IMediaFilter:: Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .</span><span class="sxs-lookup"><span data-stu-id="b7b38-106">This method implements the [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7b38-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b7b38-107">Syntax</span></span>


```C++
HRESULT Stop();
```



## <a name="parameters"></a><span data-ttu-id="b7b38-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b7b38-108">Parameters</span></span>

<span data-ttu-id="b7b38-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="b7b38-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b7b38-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b7b38-110">Return value</span></span>

<span data-ttu-id="b7b38-111">Restituisce S \_ OK o un altro valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b7b38-111">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7b38-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="b7b38-112">Remarks</span></span>

<span data-ttu-id="b7b38-113">Una volta che questo metodo esegue il commit di entrambi gli allocatori, chiama il metodo [**StopStreaming**](ctransformfilter-stopstreaming.md) .</span><span class="sxs-lookup"><span data-stu-id="b7b38-113">After this method decommits both allocators, it calls the [**StopStreaming**](ctransformfilter-stopstreaming.md) method.</span></span> <span data-ttu-id="b7b38-114">Il metodo **StopStreaming** non esegue alcuna operazione nella classe di base, ma la classe derivata può eseguirne l'override.</span><span class="sxs-lookup"><span data-stu-id="b7b38-114">The **StopStreaming** method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7b38-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7b38-115">Requirements</span></span>



| <span data-ttu-id="b7b38-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7b38-116">Requirement</span></span> | <span data-ttu-id="b7b38-117">Valore</span><span class="sxs-lookup"><span data-stu-id="b7b38-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7b38-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b7b38-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b7b38-119"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b7b38-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b7b38-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="b7b38-120">Library</span></span><br/> | <dl> <span data-ttu-id="b7b38-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b7b38-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7b38-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7b38-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7b38-123">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="b7b38-123">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




