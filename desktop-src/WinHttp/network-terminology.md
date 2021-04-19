---
description: Quando si sviluppa un'applicazione che utilizza i servizi HTTP di Microsoft Windows (WinHTTP), è importante comprendere i concetti e la terminologia seguenti relativi alla rete in generale e al protocollo HTTP in particolare.
ms.assetid: 6ea0c16f-1233-4580-97bb-14e224646857
title: Terminologia di rete (WinHTTP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8173b921957a95ebde7f00034c31b2f016b78ab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314107"
---
# <a name="network-terminology-winhttp"></a>Terminologia di rete (WinHTTP)

Quando si sviluppa un'applicazione che utilizza i servizi HTTP di Microsoft Windows (WinHTTP), è importante comprendere i concetti e la terminologia seguenti relativi alla rete in generale e al protocollo HTTP in particolare.

-   [Transazioni HTTP](#http-transactions)
-   [Server proxy](#proxy-servers)
-   [Modalità sincrona e asincrona](#synchronous-and-asynchronous-modes)
-   [autenticazione](#authentication)

## <a name="http-transactions"></a>Transazioni HTTP

Quando si utilizzano transazioni HTTP, si scambiano informazioni con un altro computer in una rete. Le informazioni scambiate possono essere un file contenente testo o Multimedia oppure i risultati di una query di database. Una parte delle informazioni scambiate su una rete è detta *risorsa*. In genere il computer che invia una risorsa è il server e il computer che riceve la risorsa è un client. Tuttavia, è anche possibile che un client invii i dati a un server. A volte una transazione HTTP comporta un server di livello intermedio. Un server di livello intermedio raccoglie diverse risorse da altri server, compila le informazioni in un'unica risorsa e invia tale risorsa al client.

Il processo di ottenimento di una risorsa tramite il protocollo HTTP richiede che una serie di messaggi venga scambiata tra il client e il server. Il client avvia la transazione inviando un messaggio che richiede una risorsa. Questo messaggio viene chiamato richiesta HTTP o a volte solo una richiesta. Una richiesta HTTP è costituita dai componenti seguenti.

-   Metodo, Uniform Resource Identifier (URI), numero di versione protocollo
-   Intestazioni
-   Corpo entità

Quando un server riceve una richiesta, risponde inviando un messaggio al client. Il messaggio inviato dal server è denominato risposta HTTP. Una risposta HTTP è costituita dai componenti seguenti.

-   Numero di versione protocollo, codice di stato, testo di stato
-   Intestazioni
-   Corpo entità

La risposta indica che la richiesta non può essere elaborata o fornisce informazioni richieste. A seconda del tipo di richiesta, può trattarsi di informazioni su una risorsa, ad esempio le dimensioni e il tipo, oppure può essere una o tutte le risorse. La parte di una risposta che include alcune o tutte le risorse richieste viene chiamata "dati di risposta" o "corpo dell'entità" e la risposta non viene completata fino a quando non vengono ricevuti tutti i dati di risposta.

Per informazioni dettagliate sulle transazioni HTTP e sul protocollo HTTP, vedere [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt), HYPERTEXT Transfer Protocol-HTTP/1.1.

## <a name="proxy-servers"></a>Server proxy

Anche se una richiesta inviata da un client viene ricevuta dal server di destinazione, a volte la transazione passa prima di tutto tramite un server proxy. Un proxy intercetta la richiesta e può anche modificare la richiesta, prima di inviarla al server. Quando il server risponde, la risposta passa anche attraverso il proxy prima che venga inoltrata al client. Il proxy può modificare le intestazioni in questa risposta.

Tramite l'intercettazione e la conversione di transazioni di rete, un proxy può:

-   Proteggi il client monitorando transazioni potenzialmente pericolose.
-   Consentire al client di comunicare utilizzando protocolli che potrebbero non essere implementati dal software client.
-   Fungere da gateway tra una rete privata e una rete pubblica.

L'API WinHTTP include uno strumento di configurazione proxy che consente di fornire WinHTTP con informazioni relative a tutti i server proxy che intercettano le transazioni HTTP. Per informazioni sull'utilizzo dello strumento di configurazione proxy, vedere [ProxyCfg.exe, uno strumento di configurazione proxy](proxycfg-exe--a-proxy-configuration-tool.md).

## <a name="synchronous-and-asynchronous-modes"></a>Modalità sincrona e asincrona

Sono disponibili due modelli di programmazione per ottenere le risorse in una rete tramite WinHTTP, ovvero i modelli sincroni e asincroni. In un modello sincrono, una chiamata a una funzione o a un metodo non viene completata fino al completamento dell'operazione richiesta o fino a quando non si verifica un errore. Se, ad esempio, l'applicazione richiede una risorsa usando WinHTTP in modo sincrono, non continua con il passaggio successivo fino a quando non vengono ricevuti i dati richiesti.

Un modello asincrono, d'altra parte, consente a un'applicazione di eseguire altre attività durante l'attesa del recupero della risorsa. Se viene chiamato un altro metodo o funzione WinHTTP e un'operazione precedente non è stata completata, la funzione restituisce un errore. Quando si usa WinHTTP in modo asincrono, sono disponibili eventi e callback Component Object Model (COM) per notificare a un'applicazione lo stato di avanzamento in un'operazione HTTP.

## <a name="authentication"></a>Authentication

L'autenticazione è il processo mediante il quale un proxy HTTP o un server HTTP convalida le informazioni di accesso di un utente prima di consentire l'accesso alle risorse. In Internet vengono usati diversi schemi di autenticazione. In genere, il nome e la password di un utente vengono confrontati con un elenco autorizzato e se il sistema rileva una corrispondenza, viene concesso l'accesso all'extent specificato nell'elenco di autorizzazioni per l'utente.

Le funzioni WinHTTP supportano sia l'autenticazione server che quella proxy per le sessioni HTTP. WinHTTP supporta i seguenti schemi di autenticazione: Basic, digest (vedere [RFC 2617](https://www.ietf.org/rfc/rfc2617.txt)), [NTLM Authentication](../com/ntlmssp.md), Negotiate/ [Kerberos](../com/kerberos-v5-protocol.md)e Microsoft Passport 1,4. Per informazioni dettagliate sull'autenticazione, nonché un esempio di uso dell'autenticazione in un'applicazione Microsoft Visual C++, vedere [autenticazione in WinHTTP](authentication-in-winhttp.md).

Per informazioni sulle considerazioni sulla sicurezza relative all'autenticazione di base e Passport, vedere [considerazioni sulla sicurezza di WinHTTP](winhttp-security-considerations.md).

 

 
