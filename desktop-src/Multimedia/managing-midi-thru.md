---
title: Gestione di MIDI Thru
description: Gestione di MIDI Thru
ms.assetid: ba03a2a1-d998-498d-ad53-027ba2b6e276
keywords:
- Digital Instrumental Interface (MIDI), thru driver
- MIDI (Musical Instrument Digital Interface), thru driver
- registrazione audio MIDI, driver thru
- Driver MIDI Thru
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24214dd3f6cd13ca034b2555398f6055e4ce2da1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956389"
---
# <a name="managing-midi-thru"></a>Gestione di MIDI Thru

È possibile connettere un dispositivo di input MIDI direttamente a un dispositivo di output MIDI, in modo che quando il dispositivo di input riceve un messaggio di [**\_ dati MIM**](mim-data.md) , il sistema invia un messaggio con gli stessi dati di evento MIDI al driver di dispositivo di output. Per connettere un dispositivo di output MIDI a un dispositivo di input MIDI, usare la funzione [**midiConnect**](/windows/win32/api/mmeapi/nf-mmeapi-midiconnect) .

Per ottenere le migliori prestazioni possibili con più output, un'applicazione può scegliere di fornire un modulo speciale di driver di output MIDI, denominato *driver thru*. Sebbene il sistema consenta la connessione di un solo dispositivo di output MIDI a un dispositivo di input MIDI, è possibile connettere più dispositivi di output MIDI a un driver thru. Un'applicazione in un sistema di questo tipo potrebbe connettere il dispositivo di input MIDI a questo dispositivo tramite e connettere il dispositivo MIDI Thru a tutti i dispositivi di output MIDI necessari. Per ulteriori informazioni sui driver thru, vedere la documentazione di Windows Device-driver.

## <a name="using-messages-to-manage-midi-recording"></a>Uso dei messaggi per gestire la registrazione MIDI

I messaggi seguenti possono essere inviati a una procedura di callback di finestra o di thread per la gestione della registrazione MIDI.



| Valore                                          | Significato                                                                                                                                |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**MM \_ di \_ chiusura MIM**](mm-mim-close.md)         | Inviato quando un dispositivo di input MIDI viene chiuso tramite la funzione [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) .                                      |
| [**\_dati MIM \_ mm**](mm-mim-data.md)           | Inviato quando viene ricevuto un messaggio MIDI completo. (Questo messaggio viene usato per tutti i messaggi MIDI ad eccezione dei messaggi esclusivi del sistema).          |
| [**\_errore MIM \_ mm**](mm-mim-error.md)         | Inviato quando viene ricevuto un messaggio MIDI non valido. (Questo messaggio viene usato per tutti i messaggi MIDI ad eccezione dei messaggi esclusivi del sistema).          |
| [**\_LONGDATA MIM \_ mm**](mm-mim-longdata.md)   | Inviato quando viene ricevuto un messaggio esclusivo del sistema MIDI completo o quando un buffer è stato riempito con dati esclusivi del sistema.     |
| [**\_LONGERROR MIM \_ mm**](mm-mim-longerror.md) | Inviato quando viene ricevuto un messaggio esclusivo del sistema MIDI non valido.                                                                        |
| [**\_MOREDATA MIM \_ mm**](mm-mim-moredata.md)   | Inviato quando un'applicazione non elabora i messaggi di [**\_ dati MIM**](mim-data.md) abbastanza rapidamente da restare al passo con il driver di dispositivo di input. |
| [**\_apertura MIM \_ mm**](mm-mim-open.md)           | Inviato quando un dispositivo di input MIDI viene aperto tramite la funzione [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .                                        |



 

Un parametro *wParam* e un parametro *lParam* sono associati a ognuno di questi messaggi. Il parametro *wParam* specifica sempre l'handle di un dispositivo MIDI aperto. Il parametro *lParam* non è usato per i messaggi aperti di [**mm \_ MIM \_ Close**](mm-mim-close.md) e [**mm \_ MIM \_**](mm-mim-open.md) .

Per il [**messaggio \_ \_ LONGDATA MIM mm**](mm-mim-longdata.md) , *lpMidiHdr* specifica un indirizzo di una struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) che identifica il buffer per i messaggi esclusivi del sistema. Il buffer non può essere riempito completamente, perché la dimensione dei messaggi esclusivi del sistema non è in genere nota prima di essere registrata e perché i buffer le cui dimensioni totali possono contenere il messaggio massimo previsto devono essere allocati. Per determinare la quantità di dati validi presenti nel buffer, usare il membro **dwBytesRecorded** della struttura **MIDIHDR** .

## <a name="using-a-callback-function-to-manage-midi-recording"></a>Uso di una funzione di callback per gestire la registrazione MIDI

È possibile definire una funzione di callback personalizzata per gestire la registrazione per i dispositivi di input MIDI. La funzione di callback è documentata come [**MidiInProc**](/previous-versions//dd798460(v=vs.85)).

I messaggi seguenti possono essere inviati al parametro *wmsg* della funzione di callback **MidiInProc** .



| Valore                                   | Significato                                                                                                                                |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**\_chiusura MIM**](mim-close.md)         | Inviato quando il dispositivo viene chiuso tramite la funzione [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) .                                               |
| [**\_dati MIM**](mim-data.md)           | Inviato quando viene ricevuto un messaggio MIDI completo (questo messaggio viene usato per tutti i messaggi MIDI ad eccezione dei messaggi esclusivi del sistema).           |
| [**\_errore MIM**](mim-error.md)         | Inviato quando viene ricevuto un messaggio MIDI non valido (questo messaggio viene usato per tutti i messaggi MIDI ad eccezione dei messaggi esclusivi del sistema).           |
| [**\_LONGDATA MIM**](mim-longdata.md)   | Inviato quando viene ricevuto un messaggio esclusivo del sistema MIDI completo o quando un buffer è stato riempito con dati esclusivi del sistema.     |
| [**\_LONGERROR MIM**](mim-longerror.md) | Inviato quando viene ricevuto un messaggio esclusivo del sistema MIDI non valido.                                                                        |
| [**\_MOREDATA MIM**](mim-moredata.md)   | Inviato quando un'applicazione non elabora i messaggi di [**\_ dati MIM**](mim-data.md) abbastanza rapidamente da restare al passo con il driver di dispositivo di input. |
| [**MIM \_ aperto**](mim-open.md)           | Inviato quando il dispositivo di input MIDI viene aperto tramite la funzione [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .                                      |



 

Questi messaggi sono simili a quelli inviati alle funzioni di routine della finestra, ma i parametri sono diversi. Un handle del dispositivo MIDI aperto viene passato come parametro alla funzione di callback, insieme al parola doppia dei dati dell'istanza passati usando **midiInOpen**.

Per il [**messaggio \_ LONGDATA MIM**](mim-longdata.md) , *lpMidiHdr* specifica un indirizzo di una struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) che identifica il buffer per i messaggi esclusivi del sistema. Il buffer potrebbe non essere riempito completamente. Per determinare la quantità di dati validi presenti nel buffer, usare il membro **dwBytesRecorded** della struttura **MIDIHDR** .

Una volta che il driver di dispositivo è terminato con un blocco di dati, è possibile pulire e liberare il blocco di dati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione audio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 