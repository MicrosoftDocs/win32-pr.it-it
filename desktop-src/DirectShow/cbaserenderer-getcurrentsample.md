---
description: Il metodo GetCurrentSample recupera l'esempio corrente.
ms.assetid: cfdc66e3-7d32-47b7-87f6-99dd9513c93b
title: Metodo CBaseRenderer. GetCurrentSample (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetCurrentSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 48c42ff02b22d30138fcad7d1e8af5e57a391b99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329381"
---
# <a name="cbaserenderergetcurrentsample-method"></a><span data-ttu-id="743e8-103">CBaseRenderer. GetCurrentSample, metodo</span><span class="sxs-lookup"><span data-stu-id="743e8-103">CBaseRenderer.GetCurrentSample method</span></span>

<span data-ttu-id="743e8-104">Il `GetCurrentSample` metodo recupera l'esempio corrente.</span><span class="sxs-lookup"><span data-stu-id="743e8-104">The `GetCurrentSample` method retrieves the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="743e8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="743e8-105">Syntax</span></span>


```C++
virtual IMediaSample* GetCurrentSample();
```



## <a name="parameters"></a><span data-ttu-id="743e8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="743e8-106">Parameters</span></span>

<span data-ttu-id="743e8-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="743e8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="743e8-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="743e8-108">Return value</span></span>

<span data-ttu-id="743e8-109">Restituisce un puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio oppure **null** se non è disponibile alcun campione.</span><span class="sxs-lookup"><span data-stu-id="743e8-109">Returns a pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface, or **NULL** if no sample is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="743e8-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="743e8-110">Remarks</span></span>

<span data-ttu-id="743e8-111">A meno che il metodo non restituisca **null**, il metodo chiama **AddRef** sul puntatore [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) prima di restituirlo.</span><span class="sxs-lookup"><span data-stu-id="743e8-111">Unless the method returns **NULL**, the method calls **AddRef** on the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) pointer before returning it.</span></span> <span data-ttu-id="743e8-112">Il chiamante deve rilasciare il puntatore.</span><span class="sxs-lookup"><span data-stu-id="743e8-112">The caller must release the pointer.</span></span> <span data-ttu-id="743e8-113">In modo implicito, è necessario assegnare il valore restituito a una variabile, in modo che sia possibile rilasciarlo in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="743e8-113">(By implication, you must assign the return value to a variable, so that you can release it later.)</span></span>

## <a name="requirements"></a><span data-ttu-id="743e8-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="743e8-114">Requirements</span></span>



| <span data-ttu-id="743e8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="743e8-115">Requirement</span></span> | <span data-ttu-id="743e8-116">Valore</span><span class="sxs-lookup"><span data-stu-id="743e8-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="743e8-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="743e8-117">Header</span></span><br/>  | <dl> <span data-ttu-id="743e8-118"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="743e8-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="743e8-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="743e8-119">Library</span></span><br/> | <dl> <span data-ttu-id="743e8-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="743e8-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="743e8-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="743e8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="743e8-122">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="743e8-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




