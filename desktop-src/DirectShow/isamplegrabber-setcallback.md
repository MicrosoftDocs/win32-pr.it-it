---
description: Il metodo di callback specifica un metodo di callback da chiamare sugli esempi in arrivo.
ms.assetid: b84d3f52-b986-492a-a8b9-1d98618dcdd3
title: 'Metodo ISampleGrabber:: secallback (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetCallback
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 46e0565c314bab86967ee0d5dabee6ba449a87dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330505"
---
# <a name="isamplegrabbersetcallback-method"></a><span data-ttu-id="13a97-103">Metodo ISampleGrabber:: secallback</span><span class="sxs-lookup"><span data-stu-id="13a97-103">ISampleGrabber::SetCallback method</span></span>

> [!Note]  
> <span data-ttu-id="13a97-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="13a97-104">\[Deprecated.</span></span> <span data-ttu-id="13a97-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="13a97-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="13a97-106">Il **metodo di callback specifica** un metodo di callback da chiamare sugli esempi in arrivo.</span><span class="sxs-lookup"><span data-stu-id="13a97-106">The **SetCallback** method specifies a callback method to call on incoming samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="13a97-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="13a97-107">Syntax</span></span>


```C++
HRESULT SetCallback(
   ISampleGrabberCB *pCallback,
   long             WhichMethodToCallback
);
```



## <a name="parameters"></a><span data-ttu-id="13a97-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="13a97-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13a97-109">*pCallback*</span><span class="sxs-lookup"><span data-stu-id="13a97-109">*pCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="13a97-110">Puntatore a un'interfaccia [**ISampleGrabberCB**](isamplegrabbercb.md) contenente il metodo di callback o **null** per annullare il callback.</span><span class="sxs-lookup"><span data-stu-id="13a97-110">Pointer to an [**ISampleGrabberCB**](isamplegrabbercb.md) interface containing the callback method, or **NULL** to cancel the callback.</span></span>

</dd> <dt>

<span data-ttu-id="13a97-111">*WhichMethodToCallback*</span><span class="sxs-lookup"><span data-stu-id="13a97-111">*WhichMethodToCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="13a97-112">Indice che specifica il metodo di callback.</span><span class="sxs-lookup"><span data-stu-id="13a97-112">Index specifying the callback method.</span></span> <span data-ttu-id="13a97-113">Deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="13a97-113">Must be one of the following values.</span></span>



| <span data-ttu-id="13a97-114">Valore</span><span class="sxs-lookup"><span data-stu-id="13a97-114">Value</span></span> | <span data-ttu-id="13a97-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13a97-115">Description</span></span>                                                                                                                                                                                     |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13a97-116">0</span><span class="sxs-lookup"><span data-stu-id="13a97-116">0</span></span>     | <span data-ttu-id="13a97-117">Il filtro Grabber di esempio chiama il metodo [**ISampleGrabberCB:: SampleCB**](isamplegrabbercb-samplecb.md) .</span><span class="sxs-lookup"><span data-stu-id="13a97-117">The Sample Grabber filter calls the [**ISampleGrabberCB::SampleCB**](isamplegrabbercb-samplecb.md) method.</span></span> <span data-ttu-id="13a97-118">Questo metodo riceve un puntatore [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) .</span><span class="sxs-lookup"><span data-stu-id="13a97-118">This method receives an [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) pointer.</span></span>               |
| <span data-ttu-id="13a97-119">1</span><span class="sxs-lookup"><span data-stu-id="13a97-119">1</span></span>     | <span data-ttu-id="13a97-120">Il filtro Grabber di esempio chiama il metodo [**ISampleGrabberCB:: BufferCB**](isamplegrabbercb-buffercb.md) .</span><span class="sxs-lookup"><span data-stu-id="13a97-120">The Sample Grabber filter calls the [**ISampleGrabberCB::BufferCB**](isamplegrabbercb-buffercb.md) method.</span></span> <span data-ttu-id="13a97-121">Questo metodo riceve un puntatore al buffer contenuto nell'esempio multimediale.</span><span class="sxs-lookup"><span data-stu-id="13a97-121">This method receives a pointer to the buffer that is contained in the media sample.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13a97-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="13a97-122">Return value</span></span>

<span data-ttu-id="13a97-123">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="13a97-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="13a97-124">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="13a97-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="13a97-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="13a97-125">Remarks</span></span>

<span data-ttu-id="13a97-126">Il thread di elaborazione dati si blocca fino a quando il metodo di callback non viene restituito.</span><span class="sxs-lookup"><span data-stu-id="13a97-126">The data processing thread blocks until the callback method returns.</span></span> <span data-ttu-id="13a97-127">Se il callback non viene restituito rapidamente, può interferire con la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="13a97-127">If the callback does not return quickly, it can interfere with playback.</span></span>

<span data-ttu-id="13a97-128">Il filtro non richiama la funzione di callback per gli esempi di preroll o per gli esempi in cui il membro **dwStreamId** della struttura delle [**\_ \_ Proprietà SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) è diverso da quello dei flussi di dati am \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="13a97-128">The filter does not invoke the callback function for preroll samples, or for samples in which the **dwStreamId** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure is anything other than AM\_STREAM\_MEDIA.</span></span>

> [!Note]  
> <span data-ttu-id="13a97-129">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="13a97-129">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="13a97-130">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="13a97-130">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="13a97-131">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="13a97-131">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="13a97-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="13a97-132">Requirements</span></span>



| <span data-ttu-id="13a97-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="13a97-133">Requirement</span></span> | <span data-ttu-id="13a97-134">Valore</span><span class="sxs-lookup"><span data-stu-id="13a97-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13a97-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="13a97-135">Header</span></span><br/>  | <dl> <span data-ttu-id="13a97-136"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="13a97-136"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="13a97-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="13a97-137">Library</span></span><br/> | <dl> <span data-ttu-id="13a97-138"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="13a97-138"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13a97-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13a97-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13a97-140">Uso del grabber di esempio</span><span class="sxs-lookup"><span data-stu-id="13a97-140">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="13a97-141">**Interfaccia ISampleGrabber**</span><span class="sxs-lookup"><span data-stu-id="13a97-141">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




