---
description: 'Sono disponibili tre tipi di oggetti voce XAudio2: Source, submix e mastering Voices.'
ms.assetid: 3a4acc03-e47a-ff33-dee8-a374051f85f6
title: Voci di XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b11300cea770f59485e8a78b0d30110b5469befe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317838"
---
# <a name="xaudio2-voices"></a>Voci di XAudio2

Sono disponibili tre tipi di oggetti voce XAudio2: *source*, *submix* e *Mastering* Voices. Le voci di origine operano sui dati forniti dal client. Le voci di origine e di missaggio secondario inviano l'output a una o più voci di missaggio secondario o mastering. Le voci di missaggio secondario e mastering missano l'audio proveniente da tutte le voci che le alimentano e operano sul risultato. Le voci mastering scrivono dati audio in un dispositivo audio.

## <a name="actions-performed-by-all-voices"></a>Azioni eseguite da tutte le voci

Tutte le voci eseguono le azioni seguenti in ordine sull'audio che viaggia comunque.

1.  Regolazione complessiva del volume, che interessano tutti i canali audio. Vedere [**IXAudio2Voice:: sevolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume).
2.  Una catena facoltativa specificata dal client di uno o più effetti DSP, ad esempio il riverbero incorporato o un effetto utente definito dall'interfaccia [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) . Vedere [XAudio2 Audio Effects](xaudio2-audio-effects.md).
3.  Regolazione del volume di output per canale. Vedere [**IXAudio2Voice:: SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes).
4.  Separare la combinazione di matrici in ogni voce di destinazione o nel dispositivo di output audio per le voci di mastering. Questa combinazione modifica il numero di canali nell'audio, se necessario.

## <a name="source-voices"></a>Voci di origine

Usare le voci di origine per inviare i dati audio alla pipeline di elaborazione XAudio2. Sono i punti di ingresso nel [grafico audio XAudio2](xaudio2-audio-graph.md). È necessario inviare i dati vocali a una voce di Mastering da ascoltare, direttamente o tramite le voci submix intermedie.

Oltre alle azioni eseguite da tutte le voci, le voci di origine eseguono le azioni seguenti.

-   Se necessario, viene eseguito prima un decodificatore per convertire i dati di origine codificati in Pulse Code Modulation (PCM).
-   Una conversione della frequenza di campionamento a frequenza variabile (SRC) converte i dati audio di origine della voce nella frequenza di campionamento prevista dalle voci di destinazione, se necessario, e supporta anche le modifiche di Dynamic pitch.
-   Un filtro facoltativo di variabile di stato può essere utilizzato per colorare il suono in diversi modi. Vedere [**IXAudio2Voice:: SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).
-   È possibile applicare un filtro facoltativo agli output della voce. Vedere [**IXAudio2Voice:: SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).

## <a name="submix-voices"></a>Voci di submix

Una voce submix viene utilizzata principalmente per i miglioramenti delle prestazioni e l'elaborazione degli effetti. Non è possibile inviare i buffer di dati direttamente alle voci submix. Non sarà udibile a meno che non lo invii a una voce Master. È possibile usare un submix Voice per assicurarsi che un particolare set di dati vocali venga convertito nello stesso formato e che una particolare catena di effetti venga elaborata sul risultato collettivo.

Oltre alle azioni eseguite da tutte le voci, le voci submix eseguono le azioni seguenti.

-   Un SRC a frequenza fissa viene eseguito sull'output della voce, se necessario, per convertire l'audio nella frequenza di campionamento prevista dalle voci di destinazione.
-   Un filtro facoltativo di variabile di stato può essere utilizzato per colorare il suono in diversi modi. Vedere [**IXAudio2Voice:: SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).
-   È possibile applicare un filtro facoltativo agli output della voce. Vedere [**IXAudio2Voice:: SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).

## <a name="mastering-voices"></a>Voci di mastering

Usare una voce Master per rappresentare il dispositivo di output audio. Non è possibile inviare i buffer di dati direttamente a voci di mastering, ma i dati inviati ad altri tipi di voci devono essere indirizzati a una voce di Mastering da sentire.

Oltre alle azioni eseguite da tutte le voci, le voci di mastering eseguono le azioni seguenti.

-   Se si crea la voce Master con un valore *InputSampleRate* esplicito che non è supportato dal dispositivo audio, viene usata una src a frequenza fissa per eseguire la conversione alla frequenza di campionamento più vicina supportata dal dispositivo.
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

 

 
