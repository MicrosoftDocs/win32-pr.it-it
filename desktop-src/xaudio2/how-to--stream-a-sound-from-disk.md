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
# <a name="how-to-stream-a-sound-from-disk"></a><span data-ttu-id="9d790-103">Procedura: Trasmissione di un suono in un flusso da disco</span><span class="sxs-lookup"><span data-stu-id="9d790-103">How to: Stream a Sound from Disk</span></span>

> [!Note]  
> <span data-ttu-id="9d790-104">Questo contenuto si applica solo alle app desktop e richiede la revisione per funzionare in un'app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9d790-104">This content applies only to desktop apps and will require revision to function in a Windows Store app.</span></span> <span data-ttu-id="9d790-105">Consultare la documentazione per **CreateFile2**, [CreateEventEx](/windows/win32/api/synchapi/nf-synchapi-createeventexa), [WaitForSingleObjectEx](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex), [SetFilePointerEx](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex)e **GetOverlappedResultEx**.</span><span class="sxs-lookup"><span data-stu-id="9d790-105">Please refer to the documentation for **CreateFile2**, [CreateEventEx](/windows/win32/api/synchapi/nf-synchapi-createeventexa), [WaitForSingleObjectEx](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex), [SetFilePointerEx](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex), and **GetOverlappedResultEx**.</span></span> <span data-ttu-id="9d790-106">Vedere l'esempio di StreamEffect per Windows 8 dalla [raccolta di esempi Windows SDK](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20stream%20effect%20sample%20(Windows%208)).</span><span class="sxs-lookup"><span data-stu-id="9d790-106">See the StreamEffect Windows 8 sample from the [Windows SDK Samples Gallery](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20stream%20effect%20sample%20(Windows%208)).</span></span>

 

<span data-ttu-id="9d790-107">È possibile trasmettere dati audio in XAudio2 creando un thread separato ed eseguendo letture del buffer dei dati audio nel thread di streaming, quindi usare i callback per controllare quel thread.</span><span class="sxs-lookup"><span data-stu-id="9d790-107">You can stream audio data in XAudio2 by creating a separate thread and perform buffer reads of the audio data in the streaming thread, and then use callbacks to control that thread.</span></span>

-   [<span data-ttu-id="9d790-108">Esecuzione delle letture del buffer nel thread di streaming</span><span class="sxs-lookup"><span data-stu-id="9d790-108">Performing buffer reads in the streaming thread</span></span>](#performing-buffer-reads-in-the-streaming-thread)
-   [<span data-ttu-id="9d790-109">Creazione della classe di callback</span><span class="sxs-lookup"><span data-stu-id="9d790-109">Creating the callback class</span></span>](#creating-the-callback-class)

## <a name="performing-buffer-reads-in-the-streaming-thread"></a><span data-ttu-id="9d790-110">Esecuzione delle letture del buffer nel thread di streaming</span><span class="sxs-lookup"><span data-stu-id="9d790-110">Performing buffer reads in the streaming thread</span></span>

<span data-ttu-id="9d790-111">Per eseguire le letture del buffer nel thread di streaming, attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="9d790-111">To perform buffer reads in the streaming thread follow these steps:</span></span>

1.  <span data-ttu-id="9d790-112">Creare una matrice di buffer di lettura.</span><span class="sxs-lookup"><span data-stu-id="9d790-112">Create an array of read buffers.</span></span>

    ```
    #define STREAMING_BUFFER_SIZE 65536
    #define MAX_BUFFER_COUNT 3
    BYTE buffers[MAX_BUFFER_COUNT][STREAMING_BUFFER_SIZE];
    ```

    

2.  <span data-ttu-id="9d790-113">Inizializzare una struttura SOVRAPPOSTa.</span><span class="sxs-lookup"><span data-stu-id="9d790-113">Initialize an OVERLAPPED structure.</span></span>

    <span data-ttu-id="9d790-114">La struttura viene utilizzata per verificare il completamento di una lettura asincrona del disco.</span><span class="sxs-lookup"><span data-stu-id="9d790-114">The structure is used to check when an asynchronous disk read has finished.</span></span>

    ```
    OVERLAPPED Overlapped = {0};
    Overlapped.hEvent = CreateEvent( NULL, TRUE, FALSE, NULL );
    ```

    

3.  <span data-ttu-id="9d790-115">Chiamare la funzione [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) sulla [**voce di origine**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) che riprodurrà l'audio di streaming.</span><span class="sxs-lookup"><span data-stu-id="9d790-115">Call the [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) function on the [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) that will be playing the streaming audio.</span></span>

    ```
    hr = pSourceVoice->Start( 0, 0 );
    ```

    

4.  <span data-ttu-id="9d790-116">Ciclo mentre la posizione di lettura corrente non è passata alla fine del file audio.</span><span class="sxs-lookup"><span data-stu-id="9d790-116">Loop while the current read position is not passed the end of the audio file.</span></span>

    ```
    CurrentDiskReadBuffer = 0;
    CurrentPosition = 0;
    while ( CurrentPosition < cbWaveSize )
    {
        ...
    }
    ```

    

    <span data-ttu-id="9d790-117">Nel ciclo eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="9d790-117">In the loop, do the following:</span></span>

    1.  <span data-ttu-id="9d790-118">Legge un blocco di dati dal disco nel buffer di lettura corrente.</span><span class="sxs-lookup"><span data-stu-id="9d790-118">Read a chunk of data from the disk into the current read buffer.</span></span>

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

        

    2.  <span data-ttu-id="9d790-119">Usare la funzione **GetOverlappedResult** per attendere l'evento che segnala che la lettura è stata completata.</span><span class="sxs-lookup"><span data-stu-id="9d790-119">Use the **GetOverlappedResult** function to wait for the event that signals the read has finished.</span></span>

        ```
        DWORD NumberBytesTransferred;
        ::GetOverlappedResult(hFile,&Overlapped,&NumberBytesTransferred, TRUE);
        ```

        

    3.  <span data-ttu-id="9d790-120">Attendere che il numero di buffer in coda nella voce di [**origine**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) sia inferiore al numero di buffer di lettura.</span><span class="sxs-lookup"><span data-stu-id="9d790-120">Wait for the number of buffers queued on the [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) to be less than the number of read buffers.</span></span>

        <span data-ttu-id="9d790-121">Lo stato della [**voce di origine**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) viene controllato con la funzione [**GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) .</span><span class="sxs-lookup"><span data-stu-id="9d790-121">The state of the [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) is checked with the [**GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) function.</span></span>

        ```
        XAUDIO2_VOICE_STATE state;
        while( pSourceVoice->GetState( &state ), state.BuffersQueued >= MAX_BUFFER_COUNT - 1)
        {
            WaitForSingleObject( Context.hBufferEndEvent, INFINITE );
        }
        ```

        

    4.  <span data-ttu-id="9d790-122">Inviare il buffer di lettura corrente alla [**voce di origine**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) usando la funzione [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) .</span><span class="sxs-lookup"><span data-stu-id="9d790-122">Submit the current read buffer to the [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) using the [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) function.</span></span>

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

        

    5.  <span data-ttu-id="9d790-123">Imposta l'indice del buffer di lettura corrente sul buffer successivo.</span><span class="sxs-lookup"><span data-stu-id="9d790-123">Set the current read buffer index to the next buffer.</span></span>

        ```
        CurrentDiskReadBuffer++;
        CurrentDiskReadBuffer %= MAX_BUFFER_COUNT;
        ```

        

5.  <span data-ttu-id="9d790-124">Al termine del ciclo, attendere il completamento della riproduzione dei rimanenti buffer in coda.</span><span class="sxs-lookup"><span data-stu-id="9d790-124">After the loop has finished, wait for the remaining queued buffers to finish playing.</span></span>

    <span data-ttu-id="9d790-125">Quando i buffer rimanenti hanno terminato la riproduzione, il suono si interrompe e il thread può uscire o essere riutilizzato per trasmettere un altro suono.</span><span class="sxs-lookup"><span data-stu-id="9d790-125">When the remaining buffers have finished playing, the sound stops, and the thread can exit or be reused to stream another sound.</span></span>

    ```
    XAUDIO2_VOICE_STATE state;
    while( pSourceVoice->GetState( &state ), state.BuffersQueued > 0 )
    {
        WaitForSingleObjectEx( Context.hBufferEndEvent, INFINITE, TRUE );
    }
    ```

    

## <a name="creating-the-callback-class"></a><span data-ttu-id="9d790-126">Creazione della classe di callback</span><span class="sxs-lookup"><span data-stu-id="9d790-126">Creating the callback class</span></span>

<span data-ttu-id="9d790-127">Per creare la classe di callback, creare una classe che erediti dall'interfaccia [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) .</span><span class="sxs-lookup"><span data-stu-id="9d790-127">To create the callback class, create a class that inherits from the [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) interface.</span></span>

<span data-ttu-id="9d790-128">La classe deve impostare un evento nel metodo [**OnBufferEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onbufferend) .</span><span class="sxs-lookup"><span data-stu-id="9d790-128">The class should set an event in its [**OnBufferEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onbufferend) method.</span></span> <span data-ttu-id="9d790-129">Ciò consente al thread di streaming di mettersi in stato di sospensione fino a quando l'evento non segnala che XAudio2 ha terminato la lettura da un buffer audio.</span><span class="sxs-lookup"><span data-stu-id="9d790-129">This allows the streaming thread to put itself to sleep until the event signals it that XAudio2 has finished reading from an audio buffer.</span></span> <span data-ttu-id="9d790-130">Per altre informazioni sull'uso dei callback con XAudio2, vedere [procedura: usare callback vocali di origine](how-to--use-source-voice-callbacks.md).</span><span class="sxs-lookup"><span data-stu-id="9d790-130">For more information about using callbacks with XAudio2, see [How to: Use Source Voice Callbacks](how-to--use-source-voice-callbacks.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="9d790-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9d790-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d790-132">Streaming di dati audio</span><span class="sxs-lookup"><span data-stu-id="9d790-132">Streaming Audio Data</span></span>](streaming-audio-data.md)
</dt> <dt>

[<span data-ttu-id="9d790-133">Callback di XAudio2</span><span class="sxs-lookup"><span data-stu-id="9d790-133">XAudio2 Callbacks</span></span>](callbacks.md)
</dt> <dt>

[<span data-ttu-id="9d790-134">Guida alla programmazione di XAudio2</span><span class="sxs-lookup"><span data-stu-id="9d790-134">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="9d790-135">Procedura: Creare un grafico di elaborazione audio di base</span><span class="sxs-lookup"><span data-stu-id="9d790-135">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="9d790-136">Procedura: Usare callback di voci di origine</span><span class="sxs-lookup"><span data-stu-id="9d790-136">How to: Use Source Voice Callbacks</span></span>](how-to--use-source-voice-callbacks.md)
</dt> </dl>

 

 
