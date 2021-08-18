---
description: XAudio2 viene inizializzato per la riproduzione audio creando un'istanza del motore XAudio2 e creando una voce di mastering.
ms.assetid: 4db2e7fc-0a87-0344-a07c-3abf2b21af32
title: 'Procedura: Inizializzare XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eb55425c92e6d28a2689fb388869bbf42339d14bec3550e3f9e17798c1af68f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962730"
---
# <a name="how-to-initialize-xaudio2"></a>Procedura: Inizializzare XAudio2

XAudio2 viene inizializzato per la riproduzione audio creando un'istanza del motore XAudio2 e creando una voce di mastering.

**Per inizializzare XAudio2**

1.  Assicurarsi di aver inizializzato COM. Per un'app Windows Store, questa operazione viene eseguita nell'ambito dell'inizializzazione del Windows Runtime. In caso contrario, [**usare CoInitializeEx.**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)

    ```
    HRESULT hr;
    hr = CoInitializeEx( nullptr, COINIT_MULTITHREADED );
    if (FAILED(hr))
        return hr;
    ```



2.  Usare la [**funzione XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) per creare un'istanza del motore XAudio2.

    ```
    IXAudio2* pXAudio2 = nullptr;
    if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
        return hr;
    ```

    

3.  Usare il [**metodo CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) per creare una voce di mastering.

    Le voci di mastering incapsulano un dispositivo audio. È la destinazione finale per tutto l'audio che passa attraverso un grafico audio.

    ```
    IXAudio2MasteringVoice* pMasterVoice = nullptr;
    if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice ) ) )
        return hr;
    ```

    

## <a name="notes-for-windows-store-apps"></a>Note per le Windows Store

È consigliabile usare un puntatore intelligente [per](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) gestire la durata degli oggetti XAUDIO2 in modo sicuro per le eccezioni. Per Windows store, è possibile usare il modello di puntatore intelligente [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) della libreria di modelli C++ di Windows Runtime.


```C++
Microsoft::WRL::ComPtr<IXAudio2> XAudio2;
HRESULT hr;
if ( FAILED(hr = XAudio2Create( &XAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
    throw Platform::Exception::CreateException(hr);

IXAudio2MasteringVoice* pMasterVoice = nullptr;
if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice ) ) )
    return hr;
```



> [!Note]  
> Assicurarsi che tutti gli oggetti figlio XAUDIO2 siano rilasciati completamente prima di rilasciare [**l'oggetto IXAudio2.**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2)

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[XAudio2 Attività iniziali](getting-started.md)
</dt> <dt>

[Procedura: Caricare file di dati audio in XAudio2](how-to--load-audio-data-files-in-xaudio2.md)
</dt> <dt>

[Procedura: Riprodurre un suono con XAudio2](how-to--play-a-sound-with-xaudio2.md)
</dt> </dl>

 

 
