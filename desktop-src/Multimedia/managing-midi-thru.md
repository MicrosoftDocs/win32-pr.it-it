---
title: Gestione di MIDI Thru
description: Gestione di MIDI Thru
ms.assetid: ba03a2a1-d998-498d-ad53-027ba2b6e276
keywords:
- Instrument Digital Interface (MIDI), driver thru
- MIDI (Instrument Digital Interface), driver thru
- registrazione di audio MIDI, driver thru
- Driver MIDI thru
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c108ac13fbbfb80d1f7c41960984c904374db31e3a790f14c326cf9e7946dac9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138944"
---
# <a name="managing-midi-thru"></a>Gestione di MIDI Thru

È possibile connettere un dispositivo di input MIDI direttamente a un dispositivo di output MIDI in modo che, quando il dispositivo di input riceve un messaggio [**MIM \_ DATA,**](mim-data.md) il sistema invii un messaggio con gli stessi dati degli eventi MIDI al driver di dispositivo di output. Per connettere un dispositivo di output MIDI a un dispositivo di input MIDI, usare la [**funzione midiConnect.**](/windows/win32/api/mmeapi/nf-mmeapi-midiconnect)

Per ottenere le migliori prestazioni possibili con più output, un'applicazione può scegliere di fornire una forma speciale di driver di output MIDI, denominato *driver thru.* Anche se il sistema consente la connessione di un solo dispositivo di output MIDI a un dispositivo di input MIDI, è possibile collegare più dispositivi di output MIDI a un driver thru. Un'applicazione in un sistema di questo tipo potrebbe connettere il dispositivo di input MIDI a questo dispositivo e connettere il dispositivo MIDI a tutti i dispositivi di output MIDI necessari. Per altre informazioni sui driver thru, vedere la Windows device-driver.

## <a name="using-messages-to-manage-midi-recording"></a>Uso dei messaggi per gestire la registrazione MIDI

I messaggi seguenti possono essere inviati a una routine di callback di finestra o thread per la gestione della registrazione MIDI.



| Valore                                          | Significato                                                                                                                                |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**MM \_ MIM \_ CLOSE**](mm-mim-close.md)         | Inviato quando un dispositivo di input MIDI viene chiuso usando la [**funzione midiInClose.**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose)                                      |
| [**DATI \_ MIM \_ MM**](mm-mim-data.md)           | Inviato quando viene ricevuto un messaggio MIDI completo. Questo messaggio viene usato per tutti i messaggi MIDI ad eccezione dei messaggi esclusivi di sistema.          |
| [**ERRORE \_ MIM \_ MM**](mm-mim-error.md)         | Inviato quando viene ricevuto un messaggio MIDI non valido. Questo messaggio viene usato per tutti i messaggi MIDI ad eccezione dei messaggi esclusivi di sistema.          |
| [**MM \_ MIM \_ LONGDATA**](mm-mim-longdata.md)   | Inviato quando viene ricevuto un messaggio esclusivo di sistema MIDI completo o quando un buffer è stato riempito con dati esclusivi del sistema.     |
| [**MM \_ MIM \_ LONGERROR**](mm-mim-longerror.md) | Inviato quando viene ricevuto un messaggio esclusivo di sistema MIDI non valido.                                                                        |
| [**MM \_ MIM \_ MOREDATA**](mm-mim-moredata.md)   | Inviato quando un'applicazione non elabora i [**MIM \_ dati**](mim-data.md) in modo sufficientemente veloce da rimanere al passo con il driver di dispositivo di input. |
| [**MM \_ MIM \_ OPEN**](mm-mim-open.md)           | Inviato quando un dispositivo di input MIDI viene aperto usando la [**funzione midiInOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)                                        |



 

A ognuno di questi messaggi sono associati un parametro *wParam* e un parametro *lParam.* Il *parametro wParam* specifica sempre l'handle di un dispositivo MIDI aperto. Il *parametro lParam* non viene usato per i messaggi [**MM MIM \_ \_ CLOSE**](mm-mim-close.md) [**e MM MIM \_ \_ OPEN.**](mm-mim-open.md)

Per il [**messaggio MM \_ MIM \_ LONGDATA,**](mm-mim-longdata.md) *lpMidiHdr* specifica un indirizzo di una [**struttura MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) che identifica il buffer per i messaggi esclusivi del sistema. Il buffer potrebbe non essere completamente riempito, perché le dimensioni dei messaggi esclusivi del sistema non sono in genere note prima della registrazione e perché i buffer la cui dimensione totale può contenere il messaggio più grande previsto devono essere allocati. Per determinare la quantità di dati validi presenti nel buffer, usare il **membro dwBytesRecorded** della **struttura MIDIHDR.**

## <a name="using-a-callback-function-to-manage-midi-recording"></a>Uso di una funzione di callback per gestire la registrazione MIDI

È possibile definire una funzione di callback personalizzata per gestire la registrazione per i dispositivi di input MIDI. La funzione di callback è documentata [**come MidiInProc.**](/previous-versions//dd798460(v=vs.85))

I messaggi seguenti possono essere inviati al *parametro wMsg* della funzione di callback **MidiInProc.**



| Valore                                   | Significato                                                                                                                                |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**\_MIM Vicino**](mim-close.md)         | Inviato quando il dispositivo viene chiuso usando la [**funzione midiInClose.**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose)                                               |
| [**\_MIM Dati**](mim-data.md)           | Inviato quando viene ricevuto un messaggio MIDI completo (questo messaggio viene usato per tutti i messaggi MIDI ad eccezione dei messaggi esclusivi del sistema).           |
| [**\_MIM Errore**](mim-error.md)         | Inviato quando viene ricevuto un messaggio MIDI non valido (questo messaggio viene usato per tutti i messaggi MIDI ad eccezione dei messaggi esclusivi del sistema).           |
| [**\_MIM LONGDATA**](mim-longdata.md)   | Inviato quando viene ricevuto un messaggio esclusivo di sistema MIDI completo o quando un buffer è stato riempito con dati esclusivi del sistema.     |
| [**\_MIM LONGERROR**](mim-longerror.md) | Inviato quando viene ricevuto un messaggio esclusivo di sistema MIDI non valido.                                                                        |
| [**\_MIM MOREDATA**](mim-moredata.md)   | Inviato quando un'applicazione non elabora i [**MIM \_ dati**](mim-data.md) in modo sufficientemente veloce da rimanere al passo con il driver di dispositivo di input. |
| [**\_MIM Aperto**](mim-open.md)           | Inviato quando il dispositivo di input MIDI viene aperto usando la [**funzione midiInOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)                                      |



 

Questi messaggi sono simili a quelli inviati alle funzioni di routine della finestra, ma i parametri sono diversi. Un handle del dispositivo MIDI aperto viene passato come parametro alla funzione di callback, insieme alla doppia parola dei dati dell'istanza passati tramite **midiInOpen.**

Per il [**MIM \_ LONGDATA,**](mim-longdata.md) *lpMidiHdr* specifica un indirizzo di una struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) che identifica il buffer per i messaggi esclusivi del sistema. Il buffer potrebbe non essere completamente riempito. Per determinare la quantità di dati validi presenti nel buffer, usare il **membro dwBytesRecorded** della **struttura MIDIHDR.**

Dopo aver completato il driver di dispositivo con un blocco di dati, è possibile pulire e liberare il blocco di dati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione di audio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 