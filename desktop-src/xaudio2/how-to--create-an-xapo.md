---
description: L'API XAPO fornisce l'interfaccia IXAPO e la classe CXAPOBase per la compilazione di nuovi tipi XAPO.
ms.assetid: 34f5c3d5-ee40-e304-7c97-d30c17621d26
title: 'Procedura: Creare un oggetto di elaborazione audio di XAudio2 (XAPO)'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ea17729c5a6d872d98443c85f79dc72e8eee6dd2233b99f31e189a9eb28708e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583851"
---
# <a name="how-to-create-an-xapo"></a>Procedura: Creare un oggetto di elaborazione audio di XAudio2 (XAPO)

L'API XAPO fornisce [**l'interfaccia IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) e la [**classe CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) per la compilazione di nuovi tipi XAPO. **L'interfaccia IXAPO** contiene tutti i metodi che devono essere implementati per creare un nuovo XAPO. La **classe CXAPOBase** fornisce un'implementazione di base **dell'interfaccia IXAPO.** **CXAPOBase** implementa tutti i metodi di interfaccia **IXAPO,** ad eccezione del metodo [**IXAPO::P rocess,**](/windows/win32/api/xapo/nf-xapo-ixapo-process) univoco per ogni XAPO.

## <a name="to-create-a-new-static-xapo"></a>Per creare un nuovo XAPO statico

1.  Derivare una nuova classe XAPO dalla classe di base [**CXAPOBase.**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase)

    > [!Note]  
    > Gli XAPO implementano **l'interfaccia IUnknown.** Le [**interfacce IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) e [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) includono i tre metodi **IUnknown:** **QueryInterface,** **AddRef** e **Release.** [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) fornisce implementazioni di tutti e tre i **metodi IUnknown.** Una nuova istanza di **CXAPOBase** avrà un conteggio dei riferimenti di 1. Verrà eliminato quando il conteggio dei riferimenti diventa 0. Per consentire a XAudio2 di eliminare un'istanza di XAPO quando non è più necessaria, chiamare **IUnknown::Release** in XAPO dopo l'aggiunta a una catena di effetti XAudio2. Per altre informazioni sull'uso di [XAPO con XAudio2, vedere Procedura: Usare XAPO in XAudio2.](how-to--use-an-xapo-in-xaudio2.md)

     

2.  Eseguire [**l'override dell'implementazione della classe CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) del metodo [**IXAPO::LockForProcess.**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess)

    L'override di [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) consente di archiviare informazioni sul formato dei dati audio per l'uso in [**IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process).

3.  Implementare [**il metodo IXAPO::P rocess.**](/windows/win32/api/xapo/nf-xapo-ixapo-process)

    XAudio2 chiama il [**metodo IXAPO::P rocess ogni**](/windows/win32/api/xapo/nf-xapo-ixapo-process) volta che un XAPO deve elaborare i dati audio. **Process** contiene la maggior parte del codice per un XAPO.

## <a name="implementing-the-process-method"></a>Implementazione del metodo Process

Il [**metodo IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) accetta buffer di flusso per i dati audio di input e output. Un tipico XAPO prevede un buffer del flusso di input e un buffer del flusso di output. È necessario basare l'elaborazione dei dati dal buffer del flusso di input sul formato specificato nella funzione [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) ed eventuali flag passati alla funzione **Process** con il buffer del flusso di input. Copiare i dati del buffer del flusso di input elaborati nel buffer del flusso di output. Impostare il parametro BufferFlags del buffer del flusso di output come [**XAPO \_ BUFFER \_ VALID**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags) o **XAPO \_ BUFFER \_ SILENT**.

L'esempio seguente illustra [**un'implementazione LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) [**e Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) che copia semplicemente i dati da un buffer di input a un buffer di output. Tuttavia, non viene elaborata se il buffer di input è contrassegnato con [**XAPO \_ BUFFER \_ SILENT**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags).


```
STDMETHOD(LockForProcess) (UINT32 InputLockedParameterCount,
          const XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS* pInputLockedParameters,
          UINT32 OutputLockedParameterCount,
          const XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS* pOutputLockedParameters)
{
    assert(!IsLocked());
    assert(InputLockedParameterCount == 1);
    assert(OutputLockedParameterCount == 1);
    assert(pInputLockedParameters != NULL);
    assert(pOutputLockedParameters != NULL);
    assert(pInputLockedParameters[0].pFormat != NULL);
    assert(pOutputLockedParameters[0].pFormat != NULL);


    m_uChannels = pInputLockedParameters[0].pFormat->nChannels;
    m_uBytesPerSample = (pInputLockedParameters[0].pFormat->wBitsPerSample >> 3);

    return CXAPOBase::LockForProcess(
        InputLockedParameterCount,
        pInputLockedParameters,
        OutputLockedParameterCount,
        pOutputLockedParameters);
}
STDMETHOD_(void, Process)(UINT32 InputProcessParameterCount,
           const XAPO_PROCESS_BUFFER_PARAMETERS* pInputProcessParameters,
           UINT32 OutputProcessParameterCount,
           XAPO_PROCESS_BUFFER_PARAMETERS* pOutputProcessParameters,
           BOOL IsEnabled)
{
    assert(IsLocked());
    assert(InputProcessParameterCount == 1);
    assert(OutputProcessParameterCount == 1);
    assert(NULL != pInputProcessParameters);
    assert(NULL != pOutputProcessParameters);


    XAPO_BUFFER_FLAGS inFlags = pInputProcessParameters[0].BufferFlags;
    XAPO_BUFFER_FLAGS outFlags = pOutputProcessParameters[0].BufferFlags;

    // assert buffer flags are legitimate
    assert(inFlags == XAPO_BUFFER_VALID || inFlags == XAPO_BUFFER_SILENT);
    assert(outFlags == XAPO_BUFFER_VALID || outFlags == XAPO_BUFFER_SILENT);

    // check input APO_BUFFER_FLAGS
    switch (inFlags)
    {
    case XAPO_BUFFER_VALID:
        {
            void* pvSrc = pInputProcessParameters[0].pBuffer;
            assert(pvSrc != NULL);

            void* pvDst = pOutputProcessParameters[0].pBuffer;
            assert(pvDst != NULL);

            memcpy(pvDst,pvSrc,pInputProcessParameters[0].ValidFrameCount * m_uChannels * m_uBytesPerSample);
            break;
        }

    case XAPO_BUFFER_SILENT:
        {
            // All that needs to be done for this case is setting the
            // output buffer flag to XAPO_BUFFER_SILENT which is done below.
            break;
        }

    }

    // set destination valid frame count, and buffer flags
    pOutputProcessParameters[0].ValidFrameCount = pInputProcessParameters[0].ValidFrameCount; // set destination frame count same as source
    pOutputProcessParameters[0].BufferFlags     = pInputProcessParameters[0].BufferFlags;     // set destination buffer flags same as source

}
```



Quando si scrive [**un metodo Process,**](/windows/win32/api/xapo/nf-xapo-ixapo-process) è importante notare che i dati audio XAudio2 sono interleaved. Ciò significa che i dati di ogni canale sono adiacenti per un numero di campione specifico. Ad esempio, se è presente un'onda a 4 canali che riproduce una voce di origine XAudio2, i dati audio sono un campione di canale 0, un campione di canale 1, un campione di canale 2, un campione di canale 3 e quindi il campione successivo di canali 0, 1, 2, 3 e così via.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti audio](audio-effects.md)
</dt> <dt>

[Panoramica di XAPO](xapo-overview.md)
</dt> </dl>

 

 
