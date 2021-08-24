---
description: Le interfacce di evento (notifica) consentono a un'applicazione TAPI 3 di rispondere agli eventi asincroni.
ms.assetid: 27fd91e8-b628-49ee-af4e-9aec0afa5449
title: Interfacce eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01a4ecf097d761e98b723b37d9de6adcfd7ebb60696ce5e389426965534d63f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660841"
---
# <a name="event-interfaces"></a>Interfacce eventi

Le interfacce di evento (notifica) consentono a un'applicazione TAPI 3 di rispondere agli eventi asincroni.

È necessario chiamare il [**metodo ITTAPI::p ut \_ EventFilter**](/windows/win32/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) e impostare una maschera di filtro eventi per abilitare la ricezione degli eventi di richiesta. Se non si chiama **ITTAPI::p ut \_ EventFilter,** l'applicazione non riceverà eventi.

Per una descrizione [del modo](./asynchronous-spontaneous-events.md) in cui un'applicazione garantisce la ricezione delle notifiche, vedere panoramica degli eventi. Per altre informazioni sull'impostazione di una maschera di filtro per i singoli tipi di evento, vedere le singole interfacce elencate nella tabella seguente.



| Interfaccia                                                           | Descrizione                                                                                                                                 |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITAddressEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itaddressevent)                   | Recupera la descrizione degli eventi di indirizzo.                                                                                                |
| [**ITASRTerminalEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itasrterminalevent)           | Recupera la descrizione degli eventi del terminale riconoscimento vocale automatico.                                                                  |
| [**ITCallHubEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallhubevent)                   | Recupera la descrizione degli eventi CallHub.                                                                                                |
| [**ITCallInfoChangeEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallinfochangeevent)     | Recupera la descrizione degli eventi di modifica delle informazioni sulle chiamate.                                                                                |
| [**ITCallMediaEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallmediaevent)               | Recupera la descrizione degli eventi multimediali di chiamata.                                                                                             |
| [**ITCallNotificationEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallnotificationevent) | Recupera la descrizione degli eventi di notifica delle chiamate.                                                                                      |
| [**ITCallStateEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallstateevent)               | Recupera la descrizione degli eventi di stato della chiamata.                                                                                             |
| [**ITDigitDetectionEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itdigitdetectionevent)     | Recupera informazioni sugli eventi di cifra DTMF durante una chiamata.                                                                                |
| [**ITDigitGenerationEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itdigitgenerationevent)   | Recupera informazioni sulle chiamate che richiedono la generazione di cifre DTMF.                                                               |
| [**ITDigitsGatheredEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itdigitsgatheredevent)     | Recupera i dati correlati alla richiesta di raccolta delle cifre di un'applicazione.                                                                         |
| [**ITFileTerminalEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itfileterminalevent)         | Recupera la descrizione degli eventi del terminale file.                                                                                          |
| [**ITParticipantEvent**](./itparticipantevent.md)           | Recupera la descrizione degli eventi dei partecipanti alla conferenza.                                                                                 |
| [**ITPhoneEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itphoneevent)                       | Recupera la descrizione degli eventi del telefono.                                                                                                  |
| [**ITQOSEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent)                           | Recupera la descrizione degli eventi QOS (Quality of Service).                                                                               |
| [**ITQueueEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueueevent)                       | Recupera la descrizione degli eventi della coda acd (Automatic Call Distribution).                                                                |
| [**ITRequestEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itrequestevent)                   | Recupera la descrizione degli [eventi di richiesta di telefonia](./assisted-telephony-overview.md) assistita.                                 |
| [**ITTAPIObjectEvent**](/windows/win32/api/tapi3if/nn-tapi3if-ittapiobjectevent)             | Recupera la descrizione degli eventi dell'oggetto TAPI.                                                                                            |
| [**ITTAPIObjectEvent2**](/windows/win32/api/tapi3if/nn-tapi3if-ittapiobjectevent2)           | Estende [**ITTAPIObjectEvent**](/windows/win32/api/tapi3if/nn-tapi3if-ittapiobjectevent); recupera un puntatore all'oggetto telefono che ha causato l'evento dell'oggetto TAPI. |
| [**ITToneDetectionEvent**](/windows/win32/api/tapi3if/nn-tapi3if-ittonedetectionevent)       | Recupera informazioni su un evento di rilevamento del tono.                                                                                         |
| [**ITToneTerminalEvent**](/windows/win32/api/tapi3if/nn-tapi3if-ittoneterminalevent)         | Recupera la descrizione degli eventi del terminale tono.                                                                                          |
| [**ITTTSTerminalEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itttsterminalevent)           | Recupera la descrizione degli eventi del terminale di sintesi vocale (TTS).                                                                          |



 



| Interfaccia                                                                                             | Descrizione                                                                                      |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**ITPluggableTerminalEventSink**](/windows/win32/api/tapi3/nn-tapi3-itpluggableterminaleventsink)                         | Notifica alle applicazioni client le modifiche apportate a un terminale collegabile.                              |
| [**ITPluggableTerminalEventSinkRegistration**](/windows/win32/api/tapi3/nn-tapi3-itpluggableterminaleventsinkregistration) | Registra e annulla la registrazione di un'applicazione client per la notifica degli eventi del terminale collegabili. |



 

 

 
