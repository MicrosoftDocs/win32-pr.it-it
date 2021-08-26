---
description: Passaggio 3 Implementare la funzione Frame-Grabbing
ms.assetid: 4ec2e4a4-3ab0-45f1-b29a-313599fe9e7d
title: Passaggio 3 Implementare la funzione Frame-Grabbing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75410c48765e9437cd328a220ccbecf2c207bdaae5242a9e41060bc13fa02eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904096"
---
# <a name="step-3-implement-the-frame-grabbing-function"></a>Passaggio 3: Implementare la funzione Frame-Grabbing

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro.\]

Questo argomento è il passaggio 3 di [Grabbing a Poster Frame](grabbing-a-poster-frame.md).

Il passaggio successivo consiste nell'implementare la funzione GetBitmap, che usa Media Detector per afferrare un fotogramma poster. All'interno di questa funzione seguire questa procedura:

1.  Creare Media Detector.
2.  Specificare un file multimediale.
3.  Esaminare ogni flusso nel file. Se si tratta di un flusso video, ottenere le dimensioni native del video.
4.  Ottenere una cornice poster, specificando il tempo di ricerca e la dimensione di destinazione.

Creare l'oggetto Media Detector chiamando [**CoCreateInstance:**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)


```C++
CComPtr<IMediaDet> pDet;
hr = pDet.CoCreateInstance(__uuidof(MediaDet));
```



Specificare un nome file usando il [**metodo IMediaDet::p ut \_ Filename.**](imediadet-put-filename.md) Questo metodo accetta un **parametro BSTR.**


```C++
hr = pDet->put_Filename(bstrFilename);
```



Ottenere il numero di flussi e scorrere ogni flusso controllando il tipo di supporto. Il [**metodo IMediaDet::get \_ OutputStreams**](imediadet-get-outputstreams.md) recupera il numero di flussi e il metodo [**IMediaDet::p ut \_ CurrentStream**](imediadet-put-currentstream.md) specifica il flusso da esaminare. Uscire dal ciclo nel primo flusso video.


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



Se non è stato trovato alcun flusso video, la funzione viene chiusa.

Nel codice precedente il metodo [**IMediaDet::get \_ StreamType**](imediadet-get-streamtype.md) restituisce solo il GUID del tipo principale. Questa operazione risulta utile se non è necessario esaminare il tipo di supporto completo. Per ottenere le dimensioni video, tuttavia, è necessario esaminare il blocco di formato, quindi è necessario il tipo di supporto completo. È possibile recuperarlo chiamando il metodo [**IMediaDet::get \_ StreamMediaType,**](imediadet-get-streammediatype.md) che compila una [**struttura AM MEDIA \_ \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type) Media Detector converte tutti i flussi video in formato non compresso, con un [**blocco di formato VIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)


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



Il [**metodo get \_ StreamMediaType**](imediadet-get-streammediatype.md) alloca il blocco di formato che il chiamante deve liberare. Questo esempio usa la [**funzione FreeMediaType**](freemediatype.md) della libreria di classi di base.

A questo punto è possibile ottenere la cornice del poster. Chiamare prima il [**metodo IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md) con un **puntatore NULL** per il buffer:


```C++
long lSize;
hr = pDet->GetBitmapBits(0, &lSize, NULL, width, height);
```



Questa chiamata restituisce le dimensioni del buffer necessarie nel *parametro lSize.* Il primo parametro specifica il tempo di ricerca del flusso; Questo esempio usa l'ora zero. Per la larghezza e l'altezza, questo esempio usa le dimensioni video native ottenute in precedenza. Se si specificano altri valori, Media Detector estenderà la bitmap in modo che corrisponda.

Se il metodo ha esito positivo, allocare il buffer e [**chiamare di nuovo GetBitmapBits:**](imediadet-getbitmapbits.md)


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



Ecco la funzione completa, con una gestione degli errori leggermente migliore.


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



Passaggio [4: Disegnare la bitmap nell'area client](step-4--draw-the-bitmap-on-the-client-area.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Afferrare una cornice poster](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
