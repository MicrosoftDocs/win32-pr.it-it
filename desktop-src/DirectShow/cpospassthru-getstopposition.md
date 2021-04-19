---
description: "Il metodo GetStopPosition recupera l'ora in cui la riproduzione viene arrestata rispetto alla durata del flusso. Questo metodo implementa il metodo IMediaSeeking:: GetStopPosition."
ms.assetid: 11486371-da0a-4b83-956b-ef6b92721e74
title: Metodo CPosPassThru. GetStopPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetStopPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ee704a47074db032badfa1f02ffbf2db8c7efa4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333206"
---
# <a name="cpospassthrugetstopposition-method"></a><span data-ttu-id="1c04d-104">CPosPassThru. GetStopPosition, metodo</span><span class="sxs-lookup"><span data-stu-id="1c04d-104">CPosPassThru.GetStopPosition method</span></span>

<span data-ttu-id="1c04d-105">Il `GetStopPosition` metodo recupera l'ora in cui la riproduzione viene arrestata rispetto alla durata del flusso.</span><span class="sxs-lookup"><span data-stu-id="1c04d-105">The `GetStopPosition` method retrieves the time at which the playback will stop, relative to the duration of the stream.</span></span> <span data-ttu-id="1c04d-106">Questo metodo implementa il metodo [**IMediaSeeking:: GetStopPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) .</span><span class="sxs-lookup"><span data-stu-id="1c04d-106">This method implements the [**IMediaSeeking::GetStopPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c04d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c04d-107">Syntax</span></span>


```C++
HRESULT GetStopPosition(
   LONGLONG *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="1c04d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1c04d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c04d-109">*pStop*</span><span class="sxs-lookup"><span data-stu-id="1c04d-109">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="1c04d-110">Puntatore a una variabile che riceve l'ora di arresto, in unità del formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="1c04d-110">Pointer to a variable that receives the stop time, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c04d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1c04d-111">Return value</span></span>

<span data-ttu-id="1c04d-112">Restituisce il valore **HRESULT** dal pin connesso.</span><span class="sxs-lookup"><span data-stu-id="1c04d-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c04d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c04d-113">Requirements</span></span>



| <span data-ttu-id="1c04d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c04d-114">Requirement</span></span> | <span data-ttu-id="1c04d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="1c04d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c04d-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1c04d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="1c04d-117"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1c04d-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1c04d-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="1c04d-118">Library</span></span><br/> | <dl> <span data-ttu-id="1c04d-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1c04d-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c04d-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c04d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c04d-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="1c04d-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




