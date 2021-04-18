---
description: Il metodo NewSegment notifica al filtro che gli esempi di supporti ricevuti dopo questa chiamata vengono raggruppati come un segmento.
ms.assetid: 78ddaac7-9c1f-47b6-835d-dd16b1f5b01f
title: Metodo CTransformFilter. NewSegment (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0fd046288886d3e7619419dd591dd94310f56020
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331133"
---
# <a name="ctransformfilternewsegment-method"></a><span data-ttu-id="f8478-103">CTransformFilter. NewSegment, metodo</span><span class="sxs-lookup"><span data-stu-id="f8478-103">CTransformFilter.NewSegment method</span></span>

<span data-ttu-id="f8478-104">Il `NewSegment` metodo notifica al filtro che gli esempi di supporti ricevuti dopo questa chiamata vengono raggruppati come segmento.</span><span class="sxs-lookup"><span data-stu-id="f8478-104">The `NewSegment` method notifies the filter that media samples received after this call are grouped as a segment.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8478-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f8478-105">Syntax</span></span>


```C++
virtual HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a><span data-ttu-id="f8478-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f8478-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8478-107">*tStart*</span><span class="sxs-lookup"><span data-stu-id="f8478-107">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="f8478-108">Ora di inizio del segmento rispetto all'origine originale.</span><span class="sxs-lookup"><span data-stu-id="f8478-108">Start time of the segment, relative to the original source.</span></span>

</dd> <dt>

<span data-ttu-id="f8478-109">*tStop*</span><span class="sxs-lookup"><span data-stu-id="f8478-109">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="f8478-110">Ora di arresto del segmento rispetto all'origine originale.</span><span class="sxs-lookup"><span data-stu-id="f8478-110">Stop time of the segment, relative to the original source.</span></span>

</dd> <dt>

<span data-ttu-id="f8478-111">*dRate*</span><span class="sxs-lookup"><span data-stu-id="f8478-111">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="f8478-112">Velocità di elaborazione del segmento.</span><span class="sxs-lookup"><span data-stu-id="f8478-112">Rate at which the segment should be processed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8478-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f8478-113">Return value</span></span>

<span data-ttu-id="f8478-114">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f8478-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8478-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="f8478-115">Remarks</span></span>

<span data-ttu-id="f8478-116">Il metodo [**CTransformInputPin:: NewSegment**](ctransforminputpin-newsegment.md) del PIN di input chiama questo metodo.</span><span class="sxs-lookup"><span data-stu-id="f8478-116">The input pin's [**CTransformInputPin::NewSegment**](ctransforminputpin-newsegment.md) method calls this method.</span></span> <span data-ttu-id="f8478-117">Questo metodo recapita la `NewSegment` chiamata al pin di input downstream.</span><span class="sxs-lookup"><span data-stu-id="f8478-117">This method delivers the `NewSegment` call to the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8478-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8478-118">Requirements</span></span>



| <span data-ttu-id="f8478-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8478-119">Requirement</span></span> | <span data-ttu-id="f8478-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f8478-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8478-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f8478-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f8478-122"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8478-122"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f8478-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="f8478-123">Library</span></span><br/> | <dl> <span data-ttu-id="f8478-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f8478-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8478-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f8478-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8478-126">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="f8478-126">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




