---
title: Gestione dei blocchi di dati MIDI
description: Gestione dei blocchi di dati MIDI
ms.assetid: f29fbc08-ef67-489c-aedf-5a2bc65233f7
keywords:
- MIDI (Musical Instrument Digital Interface), gestione di blocchi di dati
- MIDI (Musical Instrument Digital Interface), gestione di blocchi di dati
- Servizi MIDI, gestione di blocchi di dati
- gestione dei blocchi di dati MIDI
- MIDI (Musical Instrument Digital Interface), elaborazione dei messaggi del driver
- MIDI (Musical Instrument Digital Interface), elaborazione dei messaggi del driver
- Servizi MIDI, elaborazione dei messaggi del driver
- elaborazione dei messaggi del driver
- MIDI (Musical Instrument Digital Interface), blocchi di dati
- MIDI (Musical Instrument Digital Interface), blocchi di dati
- Servizi MIDI, blocchi di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af348d6c53d2944bf22c026674704baa1fe74e07
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956390"
---
# <a name="managing-midi-data-blocks"></a>Gestione dei blocchi di dati MIDI

Le applicazioni che utilizzano blocchi di dati per passare i messaggi esclusivi del sistema (mediante le funzioni [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) e [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) ) e i buffer di flusso (mediante la funzione [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) ) devono fornire continuamente al driver di dispositivo i blocchi di dati fino al completamento della riproduzione o della registrazione.

Anche se viene utilizzato un singolo blocco di dati, un'applicazione deve essere in grado di determinare quando un driver di dispositivo è terminato con il blocco di dati, in modo da poter liberare la memoria associata al blocco di dati e alla struttura dell'intestazione. Per determinare quando un driver di dispositivo è terminato con un blocco di dati, è possibile usare tre metodi:

-   Specificare una funzione di callback per ricevere un messaggio inviato dal driver al termine di un blocco di dati. Per ottenere i dati di input MIDI timestamp, è necessario usare una funzione di callback.
-   Usare un callback di evento (solo per l'output).
-   Usare un callback di finestra o di thread per ricevere un messaggio inviato dal driver al termine di un blocco di dati.

Se un'applicazione non ottiene un blocco di dati per il driver di dispositivo quando necessario, potrebbe verificarsi una lacuna udibile nella riproduzione o una perdita di informazioni registrate in arrivo. Come minimo, un'applicazione deve usare uno schema a doppio buffer per mantenere almeno un blocco di dati prima del driver di dispositivo.

## <a name="using-a-callback-function-to-process-driver-messages"></a>Utilizzo di una funzione di callback per elaborare i messaggi del driver

È possibile scrivere una funzione di callback personalizzata per elaborare i messaggi inviati dal driver di dispositivo. Per usare una funzione di callback, specificare il \_ flag della funzione di callback nel parametro *dwFlags* e l'indirizzo della funzione di callback nel parametro *dwCallback* della funzione [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) o [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .

I messaggi inviati a una funzione di callback sono simili ai messaggi inviati a una finestra, con la differenza che hanno due parametri parola doppia anziché un parametro Unsigned Integer e un parametro parola doppia. Per ulteriori informazioni su questi messaggi, vedere [invio di messaggi di System-Exclusive](sending-system-exclusive-messages.md) e [gestione della registrazione MIDI](managing-midi-recording.md).

Usare una delle tecniche seguenti per passare i dati dell'istanza da un'applicazione a una funzione di callback:

-   Usare il parametro *dwCallbackInstance* della funzione che apre il driver di dispositivo.
-   Usare il membro **dwUser** della struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) che identifica un blocco di dati inviato a un driver di dispositivo MIDI.

Se sono necessari più di 32 bit di dati dell'istanza, passare un indirizzo di una struttura contenente le informazioni aggiuntive.

## <a name="using-an-event-callback-to-process-driver-messages"></a>Utilizzo di un callback di evento per elaborare i messaggi del driver

Per usare un callback di evento, usare la funzione [CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) per recuperare l'handle di un evento e specificare un evento di callback \_ nella chiamata alla funzione [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .

Un callback di evento viene impostato da qualsiasi elemento che potrebbe causare un callback di funzione. Diversamente dalle funzioni di callback e dai callback della finestra o del thread, i callback degli eventi non ricevono notifiche di chiusura, fine o apertura specifiche. È pertanto possibile che un'applicazione debba controllare lo stato del processo in attesa dopo l'evento.

Per ulteriori informazioni sui callback di evento, vedere [utilizzo di un callback di evento per gestire la riproduzione memorizzata nel buffer](using-an-callback-to-manage-buffered-playback.md).

## <a name="using-a-window-or-thread-callback-to-process-driver-messages"></a>Utilizzo di una finestra o di un callback di thread per elaborare i messaggi del driver

Per usare un callback della finestra, specificare il \_ flag della finestra di callback nel parametro *dwFlags* e un handle di finestra nella parola di ordine inferiore del parametro *dwCallback* della funzione [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) o [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) . I messaggi del driver verranno inviati alla funzione routine della finestra per la finestra identificata dall'handle in *dwCallback*.

Analogamente, per usare un callback di thread, specificare il flag del thread di CALLBACK \_ e un identificatore del thread nella chiamata a **MidiInOpen** o **midiOutOpen**. In questo caso, i messaggi verranno inviati al thread specificato anziché a una finestra.

I messaggi inviati a una finestra o a un callback di thread sono specifici del dispositivo MIDI usato. Per ulteriori informazioni su questi messaggi, vedere [invio di messaggi di System-Exclusive](sending-system-exclusive-messages.md) e [gestione della registrazione MIDI](managing-midi-recording.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Servizi MIDI](midi-services.md)
</dt> </dl>

 

 