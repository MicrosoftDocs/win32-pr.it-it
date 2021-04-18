---
description: Il metodo WriteBitmapBits recupera un frame video nel tempo di supporto specificato e lo scrive in un file. Il fotogramma video è sempre in formato RGB a 24 bit.
ms.assetid: 8b21f37b-553d-4de2-8725-c94c29fa3a1a
title: 'Metodo IMediaDet:: WriteBitmapBits (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.WriteBitmapBits
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 79bf54f136cc2ab9db1208ad6c2b4e5cb12bd950
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327821"
---
# <a name="imediadetwritebitmapbits-method"></a><span data-ttu-id="5c047-104">Metodo IMediaDet:: WriteBitmapBits</span><span class="sxs-lookup"><span data-stu-id="5c047-104">IMediaDet::WriteBitmapBits method</span></span>

> [!Note]  
> <span data-ttu-id="5c047-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="5c047-105">\[Deprecated.</span></span> <span data-ttu-id="5c047-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5c047-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5c047-107">Il `WriteBitmapBits` metodo recupera un frame video nel tempo di supporto specificato e lo scrive in un file.</span><span class="sxs-lookup"><span data-stu-id="5c047-107">The `WriteBitmapBits` method retrieves a video frame at the specified media time and writes it to a file.</span></span> <span data-ttu-id="5c047-108">Il fotogramma video è sempre in formato RGB a 24 bit.</span><span class="sxs-lookup"><span data-stu-id="5c047-108">The video frame is always in 24-bit RGB format.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c047-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c047-109">Syntax</span></span>


```C++
HRESULT WriteBitmapBits(
   double StreamTime,
   long   Width,
   long   Height,
   BSTR   Filename
);
```



## <a name="parameters"></a><span data-ttu-id="5c047-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="5c047-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c047-111">*StreamTime*</span><span class="sxs-lookup"><span data-stu-id="5c047-111">*StreamTime*</span></span> 
</dt> <dd>

<span data-ttu-id="5c047-112">Ora in cui recuperare il frame del video.</span><span class="sxs-lookup"><span data-stu-id="5c047-112">Time at which to retrieve the video frame.</span></span>

</dd> <dt>

<span data-ttu-id="5c047-113">*Larghezza*</span><span class="sxs-lookup"><span data-stu-id="5c047-113">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="5c047-114">Larghezza dell'immagine in pixel.</span><span class="sxs-lookup"><span data-stu-id="5c047-114">Width of the image, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="5c047-115">*Altezza*</span><span class="sxs-lookup"><span data-stu-id="5c047-115">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="5c047-116">Altezza, in pixel, dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="5c047-116">Height of the image, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="5c047-117">*Filename*</span><span class="sxs-lookup"><span data-stu-id="5c047-117">*Filename*</span></span> 
</dt> <dd>

<span data-ttu-id="5c047-118">Percorso del file in cui salvare la bitmap.</span><span class="sxs-lookup"><span data-stu-id="5c047-118">Path of the file in which to save the bitmap.</span></span> <span data-ttu-id="5c047-119">Se il file esiste già, questo metodo lo sovrascrive.</span><span class="sxs-lookup"><span data-stu-id="5c047-119">If the file already exists, this method overwrites it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c047-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5c047-120">Return value</span></span>

<span data-ttu-id="5c047-121">Restituisce \_ OK. l'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="5c047-121">Returns S\_OK it successful.</span></span> <span data-ttu-id="5c047-122">In caso contrario, restituisce un valore **HRESULT** che indica la cause dell'errore.</span><span class="sxs-lookup"><span data-stu-id="5c047-122">Otherwise, returns an **HRESULT** value that indicates the cause of the error.</span></span> <span data-ttu-id="5c047-123">I codici di errore possibili includono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="5c047-123">Possible error codes include the following:</span></span>



| <span data-ttu-id="5c047-124">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5c047-124">Return code</span></span>                                                                                             | <span data-ttu-id="5c047-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c047-125">Description</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5c047-126"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="5c047-126"><dt>**E\_NOINTERFACE**</dt></span></span> </dl>           | <span data-ttu-id="5c047-127">Non è stato possibile aggiungere il filtro [**grabber di esempio**](sample-grabber-filter.md) al grafo.</span><span class="sxs-lookup"><span data-stu-id="5c047-127">Could not add the [**Sample Grabber**](sample-grabber-filter.md) filter to the graph.</span></span><br/> |
| <dl> <span data-ttu-id="5c047-128"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="5c047-128"><dt>**E\_FAIL**</dt></span></span> </dl>                  | <span data-ttu-id="5c047-129">Esito negativo.</span><span class="sxs-lookup"><span data-stu-id="5c047-129">Failure.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="5c047-130"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="5c047-130"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>           | <span data-ttu-id="5c047-131">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="5c047-131">Insufficient memory.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="5c047-132"><dt>**E \_ imprevisto**</dt></span><span class="sxs-lookup"><span data-stu-id="5c047-132"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>            | <span data-ttu-id="5c047-133">Errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="5c047-133">Unexpected error.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="5c047-134"><dt>**STG \_ E \_ AccessDenied**</dt></span><span class="sxs-lookup"><span data-stu-id="5c047-134"><dt>**STG\_E\_ACCESSDENIED**</dt></span></span> </dl>     | <span data-ttu-id="5c047-135">Impossibile sovrascrivere il file.</span><span class="sxs-lookup"><span data-stu-id="5c047-135">Cannot overwrite file.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="5c047-136"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="5c047-136"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="5c047-137">Tipo di supporto non valido.</span><span class="sxs-lookup"><span data-stu-id="5c047-137">Invalid media type.</span></span><br/>                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="5c047-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c047-138">Remarks</span></span>

<span data-ttu-id="5c047-139">Prima di chiamare questo metodo, impostare il nome e il flusso del file chiamando [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) e [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="5c047-139">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="5c047-140">Questo metodo inserisce il rilevatore multimediale in modalità di cattura bitmap.</span><span class="sxs-lookup"><span data-stu-id="5c047-140">This method puts the media detector into bitmap grab mode.</span></span> <span data-ttu-id="5c047-141">Una volta che questo metodo è stato chiamato, i vari metodi di informazioni sui flussi in **IMediaDet** non funzionano, a meno che non si crei una nuova istanza del rilevamento multimediale.</span><span class="sxs-lookup"><span data-stu-id="5c047-141">Once this method has been called, the various stream information methods in **IMediaDet** do not work, unless you create a new instance of the media detector.</span></span>

> [!Note]  
> <span data-ttu-id="5c047-142">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="5c047-142">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5c047-143">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5c047-143">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5c047-144">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5c047-144">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5c047-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c047-145">Requirements</span></span>



| <span data-ttu-id="5c047-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c047-146">Requirement</span></span> | <span data-ttu-id="5c047-147">Valore</span><span class="sxs-lookup"><span data-stu-id="5c047-147">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c047-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c047-148">Header</span></span><br/>  | <dl> <span data-ttu-id="5c047-149"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c047-149"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5c047-150">Libreria</span><span class="sxs-lookup"><span data-stu-id="5c047-150">Library</span></span><br/> | <dl> <span data-ttu-id="5c047-151"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c047-151"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c047-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c047-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c047-153">**Interfaccia IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="5c047-153">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="5c047-154">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="5c047-154">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




