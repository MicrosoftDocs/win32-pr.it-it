---
description: Questo argomento descrive i passaggi minimi necessari per riprodurre dati audio caricati in precedenza in XAudio2.
ms.assetid: 5172b31c-d2af-45aa-5bd4-b62502f3c047
title: 'Procedura: Riprodurre un suono con XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18ee2636ae9b6513dba9a479d63e0fd14be2c198
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526881"
---
# <a name="how-to-play-a-sound-with-xaudio2"></a>Procedura: Riprodurre un suono con XAudio2

Questo argomento descrive i passaggi minimi necessari per riprodurre dati audio caricati in precedenza in XAudio2. Dopo l'inizializzazione di XAudio2 (vedere [procedura: inizializzare XAudio2](how-to--initialize-xaudio2.md)) e caricare i dati audio (vedere Procedura: [caricare file di dati audio in XAudio2](how-to--load-audio-data-files-in-xaudio2.md)), è possibile riprodurre un suono creando una voce di origine e passandovi i dati audio.

## <a name="to-play-a-sound"></a>Per riprodurre un suono

1.  Inizializzare il motore XAudio2 seguendo i passaggi descritti in [procedura: inizializzare XAudio2](how-to--initialize-xaudio2.md).
2.  Popolare una struttura del [**\_ buffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) e XAUDIO2 attenendosi alla procedura descritta in [procedura: caricare file di dati audio in XAUDIO2](how-to--load-audio-data-files-in-xaudio2.md).
    > [!Note]  
    > A seconda del formato dei dati audio, potrebbe essere necessario utilizzare una struttura di dati più grande contenente una struttura [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) al posto di un **WAVEFORMATEX**. Per ulteriori informazioni, vedere la pagina di riferimento di **WAVEFORMATEX** .

     

3.  Creare una voce di origine chiamando il metodo [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) in un'istanza del motore XAudio2. Il formato della voce è specificato dai valori impostati in una struttura [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) .
    ```
    IXAudio2SourceVoice* pSourceVoice;
    if( FAILED(hr = pXAudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx ) ) ) return hr;
    ```

    

4.  Inviare un [**\_ buffer XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) alla voce di origine usando la funzione [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer).
    ```
    if( FAILED(hr = pSourceVoice->SubmitSourceBuffer( &buffer ) ) )
        return hr;
    ```

    

    > [!Note]  
    > I dati di esempio audio a cui i punti del *buffer* sono ancora di proprietà dell'app e devono rimanere allocati e accessibili fino a quando il suono smette di essere riprodotto.

     

5.  Usare la funzione [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) per avviare la voce di origine. Dato che tutte le voci XAudio2 inviano l'output alla voce Master per impostazione predefinita, l'audio dalla voce di origine si sposta automaticamente sul dispositivo audio selezionato in fase di inizializzazione. In un grafico audio più complesso, la voce di origine deve specificare la voce a cui deve essere inviato l'output.
    ```
    if ( FAILED(hr = pSourceVoice->Start( 0 ) ) )
        return hr;
    ```

    

## <a name="notes-for-windows-store-apps"></a>Note per le app di Windows Store

Si consiglia di utilizzare un [puntatore intelligente](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) per gestire la durata degli oggetti XAUDIO2 in modo sicuro in un'eccezione. Per le app di Windows Store, è possibile usare il modello di puntatore intelligente [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) dalla libreria di modelli C++ Windows Runtime (WRL).


```
Microsoft::WRL::ComPtr<IXAudio2SourceVoice> SourceVoice;
HRESULT hr;
if( FAILED(hr = pXAudio2->CreateSourceVoice( &SourceVoice, (WAVEFORMATEX*)&wfx ) ) )
    throw Platform::Exception::CreateException(hr); 

if( FAILED(hr = SourceVoice->SubmitSourceBuffer( &buffer ) ) )
    throw Platform::Exception::CreateException(hr); 

if ( FAILED(hr = SourceVoice->Start( 0 ) ) )
    throw Platform::Exception::CreateException(hr);
```



> [!Note]  
> Prima di rilasciare l'oggetto [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) , verificare che tutti i puntatori intelligenti per gli oggetti XAUDIO2 siano stati completamente rilasciati.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Introduzione XAudio2](getting-started.md)
</dt> <dt>

[Procedura: Inizializzare XAudio2](how-to--initialize-xaudio2.md)
</dt> <dt>

[Procedura: Caricare file di dati audio in XAudio2](how-to--load-audio-data-files-in-xaudio2.md)
</dt> </dl>

 

 
