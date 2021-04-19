---
description: Il metodo GetSampleTimes recupera i timestamp da un campione.
ms.assetid: a8fead22-a12c-489d-9c42-d5b61f480c25
title: Metodo CBaseRenderer. GetSampleTimes (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetSampleTimes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c389c2ea55ddb15c59fe30e03f392d68aa3b5ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325933"
---
# <a name="cbaserenderergetsampletimes-method"></a><span data-ttu-id="82ea7-103">CBaseRenderer. GetSampleTimes, metodo</span><span class="sxs-lookup"><span data-stu-id="82ea7-103">CBaseRenderer.GetSampleTimes method</span></span>

<span data-ttu-id="82ea7-104">Il `GetSampleTimes` metodo recupera i timestamp da un campione.</span><span class="sxs-lookup"><span data-stu-id="82ea7-104">The `GetSampleTimes` method retrieves the time stamps from a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="82ea7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="82ea7-105">Syntax</span></span>


```C++
virtual HRESULT GetSampleTimes(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="82ea7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="82ea7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82ea7-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="82ea7-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="82ea7-108">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="82ea7-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> <dt>

<span data-ttu-id="82ea7-109">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="82ea7-109">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="82ea7-110">Puntatore a una variabile che riceve l'ora di inizio.</span><span class="sxs-lookup"><span data-stu-id="82ea7-110">Pointer to a variable that receives the start time.</span></span>

</dd> <dt>

<span data-ttu-id="82ea7-111">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="82ea7-111">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="82ea7-112">Puntatore a una variabile che riceve l'ora di fine.</span><span class="sxs-lookup"><span data-stu-id="82ea7-112">Pointer to a variable that receives the end time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82ea7-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="82ea7-113">Return value</span></span>

<span data-ttu-id="82ea7-114">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="82ea7-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="82ea7-115">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="82ea7-115">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="82ea7-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="82ea7-116">Return code</span></span>                                                                                                    | <span data-ttu-id="82ea7-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82ea7-117">Description</span></span>                                                                        |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="82ea7-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="82ea7-118"><dt>**S\_OK**</dt></span></span> </dl>                           | <span data-ttu-id="82ea7-119">Il rendering dell'esempio deve essere eseguito immediatamente.</span><span class="sxs-lookup"><span data-stu-id="82ea7-119">The sample should be rendered immediately.</span></span><br/>                              |
| <dl> <span data-ttu-id="82ea7-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="82ea7-120"><dt>**S\_FALSE**</dt></span></span> </dl>                        | <span data-ttu-id="82ea7-121">L'esempio deve essere pianificato per il rendering, in base agli indicatori temporali.</span><span class="sxs-lookup"><span data-stu-id="82ea7-121">The sample should be scheduled for rendering, based on the time stamps.</span></span><br/> |
| <dl> <span data-ttu-id="82ea7-122"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="82ea7-122"><dt>**E\_FAIL**</dt></span></span> </dl>                         | <span data-ttu-id="82ea7-123">Non eseguire il rendering di questo esempio.</span><span class="sxs-lookup"><span data-stu-id="82ea7-123">Do not render this sample.</span></span><br/>                                              |
| <dl> <span data-ttu-id="82ea7-124"><dt>**ora di inizio di VFW \_ E \_ dopo la \_ \_ \_ fine**</dt></span><span class="sxs-lookup"><span data-stu-id="82ea7-124"><dt>**VFW\_E\_START\_TIME\_AFTER\_END**</dt></span></span> </dl> | <span data-ttu-id="82ea7-125">Timestamp non valido: l'ora di fine è precedente all'ora di inizio.</span><span class="sxs-lookup"><span data-stu-id="82ea7-125">Bad time stamp: The end time is earlier than the start time.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="82ea7-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="82ea7-126">Remarks</span></span>

<span data-ttu-id="82ea7-127">Il filtro chiama questo metodo per determinare la modalità di gestione di un campione.</span><span class="sxs-lookup"><span data-stu-id="82ea7-127">The filter calls this method to determine how it should handle a sample.</span></span> <span data-ttu-id="82ea7-128">Se il valore restituito è S \_ OK, il filtro esegue immediatamente il rendering dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="82ea7-128">If the return value is S\_OK, the filter renders the sample immediately.</span></span> <span data-ttu-id="82ea7-129">Se il valore restituito è S \_ false, il filtro pianifica l'esempio per il rendering in base ai timestamp.</span><span class="sxs-lookup"><span data-stu-id="82ea7-129">If the return value is S\_FALSE, the filter schedules the sample for rendering, based on the time stamps.</span></span> <span data-ttu-id="82ea7-130">Se il valore restituito è un codice di errore, il filtro rifiuterà l'esempio.</span><span class="sxs-lookup"><span data-stu-id="82ea7-130">If the return value is an error code, the filter rejects the sample.</span></span>

<span data-ttu-id="82ea7-131">Questo metodo restituisce \_ OK se l'esempio non dispone di timestamp o se il filtro non dispone di un clock di riferimento.</span><span class="sxs-lookup"><span data-stu-id="82ea7-131">This method returns S\_OK if the sample has no time stamps, or if the filter does not have a reference clock.</span></span> <span data-ttu-id="82ea7-132">In caso contrario, restituisce il valore del metodo [**CBaseRenderer:: ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md) .</span><span class="sxs-lookup"><span data-stu-id="82ea7-132">Otherwise, it returns the value of the [**CBaseRenderer::ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md) method.</span></span> <span data-ttu-id="82ea7-133">Nella classe di base, **ShouldDrawSampleNow** restituisce sempre \_ false.</span><span class="sxs-lookup"><span data-stu-id="82ea7-133">In the base class, **ShouldDrawSampleNow** always returns S\_FALSE.</span></span> <span data-ttu-id="82ea7-134">La classe derivata può eseguire l'override di questo comportamento.</span><span class="sxs-lookup"><span data-stu-id="82ea7-134">The derived class can override this behavior.</span></span> <span data-ttu-id="82ea7-135">Se, ad esempio, la classe derivata implementa la gestione del controllo di qualità, potrebbe restituire E \_ non riuscire a eliminare un campione.</span><span class="sxs-lookup"><span data-stu-id="82ea7-135">For example, if the derived class implements quality control management, it might return E\_FAIL to drop a sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="82ea7-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82ea7-136">Requirements</span></span>



| <span data-ttu-id="82ea7-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="82ea7-137">Requirement</span></span> | <span data-ttu-id="82ea7-138">Valore</span><span class="sxs-lookup"><span data-stu-id="82ea7-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82ea7-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="82ea7-139">Header</span></span><br/>  | <dl> <span data-ttu-id="82ea7-140"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="82ea7-140"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="82ea7-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="82ea7-141">Library</span></span><br/> | <dl> <span data-ttu-id="82ea7-142"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="82ea7-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82ea7-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="82ea7-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82ea7-144">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="82ea7-144">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




