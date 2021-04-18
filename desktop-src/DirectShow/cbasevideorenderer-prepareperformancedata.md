---
description: Il metodo PreparePerformanceData imposta i \_ valori m trLate e m \_ trFrame del frame corrente.
ms.assetid: c4c5701b-eccd-4259-a1d1-7c5000f6b2df
title: Metodo CBaseVideoRenderer. PreparePerformanceData (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.PreparePerformanceData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 12dd61dee7416ce8ca7ac07cba62cbc769df5973
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325361"
---
# <a name="cbasevideorendererprepareperformancedata-method"></a><span data-ttu-id="eeb18-103">CBaseVideoRenderer. PreparePerformanceData, metodo</span><span class="sxs-lookup"><span data-stu-id="eeb18-103">CBaseVideoRenderer.PreparePerformanceData method</span></span>

<span data-ttu-id="eeb18-104">Il `PreparePerformanceData` metodo imposta i valori **m \_ trLate** e **m \_ trFrame** del frame corrente.</span><span class="sxs-lookup"><span data-stu-id="eeb18-104">The `PreparePerformanceData` method sets the **m\_trLate** and **m\_trFrame** values of the current frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="eeb18-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eeb18-105">Syntax</span></span>


```C++
void PreparePerformanceData(
   int trLate,
   int trFrame
);
```



## <a name="parameters"></a><span data-ttu-id="eeb18-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="eeb18-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eeb18-107">*trLate*</span><span class="sxs-lookup"><span data-stu-id="eeb18-107">*trLate*</span></span> 
</dt> <dd>

<span data-ttu-id="eeb18-108">Valore che indica la latenza dell'esempio oltre il tempo di scadenza, in unità di tempo di riferimento.</span><span class="sxs-lookup"><span data-stu-id="eeb18-108">Value indicating how late the sample was beyond its due time, in reference time units.</span></span>

</dd> <dt>

<span data-ttu-id="eeb18-109">*trFrame*</span><span class="sxs-lookup"><span data-stu-id="eeb18-109">*trFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="eeb18-110">Tempo di interframe, in unità di tempo di riferimento.</span><span class="sxs-lookup"><span data-stu-id="eeb18-110">Interframe time, in reference time units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eeb18-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eeb18-111">Return value</span></span>

<span data-ttu-id="eeb18-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="eeb18-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eeb18-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="eeb18-113">Remarks</span></span>

<span data-ttu-id="eeb18-114">Questa funzione membro imposta **m \_ trLate** sul valore di *trLate* e **m \_ trFrame** sul valore di *trFrame*.</span><span class="sxs-lookup"><span data-stu-id="eeb18-114">This member function sets **m\_trLate** to the value of *trLate* and **m\_trFrame** to the value of *trFrame*.</span></span>

<span data-ttu-id="eeb18-115">Quando la funzione membro [**CBaseVideoRenderer:: RecordFrameLateness**](cbasevideorenderer-recordframelateness.md) viene chiamata da [**CBaseVideoRenderer:: OnRenderStart**](cbasevideorenderer-onrenderstart.md) o [**CBaseVideoRenderer:: OnDirectRender**](cbasevideorenderer-ondirectrender.md), passa i valori di **m \_ trLate** e **m \_ trFrame** per l'aggiornamento delle statistiche.</span><span class="sxs-lookup"><span data-stu-id="eeb18-115">When the [**CBaseVideoRenderer::RecordFrameLateness**](cbasevideorenderer-recordframelateness.md) member function is called from either [**CBaseVideoRenderer::OnRenderStart**](cbasevideorenderer-onrenderstart.md) or [**CBaseVideoRenderer::OnDirectRender**](cbasevideorenderer-ondirectrender.md), it passes the values of **m\_trLate** and **m\_trFrame** for it to update the statistics.</span></span> <span data-ttu-id="eeb18-116">`PreparePerformanceData` viene chiamato da [**CBaseVideoRenderer:: OnWaitEnd**](cbasevideorenderer-onwaitend.md) per impostare questi valori del membro dati.</span><span class="sxs-lookup"><span data-stu-id="eeb18-116">`PreparePerformanceData` is called from [**CBaseVideoRenderer::OnWaitEnd**](cbasevideorenderer-onwaitend.md) to set these data member values.</span></span>

## <a name="requirements"></a><span data-ttu-id="eeb18-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eeb18-117">Requirements</span></span>



| <span data-ttu-id="eeb18-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="eeb18-118">Requirement</span></span> | <span data-ttu-id="eeb18-119">Valore</span><span class="sxs-lookup"><span data-stu-id="eeb18-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eeb18-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eeb18-120">Header</span></span><br/>  | <dl> <span data-ttu-id="eeb18-121"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eeb18-121"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="eeb18-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="eeb18-122">Library</span></span><br/> | <dl> <span data-ttu-id="eeb18-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="eeb18-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eeb18-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eeb18-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeb18-125">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="eeb18-125">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




