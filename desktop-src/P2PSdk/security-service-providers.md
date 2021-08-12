---
description: L'interfaccia SSPI (Security Service Provider Interface) fornisce un'interfaccia universale e standard del settore per applicazioni distribuite sicure.
ms.assetid: c3cebb9d-9094-493f-96d3-763a0c282dfb
title: Provider di servizi di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b53353dc9ed3236ccca5d9a345053870151a7b79e004c5e2ea69e39944209b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118612154"
---
# <a name="security-service-providers"></a>Provider di servizi di sicurezza

L'interfaccia SSPI (Security Service Provider Interface) fornisce un'interfaccia universale e standard del settore per applicazioni distribuite sicure. L'API Peer Graphing consente alle applicazioni di proteggere i collegamenti in un grafo specificando un provider del servizio di sicurezza (SSP), ovvero una DLL che implementa un'interfaccia SSPI. Un'applicazione specifica un provider di servizi di configurazione quando crea un grafo usando [**PeerGraphCreate.**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate)

Per altre informazioni sulla creazione di un provider di servizi di configurazione personalizzato, vedere il collegamento alla documentazione di SSPI nell'elenco [dei collegamenti di riferimento per la creazione di grafici.](graphing-reference-links.md)

## <a name="programming-considerations-for-implementing-an-ssp"></a>Considerazioni sulla programmazione per l'implementazione di un provider di servizi di servizi condivisi

Prestare attenzione quando si effettua una chiamata a un'applicazione dall'interno di un provider di servizi condivisi. Ai callback SSP si applicano le considerazioni seguenti:

-   La restituzione dei callback non deve richiedere molto tempo, perché vengono chiamati durante la negoziazione della connessione. Se il tempo necessario per stabilire una connessione è troppo lungo, è possibile eliminare la connessione.
-   L'API Peer Graphing regola dinamicamente i valori di timeout della connessione, in base al carico effettivo di un sistema. Il valore di timeout più basso è 20 secondi.
-   Per evitare potenziali situazioni di deadlock, un'applicazione non deve accedere al database di grafi peer da un callback. Se un'applicazione richiede informazioni dal database di grafi, l'applicazione può memorizzare nella cache le informazioni necessarie e quindi fare riferimento alla cache dall'interno del callback. Caching consente anche di ridurre il tempo di connessione.

Quando si chiamano i punti di ingresso SSPI, Peer Graphing Infrastructure richiede valori specifici per parametri specifici di cinque (5) funzioni. Non è possibile modificare i valori dei parametri forniti a SSP e il provider di servizi può ignorare i valori per i cinque parametri o gestirli normalmente. L'elenco seguente identifica questi parametri specifici e i valori obbligatori:

-   [**AcquireCredentialsHandle**](graphing-reference-links.md)

    Specificare uno (1) per il *parametro pvGetKeyArgument.* Specifica **NULL per** i *parametri pszPrincipal*, *pvLogonID* e *pGetKeyFn.*

-   [**InitializeSecurityContext**](graphing-reference-links.md)

    Specificare i flag seguenti per il *parametro fContextReq:* **ISC \_ REQ \_ MUTUAL \_ AUTH \| ISC \_ REQ \_ CONFIDENTIALITY \| ISC \_ REQ INTEGRITY \_ \| ISC \_ REQ SEQUENCE DETECT \_ \_ \| ISC \_ REQ STREAM \_ \| ISC \_ REQ ALLOCATE \_ \_ MEMORY**.

-   [**AcceptSecurityContext**](graphing-reference-links.md)

    Specificare i flag seguenti per il *parametro fContextReq:* **ASC \_ REQ \_ MUTUAL \_ AUTH \| ASC \_ REQ \_ CONFIDENTIALITY \| ASC \_ REQ INTEGRITY \_ \| ASC \_ REQ SEQUENCE DETECT \_ \_ \| ASC \_ REQ STREAM \_ \| ASC \_ REQ ALLOCATE \_ \_ MEMORY**.

-   [**EncryptMessage**](graphing-reference-links.md)

    Specificare zero (0) per i *parametri fQOP* *e MessageSeqNo.*

-   [**DecryptMessage**](graphing-reference-links.md)

    Specificare zero (0) per il *parametro MessageSeqNo* e **NULL** per il *parametro pfQOP.*

Quando si [**chiama EncryptMessage,**](graphing-reference-links.md)nella struttura **SecBufferDesc** vengono passati quattro buffer. La tabella seguente identifica l'ordine in cui passare i buffer.

| Struttura specifica di SSP         | Descrizione                                                                                                                                                                                                       |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **INTESTAZIONE DEL FLUSSO SECBUFFER \_ \_**  | Contiene i dati dell'intestazione di sicurezza. Le dimensioni del buffer di intestazione vengono ottenute chiamando [**QueryContextAttributes**](graphing-reference-links.md) e specificando l'attributo **SECPKG \_ ATTR \_ STREAM \_ SIZES.**  |
| **SECBUFFER \_ DATA**            | Contiene il messaggio di testo normale da crittografare.                                                                                                                                                                  |
| **TRAILER DEL FLUSSO SECBUFFER \_ \_** | Contiene i dati del trailer di sicurezza. Le dimensioni del buffer di intestazione vengono ottenute chiamando [**QueryContextAttributes**](graphing-reference-links.md) e specificando l'attributo **SECPKG \_ ATTR \_ STREAM \_ SIZES.** |
| **SECBUFFER \_ EMPTY**           | Non inizializzato. La dimensione di questo buffer è zero (0).                                                                                                                                                             |



 

Quando si [**chiama DecryptMessage,**](graphing-reference-links.md)l'API Peer Graphing passa esattamente **quattro strutture SecBuffer.** Il primo buffer è **SECBUFFER \_ DATA** e contiene un messaggio crittografato. I buffer rimanenti vengono usati per l'output e sono di tipo **SECBUFFER \_ EMPTY.**

Il provider di servizi di configurazione deve supportare la crittografia e la decrittografia dei buffer dei dati utente con dimensioni di 16 KB o superiori in una chiamata.

 

 



