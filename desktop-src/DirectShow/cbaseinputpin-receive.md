---
description: 'Il metodo Receive riceve il campione multimediale successivo nel flusso. Questo metodo implementa il metodo IMemInputPin:: Receive.'
ms.assetid: 30fefc7b-7c9c-44cd-b58b-2b275dfa2520
title: Metodo CBaseInputPin. Receive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10306d5568ae1754105a4367952cef82f931be99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324858"
---
# <a name="cbaseinputpinreceive-method"></a><span data-ttu-id="334e9-104">Metodo CBaseInputPin. Receive</span><span class="sxs-lookup"><span data-stu-id="334e9-104">CBaseInputPin.Receive method</span></span>

<span data-ttu-id="334e9-105">Il `Receive` metodo riceve il campione multimediale successivo nel flusso.</span><span class="sxs-lookup"><span data-stu-id="334e9-105">The `Receive` method receives the next media sample in the stream.</span></span> <span data-ttu-id="334e9-106">Questo metodo implementa il metodo [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) .</span><span class="sxs-lookup"><span data-stu-id="334e9-106">This method implements the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="334e9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="334e9-107">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="334e9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="334e9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="334e9-109">*pSample*</span><span class="sxs-lookup"><span data-stu-id="334e9-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="334e9-110">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="334e9-110">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="334e9-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="334e9-111">Return value</span></span>

<span data-ttu-id="334e9-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="334e9-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="334e9-113">I valori possibili includono quelli elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="334e9-113">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="334e9-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="334e9-114">Return code</span></span>                                                                                             | <span data-ttu-id="334e9-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="334e9-115">Description</span></span>                                                |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="334e9-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="334e9-116"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="334e9-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="334e9-117">Success.</span></span><br/>                                        |
| <dl> <span data-ttu-id="334e9-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="334e9-118"><dt>**S\_FALSE**</dt></span></span> </dl>                 | <span data-ttu-id="334e9-119">Il PIN sta attualmente scaricando; esempio rifiutato.</span><span class="sxs-lookup"><span data-stu-id="334e9-119">Pin is currently flushing; sample was rejected.</span></span><br/> |
| <dl> <span data-ttu-id="334e9-120"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="334e9-120"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="334e9-121">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="334e9-121">**NULL** pointer argument.</span></span><br/>                      |
| <dl> <span data-ttu-id="334e9-122"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="334e9-122"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="334e9-123">Tipo di supporto non valido.</span><span class="sxs-lookup"><span data-stu-id="334e9-123">Invalid media type.</span></span><br/>                             |
| <dl> <span data-ttu-id="334e9-124"><dt>**errore di runtime di VFW \_ E \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="334e9-124"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl>   | <span data-ttu-id="334e9-125">Si è verificato un errore in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="334e9-125">A run-time error occurred.</span></span><br/>                      |
| <dl> <span data-ttu-id="334e9-126"><dt>**\_ \_ stato non corretto di VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="334e9-126"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>     | <span data-ttu-id="334e9-127">Il PIN è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="334e9-127">The pin is stopped.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="334e9-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="334e9-128">Remarks</span></span>

<span data-ttu-id="334e9-129">Il pin di output upstream chiama questo metodo per recapitare un campione al pin di input.</span><span class="sxs-lookup"><span data-stu-id="334e9-129">The upstream output pin calls this method to deliver a sample to the input pin.</span></span> <span data-ttu-id="334e9-130">Il pin di input deve eseguire una delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="334e9-130">The input pin must do one of the following:</span></span>

-   <span data-ttu-id="334e9-131">Elaborare l'esempio prima di restituire.</span><span class="sxs-lookup"><span data-stu-id="334e9-131">Process the sample before returning.</span></span>
-   <span data-ttu-id="334e9-132">Restituisce ed elabora l'esempio in un thread di lavoro.</span><span class="sxs-lookup"><span data-stu-id="334e9-132">Return, and process the sample in a worker thread.</span></span>
-   <span data-ttu-id="334e9-133">Rifiutare l'esempio.</span><span class="sxs-lookup"><span data-stu-id="334e9-133">Reject the sample.</span></span>

<span data-ttu-id="334e9-134">Se il pin usa un thread di lavoro per elaborare l'esempio, aggiungere un conteggio dei riferimenti all'esempio all'interno di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="334e9-134">If the pin uses a worker thread to process the sample, add a reference count to the sample inside this method.</span></span> <span data-ttu-id="334e9-135">Quando il metodo restituisce il risultato, il pin upstream rilascia l'esempio.</span><span class="sxs-lookup"><span data-stu-id="334e9-135">After the method returns, the upstream pin releases the sample.</span></span> <span data-ttu-id="334e9-136">Quando il conteggio dei riferimenti dell'esempio raggiunge zero, l'esempio torna all'allocatore per riutilizzarlo.</span><span class="sxs-lookup"><span data-stu-id="334e9-136">When the sample's reference count reaches zero, the sample returns to the allocator for re-use.</span></span>

<span data-ttu-id="334e9-137">Questo metodo è sincrono e può bloccare.</span><span class="sxs-lookup"><span data-stu-id="334e9-137">This method is synchronous and can block.</span></span> <span data-ttu-id="334e9-138">Se il metodo potrebbe bloccarsi, il metodo [**CBaseInputPin:: ReceiveCanBlock**](cbaseinputpin-receivecanblock.md) del PIN deve restituire s \_ OK.</span><span class="sxs-lookup"><span data-stu-id="334e9-138">If the method might block, the pin's [**CBaseInputPin::ReceiveCanBlock**](cbaseinputpin-receivecanblock.md) method should return S\_OK.</span></span>

<span data-ttu-id="334e9-139">Nella classe di base, questo metodo esegue i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="334e9-139">In the base class, this method performs the following steps:</span></span>

1.  <span data-ttu-id="334e9-140">Chiama il metodo [**CBaseInputPin:: CheckStreaming**](cbaseinputpin-checkstreaming.md) per verificare che il pin possa elaborare gli esempi.</span><span class="sxs-lookup"><span data-stu-id="334e9-140">Calls the [**CBaseInputPin::CheckStreaming**](cbaseinputpin-checkstreaming.md) method to verify that the pin can process samples now.</span></span> <span data-ttu-id="334e9-141">Se non è possibile, ad esempio, se il PIN viene arrestato, il metodo ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="334e9-141">If it cannot for example, if the pin is stopped the method fails.</span></span>
2.  <span data-ttu-id="334e9-142">Recupera le proprietà di esempio e controlla se il formato è stato modificato (vedere di seguito).</span><span class="sxs-lookup"><span data-stu-id="334e9-142">Retrieves the sample properties and checks whether the format has changed (see below).</span></span>
3.  <span data-ttu-id="334e9-143">Se il formato è stato modificato, il metodo chiama il metodo [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) per determinare se il nuovo formato è accettabile.</span><span class="sxs-lookup"><span data-stu-id="334e9-143">If the format has changed, the method calls the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method to determine whether the new format is acceptable.</span></span>
4.  <span data-ttu-id="334e9-144">Se il nuovo formato non è accettabile, il metodo chiama il metodo [**CBasePin:: EndOfStream**](cbasepin-endofstream.md) , pubblica un \_ evento EC ERRORABORT e restituisce un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="334e9-144">If the new format is not acceptable, the method calls the [**CBasePin::EndOfStream**](cbasepin-endofstream.md) method, posts an EC\_ERRORABORT event, and returns an error code.</span></span>
5.  <span data-ttu-id="334e9-145">Supponendo che non si siano verificati errori, il metodo restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="334e9-145">Assuming there were no errors, the method returns S\_OK.</span></span>

<span data-ttu-id="334e9-146">Verificare la presenza di un formato modificato come segue:</span><span class="sxs-lookup"><span data-stu-id="334e9-146">Test for a format change as follows:</span></span>

-   <span data-ttu-id="334e9-147">Se l'esempio supporta l'interfaccia [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) , verificare il membro **dwSampleFlags** della struttura delle [**\_ \_ Proprietà am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .</span><span class="sxs-lookup"><span data-stu-id="334e9-147">If the sample supports the [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) interface, check the **dwSampleFlags** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span> <span data-ttu-id="334e9-148">Se \_ \_ è presente il flag TYPECHANGED Sample, il formato è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="334e9-148">If the AM\_SAMPLE\_TYPECHANGED flag is present, the format has changed.</span></span>
-   <span data-ttu-id="334e9-149">In caso contrario, se l'esempio non supporta **IMediaSample2**, chiamare il metodo [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) .</span><span class="sxs-lookup"><span data-stu-id="334e9-149">Otherwise, if the sample does not support **IMediaSample2**, call the [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) method.</span></span> <span data-ttu-id="334e9-150">Se il metodo restituisce un valore non **null** , il formato è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="334e9-150">If the method returns a non-**NULL** value, the format has changed.</span></span>

<span data-ttu-id="334e9-151">Nella classe di base, questo metodo non elabora l'esempio.</span><span class="sxs-lookup"><span data-stu-id="334e9-151">In the base class, this method does not process the sample.</span></span> <span data-ttu-id="334e9-152">La classe derivata deve eseguire l'override di questo metodo per eseguire l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="334e9-152">The derived class must override this method to perform the processing.</span></span> <span data-ttu-id="334e9-153">Ciò che si comporta dipende interamente dal filtro. La classe derivata deve chiamare il metodo della classe di base per verificare gli errori descritti in precedenza.</span><span class="sxs-lookup"><span data-stu-id="334e9-153">(What this entails depends entirely on the filter.) The derived class should call the base-class method, to check for the errors described previously.</span></span>

## <a name="requirements"></a><span data-ttu-id="334e9-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="334e9-154">Requirements</span></span>



| <span data-ttu-id="334e9-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="334e9-155">Requirement</span></span> | <span data-ttu-id="334e9-156">Valore</span><span class="sxs-lookup"><span data-stu-id="334e9-156">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="334e9-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="334e9-157">Header</span></span><br/>  | <dl> <span data-ttu-id="334e9-158"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="334e9-158"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="334e9-159">Libreria</span><span class="sxs-lookup"><span data-stu-id="334e9-159">Library</span></span><br/> | <dl> <span data-ttu-id="334e9-160"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="334e9-160"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="334e9-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="334e9-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="334e9-162">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="334e9-162">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




