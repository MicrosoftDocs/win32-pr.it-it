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
# <a name="step-3-implement-the-frame-grabbing-function"></a>Passaggio 3: implementare la funzione Frame-Grabbing

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Questo argomento è il passaggio 3 relativo [all'acquisizione di un frame di poster](grabbing-a-poster-frame.md).

Il passaggio successivo consiste nell'implementare la funzione GetBitmap, che usa il rilevatore multimediale per acquisire un frame di poster. All'interno di questa funzione, seguire questa procedura:

1.  Creare il rilevatore multimediale.
2.  Specificare un file multimediale.
3.  Esaminare ogni flusso del file. Se si tratta di un flusso video, ottenere le dimensioni native del video.
4.  Ottenere un frame di poster, specificando il tempo di ricerca e la dimensione di destinazione.

Creare l'oggetto Media Detector chiamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance):


```C++
CComPtr<IMediaDet> pDet;
hr = pDet.CoCreateInstance(__uuidof(MediaDet));
```



Specificare un nome file usando il metodo [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) . Questo metodo accetta un parametro **BSTR** .


```C++
hr = pDet->put_Filename(bstrFilename);
```



Ottenere il numero di flussi e scorrere ogni flusso controllando il tipo di supporto. Il metodo [**IMediaDet:: Get \_ OutputStreams**](imediadet-get-outputstreams.md) Recupera il numero di flussi e il metodo [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md) specifica quale flusso esaminare. Uscire dal ciclo sul primo flusso video.


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

Nel codice precedente, il metodo [**IMediaDet:: Get \_ StreamType**](imediadet-get-streamtype.md) restituisce solo il tipo principale GUID. Questa operazione è utile se non è necessario esaminare il tipo di supporto completo. Per ottenere le dimensioni del video, tuttavia, è necessario esaminare il blocco di formato, quindi è necessario il tipo di supporto completo. È possibile recuperarlo chiamando il metodo [**IMediaDet:: Get \_ StreamMediaType**](imediadet-get-streammediatype.md) , che compila una struttura del [**tipo di \_ supporto \_ am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . Il rilevatore multimediale converte tutti i flussi video in formato non compresso, con un blocco di formato [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .


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



Il metodo [**get \_ StreamMediaType**](imediadet-get-streammediatype.md) alloca il blocco di formato, che deve essere liberato dal chiamante. In questo esempio viene utilizzata la funzione [**FreeMediaType**](freemediatype.md) dalla libreria di classi di base.

A questo punto si è pronti per ottenere il frame del poster. Chiamare prima il metodo [**IMediaDet:: GetBitmapBits**](imediadet-getbitmapbits.md) con un puntatore **null** per il buffer:


```C++
long lSize;
hr = pDet->GetBitmapBits(0, &lSize, NULL, width, height);
```



Questa chiamata restituisce le dimensioni del buffer richieste nel parametro *lSize* . Il primo parametro specifica il tempo di flusso da ricercare; Questo esempio usa l'ora zero. Per la larghezza e l'altezza, in questo esempio vengono usate le dimensioni video native ottenute in precedenza. Se si specificano altri valori, il rilevatore multimediale estenderà la bitmap per la corrispondenza.

Se il metodo ha esito positivo, allocare il buffer e chiamare di nuovo [**GetBitmapBits**](imediadet-getbitmapbits.md) :


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



Di seguito è illustrata la funzione completa, con una gestione degli errori leggermente migliore.


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



[Passaggio 4: creare la bitmap nell'area client](step-4--draw-the-bitmap-on-the-client-area.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Acquisizione di un frame di poster](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
