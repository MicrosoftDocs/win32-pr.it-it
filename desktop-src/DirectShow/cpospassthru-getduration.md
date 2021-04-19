---
description: 'Il metodo GetDuration recupera la durata del flusso. Questo metodo implementa il metodo IMediaSeeking:: GetDuration.'
ms.assetid: 0552e7bb-4d7e-40a8-a8ad-89ae6fff8ccb
title: Metodo CPosPassThru. GetDuration (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetDuration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b9b533537c36ac7ec4c76289307368539482aa47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324182"
---
# <a name="cpospassthrugetduration-method"></a><span data-ttu-id="79820-104">CPosPassThru. GetDuration, metodo</span><span class="sxs-lookup"><span data-stu-id="79820-104">CPosPassThru.GetDuration method</span></span>

<span data-ttu-id="79820-105">Il `GetDuration` metodo recupera la durata del flusso.</span><span class="sxs-lookup"><span data-stu-id="79820-105">The `GetDuration` method retrieves the duration of the stream.</span></span> <span data-ttu-id="79820-106">Questo metodo implementa il metodo [**IMediaSeeking:: GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) .</span><span class="sxs-lookup"><span data-stu-id="79820-106">This method implements the [**IMediaSeeking::GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="79820-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="79820-107">Syntax</span></span>


```C++
HRESULT GetDuration(
   LONGLONG *pDuration
);
```



## <a name="parameters"></a><span data-ttu-id="79820-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="79820-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79820-109">*pDuration*</span><span class="sxs-lookup"><span data-stu-id="79820-109">*pDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="79820-110">Puntatore a una variabile che riceve la durata, in unità del formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="79820-110">Pointer to a variable that receives the duration, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79820-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="79820-111">Return value</span></span>

<span data-ttu-id="79820-112">Restituisce il valore **HRESULT** dal pin connesso.</span><span class="sxs-lookup"><span data-stu-id="79820-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="79820-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="79820-113">Requirements</span></span>



| <span data-ttu-id="79820-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="79820-114">Requirement</span></span> | <span data-ttu-id="79820-115">Valore</span><span class="sxs-lookup"><span data-stu-id="79820-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79820-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="79820-116">Header</span></span><br/>  | <dl> <span data-ttu-id="79820-117"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="79820-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="79820-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="79820-118">Library</span></span><br/> | <dl> <span data-ttu-id="79820-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="79820-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79820-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="79820-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79820-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="79820-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




