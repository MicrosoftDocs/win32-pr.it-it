---
title: Informazioni sull'autenticazione reciproca tramite Kerberos
description: Nell'autenticazione reciproca, il client e il servizio devono verificare tra loro le rispettive identità prima di eseguire le funzioni dell'applicazione.
ms.assetid: 5ce923d6-bede-4acb-b297-e93f2f506ea9
ms.tgt_platform: multiple
keywords:
- Informazioni sull'autenticazione reciproca con Kerberos AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b020b2d808cee96319cf411b4199bb4ff78f357cfdf8379f01c7d07bc1c5c1c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841011"
---
# <a name="about-mutual-authentication-using-kerberos"></a>Informazioni sull'autenticazione reciproca tramite Kerberos

Nell'autenticazione reciproca, il client e il servizio devono verificare tra loro le rispettive identità prima di eseguire le funzioni dell'applicazione. Nessuna delle due parti può eseguire operazioni con l'altra finché non viene verificata l'identità. in altri modo, il servizio deve essere in grado di verificare il client senza eseguire query sul client e il client deve essere in grado di verificare il servizio senza eseguire query sul servizio.

Il valore di un servizio in grado di autenticare un client è noto. Ad esempio, un servizio file rappresenta un client per determinare a quali file il client può accedere.

Il valore di un client in grado di autenticare un servizio è meno comprensibile. L'autenticazione di un servizio consente al client di considerare attendibili i dati che ottiene dal servizio e di essere sicuro nell'invio di dati sensibili al servizio. La possibilità di un client di autenticare un servizio è particolarmente importante nelle applicazioni client/servizio che supportano la delega del contesto di sicurezza del client; in altre informazioni, il client autorizza il servizio a fungere da delegato per l'accesso a servizi aggiuntivi o risorse di rete.

Un servizio autentica un client come segue: il client stabilisce un contesto di sicurezza locale eseguendo in un contesto stabilito in precedenza, ad esempio nella sessione di un utente connesso o presentando in modo esplicito le credenziali al provider di sicurezza sottostante. Il servizio non può accettare connessioni da client non autenticati.

Il meccanismo Kerberos con cui un client autentica un servizio funziona come segue: quando viene installato un servizio, un programma di installazione del servizio, in esecuzione con privilegi di amministratore, registra uno o più nomi SPN univoci per ogni istanza del servizio. I nomi vengono registrati nel controller Dominio di Active Directory (DC) nell'oggetto account utente o computer che verrà utilizzato dall'istanza del servizio per accedere. Quando un client richiede una connessione a un servizio, crea un nome SPN per un'istanza del servizio, usando dati noti o dati forniti dall'utente. Il client usa quindi il pacchetto di negoziazione SSPI per presentare il nome SPN al Centro distribuzione chiavi (KDC) per l'account di dominio client. Il KDC cerca nella foresta un account utente o computer in cui tale nome SPN è registrato. Se il nome SPN è registrato in più account, l'autenticazione non riesce. In caso contrario, il KDC crittografa un messaggio usando la password dell'account in cui è stato registrato il nome SPN. Il KDC passa questo messaggio crittografato al client, che a sua volta lo passa all'istanza del servizio. Il servizio usa il pacchetto di negoziazione SSPI per decrittografare il messaggio, che passa nuovamente al client e al KDC del client. Il KDC autentica il servizio se il messaggio decrittografato corrisponde al messaggio originale.

-   Per altre informazioni sulla composizione e la registrazione di nomi SPN, vedere . [Nomi delle entità servizio](service-principal-names.md)
-   Per altre informazioni e un esempio di codice che compone un nome SPN per un servizio Windows Sockets che si pubblica con un punto di connessione del servizio, vedere Composizione dei nomi SPN per un servizio con [un SCP.](composing-the-spns-for-a-service-with-an-scp.md)
-   Per altre informazioni e un esempio di codice che compone un nome SPN per un servizio RPC, vedere Composizione di nomi [SPN per un servizio RpcNs](composing-spns-for-an-rpcns-service.md).

 

 




