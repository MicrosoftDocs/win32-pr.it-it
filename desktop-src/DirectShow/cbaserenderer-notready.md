---
description: Il metodo nobattistrada segnala che una transizione di stato non è ancora completa.
ms.assetid: 85529a22-5343-4c22-b282-31c0e7ff0f5f
title: Metodo CBaseRenderer. nobattistrada (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.NotReady
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff07303f9aa8f68ae702ed09bc3a2fd544373f6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333360"
---
# <a name="cbaserenderernotready-method"></a><span data-ttu-id="6bff0-103">CBaseRenderer. nobattistrada (metodo)</span><span class="sxs-lookup"><span data-stu-id="6bff0-103">CBaseRenderer.NotReady method</span></span>

<span data-ttu-id="6bff0-104">Il `NotReady` metodo segnala che una transizione di stato non è ancora completa.</span><span class="sxs-lookup"><span data-stu-id="6bff0-104">The `NotReady` method signals that a state transition is not yet complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bff0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6bff0-105">Syntax</span></span>


```C++
void NotReady();
```



## <a name="parameters"></a><span data-ttu-id="6bff0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6bff0-106">Parameters</span></span>

<span data-ttu-id="6bff0-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="6bff0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6bff0-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6bff0-108">Return value</span></span>

<span data-ttu-id="6bff0-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="6bff0-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bff0-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="6bff0-110">Remarks</span></span>

<span data-ttu-id="6bff0-111">Questo metodo fa sì che il metodo [**CBaseRenderer:: GetState**](cbaserenderer-getstate.md) restituisca il metodo \_ \_ intermedio di stato di VFW \_ , che indica che il filtro sta ancora passando allo stato corrente.</span><span class="sxs-lookup"><span data-stu-id="6bff0-111">This method causes the [**CBaseRenderer::GetState**](cbaserenderer-getstate.md) method to return VFW\_S\_STATE\_INTERMEDIATE, which indicates that the filter is still transitioning to its current state.</span></span> <span data-ttu-id="6bff0-112">Il filtro chiama questo metodo ogni volta che una transizione di stato è in sospeso.</span><span class="sxs-lookup"><span data-stu-id="6bff0-112">The filter calls this method whenever a state transition is pending.</span></span> <span data-ttu-id="6bff0-113">Questo errore si verifica quando il filtro viene sospeso fino a quando non riceve un campione.</span><span class="sxs-lookup"><span data-stu-id="6bff0-113">(This occurs when the filter pauses, until it receives a sample.)</span></span>

## <a name="requirements"></a><span data-ttu-id="6bff0-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6bff0-114">Requirements</span></span>



| <span data-ttu-id="6bff0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bff0-115">Requirement</span></span> | <span data-ttu-id="6bff0-116">Valore</span><span class="sxs-lookup"><span data-stu-id="6bff0-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bff0-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6bff0-117">Header</span></span><br/>  | <dl> <span data-ttu-id="6bff0-118"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6bff0-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6bff0-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="6bff0-119">Library</span></span><br/> | <dl> <span data-ttu-id="6bff0-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6bff0-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bff0-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6bff0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bff0-122">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="6bff0-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> <dt>

[<span data-ttu-id="6bff0-123">**CheckReady**</span><span class="sxs-lookup"><span data-stu-id="6bff0-123">**CheckReady**</span></span>](cbaserenderer-checkready.md)
</dt> <dt>

[<span data-ttu-id="6bff0-124">**Ready**</span><span class="sxs-lookup"><span data-stu-id="6bff0-124">**Ready**</span></span>](cbaserenderer-ready.md)
</dt> </dl>

 

 




