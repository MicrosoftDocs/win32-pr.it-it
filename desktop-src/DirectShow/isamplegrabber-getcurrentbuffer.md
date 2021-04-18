---
description: Il metodo GetCurrentBuffer recupera una copia del buffer associato all'esempio più recente.
ms.assetid: 08550c82-4711-4725-9cd0-19b43cf4c92e
title: 'Metodo ISampleGrabber:: GetCurrentBuffer (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.GetCurrentBuffer
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d4df4c825761b42533590f10432bf62e5e4e0298
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330509"
---
# <a name="isamplegrabbergetcurrentbuffer-method"></a><span data-ttu-id="49de8-103">Metodo ISampleGrabber:: GetCurrentBuffer</span><span class="sxs-lookup"><span data-stu-id="49de8-103">ISampleGrabber::GetCurrentBuffer method</span></span>

> [!Note]  
> <span data-ttu-id="49de8-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="49de8-104">\[Deprecated.</span></span> <span data-ttu-id="49de8-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="49de8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="49de8-106">Il metodo **GetCurrentBuffer** recupera una copia del buffer associato all'esempio più recente.</span><span class="sxs-lookup"><span data-stu-id="49de8-106">The **GetCurrentBuffer** method retrieves a copy of the buffer associated with the most recent sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="49de8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="49de8-107">Syntax</span></span>


```C++
HRESULT GetCurrentBuffer(
  [in, out] long *pBufferSize,
  [out]     long *pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="49de8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="49de8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49de8-109">*pBufferSize* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="49de8-109">*pBufferSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="49de8-110">Puntatore alla dimensione del buffer.</span><span class="sxs-lookup"><span data-stu-id="49de8-110">Pointer to the size of the buffer.</span></span> <span data-ttu-id="49de8-111">Se *pbuffer* è **null**, questo parametro riceve le dimensioni del buffer richieste, in byte.</span><span class="sxs-lookup"><span data-stu-id="49de8-111">If *pBuffer* is **NULL**, this parameter receives the required buffer size, in bytes.</span></span> <span data-ttu-id="49de8-112">Se *pbuffer* non è **null**, impostare questo parametro in modo che corrisponda alla dimensione del buffer, in byte.</span><span class="sxs-lookup"><span data-stu-id="49de8-112">If *pBuffer* is not **NULL**, set this parameter equal to the size of the buffer, in bytes.</span></span> <span data-ttu-id="49de8-113">Nell'output il parametro riceve il numero di byte che sono stati copiati nel buffer.</span><span class="sxs-lookup"><span data-stu-id="49de8-113">On output, the parameter receives the number of bytes that were copied into the buffer.</span></span> <span data-ttu-id="49de8-114">Questo valore può essere inferiore alla dimensione del buffer.</span><span class="sxs-lookup"><span data-stu-id="49de8-114">This value might be smaller than the size of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="49de8-115">*pbuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="49de8-115">*pBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="49de8-116">Puntatore a una matrice di byte di dimensioni *pBufferSize* o **null**.</span><span class="sxs-lookup"><span data-stu-id="49de8-116">Pointer to an array of bytes of size *pBufferSize*, or **NULL**.</span></span> <span data-ttu-id="49de8-117">Se questo parametro non è **null**, il buffer corrente viene copiato nella matrice.</span><span class="sxs-lookup"><span data-stu-id="49de8-117">If this parameter is not **NULL**, the current buffer is copied into the array.</span></span> <span data-ttu-id="49de8-118">Se questo parametro è **null**, il parametro *pBufferSize* riceve le dimensioni del buffer richieste.</span><span class="sxs-lookup"><span data-stu-id="49de8-118">If this parameter is **NULL**, the *pBufferSize* parameter receives the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49de8-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49de8-119">Return value</span></span>

<span data-ttu-id="49de8-120">Restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="49de8-120">Returns one of the following values.</span></span>



| <span data-ttu-id="49de8-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="49de8-121">Return code</span></span>                                                                                           | <span data-ttu-id="49de8-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49de8-122">Description</span></span>                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="49de8-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="49de8-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="49de8-124">Gli esempi non vengono memorizzati nel buffer.</span><span class="sxs-lookup"><span data-stu-id="49de8-124">Samples are not being buffered.</span></span> <span data-ttu-id="49de8-125">Chiamare [**ISampleGrabber:: SetBufferSamples**](isamplegrabber-setbuffersamples.md).</span><span class="sxs-lookup"><span data-stu-id="49de8-125">Call [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md).</span></span><br/> |
| <dl> <span data-ttu-id="49de8-126"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="49de8-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>         | <span data-ttu-id="49de8-127">Il buffer specificato non è sufficientemente grande.</span><span class="sxs-lookup"><span data-stu-id="49de8-127">The specified buffer is not large enough.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="49de8-128"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="49de8-128"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="49de8-129">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="49de8-129">**NULL** pointer argument.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="49de8-130"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="49de8-130"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="49de8-131">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="49de8-131">Success.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="49de8-132"><dt>**VFW \_ E \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="49de8-132"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="49de8-133">Il filtro non è connesso.</span><span class="sxs-lookup"><span data-stu-id="49de8-133">The filter is not connected.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="49de8-134"><dt>**\_ \_ stato non corretto di VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="49de8-134"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>   | <span data-ttu-id="49de8-135">Il filtro non ha ancora ricevuto esempi.</span><span class="sxs-lookup"><span data-stu-id="49de8-135">The filter has not received any samples yet.</span></span> <span data-ttu-id="49de8-136">Per recapitare un esempio, eseguire o sospendere il grafo.</span><span class="sxs-lookup"><span data-stu-id="49de8-136">To deliver a sample, run or pause the graph.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="49de8-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="49de8-137">Remarks</span></span>

<span data-ttu-id="49de8-138">Per attivare il buffering, chiamare [**ISampleGrabber:: SetBufferSamples**](isamplegrabber-setbuffersamples.md) con il valore **true**.</span><span class="sxs-lookup"><span data-stu-id="49de8-138">To activate buffering, call [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) with a value of **TRUE**.</span></span>

<span data-ttu-id="49de8-139">Chiamare questo metodo due volte.</span><span class="sxs-lookup"><span data-stu-id="49de8-139">Call this method twice.</span></span> <span data-ttu-id="49de8-140">Alla prima chiamata, impostare *pbuffer* su **null**.</span><span class="sxs-lookup"><span data-stu-id="49de8-140">On the first call, set *pBuffer* to **NULL**.</span></span> <span data-ttu-id="49de8-141">La dimensione del buffer viene restituita in *pBufferSize*.</span><span class="sxs-lookup"><span data-stu-id="49de8-141">The size of the buffer is returned in *pBufferSize*.</span></span> <span data-ttu-id="49de8-142">Quindi allocare una matrice e chiamare di nuovo il metodo.</span><span class="sxs-lookup"><span data-stu-id="49de8-142">Then allocate an array and call the method again.</span></span> <span data-ttu-id="49de8-143">Alla seconda chiamata, passare le dimensioni della matrice in *pBufferSize* e passare l'indirizzo della matrice in *pbuffer*.</span><span class="sxs-lookup"><span data-stu-id="49de8-143">On the second call, pass the size of the array in *pBufferSize*, and pass the address of the array in *pBuffer*.</span></span> <span data-ttu-id="49de8-144">Se la matrice non è sufficientemente grande, il metodo restituisce E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="49de8-144">If the array is not large enough, the method returns E\_OUTOFMEMORY.</span></span>

<span data-ttu-id="49de8-145">Il parametro *pbuffer* è tipizzato come puntatore **Long** , ma il contenuto del buffer dipende dal formato dei dati.</span><span class="sxs-lookup"><span data-stu-id="49de8-145">The *pBuffer* parameter is typed as a **long** pointer, but the contents of the buffer depend on the format of the data.</span></span> <span data-ttu-id="49de8-146">Chiamare [**ISampleGrabber:: GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) per ottenere il tipo di supporto del formato.</span><span class="sxs-lookup"><span data-stu-id="49de8-146">Call [**ISampleGrabber::GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) to get the media type of the format.</span></span>

<span data-ttu-id="49de8-147">Non chiamare questo metodo mentre è in esecuzione il grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="49de8-147">Do not call this method while the filter graph is running.</span></span> <span data-ttu-id="49de8-148">Durante l'esecuzione del grafico del filtro, il filtro Grabber di esempio sovrascrive il contenuto del buffer ogni volta che viene ricevuto un nuovo esempio.</span><span class="sxs-lookup"><span data-stu-id="49de8-148">While the filter graph is running, the Sample Grabber filter overwrites the contents of the buffer whenever it receives a new sample.</span></span> <span data-ttu-id="49de8-149">Il modo migliore per utilizzare questo metodo consiste nell'utilizzare la modalità "One-Shot", che interrompe il grafico dopo la ricezione del primo campione.</span><span class="sxs-lookup"><span data-stu-id="49de8-149">The best way to use this method is to use "one-shot mode," which stops the graph after receiving the first sample.</span></span> <span data-ttu-id="49de8-150">Per impostare la modalità One-Shot, chiamare [**ISampleGrabber:: SetOneShot**](isamplegrabber-setoneshot.md).</span><span class="sxs-lookup"><span data-stu-id="49de8-150">To set one-shot mode, call [**ISampleGrabber::SetOneShot**](isamplegrabber-setoneshot.md).</span></span>

<span data-ttu-id="49de8-151">Il filtro non memorizza nel buffer gli esempi di preroll o gli esempi in cui il membro **dwStreamId** della struttura delle [**\_ \_ Proprietà SAMPLE2 di Am**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) è diverso da quello dei flussi di dati \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="49de8-151">The filter does not buffer preroll samples, or samples in which the **dwStreamId** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure is anything other than AM\_STREAM\_MEDIA.</span></span>

> [!Note]  
> <span data-ttu-id="49de8-152">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="49de8-152">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="49de8-153">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="49de8-153">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="49de8-154">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="49de8-154">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="49de8-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49de8-155">Requirements</span></span>



| <span data-ttu-id="49de8-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="49de8-156">Requirement</span></span> | <span data-ttu-id="49de8-157">Valore</span><span class="sxs-lookup"><span data-stu-id="49de8-157">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49de8-158">Intestazione</span><span class="sxs-lookup"><span data-stu-id="49de8-158">Header</span></span><br/>  | <dl> <span data-ttu-id="49de8-159"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="49de8-159"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="49de8-160">Libreria</span><span class="sxs-lookup"><span data-stu-id="49de8-160">Library</span></span><br/> | <dl> <span data-ttu-id="49de8-161"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="49de8-161"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49de8-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="49de8-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49de8-163">Uso del grabber di esempio</span><span class="sxs-lookup"><span data-stu-id="49de8-163">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="49de8-164">**Interfaccia ISampleGrabber**</span><span class="sxs-lookup"><span data-stu-id="49de8-164">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




