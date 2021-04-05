---
title: Individuazione del formato di un file
description: Individuazione del formato di un file
ms.assetid: f1b3f811-8161-41ca-a92c-2735c0bec2e8
keywords:
- Windows Media Gestione dispositivi, formati di file
- Gestione dispositivi, formati di file
- Guida per programmatori, formati di file
- applicazioni desktop, formati di file
- creazione di applicazioni Windows Media Gestione dispositivi, formati di file
- scrittura di file in dispositivi, formati di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b06c963b01e3b681fd078d8685e1c788c73352e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709703"
---
# <a name="discovering-a-files-format"></a>Individuazione del formato di un file

Prima di inviare un file al dispositivo, un'applicazione deve determinare se il dispositivo supporta tale formato di file.

L'individuazione del formato di un file può essere complessa. Il modo più semplice consiste nel creare un elenco di estensioni di file di cui è stato eseguito il mapping a \_ valori di enumerazione WMDM FORMATCODE specifici. Tuttavia, esistono alcuni problemi con questo sistema: uno è che un singolo formato può avere più estensioni, ad esempio jpg, JPE e JPEG per le immagini JPEG. Inoltre, la stessa estensione di file può essere utilizzata da programmi diversi per formati diversi.

Per superare le limitazioni di un mapping rigoroso, è preferibile che in un'applicazione venga verificata la corrispondenza tra il formato e l'estensione. DirectShow SDK fornisce strumenti che consentono a un'applicazione di individuare un set limitato di dettagli sulla maggior parte dei tipi di file multimediali. Windows Media Format SDK espone un numero elevato di dettagli, ma solo i file ASF. Poiché tutti i tipi di file devono avere il codice di formato verificato se possibile, è quindi consigliabile usare DirectShow per individuare o verificare il codice del formato di base e usare Windows Media Format SDK per individuare eventuali metadati aggiuntivi che si desiderano sui file ASF. È inoltre possibile utilizzare DirectShow per individuare i metadati di base per i file non ASF.

Di seguito è riportato un modo per individuare un formato di file usando il mapping delle estensioni e DirectShow.

Per prima cosa, confrontare l'estensione del nome file con un elenco di estensioni note. Assicurarsi di eseguire il confronto senza distinzione tra maiuscole e minuscole. Se l'estensione non è mappata, impostare il formato su WMDM \_ FORMATCODE \_ undefined.

-   Se il codice di formato non è stato trovato (oppure si vuole verificare che un file sia un file multimediale), è possibile eseguire i passaggi seguenti:
    1.  Creare un oggetto di rilevamento multimediale DirectShow usando **CoCreateInstance**(CLSID \_ mediadet) e recuperare l'interfaccia **IMediaDet** .
    2.  Aprire il file chiamando **IMediaDet::p UT \_ filename**. La chiamata avrà esito negativo se il file è protetto.
    3.  Ottenere il tipo di supporto del flusso predefinito chiamando **IMediaDet:: Get \_ StreamMediaType**, che restituisce un **tipo di \_ supporto \_ am**.
    4.  Ottenere il numero di flussi chiamando **IMediaDet:: Get \_ OutputStreams**.
        -   Se è presente un solo flusso ed è audio, il tipo di file è WMDM \_ FORMATCODE \_ UNDEFINEDAUDIO
        -   Se è presente un solo flusso ed è video, il tipo di file è WMDM \_ FORMATCODE \_ UNDEFINEDVIDEO
        -   Se è presente un solo flusso ed è video e la velocità in bit è zero, il tipo di file è WMDM \_ FORMATCODE \_ WINDOWSIMAGEFORMAT.

È anche possibile provare a abbinare codec audio o video dai membri **VIDEOINFOHEADER** o **WAVEFORMATEX** recuperati da **get \_ StreamMediaType**.

La seguente funzione C++ illustra la corrispondenza dell'estensione di file e USA DirectShow per provare ad analizzare i file sconosciuti.


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

 

 




