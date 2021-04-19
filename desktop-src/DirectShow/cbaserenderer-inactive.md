---
description: Il metodo inattivo viene chiamato quando lo stato viene impostato su arrestato.
ms.assetid: 2bad81ef-d2a4-4c20-a49b-e40e5097b430
title: Metodo CBaseRenderer. Inactive (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ac328c772b740a0d7ab05be4c6ea9f2a24f852e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326282"
---
# <a name="cbaserendererinactive-method"></a><span data-ttu-id="0466e-103">Metodo CBaseRenderer. Inactive</span><span class="sxs-lookup"><span data-stu-id="0466e-103">CBaseRenderer.Inactive method</span></span>

<span data-ttu-id="0466e-104">Il `Inactive` metodo viene chiamato quando lo stato viene impostato come arrestato.</span><span class="sxs-lookup"><span data-stu-id="0466e-104">The `Inactive` method is called when the state is switched to stopped.</span></span>

## <a name="syntax"></a><span data-ttu-id="0466e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0466e-105">Syntax</span></span>


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="0466e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0466e-106">Parameters</span></span>

<span data-ttu-id="0466e-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="0466e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0466e-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0466e-108">Return value</span></span>

<span data-ttu-id="0466e-109">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0466e-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="0466e-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="0466e-110">Remarks</span></span>

<span data-ttu-id="0466e-111">Il pin di input chiama questo metodo dal proprio metodo [**CRendererInputPin:: inactive**](crendererinputpin-inactive.md) .</span><span class="sxs-lookup"><span data-stu-id="0466e-111">The input pin calls this method from its own [**CRendererInputPin::Inactive**](crendererinputpin-inactive.md) method.</span></span> <span data-ttu-id="0466e-112">Il filtro chiama il metodo [**CBaseRenderer:: ClearPendingSample**](cbaserenderer-clearpendingsample.md) per rilasciare l'esempio più recente.</span><span class="sxs-lookup"><span data-stu-id="0466e-112">The filter calls the [**CBaseRenderer::ClearPendingSample**](cbaserenderer-clearpendingsample.md) method to release the most recent sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="0466e-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0466e-113">Requirements</span></span>



| <span data-ttu-id="0466e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0466e-114">Requirement</span></span> | <span data-ttu-id="0466e-115">Valore</span><span class="sxs-lookup"><span data-stu-id="0466e-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0466e-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0466e-116">Header</span></span><br/>  | <dl> <span data-ttu-id="0466e-117"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0466e-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0466e-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="0466e-118">Library</span></span><br/> | <dl> <span data-ttu-id="0466e-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0466e-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0466e-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0466e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0466e-121">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="0466e-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




