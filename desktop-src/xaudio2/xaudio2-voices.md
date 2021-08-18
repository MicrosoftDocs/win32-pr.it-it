---
description: 'Esistono tre tipi di oggetti voce XAudio2: voci di origine, submix e mastering.'
ms.assetid: 3a4acc03-e47a-ff33-dee8-a374051f85f6
title: Voci di XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b756033be5b64dbf03e3b3756902014774a53c9aebc8f41a1df1f982685cca16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025939"
---
# <a name="xaudio2-voices"></a>Voci di XAudio2

Esistono tre tipi di oggetti voce XAudio2: *voci* di origine, *submix* *e voci di* mastering. Le voci di origine operano sui dati forniti dal client. Le voci di origine e di missaggio secondario inviano l'output a una o più voci di missaggio secondario o mastering. Le voci di missaggio secondario e mastering missano l'audio proveniente da tutte le voci che le alimentano e operano sul risultato. Le voci mastering scrivono dati audio in un dispositivo audio.

## <a name="actions-performed-by-all-voices"></a>Azioni eseguite da tutte le voci

Tutte le voci eseguono le azioni seguenti in ordine sull'audio che le segue.

1.  Regolazione generale del volume, che influisce su tutti i canali audio. Vedere [**IXAudio2Voice::SetVolume.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume)
2.  Catena facoltativa specificata dal client di uno o più effetti DSP, ad esempio il riverbero predefinito o un effetto utente definito [**dall'interfaccia IXAPO.**](/windows/desktop/api/XAPO/nn-xapo-ixapo) Vedere [Effetti audio XAudio2.](xaudio2-audio-effects.md)
3.  Regolazione del volume di output per canale. Vedere [**IXAudio2Voice::SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes).
4.  Combinazione di matrici separata per ognuna delle voci di destinazione o per il dispositivo di output audio per la gestione delle voci. Questa combinazione modifica il numero di canali nell'audio, se necessario.

## <a name="source-voices"></a>Voci di origine

Usare le voci di origine per inviare dati audio nella pipeline di elaborazione XAudio2. Si tratta dei punti di ingresso nella classe [audio XAudio2 Graph](xaudio2-audio-graph.md). È necessario inviare i dati vocali a una voce mastering per essere ascoltati, direttamente o tramite voci submix intermedie.

Oltre alle azioni eseguite da tutte le voci, le voci di origine eseguono le azioni seguenti.

-   Se necessario, un decodificatore viene eseguito per primo per convertire i dati di origine codificati in Pulse Code Modulation (PCM).
-   Una conversione della frequenza di campionamento a frequenza variabile (SRC) converte i dati audio di origine della voce nella frequenza di campionamento prevista dalle voci di destinazione, se necessario, e supporta anche le modifiche del passo dinamico.
-   È possibile usare un filtro facoltativo per variabili di stato per colorare il suono in vari modi. Vedere [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).
-   È possibile applicare un filtro facoltativo agli output della voce. Vedere [**IXAudio2Voice::SetOutputFilterParameters.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters)

## <a name="submix-voices"></a>Voci submix

Una voce submix viene usata principalmente per migliorare le prestazioni ed eseguire l'elaborazione degli effetti. Non è possibile inviare i buffer di dati direttamente alle voci submix. Non sarà udibile a meno che non lo si invii a una voce di mastering. È possibile usare una voce submix per assicurarsi che un particolare set di dati vocali sia convertito nello stesso formato e che una particolare catena di effetti sia elaborata sul risultato collettivo.

Oltre alle azioni eseguite da tutte le voci, le voci submix eseguono le azioni seguenti.

-   Un SRC a velocità fissa viene eseguito nell'output della voce, se necessario, per convertire l'audio nella frequenza di campionamento prevista dalle voci di destinazione.
-   È possibile usare un filtro facoltativo per variabili di stato per colorare il suono in vari modi. Vedere [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).
-   È possibile applicare un filtro facoltativo agli output della voce. Vedere [**IXAudio2Voice::SetOutputFilterParameters.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters)

## <a name="mastering-voices"></a>Mastering Voices

Usare una voce di mastering per rappresentare il dispositivo di output audio. Non è possibile inviare i buffer di dati direttamente alle voci di mastering, ma i dati inviati ad altri tipi di voci devono essere inviati a una voce di mastering per essere ascoltati.

Oltre alle azioni eseguite da tutte le voci, le voci di mastering eseguono le azioni seguenti.

-   Se si crea la voce mastering con un valore *InputSampleRate* esplicito non supportato dal dispositivo audio, viene usato un SRC a velocità fissa per eseguire la conversione alla frequenza di campionamento più vicina supportata dal dispositivo.
-   Ritagliare l'audio di output finale, se richiesto dal dispositivo di output.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Voci](voices.md)
</dt> <dt>

[Guida alla programmazione di XAudio2](programming-guide.md)
</dt> <dt>

[**IXAudio2SourceVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)
</dt> <dt>

[**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)
</dt> <dt>

[**IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)
</dt> </dl>

 

 
