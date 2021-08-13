---
title: Individuazione del formato di un file
description: Individuazione del formato di un file
ms.assetid: f1b3f811-8161-41ca-a92c-2735c0bec2e8
keywords:
- Windows Gestione dispositivi multimediali, formati di file
- Gestione dispositivi, formati di file
- guida per programmatori, formati di file
- applicazioni desktop, formati di file
- creazione Windows applicazioni di Gestione dispositivi multimediali,formati di file
- scrittura di file in dispositivi, formati di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83706a3026968a694d3629551d310db9021b7f8c8118f3d98621751a95af26b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585330"
---
# <a name="discovering-a-files-format"></a>Individuazione del formato di un file

Prima di inviare un file al dispositivo, un'applicazione deve determinare se il dispositivo supporta tale formato di file.

L'individuazione del formato di un file può essere complessa. Il modo più semplice è creare un elenco di estensioni di file mappate a valori di enumerazione WMDM \_ FORMATCODE specifici. Esistono tuttavia alcuni problemi con questo sistema: uno è che un singolo formato può avere più estensioni,ad esempio .jpg, jpe e jpeg per le immagini JPEG. Inoltre, la stessa estensione di file può essere usata da programmi diversi per formati diversi.

Per superare le limitazioni di un mapping rigoroso, è meglio che un'applicazione verifichi che il formato corrisponda all'estensione. L DirectShow SDK fornisce strumenti che consentono a un'applicazione di individuare un set limitato di dettagli sulla maggior parte dei tipi di file multimediali. L Windows Media Format SDK espone un numero elevato di dettagli, ma solo sui file ASF. Poiché tutti i tipi di file devono avere il codice di formato verificato, se possibile, è consigliabile usare DirectShow per individuare o verificare il codice di formato di base e usare Windows Media Format SDK per individuare eventuali metadati aggiuntivi desiderati sui file ASF. DirectShow può essere usato anche per individuare i metadati di base per i file non ASF.

Di seguito è riportato un modo per individuare un formato di file usando il mapping delle estensioni e DirectShow.

Prima di tutto, confrontare l'estensione di file con un elenco di estensioni note. Assicurarsi di fare in modo che il confronto non eserciti la distinzione tra maiuscole e minuscole. Se non è stato eseguito il mapping dell'estensione, impostare il formato su WMDM \_ FORMATCODE \_ UNDEFINED.

-   Se il codice di formato non è stato trovato o si vuole verificare che un file sia un file multimediale, è possibile seguire questa procedura:
    1.  Creare un DirectShow media detector usando **CoCreateInstance**(CLSID \_ MediaDet) e recuperando l'interfaccia **IMediaDet.**
    2.  Aprire il file chiamando **IMediaDet::p ut \_ Filename**. Questa chiamata avrà esito negativo se il file è protetto.
    3.  Ottenere il tipo di supporto del flusso predefinito chiamando **IMediaDet::get \_ StreamMediaType**, che restituisce **am MEDIA \_ \_ TYPE**.
    4.  Ottenere il numero di flussi chiamando **IMediaDet::get \_ OutputStreams**.
        -   Se è presente un solo flusso e si tratta di audio, il tipo di file è WMDM \_ FORMATCODE \_ UNDEFINEDAUDIO
        -   Se è presente un solo flusso ed è video, il tipo di file è WMDM \_ FORMATCODE \_ UNDEFINEDVIDEO
        -   Se è presente un solo flusso ed è video e la velocità in bit è zero, il tipo di file è WMDM \_ FORMATCODE \_ WINDOWSIMAGEFORMAT.

È anche possibile provare a trovare i codec audio o video corrispondenti dai **membri VIDEOINFOHEADER** o **WAVEFORMATEX** recuperati da **get \_ StreamMediaType**.

La funzione C++ seguente illustra la corrispondenza delle estensioni di file e DirectShow per provare ad analizzare i file sconosciuti.


```C++
// For IMediaDet, you must link to strmiids.lib. Also include the following:
//#include <Qedit.h>  // for IMediaDet declaration.
//#include <Dshow.h>  // for VIDEOINFOHEADER declaration.
WMDM_FORMATCODE CWMDMController::myGetWMDM_FORMATCODE(LPCWSTR pFileName)
{
    HRESULT hr = S_OK;

    // Declare the variable to hold the WMDM format code.
    WMDM_FORMATCODE fmt = WMDM_FORMATCODE_UNDEFINED;
    
    // Get the file extension.
    wstring ext = pFileName;
    ext = ext.substr(ext.find_last_of(L".") + 1);

    // This is not an exhaustive list. 
    // It is also case-sensitive.
    if (ext == L"js" || ext == L"vb")
        fmt = WMDM_FORMATCODE_SCRIPT;
    else if (ext == L".exe")
        fmt = WMDM_FORMATCODE_EXECUTABLE;
    else if (ext == L"txt")
        fmt = WMDM_FORMATCODE_TEXT;
    else if (ext == L"html" || ext == L"htm" || ext == L"shtm")
        fmt = WMDM_FORMATCODE_HTML;
    else if (ext == L"aiff")
        fmt = WMDM_FORMATCODE_AIFF;
    else if (ext == L"wav")
        fmt = WMDM_FORMATCODE_WAVE;
    else if (ext == L"mp3")
        fmt = WMDM_FORMATCODE_MP3;
    else if (ext == L"mpg" || ext == L"mpeg" || ext == L"mp2")
        fmt = WMDM_FORMATCODE_MPEG;
    else if (ext == L"bmp")
        fmt = WMDM_FORMATCODE_IMAGE_BMP;
    else if (ext == L"avi")
        fmt = WMDM_FORMATCODE_AVI;
    else if (ext == L"asf")
        fmt = WMDM_FORMATCODE_ASF;
    else if (ext == L"tif")
        fmt = WMDM_FORMATCODE_IMAGE_TIFF;
    else if (ext == L"gif")
        fmt = WMDM_FORMATCODE_IMAGE_GIF;
    else if (ext == L"pct")
        fmt = WMDM_FORMATCODE_IMAGE_PICT;
    else if (ext == L"png")
        fmt = WMDM_FORMATCODE_IMAGE_PNG;
    else if (ext == L"wma")
        fmt = WMDM_FORMATCODE_WMA;
    else if (ext == L"wpl")
        fmt = WMDM_FORMATCODE_WPLPLAYLIST;
    else if (ext == L"asx")
        fmt = WMDM_FORMATCODE_ASXPLAYLIST;
    else if (ext == L"m3u")
        fmt = WMDM_FORMATCODE_M3UPLAYLIST;
    else if (ext == L"wmv")
        fmt = WMDM_FORMATCODE_WMV;
    else if (ext == L"jpg" || ext == L"jpeg" || ext == L"jpe")
        fmt = WMDM_FORMATCODE_IMAGE_EXIF;
    else if (ext == L"jp2")
        fmt = WMDM_FORMATCODE_IMAGE_JP2;
    else if (ext == L"jpx" || ext == L"jpf")
        fmt = WMDM_FORMATCODE_IMAGE_JPX;

    // If we couldn't get the type from the extension, perhaps DirectShow 
    // can determine the type. You could also modify this to verify that 
    // the major media type matches the file extension (for example, that 
    // a .gif file has a video image stream with a bit rate of zero).
    if (fmt == WMDM_FORMATCODE_UNDEFINED)
    {
        CComPtr<IMediaDet> pIMediaDet;
        hr = pIMediaDet.CoCreateInstance(CLSID_MediaDet, NULL);
        if (hr == S_OK && pIMediaDet != NULL)
        {
            hr = pIMediaDet->put_Filename(BSTR(pFileName));
            if (FAILED(hr)) return WMDM_FORMATCODE_UNDEFINED;

            AM_MEDIA_TYPE mediaType;
            if (hr == S_OK)
            {
                hr = pIMediaDet->get_StreamMediaType(&mediaType);
                CHECK_HR(hr, 
                  "get_StreamMediaType succeeded in myGetWMDM_FORMATCODE.", 
                  "get_StreamMediaType failed in myGetWMDM_FORMATCODE.");
            }

            if (hr == S_OK)
            {
                LONG numStreams = 0;
                hr = pIMediaDet->get_OutputStreams(&numStreams);

                // If there is at least one video stream, the file is video. 
                // If there are only audio streams, it is audio.
                // Loop through all streams or until first video stream is found.
                for (int i = 0; i < numStreams; i++)
                {
                    // Choices are either VIDEOINFOHEADER or WAVEFORMATEX. 
                    // VIDEOINFOHEADER2 is not supported.
                    if (IsEqualGUID(mediaType.formattype, 
                        FORMAT_VideoInfo))
                    {
                        VIDEOINFOHEADER* data = 
                            (VIDEOINFOHEADER*) mediaType.pbFormat;

                        // If only one stream and there was no matching 
                        // extension, it is undefined video. If no 
                        // bit rate, it's a still image.
                        if (data->dwBitRate == 0) fmt = 
                            WMDM_FORMATCODE_WINDOWSIMAGEFORMAT;
                        else fmt = WMDM_FORMATCODE_UNDEFINEDVIDEO;
                        break; // Found video--any additional streams are soundtracks.
                    }
                    if (IsEqualGUID(mediaType.formattype, FORMAT_WaveFormatEx))
                    {
                        // If only one stream and there was no matching 
                        // extension, it is undefined audio. 
                        if (fmt == WMDM_FORMATCODE_UNDEFINED)
                        {
                            fmt = WMDM_FORMATCODE_UNDEFINEDAUDIO;
                        }
                        WAVEFORMATEX* data = 
                            (WAVEFORMATEX*) mediaType.pbFormat;
                    }
                } // Loop through streams.
            }     // Got a stream media type.
        }         // Created a media detector object.
    }
    return fmt;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Scrittura di file nel dispositivo**](writing-files-to-the-device.md)
</dt> </dl>

 

 




