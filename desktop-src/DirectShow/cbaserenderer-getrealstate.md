---
description: Il metodo GetRealState recupera lo stato del filtro.
ms.assetid: d31c5c0b-6220-4d2e-a81a-d16b7d513c87
title: Metodo CBaseRenderer. GetRealState (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetRealState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40f2e49137a4324b14f25e4abb9b14cb919efbb9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325934"
---
# <a name="cbaserenderergetrealstate-method"></a><span data-ttu-id="a0193-103">CBaseRenderer. GetRealState, metodo</span><span class="sxs-lookup"><span data-stu-id="a0193-103">CBaseRenderer.GetRealState method</span></span>

<span data-ttu-id="a0193-104">Il `GetRealState` metodo recupera lo stato del filtro.</span><span class="sxs-lookup"><span data-stu-id="a0193-104">The `GetRealState` method retrieves the filter state.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0193-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0193-105">Syntax</span></span>


```C++
FILTER_STATE GetRealState();
```



## <a name="parameters"></a><span data-ttu-id="a0193-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0193-106">Parameters</span></span>

<span data-ttu-id="a0193-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a0193-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a0193-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0193-108">Return value</span></span>

<span data-ttu-id="a0193-109">Restituisce il valore dello [**\_ stato CBaseFilter:: m**](cbasefilter-m-state.md).</span><span class="sxs-lookup"><span data-stu-id="a0193-109">Returns the value of [**CBaseFilter::m\_State**](cbasefilter-m-state.md).</span></span> <span data-ttu-id="a0193-110">Il valore è un membro del tipo enumerato [**\_ stato filtro**](/windows/win32/api/strmif/ne-strmif-filter_state) .</span><span class="sxs-lookup"><span data-stu-id="a0193-110">The value is a member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumerated type.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0193-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0193-111">Remarks</span></span>

<span data-ttu-id="a0193-112">Questo metodo fornisce un'alternativa più semplice al metodo [**CBaseRenderer:: GetState**](cbaserenderer-getstate.md) , per uso interno.</span><span class="sxs-lookup"><span data-stu-id="a0193-112">This method provides a simpler alternative to the [**CBaseRenderer::GetState**](cbaserenderer-getstate.md) method, for internal use.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0193-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0193-113">Requirements</span></span>



| <span data-ttu-id="a0193-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0193-114">Requirement</span></span> | <span data-ttu-id="a0193-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a0193-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0193-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0193-116">Header</span></span><br/>  | <dl> <span data-ttu-id="a0193-117"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0193-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a0193-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="a0193-118">Library</span></span><br/> | <dl> <span data-ttu-id="a0193-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a0193-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0193-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0193-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0193-121">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="a0193-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




