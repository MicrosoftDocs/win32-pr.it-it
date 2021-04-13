---
title: Ricerca di endpoint
description: I programmi server restano in ascolto degli endpoint per le richieste client. La sintassi della stringa dell'endpoint dipende dalla sequenza di protocollo utilizzata. L'endpoint per TCP/IP, ad esempio, è un numero di porta e la sintassi dell'endpoint per Named Pipes è un nome di pipe valido.
ms.assetid: 330bbe9f-b7e9-4a5b-86d8-824edec960d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb0a97df3408a4d3c24dff9de28553f9e4b2210d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337783"
---
# <a name="finding-endpoints"></a>Ricerca di endpoint

I programmi server restano in ascolto degli endpoint per le richieste client. La sintassi della stringa dell'endpoint dipende dalla sequenza di protocollo utilizzata. L'endpoint per TCP/IP, ad esempio, è un numero di porta e la sintassi dell'endpoint per Named Pipes è un nome di pipe valido.

Esistono due tipi di endpoint: ben noti e dinamici. La scelta del tipo di endpoint utilizzato dal programma determina se l'applicazione distribuita o la libreria di runtime specifica l'endpoint.

Questa sezione illustra gli endpoint e presenta informazioni su come trovarli. Sono organizzati negli argomenti seguenti:

-   [Uso di endpoint Well-Known](#using-well-known-endpoints)
-   [Uso di endpoint dinamici](#using-dynamic-endpoints)
-   [Esportazione di endpoint Well-Known nel database di mapping degli endpoint](#exporting-well-known-endpoints-into-the-endpoint-map-database)

> [!Note]  
> I termini *endpoint statici* ed *endpoint noti* sono equivalenti e vengono usati in modo interscambiabile.

 

È possibile che l'applicazione client utilizzi la mappa dell'endpoint per determinare se un programma server è attualmente in esecuzione. Il client può chiamare [**RpcMgmtInqIfIds**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqifids), [**RpcMgmtEpEltInqBegin**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqbegin)e [**RpcMgmtEpEltInqDone**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqdone) per verificare se il server ha registrato la particolare interfaccia richiesta nella mappa dell'endpoint.

## <a name="using-well-known-endpoints"></a>Uso di endpoint noti

Gli endpoint noti sono endpoint pre-assegnati che il programma server utilizza ogni volta che viene eseguito. Poiché il server è sempre in ascolto di tale endpoint specifico, il client tenta sempre di connettersi a tale endpoint. Gli endpoint noti vengono in genere assegnati dall'autorità responsabile del protocollo di trasporto. Poiché i computer host server hanno un numero finito di endpoint disponibili, gli sviluppatori di applicazioni sono fortemente sconsigliati di usare endpoint noti. Un altro vantaggio degli endpoint dinamici è che semplificano la gestione e la manutenzione a lungo termine del sistema.

Un'applicazione distribuita può specificare un endpoint noto in una stringa e passare tale stringa come parametro alla funzione [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep). In alternativa, la stringa dell'endpoint può essere visualizzata nell'intestazione dell'interfaccia del file IDL come parte dell'attributo dell'interfaccia dell' \[ [endpoint](/windows/desktop/Midl/endpoint) \] .

Per implementare l'endpoint noto, è possibile usare due approcci:

-   Specificare tutte le informazioni in un'associazione di stringa
-   Archiviare l'endpoint noto nel database del servizio dei nomi

È possibile scrivere tutte le informazioni necessarie per stabilire un'associazione in un'applicazione distribuita quando lo si sviluppa. Il client può specificare l'endpoint noto direttamente in una stringa, chiamare [**errore in RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) per creare una stringa che contiene tutte le informazioni di binding e fornire questa stringa alla funzione [**errore in RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) per ottenere un handle. Il client e il server possono essere hardcoded per utilizzare un endpoint noto o scritti in modo che le informazioni dell'endpoint provengano dalla riga di comando, da un file di dati, da un file di configurazione o dal file IDL.

L'applicazione client può anche eseguire una query su un database del servizio dei nomi per ottenere informazioni note sugli endpoint.

## <a name="using-dynamic-endpoints"></a>Uso di endpoint dinamici

Il numero di endpoint per un determinato server e una particolare sequenza di protocollo sono in genere limitati. Ad esempio, quando si utilizza la sequenza di protocollo [ \_ \_ TCP IP ncacn](/windows/desktop/Midl/ncacn-ip-tcp) , che indica che la comunicazione di rete RPC viene eseguita utilizzando TCP/IP, sono disponibili solo un numero limitato di porte (la maggior parte dei sistemi ha aperto solo l'intervallo da 1025 a 5000). Le librerie di runtime RPC consentono di assegnare gli endpoint in modo dinamico, in base alle esigenze. Poiché il numero degli UUID di interfaccia possibili è praticamente illimitato, l'uso dell'UUID dell'interfaccia per indirizzare la chiamata offre più spazio per l'espansione e una maggiore flessibilità.

Per impostazione predefinita, le funzioni della libreria di runtime RPC eseguono la ricerca di informazioni sull'endpoint quando eseguono una query su un database del servizio. Se l'endpoint è dinamico, il database del servizio nomi non conterrà informazioni sull'endpoint. Tuttavia, la query fornirà al programma client il nome di un server. Può quindi eseguire la ricerca nella mappa dell'endpoint del server.

Se il client deve eseguire una chiamata di procedura remota utilizzando un endpoint dinamico, il metodo preferito consiste nel effettuare la chiamata su un handle di associazione parzialmente associato. Il runtime RPC risolve l'endpoint in modo trasparente. Questo metodo è superiore all'uso della funzione [**RpcEpResolveBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepresolvebinding) , in quanto consente meccanismi avanzati di memorizzazione nella cache in fase di esecuzione RPC.

Se è necessario un controllo più specifico sulla selezione dell'endpoint, i client possono cercare l'endpoint mappare una voce alla volta chiamando le funzioni [**RpcMgmtEpEltInqBegin**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqbegin), [**RpcMgmtEpEltInqNext**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqnext)e [**RpcMgmtEpEltInqDone**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqdone) .

## <a name="exporting-well-known-endpoints-into-the-endpoint-map-database"></a>Esportazione di endpoint noti nel database di mapping degli endpoint

È possibile combinare i due approcci per trovare gli endpoint, soprattutto quando un sistema distribuito esegue la transizione da un modello di endpoint noto a un modello di endpoint dinamico. In tali transizioni, una versione intermedia del server utilizzerà un endpoint noto, ma registrerà anche l'endpoint noto con il database di mapping degli endpoint. Questo approccio consente ai client che utilizzano endpoint e client noti che utilizzano un endpoint dinamico di connettersi. Una volta che tutti i server sono stati aggiornati, è possibile distribuire una nuova versione del client che usa solo endpoint dinamici. Una volta che tutti i client sono stati aggiornati, una versione finale del server può arrestare l'uso di endpoint noti e iniziare a usare solo gli endpoint dinamici.

Questo approccio consente un percorso di transizione per le applicazioni che sono state avviate con un endpoint noto, ma che desiderano eseguire la migrazione a un endpoint dinamico senza richiedere un aggiornamento simultaneo di tutti i server e i client.

 

 