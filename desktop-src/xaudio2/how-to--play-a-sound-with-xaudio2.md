---
description: Questo argomento descrive i passaggi minimi necessari per riprodurre dati audio caricati in precedenza in XAudio2.
ms.assetid: 5172b31c-d2af-45aa-5bd4-b62502f3c047
title: 'Procedura: Riprodurre un suono con XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cfa5cb2a7a47b7fb54e6a7e9f098a545b0c630c6c27889d7aa6eff1242121d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082911"
---
# <a name="how-to-play-a-sound-with-xaudio2"></a>Procedura: Riprodurre un suono con XAudio2

Questo argomento descrive i passaggi minimi necessari per riprodurre dati audio caricati in precedenza in XAudio2. Dopo aver inizializzato XAudio2 (vedere Procedura: Inizializzare [XAudio2)](how-to--initialize-xaudio2.md)e aver caricato i dati audio (vedere Procedura: Procedura: Caricare file di dati [audio in XAudio2),](how-to--load-audio-data-files-in-xaudio2.md)è possibile riprodurre un suono creando una voce di origine e passando i dati audio.

## <a name="to-play-a-sound"></a>Per riprodurre un suono

1.  Inizializzare il motore XAudio2 seguendo la procedura descritta in [Procedura: Inizializzare XAudio2](how-to--initialize-xaudio2.md).
2.  Popolare una [**struttura WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) e [**XAUDIO2 \_ BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) seguendo la procedura descritta in Procedura: Caricare file di dati [audio in XAudio2.](how-to--load-audio-data-files-in-xaudio2.md)
    > [!Note]  
    > A seconda del formato dei dati audio, potrebbe essere necessario usare una struttura di dati più grande contenente una struttura [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) al posto di **WAVEFORMATEX**. Per altre informazioni, vedere la pagina di riferimento **waveFORMATEX.**

     

3.  Creare una voce di origine chiamando il [**metodo IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) in un'istanza del motore XAudio2. Il formato della voce viene specificato dai valori impostati in una [**struttura WAVEFORMATEX.**](/windows/win32/api/mmreg/ns-mmreg-waveformatex)
    ```
    IXAudio2SourceVoice* pSourceVoice;
    if( FAILED(hr = pXAudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx ) ) ) return hr;
    ```

    

4.  Inviare [**un BUFFER XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) alla voce di origine usando la funzione [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer).
    ```
    if( FAILED(hr = pSourceVoice->SubmitSourceBuffer( &buffer ) ) )
        return hr;
    ```

    

    > [!Note]  
    > I dati di esempio audio a cui *i punti del buffer* sono ancora di proprietà dell'app e devono rimanere allocati e accessibili fino a quando il suono non smette di essere riprodotto.

     

5.  Usare la [**funzione Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) per avviare la voce di origine. Poiché tutte le voci XAudio2 inviano l'output alla voce mastering per impostazione predefinita, l'audio dalla voce di origine si fa automaticamente strada al dispositivo audio selezionato durante l'inizializzazione. In un grafico audio più complesso, la voce di origine deve specificare la voce a cui inviare l'output.
    ```
    if ( FAILED(hr = pSourceVoice->Start( 0 ) ) )
        return hr;
    ```

    

## <a name="notes-for-windows-store-apps"></a>Note per le app Windows Store

È consigliabile usare un puntatore [intelligente](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) per gestire la durata degli oggetti XAUDIO2 in modo sicuro per le eccezioni. Per Windows app di Store, è possibile usare il modello di puntatore intelligente [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) dalla libreria di modelli C++ di Windows Runtime (WRL).


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
> Assicurarsi che tutti i puntatori intelligenti agli oggetti XAUDIO2 siano completamente rilasciati prima di rilasciare [**l'oggetto IXAudio2.**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2)

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[XAudio2 Attività iniziali](getting-started.md)
</dt> <dt>

[Procedura: Inizializzare XAudio2](how-to--initialize-xaudio2.md)
</dt> <dt>

[Procedura: Caricare file di dati audio in XAudio2](how-to--load-audio-data-files-in-xaudio2.md)
</dt> </dl>

 

 
