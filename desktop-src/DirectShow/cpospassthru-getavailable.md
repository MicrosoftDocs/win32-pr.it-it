---
description: "Metodo CPosPassThru.GetAvailable: il metodo GetAvailable recupera l'intervallo di tempo in cui la ricerca è efficiente. Questo metodo implementa il metodo IMediaSeeking::GetAvailable."
ms.assetid: 5f4af41a-eb7b-4caa-97e0-aaed78467723
title: Metodo CPosPassThru.GetAvailable (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0d56827a68f4c287e5808f0d8f64b8142c31b1f4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095289"
---
# <a name="cpospassthrugetavailable-method"></a><span data-ttu-id="d523c-104">Metodo CPosPassThru.GetAvailable</span><span class="sxs-lookup"><span data-stu-id="d523c-104">CPosPassThru.GetAvailable method</span></span>

<span data-ttu-id="d523c-105">Il `GetAvailable` metodo recupera l'intervallo di volte in cui la ricerca è efficiente.</span><span class="sxs-lookup"><span data-stu-id="d523c-105">The `GetAvailable` method retrieves the range of times in which seeking is efficient.</span></span> <span data-ttu-id="d523c-106">Questo metodo implementa il [**metodo IMediaSeeking::GetAvailable.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable)</span><span class="sxs-lookup"><span data-stu-id="d523c-106">This method implements the [**IMediaSeeking::GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d523c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d523c-107">Syntax</span></span>


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a><span data-ttu-id="d523c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d523c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d523c-109">*pEarliest*</span><span class="sxs-lookup"><span data-stu-id="d523c-109">*pEarliest*</span></span> 
</dt> <dd>

<span data-ttu-id="d523c-110">Puntatore a una variabile che riceve il primo tempo per una ricerca efficiente.</span><span class="sxs-lookup"><span data-stu-id="d523c-110">Pointer to a variable that receives the earliest time for efficient seeking.</span></span>

</dd> <dt>

<span data-ttu-id="d523c-111">*pLatest*</span><span class="sxs-lookup"><span data-stu-id="d523c-111">*pLatest*</span></span> 
</dt> <dd>

<span data-ttu-id="d523c-112">Puntatore a una variabile che riceve l'ora più recente per una ricerca efficiente.</span><span class="sxs-lookup"><span data-stu-id="d523c-112">Pointer to a variable that receives the latest time for efficient seeking.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d523c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d523c-113">Return value</span></span>

<span data-ttu-id="d523c-114">Restituisce il **valore HRESULT** dal pin connesso.</span><span class="sxs-lookup"><span data-stu-id="d523c-114">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="d523c-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d523c-115">Requirements</span></span>



| <span data-ttu-id="d523c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d523c-116">Requirement</span></span> | <span data-ttu-id="d523c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d523c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d523c-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d523c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d523c-119"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="d523c-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d523c-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="d523c-120">Library</span></span><br/> | <dl> <span data-ttu-id="d523c-121"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d523c-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d523c-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d523c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d523c-123">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="d523c-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




