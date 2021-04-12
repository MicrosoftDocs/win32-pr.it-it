---
description: Le interfacce di evento (notifica) consentono a un'applicazione TAPI 3 di rispondere agli eventi asincroni.
ms.assetid: 27fd91e8-b628-49ee-af4e-9aec0afa5449
title: Interfacce evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd7b705c89988ff62d972e594ceb936bb01db78e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526317"
---
# <a name="event-interfaces"></a>Interfacce evento

Le interfacce di evento (notifica) consentono a un'applicazione TAPI 3 di rispondere agli eventi asincroni.

È necessario chiamare il metodo [**ITTAPI::p UT \_ EventFilter**](/windows/win32/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) e impostare una maschera di filtro eventi per abilitare la ricezione degli eventi di richiesta. Se non si chiama **ITTAPI::p UT \_ EventFilter**, l'applicazione non riceverà alcun evento.

Per una descrizione del modo in cui un'applicazione garantisce la ricezione di notifiche, vedere la panoramica degli [eventi](./asynchronous-spontaneous-events.md) . Per ulteriori informazioni sull'impostazione di una maschera di filtro per i singoli tipi di evento, vedere le singole interfacce elencate nella tabella seguente.



| Interfaccia                                                           | Descrizione                                                                                                                                 |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITAddressEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itaddressevent)                   | Recupera la descrizione degli eventi di indirizzo.                                                                                                |
| [**ITASRTerminalEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itasrterminalevent)           | Recupera la descrizione degli eventi del terminale di riconoscimento vocale automatico.                                                                  |
| [**ITCallHubEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallhubevent)                   | Recupera la descrizione degli eventi CallHub.                                                                                                |
| [**ITCallInfoChangeEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallinfochangeevent)     | Recupera la descrizione degli eventi di modifica delle informazioni sulle chiamate.                                                                                |
| [**ITCallMediaEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallmediaevent)               | Recupera la descrizione degli eventi del supporto di chiamata.                                                                                             |
| [**ITCallNotificationEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallnotificationevent) | Recupera la descrizione degli eventi di notifica della chiamata.                                                                                      |
| [**ITCallStateEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallstateevent)               | Recupera la descrizione degli eventi dello stato di chiamata.                                                                                             |
| [**ITDigitDetectionEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itdigitdetectionevent)     | Recupera informazioni sugli eventi di cifre DTMF durante una chiamata.                                                                                |
| [**ITDigitGenerationEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itdigitgenerationevent)   | Recupera le informazioni sulle chiamate che richiedono la generazione di cifre DTMF.                                                               |
| [**ITDigitsGatheredEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itdigitsgatheredevent)     | Recupera i dati correlati alla richiesta di raccolta di cifre di un'applicazione.                                                                         |
| [**ITFileTerminalEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itfileterminalevent)         | Recupera la descrizione degli eventi terminal del file.                                                                                          |
| [**ITParticipantEvent**](./itparticipantevent.md)           | Recupera la descrizione degli eventi del partecipante della conferenza.                                                                                 |
| [**ITPhoneEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itphoneevent)                       | Recupera la descrizione degli eventi del telefono.                                                                                                  |
| [**ITQOSEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent)                           | Recupera la descrizione degli eventi di qualità del servizio (QOS).                                                                               |
| [**ITQueueEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueueevent)                       | Recupera la descrizione degli eventi della coda di distribuzione automatica delle chiamate (ACD).                                                                |
| [**ITRequestEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itrequestevent)                   | Recupera la descrizione degli eventi di richiesta di [telefonia assistita](./assisted-telephony-overview.md) .                                 |
| [**ITTAPIObjectEvent**](/windows/win32/api/tapi3if/nn-tapi3if-ittapiobjectevent)             | Recupera la descrizione degli eventi dell'oggetto TAPI.                                                                                            |
| [**ITTAPIObjectEvent2**](/windows/win32/api/tapi3if/nn-tapi3if-ittapiobjectevent2)           | Estende [**ITTAPIObjectEvent**](/windows/win32/api/tapi3if/nn-tapi3if-ittapiobjectevent); Recupera un puntatore all'oggetto Phone che ha causato l'evento dell'oggetto TAPI. |
| [**ITToneDetectionEvent**](/windows/win32/api/tapi3if/nn-tapi3if-ittonedetectionevent)       | Recupera informazioni su un evento di rilevamento di un tono.                                                                                         |
| [**ITToneTerminalEvent**](/windows/win32/api/tapi3if/nn-tapi3if-ittoneterminalevent)         | Recupera la descrizione degli eventi del terminale di tono.                                                                                          |
| [**ITTTSTerminalEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itttsterminalevent)           | Recupera la descrizione degli eventi del terminale di sintesi vocale.                                                                          |



 



| Interfaccia                                                                                             | Descrizione                                                                                      |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**ITPluggableTerminalEventSink**](/windows/win32/api/tapi3/nn-tapi3-itpluggableterminaleventsink)                         | Notifica alle applicazioni client le modifiche apportate a un terminale innestabile.                              |
| [**ITPluggableTerminalEventSinkRegistration**](/windows/win32/api/tapi3/nn-tapi3-itpluggableterminaleventsinkregistration) | Registra e Annulla la registrazione di un'applicazione client per la notifica di eventi Terminal collegabili. |



 

 

 
