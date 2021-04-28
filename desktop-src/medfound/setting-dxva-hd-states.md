---
description: Impostazione degli stati DXVA-HD
ms.assetid: 7f339ee8-01e6-4bbb-8563-020ff0e02499
title: Impostazione degli stati DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91766e3eb10399d908ab361e13db4b94fe07b653
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092699"
---
# <a name="setting-dxva-hd-states"></a>Impostazione degli stati DXVA-HD

Durante l'elaborazione video, il dispositivo Microsoft DirectX Video Acceleration High Definition (DXVA-HD) mantiene uno stato permanente da un fotogramma a quello successivo. Ogni stato ha un valore predefinito documentato. Dopo aver configurato il dispositivo, impostare gli stati da modificare rispetto alle impostazioni predefinite. Prima di elaborare ogni frame, aggiornare gli stati che devono cambiare.

> [!Note]  
> Questa progettazione è diversa da DXVA-VP. In DXVA-VP l'applicazione deve specificare tutti i parametri VP con ogni frame.

 

Gli stati del dispositivo rientrano in due categorie:

-   *Gli stati* di flusso applicano ogni flusso di input separatamente. È possibile applicare impostazioni diverse a ogni flusso.
-   *Gli stati blit* si applicano a livello globale all'intero blit di elaborazione video.

Vengono definiti gli stati del flusso seguenti.



| Stato del flusso                                   | Descrizione                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| **DXVAHD \_ STREAM \_ STATE \_ D3DFORMAT**           | Formato video di input.                                                                                             |
| **FORMATO FRAME STATO FLUSSO DXVAHD \_ \_ \_ \_**       | Interlacciamento.                                                                                                    |
| **SPAZIO COLORE DI \_ \_ \_ INPUT \_ \_ DELLO STATO DEL FLUSSO DXVAHD** | Spazio colore di input. Questo stato specifica l'intervallo di colori RGB e la matrice di trasferimento YCbCr per il flusso di input. |
| **FREQUENZA DI OUTPUT DELLO \_ STATO \_ DEL FLUSSO \_ \_ DXVAHD**        | Frequenza dei fotogrammi di output. Questo stato controlla la conversione della frequenza dei fotogrammi.                                                   |
| **DXVAHD \_ STREAM \_ STATE \_ SOURCE \_ RECT**        | Rettangolo di origine.                                                                                               |
| **DXVAHD \_ STREAM \_ STATE \_ DESTINATION \_ RECT**   | Rettangolo di destinazione.                                                                                          |
| **DXVAHD \_ STREAM \_ STATE \_ ALPHA**               | Alfa planare.                                                                                                   |
| **TAVOLOZZA DELLO STATO DEL FLUSSO DXVAHD \_ \_ \_**             | Tavolozza. Questo stato si applica solo ai formati di input con svasato.                                             |
| **CHIAVE LUMA DELLO \_ STATO DEL FLUSSO \_ \_ DXVAHD \_**           | Tasto Luma.                                                                                                       |
| **PROPORZIONI DELLO STATO DEL FLUSSO DXVAHD \_ \_ \_ \_**       | Proporzioni pixel.                                                                                             |
| **DXVAHD \_ STREAM \_ STATE \_ FILTER \_ Xxxx**        | Impostazioni del filtro delle immagini. Il driver può supportare luminosità, contrasto e altri filtri di immagine.                    |



 

Sono definiti gli stati di blit seguenti:



| Stato blit                                   | Descrizione                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------|
| **DXVAHD \_ BLT \_ STATE \_ TARGET \_ RECT**         | Rettangolo di destinazione.                                                            |
| **COLORE DI SFONDO DELLO STATO BLT DXVAHD \_ \_ \_ \_**    | Colore di sfondo.                                                            |
| **SPAZIO COLORE DI OUTPUT DELLO STATO BLT DXVAHD \_ \_ \_ \_ \_** | Spazio colore di output.                                                          |
| **DXVAHD \_ BLT \_ STATE \_ ALPHA \_ FILL**          | Modalità di riempimento alfa.                                                             |
| **DXVAHD \_ BLT \_ STATE \_ CONSTRICTION**         | Costrizione. Questo stato controlla se il dispositivo sottocampiona l'output. |



 

Per impostare uno stato del flusso, chiamare il [**metodo IDXVAHD \_ VideoProcessor::SetVideoProcessStreamState.**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate) Per impostare uno stato blit, chiamare il [**metodo IDXVAHD \_ VideoProcessor::SetVideoProcessBltState.**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate) In entrambi questi metodi, un valore di enumerazione specifica lo stato da impostare. I dati sullo stato vengono dati usando una struttura di dati specifica dello stato, di cui l'applicazione esegue il cast in un **tipo void. \***

L'esempio di codice seguente imposta il formato di input e il rettangolo di destinazione per il flusso 0 e imposta il colore di sfondo su nero.


```C++
HRESULT SetDXVAHDStates(HWND hwnd, D3DFORMAT inputFormat)
{
    // Set the initial stream states.

    // Set the format of the input stream

    DXVAHD_STREAM_STATE_D3DFORMAT_DATA d3dformat = { inputFormat };

    HRESULT hr = g_pDXVAVP->SetVideoProcessStreamState(
        0,  // Stream index
        DXVAHD_STREAM_STATE_D3DFORMAT,
        sizeof(d3dformat),
        &d3dformat
        );

    if (SUCCEEDED(hr))
    { 
        // For this example, the input stream contains progressive frames.

        DXVAHD_STREAM_STATE_FRAME_FORMAT_DATA frame_format = { DXVAHD_FRAME_FORMAT_PROGRESSIVE };
        
        hr = g_pDXVAVP->SetVideoProcessStreamState(
            0, // Stream index
            DXVAHD_STREAM_STATE_FRAME_FORMAT,
            sizeof(frame_format),
            &frame_format
            );
    }

    if (SUCCEEDED(hr))
    { 
        // Compute the letterbox area.

        RECT rcDest;
        GetClientRect(hwnd, &rcDest);

        RECT rcSrc;
        SetRect(&rcSrc, 0, 0, VIDEO_WIDTH, VIDEO_HEIGHT);

        rcDest = LetterBoxRect(rcSrc, rcDest);

        // Set the destination rectangle, so the frame is displayed within the 
        // letterbox area. Otherwise, the frame is stretched to cover the 
        // entire surface.

        DXVAHD_STREAM_STATE_DESTINATION_RECT_DATA DstRect = { TRUE, rcDest };

        hr = g_pDXVAVP->SetVideoProcessStreamState(
            0, // Stream index 
            DXVAHD_STREAM_STATE_DESTINATION_RECT,
            sizeof(DstRect),
            &DstRect
            );
    }

    if (SUCCEEDED(hr))
    { 
        DXVAHD_COLOR_RGBA rgbBackground = { 0.0f, 0.0f, 0.0f, 1.0f };  // RGBA

        DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA background = { FALSE, rgbBackground };

        hr = g_pDXVAVP->SetVideoProcessBltState(
            DXVAHD_BLT_STATE_BACKGROUND_COLOR,
            sizeof (background),
            &background
            );
    }

    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DXVA-HD](dxva-hd.md)
</dt> </dl>

 

 



