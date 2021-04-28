---
description: "Metodo CBaseInputPin.Receive: il metodo Receive riceve l'esempio multimediale successivo nel flusso. Questo metodo implementa il metodo IMemInputPin::Receive."
ms.assetid: 30fefc7b-7c9c-44cd-b58b-2b275dfa2520
title: Metodo CBaseInputPin.Receive (Amfilter.h)
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
ms.openlocfilehash: 4fe88913ad374923c11cf058a3dc0aa70580411e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099689"
---
# <a name="cbaseinputpinreceive-method"></a><span data-ttu-id="99463-104">Metodo CBaseInputPin.Receive</span><span class="sxs-lookup"><span data-stu-id="99463-104">CBaseInputPin.Receive method</span></span>

<span data-ttu-id="99463-105">Il `Receive` metodo riceve l'esempio multimediale successivo nel flusso.</span><span class="sxs-lookup"><span data-stu-id="99463-105">The `Receive` method receives the next media sample in the stream.</span></span> <span data-ttu-id="99463-106">Questo metodo implementa il [**metodo IMemInputPin::Receive.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)</span><span class="sxs-lookup"><span data-stu-id="99463-106">This method implements the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="99463-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="99463-107">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="99463-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="99463-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99463-109">*pSample*</span><span class="sxs-lookup"><span data-stu-id="99463-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="99463-110">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="99463-110">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99463-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="99463-111">Return value</span></span>

<span data-ttu-id="99463-112">Restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="99463-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="99463-113">I valori possibili includono quelli elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="99463-113">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="99463-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="99463-114">Return code</span></span>                                                                                             | <span data-ttu-id="99463-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99463-115">Description</span></span>                                                |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="99463-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="99463-116"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="99463-117">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="99463-117">Success.</span></span><br/>                                        |
| <dl> <span data-ttu-id="99463-118"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="99463-118"><dt>**S\_FALSE**</dt></span></span> </dl>                 | <span data-ttu-id="99463-119">Lo scaricamento del pin è in corso. l'esempio è stato rifiutato.</span><span class="sxs-lookup"><span data-stu-id="99463-119">Pin is currently flushing; sample was rejected.</span></span><br/> |
| <dl> <span data-ttu-id="99463-120"><dt>**PUNTATORE E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="99463-120"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="99463-121">Argomento del puntatore **NULL.**</span><span class="sxs-lookup"><span data-stu-id="99463-121">**NULL** pointer argument.</span></span><br/>                      |
| <dl> <span data-ttu-id="99463-122"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="99463-122"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="99463-123">Tipo di supporto non valido.</span><span class="sxs-lookup"><span data-stu-id="99463-123">Invalid media type.</span></span><br/>                             |
| <dl> <span data-ttu-id="99463-124"><dt>**ERRORE DI RUNTIME DI VFW \_ E \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="99463-124"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl>   | <span data-ttu-id="99463-125">Si è verificato un errore di run-time.</span><span class="sxs-lookup"><span data-stu-id="99463-125">A run-time error occurred.</span></span><br/>                      |
| <dl> <span data-ttu-id="99463-126"><dt>**VFW \_ E \_ STATO \_ ERRATO**</dt></span><span class="sxs-lookup"><span data-stu-id="99463-126"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>     | <span data-ttu-id="99463-127">Il pin è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="99463-127">The pin is stopped.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="99463-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="99463-128">Remarks</span></span>

<span data-ttu-id="99463-129">Il pin di output upstream chiama questo metodo per recapitare un campione al pin di input.</span><span class="sxs-lookup"><span data-stu-id="99463-129">The upstream output pin calls this method to deliver a sample to the input pin.</span></span> <span data-ttu-id="99463-130">Il pin di input deve eseguire una delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="99463-130">The input pin must do one of the following:</span></span>

-   <span data-ttu-id="99463-131">Elaborare l'esempio prima della restituzione.</span><span class="sxs-lookup"><span data-stu-id="99463-131">Process the sample before returning.</span></span>
-   <span data-ttu-id="99463-132">Restituire ed elaborare l'esempio in un thread di lavoro.</span><span class="sxs-lookup"><span data-stu-id="99463-132">Return, and process the sample in a worker thread.</span></span>
-   <span data-ttu-id="99463-133">Rifiutare l'esempio.</span><span class="sxs-lookup"><span data-stu-id="99463-133">Reject the sample.</span></span>

<span data-ttu-id="99463-134">Se il pin usa un thread di lavoro per elaborare l'esempio, aggiungere un conteggio dei riferimenti all'esempio all'interno di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="99463-134">If the pin uses a worker thread to process the sample, add a reference count to the sample inside this method.</span></span> <span data-ttu-id="99463-135">Dopo la fine del metodo, il pin upstream rilascia l'esempio.</span><span class="sxs-lookup"><span data-stu-id="99463-135">After the method returns, the upstream pin releases the sample.</span></span> <span data-ttu-id="99463-136">Quando il conteggio dei riferimenti del campione raggiunge lo zero, il campione torna all'allocatore per il nuovo utilizzo.</span><span class="sxs-lookup"><span data-stu-id="99463-136">When the sample's reference count reaches zero, the sample returns to the allocator for re-use.</span></span>

<span data-ttu-id="99463-137">Questo metodo è sincrono e può bloccarsi.</span><span class="sxs-lookup"><span data-stu-id="99463-137">This method is synchronous and can block.</span></span> <span data-ttu-id="99463-138">Se il metodo potrebbe bloccarsi, il metodo [**CBaseInputPin::ReceiveCanBlock**](cbaseinputpin-receivecanblock.md) del pin deve restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="99463-138">If the method might block, the pin's [**CBaseInputPin::ReceiveCanBlock**](cbaseinputpin-receivecanblock.md) method should return S\_OK.</span></span>

<span data-ttu-id="99463-139">Nella classe di base questo metodo esegue i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="99463-139">In the base class, this method performs the following steps:</span></span>

1.  <span data-ttu-id="99463-140">Chiama il [**metodo CBaseInputPin::CheckStreaming**](cbaseinputpin-checkstreaming.md) per verificare che il pin sia in grado di elaborare gli esempi ora.</span><span class="sxs-lookup"><span data-stu-id="99463-140">Calls the [**CBaseInputPin::CheckStreaming**](cbaseinputpin-checkstreaming.md) method to verify that the pin can process samples now.</span></span> <span data-ttu-id="99463-141">Se non è possibile, ad esempio, se il pin viene arrestato, il metodo ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="99463-141">If it cannot for example, if the pin is stopped the method fails.</span></span>
2.  <span data-ttu-id="99463-142">Recupera le proprietà di esempio e controlla se il formato è stato modificato (vedere di seguito).</span><span class="sxs-lookup"><span data-stu-id="99463-142">Retrieves the sample properties and checks whether the format has changed (see below).</span></span>
3.  <span data-ttu-id="99463-143">Se il formato è stato modificato, il metodo chiama il metodo [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) per determinare se il nuovo formato è accettabile.</span><span class="sxs-lookup"><span data-stu-id="99463-143">If the format has changed, the method calls the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method to determine whether the new format is acceptable.</span></span>
4.  <span data-ttu-id="99463-144">Se il nuovo formato non è accettabile, il metodo chiama il metodo [**CBasePin::EndOfStream,**](cbasepin-endofstream.md) pubblica un evento \_ EC ERRORABORT e restituisce un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="99463-144">If the new format is not acceptable, the method calls the [**CBasePin::EndOfStream**](cbasepin-endofstream.md) method, posts an EC\_ERRORABORT event, and returns an error code.</span></span>
5.  <span data-ttu-id="99463-145">Supponendo che non siano presenti errori, il metodo restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="99463-145">Assuming there were no errors, the method returns S\_OK.</span></span>

<span data-ttu-id="99463-146">Verificare la modifica del formato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="99463-146">Test for a format change as follows:</span></span>

-   <span data-ttu-id="99463-147">Se l'esempio supporta [**l'interfaccia IMediaSample2,**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) controllare il **membro dwSampleFlags** della [**struttura AM \_ SAMPLE2 \_ PROPERTIES.**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties)</span><span class="sxs-lookup"><span data-stu-id="99463-147">If the sample supports the [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) interface, check the **dwSampleFlags** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span> <span data-ttu-id="99463-148">Se è presente il flag AM \_ SAMPLE \_ TYPECHANGED, il formato è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="99463-148">If the AM\_SAMPLE\_TYPECHANGED flag is present, the format has changed.</span></span>
-   <span data-ttu-id="99463-149">In caso contrario, se l'esempio non supporta **IMediaSample2,** chiamare il [**metodo IMediaSample::GetMediaType.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype)</span><span class="sxs-lookup"><span data-stu-id="99463-149">Otherwise, if the sample does not support **IMediaSample2**, call the [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) method.</span></span> <span data-ttu-id="99463-150">Se il metodo restituisce un valore non **NULL,** il formato è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="99463-150">If the method returns a non-**NULL** value, the format has changed.</span></span>

<span data-ttu-id="99463-151">Nella classe di base questo metodo non elabora l'esempio.</span><span class="sxs-lookup"><span data-stu-id="99463-151">In the base class, this method does not process the sample.</span></span> <span data-ttu-id="99463-152">La classe derivata deve eseguire l'override di questo metodo per eseguire l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="99463-152">The derived class must override this method to perform the processing.</span></span> <span data-ttu-id="99463-153">Ciò che ciò comporta dipende interamente dal filtro. La classe derivata deve chiamare il metodo della classe base per verificare la presenza degli errori descritti in precedenza.</span><span class="sxs-lookup"><span data-stu-id="99463-153">(What this entails depends entirely on the filter.) The derived class should call the base-class method, to check for the errors described previously.</span></span>

## <a name="requirements"></a><span data-ttu-id="99463-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99463-154">Requirements</span></span>



| <span data-ttu-id="99463-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="99463-155">Requirement</span></span> | <span data-ttu-id="99463-156">Valore</span><span class="sxs-lookup"><span data-stu-id="99463-156">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99463-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="99463-157">Header</span></span><br/>  | <dl> <span data-ttu-id="99463-158"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="99463-158"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="99463-159">Libreria</span><span class="sxs-lookup"><span data-stu-id="99463-159">Library</span></span><br/> | <dl> <span data-ttu-id="99463-160"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="99463-160"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99463-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="99463-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99463-162">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="99463-162">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




