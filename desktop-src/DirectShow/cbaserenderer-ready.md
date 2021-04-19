---
description: Il metodo Ready segnala che una transizione di stato è stata completata.
ms.assetid: 01328281-cf25-43fd-9f9c-e55fccbac217
title: Metodo CBaseRenderer. Ready (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Ready
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a7f70ec258fde7f6208d44c35ca2c284f99e0a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333339"
---
# <a name="cbaserendererready-method"></a><span data-ttu-id="aae16-103">Metodo CBaseRenderer. Ready</span><span class="sxs-lookup"><span data-stu-id="aae16-103">CBaseRenderer.Ready method</span></span>

<span data-ttu-id="aae16-104">Il `Ready` metodo segnala che una transizione di stato è stata completata.</span><span class="sxs-lookup"><span data-stu-id="aae16-104">The `Ready` method signals that a state transition is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="aae16-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aae16-105">Syntax</span></span>


```C++
void Ready();
```



## <a name="parameters"></a><span data-ttu-id="aae16-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="aae16-106">Parameters</span></span>

<span data-ttu-id="aae16-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="aae16-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="aae16-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aae16-108">Return value</span></span>

<span data-ttu-id="aae16-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="aae16-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aae16-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="aae16-110">Remarks</span></span>

<span data-ttu-id="aae16-111">Questo metodo fa sì che il metodo [**CBaseRenderer:: GetState**](cbaserenderer-getstate.md) restituisca S \_ OK, a indicare che il filtro ha completato la transizione allo stato corrente.</span><span class="sxs-lookup"><span data-stu-id="aae16-111">This method causes the [**CBaseRenderer::GetState**](cbaserenderer-getstate.md) method to return S\_OK, which indicates that the filter has completed the transition to its current state.</span></span> <span data-ttu-id="aae16-112">Il filtro chiama questo metodo ogni volta che viene completata una transizione di stato.</span><span class="sxs-lookup"><span data-stu-id="aae16-112">The filter calls this method whenever it completes a state transition.</span></span>

## <a name="requirements"></a><span data-ttu-id="aae16-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aae16-113">Requirements</span></span>



| <span data-ttu-id="aae16-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="aae16-114">Requirement</span></span> | <span data-ttu-id="aae16-115">Valore</span><span class="sxs-lookup"><span data-stu-id="aae16-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aae16-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aae16-116">Header</span></span><br/>  | <dl> <span data-ttu-id="aae16-117"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aae16-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="aae16-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="aae16-118">Library</span></span><br/> | <dl> <span data-ttu-id="aae16-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="aae16-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aae16-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aae16-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aae16-121">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="aae16-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> <dt>

[<span data-ttu-id="aae16-122">**CBaseRenderer::CheckReady**</span><span class="sxs-lookup"><span data-stu-id="aae16-122">**CBaseRenderer::CheckReady**</span></span>](cbaserenderer-checkready.md)
</dt> <dt>

[<span data-ttu-id="aae16-123">**CBaseRenderer:: nobattistrada**</span><span class="sxs-lookup"><span data-stu-id="aae16-123">**CBaseRenderer::NotReady**</span></span>](cbaserenderer-notready.md)
</dt> </dl>

 

 




