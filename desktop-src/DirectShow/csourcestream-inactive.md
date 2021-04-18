---
description: "Il metodo inattivo notifica al pin che il filtro non è più attivo. Questo metodo esegue l'override del Metodo CBasePin:: Inactive. Se il thread di streaming è attivo, questo metodo lo arresta e attende la chiusura del thread."
ms.assetid: 82cf0f13-e563-4a0b-b2e1-25ab19f7ed78
title: Metodo CSourceStream. Inactive (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c4fab336f5f06d932189ee991fd190d1ae42b27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328170"
---
# <a name="csourcestreaminactive-method"></a><span data-ttu-id="5334b-105">Metodo CSourceStream. Inactive</span><span class="sxs-lookup"><span data-stu-id="5334b-105">CSourceStream.Inactive method</span></span>

<span data-ttu-id="5334b-106">Il `Inactive` metodo notifica al pin che il filtro non è più attivo.</span><span class="sxs-lookup"><span data-stu-id="5334b-106">The `Inactive` method notifies the pin that the filter is no longer active.</span></span> <span data-ttu-id="5334b-107">Questo metodo esegue l'override del metodo [**CBasePin:: inactive**](cbasepin-inactive.md) .</span><span class="sxs-lookup"><span data-stu-id="5334b-107">This method overrides the [**CBasePin::Inactive**](cbasepin-inactive.md) method.</span></span> <span data-ttu-id="5334b-108">Se il thread di streaming è attivo, questo metodo lo arresta e attende la chiusura del thread.</span><span class="sxs-lookup"><span data-stu-id="5334b-108">If the streaming thread is active, this method stops it and waits for the thread to exit.</span></span>

## <a name="syntax"></a><span data-ttu-id="5334b-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5334b-109">Syntax</span></span>


```C++
HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="5334b-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="5334b-110">Parameters</span></span>

<span data-ttu-id="5334b-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="5334b-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5334b-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5334b-112">Return value</span></span>

<span data-ttu-id="5334b-113">Restituisce S \_ OK o un altro valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5334b-113">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5334b-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5334b-114">Requirements</span></span>



| <span data-ttu-id="5334b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5334b-115">Requirement</span></span> | <span data-ttu-id="5334b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="5334b-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5334b-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5334b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5334b-118"><dt>Source. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5334b-118"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="5334b-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="5334b-119">Library</span></span><br/> | <dl> <span data-ttu-id="5334b-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5334b-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5334b-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5334b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5334b-122">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="5334b-122">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




