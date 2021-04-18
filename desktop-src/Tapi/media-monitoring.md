---
description: Quando una chiamata è nello stato connesso, i dati possono essere trasportati sulla chiamata. Il tipo di supporto di chiamata fornisce un'indicazione del tipo di dati (ad esempio, il tipo di dati o il protocollo di livello superiore) del flusso multimediale.
ms.assetid: 3281387e-3f72-4fda-8199-b3ce6e45e910
title: Monitoraggio dei supporti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb54989306fd80c48c0b99c9f8285a83b40bed25
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320657"
---
# <a name="media-monitoring"></a>Monitoraggio dei supporti

Quando una chiamata è nello stato *connesso* , i dati possono essere trasportati sulla chiamata. Il tipo di supporto di chiamata fornisce un'indicazione del tipo di dati (ad esempio, il tipo di dati o il protocollo di livello superiore) del flusso multimediale.

TAPI consente di fornire le applicazioni con una notifica sulle modifiche apportate al tipo di supporto di una chiamata. La notifica fornisce un'indicazione del nuovo tipo di supporto della chiamata. Il provider di servizi decide come desidera effettuare questa determinazione. Il provider di servizi, ad esempio, può usare l'elaborazione del segnale del flusso multimediale per determinare il tipo di supporto oppure può basarsi su modelli di suoneria distinti assegnati a flussi multimediali diversi o su elementi di informazioni passati in un protocollo di segnalazione fuori banda. Indipendentemente dal modo in cui viene eseguita la determinazione del tipo di supporto, l'applicazione viene semplicemente informati sulle modifiche del tipo di supporto in una chiamata esistente.

Per ulteriori informazioni e per un elenco dei tipi di supporti o delle modalità TAPI attualmente definiti, vedere [ \_ costanti LINEMEDIAMODE](linemediamode--constants.md). I provider di servizi possono implementare tipi di supporto specifici del provider per i dispositivi altamente specializzati. Le informazioni su questi dati saranno disponibili nella documentazione del dispositivo.

I tipi di supporto definiti da TAPI includono:

-   Sconosciuto. Il tipo di supporto della chiamata non è attualmente noto — la chiamata non è classificata.
-   Voce interattiva. L'energia vocale è stata rilevata nella chiamata e la chiamata viene gestita come chiamata vocale interattiva con una persona al termine dell'applicazione.
-   Voice automatizzato. L'energia vocale è stata rilevata nella chiamata e la chiamata viene gestita come chiamata vocale, ma senza persona alla fine dell'applicazione, ad esempio con un'applicazione per la segreteria del computer.
-   Modem dati. Una sessione modem sulla chiamata. Per i protocolli modem correnti è richiesta la stazione chiamata per avviare l'handshake. Per una chiamata al modem dati in ingresso, l'applicazione in genere non può eseguire alcun rilevamento positivo. Il modo in cui il provider di servizi effettua questa determinazione è la scelta. Ad esempio, un periodo di silenzio immediatamente dopo la risposta a una chiamata in ingresso può essere usato come euristica per decidere che potrebbe trattarsi di una chiamata al modem dati.
-   Fax G3. Una sessione fax del gruppo 3 nella chiamata.
-   Fax G4. Una sessione fax del gruppo 4 nella chiamata.
-   TDD. Il flusso multimediale della chiamata usa i dispositivi di telefonia per il protocollo Deaf.
-   Dati digitali. Flusso di dati digitali di formato non specificato.
-   Teletex, videotex, telex, misto. Questi corrispondono ai servizi telematici con gli stessi nomi.
-   ADSI. Una sessione di interfaccia di servizi di visualizzazione analoga nella chiamata. ADSI migliora le chiamate vocali con le informazioni alfanumeriche scaricate sul telefono e l'uso di pulsanti soft sul telefono.

Un'applicazione può abilitare o disabilitare il monitoraggio dei supporti in una chiamata specificata con [**lineMonitorMedia**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia). L'applicazione specifica quali tipi di supporti sono interessati al monitoraggio e quando il monitoraggio dei supporti è abilitato, il rilevamento di una modifica del tipo di supporto causa la notifica dell'applicazione con il messaggio di [**riga \_ MONITORMEDIA**](line-monitormedia.md) . Questo messaggio fornisce l'handle di chiamata su cui è stata rilevata la modifica del tipo di supporto e il nuovo tipo di supporto.

Esiste una differenza tra il tipo di supporto di una chiamata come segnalato da [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) e l'evento Media Type segnala i messaggi di riga \_ MONITORMEDIA. Il tipo di supporto di una chiamata viene determinato esclusivamente dalle applicazioni proprietarie della chiamata e non viene modificato automaticamente dagli eventi di monitoraggio multimediale. L'unica eccezione è la determinazione iniziale del tipo di supporto che può essere eseguita dalla libreria a collegamento dinamico TAPI per selezionare il primo proprietario di una chiamata. Si può affermare che in questo caso la libreria è il proprietario della chiamata.

Viene eseguito il monitoraggio del tipo di supporto predefinito per i tipi di supporto per i quali è stato aperto il dispositivo a linee. Ciò consente di determinare il tipo di supporto di una chiamata in ingresso prima che la chiamata venga passata a un'applicazione in base alle richieste dell'applicazione. L'ambito del monitoraggio del supporto di una chiamata è associato alla durata della chiamata. Il monitoraggio dei supporti in una chiamata termina non appena la chiamata si *disconnette* o diventa *inattiva*.

Un'applicazione può ottenere gli identificatori dei dispositivi per varie classi di dispositivi associate a una riga aperta chiamando [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid). Questa funzione accetta un handle di riga, un indirizzo o un handle di chiamata e una descrizione della classe del dispositivo. Restituisce l'identificatore del dispositivo per il dispositivo della classe di dispositivo specificata associata al dispositivo, all'indirizzo o alla chiamata open line. Se la classe del dispositivo è "TAPI/line", viene restituito l'identificatore del dispositivo della linea. Se la classe del dispositivo è "MCI/Wave", viene restituito l'identificatore del dispositivo WaveAudio MCI (se supportato), che consente attività come la registrazione o la riproduzione di audio sulla chiamata sulla riga.

L'applicazione può usare l'identificatore di dispositivo restituito con l'API media corrispondente per eseguire query sulle funzionalità del dispositivo e successivamente aprire il dispositivo multimediale. Ad esempio, se l'applicazione deve usare la riga come dispositivo di forma d'onda, deve prima chiamare [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps) e/o [**waveOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps) per determinare le funzionalità di forma d'onda del dispositivo. Il formato dei dati della forma d'onda tipico supportato dalla telefonia in America del Nord è la m-Law a 8 bit a 8000 campioni al secondo, sebbene il driver di dispositivo Wave possa convertire questa frequenza di campionamento e companding ad altri formati audio multimediali più comuni.

Per aprire successivamente un dispositivo a linee per la riproduzione audio usando l'API Waveform, un'applicazione chiama [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen). L'implementazione di **waveOutOpen** è specifica del dispositivo e sono disponibili diverse opzioni per l'implementazione di questa funzione.

 

 
