---
description: L'autenticazione iniziale si verifica quando il server riceve una risposta di verifica da un client.
ms.assetid: 8a5cf26b-0b2a-4f19-807b-9ec4d533cdd4
title: Autenticazione iniziale tramite Microsoft Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ed4960d947bbc60df962e6a9b71be755e158c8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884505"
---
# <a name="initial-authentication-using-microsoft-digest"></a>Autenticazione iniziale tramite Microsoft Digest

L'autenticazione iniziale si verifica quando il server riceve una risposta di verifica da un client. L'autenticazione di una risposta di richiesta in genere comporta un minimo di due server:

-   Il server di origine: riceve la richiesta dal client e genera una richiesta di verifica e quindi riceve la risposta di verifica da parte del client che deve essere autenticata.
-   Il server di autenticazione, riceve le informazioni di autorizzazione dal server di origine ed esegue l'autenticazione. Questo server è in genere un controller di dominio che supporta più server di origine.

Quando il server di origine riceve una richiesta con un'intestazione di autorizzazione contenente una risposta di verifica del digest, l'autenticazione procede come segue:

-   L'identità del server di origine viene verificata rispetto al server codificato nel parametro nonce della richiesta di verifica.
-   Il timestamp codificato nel parametro nonce viene controllato. Se il parametro nonce è scaduto e le informazioni sul nome utente e sulla password sono valide, il server di origine termina l'autenticazione emettendo una nuova richiesta digest con la direttiva obsoleta impostata su "true". Ciò indica che solo il parametro nonce è "obsoleto" e che il client può rispondere alla nuova richiesta utilizzando la password utilizzata nella risposta precedente. Se il client riceve una nuova richiesta dopo l'invio della risposta alla richiesta di verifica non aggiornata, il client deve generare una nuova risposta alla richiesta di verifica.
-   Se il rilevamento della riproduzione viene applicato, la direttiva NC (conteggio nonce) viene verificata rispetto al database della sessione nonce gestito dal server.
-   Il server di autenticazione viene identificato e invia le informazioni di autorizzazione del client.
-   Il server di autenticazione controlla l'identità del server codificato nel parametro nonce rispetto all'identità del server di origine.
-   Il server di autenticazione, che è un controller di dominio, recupera la password dell'utente.
-   Utilizzando le informazioni di autorizzazione, la password e l'identificazione del server di origine, il server di autenticazione calcola il valore che il client deve fornire nella direttiva di risposta della risposta alla richiesta di verifica. Il server di autenticazione confronta il valore calcolato con la risposta del client per determinare l'esito positivo o negativo dell'autenticazione.

Se l'autenticazione ha esito positivo, il [*contesto di sicurezza*](../secgloss/s-gly.md) dell'utente e una chiave della [*sessione*](../secgloss/s-gly.md) digest vengono restituiti al server di origine. Se l'autenticazione ha esito negativo, il server di origine deve generare una risposta di errore. Una volta completata l'autenticazione, il server di origine restituisce la risorsa richiesta al client.

La chiave della sessione digest restituita dal server di autenticazione viene memorizzata nella cache dal server di origine per l'utilizzo nell'autenticazione delle richieste future. Per altre informazioni, vedere [autenticazione delle richieste successive con Microsoft Digest](authenticating-subsequent-requests-using-microsoft-digest.md).

 

 
