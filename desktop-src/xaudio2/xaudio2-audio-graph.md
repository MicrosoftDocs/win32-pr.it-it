---
description: Il set di tutte le voci, con i relativi effetti contenuti e le relative interconnessioni, viene definito grafico di elaborazione audio.
ms.assetid: 4fa45dbf-3811-c91c-7561-3b896e9e1f03
title: XAudio2 Audio Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b461b89095152f3f8073a09a230e18f5e30fd7f42ffb60b4c45a32702094f70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707021"
---
# <a name="xaudio2-audio-graph"></a>XAudio2 Audio Graph

Il set di tutte le voci, con i relativi effetti contenuti e le relative interconnessioni, viene definito grafico di elaborazione audio. Il grafico accetta un set di flussi audio dal client come input, li elabora e recapita il risultato finale a un dispositivo audio. Tutta l'elaborazione audio avviene in un thread separato con una periodicità definita dal quantistico del grafo (attualmente 10 millisecondi in Microsoft Windows e 5 millisecondi e 1/3 in Xbox 360). Ogni millisecondo quantistico, il thread si riattiva e disperde i millisecondi quantistici di dati audio attraverso l'intero grafico. Per un esempio di creazione di un grafo audio di base, vedere Procedura: Creare un'elaborazione [audio di base Graph](how-to--build-a-basic-audio-processing-graph.md).

Un semplice grafo audio:

![un semplice grafo audio](images/xaudio2-audio-graph.png)

Il client può controllare lo stato del grafo in modo dinamico mentre è in esecuzione. Le azioni di controllo possono includere l'aggiunta e la rimozione di input e output, la modifica degli effetti interni e delle interconnessioni, l'impostazione dei parametri sugli effetti, l'abilitazione e la disabilitazione di parti del grafo e così via. Per un esempio di modifica dinamica di un grafo audio, vedere [Procedura:](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md)Aggiungere o rimuovere dinamicamente voci da un grafico audio Graph .

## <a name="processing-the-graph"></a>Elaborazione del Graph

Qualsiasi chiamata al metodo che influisce su qualsiasi oggetto nel grafico viene considerata come effetto di una modifica dello stato del grafo. Graph le modifiche di stato includono quanto segue:

-   Creazione e eliminazione di voci
-   Avvio o arresto di voci
-   Modifica delle destinazioni di una voce
-   Modifica delle catene di effetti
-   Abilitazione o disabilitazione degli effetti
-   Impostazione dei parametri sugli effetti o sugli SRC, i filtri, i volumi e i mixer predefiniti

Qualsiasi set di modifiche dello stato del grafo può essere combinato ed eseguito come transazione atomica. Queste operazioni atomiche sono note come set di operazioni. Vengono illustrati nella panoramica dei set [di operazioni XAudio2.](xaudio2-operation-sets.md)

## <a name="internal-data-representation"></a>Rappresentazione interna dei dati

I dati audio all'interno del grafo XAudio2 vengono sempre archiviati ed elaborati in formato PCM a virgola mobile a 32 bit. Tuttavia, il numero di canali e la frequenza di campionamento possono variare all'interno del grafico. Il formato in cui una determinata voce elabora l'audio è determinato dal tipo di voce e dai parametri usati per creare la voce.



| Tipo di voce                                                                                                      | Parametri                                                                                     |
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**IXAudio2SourceVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)                                                              | Numero di canali e frequenza di campionamento delle voci a cui la voce di origine invia l'audio.         |
| [**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) e [ **IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice) | Argomenti *InputChannels e* *InputSampleRate* usati per creare la voce submix/mastering. |



 

## <a name="format-conversion"></a>Conversione del formato

XAudio2 gestisce tutte le conversioni di frequenza di campionamento o canale necessarie quando l'audio viaggia da una voce a un'altra, con le limitazioni seguenti:

-   Tutte le voci di destinazione per una determinata voce devono essere in esecuzione alla stessa frequenza di campionamento
-   Gli effetti in una catena di effetti possono modificare il numero di canali dell'audio, ma non la frequenza di campionamento
-   Il numero di canali di output di una catena di effetti deve corrispondere a quello delle voci a cui invia
-   Non è possibile a apportare modifiche dinamiche al grafo che potrebbero interrompere le regole precedenti

Sul lato input, le voci di origine possono leggere i dati in qualsiasi formato PCM valido o in uno dei formati compressi supportati da XAudio2. Se i dati di input vengono compressi, vengono decodificati in PCM a virgola mobile prima che venga eseguita un'ulteriore elaborazione.

Sul lato output, le voci di mastering possono produrre solo dati PCM. Questi dati soddisferanno sempre le stesse restrizioni descritte in precedenza per i dati PCM di input.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Grafici audio](audio-graphs.md)
</dt> <dt>

[Guida alla programmazione di XAudio2](programming-guide.md)
</dt> <dt>

[Procedura: Creare un grafico di elaborazione audio di base](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Procedura: Aggiungere o rimuovere dinamicamente voci da un grafico audio](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md)
</dt> <dt>

[Procedura: Usare voci di missaggio secondario](how-to--use-submix-voices.md)
</dt> <dt>

[Procedura: Creare una catena di effetti](how-to--create-an-effect-chain.md)
</dt> </dl>

 

 



