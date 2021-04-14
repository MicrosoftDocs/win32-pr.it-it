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
# <a name="how-to-use-engine-callbacks"></a>Procedura: Usare callback del motore

È possibile inviare una notifica al codice client di XAudio2 degli eventi del motore registrando un'istanza di una classe che implementa l'interfaccia [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) con il motore XAudio2. Ciò consente al codice client di XAudio2 di tenere traccia del momento in cui si verifica l'elaborazione audio e quando riavviare il motore in caso di errore critico.

## <a name="to-use-an-engine-callback"></a>Per usare un callback del motore

Nei passaggi seguenti viene registrato un oggetto per gestire gli eventi del motore.

1.  Creare una classe che erediti dall'interfaccia [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) .

    Tutti i metodi di [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) sono puramente virtuali e devono essere definiti. Il metodo di interesse in questo esempio è [**IXAudio2EngineCallback:: OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror), che imposta un flag per segnalare il ciclo del gioco principale in cui si è verificato un errore critico. I metodi rimanenti, [**IXAudio2EngineCallback:: OnProcessingPassStart**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassstart) e [**IXAudio2EngineCallback:: OnProcessingPassEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassend), sono stub in questo esempio.

    ```
    class EngineCallback : public IXAudio2EngineCallback
    {
        void OnProcessingPassEnd () {}
        void OnProcessingPassStart() {}
        void OnCriticalError (HRESULT Error) {}
    };
    ```

    

2.  Usare [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) per creare un'istanza del motore XAudio2.

    ```
    if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
        return hr;
    ```

    

3.  Usare [**IXAudio2:: RegisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) per registrare il callback del motore.

    ```
    pXAudio2->RegisterForCallbacks( &engineCallback );
    ```

    

4.  Se il callback del motore non è più necessario, chiamare [**IXAudio2:: UnregisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-unregisterforcallbacks).

    ```
    pXAudio2->UnregisterForCallbacks( &engineCallback );
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

 

 
