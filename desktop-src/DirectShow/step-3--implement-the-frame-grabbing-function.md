---
description: Passaggio 3 implementare la funzione Frame-Grabbing
ms.assetid: 4ec2e4a4-3ab0-45f1-b29a-313599fe9e7d
title: Passaggio 3 implementare la funzione Frame-Grabbing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a97f585ff365e40ec611a9e11ce365839aa87be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883733"
---
# <a name="step-3-implement-the-frame-grabbing-function"></a><span data-ttu-id="907d7-103">Passaggio 3: implementare la funzione Frame-Grabbing</span><span class="sxs-lookup"><span data-stu-id="907d7-103">Step 3: Implement the Frame-Grabbing Function</span></span>

<span data-ttu-id="907d7-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="907d7-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="907d7-105">Questo argomento è il passaggio 3 relativo [all'acquisizione di un frame di poster](grabbing-a-poster-frame.md).</span><span class="sxs-lookup"><span data-stu-id="907d7-105">This topic is Step 3 of [Grabbing a Poster Frame](grabbing-a-poster-frame.md).</span></span>

<span data-ttu-id="907d7-106">Il passaggio successivo consiste nell'implementare la funzione GetBitmap, che usa il rilevatore multimediale per acquisire un frame di poster.</span><span class="sxs-lookup"><span data-stu-id="907d7-106">The next step is to implement the GetBitmap function, which uses the Media Detector to grab a poster frame.</span></span> <span data-ttu-id="907d7-107">All'interno di questa funzione, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="907d7-107">Inside this function, perform the following steps:</span></span>

1.  <span data-ttu-id="907d7-108">Creare il rilevatore multimediale.</span><span class="sxs-lookup"><span data-stu-id="907d7-108">Create the Media Detector.</span></span>
2.  <span data-ttu-id="907d7-109">Specificare un file multimediale.</span><span class="sxs-lookup"><span data-stu-id="907d7-109">Specify a media file.</span></span>
3.  <span data-ttu-id="907d7-110">Esaminare ogni flusso del file.</span><span class="sxs-lookup"><span data-stu-id="907d7-110">Examine each stream in the file.</span></span> <span data-ttu-id="907d7-111">Se si tratta di un flusso video, ottenere le dimensioni native del video.</span><span class="sxs-lookup"><span data-stu-id="907d7-111">If it is a video stream, get the native dimensions of the video.</span></span>
4.  <span data-ttu-id="907d7-112">Ottenere un frame di poster, specificando il tempo di ricerca e la dimensione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="907d7-112">Obtain a poster frame, specifying the seek time and the target dimension.</span></span>

<span data-ttu-id="907d7-113">Creare l'oggetto Media Detector chiamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance):</span><span class="sxs-lookup"><span data-stu-id="907d7-113">Create the Media Detector object by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance):</span></span>


```C++
CComPtr<IMediaDet> pDet;
hr = pDet.CoCreateInstance(__uuidof(MediaDet));
```



<span data-ttu-id="907d7-114">Specificare un nome file usando il metodo [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) .</span><span class="sxs-lookup"><span data-stu-id="907d7-114">Specify a file name, using the [**IMediaDet::put\_Filename**](imediadet-put-filename.md) method.</span></span> <span data-ttu-id="907d7-115">Questo metodo accetta un parametro **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="907d7-115">This method takes a **BSTR** parameter.</span></span>


```C++
hr = pDet->put_Filename(bstrFilename);
```



<span data-ttu-id="907d7-116">Ottenere il numero di flussi e scorrere ogni flusso controllando il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="907d7-116">Get the number of streams, and loop through each stream checking the media type.</span></span> <span data-ttu-id="907d7-117">Il metodo [**IMediaDet:: Get \_ OutputStreams**](imediadet-get-outputstreams.md) Recupera il numero di flussi e il metodo [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md) specifica quale flusso esaminare.</span><span class="sxs-lookup"><span data-stu-id="907d7-117">The [**IMediaDet::get\_OutputStreams**](imediadet-get-outputstreams.md) method retrieves the number of streams, and the [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md) method specifies which stream to examine.</span></span> <span data-ttu-id="907d7-118">Uscire dal ciclo sul primo flusso video.</span><span class="sxs-lookup"><span data-stu-id="907d7-118">Exit the loop on the first video stream.</span></span>


```C++
long lStreams;
bool bFound = false;
hr = pDet->get_OutputStreams(&lStreams);
for (long i = 0; i < lStreams; i++)
{
    GUID major_type;
    hr = pDet->put_CurrentStream(i);
    hr = pDet->get_StreamType(&major_type);
    if (major_type == MEDIATYPE_Video)  // Found a video stream.
    {
        bFound = true;
        break;
    }
}
if (!bFound) return VFW_E_INVALIDMEDIATYPE;
```



<span data-ttu-id="907d7-119">Se non è stato trovato alcun flusso video, la funzione viene chiusa.</span><span class="sxs-lookup"><span data-stu-id="907d7-119">If no video stream was found, the function exits.</span></span>

<span data-ttu-id="907d7-120">Nel codice precedente, il metodo [**IMediaDet:: Get \_ StreamType**](imediadet-get-streamtype.md) restituisce solo il tipo principale GUID.</span><span class="sxs-lookup"><span data-stu-id="907d7-120">In the previous code, the [**IMediaDet::get\_StreamType**](imediadet-get-streamtype.md) method returns just the major type GUID.</span></span> <span data-ttu-id="907d7-121">Questa operazione è utile se non è necessario esaminare il tipo di supporto completo.</span><span class="sxs-lookup"><span data-stu-id="907d7-121">This is convenient if you do not need to examine the complete media type.</span></span> <span data-ttu-id="907d7-122">Per ottenere le dimensioni del video, tuttavia, è necessario esaminare il blocco di formato, quindi è necessario il tipo di supporto completo.</span><span class="sxs-lookup"><span data-stu-id="907d7-122">To get the video dimensions, however, it is necessary to examine the format block, so the full media type is needed.</span></span> <span data-ttu-id="907d7-123">È possibile recuperarlo chiamando il metodo [**IMediaDet:: Get \_ StreamMediaType**](imediadet-get-streammediatype.md) , che compila una struttura del [**tipo di \_ supporto \_ am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="907d7-123">You can retrieve that by calling the [**IMediaDet::get\_StreamMediaType**](imediadet-get-streammediatype.md) method, which fills in an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="907d7-124">Il rilevatore multimediale converte tutti i flussi video in formato non compresso, con un blocco di formato [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="907d7-124">The Media Detector converts all video streams into uncompressed format, with a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) format block.</span></span>


```C++
long width = 0, height = 0; 
AM_MEDIA_TYPE mt;
hr = pDet->get_StreamMediaType(&mt);
if (mt.formattype == FORMAT_VideoInfo) 
{
    VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)(mt.pbFormat);
    width = pVih->bmiHeader.biWidth;
    height = pVih->bmiHeader.biHeight;
    
    // We want the absolute height, and don't care about up-down orientation.
    if (height < 0) height *= -1;
}
else {
    return VFW_E_INVALIDMEDIATYPE; // This should not happen, in theory.
}
FreeMediaType(mt);
```



<span data-ttu-id="907d7-125">Il metodo [**get \_ StreamMediaType**](imediadet-get-streammediatype.md) alloca il blocco di formato, che deve essere liberato dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="907d7-125">The [**get\_StreamMediaType**](imediadet-get-streammediatype.md) method allocates the format block, which the caller must free.</span></span> <span data-ttu-id="907d7-126">In questo esempio viene utilizzata la funzione [**FreeMediaType**](freemediatype.md) dalla libreria di classi di base.</span><span class="sxs-lookup"><span data-stu-id="907d7-126">This example uses the [**FreeMediaType**](freemediatype.md) function from the base class library.</span></span>

<span data-ttu-id="907d7-127">A questo punto si è pronti per ottenere il frame del poster.</span><span class="sxs-lookup"><span data-stu-id="907d7-127">Now you are ready to get the poster frame.</span></span> <span data-ttu-id="907d7-128">Chiamare prima il metodo [**IMediaDet:: GetBitmapBits**](imediadet-getbitmapbits.md) con un puntatore **null** per il buffer:</span><span class="sxs-lookup"><span data-stu-id="907d7-128">First call the [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md) method with a **NULL** pointer for the buffer:</span></span>


```C++
long lSize;
hr = pDet->GetBitmapBits(0, &lSize, NULL, width, height);
```



<span data-ttu-id="907d7-129">Questa chiamata restituisce le dimensioni del buffer richieste nel parametro *lSize* .</span><span class="sxs-lookup"><span data-stu-id="907d7-129">This call returns the required buffer size in the *lSize* parameter.</span></span> <span data-ttu-id="907d7-130">Il primo parametro specifica il tempo di flusso da ricercare; Questo esempio usa l'ora zero.</span><span class="sxs-lookup"><span data-stu-id="907d7-130">The first parameter specifies the stream time to seek to; this example uses time zero.</span></span> <span data-ttu-id="907d7-131">Per la larghezza e l'altezza, in questo esempio vengono usate le dimensioni video native ottenute in precedenza.</span><span class="sxs-lookup"><span data-stu-id="907d7-131">For the width and height, this example uses the native video dimensions obtained earlier.</span></span> <span data-ttu-id="907d7-132">Se si specificano altri valori, il rilevatore multimediale estenderà la bitmap per la corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="907d7-132">If you specify other values, the Media Detector will stretch the bitmap to match.</span></span>

<span data-ttu-id="907d7-133">Se il metodo ha esito positivo, allocare il buffer e chiamare di nuovo [**GetBitmapBits**](imediadet-getbitmapbits.md) :</span><span class="sxs-lookup"><span data-stu-id="907d7-133">If the method succeeds, allocate the buffer and call [**GetBitmapBits**](imediadet-getbitmapbits.md) again:</span></span>


```C++
if (SUCCEEDED(hr)) 
{
    char *pBuffer = new char[lSize];
    if (!pBuffer) return E_OUTOFMEMORY;
    hr = pDet->GetBitmapBits(0, NULL, pBuffer, width, height);
    if (FAILED(hr))
        delete [] pBuffer;
}
```



<span data-ttu-id="907d7-134">Di seguito è illustrata la funzione completa, con una gestione degli errori leggermente migliore.</span><span class="sxs-lookup"><span data-stu-id="907d7-134">Here is the complete function, with somewhat better error handling.</span></span>


```C++
HRESULT GetBitmap(LPTSTR pszFileName, BITMAPINFOHEADER** ppbmih)
{
    HRESULT hr;
    CComPtr<IMediaDet> pDet;
    hr = pDet.CoCreateInstance(__uuidof(MediaDet));
    if (FAILED(hr)) return hr;

    // Convert the file name to a BSTR.
    CComBSTR bstrFilename(pszFileName);
    hr = pDet->put_Filename(bstrFilename);
    if (FAILED(hr)) return hr;

    long lStreams;
    bool bFound = false;
    hr = pDet->get_OutputStreams(&lStreams);
    if (FAILED(hr)) return hr;

    for (long i = 0; i < lStreams; i++)
    {
        GUID major_type;
        hr = pDet->put_CurrentStream(i);
        if (SUCCEEDED(hr))
        {
            hr = pDet->get_StreamType(&major_type);
        }
        if (FAILED(hr)) break;

        if (major_type == MEDIATYPE_Video)
        {
            bFound = true;
            break;
        }
    }
    if (!bFound) return VFW_E_INVALIDMEDIATYPE;

    long width = 0, height = 0; 
    AM_MEDIA_TYPE mt;
    hr = pDet->get_StreamMediaType(&mt);
    if (SUCCEEDED(hr)) 
    {
        if ((mt.formattype == FORMAT_VideoInfo) && 
            (mt.cbFormat >= sizeof(VIDEOINFOHEADER)))
        {
            VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)(mt.pbFormat);
            width = pVih->bmiHeader.biWidth;
            height = pVih->bmiHeader.biHeight;
        
            // We want the absolute height, don't care about orientation.
            if (height < 0) height *= -1;
        }
        else
        {
            hr = VFW_E_INVALIDMEDIATYPE; // Should not happen, in theory.
        }
        FreeMediaType(mt);
    }
    if (FAILED(hr)) return hr;
    
    // Find the required buffer size.
    long size;
    hr = pDet->GetBitmapBits(0, &size, NULL, width, height);
    if (SUCCEEDED(hr)) 
    {
        char *pBuffer = new char[size];
        if (!pBuffer) return E_OUTOFMEMORY;
        try {
            hr = pDet->GetBitmapBits(0, NULL, pBuffer, width, height);
            if (SUCCEEDED(hr))
            {
                // Delete the old image, if any.
                if (*ppbmih) delete[] (*ppbmih);
                (*ppbmih) = (BITMAPINFOHEADER*)pBuffer;
            }
            else
            {
                delete [] pBuffer;
            }
        }
        catch (...) {
            delete [] pBuffer;
            return E_OUTOFMEMORY;
        }
    }
    return hr;
}
```



<span data-ttu-id="907d7-135">[Passaggio 4: creare la bitmap nell'area client](step-4--draw-the-bitmap-on-the-client-area.md)</span><span class="sxs-lookup"><span data-stu-id="907d7-135">Next: [Step 4: Draw the Bitmap on the Client Area](step-4--draw-the-bitmap-on-the-client-area.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="907d7-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="907d7-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="907d7-137">Acquisizione di un frame di poster</span><span class="sxs-lookup"><span data-stu-id="907d7-137">Grabbing a Poster Frame</span></span>](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
