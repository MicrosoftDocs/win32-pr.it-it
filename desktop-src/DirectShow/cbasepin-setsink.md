---
description: 'Il metodo SESINK imposta un gestore di qualità esterno. Questo metodo implementa il metodo IQualityControl:: SetValue.'
ms.assetid: 714e6839-954e-4231-824d-72a45f270f59
title: Metodo CBasePin. SESINK (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetSink
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4237e342f8f49059cab017b17a1f116ca6e2da67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327347"
---
# <a name="cbasepinsetsink-method"></a><span data-ttu-id="7aa65-104">Metodo CBasePin. SESINK</span><span class="sxs-lookup"><span data-stu-id="7aa65-104">CBasePin.SetSink method</span></span>

<span data-ttu-id="7aa65-105">Il `SetSink` metodo imposta un gestore di qualità esterno.</span><span class="sxs-lookup"><span data-stu-id="7aa65-105">The `SetSink` method sets an external quality manager.</span></span> <span data-ttu-id="7aa65-106">Questo metodo implementa il metodo [**IQualityControl::**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) SetValue.</span><span class="sxs-lookup"><span data-stu-id="7aa65-106">This method implements the [**IQualityControl::SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7aa65-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7aa65-107">Syntax</span></span>


```C++
HRESULT SetSink(
   IQualityControl *piqc
);
```



## <a name="parameters"></a><span data-ttu-id="7aa65-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7aa65-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7aa65-109">*piqc*</span><span class="sxs-lookup"><span data-stu-id="7aa65-109">*piqc*</span></span> 
</dt> <dd>

<span data-ttu-id="7aa65-110">Puntatore all'interfaccia [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) del gestore qualità.</span><span class="sxs-lookup"><span data-stu-id="7aa65-110">Pointer to the [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) interface of the quality manager.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7aa65-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7aa65-111">Return value</span></span>

<span data-ttu-id="7aa65-112">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7aa65-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="7aa65-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="7aa65-113">Remarks</span></span>

<span data-ttu-id="7aa65-114">Chiamare questo metodo per reindirizzare i messaggi di controllo di qualità a un gestore di qualità esterno.</span><span class="sxs-lookup"><span data-stu-id="7aa65-114">Call this method to redirect quality-control messages to an external quality manager.</span></span> <span data-ttu-id="7aa65-115">Per altre informazioni, vedere [gestione del controllo di qualità](quality-control-management.md).</span><span class="sxs-lookup"><span data-stu-id="7aa65-115">For more information, see [Quality-Control Management](quality-control-management.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7aa65-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7aa65-116">Requirements</span></span>



| <span data-ttu-id="7aa65-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7aa65-117">Requirement</span></span> | <span data-ttu-id="7aa65-118">Valore</span><span class="sxs-lookup"><span data-stu-id="7aa65-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7aa65-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7aa65-119">Header</span></span><br/>  | <dl> <span data-ttu-id="7aa65-120"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7aa65-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7aa65-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="7aa65-121">Library</span></span><br/> | <dl> <span data-ttu-id="7aa65-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7aa65-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7aa65-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7aa65-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7aa65-124">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="7aa65-124">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




