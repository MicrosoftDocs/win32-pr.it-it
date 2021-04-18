---
description: Il metodo RegisterMediaTime memorizza nella cache i timestamp dell'esempio corrente. Questo metodo usa i parametri *StartTime* e *EndTime* .
ms.assetid: 65755906-cf54-46d6-8149-5ad982be55f3
title: Metodo CRendererPosPassThru. RegisterMediaTime (Ctlutil. h)-parametri StartTime e EndTime
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.RegisterMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e7d9fca04be9381fc739467647fedfa064040a0
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334341"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh---starttime-and-endtime-parameters"></a><span data-ttu-id="c5fe3-104">Metodo CRendererPosPassThru. RegisterMediaTime (Ctlutil. h)-parametri StartTime e EndTime</span><span class="sxs-lookup"><span data-stu-id="c5fe3-104">CRendererPosPassThru.RegisterMediaTime method (Ctlutil.h) - StartTime and EndTime parameters</span></span>

<span data-ttu-id="c5fe3-105">Il metodo [**RegisterMediaTime**](crendererpospassthru-registermediatime.md) memorizza nella cache i timestamp dell'esempio corrente.</span><span class="sxs-lookup"><span data-stu-id="c5fe3-105">The [**RegisterMediaTime**](crendererpospassthru-registermediatime.md) method caches the time stamps from the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5fe3-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c5fe3-106">Syntax</span></span>


```C++
HRESULT RegisterMediaTime(
   LONGLONG StartTime,
   LONGLONG EndTime
);
```



## <a name="parameters"></a><span data-ttu-id="c5fe3-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c5fe3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5fe3-108">*StartTime*</span><span class="sxs-lookup"><span data-stu-id="c5fe3-108">*StartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="c5fe3-109">Ora di inizio di esempio, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="c5fe3-109">Sample start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="c5fe3-110">*EndTime*</span><span class="sxs-lookup"><span data-stu-id="c5fe3-110">*EndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="c5fe3-111">Ora di fine campione, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="c5fe3-111">Sample end time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5fe3-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c5fe3-112">Return value</span></span>

<span data-ttu-id="c5fe3-113">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c5fe3-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c5fe3-114">I valori possibili includono quelli elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="c5fe3-114">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="c5fe3-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c5fe3-115">Return code</span></span>                                                                          | <span data-ttu-id="c5fe3-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5fe3-116">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="c5fe3-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c5fe3-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c5fe3-118">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="c5fe3-118">Success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c5fe3-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="c5fe3-119">Remarks</span></span>

<span data-ttu-id="c5fe3-120">Questo metodo archivia i valori timestamp specificati in *StartTime* e *EndTime*.</span><span class="sxs-lookup"><span data-stu-id="c5fe3-120">This method stores the time stamp values given in *StartTime* and *EndTime*.</span></span> <span data-ttu-id="c5fe3-121">Il metodo [**CRendererPosPassThru:: GetMediaTime**](crendererpospassthru-getmediatime.md) recupera gli stessi valori.</span><span class="sxs-lookup"><span data-stu-id="c5fe3-121">The [**CRendererPosPassThru::GetMediaTime**](crendererpospassthru-getmediatime.md) method retrieves the same values.</span></span>

<span data-ttu-id="c5fe3-122">Il filtro deve chiamare questo metodo per ogni campione che riceve.</span><span class="sxs-lookup"><span data-stu-id="c5fe3-122">The filter should call this method for each sample that it receives.</span></span> <span data-ttu-id="c5fe3-123">Il metodo è sottoposto a overload per accettare un puntatore all'esempio o i valori timestamp stessi.</span><span class="sxs-lookup"><span data-stu-id="c5fe3-123">The method is overloaded to accept either a pointer to the sample, or the time stamp values themselves.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5fe3-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5fe3-124">Requirements</span></span>



| <span data-ttu-id="c5fe3-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5fe3-125">Requirement</span></span> | <span data-ttu-id="c5fe3-126">Valore</span><span class="sxs-lookup"><span data-stu-id="c5fe3-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5fe3-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c5fe3-127">Header</span></span>  | <span data-ttu-id="c5fe3-128">Ctlutil. h (include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="c5fe3-128">Ctlutil.h (include Streams.h)</span></span>                                                                                   |
| <span data-ttu-id="c5fe3-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="c5fe3-129">Library</span></span> | <span data-ttu-id="c5fe3-130">Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug)</span><span class="sxs-lookup"><span data-stu-id="c5fe3-130">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |



 

 




