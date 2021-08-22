---
description: La notifica degli eventi è il mezzo principale con cui un'applicazione ottiene informazioni da TAPI e dai provider di servizi.
ms.assetid: 02160f10-dc3f-484c-9cd3-bcfb07ded822
title: Notifica dell'evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21a83ed721ed22049baeaf3de15626ed8deecf2a7562d883658195eb1eb590f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003669"
---
# <a name="event-notification"></a>Notifica dell'evento

La notifica degli eventi è il mezzo principale con cui un'applicazione ottiene informazioni da TAPI e dai provider di servizi. Queste informazioni possono essere lo stato di un'operazione asincrona avviata dall'applicazione o possono riguardare un processo avviato all'esterno dell'applicazione, ad esempio notifiche di nuove chiamate in ingresso.

**TAPI 2.x:** Le applicazioni gestiscono la notifica in uno dei tre modi seguenti: Finestra nascosta, Handle eventi o Porta di completamento. Per altre informazioni su questi meccanismi di notifica, vedere la sezione Osservazioni per [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa). Un'applicazione specifica il meccanismo impostando il **membro dwOptions** della [**struttura LINEINITIALIZEEXPARAMS**](/windows/win32/api/tapi/ns-tapi-lineinitializeexparams) prima di chiamare [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa).

La [**funzione lineSetStatusMessages**](/windows/win32/api/tapi/nf-tapi-linesetstatusmessages) consente a un'applicazione di specificare i messaggi di notifica da ricevere per gli eventi correlati alle modifiche dello stato per la riga specificata o uno dei relativi indirizzi.

**TAPI 3.x:** Le applicazioni gestiscono la notifica generale usando oggetti collegabili standard [COM.](../com/events-in-com-and-connectable-objects.md) [**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) è l'interfaccia in uscita che deve essere registrata con l'oggetto contenitore TAPI e [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) è il metodo che TAPI chiama per determinare la risposta dell'applicazione. Il [**metodo ITTAPI::p ut \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) indica a TAPI quali eventi sono di interesse per l'applicazione. Se non viene immesso un filtro eventi, l'applicazione non riceverà alcuna notifica di eventi. Il [**metodo ITTAPI::RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) indica a TAPI i tipi di supporti e gli indirizzi per cui l'applicazione gestirà le sessioni in ingresso. Per altre informazioni sulla gestione degli eventi TAPI 3, vedere la [panoramica](events.md) degli eventi o l'esempio di codice [Registra](register-events.md) eventi.

I provider di servizi di [**telefonia \_ implementano lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) [**E TSPI \_ lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages). TAPI chiama queste funzioni per indicare il set di tutti gli eventi di riga, indirizzo e tipo di supporto richiesti dalle applicazioni.

 

 
