---
description: Il metodo GetBitmapBits recupera un frame video al momento del supporto specificato. Il frame restituito è sempre in formato RGB a 24 bit.
ms.assetid: b51df9d1-9c54-41bd-b0f8-ec290525deca
title: 'Metodo IMediaDet:: GetBitmapBits (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.GetBitmapBits
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 95aea5281f77b32868e0f0856bc63063e4f08639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332028"
---
# <a name="imediadetgetbitmapbits-method"></a><span data-ttu-id="a866a-104">Metodo IMediaDet:: GetBitmapBits</span><span class="sxs-lookup"><span data-stu-id="a866a-104">IMediaDet::GetBitmapBits method</span></span>

> [!Note]  
> <span data-ttu-id="a866a-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="a866a-105">\[Deprecated.</span></span> <span data-ttu-id="a866a-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a866a-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a866a-107">Il `GetBitmapBits` metodo recupera un frame video al momento del supporto specificato.</span><span class="sxs-lookup"><span data-stu-id="a866a-107">The `GetBitmapBits` method retrieves a video frame at the specified media time.</span></span> <span data-ttu-id="a866a-108">Il frame restituito è sempre in formato RGB a 24 bit.</span><span class="sxs-lookup"><span data-stu-id="a866a-108">The returned frame is always in 24-bit RGB format.</span></span>

## <a name="syntax"></a><span data-ttu-id="a866a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a866a-109">Syntax</span></span>


```C++
HRESULT GetBitmapBits(
   double StreamTime,
   long   *pBufferSize,
   char   *pBuffer,
   long   Width,
   long   Height
);
```



## <a name="parameters"></a><span data-ttu-id="a866a-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="a866a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a866a-111">*StreamTime*</span><span class="sxs-lookup"><span data-stu-id="a866a-111">*StreamTime*</span></span> 
</dt> <dd>

<span data-ttu-id="a866a-112">Tempo di recupero del fotogramma video, in secondi.</span><span class="sxs-lookup"><span data-stu-id="a866a-112">Time at which to retrieve the video frame, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="a866a-113">*pBufferSize*</span><span class="sxs-lookup"><span data-stu-id="a866a-113">*pBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="a866a-114">Riceve le dimensioni del buffer richieste.</span><span class="sxs-lookup"><span data-stu-id="a866a-114">Receives the required buffer size.</span></span> <span data-ttu-id="a866a-115">Se *pbuffer* è **null**, la variabile riceve la dimensione del buffer necessaria per recuperare il frame.</span><span class="sxs-lookup"><span data-stu-id="a866a-115">If *pBuffer* is **NULL**, the variable receives the size of the buffer needed to retrieve the frame.</span></span> <span data-ttu-id="a866a-116">Se *pbuffer* non è **null**, questo parametro viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="a866a-116">If *pBuffer* is not **NULL**, this parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="a866a-117">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="a866a-117">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="a866a-118">Puntatore a un buffer che riceve una struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) seguita dai bit DIB.</span><span class="sxs-lookup"><span data-stu-id="a866a-118">Pointer to a buffer that receives a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure followed by the DIB bits.</span></span>

</dd> <dt>

<span data-ttu-id="a866a-119">*Larghezza*</span><span class="sxs-lookup"><span data-stu-id="a866a-119">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="a866a-120">Larghezza dell'immagine video, in pixel.</span><span class="sxs-lookup"><span data-stu-id="a866a-120">Width of the video image, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="a866a-121">*Altezza*</span><span class="sxs-lookup"><span data-stu-id="a866a-121">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="a866a-122">Altezza dell'immagine video, in pixel.</span><span class="sxs-lookup"><span data-stu-id="a866a-122">Height of the video image, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a866a-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a866a-123">Return value</span></span>

<span data-ttu-id="a866a-124">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a866a-124">Returns an **HRESULT** value.</span></span> <span data-ttu-id="a866a-125">I possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a866a-125">Possible values include the following:</span></span>



| <span data-ttu-id="a866a-126">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a866a-126">Return code</span></span>                                                                                             | <span data-ttu-id="a866a-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a866a-127">Description</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a866a-128"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a866a-128"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="a866a-129">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="a866a-129">Success.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="a866a-130"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="a866a-130"><dt>**E\_NOINTERFACE**</dt></span></span> </dl>           | <span data-ttu-id="a866a-131">Non è stato possibile aggiungere il filtro [**grabber di esempio**](sample-grabber-filter.md) al grafo.</span><span class="sxs-lookup"><span data-stu-id="a866a-131">Could not add the [**Sample Grabber**](sample-grabber-filter.md) filter to the graph.</span></span><br/> |
| <dl> <span data-ttu-id="a866a-132"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="a866a-132"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>           | <span data-ttu-id="a866a-133">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="a866a-133">Insufficient memory.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="a866a-134"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="a866a-134"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="a866a-135">Errore puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="a866a-135">**NULL** pointer error.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="a866a-136"><dt>**E \_ imprevisto**</dt></span><span class="sxs-lookup"><span data-stu-id="a866a-136"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>            | <span data-ttu-id="a866a-137">Errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="a866a-137">Unexpected error.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="a866a-138"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="a866a-138"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="a866a-139">Tipo di supporto non valido.</span><span class="sxs-lookup"><span data-stu-id="a866a-139">Invalid media type.</span></span><br/>                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="a866a-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="a866a-140">Remarks</span></span>

<span data-ttu-id="a866a-141">Prima di chiamare questo metodo, impostare il nome e il flusso del file chiamando [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) e [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="a866a-141">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="a866a-142">Per determinare le dimensioni del buffer necessario, chiamare questo metodo con *pbuffer* uguale a **null**.</span><span class="sxs-lookup"><span data-stu-id="a866a-142">To determine the size of the buffer that is required, call this method with *pBuffer* equal to **NULL**.</span></span> <span data-ttu-id="a866a-143">La dimensione viene restituita nella variabile a cui punta *pBufferSize*.</span><span class="sxs-lookup"><span data-stu-id="a866a-143">The size is returned in the variable pointed to by *pBufferSize*.</span></span> <span data-ttu-id="a866a-144">Creare quindi il buffer e chiamare di nuovo il metodo, con *pbuffer* uguale all'indirizzo del buffer.</span><span class="sxs-lookup"><span data-stu-id="a866a-144">Then create the buffer and call the method again, with *pBuffer* equal to the address of the buffer.</span></span> <span data-ttu-id="a866a-145">Quando il metodo viene restituito, il buffer contiene una struttura **BITMAPINFOHEADER** seguita dalla bitmap.</span><span class="sxs-lookup"><span data-stu-id="a866a-145">When the method returns, the buffer contains a **BITMAPINFOHEADER** structure followed by the bitmap.</span></span> <span data-ttu-id="a866a-146">La bitmap viene ridimensionata alle dimensioni specificate nei parametri *Width* e *Height* .</span><span class="sxs-lookup"><span data-stu-id="a866a-146">The bitmap is scaled to the dimensions specified in the *Width* and *Height* parameters.</span></span>

<span data-ttu-id="a866a-147">Questo metodo inserisce il rilevatore multimediale in modalità di cattura bitmap.</span><span class="sxs-lookup"><span data-stu-id="a866a-147">This method puts the media detector into bitmap grab mode.</span></span> <span data-ttu-id="a866a-148">Una volta che questo metodo è stato chiamato, i vari metodi di informazioni sui flussi in **IMediaDet** non funzionano, a meno che non si crei una nuova istanza del rilevamento multimediale.</span><span class="sxs-lookup"><span data-stu-id="a866a-148">Once this method has been called, the various stream information methods in **IMediaDet** do not work, unless you create a new instance of the media detector.</span></span>

> [!Note]  
> <span data-ttu-id="a866a-149">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="a866a-149">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a866a-150">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a866a-150">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a866a-151">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a866a-151">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="examples"></a><span data-ttu-id="a866a-152">Esempio</span><span class="sxs-lookup"><span data-stu-id="a866a-152">Examples</span></span>

<span data-ttu-id="a866a-153">Il codice seguente usa il `GetBitmapBits` metodo per creare una bitmap indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a866a-153">The following code uses the `GetBitmapBits` method to create a device-independent bitmap.</span></span>


```C++
long size;
hr = pDet->GetBitmapBits(0, &size, 0, width, height);
if (SUCCEEDED(hr)) 
{
    char *pBuffer = new char[size];
    if (!pBuffer)
        return E_OUTOFMEMORY;
    try {
        hr = pDet->GetBitmapBits(0, 0, pBuffer, width, height);
    }
    catch (...) {
        delete [] pBuffer;
        throw;
    }
    if (SUCCEEDED(hr))
    {
        BITMAPINFOHEADER *bmih = (BITMAPINFOHEADER*)pBuffer;
        HDC hdcDest = GetDC(0);
        
        // Find the address of the start of the image data.
        void *pData = pBuffer + sizeof(BITMAPINFOHEADER);
        
        // Note: In general a BITMAPINFOHEADER can include extra color
        // information at the end, so calculating the offset to the image
        // data is not generally correct. However, the IMediaDet interface
        // always returns an RGB-24 image with no extra color information.
        
        BITMAPINFO bmi;
        ZeroMemory(&bmi, sizeof(BITMAPINFO));
        CopyMemory(&(bmi.bmiHeader), bmih, sizeof(BITMAPINFOHEADER));
        HBITMAP hBitmap = CreateDIBitmap(hdcDest, bmih, CBM_INIT, 
            pData, &bmi, DIB_RGB_COLORS);
    }
    delete[] pBuffer;
}
```



## <a name="requirements"></a><span data-ttu-id="a866a-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a866a-154">Requirements</span></span>



| <span data-ttu-id="a866a-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="a866a-155">Requirement</span></span> | <span data-ttu-id="a866a-156">Valore</span><span class="sxs-lookup"><span data-stu-id="a866a-156">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a866a-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a866a-157">Header</span></span><br/>  | <dl> <span data-ttu-id="a866a-158"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a866a-158"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a866a-159">Libreria</span><span class="sxs-lookup"><span data-stu-id="a866a-159">Library</span></span><br/> | <dl> <span data-ttu-id="a866a-160"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a866a-160"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a866a-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a866a-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a866a-162">**Interfaccia IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="a866a-162">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="a866a-163">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="a866a-163">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




