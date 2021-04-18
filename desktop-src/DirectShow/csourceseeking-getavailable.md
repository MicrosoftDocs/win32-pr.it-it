---
description: "Il metodo GetAvailable recupera l'intervallo di tempo in cui la ricerca è efficiente. Questo metodo implementa il metodo IMediaSeeking:: GetAvailable."
ms.assetid: 2a7b6cdb-47c3-4aeb-89ff-ea968c6a809b
title: Metodo CSourceSeeking. GetAvailable (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bc661d81c49798b6fe06dc569b680e5f9839e5a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329045"
---
# <a name="csourceseekinggetavailable-method"></a><span data-ttu-id="fe4d3-104">Metodo CSourceSeeking. GetAvailable</span><span class="sxs-lookup"><span data-stu-id="fe4d3-104">CSourceSeeking.GetAvailable method</span></span>

<span data-ttu-id="fe4d3-105">Il `GetAvailable` metodo recupera l'intervallo di tempo in cui la ricerca è efficiente.</span><span class="sxs-lookup"><span data-stu-id="fe4d3-105">The `GetAvailable` method retrieves the range of times in which seeking is efficient.</span></span> <span data-ttu-id="fe4d3-106">Questo metodo implementa il metodo [**IMediaSeeking:: GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) .</span><span class="sxs-lookup"><span data-stu-id="fe4d3-106">This method implements the [**IMediaSeeking::GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe4d3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe4d3-107">Syntax</span></span>


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a><span data-ttu-id="fe4d3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe4d3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe4d3-109">*pEarliest*</span><span class="sxs-lookup"><span data-stu-id="fe4d3-109">*pEarliest*</span></span> 
</dt> <dd>

<span data-ttu-id="fe4d3-110">Puntatore a una variabile che riceve la prima ora per una ricerca efficiente.</span><span class="sxs-lookup"><span data-stu-id="fe4d3-110">Pointer to a variable that receives the earliest time for efficient seeking.</span></span> <span data-ttu-id="fe4d3-111">La variabile è impostata su zero.</span><span class="sxs-lookup"><span data-stu-id="fe4d3-111">The variable is set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="fe4d3-112">*Piatto*</span><span class="sxs-lookup"><span data-stu-id="fe4d3-112">*pLatest*</span></span> 
</dt> <dd>

<span data-ttu-id="fe4d3-113">Puntatore a una variabile che riceve l'ora più recente per una ricerca efficiente.</span><span class="sxs-lookup"><span data-stu-id="fe4d3-113">Pointer to a variable that receives the latest time for efficient seeking.</span></span> <span data-ttu-id="fe4d3-114">La variabile è impostata sul valore della variabile membro [**CSourceSeeking:: m \_ rtDuration**](csourceseeking-m-rtduration.md) .</span><span class="sxs-lookup"><span data-stu-id="fe4d3-114">The variable is set to the value of the [**CSourceSeeking::m\_rtDuration**](csourceseeking-m-rtduration.md) member variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe4d3-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fe4d3-115">Return value</span></span>

<span data-ttu-id="fe4d3-116">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fe4d3-116">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe4d3-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe4d3-117">Requirements</span></span>



| <span data-ttu-id="fe4d3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe4d3-118">Requirement</span></span> | <span data-ttu-id="fe4d3-119">Valore</span><span class="sxs-lookup"><span data-stu-id="fe4d3-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe4d3-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fe4d3-120">Header</span></span><br/>  | <dl> <span data-ttu-id="fe4d3-121"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fe4d3-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fe4d3-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="fe4d3-122">Library</span></span><br/> | <dl> <span data-ttu-id="fe4d3-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="fe4d3-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe4d3-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe4d3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe4d3-125">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="fe4d3-125">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




