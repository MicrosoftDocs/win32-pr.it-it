---
description: .
ms.assetid: 7f339ee8-01e6-4bbb-8563-020ff0e02499
title: Impostazione di DXVA-stati HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e539796aa5d3997b35739e75c80b438a7b5da50b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308999"
---
# <a name="setting-dxva-hd-states"></a>Impostazione di DXVA-stati HD

Durante l'elaborazione video, il dispositivo Microsoft DirectX Video Acceleration High Definition (DXVA-HD) mantiene uno stato persistente da un fotogramma a quello successivo. Ogni stato ha un valore predefinito documentato. Dopo aver configurato il dispositivo, impostare gli Stati che si desidera modificare rispetto alle impostazioni predefinite. Prima di elaborare ogni frame, aggiornare gli Stati che devono essere modificati.

> [!Note]  
> Questa progettazione è diversa da DXVA-VP. In DXVA-VP, l'applicazione deve specificare tutti i parametri VP con ciascun frame.

 

Gli Stati del dispositivo rientrano in due categorie:

-   Gli Stati del *flusso* applicano ogni flusso di input separatamente. È possibile applicare impostazioni diverse a ogni flusso.
-   Gli stati *blit* si applicano globalmente all'intera blit di elaborazione video.

Vengono definiti gli Stati di flusso seguenti.



| Stato del flusso                                   | Descrizione                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| **\_ \_ D3DFORMAT stato flusso \_ DXVAHD**           | Formato video di input.                                                                                             |
| **\_ \_ formato frame dello stato del flusso DXVAHD \_ \_**       | Interlacciamento.                                                                                                    |
| **\_ \_ \_ \_ spazio colore input stato flusso \_ DXVAHD** | Spazio colore di input. Questo stato specifica l'intervallo di colori RGB e la matrice di trasferimento YCbCr per il flusso di input. |
| **\_frequenza di \_ output dello stato del flusso \_ DXVAHD \_**        | Frequenza del frame di output. Questo stato controlla la conversione della frequenza del frame.                                                   |
| **\_ \_ \_ Rect origine stato flusso \_ DXVAHD**        | Rettangolo di origine.                                                                                               |
| **\_ \_ \_ Rect destinazione stato flusso \_ DXVAHD**   | Rettangolo di destinazione.                                                                                          |
| **\_ \_ alfa stato flusso \_ DXVAHD**               | Alfa planare.                                                                                                   |
| **\_ \_ tavolozza dello stato del flusso DXVAHD \_**             | Tavolozza dei colori. Questo stato è valido solo per i formati di input pallettizzati.                                             |
| **\_ \_ chiave Luma dello stato del flusso DXVAHD \_ \_**           | Chiave Luma.                                                                                                       |
| **proporzioni \_ \_ dello stato del flusso DXVAHD \_ \_**       | Proporzioni pixel.                                                                                             |
| **\_ \_ Filtro stato flusso \_ DXVAHD \_ xxxx**        | Impostazioni filtro immagine. Il driver può supportare la luminosità, il contrasto e altri filtri immagine.                    |



 

Sono definiti gli Stati blit seguenti:



| Stato blit                                   | Descrizione                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------|
| **DXVAHD \_ \_ destinazione stato \_ BLT \_ Rect**         | Rettangolo di destinazione.                                                            |
| **\_colore di \_ \_ sfondo stato BLT DXVAHD \_**    | Colore di sfondo.                                                            |
| **\_ \_ \_ spazio colore di output dello stato \_ di DXVAHD BLT \_** | Spazio colore di output.                                                          |
| **\_ \_ \_ riempimento alfa stato DXVAHD \_ BLT**          | Modalità di riempimento alfa.                                                             |
| **\_ \_ limitazione dello stato del BLT DXVAHD \_**         | Limitazioni. Questo stato controlla se il dispositivo downsampling delle l'output. |



 

Per impostare lo stato di un flusso, chiamare il metodo [**IDXVAHD \_ VideoProcessor:: SetVideoProcessStreamState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate) . Per impostare uno stato blit, chiamare il metodo [**IDXVAHD \_ VideoProcessor:: SetVideoProcessBltState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate) . In entrambi i metodi, un valore di enumerazione specifica lo stato da impostare. I dati relativi allo stato vengono forniti utilizzando una struttura di dati specifica dello stato, a cui l'applicazione esegue il cast a un tipo **void \*** .

Nell'esempio di codice seguente vengono impostati il formato di input e il rettangolo di destinazione per il flusso 0 e il colore di sfondo viene impostato su nero.


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

 

 



