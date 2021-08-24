---
description: Questo argomento illustra come applicare una catena di effetti a una voce per consentire l'elaborazione personalizzata dei dati audio per tale voce. Questo argomento descrive come usare l'effetto riverbero, uno degli effetti XAudio2 predefiniti.
ms.assetid: 4c33bd83-2654-cd6f-ea6c-bbc0d5872638
title: 'Procedura: Creare una catena di effetti'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46abd6372fe07f71d75a4963f6617cdeda15ecf8390e3142fcf110029bd8f6dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119838413"
---
# <a name="how-to-create-an-effect-chain"></a>Procedura: Creare una catena di effetti

Questo argomento illustra come applicare una catena di effetti a una voce per consentire l'elaborazione personalizzata dei dati audio per tale voce. Questo argomento descrive come usare l'effetto riverbero, uno degli effetti XAudio2 predefiniti.

## <a name="to-create-a-basic-effect-chain-that-applies-an-effect-to-a-voice"></a>Per creare una catena di effetti di base che applica un effetto a una voce

1.  Creare l'effetto.

    In questo esempio la [**funzione XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) crea un effetto di riverbero. Vedere [Effetti audio XAudio2](xaudio2-audio-effects.md) per un elenco di possibili origini di effetti da usare con XAudio2.

    ```
    IUnknown * pXAPO;
    hr = XAudio2CreateReverb(&pXAPO);
    ```

    

2.  Popolare una struttura [**XAUDIO2 \_ EFFECT \_ DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) con dati.

    Se sono presenti più effetti nella catena, per ogni effetto sarà necessaria una [**struttura \_ \_ DESCRIPTOR XAUDIO2 EFFECT.**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor)

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

3.  Popolare una struttura [**XAUDIO2 \_ EFFECT \_ CHAIN**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) con dati. In questo caso, la catena ha un solo effetto. Se la catena ha più di un effetto, il membro EffectCount conterrà il conteggio degli effetti e il membro pEffectDescriptors farà riferimento a una matrice di strutture DESCRIPTOR XAUDIO2 \_ \_ EFFECT.

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

4.  Applicare la catena di effetti a una voce con la [**funzione SetEffectChain.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain)

    È possibile applicare catene di effetti a voci master, voci di origine e voci submix.

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

5.  Rilasciare l'effetto con IUnknown::Release.

    Quando si crea un XAPO, il conteggio dei riferimenti sarà 1. Quando XAPO viene passato a XAudio2 con [**SetEffectChain,**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain)XAudio2 incrementa il conteggio dei riferimenti in XAPO. Il rilascio del riferimento del client a XAPO consente a XAudio2 di assumere la proprietà di XAPO. Se XAudio2 ha l'unico riferimento a XAPO, verrà eliminato quando non viene più usato da XAudio2. Se il codice client deve mantenere un riferimento a XAPO, ad esempio per un successivo riutilizzo, è consigliabile ignorare questo passaggio.

    ```
    pXAPO->Release();
    ```

    

6.  Popolare la struttura dei parametri, se presente, associata all'effetto. L'effetto riverbero usa una [**struttura PARAMETERS \_ REVERB \_ XAUDIO2FX.**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters)

    ```
    XAUDIO2FX_REVERB_PARAMETERS reverbParameters;
    reverbParameters.ReflectionsDelay = XAUDIO2FX_REVERB_DEFAULT_REFLECTIONS_DELAY;
    reverbParameters.ReverbDelay = XAUDIO2FX_REVERB_DEFAULT_REVERB_DELAY;
    reverbParameters.RearDelay = XAUDIO2FX_REVERB_DEFAULT_REAR_DELAY;
    reverbParameters.PositionLeft = XAUDIO2FX_REVERB_DEFAULT_POSITION;
    reverbParameters.PositionRight = XAUDIO2FX_REVERB_DEFAULT_POSITION;
    reverbParameters.PositionMatrixLeft = XAUDIO2FX_REVERB_DEFAULT_POSITION_MATRIX;
    reverbParameters.PositionMatrixRight = XAUDIO2FX_REVERB_DEFAULT_POSITION_MATRIX;
    reverbParameters.EarlyDiffusion = XAUDIO2FX_REVERB_DEFAULT_EARLY_DIFFUSION;
    reverbParameters.LateDiffusion = XAUDIO2FX_REVERB_DEFAULT_LATE_DIFFUSION;
    reverbParameters.LowEQGain = XAUDIO2FX_REVERB_DEFAULT_LOW_EQ_GAIN;
    reverbParameters.LowEQCutoff = XAUDIO2FX_REVERB_DEFAULT_LOW_EQ_CUTOFF;
    reverbParameters.HighEQGain = XAUDIO2FX_REVERB_DEFAULT_HIGH_EQ_GAIN;
    reverbParameters.HighEQCutoff = XAUDIO2FX_REVERB_DEFAULT_HIGH_EQ_CUTOFF;
    reverbParameters.RoomFilterFreq = XAUDIO2FX_REVERB_DEFAULT_ROOM_FILTER_FREQ;
    reverbParameters.RoomFilterMain = XAUDIO2FX_REVERB_DEFAULT_ROOM_FILTER_MAIN;
    reverbParameters.RoomFilterHF = XAUDIO2FX_REVERB_DEFAULT_ROOM_FILTER_HF;
    reverbParameters.ReflectionsGain = XAUDIO2FX_REVERB_DEFAULT_REFLECTIONS_GAIN;
    reverbParameters.ReverbGain = XAUDIO2FX_REVERB_DEFAULT_REVERB_GAIN;
    reverbParameters.DecayTime = XAUDIO2FX_REVERB_DEFAULT_DECAY_TIME;
    reverbParameters.Density = XAUDIO2FX_REVERB_DEFAULT_DENSITY;
    reverbParameters.RoomSize = XAUDIO2FX_REVERB_DEFAULT_ROOM_SIZE;
    reverbParameters.WetDryMix = XAUDIO2FX_REVERB_DEFAULT_WET_DRY_MIX;
    ```

    

7.  Passare la struttura dei parametri dell'effetto all'effetto chiamando la [**funzione SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) sulla voce a cui è collegato l'effetto.

    ```
    hr = pVoice->SetEffectParameters( 0, &reverbParameters, sizeof( reverbParameters ) );
    ```

    

8.  Disabilitare o abilitare l'effetto, se appropriato.

    È possibile usare [**DisableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) in qualsiasi momento per disattivare un effetto.

    ```
    pVoice->DisableEffect(0);
    ```

    

    È possibile riattivare un effetto con [**EnableEffect.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect)

    ```
    pVoice->EnableEffect(0);
    ```

    

    I parametri [**per DisableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) e [**EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect) specificano l'effetto nella catena da abilitare o disabilitare.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti audio](audio-effects.md)
</dt> <dt>

[Guida alla programmazione di XAudio2](programming-guide.md)
</dt> <dt>

[Procedura: Creare un grafico di elaborazione audio di base](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Panoramica di XAPO](xapo-overview.md)
</dt> <dt>

[Procedura: Usare XAOPFX in XAudio2](how-to--use-xapofx-in-xaudio2.md)
</dt> <dt>

[Procedura: Usare un'applicazione XAOP in XAudio2](how-to--use-an-xapo-in-xaudio2.md)
</dt> </dl>

 

 
