---
description: "Metodo CSourceSeeking.GetAvailable: il metodo GetAvailable recupera l'intervallo di volte in cui la ricerca è efficiente. Questo metodo implementa il metodo IMediaSeeking::GetAvailable."
ms.assetid: 2a7b6cdb-47c3-4aeb-89ff-ea968c6a809b
title: Metodo CSourceSeeking.GetAvailable (Ctlutil.h)
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
ms.openlocfilehash: f24bc667eec4f5b21c90415e4721aa8cf0a0ad4c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085239"
---
# <a name="csourceseekinggetavailable-method"></a><span data-ttu-id="60d19-104">Metodo CSourceSeeking.GetAvailable</span><span class="sxs-lookup"><span data-stu-id="60d19-104">CSourceSeeking.GetAvailable method</span></span>

<span data-ttu-id="60d19-105">Il `GetAvailable` metodo recupera l'intervallo di volte in cui la ricerca è efficiente.</span><span class="sxs-lookup"><span data-stu-id="60d19-105">The `GetAvailable` method retrieves the range of times in which seeking is efficient.</span></span> <span data-ttu-id="60d19-106">Questo metodo implementa il [**metodo IMediaSeeking::GetAvailable.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable)</span><span class="sxs-lookup"><span data-stu-id="60d19-106">This method implements the [**IMediaSeeking::GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="60d19-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60d19-107">Syntax</span></span>


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a><span data-ttu-id="60d19-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="60d19-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60d19-109">*pEarliest*</span><span class="sxs-lookup"><span data-stu-id="60d19-109">*pEarliest*</span></span> 
</dt> <dd>

<span data-ttu-id="60d19-110">Puntatore a una variabile che riceve l'ora meno recente per una ricerca efficiente.</span><span class="sxs-lookup"><span data-stu-id="60d19-110">Pointer to a variable that receives the earliest time for efficient seeking.</span></span> <span data-ttu-id="60d19-111">La variabile è impostata su zero.</span><span class="sxs-lookup"><span data-stu-id="60d19-111">The variable is set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="60d19-112">*pLatest*</span><span class="sxs-lookup"><span data-stu-id="60d19-112">*pLatest*</span></span> 
</dt> <dd>

<span data-ttu-id="60d19-113">Puntatore a una variabile che riceve l'ora più recente per una ricerca efficiente.</span><span class="sxs-lookup"><span data-stu-id="60d19-113">Pointer to a variable that receives the latest time for efficient seeking.</span></span> <span data-ttu-id="60d19-114">La variabile è impostata sul valore della variabile membro [**CSourceSeeking::m \_ rtDuration.**](csourceseeking-m-rtduration.md)</span><span class="sxs-lookup"><span data-stu-id="60d19-114">The variable is set to the value of the [**CSourceSeeking::m\_rtDuration**](csourceseeking-m-rtduration.md) member variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60d19-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="60d19-115">Return value</span></span>

<span data-ttu-id="60d19-116">Restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="60d19-116">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="60d19-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60d19-117">Requirements</span></span>



| <span data-ttu-id="60d19-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="60d19-118">Requirement</span></span> | <span data-ttu-id="60d19-119">Valore</span><span class="sxs-lookup"><span data-stu-id="60d19-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60d19-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="60d19-120">Header</span></span><br/>  | <dl> <span data-ttu-id="60d19-121"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="60d19-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="60d19-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="60d19-122">Library</span></span><br/> | <dl> <span data-ttu-id="60d19-123"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="60d19-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60d19-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60d19-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60d19-125">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="60d19-125">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




