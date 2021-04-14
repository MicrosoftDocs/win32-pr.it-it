---
description: È possibile inviare una notifica al codice client di XAudio2 degli eventi del motore registrando un'istanza di una classe che implementa l'interfaccia IXAudio2EngineCallback con il motore XAudio2.
ms.assetid: 006a8cb6-c24c-f7d1-9e8b-9cb2baa046c0
title: 'Procedura: Usare callback del motore'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04adec0efd0625157740488d70be7896688d1176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104401771"
---
# <a name="how-to-use-engine-callbacks"></a><span data-ttu-id="40566-103">Procedura: Usare callback del motore</span><span class="sxs-lookup"><span data-stu-id="40566-103">How to: Use Engine Callbacks</span></span>

<span data-ttu-id="40566-104">È possibile inviare una notifica al codice client di XAudio2 degli eventi del motore registrando un'istanza di una classe che implementa l'interfaccia [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) con il motore XAudio2.</span><span class="sxs-lookup"><span data-stu-id="40566-104">You can notify the XAudio2 client code of engine events by registering an instance of a class implementing the [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) interface with the XAudio2 engine.</span></span> <span data-ttu-id="40566-105">Ciò consente al codice client di XAudio2 di tenere traccia del momento in cui si verifica l'elaborazione audio e quando riavviare il motore in caso di errore critico.</span><span class="sxs-lookup"><span data-stu-id="40566-105">This allows the XAudio2 client code to keep track of when audio processing is occurring, and when to restart the engine in the event of a critical error.</span></span>

## <a name="to-use-an-engine-callback"></a><span data-ttu-id="40566-106">Per usare un callback del motore</span><span class="sxs-lookup"><span data-stu-id="40566-106">To use an engine callback</span></span>

<span data-ttu-id="40566-107">Nei passaggi seguenti viene registrato un oggetto per gestire gli eventi del motore.</span><span class="sxs-lookup"><span data-stu-id="40566-107">The following steps register an object to handle engine events.</span></span>

1.  <span data-ttu-id="40566-108">Creare una classe che erediti dall'interfaccia [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) .</span><span class="sxs-lookup"><span data-stu-id="40566-108">Create a class that inherits from the [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) interface.</span></span>

    <span data-ttu-id="40566-109">Tutti i metodi di [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) sono puramente virtuali e devono essere definiti.</span><span class="sxs-lookup"><span data-stu-id="40566-109">All methods of [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) are purely virtual and must be defined.</span></span> <span data-ttu-id="40566-110">Il metodo di interesse in questo esempio è [**IXAudio2EngineCallback:: OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror), che imposta un flag per segnalare il ciclo del gioco principale in cui si è verificato un errore critico.</span><span class="sxs-lookup"><span data-stu-id="40566-110">The method of interest in this example is [**IXAudio2EngineCallback::OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror), which sets a flag to signal the main game loop that a critical error has occurred.</span></span> <span data-ttu-id="40566-111">I metodi rimanenti, [**IXAudio2EngineCallback:: OnProcessingPassStart**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassstart) e [**IXAudio2EngineCallback:: OnProcessingPassEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassend), sono stub in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="40566-111">The remaining methods, [**IXAudio2EngineCallback::OnProcessingPassStart**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassstart) and [**IXAudio2EngineCallback::OnProcessingPassEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassend), are stubs in this example.</span></span>

    ```
    class EngineCallback : public IXAudio2EngineCallback
    {
        void OnProcessingPassEnd () {}
        void OnProcessingPassStart() {}
        void OnCriticalError (HRESULT Error) {}
    };
    ```

    

2.  <span data-ttu-id="40566-112">Usare [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) per creare un'istanza del motore XAudio2.</span><span class="sxs-lookup"><span data-stu-id="40566-112">Use [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) to create an instance of the XAudio2 engine.</span></span>

    ```
    if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
        return hr;
    ```

    

3.  <span data-ttu-id="40566-113">Usare [**IXAudio2:: RegisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) per registrare il callback del motore.</span><span class="sxs-lookup"><span data-stu-id="40566-113">Use [**IXAudio2::RegisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) to register the engine callback.</span></span>

    ```
    pXAudio2->RegisterForCallbacks( &engineCallback );
    ```

    

4.  <span data-ttu-id="40566-114">Se il callback del motore non è più necessario, chiamare [**IXAudio2:: UnregisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-unregisterforcallbacks).</span><span class="sxs-lookup"><span data-stu-id="40566-114">If you don't need the engine callback any more, call [**IXAudio2::UnregisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-unregisterforcallbacks).</span></span>

    ```
    pXAudio2->UnregisterForCallbacks( &engineCallback );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="40566-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="40566-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40566-116">Callback</span><span class="sxs-lookup"><span data-stu-id="40566-116">Callbacks</span></span>](callbacks.md)
</dt> <dt>

[<span data-ttu-id="40566-117">Callback di XAudio2</span><span class="sxs-lookup"><span data-stu-id="40566-117">XAudio2 Callbacks</span></span>](xaudio2-callbacks.md)
</dt> <dt>

[<span data-ttu-id="40566-118">Guida alla programmazione di XAudio2</span><span class="sxs-lookup"><span data-stu-id="40566-118">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="40566-119">Procedura: Creare un grafico di elaborazione audio di base</span><span class="sxs-lookup"><span data-stu-id="40566-119">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="40566-120">Procedura: Trasmissione di un suono in un flusso da disco</span><span class="sxs-lookup"><span data-stu-id="40566-120">How to: Stream a Sound from Disk</span></span>](how-to--stream-a-sound-from-disk.md)
</dt> </dl>

 

 
