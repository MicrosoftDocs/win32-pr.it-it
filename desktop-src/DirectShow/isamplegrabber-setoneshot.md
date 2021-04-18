---
description: Il metodo SetOneShot specifica se il filtro Grabber di esempio si interrompe dopo che il filtro riceve un campione.
ms.assetid: 7e3a3e8c-1834-425b-9657-279ab4451a2b
title: 'Metodo ISampleGrabber:: SetOneShot (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetOneShot
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 72a6e0e1798bcb8e19807619e982f487b0f04e6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327664"
---
# <a name="isamplegrabbersetoneshot-method"></a><span data-ttu-id="6623e-103">Metodo ISampleGrabber:: SetOneShot</span><span class="sxs-lookup"><span data-stu-id="6623e-103">ISampleGrabber::SetOneShot method</span></span>

> [!Note]  
> <span data-ttu-id="6623e-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="6623e-104">\[Deprecated.</span></span> <span data-ttu-id="6623e-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6623e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6623e-106">Il metodo **SetOneShot** specifica se il filtro [**grabber di esempio**](sample-grabber-filter.md) si interrompe dopo che il filtro riceve un campione.</span><span class="sxs-lookup"><span data-stu-id="6623e-106">The **SetOneShot** method specifies whether the [**Sample Grabber**](sample-grabber-filter.md) filter halts after the filter receives a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="6623e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6623e-107">Syntax</span></span>


```C++
HRESULT SetOneShot(
   BOOL OneShot
);
```



## <a name="parameters"></a><span data-ttu-id="6623e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6623e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6623e-109">*OneShot*</span><span class="sxs-lookup"><span data-stu-id="6623e-109">*OneShot*</span></span> 
</dt> <dd>

<span data-ttu-id="6623e-110">Valore booleano che specifica se il filtro Grabber di esempio si arresta dopo la ricezione di un campione.</span><span class="sxs-lookup"><span data-stu-id="6623e-110">A Boolean value that specifies whether the Sample Grabber filter halts after receiving a sample.</span></span>



| <span data-ttu-id="6623e-111">Valore</span><span class="sxs-lookup"><span data-stu-id="6623e-111">Value</span></span>                                                                                                                                    | <span data-ttu-id="6623e-112">Significato</span><span class="sxs-lookup"><span data-stu-id="6623e-112">Meaning</span></span>                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="6623e-113"><dt>TRUE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="6623e-113"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>    | <span data-ttu-id="6623e-114">Il grabber di esempio si arresta dopo il primo campione.</span><span class="sxs-lookup"><span data-stu-id="6623e-114">The Sample Grabber halts after the first sample.</span></span> <br/>                                                      |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="6623e-115"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="6623e-115"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="6623e-116">Dopo il primo esempio, il grabber di esempio continua a elaborare gli esempi.</span><span class="sxs-lookup"><span data-stu-id="6623e-116">After the first sample, the Sample Grabber continues to process samples.</span></span> <span data-ttu-id="6623e-117">Comportamento predefinito.</span><span class="sxs-lookup"><span data-stu-id="6623e-117">This is the default behavior.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6623e-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6623e-118">Return value</span></span>

<span data-ttu-id="6623e-119">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6623e-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6623e-120">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6623e-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6623e-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="6623e-121">Remarks</span></span>

<span data-ttu-id="6623e-122">Usare questo metodo per ottenere un singolo campione dal flusso, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="6623e-122">Use this method to get a single sample from the stream, as follows:</span></span>

1.  <span data-ttu-id="6623e-123">Chiamare **SetOneShot** con il valore **true**.</span><span class="sxs-lookup"><span data-stu-id="6623e-123">Call **SetOneShot** with the value **TRUE**.</span></span>
2.  <span data-ttu-id="6623e-124">Facoltativamente, usare l'interfaccia [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) per cercare una posizione nel flusso.</span><span class="sxs-lookup"><span data-stu-id="6623e-124">Optionally, use the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface to seek to a position in the stream.</span></span>
3.  <span data-ttu-id="6623e-125">Chiamare [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) per eseguire il grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="6623e-125">Call [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) to run the filter graph.</span></span>
4.  <span data-ttu-id="6623e-126">Chiamare [**IMediaEvent:: WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) per attendere che il grafico si interrompa.</span><span class="sxs-lookup"><span data-stu-id="6623e-126">Call [**IMediaEvent::WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) to wait for the graph to halt.</span></span> <span data-ttu-id="6623e-127">In alternativa, chiamare [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) per ottenere gli eventi del grafo, fino a quando non si riceve l'evento di [**\_ completamento EC**](ec-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="6623e-127">Alternatively, call [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) to get graph events, until you receive the [**EC\_COMPLETE**](ec-complete.md) event.</span></span>

<span data-ttu-id="6623e-128">Dopo l'arresto di Sample grabber, il grafico del filtro è ancora in stato di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6623e-128">After the Sample Grabber halts, the filter graph is still in a running state.</span></span> <span data-ttu-id="6623e-129">È possibile cercare o sospendere il grafo per ottenere un altro esempio.</span><span class="sxs-lookup"><span data-stu-id="6623e-129">You can seek or pause the graph to get another sample.</span></span>

> [!Note]  
> <span data-ttu-id="6623e-130">Una versione precedente della documentazione ha dichiarato che il grafico di filtro si interrompe dopo la ricezione dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="6623e-130">An earlier version of the documentation stated that the filter graph stops after the sample is received.</span></span> <span data-ttu-id="6623e-131">Questo non è accurato.</span><span class="sxs-lookup"><span data-stu-id="6623e-131">That is not accurate.</span></span> <span data-ttu-id="6623e-132">Il flusso termina, ma il grafo rimane nello stato in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6623e-132">The stream ends, but the graph remains in the running state.</span></span>

 

<span data-ttu-id="6623e-133">Il grabber di esempio implementa la modalità One-Shot chiamando [**Ipin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) sul filtro downstream e restituendo \_ false dal metodo [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) .</span><span class="sxs-lookup"><span data-stu-id="6623e-133">The Sample Grabber implements one-shot mode by calling [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) on the downstream filter and returning S\_FALSE from the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method of it.</span></span>

> [!Note]  
> <span data-ttu-id="6623e-134">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="6623e-134">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6623e-135">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6623e-135">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6623e-136">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="6623e-136">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6623e-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6623e-137">Requirements</span></span>



| <span data-ttu-id="6623e-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="6623e-138">Requirement</span></span> | <span data-ttu-id="6623e-139">Valore</span><span class="sxs-lookup"><span data-stu-id="6623e-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6623e-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6623e-140">Header</span></span><br/>  | <dl> <span data-ttu-id="6623e-141"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6623e-141"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6623e-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="6623e-142">Library</span></span><br/> | <dl> <span data-ttu-id="6623e-143"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6623e-143"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6623e-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6623e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6623e-145">Uso del grabber di esempio</span><span class="sxs-lookup"><span data-stu-id="6623e-145">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="6623e-146">**Interfaccia ISampleGrabber**</span><span class="sxs-lookup"><span data-stu-id="6623e-146">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




