---
description: La notifica degli eventi è il mezzo principale mediante il quale un'applicazione ottiene informazioni da TAPI e dai provider di servizi.
ms.assetid: 02160f10-dc3f-484c-9cd3-bcfb07ded822
title: Notifica dell'evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63aa232b0e712a76442c298ea04e24ec7671cb4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311897"
---
# <a name="event-notification"></a>Notifica dell'evento

La notifica degli eventi è il mezzo principale mediante il quale un'applicazione ottiene informazioni da TAPI e dai provider di servizi. Queste informazioni possono essere lo stato di un'operazione asincrona istigata dall'applicazione o possono riguardare un processo avviato all'esterno dell'applicazione, ad esempio le notifiche di nuove chiamate in ingresso.

**TAPI 2. x:** Le applicazioni gestiscono le notifiche in uno dei tre modi seguenti: finestra nascosta, handle di evento o porta di completamento. Per ulteriori informazioni su questi meccanismi di notifica, vedere la sezione Osservazioni per [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa). Un'applicazione specifica il meccanismo impostando il membro **dwOptions** della struttura [**LINEINITIALIZEEXPARAMS**](/windows/win32/api/tapi/ns-tapi-lineinitializeexparams) prima di chiamare [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa).

La funzione [**lineSetStatusMessages**](/windows/win32/api/tapi/nf-tapi-linesetstatusmessages) consente a un'applicazione di specificare i messaggi di notifica da ricevere per gli eventi correlati alle modifiche dello stato per la riga specificata o per uno qualsiasi dei relativi indirizzi.

**TAPI 3. x:** Le applicazioni gestiscono le notifiche generali mediante oggetti COM standard [collegabili](../com/events-in-com-and-connectable-objects.md). [**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) è l'interfaccia in uscita che deve essere registrata con l'oggetto contenitore di TAPI e [**ITTAPIEventNotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) è il metodo chiamate TAPI per determinare la risposta dell'applicazione. Il metodo [**ITTAPI::p UT \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) indica a TAPI quali eventi sono di interesse per l'applicazione. Se non viene immesso un filtro eventi, l'applicazione non riceverà alcuna notifica degli eventi. Il metodo [**ITTAPI:: RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) indica a TAPI i tipi di supporto e gli indirizzi per i quali l'applicazione gestirà le sessioni in ingresso. Per altre informazioni sulla gestione degli eventi di TAPI 3, vedere Cenni preliminari sugli [eventi](events.md) o l'esempio di codice per gli [eventi di registrazione](register-events.md) .

I provider di servizi di telefonia implementano [**TSPI \_ LineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) e [**TSPI \_ lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages). TAPI chiama queste funzioni per indicare il set di tutti gli eventi di tipo riga, indirizzo e supporto richiesti dalle applicazioni.

 

 
