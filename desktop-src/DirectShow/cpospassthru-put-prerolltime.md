---
description: Il \_ metodo Put PrerollTime imposta la quantità di dati che verranno accodati prima della posizione iniziale. Questo metodo implementa il metodo IMediaPosition::p UT \_ PrerollTime.
ms.assetid: 5c35fb1d-2296-493f-8104-601127d7dd9f
title: Metodo CPosPassThru.put_PrerollTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_PrerollTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60bd4eddc7688373386147ea7999fdbd17f9af6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329757"
---
# <a name="cpospassthruput_prerolltime-method"></a><span data-ttu-id="15526-104">CPosPassThru. put \_ PrerollTime (metodo)</span><span class="sxs-lookup"><span data-stu-id="15526-104">CPosPassThru.put\_PrerollTime method</span></span>

<span data-ttu-id="15526-105">Il `put_PrerollTime` metodo imposta la quantità di dati che verranno accodati prima della posizione iniziale.</span><span class="sxs-lookup"><span data-stu-id="15526-105">The `put_PrerollTime` method sets the amount of data that will be queued before the start position.</span></span> <span data-ttu-id="15526-106">Questo metodo implementa il metodo [**IMediaPosition::p UT \_ PrerollTime**](/windows/desktop/api/Control/nf-control-imediaposition-put_prerolltime) .</span><span class="sxs-lookup"><span data-stu-id="15526-106">This method implements the [**IMediaPosition::put\_PrerollTime**](/windows/desktop/api/Control/nf-control-imediaposition-put_prerolltime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="15526-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15526-107">Syntax</span></span>


```C++
HRESULT put_PrerollTime(
   REFTIME llTime
);
```



## <a name="parameters"></a><span data-ttu-id="15526-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="15526-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15526-109">*llTime*</span><span class="sxs-lookup"><span data-stu-id="15526-109">*llTime*</span></span> 
</dt> <dd>

<span data-ttu-id="15526-110">Tempo di preiscrizione, in secondi.</span><span class="sxs-lookup"><span data-stu-id="15526-110">Preroll time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15526-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="15526-111">Return value</span></span>

<span data-ttu-id="15526-112">Restituisce il valore **HRESULT** dal pin connesso.</span><span class="sxs-lookup"><span data-stu-id="15526-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="15526-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15526-113">Requirements</span></span>



| <span data-ttu-id="15526-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="15526-114">Requirement</span></span> | <span data-ttu-id="15526-115">Valore</span><span class="sxs-lookup"><span data-stu-id="15526-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15526-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="15526-116">Header</span></span><br/>  | <dl> <span data-ttu-id="15526-117"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="15526-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="15526-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="15526-118">Library</span></span><br/> | <dl> <span data-ttu-id="15526-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="15526-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15526-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15526-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15526-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="15526-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




