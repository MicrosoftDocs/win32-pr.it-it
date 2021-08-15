---
description: Questo argomento illustra come usare uno degli effetti inclusi in XAPOFX in una catena di effetti XAudio2.
ms.assetid: dc325584-13f7-231a-e0c7-17f38d54ae11
title: 'Procedura: Usare XAPOFX in XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 618e508d5e023c29c373193aa38da9d0e7f9f76c94a57f63e50df0c346426b6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118696152"
---
# <a name="how-to-use-xapofx-in-xaudio2"></a>Procedura: Usare XAPOFX in XAudio2

Questo argomento illustra come usare uno degli effetti inclusi in XAPOFX in una catena di effetti XAudio2.

## <a name="to-use-an-effect-from-xapofx-in-an-xaudio2-effect-chain"></a>Per usare un effetto di XAPOFX in una catena di effetti XAudio2

1.  Creare l'effetto passando il CLSID di un effetto XAPOFX alla [**funzione CreateFX.**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx)

    In questo caso, viene creato l'effetto di riverbero semplificato FXReverb.

    ```
    IUnknown * pXAPO;
    CreateFX(__uuidof(FXReverb),&pXAPO);
    ```

    

2.  Popolare una struttura [**\_ \_ DESCRIPTOR XAUDIO2 EFFECT**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) con dati.

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

3.  Popolare una struttura [**XAUDIO2 \_ EFFECT \_ CHAIN**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) con dati.

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

4.  Applicare la catena di effetti a una voce XAudio2 con la [**funzione SetEffectChain.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain)

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

    > [!Note]  
    > È anche possibile applicare una catena di effetti a una voce quando si crea la voce passando la catena come parametro a [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2::CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice)o [**IXAudio2::CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).

     

5.  Rilasciare l'effetto con IUnknown::Release. Quando si crea un XAPO, il conteggio dei riferimenti sarà 1. Quando XAPO viene passato a XAudio2 con [**SetEffectChain,**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain)XAudio2 incrementa il conteggio dei riferimenti in XAPO. Il rilascio del riferimento del client all'XAPO consente a XAudio2 di diventare proprietario dell'XAPO. Se XAudio2 ha l'unico riferimento a XAPO, questo riferimento viene eliminato quando non viene più usato da XAudio2. Se il codice client deve mantenere un riferimento all'XAPO, ad esempio per riutilizzarlo in un secondo momento, è possibile ignorare questo passaggio.

    ```
    pXAPO->Release();
    ```

    

6.  Popolare la struttura dei parametri, se presente, associata all'effetto.

    In questo caso, la [**struttura FXREVERB \_ PARAMETERS**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters) viene usata per impostare la diffusione e le dimensioni della stanza che l'effetto riverbero deve usare.

    ```
    FXREVERB_PARAMETERS XAPOParameters;
    XAPOParameters.Diffusion = FXREVERB_DEFAULT_DIFFUSION;
    XAPOParameters.RoomSize = FXREVERB_DEFAULT_ROOMSIZE;
    ```

    

7.  Passare la struttura del parametro dell'effetto all'effetto chiamando la [**funzione SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) sulla voce a cui è collegato l'effetto.

    ```
    hr = pVoice->SetEffectParameters( 0, &XAPOParameters, sizeof( FXREVERB_PARAMETERS ) );
    ```

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti audio](audio-effects.md)
</dt> <dt>

[Guida alla programmazione di XAudio2](programming-guide.md)
</dt> </dl>

 

 
