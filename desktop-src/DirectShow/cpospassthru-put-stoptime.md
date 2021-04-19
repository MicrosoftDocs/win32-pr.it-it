---
description: Il \_ metodo Put StopTime imposta l'ora in cui la riproduzione viene arrestata rispetto alla durata del flusso. Questo metodo implementa il metodo IMediaPosition::p UT \_ StopTime.
ms.assetid: 0a344cad-df93-47f1-8c7f-5d5ef775b850
title: Metodo CPosPassThru.put_StopTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_StopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f5763700947596a0fb437ba3840df058d4d3239
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333193"
---
# <a name="cpospassthruput_stoptime-method"></a><span data-ttu-id="2025d-104">CPosPassThru. put \_ StopTime (metodo)</span><span class="sxs-lookup"><span data-stu-id="2025d-104">CPosPassThru.put\_StopTime method</span></span>

<span data-ttu-id="2025d-105">Il `put_StopTime` metodo imposta l'ora in cui la riproduzione viene arrestata rispetto alla durata del flusso.</span><span class="sxs-lookup"><span data-stu-id="2025d-105">The `put_StopTime` method sets the time at which the playback will stop, relative to the duration of the stream.</span></span> <span data-ttu-id="2025d-106">Questo metodo implementa il metodo [**IMediaPosition::p UT \_ StopTime**](/windows/desktop/api/Control/nf-control-imediaposition-put_stoptime) .</span><span class="sxs-lookup"><span data-stu-id="2025d-106">This method implements the [**IMediaPosition::put\_StopTime**](/windows/desktop/api/Control/nf-control-imediaposition-put_stoptime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2025d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2025d-107">Syntax</span></span>


```C++
HRESULT put_StopTime(
   REFTIME llTime
);
```



## <a name="parameters"></a><span data-ttu-id="2025d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2025d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2025d-109">*llTime*</span><span class="sxs-lookup"><span data-stu-id="2025d-109">*llTime*</span></span> 
</dt> <dd>

<span data-ttu-id="2025d-110">Arrestare l'ora come valore **doppio** , in secondi.</span><span class="sxs-lookup"><span data-stu-id="2025d-110">Stop time as a **double** value, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2025d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2025d-111">Return value</span></span>

<span data-ttu-id="2025d-112">Restituisce il valore **HRESULT** dal pin connesso.</span><span class="sxs-lookup"><span data-stu-id="2025d-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="2025d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2025d-113">Requirements</span></span>



| <span data-ttu-id="2025d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2025d-114">Requirement</span></span> | <span data-ttu-id="2025d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="2025d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2025d-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2025d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="2025d-117"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2025d-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2025d-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="2025d-118">Library</span></span><br/> | <dl> <span data-ttu-id="2025d-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2025d-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2025d-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2025d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2025d-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="2025d-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




