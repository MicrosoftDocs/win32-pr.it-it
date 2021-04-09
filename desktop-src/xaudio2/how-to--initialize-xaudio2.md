---
description: XAudio2 viene inizializzato per la riproduzione audio creando un'istanza del motore XAudio2 e creando una voce Master.
ms.assetid: 4db2e7fc-0a87-0344-a07c-3abf2b21af32
title: 'Procedura: Inizializzare XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4a613c1ae2b7c3a7f0c55ab5349a0a605aaeb2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879594"
---
# <a name="how-to-initialize-xaudio2"></a>Procedura: Inizializzare XAudio2

XAudio2 viene inizializzato per la riproduzione audio creando un'istanza del motore XAudio2 e creando una voce Master.

**Per inizializzare XAudio2**

1.  Assicurarsi di aver inizializzato COM. Per un'app di Windows Store, questa operazione viene eseguita come parte dell'inizializzazione del Windows Runtime. In caso contrario, usare [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).

    ```
    HRESULT hr;
    hr = CoInitializeEx( nullptr, COINIT_MULTITHREADED );
    if (FAILED(hr))
        return hr;
    ```



2.  Usare la funzione [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) per creare un'istanza del motore XAudio2.

    ```
    IXAudio2* pXAudio2 = nullptr;
    if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
        return hr;
    ```

    

3.  Usare il metodo [**CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) per creare una voce di master.

    Le voci di Master incapsulano un dispositivo audio. Si tratta della destinazione finale per tutti i file audio che passano attraverso un grafo audio.

    ```
    IXAudio2MasteringVoice* pMasterVoice = nullptr;
    if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice ) ) )
        return hr;
    ```

    

## <a name="notes-for-windows-store-apps"></a>Note per le app di Windows Store

Si consiglia di utilizzare un [puntatore intelligente](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) per gestire la durata degli oggetti XAUDIO2 in modo sicuro in un'eccezione. Per le app di Windows Store, è possibile usare il modello di puntatore intelligente [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) dalla libreria di modelli C++ Windows Runtime (WRL).


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
> Verificare che tutti gli oggetti figlio XAUDIO2 siano completamente rilasciati prima di rilasciare l'oggetto [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) .

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Introduzione XAudio2](getting-started.md)
</dt> <dt>

[Procedura: Caricare file di dati audio in XAudio2](how-to--load-audio-data-files-in-xaudio2.md)
</dt> <dt>

[Procedura: Riprodurre un suono con XAudio2](how-to--play-a-sound-with-xaudio2.md)
</dt> </dl>

 

 
