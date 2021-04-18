---
description: Questo argomento illustra come usare uno degli effetti inclusi in XAPOFX in una catena di effetti XAudio2.
ms.assetid: dc325584-13f7-231a-e0c7-17f38d54ae11
title: 'Procedura: Usare XAPOFX in XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b0bb4cbeabb38f408d9102a2534634e8eed7cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307942"
---
# <a name="how-to-use-xapofx-in-xaudio2"></a>Procedura: Usare XAPOFX in XAudio2

Questo argomento illustra come usare uno degli effetti inclusi in XAPOFX in una catena di effetti XAudio2.

## <a name="to-use-an-effect-from-xapofx-in-an-xaudio2-effect-chain"></a>Per usare un effetto di XAPOFX in una catena di effetti XAudio2

1.  Creare l'effetto passando il CLSID di un effetto XAPOFX alla funzione [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) .

    In questo caso, viene creato l'effetto di riverbero semplificato FXReverb.

    ```
    IUnknown * pXAPO;
    CreateFX(__uuidof(FXReverb),&pXAPO);
    ```

    

2.  Popola una struttura del [**\_ \_ descrittore dell'effetto XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) con i dati.

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

3.  Popola una struttura della [**\_ \_ catena di effetti XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) con i dati.

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

4.  Applicare la catena di effetti a una voce XAudio2 con la funzione [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) .

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

    > [!Note]  
    > È anche possibile applicare una catena di effetti a una voce quando si crea la voce passando la catena come parametro a [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2:: CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice)o [**IXAudio2:: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).

     

5.  Rilasciare l'effetto con IUnknown:: Release. Quando si crea un XAPO, il conteggio dei riferimenti sarà 1. Quando XAPO viene passato a XAudio2 con [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 incrementa il conteggio dei riferimenti in XAPO. Il rilascio del riferimento del client a XAPO consente a XAudio2 di assumere la proprietà del XAPO. Se XAudio2 ha l'unico riferimento a XAPO, questo riferimento viene eliminato quando non è più usato da XAudio2. Se il codice client deve mantenere un riferimento a XAPO, ad esempio per riutilizzarlo in un secondo momento, è possibile ignorare questo passaggio.

    ```
    pXAPO->Release();
    ```

    

6.  Popola la struttura di parametri, se presente, associata all'effetto.

    In questo caso, la struttura dei [**\_ parametri FXREVERB**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters) viene utilizzata per impostare le dimensioni della diffusione e della stanza che devono essere utilizzate dall'effetto di riverbero.

    ```
    FXREVERB_PARAMETERS XAPOParameters;
    XAPOParameters.Diffusion = FXREVERB_DEFAULT_DIFFUSION;
    XAPOParameters.RoomSize = FXREVERB_DEFAULT_ROOMSIZE;
    ```

    

7.  Passare la struttura del parametro Effect all'effetto chiamando la funzione [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) sulla voce a cui è collegato l'effetto.

    ```
    hr = pVoice->SetEffectParameters( 0, &XAPOParameters, sizeof( FXREVERB_PARAMETERS ) );
    ```

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti audio](audio-effects.md)
</dt> <dt>

[Guida alla programmazione di XAudio2](programming-guide.md)
</dt> </dl>

 

 
