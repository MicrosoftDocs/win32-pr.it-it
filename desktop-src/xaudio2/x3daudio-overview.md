---
description: X3DAudio è un'API usata con XAudio2 per posizionare il suono nello spazio 3D per creare l'illusione di suoni provenienti da un punto nello spazio relativo alla posizione della fotocamera.
ms.assetid: 1638e848-4186-5dea-18e8-5369eee544ae
title: Panoramica di X3DAudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff509b16556ee1932d2a2543ad5008ddcbaa5b92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319076"
---
# <a name="x3daudio-overview"></a>Panoramica di X3DAudio

X3DAudio è un'API usata con [XAudio2](programming-guide.md) per posizionare il suono nello spazio 3D per creare l'illusione di suoni provenienti da un punto nello spazio relativo alla posizione della fotocamera. In particolare, i titoli con le scene 3D per la funzionalità vorranno usare X3DAudio. I suoni che non richiedono il posizionamento 3D, ad esempio colonne o suoni di ambiente non posizionati, possono ignorare completamente X3DAudio.

## <a name="listeners-and-emitters"></a>Listener e generatori

Per gestire i suoni nello spazio 3D, X3DAudio usa i concetti dei *listener* e degli *emettitori*. I listener e gli emettitori rappresentano la posizione di tutti i suoni 3D e il punto da cui hanno origine i suoni.

-   Un listener viene definito come punto nello spazio e un orientamento. Si tratta della posizione in cui viene *udito* il suono. La posizione e l'orientamento del listener in genere corrispondono alla posizione e all'orientamento della fotocamera. Si tratta di un valore che indica se un titolo utilizza una visualizzazione prospettica della prima persona o della terza persona. La posizione del listener è espressa in coordinate internazionali. È importante notare che si tratta della posizione del listener *relativa* a un emittente che determina come calcolare i volumi finali del relatore.
-   Un emettitore viene definito come uno o più punti nello spazio da cui ha *origine* un suono. La posizione del emettitore può trovarsi in qualsiasi punto dello spazio 3D. Analogamente a un listener, la posizione di un emittente è espressa in coordinate internazionali. Si tratta della posizione dell'emettitore *rispetto* al listener che determina come vengono calcolati i volumi finali del relatore.
-   X3DAudio utilizza le coordinate di sinistra. Per usare con le coordinate di destra, gli sviluppatori devono negare l'elemento. z dei membri OrientTop, OrientFront, position e Velocity del listener X3DAUDIO e dell' \_ \_ emettitore X3DAUDIO.

Oltre alla posizione, i listener e gli emettitori possono includere la velocità. A differenza di un motore di rendering 3D, X3DAudio usa solo la velocità per calcolare gli effetti Doppler (non viene usato per calcolare la posizione).

Per altri dettagli sui listener e gli emettitori, vedere gli argomenti di riferimento sulla struttura di [**\_ listener X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) e [**X3DAUDIO \_ emittor**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) .

## <a name="using-x3daudio-with-xaudio2"></a>Uso di X3DAudio con XAudio2

Per tutte le interazioni tra X3DAudio e XAudio2, usare le funzioni X3DAudio seguenti.

-   [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize)

    Chiamare la funzione [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) per inizializzare X3DAudio. In genere, è sufficiente chiamare **X3DAudioInitialize** una volta per la durata di un gioco, a meno che la configurazione dell'altoparlante non venga modificata.

-   [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate)

    Dopo l'inizializzazione di X3DAudio, è possibile determinare il volume e gli altri valori per un determinato suono passando l'emettitore del suono e il listener alla funzione [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) . I valori calcolati da **X3DAudioCalculate** possono quindi essere applicati a voci o effetti XAudio2 appropriati per i flag passati alla funzione. È possibile applicare i valori volume e pitch calcolati da X3DAudio a una voce con i metodi [**IXAudio2Voice:: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) e [**IXAudio2SourceVoice:: SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) . Gli altri valori calcolati da X3DAudio dovranno essere applicati a un [**effetto di riverbero**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) usando il metodo [**IXAudio2Voice:: SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) .

Per un esempio dettagliato dell'uso di X3DAudio con XAudio2, vedere [procedura: Integrare X3DAudio con xaudio](how-to--integrate-x3daudio-with-xaudio2.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[X3DAudio](x3daudio.md)
</dt> </dl>

 

 
