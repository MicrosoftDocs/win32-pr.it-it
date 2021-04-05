---
title: Interazione del punto di accesso e del protocollo di autenticazione durante l'autenticazione
description: La funzione RasEapMakeMessage controlla la maggior parte dell'interazione tra il protocollo di autenticazione e il punto di accesso (AP).
ms.assetid: edc128e0-3104-4df9-80f4-b2aebcfe1087
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e486e3a10e323f28bc2f6fef4c131acfc095b48
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046584"
---
# <a name="access-point-and-authentication-protocol-interaction-during-authentication"></a>Interazione del punto di accesso e del protocollo di autenticazione durante l'autenticazione

La funzione [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) controlla la maggior parte dell'interazione tra il protocollo di autenticazione e il punto di accesso (AP). **RasEapMakeMessage** elabora i pacchetti EAP in ingresso e crea pacchetti EAP per la trasmissione al peer remoto. Elabora anche eventi quali i timeout e il completamento dell'autenticazione.

Se viene ricevuto un messaggio dal peer remoto, il servizio di autenticazione AP chiama [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)), passando un puntatore al messaggio ricevuto nel parametro *pReceivePacket* .

Se il servizio chiama [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) con *PReceivePacket* impostato su **null**, l'AP avvia la finestra di dialogo con il protocollo di autenticazione oppure richiede che il protocollo invii di nuovo l'ultimo pacchetto. Il protocollo di autenticazione deve determinare quale azione sta prendendo il servizio in base al relativo stato e al contesto del messaggio.

Al ritorno da [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)), il valore del membro dell' **azione** della struttura [**di \_ \_ output EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) indica quale azione viene eseguita dal servizio di autenticazione. Il membro dell' **azione** accetta valori dal tipo enumerato dell' [**\_ \_ azione EAP PPP**](/windows/desktop/api/Raseapif/ne-raseapif-ppp_eap_action) .

Se **Action** è **EAPACTION \_ Send**, **EAPACTION \_ SendAndDone**, **EAPACTION \_ SendWithTimeout** o **EAPACTION SendWithTimeoutInteractive \_**, il servizio trasmette il pacchetto a cui punta il parametro *pSendPacket* al peer remoto.

Il **valore \_ SendWithTimeout di EAPACTION** consente un timeout, dopo il quale il servizio di autenticazione presuppone che il collegamento sia stato perso e disconnette la sessione.

Il **valore \_ SendWithTimeoutInteractive di EAPACTION** consente di eseguire una quantità infinita di timeout. L'autenticatore deve usare questo valore quando prevede l'input dell'utente nel client. Questo timeout consente all'utente un periodo di tempo non specificato per completare l'input richiesto.

Se **Action** è **EAPACTION \_ SendWithTimeout** o **EAPACTION \_ SendWithTimeoutInteractive**, il protocollo di autenticazione deve impostare il membro **dwIdExpected** della struttura di [**\_ \_ output EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) sull'identificatore del pacchetto successivo previsto dal peer remoto. Indipendentemente dal fatto che il pacchetto successivo ricevuto dal peer corrisponda a questo valore, il servizio di autenticazione passa il pacchetto al protocollo di autenticazione in una chiamata successiva a [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)). Il protocollo di autenticazione può rimuovere automaticamente il pacchetto semplicemente restituendo **l' \_ errore \_ PPP \_ non valido**. Se un pacchetto con l'identificatore previsto non viene ricevuto entro il periodo di timeout configurato, il servizio di autenticazione chiama ancora **RasEapMakeMessage**. In questo caso, la chiamata viene eseguita con il parametro *pReceivePacket* impostato su **null**, per indicare che è necessario inviare nuovamente il pacchetto precedente.

Se il membro dell' **azione** è **EAPACTION \_ done** o **EAPACTION \_ SendAndDone**, il servizio di autenticazione esamina  il membro dwAuthResultCode [**dell' \_ \_ output EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output). Se **dwAuthResultCode** non è un \_ errore, l'autenticazione ha avuto esito positivo. Se **dwAuthResultCode** è un valore diverso da nessun \_ errore, l'autenticazione non è riuscita. Il codice di errore restituito per il caso di errore deve provenire da Raserror. h, Mprerror. h o Winerror. h. I codici restituiti possibili includono, ma non sono limitati a, quanto segue:

-   ERRORE \_ Nessuna \_ autorizzazione dialin \_
-   ERRORE \_ passwd \_ scaduto
-   ERRORE \_ Acct \_ disabilitato
-   \_ore di \_ accesso con restrizioni errori \_
-   ERRORE \_ \_ interno auth

Nel caso in cui **Action** sia **EAPACTION \_ done** o **EAPACTION \_ SendAndDone**, il membro **pUserAttributes** deve puntare agli attributi che eseguono l'override degli attributi dello stesso tipo passati al server nella chiamata a [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)).

Il protocollo di autenticazione nel server può richiedere che il servizio di autenticazione richiami il provider di autenticazione corrente restituendo **EAPACTION \_ Authenticate** nel membro dell' **azione** nell' [**\_ \_ output EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output). In questo caso, il puntatore **pUserAttributes** nell' **\_ \_ output EAP PPP** punta solo agli attributi generati dal protocollo di autenticazione nel server. Non include alcuno degli attributi passati al server nella chiamata a [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)). Il provider di autenticazione non richiede questi attributi iniziali perché le credenziali di autenticazione si trovano all'interno del messaggio EAP stesso, non in un attributo RADIUS separato. Quando il servizio di autenticazione risponde all'azione di autenticazione **EAPACTION \_** , **PUserAttributes** nell' [**\_ \_ input EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input), punta a tutti gli attributi generati durante l'autenticazione. Questi attributi vengono restituiti al protocollo di autenticazione nel client.

Se il protocollo di autenticazione usa **EAPACTION \_ Authenticate**, il provider di autenticazione esegue PAP o MD5-CHAP. Questo metodo di autenticazione può essere utilizzato solo con i client Windows.

Se il protocollo di autenticazione autentica l'utente senza basarsi su un provider di autenticazione, non è necessario che il protocollo imposti mai l' **azione** su **EAPACTION \_ Authenticate**. Un esempio di questo caso è EAP-Transport Layer Security (TLS).

Il pacchetto EAP Success è un pacchetto non riconosciuto. Pertanto, può essere persa e non rinviata dal server. Se il servizio di autenticazione nel client riceve un pacchetto NCP (Network Control Protocol), il servizio di autenticazione sul lato server procede come se l'autenticazione avesse avuto esito positivo. Questo è dovuto al fatto che il server è stato spostato nella fase NCP di PPP. Di conseguenza, il servizio di autenticazione chiama [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) con il membro **fSuccessPacketReceived** della struttura di [**\_ \_ input EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) impostato su **true**.

Nel corso della sessione di autenticazione, il protocollo di autenticazione può richiedere l'interazione diretta con l'utente nel client. Il fornitore del protocollo di autenticazione può fornire un'interfaccia utente interattiva a questo scopo. Il protocollo di autenticazione può richiedere che il servizio visualizzi l'interfaccia utente interattiva impostando i membri **fInvokeInteractiveUI**, **pUIContextData** e **dwSizeOfUIContextData** nella struttura di [**\_ \_ output EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) . Per ulteriori informazioni sull'utilizzo di un'interfaccia utente interattiva, vedere [interfaccia utente interattiva](interactive-user-interface.md).

Il protocollo di autenticazione dovrebbe visualizzare un'interfaccia utente solo tramite il meccanismo descritto in [interfaccia utente interattiva](interactive-user-interface.md). Se il protocollo di autenticazione Visualizza l'interfaccia utente, il thread PPP si blocca fino a quando l'interfaccia utente non viene rilasciata.

Se durante il processo di autenticazione, [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) restituisce un valore diverso da un **\_ \_ \_ pacchetto non valido** per il PPP **\_ errore** o errore, la sessione viene disconnessa e l'errore viene registrato (sul server) o visualizzato all'utente (sul client).

 

 