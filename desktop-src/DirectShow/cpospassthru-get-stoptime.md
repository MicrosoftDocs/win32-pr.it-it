---
description: "Il \\_ metodo Get StopTime recupera l'ora in cui la riproduzione viene arrestata rispetto alla durata del flusso. Questo metodo implementa il metodo IMediaPosition:: Get \\_ StopTime."
ms.assetid: 0ca3f047-ac43-419e-a1ed-b406f89f7af7
title: Metodo CPosPassThru.get_StopTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_StopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 227b054a9737c06e56f7311acc7e0093766608b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327540"
---
# <a name="cpospassthruget_stoptime-method"></a><span data-ttu-id="00fc5-104">Metodo CPosPassThru. Get \_ StopTime</span><span class="sxs-lookup"><span data-stu-id="00fc5-104">CPosPassThru.get\_StopTime method</span></span>

<span data-ttu-id="00fc5-105">Il `get_StopTime` metodo recupera l'ora in cui la riproduzione viene arrestata rispetto alla durata del flusso.</span><span class="sxs-lookup"><span data-stu-id="00fc5-105">The `get_StopTime` method retrieves the time at which the playback will stop, relative to the duration of the stream.</span></span> <span data-ttu-id="00fc5-106">Questo metodo implementa il metodo [**IMediaPosition:: Get \_ StopTime**](/windows/desktop/api/Control/nf-control-imediaposition-get_stoptime) .</span><span class="sxs-lookup"><span data-stu-id="00fc5-106">This method implements the [**IMediaPosition::get\_StopTime**](/windows/desktop/api/Control/nf-control-imediaposition-get_stoptime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="00fc5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="00fc5-107">Syntax</span></span>


```C++
HRESULT get_StopTime(
   REFTIME *pllTime
);
```



## <a name="parameters"></a><span data-ttu-id="00fc5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="00fc5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00fc5-109">*pllTime*</span><span class="sxs-lookup"><span data-stu-id="00fc5-109">*pllTime*</span></span> 
</dt> <dd>

<span data-ttu-id="00fc5-110">Puntatore a una variabile che riceve l'ora di arresto, in secondi.</span><span class="sxs-lookup"><span data-stu-id="00fc5-110">Pointer to a variable that receives the stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00fc5-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="00fc5-111">Return value</span></span>

<span data-ttu-id="00fc5-112">Restituisce il valore **HRESULT** dal pin connesso.</span><span class="sxs-lookup"><span data-stu-id="00fc5-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="00fc5-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00fc5-113">Requirements</span></span>



| <span data-ttu-id="00fc5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="00fc5-114">Requirement</span></span> | <span data-ttu-id="00fc5-115">Valore</span><span class="sxs-lookup"><span data-stu-id="00fc5-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00fc5-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="00fc5-116">Header</span></span><br/>  | <dl> <span data-ttu-id="00fc5-117"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="00fc5-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="00fc5-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="00fc5-118">Library</span></span><br/> | <dl> <span data-ttu-id="00fc5-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="00fc5-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00fc5-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="00fc5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00fc5-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="00fc5-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




