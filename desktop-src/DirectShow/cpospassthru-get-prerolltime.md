---
description: 'Il \_ metodo Get PrerollTime recupera la quantità di dati che verranno accodati prima della posizione iniziale. Questo metodo implementa il metodo IMediaPosition:: Get \_ PrerollTime.'
ms.assetid: 37c12798-eb0d-4859-8b2e-52d6ae147863
title: Metodo CPosPassThru.get_PrerollTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_PrerollTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 55cb2cc37a18c9ea00b4eb7115590f472b8d467e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327841"
---
# <a name="cpospassthruget_prerolltime-method"></a><span data-ttu-id="8599a-104">Metodo CPosPassThru. Get \_ PrerollTime</span><span class="sxs-lookup"><span data-stu-id="8599a-104">CPosPassThru.get\_PrerollTime method</span></span>

<span data-ttu-id="8599a-105">Il `get_PrerollTime` metodo recupera la quantità di dati che verranno accodati prima della posizione iniziale.</span><span class="sxs-lookup"><span data-stu-id="8599a-105">The `get_PrerollTime` method retrieves the amount of data that will be queued before the start position.</span></span> <span data-ttu-id="8599a-106">Questo metodo implementa il metodo [**IMediaPosition:: Get \_ PrerollTime**](/windows/desktop/api/Control/nf-control-imediaposition-get_prerolltime) .</span><span class="sxs-lookup"><span data-stu-id="8599a-106">This method implements the [**IMediaPosition::get\_PrerollTime**](/windows/desktop/api/Control/nf-control-imediaposition-get_prerolltime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8599a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8599a-107">Syntax</span></span>


```C++
HRESULT get_PrerollTime(
   REFTIME *pllTime
);
```



## <a name="parameters"></a><span data-ttu-id="8599a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8599a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8599a-109">*pllTime*</span><span class="sxs-lookup"><span data-stu-id="8599a-109">*pllTime*</span></span> 
</dt> <dd>

<span data-ttu-id="8599a-110">Puntatore a una variabile che riceve il tempo di preiscrizione, in secondi.</span><span class="sxs-lookup"><span data-stu-id="8599a-110">Pointer to a variable that receives the preroll time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8599a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8599a-111">Return value</span></span>

<span data-ttu-id="8599a-112">Restituisce il valore **HRESULT** dal pin connesso.</span><span class="sxs-lookup"><span data-stu-id="8599a-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="8599a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8599a-113">Requirements</span></span>



| <span data-ttu-id="8599a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8599a-114">Requirement</span></span> | <span data-ttu-id="8599a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="8599a-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8599a-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8599a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="8599a-117"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8599a-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8599a-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="8599a-118">Library</span></span><br/> | <dl> <span data-ttu-id="8599a-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8599a-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8599a-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8599a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8599a-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="8599a-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




