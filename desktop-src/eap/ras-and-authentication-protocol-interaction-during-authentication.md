---
title: Interazione del punto di accesso e del protocollo di autenticazione durante l'autenticazione
description: La funzione RasEapMakeMessage controlla la maggior parte dell'interazione tra il protocollo di autenticazione e il punto di accesso (AP).
ms.assetid: edc128e0-3104-4df9-80f4-b2aebcfe1087
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aea18883225a2a34e592b73e0cdc93b019c1bf466124976f01851febb2a17d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119117771"
---
# <a name="access-point-and-authentication-protocol-interaction-during-authentication"></a>Interazione del punto di accesso e del protocollo di autenticazione durante l'autenticazione

La [**funzione RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) controlla la maggior parte dell'interazione tra il protocollo di autenticazione e il punto di accesso (AP). **RasEapMakeMessage elabora** i pacchetti EAP in ingresso e crea pacchetti EAP per la trasmissione al peer remoto. Elabora anche eventi come timeout e completamento dell'autenticazione.

Se viene ricevuto un messaggio dal peer remoto, il servizio di autenticazione AP chiama [**RasEapMakeMessage,**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85))passando un puntatore al messaggio ricevuto nel *parametro pReceivePacket.*

Se il servizio chiama [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) con *pReceivePacket* impostato su **NULL,** il punto di accesso avvia il dialogo con il protocollo di autenticazione o richiede che il protocollo invii nuovamente l'ultimo pacchetto. Il protocollo di autenticazione deve determinare l'azione eseguita dal servizio in base al relativo stato e dal contesto del messaggio.

Al ritorno da [**RasEapMakeMessage,**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85))il valore del membro **Action** della struttura [**\_ PPP EAP \_ OUTPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) indica l'eventuale azione eseguita dal servizio di autenticazione. Il **membro Action** accetta i valori dal tipo [**\_ enumerato PPP EAP \_ ACTION.**](/windows/desktop/api/Raseapif/ne-raseapif-ppp_eap_action)

Se **Action** è **EAPACTION \_ Send**, **EAPACTION \_ SendAndDone**, **EAPACTION \_ SendWithTimeout** o **EAPACTION \_ SendWithTimeoutInteractive**, il servizio trasmette il pacchetto a cui punta *il parametro pSendPacket* al peer remoto.

Il **valore \_ SendWithTimeout EAPACTION** consente un timeout, dopo il quale il servizio di autenticazione presuppone che il collegamento sia stato perso e disconnette la sessione.

Il **valore \_ SendWithTimeoutInteractive di EAPACTION** consente un timeout infinito. L'autenticatore deve usare questo valore quando prevede l'input dell'utente nel client. Questo timeout consente all'utente di completare l'input richiesto per un periodo di tempo non specificato.

Se **Action** è **EAPACTION \_ SendWithTimeout** o **EAPACTION \_ SendWithTimeoutInteractive,** il protocollo di autenticazione deve impostare il **membro dwIdExpected** della struttura [**\_ PPP EAP \_ OUTPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) sull'identificatore del pacchetto successivo previsto dal peer remoto. Indipendentemente dal fatto che il pacchetto successivo ricevuto dal peer corrisponda a questo valore, il servizio di autenticazione passa il pacchetto al protocollo di autenticazione in una chiamata successiva a [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)). Il protocollo di autenticazione può rimuovere automaticamente il pacchetto semplicemente restituindo **ERROR \_ PPP \_ INVALID \_ PACKET**. Se un pacchetto con l'identificatore previsto non viene ricevuto entro il periodo di timeout configurato, il servizio di autenticazione chiama **ancora RasEapMakeMessage.** In questo caso, la chiamata viene effettuata con il *parametro pReceivePacket* impostato su **NULL,** per indicare che il pacchetto precedente deve essere inviato nuovamente.

Se il **membro Action** è **EAPACTION \_ Done** o **EAPACTION \_ SendAndDone,** il servizio di autenticazione esamina il membro **dwAuthResultCode** di [**PPP \_ EAP \_ OUTPUT.**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) Se **dwAuthResultCode è** NO \_ ERROR, l'autenticazione è riuscita. Se **dwAuthResultCode è** un valore diverso da NO \_ ERROR, l'autenticazione non è riuscita. Il codice di errore restituito per il caso di errore deve derivare da Raserror.h, Mprerror.h o Winerror.h. I codici restituiti possibili includono, tra l'altro, i seguenti:

-   ERRORE \_ NESSUNA \_ AUTORIZZAZIONE \_ DIALIN
-   ERRORE \_ PASSWD \_ SCADUTO
-   ERRORE \_ ACCT \_ DISABLED
-   ORE \_ DI ACCESSO CON RESTRIZIONI PER GLI \_ \_ ERRORI
-   ERRORE \_ AUTH \_ INTERNAL

Nel caso in cui **Action** sia **EAPACTION \_ Done** o **EAPACTION \_ SendAndDone**, il membro **pUserAttributes** deve puntare ad attributi che eseguono l'override degli attributi dello stesso tipo passati al server nella chiamata [**a RasEapBegin.**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85))

Il protocollo di autenticazione nel server può richiedere che il servizio di autenticazione richiama il provider di autenticazione corrente restituisce **EAPACTION \_ Authenticate** nel membro **Action** in [**PPP \_ EAP \_ OUTPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output). In questo caso, il puntatore **pUserAttributes** in **PPP \_ EAP \_ OUTPUT** punta solo agli attributi generati dal protocollo di autenticazione nel server. Non include gli attributi passati al server nella chiamata a [**RasEapBegin.**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)) Il provider di autenticazione non richiede questi attributi iniziali perché le credenziali di autenticazione si trova all'interno del messaggio EAP stesso, non in un attributo RADIUS separato. Quando il servizio di autenticazione risponde all'azione **Authenticate EAPACTION, \_** **pUserAttributes** in [**PPP \_ EAP \_ INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input)punta a tutti gli attributi generati durante l'autenticazione. Questi attributi vengono restituiti al protocollo di autenticazione nel client.

Se il protocollo di autenticazione **utilizza EAPACTION \_ Authenticate**, il provider di autenticazione esegue PAP o MD5-CHAP. Questo metodo di autenticazione può essere usato solo con Windows client.

Se il protocollo di autenticazione autentica l'utente senza basarsi su un provider di autenticazione, non è necessario che il protocollo abbia impostato **Action** su **EAPACTION \_ Authenticate.** Un esempio di questo caso è EAP-Transport Layer Security (TLS).

Il pacchetto di esito positivo EAP è un pacchetto non riconosciuto. Pertanto, può essere perso e non reinviato dal server. Se il servizio di autenticazione sul client riceve un pacchetto NCP (Network Control Protocol), il servizio di autenticazione lato server procede come se l'autenticazione fosse riuscita. Ciò è dovuto al fatto che il server è stato spostato nella fase NCP del PPP. Di conseguenza, il servizio di autenticazione chiama [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) con il membro **fSuccessPacketReceived** della struttura [**\_ PPP EAP \_ INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) impostato su **TRUE.**

Durante la sessione di autenticazione, il protocollo di autenticazione può richiedere l'interazione diretta con l'utente nel client. Il fornitore del protocollo di autenticazione può fornire un'interfaccia utente interattiva a questo scopo. Il protocollo di autenticazione può richiedere al servizio di visualizzare l'interfaccia utente interattiva impostando i membri **fInvokeInteractiveUI**, **pUIContextData** e **dwSizeOfUIContextData** nella struttura [**\_ PPP EAP \_ OUTPUT.**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) Per altre informazioni sull'uso di un'interfaccia utente interattiva, vedere [Interactive Interfaccia utente](interactive-user-interface.md).

Il protocollo di autenticazione deve visualizzare un'interfaccia utente solo tramite il meccanismo descritto in [Interactive Interfaccia utente](interactive-user-interface.md). Se il protocollo di autenticazione stesso visualizza l'interfaccia utente, il thread PPP si blocca fino a quando l'interfaccia utente non viene chiusa.

Se durante il processo di autenticazione [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) restituisce qualsiasi valore diverso da **NO \_ ERROR** o **ERROR \_ PPP INVALID \_ \_ PACKET,** la sessione viene disconnessa e l'errore viene registrato (nel server) o visualizzato all'utente (nel client).

 

 