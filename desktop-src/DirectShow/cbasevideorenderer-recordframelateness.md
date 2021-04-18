---
description: Il metodo RecordFrameLateness registra il momento in cui si è verificato il rendering e raccoglie le statistiche per la pagina delle proprietà.
ms.assetid: 9d4b90d7-b529-40cc-a0fd-6635163fb7dd
title: Metodo CBaseVideoRenderer. RecordFrameLateness (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.RecordFrameLateness
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10ae7069ceedbe43f9614ea3fd1c7c901d7023cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325360"
---
# <a name="cbasevideorendererrecordframelateness-method"></a><span data-ttu-id="69e55-103">CBaseVideoRenderer. RecordFrameLateness, metodo</span><span class="sxs-lookup"><span data-stu-id="69e55-103">CBaseVideoRenderer.RecordFrameLateness method</span></span>

<span data-ttu-id="69e55-104">Il `RecordFrameLateness` metodo registra il momento in cui si è verificato il rendering e raccoglie le statistiche per la pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="69e55-104">The `RecordFrameLateness` method records how timely the rendering occurred and gathers statistics for the property page.</span></span>

## <a name="syntax"></a><span data-ttu-id="69e55-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="69e55-105">Syntax</span></span>


```C++
virtual void RecordFrameLateness(
   int trLate,
   int trFrame
);
```



## <a name="parameters"></a><span data-ttu-id="69e55-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="69e55-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69e55-107">*trLate*</span><span class="sxs-lookup"><span data-stu-id="69e55-107">*trLate*</span></span> 
</dt> <dd>

<span data-ttu-id="69e55-108">Valore che indica la latenza dell'esempio oltre il tempo di scadenza, in unità di tempo di riferimento.</span><span class="sxs-lookup"><span data-stu-id="69e55-108">Value indicating how late the sample was beyond its due time, in reference time units.</span></span>

</dd> <dt>

<span data-ttu-id="69e55-109">*trFrame*</span><span class="sxs-lookup"><span data-stu-id="69e55-109">*trFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="69e55-110">Tempo di interframe, in unità di tempo di riferimento.</span><span class="sxs-lookup"><span data-stu-id="69e55-110">Interframe time, in reference time units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69e55-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="69e55-111">Return value</span></span>

<span data-ttu-id="69e55-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="69e55-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="69e55-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69e55-113">Requirements</span></span>



| <span data-ttu-id="69e55-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="69e55-114">Requirement</span></span> | <span data-ttu-id="69e55-115">Valore</span><span class="sxs-lookup"><span data-stu-id="69e55-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69e55-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="69e55-116">Header</span></span><br/>  | <dl> <span data-ttu-id="69e55-117"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="69e55-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="69e55-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="69e55-118">Library</span></span><br/> | <dl> <span data-ttu-id="69e55-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="69e55-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69e55-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="69e55-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69e55-121">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="69e55-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




