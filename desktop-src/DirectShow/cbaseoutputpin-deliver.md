---
description: Il metodo Deliver recapita un campione multimediale al pin di input connesso.
ms.assetid: b871df84-c69e-42eb-9da9-c25996bf08c3
title: Metodo CBaseOutputPin. Deliver (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Deliver
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5adc603e4cdd1f49e649264d2d82d6df0fb12569
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332069"
---
# <a name="cbaseoutputpindeliver-method"></a><span data-ttu-id="8b95c-103">Metodo CBaseOutputPin. Deliver</span><span class="sxs-lookup"><span data-stu-id="8b95c-103">CBaseOutputPin.Deliver method</span></span>

<span data-ttu-id="8b95c-104">Il `Deliver` Metodo recapita un campione multimediale al pin di input connesso.</span><span class="sxs-lookup"><span data-stu-id="8b95c-104">The `Deliver` method delivers a media sample to the connected input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b95c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8b95c-105">Syntax</span></span>


```C++
virtual HRESULT Deliver(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="8b95c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8b95c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b95c-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="8b95c-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="8b95c-108">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="8b95c-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b95c-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8b95c-109">Return value</span></span>

<span data-ttu-id="8b95c-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8b95c-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="8b95c-111">I valori possibili includono quelli elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="8b95c-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="8b95c-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8b95c-112">Return code</span></span>                                                                                           | <span data-ttu-id="8b95c-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b95c-113">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8b95c-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8b95c-114"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="8b95c-115">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="8b95c-115">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="8b95c-116"><dt>**VFW \_ E \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="8b95c-116"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="8b95c-117">Il PIN non è connesso.</span><span class="sxs-lookup"><span data-stu-id="8b95c-117">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8b95c-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="8b95c-118">Remarks</span></span>

<span data-ttu-id="8b95c-119">Questo metodo chiama il metodo [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) sul pin di input.</span><span class="sxs-lookup"><span data-stu-id="8b95c-119">This method calls the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the input pin.</span></span> <span data-ttu-id="8b95c-120">**Receive** può bloccare se il metodo [**IMemInputPin:: ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8b95c-120">**Receive** can block if the [**IMemInputPin::ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) method returns S\_OK.</span></span>

<span data-ttu-id="8b95c-121">Rilasciare l'esempio dopo aver chiamato questo metodo.</span><span class="sxs-lookup"><span data-stu-id="8b95c-121">Release the sample after calling this method.</span></span> <span data-ttu-id="8b95c-122">Il pin di input potrebbe mantenere un conteggio dei riferimenti nell'esempio, quindi non riutilizzare l'esempio.</span><span class="sxs-lookup"><span data-stu-id="8b95c-122">The input pin might hold a reference count on the sample, so do not reuse the sample.</span></span> <span data-ttu-id="8b95c-123">Chiamare sempre il metodo [**CBaseOutputPin:: GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) per ottenere un nuovo campione.</span><span class="sxs-lookup"><span data-stu-id="8b95c-123">Always call the [**CBaseOutputPin::GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) method to obtain a new sample.</span></span>

<span data-ttu-id="8b95c-124">Mantenere la sezione critica del filtro prima di chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="8b95c-124">Hold the filter's critical section before calling this method.</span></span> <span data-ttu-id="8b95c-125">In caso contrario, il PIN potrebbe essere disconnesso durante la chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="8b95c-125">Otherwise, the pin might get disconnected during the method call.</span></span> <span data-ttu-id="8b95c-126">Se il filtro utilizza un thread di lavoro per recapitare gli esempi, mantenere la sezione critica quando il filtro è pronto per fornire un campione.</span><span class="sxs-lookup"><span data-stu-id="8b95c-126">If the filter uses a worker thread to deliver samples, hold the critical section when the filter is ready to deliver a sample.</span></span> <span data-ttu-id="8b95c-127">In caso contrario, è possibile mantenere la sezione critica nel metodo [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) del filtro, in cui il filtro elabora gli esempi.</span><span class="sxs-lookup"><span data-stu-id="8b95c-127">Otherwise, you can hold the critical section in the filter's [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method, where the filter processes samples.</span></span>

<span data-ttu-id="8b95c-128">I thread di lavoro possono creare un potenziale deadlock.</span><span class="sxs-lookup"><span data-stu-id="8b95c-128">Worker threads can create a potential deadlock.</span></span> <span data-ttu-id="8b95c-129">Quando il thread include la sezione critica, potrebbe attendere una modifica dello stato nel filtro.</span><span class="sxs-lookup"><span data-stu-id="8b95c-129">When the thread holds the critical section, it might wait on a state change in the filter.</span></span> <span data-ttu-id="8b95c-130">Allo stesso tempo, la modifica dello stato potrebbe essere in attesa del completamento del thread.</span><span class="sxs-lookup"><span data-stu-id="8b95c-130">At the same time, the state change might be waiting for the thread to complete.</span></span> <span data-ttu-id="8b95c-131">Per evitare questo problema, il codice di modifica dello stato dovrebbe segnalare un evento che termina il thread, quindi attendere il completamento del segnale del thread.</span><span class="sxs-lookup"><span data-stu-id="8b95c-131">To prevent this, the state-change code should signal an event that terminates the thread, and then wait for the thread to signal completion.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b95c-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b95c-132">Requirements</span></span>



| <span data-ttu-id="8b95c-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b95c-133">Requirement</span></span> | <span data-ttu-id="8b95c-134">Valore</span><span class="sxs-lookup"><span data-stu-id="8b95c-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b95c-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8b95c-135">Header</span></span><br/>  | <dl> <span data-ttu-id="8b95c-136"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8b95c-136"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8b95c-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="8b95c-137">Library</span></span><br/> | <dl> <span data-ttu-id="8b95c-138"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8b95c-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b95c-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8b95c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b95c-140">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="8b95c-140">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




