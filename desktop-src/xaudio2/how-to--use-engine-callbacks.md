---
description: È possibile notificare al codice client XAudio2 gli eventi del motore registrando un'istanza di una classe che implementa l'interfaccia IXAudio2EngineCallback con il motore XAudio2.
ms.assetid: 006a8cb6-c24c-f7d1-9e8b-9cb2baa046c0
title: 'Procedura: Usare callback del motore'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffc51e673be6972c1c5ba012c12f616e1bfe78a345081fee683aba83b6944c17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054371"
---
# <a name="how-to-use-engine-callbacks"></a>Procedura: Usare callback del motore

È possibile notificare al codice client XAudio2 gli eventi del motore registrando un'istanza di una classe che implementa [**l'interfaccia IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) con il motore XAudio2. Ciò consente al codice client XAudio2 di tenere traccia del momento in cui si verifica l'elaborazione audio e del momento in cui riavviare il motore in caso di errore critico.

## <a name="to-use-an-engine-callback"></a>Per usare un callback del motore

La procedura seguente registra un oggetto per gestire gli eventi del motore.

1.  Creare una classe che eredita [**dall'interfaccia IXAudio2EngineCallback.**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback)

    Tutti i metodi [**di IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) sono puramente virtuali e devono essere definiti. Il metodo di interesse in questo esempio è [**IXAudio2EngineCallback::OnCriticalError,**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror)che imposta un flag per segnalare al ciclo principale del gioco che si è verificato un errore critico. I metodi rimanenti, [**IXAudio2EngineCallback::OnProcessingPassStart**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassstart) e [**IXAudio2EngineCallback::OnProcessingPassEnd,**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassend)sono stub in questo esempio.

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

    

3.  Usare [**IXAudio2::RegisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) per registrare il callback del motore.

    ```
    pXAudio2->RegisterForCallbacks( &engineCallback );
    ```

    

4.  Se il callback del motore non è più necessario, chiamare [**IXAudio2::UnregisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-unregisterforcallbacks).

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

 

 
