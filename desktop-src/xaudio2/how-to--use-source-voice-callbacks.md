---
description: Quando si crea una voce di origine, è possibile passare una struttura che definisce i callback per determinati eventi audio. È possibile usare questi callback per eseguire azioni o segnalare altro codice.
ms.assetid: 0bace0c5-9171-efd8-9a38-2c2b3452f73f
title: 'Procedura: Usare callback di voci di origine'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fa19de67c8e02bfa4c283fac8677a7eae2325b074eef5d5f5c7db644b3f113a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583771"
---
# <a name="how-to-use-source-voice-callbacks"></a>Procedura: Usare callback di voci di origine

Quando si crea una voce di origine, è possibile passare una struttura che definisce i callback per determinati eventi audio. È possibile usare questi callback per eseguire azioni o segnalare altro codice.

1.  Creare una classe che eredita [**dall'interfaccia IXAudio2VoiceCallback.**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) Tutte le funzioni membro **di IXAudio2VoiceCallback** sono puramente virtuali e devono essere definite. L'unica funzione di interesse in questo esempio è [**OnStreamEnd.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onstreamend) Pertanto, il resto delle funzioni sono stub. La **funzione OnStreamEnd** attiva un evento che indica che la riproduzione del suono è stata completata.

    ```
    class VoiceCallback : public IXAudio2VoiceCallback
    {
    public:
        HANDLE hBufferEndEvent;
        VoiceCallback(): hBufferEndEvent( CreateEvent( NULL, FALSE, FALSE, NULL ) ){}
        ~VoiceCallback(){ CloseHandle( hBufferEndEvent ); }

        //Called when the voice has just finished playing a contiguous audio stream.
        void OnStreamEnd() { SetEvent( hBufferEndEvent ); }

        //Unused methods are stubs
        void OnVoiceProcessingPassEnd() { }
        void OnVoiceProcessingPassStart(UINT32 SamplesRequired) {    }
        void OnBufferEnd(void * pBufferContext)    { }
        void OnBufferStart(void * pBufferContext) {    }
        void OnLoopEnd(void * pBufferContext) {    }
        void OnVoiceError(void * pBufferContext, HRESULT Error) { }
    };
    ```

    

2.  Creare una [**voce di origine**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) con [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) usando un'istanza della classe di callback creata in precedenza come parametro pCallback.

    ```
    VoiceCallback voiceCallback;
    if( FAILED(hr = pXaudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx,
                                 0, XAUDIO2_DEFAULT_FREQ_RATIO, &voiceCallback, NULL, NULL ) ) ) return;
    ```

    

3.  Dopo aver avviato la voce, usare il [**metodo WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) per attendere l'attivazione dell'evento.

    ```
    WaitForSingleObjectEx( voiceCallback.hBufferEndEvent, INFINITE, TRUE );
    ```

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Callback](callbacks.md)
</dt> <dt>

[Callback di XAudio2](xaudio2-callbacks.md)
</dt> <dt>

[Guida alla programmazione di XAudio2](programming-guide.md)
</dt> <dt>

[Procedura: Creare un grafico di elaborazione audio di base](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Procedura: Trasmissione di un suono in un flusso da disco](how-to--stream-a-sound-from-disk.md)
</dt> </dl>

 

 
