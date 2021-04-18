---
description: "Il metodo Receive riceve un campione multimediale, lo elabora e recapita un esempio di output al filtro downstream. Questo metodo esegue l'override del metodo CTransformFilter:: Receive."
ms.assetid: 35e22a63-471e-4ca8-be3b-d84920cec7cb
title: Metodo CVideoTransformFilter. Receive (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bdc33773a31a7c9ddfd7adb0f3fb20f8fcf6d520
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328628"
---
# <a name="cvideotransformfilterreceive-method"></a><span data-ttu-id="f58b6-104">Metodo CVideoTransformFilter. Receive</span><span class="sxs-lookup"><span data-stu-id="f58b6-104">CVideoTransformFilter.Receive method</span></span>

<span data-ttu-id="f58b6-105">Il `Receive` metodo riceve un campione multimediale, lo elabora e recapita un esempio di output al filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="f58b6-105">The `Receive` method receives a media sample, processes it, and delivers an output sample to the downstream filter.</span></span> <span data-ttu-id="f58b6-106">Questo metodo esegue l'override del metodo [**CTransformFilter:: Receive**](ctransformfilter-receive.md) .</span><span class="sxs-lookup"><span data-stu-id="f58b6-106">This method overrides the [**CTransformFilter::Receive**](ctransformfilter-receive.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f58b6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f58b6-107">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="f58b6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f58b6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f58b6-109">*pSample*</span><span class="sxs-lookup"><span data-stu-id="f58b6-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="f58b6-110">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) nell'esempio di input.</span><span class="sxs-lookup"><span data-stu-id="f58b6-110">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface on the input sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f58b6-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f58b6-111">Return value</span></span>

<span data-ttu-id="f58b6-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f58b6-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="f58b6-113">I possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f58b6-113">Possible values include the following:</span></span>



| <span data-ttu-id="f58b6-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f58b6-114">Return code</span></span>                                                                             | <span data-ttu-id="f58b6-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f58b6-115">Description</span></span>                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="f58b6-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="f58b6-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="f58b6-117">Il filtro upstream deve interrompere l'invio degli esempi.</span><span class="sxs-lookup"><span data-stu-id="f58b6-117">The upstream filter should stop sending samples.</span></span><br/> |
| <dl> <span data-ttu-id="f58b6-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f58b6-118"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="f58b6-119">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="f58b6-119">Success.</span></span><br/>                                         |



 

## <a name="remarks"></a><span data-ttu-id="f58b6-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="f58b6-120">Remarks</span></span>

<span data-ttu-id="f58b6-121">Questo metodo chiama [**CVideoTransformFilter:: ShouldSkipFrame**](cvideotransformfilter-shouldskipframe.md) per determinare se deve fornire questo esempio o semplicemente rimuoverlo.</span><span class="sxs-lookup"><span data-stu-id="f58b6-121">This method calls [**CVideoTransformFilter::ShouldSkipFrame**](cvideotransformfilter-shouldskipframe.md) to determine whether it should deliver this sample or simply discard it.</span></span> <span data-ttu-id="f58b6-122">Se **ShouldSkipFrame** restituisce **false** (che indica che l'esempio deve essere recapitato), il metodo esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f58b6-122">If **ShouldSkipFrame** returns **FALSE** (indicating the sample should be delivered), the method does the following:</span></span>

1.  <span data-ttu-id="f58b6-123">Chiama [**CTransformFilter:: InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) per preparare l'esempio di output</span><span class="sxs-lookup"><span data-stu-id="f58b6-123">Calls [**CTransformFilter::InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) to prepare the output sample</span></span>
2.  <span data-ttu-id="f58b6-124">Chiama [**CTransformFilter:: Transform**](ctransformfilter-transform.md) per elaborare l'esempio di input.</span><span class="sxs-lookup"><span data-stu-id="f58b6-124">Calls [**CTransformFilter::Transform**](ctransformfilter-transform.md) to process the input sample.</span></span> <span data-ttu-id="f58b6-125">Questo metodo è virtuale puro e deve essere implementato nella classe derivata.</span><span class="sxs-lookup"><span data-stu-id="f58b6-125">This method is pure virtual, and must be implemented in the derived class.</span></span>
3.  <span data-ttu-id="f58b6-126">Chiama [**CBaseOutputPin::D Eliver**](cbaseoutputpin-deliver.md) per recapitare l'esempio di output.</span><span class="sxs-lookup"><span data-stu-id="f58b6-126">Calls [**CBaseOutputPin::Deliver**](cbaseoutputpin-deliver.md) to deliver the output sample.</span></span>

<span data-ttu-id="f58b6-127">Questo metodo, inoltre, verifica le modifiche di formato nell'esempio di input o di output, chiamando [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype).</span><span class="sxs-lookup"><span data-stu-id="f58b6-127">Also, this method checks for format changes on the input or output sample, by calling [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype).</span></span> <span data-ttu-id="f58b6-128">Se viene apportata una modifica al formato, il metodo imposta il tipo di connessione sul pin corrispondente.</span><span class="sxs-lookup"><span data-stu-id="f58b6-128">If there is a format change, the method sets the connection type on the corresponding pin.</span></span> <span data-ttu-id="f58b6-129">Prima di impostare il nuovo tipo, viene chiamato **StopStreaming**.</span><span class="sxs-lookup"><span data-stu-id="f58b6-129">Before it sets the new type, it calls **StopStreaming**.</span></span> <span data-ttu-id="f58b6-130">Dopo aver impostato il nuovo tipo, viene chiamato **StartStreaming**.</span><span class="sxs-lookup"><span data-stu-id="f58b6-130">After it sets the new type, it calls **StartStreaming**.</span></span> <span data-ttu-id="f58b6-131">La classe derivata può usare questi metodi per aggiornarne lo stato interno.</span><span class="sxs-lookup"><span data-stu-id="f58b6-131">The derived class can use these methods to update its internal state.</span></span> <span data-ttu-id="f58b6-132">La classe derivata potrebbe anche dover verificare il nuovo formato nel metodo **Transform** .</span><span class="sxs-lookup"><span data-stu-id="f58b6-132">The derived class might also need to check for the new format in its **Transform** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f58b6-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f58b6-133">Requirements</span></span>



| <span data-ttu-id="f58b6-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="f58b6-134">Requirement</span></span> | <span data-ttu-id="f58b6-135">Valore</span><span class="sxs-lookup"><span data-stu-id="f58b6-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f58b6-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f58b6-136">Header</span></span><br/>  | <dl> <span data-ttu-id="f58b6-137"><dt>Vtrans. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f58b6-137"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="f58b6-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="f58b6-138">Library</span></span><br/> | <dl> <span data-ttu-id="f58b6-139"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f58b6-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f58b6-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f58b6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f58b6-141">**Classe CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="f58b6-141">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




