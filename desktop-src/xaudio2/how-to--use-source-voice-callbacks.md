---
description: Quando si crea una voce di origine, è possibile passare una struttura che definisce i callback per determinati eventi audio. È possibile utilizzare questi callback per eseguire azioni o per segnalare altro codice.
ms.assetid: 0bace0c5-9171-efd8-9a38-2c2b3452f73f
title: 'Procedura: Usare callback di voci di origine'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c10005ed838a22ea0dfce59312d6f293c213c39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752423"
---
# <a name="how-to-use-source-voice-callbacks"></a><span data-ttu-id="4271a-104">Procedura: Usare callback di voci di origine</span><span class="sxs-lookup"><span data-stu-id="4271a-104">How to: Use Source Voice Callbacks</span></span>

<span data-ttu-id="4271a-105">Quando si crea una voce di origine, è possibile passare una struttura che definisce i callback per determinati eventi audio.</span><span class="sxs-lookup"><span data-stu-id="4271a-105">When you create a source voice, you can pass a structure to it that defines callbacks for certain audio events.</span></span> <span data-ttu-id="4271a-106">È possibile utilizzare questi callback per eseguire azioni o per segnalare altro codice.</span><span class="sxs-lookup"><span data-stu-id="4271a-106">You can use these callbacks to perform actions or to signal other code.</span></span>

1.  <span data-ttu-id="4271a-107">Creare una classe che erediti dall'interfaccia [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) .</span><span class="sxs-lookup"><span data-stu-id="4271a-107">Create a class that inherits from the [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) interface.</span></span> <span data-ttu-id="4271a-108">Tutte le funzioni membro di **IXAudio2VoiceCallback** sono puramente virtuali e devono essere definite.</span><span class="sxs-lookup"><span data-stu-id="4271a-108">All member functions of **IXAudio2VoiceCallback** are purely virtual, and must be defined.</span></span> <span data-ttu-id="4271a-109">L'unica funzione di interesse in questo esempio è [**OnStreamEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onstreamend).</span><span class="sxs-lookup"><span data-stu-id="4271a-109">The only function of interest in this example is [**OnStreamEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onstreamend).</span></span> <span data-ttu-id="4271a-110">Pertanto, le altre funzioni sono stub.</span><span class="sxs-lookup"><span data-stu-id="4271a-110">Therefore, the rest of the functions are stubs.</span></span> <span data-ttu-id="4271a-111">La funzione **OnStreamEnd** attiva un evento che indica che la riproduzione del suono è stata eseguita.</span><span class="sxs-lookup"><span data-stu-id="4271a-111">The **OnStreamEnd** function triggers an event that indicates the sound is done playing.</span></span>

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

    

2.  <span data-ttu-id="4271a-112">Creare una [**voce di origine**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) con [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) usando un'istanza della classe di callback creata in precedenza come parametro pCallback.</span><span class="sxs-lookup"><span data-stu-id="4271a-112">Create a [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) with [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) using an instance of the callback class created previously as the pCallback parameter.</span></span>

    ```
    VoiceCallback voiceCallback;
    if( FAILED(hr = pXaudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx,
                                 0, XAUDIO2_DEFAULT_FREQ_RATIO, &voiceCallback, NULL, NULL ) ) ) return;
    ```

    

3.  <span data-ttu-id="4271a-113">Dopo l'avvio della voce, usare il metodo [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) per attendere l'attivazione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="4271a-113">After starting the voice, use the [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) method to wait for the event to be triggered.</span></span>

    ```
    WaitForSingleObjectEx( voiceCallback.hBufferEndEvent, INFINITE, TRUE );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="4271a-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4271a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4271a-115">Callback</span><span class="sxs-lookup"><span data-stu-id="4271a-115">Callbacks</span></span>](callbacks.md)
</dt> <dt>

[<span data-ttu-id="4271a-116">Callback di XAudio2</span><span class="sxs-lookup"><span data-stu-id="4271a-116">XAudio2 Callbacks</span></span>](xaudio2-callbacks.md)
</dt> <dt>

[<span data-ttu-id="4271a-117">Guida alla programmazione di XAudio2</span><span class="sxs-lookup"><span data-stu-id="4271a-117">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="4271a-118">Procedura: Creare un grafico di elaborazione audio di base</span><span class="sxs-lookup"><span data-stu-id="4271a-118">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="4271a-119">Procedura: Trasmissione di un suono in un flusso da disco</span><span class="sxs-lookup"><span data-stu-id="4271a-119">How to: Stream a Sound from Disk</span></span>](how-to--stream-a-sound-from-disk.md)
</dt> </dl>

 

 
