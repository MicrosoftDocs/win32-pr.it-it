---
description: 'Il metodo NewSegment notifica al pin che gli esempi di supporti ricevuti dopo questa chiamata vengono raggruppati come un segmento. Implementa il metodo IPin:: NewSegment.'
ms.assetid: e334d5a7-0398-496c-882c-bf73e6545867
title: Metodo CBasePin. NewSegment (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f128ce8cb2fee5479efeddd5932d0392b92a6fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328511"
---
# <a name="cbasepinnewsegment-method"></a><span data-ttu-id="9cc6c-104">CBasePin. NewSegment, metodo</span><span class="sxs-lookup"><span data-stu-id="9cc6c-104">CBasePin.NewSegment method</span></span>

<span data-ttu-id="9cc6c-105">Il `NewSegment` metodo notifica al pin che gli esempi di supporti ricevuti dopo questa chiamata vengono raggruppati come segmento.</span><span class="sxs-lookup"><span data-stu-id="9cc6c-105">The `NewSegment` method notifies the pin that media samples received after this call are grouped as a segment.</span></span> <span data-ttu-id="9cc6c-106">Implementa il metodo [**Ipin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) .</span><span class="sxs-lookup"><span data-stu-id="9cc6c-106">Implements the [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cc6c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9cc6c-107">Syntax</span></span>


```C++
HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a><span data-ttu-id="9cc6c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9cc6c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cc6c-109">*tStart*</span><span class="sxs-lookup"><span data-stu-id="9cc6c-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="9cc6c-110">Posizione iniziale del supporto del segmento, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="9cc6c-110">Starting media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="9cc6c-111">*tStop*</span><span class="sxs-lookup"><span data-stu-id="9cc6c-111">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="9cc6c-112">Posizione media finale del segmento, in unità da 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="9cc6c-112">End media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="9cc6c-113">*dRate*</span><span class="sxs-lookup"><span data-stu-id="9cc6c-113">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="9cc6c-114">Velocità di elaborazione del segmento, espresso come percentuale della frequenza originale.</span><span class="sxs-lookup"><span data-stu-id="9cc6c-114">Rate at which this segment should be processed, as a percentage of the original rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cc6c-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9cc6c-115">Return value</span></span>

<span data-ttu-id="9cc6c-116">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9cc6c-116">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cc6c-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="9cc6c-117">Remarks</span></span>

<span data-ttu-id="9cc6c-118">Questo metodo imposta le variabili membro [**CBasePin:: m \_ tStart**](cbasepin-m-tstart.md), [**CBasePin:: m \_ tStop**](cbasepin-m-tstop.md)e [**CBasePin:: m \_ drate**](cbasepin-m-drate.md) .</span><span class="sxs-lookup"><span data-stu-id="9cc6c-118">This method sets the [**CBasePin::m\_tStart**](cbasepin-m-tstart.md), [**CBasePin::m\_tStop**](cbasepin-m-tstop.md), and [**CBasePin::m\_dRate**](cbasepin-m-drate.md) member variables.</span></span> <span data-ttu-id="9cc6c-119">Nella classe derivata eseguire l'override di questo metodo per passare la notifica downstream.</span><span class="sxs-lookup"><span data-stu-id="9cc6c-119">In your derived class, override this method to pass the notification downstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cc6c-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9cc6c-120">Requirements</span></span>



| <span data-ttu-id="9cc6c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cc6c-121">Requirement</span></span> | <span data-ttu-id="9cc6c-122">Valore</span><span class="sxs-lookup"><span data-stu-id="9cc6c-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cc6c-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9cc6c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="9cc6c-124"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9cc6c-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9cc6c-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="9cc6c-125">Library</span></span><br/> | <dl> <span data-ttu-id="9cc6c-126"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9cc6c-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cc6c-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9cc6c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cc6c-128">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="9cc6c-128">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




