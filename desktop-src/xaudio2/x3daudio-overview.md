---
description: X3DAudio è un'API usata con XAudio2 per posizionare il suono nello spazio 3D per creare l'illusione del suono proveniente da un punto nello spazio rispetto alla posizione della fotocamera.
ms.assetid: 1638e848-4186-5dea-18e8-5369eee544ae
title: Panoramica di X3DAudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eb39239027bf8c7387fbe4cb25b80cef88bb241b74facf0b7bd7ee35c77965b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962550"
---
# <a name="x3daudio-overview"></a>Panoramica di X3DAudio

X3DAudio è un'API usata con [XAudio2](programming-guide.md) per posizionare il suono nello spazio 3D per creare l'illusione del suono proveniente da un punto nello spazio rispetto alla posizione della fotocamera. In particolare, i titoli che presentano scene 3D vogliono usare X3DAudio. I suoni che non richiedono il posizionamento 3D, ad esempio colonne sonore o suoni di ambiente non posizionati, possono ignorare completamente X3DAudio.

## <a name="listeners-and-emitters"></a>Listener ed emettitori

Per gestire i suoni nello spazio 3D, X3DAudio usa i concetti di *listener* ed *emettitori*. I listener e gli emettitori rappresentano la posizione di qualsiasi suono 3D udibile e il punto da cui provengono tali suoni.

-   Un listener è definito come un punto nello spazio e un orientamento. È la posizione in cui viene ascoltato il *suono.* La posizione e l'orientamento del listener in genere sono uguali alla posizione e all'orientamento della fotocamera. Questo vale se un titolo usa una visualizzazione prospettica in prima persona o in terza persona. La posizione del listener è espressa in coordinate globali. È importante notare che è la posizione  del listener rispetto a un emettitore che determina come calcolare i volumi degli altoparlanti finali.
-   Un emettitore è definito come uno o più punti nello spazio da cui ha *origine un suono.* La posizione dell'emettitore può essere ovunque nello spazio 3D. Come un listener, la posizione di un emettitore è espressa in coordinate globali. È la posizione dell'emettitore *rispetto* al listener che determina il modo in cui vengono calcolati i volumi degli altoparlanti finali.
-   X3DAudio usa le coordinate mancino. Per usare con le coordinate con la mano destra, gli sviluppatori devono negare l'elemento .z dei membri OrientTop, OrientFront, Position e Velocity dei membri X3DAUDIO LISTENER e \_ X3DAUDIO \_ EMITTER.

Oltre alla posizione, i listener e gli emettitori possono includere velocità. A differenza di un motore di rendering 3D, X3DAudio usa solo la velocità per calcolare gli effetti Doppler (non viene usato per calcolare la posizione).

Per altre informazioni sui listener e sugli emettitori, vedere gli argomenti di riferimento sulla struttura [**X3DAUDIO \_ LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) e [**X3DAUDIO \_ EMITTER.**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter)

## <a name="using-x3daudio-with-xaudio2"></a>Uso di X3DAudio con XAudio2

Per tutte le interazioni tra X3DAudio e XAudio2, usare le funzioni X3DAudio seguenti.

-   [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize)

    Chiamare la [**funzione X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) per inizializzare X3DAudio. In genere, è necessario chiamare **X3DAudioInitialize** una sola volta nella durata di un gioco, a meno che la configurazione del parlante non venga modificata.

-   [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate)

    Dopo aver inizializzato X3DAudio, è possibile determinare il volume e altri valori per un determinato suono passando l'emettitore del suono e il listener alla [**funzione X3DAudioCalculate.**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) I valori calcolati da **X3DAudioCalculate** possono quindi essere applicati alle voci o agli effetti di XAudio2 in base alle esigenze dei flag passati alla funzione. È possibile applicare i valori di volume e passo calcolati da X3DAudio a una voce con i metodi [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) e [**IXAudio2SourceVoice::SetFrequencyRatio.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) Altri valori calcolati da X3DAudio dovranno essere applicati a un effetto [**di riverbero**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) usando il metodo [**IXAudio2Voice::SetEffectParameters.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters)

Per un esempio dettagliato dell'uso di X3DAudio con XAudio2, vedere Procedura: Integrare [X3DAudio con XAudio](how-to--integrate-x3daudio-with-xaudio2.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[X3DAudio](x3daudio.md)
</dt> </dl>

 

 
