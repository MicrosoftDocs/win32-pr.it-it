---
description: 'Il metodo NewSegment notifica al pin che gli esempi di supporti ricevuti dopo questa chiamata vengono raggruppati come un segmento. Questo metodo implementa il metodo IPin:: NewSegment.'
ms.assetid: 8925b8b5-13dd-4127-82d8-96525bd4d6fc
title: Metodo CTransformInputPin. NewSegment (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 25c455fe5ec6ddf9157e991b70b468ace653daa9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329966"
---
# <a name="ctransforminputpinnewsegment-method"></a><span data-ttu-id="8b644-104">CTransformInputPin. NewSegment, metodo</span><span class="sxs-lookup"><span data-stu-id="8b644-104">CTransformInputPin.NewSegment method</span></span>

<span data-ttu-id="8b644-105">Il `NewSegment` metodo notifica al pin che gli esempi di supporti ricevuti dopo questa chiamata vengono raggruppati come segmento.</span><span class="sxs-lookup"><span data-stu-id="8b644-105">The `NewSegment` method notifies the pin that media samples received after this call are grouped as a segment.</span></span> <span data-ttu-id="8b644-106">Questo metodo implementa il metodo [**Ipin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) .</span><span class="sxs-lookup"><span data-stu-id="8b644-106">This method implements the [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b644-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8b644-107">Syntax</span></span>


```C++
HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a><span data-ttu-id="8b644-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8b644-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b644-109">*tStart*</span><span class="sxs-lookup"><span data-stu-id="8b644-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="8b644-110">Ora di inizio del segmento.</span><span class="sxs-lookup"><span data-stu-id="8b644-110">Start time of the segment.</span></span>

</dd> <dt>

<span data-ttu-id="8b644-111">*tStop*</span><span class="sxs-lookup"><span data-stu-id="8b644-111">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="8b644-112">Ora di arresto del segmento.</span><span class="sxs-lookup"><span data-stu-id="8b644-112">Stop time of the segment.</span></span>

</dd> <dt>

<span data-ttu-id="8b644-113">*dRate*</span><span class="sxs-lookup"><span data-stu-id="8b644-113">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="8b644-114">Frequenza del segmento.</span><span class="sxs-lookup"><span data-stu-id="8b644-114">Rate of the segment.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b644-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8b644-115">Return value</span></span>

<span data-ttu-id="8b644-116">Restituisce S \_ OK o un altro valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8b644-116">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b644-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="8b644-117">Remarks</span></span>

<span data-ttu-id="8b644-118">Questo metodo esegue l'override del metodo [**CBasePin:: NewSegment**](cbasepin-newsegment.md) .</span><span class="sxs-lookup"><span data-stu-id="8b644-118">This method overrides the [**CBasePin::NewSegment**](cbasepin-newsegment.md) method.</span></span> <span data-ttu-id="8b644-119">Chiama il metodo [**CTransformFilter:: NewSegment**](ctransformfilter-newsegment.md) del filtro per recapitare la chiamata downstream.</span><span class="sxs-lookup"><span data-stu-id="8b644-119">It calls the filter's [**CTransformFilter::NewSegment**](ctransformfilter-newsegment.md) method to deliver the call downstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b644-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b644-120">Requirements</span></span>



| <span data-ttu-id="8b644-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b644-121">Requirement</span></span> | <span data-ttu-id="8b644-122">Valore</span><span class="sxs-lookup"><span data-stu-id="8b644-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b644-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8b644-123">Header</span></span><br/>  | <dl> <span data-ttu-id="8b644-124"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8b644-124"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8b644-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="8b644-125">Library</span></span><br/> | <dl> <span data-ttu-id="8b644-126"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8b644-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




