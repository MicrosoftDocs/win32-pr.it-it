---
description: "Il metodo Run notifica al pin che il filtro è ora in esecuzione. Questo metodo esegue l'override del Metodo CBasePin:: Run."
ms.assetid: ee0285aa-9afd-464a-b8b4-d8b7faa49dbd
title: Metodo CRenderedInputPin. Run (Amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef3de4d5ab9a06766ccce171c9d417639ce66a42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328826"
---
# <a name="crenderedinputpinrun-method"></a><span data-ttu-id="949f3-104">Metodo CRenderedInputPin. Run</span><span class="sxs-lookup"><span data-stu-id="949f3-104">CRenderedInputPin.Run method</span></span>

<span data-ttu-id="949f3-105">Il `Run` metodo notifica al pin che il filtro è ora in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="949f3-105">The `Run` method notifies the pin that the filter is now running.</span></span> <span data-ttu-id="949f3-106">Questo metodo esegue l'override del metodo [**CBasePin:: Run**](cbasepin-run.md) .</span><span class="sxs-lookup"><span data-stu-id="949f3-106">This method overrides the [**CBasePin::Run**](cbasepin-run.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="949f3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="949f3-107">Syntax</span></span>


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a><span data-ttu-id="949f3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="949f3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="949f3-109">*tStart*</span><span class="sxs-lookup"><span data-stu-id="949f3-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="949f3-110">Ora di inizio passata al metodo [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) del filtro.</span><span class="sxs-lookup"><span data-stu-id="949f3-110">The start time that was passed to the filter's [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="949f3-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="949f3-111">Return value</span></span>

<span data-ttu-id="949f3-112">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="949f3-112">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="949f3-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="949f3-113">Requirements</span></span>



| <span data-ttu-id="949f3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="949f3-114">Requirement</span></span> | <span data-ttu-id="949f3-115">Valore</span><span class="sxs-lookup"><span data-stu-id="949f3-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="949f3-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="949f3-116">Header</span></span><br/>  | <dl> <span data-ttu-id="949f3-117"><dt>Amextra. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="949f3-117"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="949f3-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="949f3-118">Library</span></span><br/> | <dl> <span data-ttu-id="949f3-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="949f3-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="949f3-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="949f3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="949f3-121">**Classe CRenderedInputPin**</span><span class="sxs-lookup"><span data-stu-id="949f3-121">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




