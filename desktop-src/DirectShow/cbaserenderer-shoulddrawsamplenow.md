---
description: Il metodo ShouldDrawSampleNow determina il modo in cui un campione viene pianificato per il rendering.
ms.assetid: 92994f1f-53d5-42d4-90a2-2984b693e4c0
title: Metodo CBaseRenderer. ShouldDrawSampleNow (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ShouldDrawSampleNow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27fbf603fd670cac2a39831114a7f141b17ffd2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333000"
---
# <a name="cbaserenderershoulddrawsamplenow-method"></a><span data-ttu-id="217db-103">CBaseRenderer. ShouldDrawSampleNow, metodo</span><span class="sxs-lookup"><span data-stu-id="217db-103">CBaseRenderer.ShouldDrawSampleNow method</span></span>

<span data-ttu-id="217db-104">Il `ShouldDrawSampleNow` metodo determina il modo in cui un campione viene pianificato per il rendering.</span><span class="sxs-lookup"><span data-stu-id="217db-104">The `ShouldDrawSampleNow` method determines how a sample is scheduled for rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="217db-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="217db-105">Syntax</span></span>


```C++
virtual HRESULT ShouldDrawSampleNow(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="217db-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="217db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="217db-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="217db-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="217db-108">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="217db-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> <dt>

<span data-ttu-id="217db-109">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="217db-109">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="217db-110">Puntatore a una variabile che contiene l'ora di inizio dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="217db-110">Pointer to a variable that contains the sample's start time.</span></span>

</dd> <dt>

<span data-ttu-id="217db-111">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="217db-111">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="217db-112">Puntatore a una variabile che contiene l'ora di fine dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="217db-112">Pointer to a variable that contains the sample's end time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="217db-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="217db-113">Return value</span></span>

<span data-ttu-id="217db-114">Restituisce un valore \_ false.</span><span class="sxs-lookup"><span data-stu-id="217db-114">Returns S\_FALSE.</span></span> <span data-ttu-id="217db-115">Se la classe derivata esegue l'override di questo metodo, restituire uno dei valori mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="217db-115">If the derived class overrides this method, return one of the values shown in the following table.</span></span>



| <span data-ttu-id="217db-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="217db-116">Return code</span></span>                                                                               | <span data-ttu-id="217db-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="217db-117">Description</span></span>                                                                        |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="217db-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="217db-118"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="217db-119">Il rendering dell'esempio deve essere eseguito immediatamente.</span><span class="sxs-lookup"><span data-stu-id="217db-119">The sample should be rendered immediately.</span></span><br/>                              |
| <dl> <span data-ttu-id="217db-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="217db-120"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="217db-121">L'esempio deve essere pianificato per il rendering, in base agli indicatori temporali.</span><span class="sxs-lookup"><span data-stu-id="217db-121">The sample should be scheduled for rendering, based on the time stamps.</span></span><br/> |
| <dl> <span data-ttu-id="217db-122"><dt>**Codice di errore**</dt></span><span class="sxs-lookup"><span data-stu-id="217db-122"><dt>**Error code**</dt></span></span> </dl> | <span data-ttu-id="217db-123">Non eseguire il rendering di questo esempio.</span><span class="sxs-lookup"><span data-stu-id="217db-123">Do not render this sample.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="217db-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="217db-124">Remarks</span></span>

<span data-ttu-id="217db-125">Il metodo [**CBaseRenderer:: GetSampleTimes**](cbaserenderer-getsampletimes.md) chiama questo metodo.</span><span class="sxs-lookup"><span data-stu-id="217db-125">The [**CBaseRenderer::GetSampleTimes**](cbaserenderer-getsampletimes.md) method calls this method.</span></span> <span data-ttu-id="217db-126">Per impostazione predefinita, gli esempi sono sempre pianificati per il rendering in base ai relativi timestamp.</span><span class="sxs-lookup"><span data-stu-id="217db-126">By default, samples are always scheduled for rendering based on their time stamps.</span></span> <span data-ttu-id="217db-127">La classe derivata può eseguire l'override di questo metodo. ad esempio, per implementare il controllo qualità.</span><span class="sxs-lookup"><span data-stu-id="217db-127">The derived class can override this method; for example, to implement quality control.</span></span>

## <a name="requirements"></a><span data-ttu-id="217db-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="217db-128">Requirements</span></span>



| <span data-ttu-id="217db-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="217db-129">Requirement</span></span> | <span data-ttu-id="217db-130">Valore</span><span class="sxs-lookup"><span data-stu-id="217db-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="217db-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="217db-131">Header</span></span><br/>  | <dl> <span data-ttu-id="217db-132"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="217db-132"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="217db-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="217db-133">Library</span></span><br/> | <dl> <span data-ttu-id="217db-134"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="217db-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="217db-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="217db-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="217db-136">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="217db-136">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




