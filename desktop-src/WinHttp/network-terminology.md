---
description: Quando si sviluppa un'applicazione che usa i servizi HTTP di Microsoft Windows (WinHTTP), è importante comprendere i concetti e la terminologia seguenti relativi alla rete in generale e al protocollo HTTP in particolare.
ms.assetid: 6ea0c16f-1233-4580-97bb-14e224646857
title: Terminologia di rete (WinHTTP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bec92d5dd99247fab3ade48760db343983cd7092ea96ac8bd059ed892c9aa42a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643801"
---
# <a name="network-terminology-winhttp"></a>Terminologia di rete (WinHTTP)

Quando si sviluppa un'applicazione che usa i servizi HTTP di Microsoft Windows (WinHTTP), è importante comprendere i concetti e la terminologia seguenti relativi alla rete in generale e al protocollo HTTP in particolare.

-   [Transazioni HTTP](#http-transactions)
-   [Server proxy](#proxy-servers)
-   [Modalità sincrone e asincrone](#synchronous-and-asynchronous-modes)
-   [autenticazione](#authentication)

## <a name="http-transactions"></a>Transazioni HTTP

Quando si lavora con le transazioni HTTP, si scambiano informazioni con un altro computer in un'altra posizione in una rete. Le informazioni scambiate possono essere un file contenente testo o elementi multimediali oppure i risultati di una query di database. Un'informazione scambiata in rete è denominata *risorsa*. In genere il computer che invia una risorsa è il server e il computer che riceve tale risorsa è un client. Tuttavia, è anche possibile che un client inviare dati a un server. A volte una transazione HTTP implica un server di livello intermedio. Un server di livello intermedio raccoglie diverse risorse da altri server, compila le informazioni in un'unica risorsa e invia tale risorsa al client.

Il processo di ottenimento di una risorsa tramite il protocollo HTTP richiede lo scambio di una serie di messaggi tra il client e il server. Il client avvia la transazione inviando un messaggio che richiede una risorsa. Questo messaggio viene chiamato richiesta HTTP o talvolta solo richiesta. Una richiesta HTTP è costituita dai componenti seguenti.

-   Metodo, Uniform Resource Identifier (URI), numero di versione del protocollo
-   Intestazioni
-   Corpo dell'entità

Quando un server riceve una richiesta, risponde inviando un messaggio al client. Il messaggio inviato dal server viene chiamato risposta HTTP. Una risposta HTTP è costituita dai componenti seguenti.

-   Numero di versione del protocollo, codice di stato, testo dello stato
-   Intestazioni
-   Corpo dell'entità

La risposta indica che la richiesta non può essere elaborata o fornisce le informazioni richieste. A seconda del tipo di richiesta, può trattarsi di informazioni su una risorsa, ad esempio le dimensioni e il tipo, oppure può essere una parte o tutta la risorsa stessa. La parte di una risposta che include una parte o tutta la risorsa richiesta è denominata "dati di risposta" o "corpo dell'entità" e la risposta non è completa fino a quando non vengono ricevuti tutti i dati di risposta.

Per informazioni dettagliate sulle transazioni HTTP e sul protocollo HTTP, vedere [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt), Hypertext Transfer Protocol — HTTP/1.1.

## <a name="proxy-servers"></a>Server proxy

Anche se una richiesta inviata da un client viene infine ricevuta dal server di destinazione, talvolta la transazione passa prima attraverso un server proxy. Un proxy intercetta la richiesta e può anche modificare la richiesta prima di inviarla al server. Quando il server risponde, la risposta passa anche attraverso il proxy prima che venga inoltrata al client. Il proxy può modificare le intestazioni in questa risposta.

Intercettando e traducendo transazioni di rete, un proxy può:

-   Proteggere il client monitorando le transazioni potenzialmente pericolose.
-   Abilitare il client per comunicare usando protocolli che potrebbero non essere implementati dal software client.
-   Funge da gateway tra una rete privata e una rete pubblica.

L'API WinHTTP include uno strumento di configurazione del proxy che consente di fornire a WinHTTP informazioni relative ai server proxy che intercettano le transazioni HTTP. Per informazioni sull'uso dello strumento di configurazione proxy, [ vedereProxyCfg.exe, a Proxy Configuration Tool](proxycfg-exe--a-proxy-configuration-tool.md).

## <a name="synchronous-and-asynchronous-modes"></a>Modalità sincrone e asincrone

Esistono due modelli di programmazione per ottenere risorse in rete usando WinHTTP, ovvero i modelli sincroni e asincroni. In un modello sincrono, una chiamata a una funzione o a un metodo non viene completata fino al completamento dell'operazione richiesta o fino a quando non si verifica un errore. Ad esempio, quando l'applicazione richiede una risorsa usando WinHTTP in modo sincrono, non continua con il passaggio successivo fino a quando non vengono ricevuti i dati richiesti.

Un modello asincrono, d'altra parte, consente a un'applicazione di eseguire altre attività durante l'attesa del recupero della risorsa. Se viene chiamata un'altra funzione o metodo WinHTTP e un'operazione precedente non è stata completata, la funzione restituisce un errore. Quando si usa WinHTTP in modo asincrono, Component Object Model eventi e callback (COM) sono disponibili per notificare a un'applicazione lo stato di avanzamento di un'operazione HTTP.

## <a name="authentication"></a>Autenticazione

L'autenticazione è il processo tramite il quale un proxy HTTP o un server HTTP convalida le informazioni di accesso di un utente prima di consentire l'accesso alle risorse. In Internet vengono usati vari schemi di autenticazione. In genere il nome e la password di un utente vengono confrontati con un elenco autorizzato e se il sistema rileva una corrispondenza, l'accesso viene concesso nell'extent specificato nell'elenco di autorizzazioni per l'utente.

Le funzioni WinHTTP supportano sia l'autenticazione server che l'autenticazione proxy per le sessioni HTTP. WinHTTP supporta gli schemi di autenticazione seguenti: Basic, Digest (vedere [RFC 2617),](https://www.ietf.org/rfc/rfc2617.txt) [Autenticazione NTLM,](../com/ntlmssp.md)Negotiate/Kerberos e Microsoft Passport 1.4. [](../com/kerberos-v5-protocol.md) Per informazioni dettagliate sull'autenticazione, nonché un esempio di uso dell'autenticazione in un'applicazione Microsoft Visual C++, vedere [Autenticazione in WinHTTP](authentication-in-winhttp.md).

Per informazioni sulle considerazioni sulla sicurezza relative all'autenticazione Di base e Passport, vedere [Considerazioni sulla sicurezza di WinHTTP](winhttp-security-considerations.md).

 

 
