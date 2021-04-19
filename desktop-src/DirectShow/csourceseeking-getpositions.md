---
description: 'Il metodo GetPositions recupera la posizione corrente e la posizione di arresto. Questo metodo implementa il metodo IMediaSeeking:: GetPositions.'
ms.assetid: f577b052-669b-457d-beab-94f574fef08d
title: Metodo CSourceSeeking. GetPositions (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8d95013b12d1ee41867ac73920ca1f9b1ca0bdca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329505"
---
# <a name="csourceseekinggetpositions-method"></a><span data-ttu-id="dbced-104">Metodo CSourceSeeking. GetPositions</span><span class="sxs-lookup"><span data-stu-id="dbced-104">CSourceSeeking.GetPositions method</span></span>

<span data-ttu-id="dbced-105">Il `GetPositions` metodo recupera la posizione corrente e la posizione di arresto.</span><span class="sxs-lookup"><span data-stu-id="dbced-105">The `GetPositions` method retrieves the current position and the stop position.</span></span> <span data-ttu-id="dbced-106">Questo metodo implementa il metodo [**IMediaSeeking:: GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) .</span><span class="sxs-lookup"><span data-stu-id="dbced-106">This method implements the [**IMediaSeeking::GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbced-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dbced-107">Syntax</span></span>


```C++
HRESULT GetPositions(
   LONGLONG *pCurrent,
   LONGLONG *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="dbced-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="dbced-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbced-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="dbced-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="dbced-110">Puntatore a una variabile che riceve la posizione iniziale.</span><span class="sxs-lookup"><span data-stu-id="dbced-110">Pointer to a variable that receives the start position.</span></span>

</dd> <dt>

<span data-ttu-id="dbced-111">*pStop*</span><span class="sxs-lookup"><span data-stu-id="dbced-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="dbced-112">Puntatore a una variabile che riceve la posizione di arresto.</span><span class="sxs-lookup"><span data-stu-id="dbced-112">Pointer to a variable that receives the stop position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbced-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dbced-113">Return value</span></span>

<span data-ttu-id="dbced-114">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dbced-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbced-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="dbced-115">Remarks</span></span>

<span data-ttu-id="dbced-116">Per il parametro *pCurrent* , questo metodo restituisce il valore della variabile membro [**\_ rtStart di CSourceSeeking:: m**](csourceseeking-m-rtstart.md) , che rappresenta il tempo di ricerca più recente, non la posizione corrente del flusso.</span><span class="sxs-lookup"><span data-stu-id="dbced-116">For the *pCurrent* parameter, this method returns the value of the [**CSourceSeeking::m\_rtStart**](csourceseeking-m-rtstart.md) member variable, which represents the latest seek time, not the current streaming position.</span></span> <span data-ttu-id="dbced-117">Tuttavia, quando un'applicazione chiama **IMediaSeeking:: GetPositions** tramite Filter Graph Manager, i valori provengono in genere da un filtro renderer, non da un filtro di origine.</span><span class="sxs-lookup"><span data-stu-id="dbced-117">However, when an application calls **IMediaSeeking::GetPositions** through the filter graph manager, the values typically come from a renderer filter, not a source filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbced-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dbced-118">Requirements</span></span>



| <span data-ttu-id="dbced-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbced-119">Requirement</span></span> | <span data-ttu-id="dbced-120">Valore</span><span class="sxs-lookup"><span data-stu-id="dbced-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbced-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dbced-121">Header</span></span><br/>  | <dl> <span data-ttu-id="dbced-122"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dbced-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dbced-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="dbced-123">Library</span></span><br/> | <dl> <span data-ttu-id="dbced-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="dbced-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbced-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dbced-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbced-126">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="dbced-126">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




