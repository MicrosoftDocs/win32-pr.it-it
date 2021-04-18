---
description: Il metodo inattivo arresta il thread di lavoro che estrae i dati dal pin di output. Questo metodo consente inoltre di eseguire il commit dell'allocatore.
ms.assetid: 90b91686-b9a8-4196-b559-de924334f11c
title: Metodo CPullPin. Inactive (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f32084428a36032152d3c3297b1fc9419e51cb3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331165"
---
# <a name="cpullpininactive-method"></a><span data-ttu-id="b5971-104">Metodo CPullPin. Inactive</span><span class="sxs-lookup"><span data-stu-id="b5971-104">CPullPin.Inactive method</span></span>

<span data-ttu-id="b5971-105">Il `Inactive` metodo arresta il thread di lavoro che estrae i dati dal pin di output.</span><span class="sxs-lookup"><span data-stu-id="b5971-105">The `Inactive` method shuts down the worker thread that pulls data from the output pin.</span></span> <span data-ttu-id="b5971-106">Questo metodo consente inoltre di eseguire il commit dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="b5971-106">This method also decommits the allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5971-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5971-107">Syntax</span></span>


```C++
HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="b5971-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5971-108">Parameters</span></span>

<span data-ttu-id="b5971-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="b5971-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b5971-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5971-110">Return value</span></span>

<span data-ttu-id="b5971-111">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b5971-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5971-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="b5971-112">Remarks</span></span>

<span data-ttu-id="b5971-113">Chiamare questo metodo quando il filtro proprietario diventa inattivo.</span><span class="sxs-lookup"><span data-stu-id="b5971-113">Call this method when the owning filter becomes inactive.</span></span> <span data-ttu-id="b5971-114">Se il pin di input deriva da [**CBasePin**](cbasepin.md), eseguire l'override del metodo [**CBasePin:: inactive**](cbasepin-inactive.md) .</span><span class="sxs-lookup"><span data-stu-id="b5971-114">(If your input pin derives from [**CBasePin**](cbasepin.md), override the [**CBasePin::Inactive**](cbasepin-inactive.md) method.)</span></span>

## <a name="requirements"></a><span data-ttu-id="b5971-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5971-115">Requirements</span></span>



| <span data-ttu-id="b5971-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5971-116">Requirement</span></span> | <span data-ttu-id="b5971-117">Valore</span><span class="sxs-lookup"><span data-stu-id="b5971-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5971-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b5971-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b5971-119"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5971-119"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="b5971-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="b5971-120">Library</span></span><br/> | <dl> <span data-ttu-id="b5971-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b5971-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5971-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5971-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5971-123">**Classe CPullPin**</span><span class="sxs-lookup"><span data-stu-id="b5971-123">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




