---
description: Il metodo Receive riceve un campione multimediale, lo elabora e recapita un esempio di output al filtro downstream.
ms.assetid: 036b209a-3535-4922-b7e9-dbed25b812f5
title: Metodo CTransformFilter. Receive (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67924bffc4d4d80b998e686d80d0e50afcd040ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331129"
---
# <a name="ctransformfilterreceive-method"></a><span data-ttu-id="4e579-103">Metodo CTransformFilter. Receive</span><span class="sxs-lookup"><span data-stu-id="4e579-103">CTransformFilter.Receive method</span></span>

<span data-ttu-id="4e579-104">Il `Receive` metodo riceve un campione multimediale, lo elabora e recapita un esempio di output al filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="4e579-104">The `Receive` method receives a media sample, processes it, and delivers an output sample to the downstream filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e579-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4e579-105">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="4e579-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4e579-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e579-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="4e579-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="4e579-108">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) nell'esempio di input.</span><span class="sxs-lookup"><span data-stu-id="4e579-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface on the input sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e579-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4e579-109">Return value</span></span>

<span data-ttu-id="4e579-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4e579-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="4e579-111">I possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4e579-111">Possible values include the following:</span></span>



| <span data-ttu-id="4e579-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="4e579-112">Return code</span></span>                                                                             | <span data-ttu-id="4e579-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e579-113">Description</span></span>                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="4e579-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="4e579-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="4e579-115">Il filtro upstream deve interrompere l'invio degli esempi.</span><span class="sxs-lookup"><span data-stu-id="4e579-115">The upstream filter should stop sending samples.</span></span><br/> |
| <dl> <span data-ttu-id="4e579-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4e579-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="4e579-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="4e579-117">Success.</span></span><br/>                                         |



 

## <a name="remarks"></a><span data-ttu-id="4e579-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="4e579-118">Remarks</span></span>

<span data-ttu-id="4e579-119">Il pin di input del filtro chiama questo metodo quando riceve un campione.</span><span class="sxs-lookup"><span data-stu-id="4e579-119">The filter's input pin calls this method when it receives a sample.</span></span> <span data-ttu-id="4e579-120">Questo metodo chiama il metodo [**CTransformFilter:: InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) , che prepara un nuovo esempio di output.</span><span class="sxs-lookup"><span data-stu-id="4e579-120">This method calls the [**CTransformFilter::InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) method, which prepares a new output sample.</span></span> <span data-ttu-id="4e579-121">Chiama quindi il metodo [**CTransformFilter:: Transform**](ctransformfilter-transform.md) , che deve essere implementato dalla classe derivata.</span><span class="sxs-lookup"><span data-stu-id="4e579-121">Then it calls the [**CTransformFilter::Transform**](ctransformfilter-transform.md) method, which the derived class must implement.</span></span> <span data-ttu-id="4e579-122">Il metodo **Transform** elabora i dati di input e produce i dati di output.</span><span class="sxs-lookup"><span data-stu-id="4e579-122">The **Transform** method processes the input data and produces output data.</span></span>

<span data-ttu-id="4e579-123">Se il metodo **Transform** restituisce \_ false, il `Receive` metodo elimina questo esempio.</span><span class="sxs-lookup"><span data-stu-id="4e579-123">If the **Transform** method returns S\_FALSE, the `Receive` method drops this sample.</span></span> <span data-ttu-id="4e579-124">Nel primo esempio eliminato, il filtro Invia un evento [**di \_ \_ modifica della qualità EC**](ec-quality-change.md) al gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="4e579-124">On the first dropped sample, the filter sends an [**EC\_QUALITY\_CHANGE**](ec-quality-change.md) event to the filter graph manager.</span></span> <span data-ttu-id="4e579-125">In caso contrario, se il metodo **Transform** restituisce S \_ OK, il filtro recapita l'esempio di output.</span><span class="sxs-lookup"><span data-stu-id="4e579-125">Otherwise, if the **Transform** method returns S\_OK, the filter delivers the output sample.</span></span> <span data-ttu-id="4e579-126">A tale scopo, viene chiamato il metodo [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) sul pin di input downstream.</span><span class="sxs-lookup"><span data-stu-id="4e579-126">To do so, it calls the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e579-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e579-127">Requirements</span></span>



| <span data-ttu-id="4e579-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e579-128">Requirement</span></span> | <span data-ttu-id="4e579-129">Valore</span><span class="sxs-lookup"><span data-stu-id="4e579-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e579-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4e579-130">Header</span></span><br/>  | <dl> <span data-ttu-id="4e579-131"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e579-131"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4e579-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="4e579-132">Library</span></span><br/> | <dl> <span data-ttu-id="4e579-133"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4e579-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e579-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4e579-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e579-135">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="4e579-135">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




