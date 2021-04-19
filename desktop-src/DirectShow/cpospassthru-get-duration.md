---
description: 'Il \_ metodo get Duration recupera la durata del flusso. Questo metodo implementa il metodo IMediaPosition:: Get \_ Duration.'
ms.assetid: 326a8cd3-d05f-49d0-941d-08f9778e9a06
title: Metodo CPosPassThru.get_Duration (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_Duration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: df518a0691a4fe1a6c0443ba93a83e65577efe21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332578"
---
# <a name="cpospassthruget_duration-method"></a><span data-ttu-id="39417-104">Metodo CPosPassThru. Get \_ Duration</span><span class="sxs-lookup"><span data-stu-id="39417-104">CPosPassThru.get\_Duration method</span></span>

<span data-ttu-id="39417-105">Il `get_Duration` metodo recupera la durata del flusso.</span><span class="sxs-lookup"><span data-stu-id="39417-105">The `get_Duration` method retrieves the duration of the stream.</span></span> <span data-ttu-id="39417-106">Questo metodo implementa il metodo [**IMediaPosition:: Get \_ Duration**](/windows/desktop/api/Control/nf-control-imediaposition-get_duration) .</span><span class="sxs-lookup"><span data-stu-id="39417-106">This method implements the [**IMediaPosition::get\_Duration**](/windows/desktop/api/Control/nf-control-imediaposition-get_duration) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="39417-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="39417-107">Syntax</span></span>


```C++
HRESULT get_Duration(
   REFTIME *plength
);
```



## <a name="parameters"></a><span data-ttu-id="39417-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="39417-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39417-109">*plength*</span><span class="sxs-lookup"><span data-stu-id="39417-109">*plength*</span></span> 
</dt> <dd>

<span data-ttu-id="39417-110">Puntatore a una variabile che riceve la lunghezza totale del flusso, in secondi.</span><span class="sxs-lookup"><span data-stu-id="39417-110">Pointer to a variable that receives the total stream length, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39417-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="39417-111">Return value</span></span>

<span data-ttu-id="39417-112">Restituisce il valore **HRESULT** dal pin connesso.</span><span class="sxs-lookup"><span data-stu-id="39417-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="39417-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39417-113">Requirements</span></span>



| <span data-ttu-id="39417-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="39417-114">Requirement</span></span> | <span data-ttu-id="39417-115">Valore</span><span class="sxs-lookup"><span data-stu-id="39417-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39417-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="39417-116">Header</span></span><br/>  | <dl> <span data-ttu-id="39417-117"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="39417-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="39417-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="39417-118">Library</span></span><br/> | <dl> <span data-ttu-id="39417-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="39417-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39417-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39417-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39417-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="39417-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




