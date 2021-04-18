---
description: Lo stato della sessione o della chiamata indica lo stato corrente di una sessione, ad esempio &\# 0034; offerta&\# 0034; oppure &\# 0034; connected. &\# 0034; Una gestione corretta delle informazioni sullo stato è essenziale per il corretto funzionamento della maggior parte delle applicazioni TAPI.
ms.assetid: a6a49b77-4e9b-4f23-bfe6-26f26549b18f
title: State
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88fb9c482fcb9e432b5bfb5d36f77cd09f538086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318931"
---
# <a name="state"></a>State

Lo stato della sessione o della chiamata indica lo stato corrente di una sessione, ad esempio "offering" o "Connected". Una gestione corretta delle informazioni sullo stato è essenziale per il corretto funzionamento della maggior parte delle applicazioni TAPI. Ad esempio, l'operazione di risposta può essere eseguita solo su una sessione offerta, ma un trasferimento avrà esito negativo se la sessione si trova in tale stato.

Lo stato di una sessione viene modificato in seguito a eventi. Gli eventi possono essere richiesti o non richiesti. Gli *eventi richiesti* sono causati dall'applicazione che controlla la sessione, ad esempio quando richiama un'operazione di sessione TAPI. Gli *eventi non richiesti* sono causati dal commutatore, dalla rete telefonica, dall'utente che preme i pulsanti sul telefono locale o dalle azioni della parte remota.

Ogni volta che un provider di servizi rileva una modifica dello stato della sessione, segnala la modifica a TAPI e TAPI genera una notifica degli eventi per tutte le applicazioni proprietarie e di monitoraggio. L'applicazione deve rispondere in modo appropriato alle notifiche. Per informazioni sul controllo degli eventi segnalati a un'applicazione, vedere notifica degli eventi nell' [inizializzazione di TAPI](tapi-initialization.md) .

Un'applicazione deve sempre elaborare le notifiche degli eventi di stato. Le transizioni di stato valide per una configurazione fisica potrebbero non essere valide per un altro. Si consideri, ad esempio, una riga che termina fisicamente sia nel computer che in un set telefonico separato, creando una configurazione della linea di entità tra il computer e il set di telefono. È possibile che un'applicazione in esecuzione nel computer non conosca le attività del set di telefono. Ovvero è possibile che la riga sia in uso senza che il provider di servizi ne sia a conoscenza. Un'applicazione che tenta di effettuare una chiamata in uscita riuscirà ad allocare un aspetto di chiamata da TAPI, ma ciò comporta la condivisione della chiamata attiva sulla riga. L'invio cieco di una stringa di connessione DTMF senza prima verificare la presenza di un tono di connessione non può comportare un comportamento intenzionale (o garbato).

Un'applicazione non deve presupporre una progressione rigida da uno stato a un altro. Gli eventi di stato arrivano e vengono inviati in modo asincrono e le notifiche potrebbero non essere ricevute in un ordine prevedibile. Pertanto, le notifiche dello stato di chiamata devono essere visualizzate come indicare all'applicazione il nuovo stato della chiamata anziché come segnalazione delle transizioni tra due Stati.

È necessario che tutti i provider di servizi di telefonia forniscano queste informazioni.

* * TAPI 2. x: * *[**lineGetCallStatus**](/windows/win32/api/tapi/nf-tapi-linegetcallstatus), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**riga \_ CALLSTATE**](./line-callstate.md) Message, [LINECALLSTATE \_ costanti](./linecallstate--constants.md)

**TAPI 3. x: **[**ITCallInfo:: Get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (** membro CIL \_ CALLID** di [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)), notifica [**ITCallStateEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent) , enumeratore [**\_ stato chiamata**](/windows/desktop/api/Tapi3if/ne-tapi3if-call_state)

 

 
