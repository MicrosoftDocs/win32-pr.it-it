---
description: "Il metodo GetStopPosition recupera l'ora in cui si interrompe la riproduzione rispetto alla durata del flusso. Questo metodo implementa il metodo IMediaSeeking:: GetStopPosition."
ms.assetid: 83928f62-7acc-43b9-9537-49131ed0b0d4
title: Metodo CSourceSeeking. GetStopPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetStopPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d9f61ad26c32cfeec285874edfcc26038d57b117
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329501"
---
# <a name="csourceseekinggetstopposition-method"></a><span data-ttu-id="084ff-104">CSourceSeeking. GetStopPosition, metodo</span><span class="sxs-lookup"><span data-stu-id="084ff-104">CSourceSeeking.GetStopPosition method</span></span>

<span data-ttu-id="084ff-105">Il `GetStopPosition` metodo recupera l'ora in cui si interrompe la riproduzione rispetto alla durata del flusso.</span><span class="sxs-lookup"><span data-stu-id="084ff-105">The `GetStopPosition` method retrieves the time when playback will stop, relative to the duration of the stream.</span></span> <span data-ttu-id="084ff-106">Questo metodo implementa il metodo [**IMediaSeeking:: GetStopPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) .</span><span class="sxs-lookup"><span data-stu-id="084ff-106">This method implements the [**IMediaSeeking::GetStopPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="084ff-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="084ff-107">Syntax</span></span>


```C++
HRESULT GetStopPosition(
   LONGLONG *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="084ff-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="084ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="084ff-109">*pStop*</span><span class="sxs-lookup"><span data-stu-id="084ff-109">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="084ff-110">Puntatore a una variabile che riceve l'ora di arresto, in unità del formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="084ff-110">Pointer to a variable that receives the stop time, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="084ff-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="084ff-111">Return value</span></span>

<span data-ttu-id="084ff-112">Restituisce uno dei valori **HRESULT** elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="084ff-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="084ff-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="084ff-113">Return code</span></span>                                                                               | <span data-ttu-id="084ff-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="084ff-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="084ff-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="084ff-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="084ff-116">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="084ff-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="084ff-117"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="084ff-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="084ff-118">Valore del puntatore **null**</span><span class="sxs-lookup"><span data-stu-id="084ff-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="084ff-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="084ff-119">Remarks</span></span>

<span data-ttu-id="084ff-120">L'ora di arresto è specificata dalla variabile membro [**CSourceSeeking:: m \_ rtStop**](csourceseeking-m-rtstop.md) .</span><span class="sxs-lookup"><span data-stu-id="084ff-120">The stop time is specified by the [**CSourceSeeking::m\_rtStop**](csourceseeking-m-rtstop.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="084ff-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="084ff-121">Requirements</span></span>



| <span data-ttu-id="084ff-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="084ff-122">Requirement</span></span> | <span data-ttu-id="084ff-123">Valore</span><span class="sxs-lookup"><span data-stu-id="084ff-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="084ff-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="084ff-124">Header</span></span><br/>  | <dl> <span data-ttu-id="084ff-125"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="084ff-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="084ff-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="084ff-126">Library</span></span><br/> | <dl> <span data-ttu-id="084ff-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="084ff-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="084ff-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="084ff-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="084ff-129">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="084ff-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




