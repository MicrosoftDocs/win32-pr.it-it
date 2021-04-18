---
description: Security Service Provider Interface (SSPI) fornisce un'interfaccia universale standard del settore per le applicazioni distribuite sicure.
ms.assetid: c3cebb9d-9094-493f-96d3-763a0c282dfb
title: Provider di servizi di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2121940337d0f4e06c53981cf30f0125180c466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315438"
---
# <a name="security-service-providers"></a>Provider di servizi di sicurezza

Security Service Provider Interface (SSPI) fornisce un'interfaccia universale standard del settore per le applicazioni distribuite sicure. L'API per la rappresentazione grafica dei peer consente alle applicazioni di proteggere i collegamenti in un grafico specificando un provider di servizi di sicurezza (SSP), ovvero una DLL che implementa un'interfaccia SSPI. Un'applicazione specifica un SSP quando crea un grafo usando [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate).

Per ulteriori informazioni sulla creazione di un SSP personalizzato, vedere il collegamento alla documentazione SSPI nell'elenco dei [collegamenti di riferimento](graphing-reference-links.md)per la creazione di grafici.

## <a name="programming-considerations-for-implementing-an-ssp"></a>Considerazioni sulla programmazione per l'implementazione di un provider di servizi condivisi

Prestare attenzione quando si chiama un'applicazione dall'interno di un SSP. Per le richiamate SSP, si applicano le considerazioni seguenti:

-   I callback non devono richiedere molto tempo per la restituzione, perché vengono chiamati durante la negoziazione della connessione. Se la connessione deve essere stabilita troppo a lungo, la connessione può essere eliminata.
-   L'API per la rappresentazione grafica dei peer regola dinamicamente i valori di timeout della connessione in base al carico effettivo di un sistema. Il valore di timeout più basso è di 20 secondi.
-   Per evitare potenziali situazioni di deadlock, un'applicazione non deve accedere al database peer Graphing da un callback. Se un'applicazione richiede informazioni dal database di Graphing, l'applicazione può memorizzare nella cache le informazioni necessarie e quindi fare riferimento alla cache dall'interno del callback. La memorizzazione nella cache consente inoltre di ridurre il tempo di connessione.

Quando si chiamano i punti di ingresso SSPI, l'infrastruttura di Peer Graphing richiede valori specifici per parametri specifici di cinque (5) funzioni. Non è possibile modificare questi valori di parametro forniti a SSP e il provider di servizi condivisi può ignorare i valori dei cinque parametri o gestirli normalmente. L'elenco seguente identifica questi parametri specifici e i valori obbligatori:

-   [**AcquireCredentialsHandle**](graphing-reference-links.md)

    Specificare uno (1) per il parametro *pvGetKeyArgument* . Specifica **null** per i parametri *pszPrincipal*, *pvLogonID* e *pGetKeyFn* .

-   [**InitializeSecurityContext**](graphing-reference-links.md)

    Specificare i flag seguenti per il parametro *fContextReq* : **ISC \_ req \_ reciproal \_ auth \| ISC \_ req \_ confidentiality \| ISC req \_ \_ Integrity \| ISC \_ req \_ \_ \| \_ \_ \| \_ \_ \_**.

-   [**AcceptSecurityContext**](graphing-reference-links.md)

    Specificare i flag seguenti per il parametro *fContextReq* : **ASC \_ req \_ Mutual \_ auth \| ASC \_ req \_ confidentiality \| ASC \_ req \_ Integrity \| ASC \_ req \_ Sequence \_ Detect \| ASC \_ req \_ Stream \| ASC \_ req \_ allocate \_ Memory**.

-   [**EncryptMessage**](graphing-reference-links.md)

    Specificare zero (0) per i parametri *fQOP* e *MessageSeqNo* .

-   [**DecryptMessage**](graphing-reference-links.md)

    Specificare zero (0) per il parametro *MessageSeqNo* e **null** per il parametro *pfQOP* .

Quando si chiama [**EncryptMessage**](graphing-reference-links.md), vengono passati quattro buffer nella struttura **SecBufferDesc** . Nella tabella seguente viene identificato l'ordine di passaggio dei buffer.

| Struttura specifica di SSP         | Descrizione                                                                                                                                                                                                       |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_intestazione del flusso SECBUFFER \_**  | Contiene i dati dell'intestazione di sicurezza. La dimensione del buffer di intestazione viene ottenuta chiamando [**QueryContextAttributes**](graphing-reference-links.md) e specificando l'attributo **SECPKG \_ attr \_ Stream \_ sizes** .  |
| **\_dati SECBUFFER**            | Contiene il messaggio di testo normale da crittografare.                                                                                                                                                                  |
| **\_trailer del flusso SECBUFFER \_** | Contiene i dati del trailer di sicurezza. La dimensione del buffer di intestazione viene ottenuta chiamando [**QueryContextAttributes**](graphing-reference-links.md) e specificando l'attributo **SECPKG \_ attr \_ Stream \_ sizes** . |
| **SECBUFFER \_ vuoto**           | Non inizializzato. La dimensione di questo buffer è zero (0).                                                                                                                                                             |



 

Quando si chiama [**DecryptMessage**](graphing-reference-links.md), l'API per la rappresentazione di peering passa esattamente quattro strutture **SecBuffer** . Il primo buffer è **SECBUFFER i \_ dati** e contiene un messaggio crittografato. I buffer rimanenti vengono usati per l'output e sono di tipo **SECBUFFER \_ vuoto**.

Il provider di servizi condivisi deve supportare la crittografia e la decrittografia dei buffer di dati utente con dimensioni di 16K e superiori in un'unica chiamata.

 

 



