---
description: In questo argomento viene illustrato come è possibile impostare gruppi di voci per inviare l'output alla stessa voce submix. Ciò consente a una singola modifica a una voce di submix di influire su un intero gruppo di voci.
ms.assetid: 76c1c138-4846-9c4f-7875-446867436ee9
title: 'Procedura: Usare voci di missaggio secondario'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7152c3224d6528ac52651f2ca2f433631b347c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232294"
---
# <a name="how-to-use-submix-voices"></a>Procedura: Usare voci di missaggio secondario

In questo argomento viene illustrato come è possibile impostare gruppi di voci per inviare l'output alla stessa voce submix. Ciò consente a una singola modifica a una voce di submix di influire su un intero gruppo di voci.

1.  Creare una [**voce submix**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) a cui tutte le voci di effetto audio del gioco invieranno.
    ```
    IXAudio2SubmixVoice * pSFXSubmixVoice;
    pXAudio2->CreateSubmixVoice(&pSFXSubmixVoice,1,44100,0,0,0,0);
    ```

    

2.  Creare una struttura [**XAUDIO2 \_ Voice \_ Send**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) che contiene un riferimento alla voce submix.
    ```
    XAUDIO2_SEND_DESCRIPTOR SFXSend = {0, pSFXSubmixVoice};
    XAUDIO2_VOICE_SENDS SFXSendList = {1, &SFXSend};
    ```

    

3.  Passare la struttura [**XAUDIO2 \_ Voice \_ Send**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) a nuove voci di origine man mano che vengono create.
    ```
    IXAudio2SourceVoice* pSFXSourceVoice;
    if( FAILED(hr = pXaudio2->CreateSourceVoice( &pSFXSourceVoice, (WAVEFORMATEX*)&wfx,
        0, XAUDIO2_DEFAULT_FREQ_RATIO, pCallback, pSFXSendList, NULL ) ) )
        return hr;
    ```

    

4.  Applicare le modifiche a tutte le voci di effetto acustico modificando la voce submix.

    In questo esempio, la modifica del volume della voce submix con la funzione [**sevolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) modifica in modo efficace il volume di tutte le voci che lo restituiscono.

    ```
    pSFXSubmixVoice->SetVolume(0.1);
    ```

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Voci](voices.md)
</dt> <dt>

[Guida alla programmazione di XAudio2](programming-guide.md)
</dt> <dt>

[Procedura: Creare un grafico di elaborazione audio di base](how-to--build-a-basic-audio-processing-graph.md)
</dt> </dl>

 

 
