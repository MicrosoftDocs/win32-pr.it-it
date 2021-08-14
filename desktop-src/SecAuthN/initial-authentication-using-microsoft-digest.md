---
description: L'autenticazione iniziale avviene quando il server riceve una risposta di richiesta di verifica da un client.
ms.assetid: 8a5cf26b-0b2a-4f19-807b-9ec4d533cdd4
title: Autenticazione iniziale tramite Microsoft Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b6e9582161eb43e5109af4dc223ae150e94cbddf9b3514dabcb30339a3acc36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482621"
---
# <a name="initial-authentication-using-microsoft-digest"></a>Autenticazione iniziale tramite Microsoft Digest

L'autenticazione iniziale avviene quando il server riceve una risposta di richiesta di verifica da un client. L'autenticazione di una risposta alla richiesta di verifica comporta in genere almeno due server:

-   Il server di origine: riceve la richiesta dal client e riceve una richiesta di verifica e quindi riceve la risposta di richiesta dal client che deve essere autenticata.
-   Il server di autenticazione riceve le informazioni di autorizzazione dal server di origine ed esegue l'autenticazione. Questo server è in genere un controller di dominio che supporta più server di origine.

Quando il server di origine riceve una richiesta con un'intestazione authorization contenente una risposta di richiesta digest, l'autenticazione procede come segue:

-   L'identità del server di origine viene verificata rispetto al server codificato nel parametro nonce della richiesta di verifica.
-   Viene controllato il timestamp codificato nel nonce. Se il parametro nonce è scaduto e le informazioni su nome utente/password sono valide, il server di origine termina l'autenticazione emettendo una nuova richiesta digest con la direttiva non aggiornate impostata su "true". Ciò indica che solo il nonce è "obsoleto" e il client può rispondere alla nuova richiesta usando la password usata nella risposta precedente. Se il client riceve una nuova richiesta di verifica dopo l'invio della risposta alla richiesta di verifica non valida, il client deve generare una nuova risposta alla richiesta.
-   Se viene applicato il rilevamento della riproduzione, la direttiva nc (conteggio nonce) viene verificata rispetto al database della sessione nonce gestito dal server.
-   Il server di autenticazione viene identificato e inviato alle informazioni di autorizzazione del client.
-   Il server di autenticazione controlla l'identità del server codificato nel parametro nonce rispetto all'identità del server di origine.
-   Il server di autenticazione, che è un controller di dominio, recupera la password dell'utente.
-   Usando le informazioni di autorizzazione, la password e l'identificazione del server di origine, il server di autenticazione calcola il valore che il client deve avere fornito nella direttiva di risposta della richiesta di verifica. Il server di autenticazione confronta il valore calcolato con la risposta del client per determinare l'esito positivo o negativo dell'autenticazione.

Se l'autenticazione ha esito [](../secgloss/s-gly.md) positivo, il contesto di sicurezza dell'utente e una chiave di [*sessione*](../secgloss/s-gly.md) digest vengono restituiti al server di origine. Se l'autenticazione non riesce, il server di origine deve generare una risposta di errore. Dopo un'autenticazione riuscita, il server di origine restituisce la risorsa richiesta al client.

La chiave di sessione digest restituita dal server di autenticazione viene memorizzata nella cache dal server di origine per l'autenticazione delle richieste future. Per altre informazioni, vedere [Autenticazione delle richieste successive tramite Microsoft Digest](authenticating-subsequent-requests-using-microsoft-digest.md).

 

 
