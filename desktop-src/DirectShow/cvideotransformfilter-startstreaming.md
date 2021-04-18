---
description: "Il metodo StartStreaming viene chiamato quando il filtro passa allo stato sospeso. Questo metodo esegue l'override del metodo CTransformFilter:: StartStreaming."
ms.assetid: fa05f88f-fed8-479d-b0b4-d9df982d51e7
title: Metodo CVideoTransformFilter. StartStreaming (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.StartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5ae8d49401389830f9d5dbf0ec91e7f390c51ca6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325500"
---
# <a name="cvideotransformfilterstartstreaming-method"></a><span data-ttu-id="4656a-104">CVideoTransformFilter. StartStreaming, metodo</span><span class="sxs-lookup"><span data-stu-id="4656a-104">CVideoTransformFilter.StartStreaming method</span></span>

<span data-ttu-id="4656a-105">Il `StartStreaming` metodo viene chiamato quando il filtro passa allo stato sospeso.</span><span class="sxs-lookup"><span data-stu-id="4656a-105">The `StartStreaming` method is called when the filter switches to the paused state.</span></span> <span data-ttu-id="4656a-106">Questo metodo esegue l'override del metodo [**CTransformFilter:: StartStreaming**](ctransformfilter-startstreaming.md) .</span><span class="sxs-lookup"><span data-stu-id="4656a-106">This method overrides the [**CTransformFilter::StartStreaming**](ctransformfilter-startstreaming.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4656a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4656a-107">Syntax</span></span>


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a><span data-ttu-id="4656a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4656a-108">Parameters</span></span>

<span data-ttu-id="4656a-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="4656a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4656a-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4656a-110">Return value</span></span>

<span data-ttu-id="4656a-111">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4656a-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="4656a-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="4656a-112">Remarks</span></span>

<span data-ttu-id="4656a-113">Questo metodo reimposta tutte le statistiche sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="4656a-113">This method resets all of the performance statistics.</span></span>

## <a name="requirements"></a><span data-ttu-id="4656a-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4656a-114">Requirements</span></span>



| <span data-ttu-id="4656a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4656a-115">Requirement</span></span> | <span data-ttu-id="4656a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="4656a-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4656a-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4656a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="4656a-118"><dt>Vtrans. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4656a-118"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4656a-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="4656a-119">Library</span></span><br/> | <dl> <span data-ttu-id="4656a-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4656a-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4656a-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4656a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4656a-122">**Classe CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="4656a-122">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




