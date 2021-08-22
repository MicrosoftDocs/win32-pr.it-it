---
description: Il requisito minimo per consentire a XAudio2 di riprodurre dati audio è un grafico di elaborazione audio, costruito da una singola voce di mastering e una singola voce di origine.
ms.assetid: 40f79959-23c9-4513-363b-2f2fc85e4c0a
title: 'Procedura: Creare un grafico di elaborazione audio di base'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5bab39c878b37a6f89ef7598f6fa6b6eb1a997654373122fe3c3980bf12f160
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082961"
---
# <a name="how-to-build-a-basic-audio-processing-graph"></a>Procedura: Creare un grafico di elaborazione audio di base

Il requisito minimo per consentire a XAudio2 di riprodurre dati audio è un grafico di elaborazione audio, costruito da una singola voce di mastering e una singola voce di origine.

## <a name="to-build-a-basic-audio-processing-graph"></a>Per compilare un grafico di elaborazione audio di base

1.  Inizializzare il motore XAudio2 seguendo la procedura descritta in [Procedura: Inizializzare XAudio2.](how-to--initialize-xaudio2.md)
2.  Popolare una **struttura WAVEFORMATEX** e [**XAUDIO2 \_ BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) seguendo la procedura descritta in Procedura: Caricare file di dati [audio in XAudio2.](how-to--load-audio-data-files-in-xaudio2.md)
3.  Creare una voce di origine usando [**la funzione CreateSourceVoice.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice)

    Quando si specifica NULL per l'argomento pSendList di [**CreateSourceVoice,**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice)l'output della voce di origine passa alla voce di mastering creata nel passaggio 1.

    ```
    IXAudio2SourceVoice* pSourceVoice;
    if( FAILED(hr = pXAudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx,
                  0, XAUDIO2_DEFAULT_FREQ_RATIO, NULL, NULL, NULL ) ) ) return hr;
    ```

    

    Al termine di questo passaggio, è disponibile un semplice grafico audio costituito dalla voce di origine, dalla voce di mastering e dal dispositivo audio. I passaggi rimanenti di questo argomento illustrano come avviare il flusso di dati audio nel grafico.

    Un semplice grafo audio

    ![un semplice grafo audio.](images/xaudio2-audio-graph.png)

4.  Usare la funzione [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) per inviare un [**\_ buffer XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) alla voce di origine.

    ```
    if( FAILED(hr = pSourceVoice->SubmitSourceBuffer( &buffer ) ) )
        return hr;
    ```

    

5.  Usare la [**funzione Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) per avviare la voce di origine.

    ```
    if ( FAILED(hr = pSourceVoice->Start( 0, XAUDIO2_COMMIT_NOW ) ) )
        return hr;
    ```

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Grafici audio](audio-graphs.md)
</dt> <dt>

[Guida alla programmazione di XAudio2](programming-guide.md)
</dt> </dl>

 

 
