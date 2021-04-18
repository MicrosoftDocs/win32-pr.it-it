---
description: Questo argomento illustra come usare un effetto creato con l'API XAPO in una catena di effetti XAudio2.
ms.assetid: d4d24177-25eb-13ca-0e38-0c876a273e0d
title: 'Procedura: Usare un oggetto di elaborazione audio XAPO in XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 780e0ba59b5032ddc01b2709f1f3e9c5a0fcce1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307944"
---
# <a name="how-to-use-an-xapo-in-xaudio2"></a>Procedura: Usare un oggetto di elaborazione audio XAPO in XAudio2

Questo argomento illustra come usare un effetto creato con l'API XAPO in una catena di effetti XAudio2.

1.  Creare il XAPO come descritto in [procedura: creare un XAPO](how-to--create-an-xapo.md).

    È anche possibile implementare la funzionalità del parametro in fase di esecuzione, come descritto in [procedura: aggiungere il supporto per i parametri della fase di esecuzione a un XAPO](how-to--add-run-time-parameter-support-to-an-xapo.md).

2.  Creare un'istanza di XAPO.

    ```
    IUnknown * pXAPO;
    pXAPO = new SimpleXAPO();
    ```

    

3.  Popola una struttura del [**\_ \_ descrittore dell'effetto XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) con i dati.

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

4.  Popola una struttura della [**\_ \_ catena di effetti XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) con i dati.

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

5.  Applicare la catena di effetti a una voce XAudio2 con la funzione [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) .

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

    > [!Note]  
    > Una catena di effetti può anche essere applicata a una voce quando la voce viene creata passando la catena come parametro a [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2:: CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice)o [**IXAudio2:: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).

     

6.  Rilasciare l'effetto con IUnknown:: Release.

    Quando si crea un XAPO, il conteggio dei riferimenti sarà 1. Quando XAPO viene passato a XAudio2 con [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 incrementa il conteggio dei riferimenti in XAPO. Il rilascio del riferimento del client a XAPO consente a XAudio2 di assumere la proprietà del XAPO. Se XAudio2 ha l'unico riferimento a XAPO, verrà eliminato quando non verrà più usato da XAudio2.. Se il codice client deve mantenere un riferimento a XAPO per un riutilizzo successivo, ad esempio, è consigliabile ignorare questo passaggio.

    ```
    pXAPO->Release();
    ```

    

7.  Popola la struttura di parametri, se presente, associata all'effetto. In questo caso, la percentuale di attendibilità totale in cui deve essere applicato l'effetto.

    ```
    XAPO_PARAMETERS XAPOParameters;
    XAPOParameters.Level = 0.75;
    ```

    

8.  Passare la struttura del parametro Effect all'effetto chiamando la funzione [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) sulla voce a cui è collegato l'effetto.

    ```
    hr = pVoice->SetEffectParameters( 0, &XAPOParameters, sizeof( XAPO_PARAMETERS ) );
    ```

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti audio](audio-effects.md)
</dt> <dt>

[Panoramica di XAPO](xapo-overview.md)
</dt> <dt>

[Guida alla programmazione di XAudio2](programming-guide.md)
</dt> </dl>

 

 
