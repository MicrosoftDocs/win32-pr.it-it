---
description: Il set di tutte le voci, con gli effetti contenuti e le relative interconnessioni, viene definito grafico di elaborazione audio.
ms.assetid: 4fa45dbf-3811-c91c-7561-3b896e9e1f03
title: Grafico audio XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eb265bd6bc2547acd04ca41cceb58ad12896fbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234060"
---
# <a name="xaudio2-audio-graph"></a>Grafico audio XAudio2

Il set di tutte le voci, con gli effetti contenuti e le relative interconnessioni, viene definito grafico di elaborazione audio. Il grafico accetta un set di flussi audio dal client come input, li elabora e recapita il risultato finale a un dispositivo audio. Tutte le elaborazioni audio avvengono in un thread separato con una periodicità definita dal quantum del grafo (attualmente 10 millisecondi in Microsoft Windows e 5 1/3 millisecondi su Xbox 360). Ogni quantum di millisecondi, il thread viene riattivato e disperde i millisecondi quantici dei dati audio attraverso l'intero grafico. Per un esempio di creazione di un grafico audio di base, vedere How to: [Build a Basic audio processing Graph](how-to--build-a-basic-audio-processing-graph.md).

Un semplice grafico audio:

![un semplice grafico audio](images/xaudio2-audio-graph.png)

Il client può controllare dinamicamente lo stato del grafo mentre è in esecuzione. Le azioni di controllo possono includere l'aggiunta e la rimozione di input e output, la modifica degli effetti interni e delle interconnessioni, l'impostazione dei parametri sugli effetti, l'abilitazione e la disabilitazione di parti del grafico e così via. Per un esempio di modifica dinamica di un grafico audio, vedere [procedura: aggiungere o rimuovere voci da un grafico audio](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md)in modo dinamico.

## <a name="processing-the-graph"></a>Elaborazione del grafo

Qualsiasi chiamata al metodo che influisce su un oggetto nel grafico viene considerata una modifica dello stato del grafico. Le modifiche dello stato del grafo includono quanto segue:

-   Creazione ed eliminazione di voci
-   Avvio o arresto di voci
-   Modifica delle destinazioni di una voce
-   Modifica delle catene degli effetti
-   Abilitazione o disabilitazione degli effetti
-   Impostazione di parametri per gli effetti o per SRCs, filtri, volumi e mixer predefiniti

Qualsiasi set di modifiche dello stato del grafico può essere combinato ed eseguito come transazione atomica. Queste operazioni atomiche sono note come set di operazioni. Sono illustrati nella panoramica dei [set di operazioni XAudio2](xaudio2-operation-sets.md) .

## <a name="internal-data-representation"></a>Rappresentazione dati interna

I dati audio all'interno del grafo XAudio2 vengono sempre archiviati ed elaborati in formato PCM a virgola mobile a 32 bit. Tuttavia, il numero di canali e la frequenza di campionamento possono variare all'interno del grafico. Il formato in cui una determinata voce elabora audio è determinato dal tipo di voce e dai parametri usati per creare la voce.



| Tipo voce                                                                                                      | Parametri                                                                                     |
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**IXAudio2SourceVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)                                                              | Il numero di canali e la frequenza di campionamento delle voci a cui la voce di origine invia audio.         |
| [**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) e [ **IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice) | Argomenti *InputChannels* e *InputSampleRate* usati per creare la voce di submix/master. |



 

## <a name="format-conversion"></a>Conversione del formato

XAudio2 gestisce la frequenza di campionamento o le conversioni di canale richieste quando l'audio passa da una voce all'altra, con le limitazioni seguenti:

-   Tutte le voci di destinazione per una voce specifica devono essere in esecuzione alla stessa frequenza di campionamento
-   Gli effetti di una catena di effetti possono modificare il numero di canali audio, ma non la frequenza di campionamento
-   Il numero di canali di output di una catena di effetti deve corrispondere a quello delle voci a cui viene inviato
-   Non è possibile apportare modifiche a grafici dinamici che interrompono le regole precedenti

Sul lato input, le voci di origine possono leggere i dati in qualsiasi formato PCM valido o in uno dei formati compressi supportati da XAudio2. Se i dati di input vengono compressi, vengono decodificati in PCM a virgola mobile prima di eseguire altre operazioni di elaborazione.

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

 

 



