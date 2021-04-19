---
description: Il metodo DeliverNewSegment recapita una notifica del nuovo segmento al pin di input connesso.
ms.assetid: 304f0267-88e0-4642-98a2-68ce973bdeab
title: Metodo CBaseOutputPin. DeliverNewSegment (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverNewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3eb6d31a50095affdf38d44b69040304674ec6fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332064"
---
# <a name="cbaseoutputpindelivernewsegment-method"></a><span data-ttu-id="33a00-103">CBaseOutputPin. DeliverNewSegment, metodo</span><span class="sxs-lookup"><span data-stu-id="33a00-103">CBaseOutputPin.DeliverNewSegment method</span></span>

<span data-ttu-id="33a00-104">Il `DeliverNewSegment` Metodo recapita una notifica del nuovo segmento al pin di input connesso.</span><span class="sxs-lookup"><span data-stu-id="33a00-104">The `DeliverNewSegment` method delivers a new-segment notification to the connected input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="33a00-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="33a00-105">Syntax</span></span>


```C++
virtual HRESULT DeliverNewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a><span data-ttu-id="33a00-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="33a00-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33a00-107">*tStart*</span><span class="sxs-lookup"><span data-stu-id="33a00-107">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="33a00-108">Posizione iniziale del supporto del segmento, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="33a00-108">Starting media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="33a00-109">*tStop*</span><span class="sxs-lookup"><span data-stu-id="33a00-109">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="33a00-110">Posizione media finale del segmento, in unità da 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="33a00-110">End media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="33a00-111">*dRate*</span><span class="sxs-lookup"><span data-stu-id="33a00-111">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="33a00-112">Velocità di elaborazione del segmento, espresso come percentuale della frequenza originale.</span><span class="sxs-lookup"><span data-stu-id="33a00-112">Rate at which this segment should be processed, as a percentage of the original rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33a00-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="33a00-113">Return value</span></span>

<span data-ttu-id="33a00-114">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="33a00-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="33a00-115">I valori possibili includono quelli elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="33a00-115">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="33a00-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="33a00-116">Return code</span></span>                                                                                           | <span data-ttu-id="33a00-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33a00-117">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="33a00-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="33a00-118"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="33a00-119">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="33a00-119">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="33a00-120"><dt>**VFW \_ E \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="33a00-120"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="33a00-121">Il PIN non è connesso.</span><span class="sxs-lookup"><span data-stu-id="33a00-121">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="33a00-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="33a00-122">Remarks</span></span>

<span data-ttu-id="33a00-123">Questo metodo chiama il metodo [**Ipin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) sul pin di input.</span><span class="sxs-lookup"><span data-stu-id="33a00-123">This method calls the [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="33a00-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33a00-124">Requirements</span></span>



| <span data-ttu-id="33a00-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="33a00-125">Requirement</span></span> | <span data-ttu-id="33a00-126">Valore</span><span class="sxs-lookup"><span data-stu-id="33a00-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33a00-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="33a00-127">Header</span></span><br/>  | <dl> <span data-ttu-id="33a00-128"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33a00-128"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="33a00-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="33a00-129">Library</span></span><br/> | <dl> <span data-ttu-id="33a00-130"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="33a00-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33a00-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33a00-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33a00-132">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="33a00-132">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




