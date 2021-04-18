---
description: Il metodo SetConfigInfo specifica il puntatore IGraphConfig e l'evento Stop.
ms.assetid: 938fe8be-5622-4954-9ba3-31fc68fbfa31
title: Metodo CDynamicOutputPin. SetConfigInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.SetConfigInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b0c14342a629a38a878649ac59d8f1f814874f12
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327543"
---
# <a name="cdynamicoutputpinsetconfiginfo-method"></a><span data-ttu-id="b2ca8-103">CDynamicOutputPin. SetConfigInfo, metodo</span><span class="sxs-lookup"><span data-stu-id="b2ca8-103">CDynamicOutputPin.SetConfigInfo method</span></span>

<span data-ttu-id="b2ca8-104">Il `SetConfigInfo` metodo specifica il puntatore [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) e l'evento Stop.</span><span class="sxs-lookup"><span data-stu-id="b2ca8-104">The `SetConfigInfo` method specifies the [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) pointer and the stop event.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2ca8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2ca8-105">Syntax</span></span>


```C++
void SetConfigInfo(
   IGraphConfig *pGraphConfig,
   HANDLE       hStopEvent
);
```



## <a name="parameters"></a><span data-ttu-id="b2ca8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b2ca8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2ca8-107">*pGraphConfig*</span><span class="sxs-lookup"><span data-stu-id="b2ca8-107">*pGraphConfig*</span></span> 
</dt> <dd>

<span data-ttu-id="b2ca8-108">Puntatore all'interfaccia [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) o **null**.</span><span class="sxs-lookup"><span data-stu-id="b2ca8-108">Pointer to the [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) interface, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b2ca8-109">*hStopEvent*</span><span class="sxs-lookup"><span data-stu-id="b2ca8-109">*hStopEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="b2ca8-110">Handle per un evento segnalato quando il filtro viene arrestato o **null**.</span><span class="sxs-lookup"><span data-stu-id="b2ca8-110">Handle to an event that is signaled when the filter stops, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2ca8-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b2ca8-111">Return value</span></span>

<span data-ttu-id="b2ca8-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="b2ca8-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2ca8-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2ca8-113">Remarks</span></span>

<span data-ttu-id="b2ca8-114">Il filtro deve chiamare questo metodo quando viene aggiunto al grafo del filtro.</span><span class="sxs-lookup"><span data-stu-id="b2ca8-114">The filter must call this method when it joins the filter graph.</span></span> <span data-ttu-id="b2ca8-115">Filter Graph Manager supporta **IGraphConfig**.</span><span class="sxs-lookup"><span data-stu-id="b2ca8-115">The filter graph manager supports **IGraphConfig**.</span></span> <span data-ttu-id="b2ca8-116">Per il parametro *hStopEvent* , creare un evento di reimpostazione manuale.</span><span class="sxs-lookup"><span data-stu-id="b2ca8-116">For the *hStopEvent* parameter, create a manual-reset event.</span></span> <span data-ttu-id="b2ca8-117">Quando il filtro lascia il grafico del filtro, chiamare nuovamente questo metodo con **null** per entrambi i parametri.</span><span class="sxs-lookup"><span data-stu-id="b2ca8-117">When the filter leaves the filter graph, call this method again with **NULL** for both parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2ca8-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2ca8-118">Requirements</span></span>



| <span data-ttu-id="b2ca8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2ca8-119">Requirement</span></span> | <span data-ttu-id="b2ca8-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b2ca8-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2ca8-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b2ca8-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b2ca8-122"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b2ca8-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b2ca8-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="b2ca8-123">Library</span></span><br/> | <dl> <span data-ttu-id="b2ca8-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b2ca8-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2ca8-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2ca8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2ca8-126">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="b2ca8-126">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




