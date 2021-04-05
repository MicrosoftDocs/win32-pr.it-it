---
description: È possibile trasmettere dati audio in XAudio2 creando un thread separato ed eseguendo letture del buffer dei dati audio nel thread di streaming, quindi usare i callback per controllare quel thread.
ms.assetid: 48b80a66-91c1-973f-069b-6f63422d7154
title: 'Procedura: Trasmissione di un suono in un flusso da disco'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c5598e8913514d6b0bf81b55bab5b481dbc43b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757688"
---
# <a name="how-to-stream-a-sound-from-disk"></a>Procedura: Trasmissione di un suono in un flusso da disco

> [!Note]  
> Questo contenuto si applica solo alle app desktop e richiede la revisione per funzionare in un'app di Windows Store. Consultare la documentazione per **CreateFile2**, [CreateEventEx](/windows/win32/api/synchapi/nf-synchapi-createeventexa), [WaitForSingleObjectEx](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex), [SetFilePointerEx](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex)e **GetOverlappedResultEx**. Vedere l'esempio di StreamEffect per Windows 8 dalla [raccolta di esempi Windows SDK](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20stream%20effect%20sample%20(Windows%208)).

 

È possibile trasmettere dati audio in XAudio2 creando un thread separato ed eseguendo letture del buffer dei dati audio nel thread di streaming, quindi usare i callback per controllare quel thread.

-   [Esecuzione delle letture del buffer nel thread di streaming](#performing-buffer-reads-in-the-streaming-thread)
-   [Creazione della classe di callback](#creating-the-callback-class)

## <a name="performing-buffer-reads-in-the-streaming-thread"></a>Esecuzione delle letture del buffer nel thread di streaming

Per eseguire le letture del buffer nel thread di streaming, attenersi alla procedura seguente:

1.  Creare una matrice di buffer di lettura.

    ```
    #define STREAMING_BUFFER_SIZE 65536
    #define MAX_BUFFER_COUNT 3
    BYTE buffers[MAX_BUFFER_COUNT][STREAMING_BUFFER_SIZE];
    ```

    

2.  Inizializzare una struttura SOVRAPPOSTa.

    La struttura viene utilizzata per verificare il completamento di una lettura asincrona del disco.

    ```
    OVERLAPPED Overlapped = {0};
    Overlapped.hEvent = CreateEvent( NULL, TRUE, FALSE, NULL );
    ```

    

3.  Chiamare la funzione [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) sulla [**voce di origine**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) che riprodurrà l'audio di streaming.

    ```
    hr = pSourceVoice->Start( 0, 0 );
    ```

    

4.  Ciclo mentre la posizione di lettura corrente non è passata alla fine del file audio.

    ```
    CurrentDiskReadBuffer = 0;
    CurrentPosition = 0;
    while ( CurrentPosition < cbWaveSize )
    {
        ...
    }
    ```

    

    Nel ciclo eseguire le operazioni seguenti:

    1.  Legge un blocco di dati dal disco nel buffer di lettura corrente.

        ```
        DWORD dwRead;
        if( SUCCEEDED(hr) && 0 == ReadFile( hFile, pData, dwDataSize, &dwRead, pOverlapped ) )
            hr = HRESULT_FROM_WIN32( GetLastError() );
            DWORD cbValid = min( STREAMING_BUFFER_SIZE, cbWaveSize - CurrentPosition );
            DWORD dwRead;
            if( 0 == ReadFile( hFile, buffers[CurrentDiskReadBuffer], STREAMING_BUFFER_SIZE, &dwRead, &Overlapped ) )
                hr = HRESULT_FROM_WIN32( GetLastError() );
            Overlapped.Offset += cbValid;

            //update the file position to where it will be once the read finishes
            CurrentPosition += cbValid;
        ```

        

    2.  Usare la funzione **GetOverlappedResult** per attendere l'evento che segnala che la lettura è stata completata.

        ```
        DWORD NumberBytesTransferred;
        ::GetOverlappedResult(hFile,&Overlapped,&NumberBytesTransferred, TRUE);
        ```

        

    3.  Attendere che il numero di buffer in coda nella voce di [**origine**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) sia inferiore al numero di buffer di lettura.

        Lo stato della [**voce di origine**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) viene controllato con la funzione [**GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) .

        ```
        XAUDIO2_VOICE_STATE state;
        while( pSourceVoice->GetState( &state ), state.BuffersQueued >= MAX_BUFFER_COUNT - 1)
        {
            WaitForSingleObject( Context.hBufferEndEvent, INFINITE );
        }
        ```

        

    4.  Inviare il buffer di lettura corrente alla [**voce di origine**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) usando la funzione [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) .

        ```
        XAUDIO2_BUFFER buf = {0};
        buf.AudioBytes = cbValid;
        buf.pAudioData = buffers[CurrentDiskReadBuffer];
        if( CurrentPosition >= cbWaveSize )
        {
            buf.Flags = XAUDIO2_END_OF_STREAM;
        }
        pSourceVoice->SubmitSourceBuffer( &buf );
        ```

        

    5.  Imposta l'indice del buffer di lettura corrente sul buffer successivo.

        ```
        CurrentDiskReadBuffer++;
        CurrentDiskReadBuffer %= MAX_BUFFER_COUNT;
        ```

        

5.  Al termine del ciclo, attendere il completamento della riproduzione dei rimanenti buffer in coda.

    Quando i buffer rimanenti hanno terminato la riproduzione, il suono si interrompe e il thread può uscire o essere riutilizzato per trasmettere un altro suono.

    ```
    XAUDIO2_VOICE_STATE state;
    while( pSourceVoice->GetState( &state ), state.BuffersQueued > 0 )
    {
        WaitForSingleObjectEx( Context.hBufferEndEvent, INFINITE, TRUE );
    }
    ```

    

## <a name="creating-the-callback-class"></a>Creazione della classe di callback

Per creare la classe di callback, creare una classe che erediti dall'interfaccia [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) .

La classe deve impostare un evento nel metodo [**OnBufferEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onbufferend) . Ciò consente al thread di streaming di mettersi in stato di sospensione fino a quando l'evento non segnala che XAudio2 ha terminato la lettura da un buffer audio. Per altre informazioni sull'uso dei callback con XAudio2, vedere [procedura: usare callback vocali di origine](how-to--use-source-voice-callbacks.md).


```
struct StreamingVoiceContext : public IXAudio2VoiceCallback
{
    HANDLE hBufferEndEvent;
    StreamingVoiceContext(): hBufferEndEvent( CreateEvent( NULL, FALSE, FALSE, NULL ) ){}
    ~StreamingVoiceContext(){ CloseHandle( hBufferEndEvent ); }
    void OnBufferEnd( void* ){ SetEvent( hBufferEndEvent ); }
    ...
};
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Streaming di dati audio](streaming-audio-data.md)
</dt> <dt>

[Callback di XAudio2](callbacks.md)
</dt> <dt>

[Guida alla programmazione di XAudio2](programming-guide.md)
</dt> <dt>

[Procedura: Creare un grafico di elaborazione audio di base](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Procedura: Usare callback di voci di origine](how-to--use-source-voice-callbacks.md)
</dt> </dl>

 

 
