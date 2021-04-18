---
description: 'Il metodo serate imposta la velocità di riproduzione. Questo metodo implementa il metodo IMediaSeeking:: SetValue.'
ms.assetid: 954e2381-207a-47d9-a0a5-87dc325f52b4
title: Metodo CSourceSeeking. serate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 718a38f3eff9cc1647d09cf142db784f53e4c755
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328483"
---
# <a name="csourceseekingsetrate-method"></a><span data-ttu-id="359c4-104">CSourceSeeking. serate (metodo)</span><span class="sxs-lookup"><span data-stu-id="359c4-104">CSourceSeeking.SetRate method</span></span>

<span data-ttu-id="359c4-105">Il `SetRate` metodo imposta la velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="359c4-105">The `SetRate` method sets the playback rate.</span></span> <span data-ttu-id="359c4-106">Questo metodo implementa il metodo [**IMediaSeeking::**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) SetValue.</span><span class="sxs-lookup"><span data-stu-id="359c4-106">This method implements the [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="359c4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="359c4-107">Syntax</span></span>


```C++
HRESULT SetRate(
   double dRate
);
```



## <a name="parameters"></a><span data-ttu-id="359c4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="359c4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="359c4-109">*dRate*</span><span class="sxs-lookup"><span data-stu-id="359c4-109">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="359c4-110">Velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="359c4-110">Playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="359c4-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="359c4-111">Return value</span></span>

<span data-ttu-id="359c4-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="359c4-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="359c4-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="359c4-113">Remarks</span></span>

<span data-ttu-id="359c4-114">Questo metodo aggiorna il valore della variabile membro [**CSourceSeeking:: m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) e quindi chiama il metodo virtuale pure [**CSourceSeeking:: changerate**](csourceseeking-changerate.md).</span><span class="sxs-lookup"><span data-stu-id="359c4-114">This method updates the value of the [**CSourceSeeking::m\_dRateSeeking**](csourceseeking-m-drateseeking.md) member variable, and then calls the pure virtual method [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md).</span></span> <span data-ttu-id="359c4-115">Il metodo non convalida il parametro *drate* .</span><span class="sxs-lookup"><span data-stu-id="359c4-115">The method does not validate the *dRate* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="359c4-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="359c4-116">Requirements</span></span>



| <span data-ttu-id="359c4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="359c4-117">Requirement</span></span> | <span data-ttu-id="359c4-118">Valore</span><span class="sxs-lookup"><span data-stu-id="359c4-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="359c4-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="359c4-119">Header</span></span><br/>  | <dl> <span data-ttu-id="359c4-120"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="359c4-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="359c4-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="359c4-121">Library</span></span><br/> | <dl> <span data-ttu-id="359c4-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="359c4-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="359c4-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="359c4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="359c4-124">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="359c4-124">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




