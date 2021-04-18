---
description: 'Il metodo GetDuration recupera la durata del flusso. Questo metodo implementa il metodo IMediaSeeking:: GetDuration.'
ms.assetid: 074eb2d0-a7a3-4bc1-82e8-2f42c6d43dac
title: Metodo CSourceSeeking. GetDuration (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetDuration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8368f655394089c1155d848bc53d2ba2375e3320
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329512"
---
# <a name="csourceseekinggetduration-method"></a><span data-ttu-id="1ba76-104">CSourceSeeking. GetDuration, metodo</span><span class="sxs-lookup"><span data-stu-id="1ba76-104">CSourceSeeking.GetDuration method</span></span>

<span data-ttu-id="1ba76-105">Il `GetDuration` metodo recupera la durata del flusso.</span><span class="sxs-lookup"><span data-stu-id="1ba76-105">The `GetDuration` method retrieves the duration of the stream.</span></span> <span data-ttu-id="1ba76-106">Questo metodo implementa il metodo [**IMediaSeeking:: GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) .</span><span class="sxs-lookup"><span data-stu-id="1ba76-106">This method implements the [**IMediaSeeking::GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ba76-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1ba76-107">Syntax</span></span>


```C++
HRESULT GetDuration(
   LONGLONG *pDuration
);
```



## <a name="parameters"></a><span data-ttu-id="1ba76-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1ba76-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ba76-109">*pDuration*</span><span class="sxs-lookup"><span data-stu-id="1ba76-109">*pDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="1ba76-110">Puntatore a una variabile che riceve la durata, in unità del formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="1ba76-110">Pointer to a variable that receives the duration, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ba76-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1ba76-111">Return value</span></span>

<span data-ttu-id="1ba76-112">Restituisce uno dei valori **HRESULT** elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="1ba76-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="1ba76-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="1ba76-113">Return code</span></span>                                                                               | <span data-ttu-id="1ba76-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ba76-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="1ba76-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1ba76-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="1ba76-116">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="1ba76-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="1ba76-117"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="1ba76-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="1ba76-118">Valore del puntatore **null**</span><span class="sxs-lookup"><span data-stu-id="1ba76-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1ba76-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="1ba76-119">Remarks</span></span>

<span data-ttu-id="1ba76-120">La durata è specificata dalla variabile membro [**CSourceSeeking:: m \_ rtDuration**](csourceseeking-m-rtduration.md) .</span><span class="sxs-lookup"><span data-stu-id="1ba76-120">The duration is specified by the [**CSourceSeeking::m\_rtDuration**](csourceseeking-m-rtduration.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ba76-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ba76-121">Requirements</span></span>



| <span data-ttu-id="1ba76-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ba76-122">Requirement</span></span> | <span data-ttu-id="1ba76-123">Valore</span><span class="sxs-lookup"><span data-stu-id="1ba76-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ba76-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1ba76-124">Header</span></span><br/>  | <dl> <span data-ttu-id="1ba76-125"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1ba76-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1ba76-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="1ba76-126">Library</span></span><br/> | <dl> <span data-ttu-id="1ba76-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1ba76-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ba76-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ba76-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ba76-129">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="1ba76-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




