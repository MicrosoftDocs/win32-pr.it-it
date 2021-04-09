---
title: Informazioni sull'autenticazione reciproca tramite Kerberos
description: Nell'autenticazione reciproca, il client e il servizio devono verificare le rispettive identità tra loro prima di eseguire le funzioni dell'applicazione.
ms.assetid: 5ce923d6-bede-4acb-b297-e93f2f506ea9
ms.tgt_platform: multiple
keywords:
- Informazioni sull'autenticazione reciproca tramite AD Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9685dad0bd20f233b8dcb0ecf12af338f318646f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044019"
---
# <a name="about-mutual-authentication-using-kerberos"></a>Informazioni sull'autenticazione reciproca tramite Kerberos

Nell'autenticazione reciproca, il client e il servizio devono verificare le rispettive identità tra loro prima di eseguire le funzioni dell'applicazione. Nessuna delle parti può eseguire operazioni con l'altra fino a quando non è stata verificata l'identità. ovvero, il servizio deve essere in grado di verificare il client senza eseguire query sul client e il client deve essere in grado di verificare il servizio senza eseguire query sul servizio.

Il valore di un servizio in grado di autenticare un client è noto. Ad esempio, un servizio file rappresenta un client per determinare a quali file può accedere il client.

Il valore di un client in grado di autenticare un servizio è meno noto. L'autenticazione di un servizio consente al client di considerare attendibili i dati ottenuti dal servizio e di essere protetti per l'invio di dati sensibili al servizio. La capacità di un client di autenticare un servizio è particolarmente importante nelle applicazioni client/di servizio che supportano la delega del contesto di sicurezza del client. ovvero il client autorizza il servizio a fungere da delegato per accedere a servizi aggiuntivi o a risorse di rete.

Un servizio autentica un client come segue: il client stabilisce un contesto di sicurezza locale eseguendo in un contesto precedentemente stabilito, ad esempio, nella sessione di un utente connesso o presentando in modo esplicito le credenziali al provider di sicurezza sottostante. Il servizio non è in grado di accettare connessioni da un client non autenticato.

Il meccanismo Kerberos mediante il quale un client autentica un servizio funziona nel modo seguente: quando viene installato un servizio, un programma di installazione del servizio, in esecuzione con privilegi di amministratore, registra uno o più nomi SPN univoci per ogni istanza del servizio. I nomi vengono registrati nel controller di Dominio di Active Directory (DC) nell'oggetto account utente o computer che verrà utilizzato dall'istanza del servizio per l'accesso. Quando un client richiede una connessione a un servizio, compone un nome SPN per un'istanza del servizio usando dati noti o dati forniti dall'utente. Il client utilizza quindi il pacchetto di negoziazione SSPI per presentare il nome SPN al Centro distribuzione chiavi (KDC) per l'account di dominio del client. Il KDC Cerca nell'insieme di strutture un account utente o computer in cui è registrato il nome SPN. Se il nome SPN è registrato in più di un account, l'autenticazione ha esito negativo. In caso contrario, il KDC crittografa un messaggio utilizzando la password dell'account in cui è stato registrato il nome SPN. Il KDC passa questo messaggio crittografato al client, che a sua volta lo passa all'istanza del servizio. Il servizio utilizza il pacchetto di negoziazione SSPI per decrittografare il messaggio, che passa di nuovo al client e al KDC del client. Il KDC autentica il servizio se il messaggio decrittografato corrisponde al messaggio originale.

-   Per ulteriori informazioni sulla composizione e la registrazione di SPN, vedere. [Nomi dell'entità servizio](service-principal-names.md)
-   Per ulteriori informazioni e un esempio di codice che compone un nome SPN per un servizio Windows Sockets che viene pubblicato con un punto di connessione del servizio, vedere [composizione dei nomi SPN per un servizio con SCP](composing-the-spns-for-a-service-with-an-scp.md).
-   Per ulteriori informazioni e un esempio di codice che compone un nome SPN per un servizio RPC, vedere [composizione di nomi SPN per un servizio RpcNs](composing-spns-for-an-rpcns-service.md).

 

 




