---
title: Ricerca di endpoint
description: I programmi server sono in ascolto degli endpoint per le richieste client. La sintassi della stringa dell'endpoint dipende dalla sequenza di protocollo in uso. Ad esempio, l'endpoint per TCP/IP è un numero di porta e la sintassi dell'endpoint per le named pipe è un nome di pipe valido.
ms.assetid: 330bbe9f-b7e9-4a5b-86d8-824edec960d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 024a85704287db7e5f78bb67eee9b64a7c6dc84ce5724623450d36f743e5fa9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021281"
---
# <a name="finding-endpoints"></a>Ricerca di endpoint

I programmi server sono in ascolto degli endpoint per le richieste client. La sintassi della stringa dell'endpoint dipende dalla sequenza di protocollo in uso. Ad esempio, l'endpoint per TCP/IP è un numero di porta e la sintassi dell'endpoint per le named pipe è un nome di pipe valido.

Esistono due tipi di endpoint: ben noti e dinamici. La scelta del tipo di endpoint utilizzato dal programma determina se l'endpoint viene specificato dall'applicazione distribuita o dalla libreria di runtime.

Questa sezione illustra gli endpoint e presenta informazioni su come trovarli. È organizzato negli argomenti seguenti:

-   [Uso Well-Known endpoint](#using-well-known-endpoints)
-   [Uso di endpoint dinamici](#using-dynamic-endpoints)
-   [Esportazione di Well-Known endpoint nel database di mapping degli endpoint](#exporting-well-known-endpoints-into-the-endpoint-map-database)

> [!Note]  
> I termini *endpoint statici* *ed endpoint noti* sono equivalenti e usati in modo intercambiabile.

 

È possibile che l'applicazione client usi il mapping degli endpoint per determinare se un programma server è attualmente in esecuzione. Il client può chiamare [**RpcMgmtInqIfIds,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqifids) [**RpcMgmtEpEltInqBegin**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqbegin)e [**RpcMgmtEpEltInqDone**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqdone) per verificare se il server ha registrato l'interfaccia specifica richiesta nella mappa endpoint.

## <a name="using-well-known-endpoints"></a>Uso di endpoint noti

Gli endpoint noti sono endpoint pre-assegnati che il programma server usa ogni volta che viene eseguito. Poiché il server è sempre in ascolto di quel particolare endpoint, il client tenta sempre di connettersi ad esso. Gli endpoint noti vengono in genere assegnati dall'autorità responsabile del protocollo di trasporto. Poiché i computer host del server hanno un numero finito di endpoint disponibili, gli sviluppatori di applicazioni sono fortemente sconsigliati dall'uso di endpoint noti. Un altro vantaggio degli endpoint dinamici è che semplificano la gestione a lungo termine e la manutenzione del sistema.

Un'applicazione distribuita può specificare un endpoint noto in una stringa e passare tale stringa come parametro alla funzione [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep). In alternativa, la stringa dell'endpoint può essere visualizzata nell'intestazione dell'interfaccia file IDL come parte \[ [dell'attributo dell'interfaccia endpoint.](/windows/desktop/Midl/endpoint) \]

È possibile usare due approcci per implementare l'endpoint noto:

-   Specificare tutte le informazioni in un'associazione di stringhe
-   Archiviare l'endpoint noto nel database del servizio nomi

È possibile scrivere tutte le informazioni necessarie per stabilire un'associazione in un'applicazione distribuita durante lo sviluppo. Il client può specificare l'endpoint noto direttamente in una stringa, chiamare [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) per creare una stringa contenente tutte le informazioni di associazione e fornire questa stringa alla funzione [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) per ottenere un handle. Il client e il server possono essere hard coded per usare un endpoint noto o scritti in modo che le informazioni sull'endpoint provengono dalla riga di comando, da un file di dati, da un file di configurazione o dal file IDL.

L'applicazione client può anche eseguire una query su un database del servizio dei nomi per ottenere informazioni sull'endpoint note.

## <a name="using-dynamic-endpoints"></a>Uso di endpoint dinamici

Il numero di endpoint per un server specifico e una sequenza di protocollo specifica è in genere limitato. Ad esempio, quando si usa la sequenza di protocollo [TCP ncacn \_ ip, \_ ](/windows/desktop/Midl/ncacn-ip-tcp) che indica che la comunicazione di rete RPC avviene tramite TCP/IP, sono disponibili solo un numero limitato di porte (la maggior parte dei sistemi ha aperto solo l'intervallo da 1025 a 5000). Le librerie di runtime RPC consentono di assegnare gli endpoint in modo dinamico, in base alle esigenze. Poiché il numero di UUID dell'interfaccia possibili è praticamente illimitato, l'uso dell'UUID dell'interfaccia per indirizzare la chiamata offre più spazio per l'espansione e una maggiore flessibilità.

Per impostazione predefinita, le funzioni della libreria di runtime RPC ricercano informazioni sull'endpoint quando eseguono query su un database del servizio nomi. Se l'endpoint è dinamico, il database del servizio dei nomi non conterrà informazioni sull'endpoint. Tuttavia, la query conseglierà al programma client il nome di un server. Può quindi cercare la mappa degli endpoint del server.

Se il client deve effettuare una chiamata di procedura remota usando un endpoint dinamico, il metodo preferito è effettuare la chiamata su un handle di associazione parzialmente associato. La fase di esecuzione RPC risolve l'endpoint in modo trasparente. Questo metodo è superiore all'uso della [**funzione RpcEpResolveBinding,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepresolvebinding) in quanto consente meccanismi avanzati di memorizzazione nella cache in fase di esecuzione RPC.

Se è necessario un controllo più specifico sulla selezione dell'endpoint, i client possono cercare nell'endpoint una voce alla volta chiamando le funzioni [**RpcMgmtEpEltInqBegin**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqbegin), [**RpcMgmtEpEltInqNext**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqnext)e [**RpcMgmtEpEltInqDone.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqdone)

## <a name="exporting-well-known-endpoints-into-the-endpoint-map-database"></a>Esportazione di endpoint noti nel database di mapping degli endpoint

È possibile combinare i due approcci per trovare gli endpoint, soprattutto quando un sistema distribuito esegue la transizione da un modello di endpoint noto a un modello di endpoint dinamico. In queste transizioni, una versione intermedia del server userà un endpoint noto, ma registrerà anche l'endpoint noto con il database di mapping degli endpoint. Questo approccio consente ai client che usano endpoint noti e ai client che usano un endpoint dinamico per la connessione. Dopo l'aggiornamento di tutti i server, è possibile distribuire una nuova versione client che usa solo endpoint dinamici. Dopo l'aggiornamento di tutti i client, una versione finale del server può arrestare l'uso di endpoint noti e iniziare a usare solo endpoint dinamici.

Questo approccio consente un percorso di transizione per le applicazioni avviate con un endpoint noto ma che vogliono eseguire la migrazione a un endpoint dinamico senza richiedere un aggiornamento simultaneo di tutti i server e i client.

 

 