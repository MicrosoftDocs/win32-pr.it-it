---
title: Utilizzo di HTTP come trasporto RPC
description: RPC-over-HTTP consente ai programmi client di usare Internet per eseguire le procedure fornite dai programmi server in reti remote.
ms.assetid: b5062d70-7625-4a9f-a8c1-025ef8342fcb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5860757a6c5df9937e77fc078df2526affb967fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471366"
---
# <a name="using-http-as-an-rpc-transport"></a>Utilizzo di HTTP come trasporto RPC

RPC-over-HTTP consente ai programmi client di usare Internet per eseguire le procedure fornite dai programmi server in reti remote. RPC su HTTP esegue il tunneling delle chiamate tramite una porta HTTP stabilita. Pertanto, le chiamate possono attraversare i firewall di rete sia per le reti client che per quelle server.

RPC su HTTP instrada le chiamate al proxy RPC che si trova nella rete del server RPC. Il proxy RPC stabilisce e gestisce una connessione al server RPC. Funge da proxy, inviando chiamate a procedure remote al server RPC e inviando le risposte del server attraverso Internet all'applicazione client. Questo processo è illustrato nella figura seguente.

![interazione tra un server RPC e Internet Information Server per http RPC](images/httprpc1.png)

Il diagramma mostra un firewall nella rete dell'applicazione client. Questa operazione non è necessaria per il funzionamento di RPC su HTTP. Tuttavia, se la rete client dispone di un firewall, sarà necessario anche un programma server proxy quale Microsoft Proxy Server.

Quando il programma client invia una chiamata di procedura remota utilizzando HTTP come trasporto, la libreria di runtime RPC sul client contatta il proxy RPC. A seconda che il client RPC debba utilizzare rispettivamente la porta HTTP o HTTPS (HTTP con SSL) 80 o la porta 443. Il proxy RPC contatta il programma server RPC e stabilisce una connessione TCP/IP. Il client e il proxy RPC gestiscono la connessione HTTP o HTTPS su Internet. La connessione HTTP o HTTPS del client al proxy RPC può passare attraverso un firewall (soggetto alle autorizzazioni di accesso appropriate) se presente. Il server può quindi eseguire la chiamata di procedura remota e utilizzare la connessione tramite il proxy RPC per rispondere al client. Il proxy RPC è un'estensione ISAPI in esecuzione nel contesto di IIS.

Se per qualsiasi motivo il client o il server si disconnette, il proxy RPC lo rileverà e terminerà la sessione RPC. Fino a quando la sessione continua, il proxy RPC manterrà le connessioni al client e al server. Inoltra le chiamate di procedura remota dal client al server e invierà le risposte dal server al client.

Il programma client RPC può eseguire il tunneling delle chiamate RPC tramite Internet creando un'associazione di stringa nel formato seguente:

``` syntax
[object_uuid@]ncacn_http:rpc_server[endpoint,HttpProxy=proxy_server:http_port,RpcProxy=rpc_proxy:rpc_port,HttpConnectionOption=UseHttpProxy]
```

Dove:

-   *\_ UUID oggetto* specifica un UUID dell'oggetto RPC. Per altre informazioni, vedere [generazione di UUID di interfaccia](generating-interface-uuids.md) e [UUID di stringa](string-uuid.md).
-   **ncacn \_ http** consente di selezionare la specifica della sequenza di protocollo per RPC su http. Per altre informazioni, vedere [costanti di sequenza del protocollo](protocol-sequence-constants.md) e [binding di stringa](string-binding.md).
-   *il \_ server RPC* è l'indirizzo di rete del computer in cui è in esecuzione il processo server RPC. L'indirizzo del server deve essere specificato in un form visibile e comprensibile dal computer proxy RPC, non dal client. Poiché il client non si connette direttamente al server, non è necessario che sia in grado di risolvere il nome del server o di stabilire una connessione. Il proxy RPC stabilirà la connessione per conto del client e pertanto il *\_ server RPC* deve essere un nome riconoscibile dal proxy RPC.
-   *endpoint* specifica la porta TCP/IP su cui il processo server RPC è in ascolto per le chiamate di procedure remote. Per ulteriori informazioni, vedere la pagina relativa alla [ricerca di endpoint](finding-endpoints.md).
-   **HttpProxy** consente di specificare facoltativamente un server proxy HTTP nella rete del client RPC, ad esempio Microsoft Proxy Server. Se è selezionato un server proxy, non viene specificato alcun numero di porta, lo stub RPC usa la porta 80 per impostazione predefinita se non viene richiesto SSL e la porta 443 se è specificato SSL.
-   **Rpcproxy** specifica l'indirizzo e il numero di porta del computer IIS che funge da proxy per il server RPC. È necessario specificare questa impostazione solo se il processo server RPC si trova in un computer diverso da quello del proxy RPC. Se non si specifica un numero di porta, per impostazione predefinita lo stub del client RPC utilizza la porta 80 se non si specifica SSL e utilizza la porta 443 se viene specificato SSL (HTTPS).
-   **HttpConnectionOption** facoltativamente consente di indirizzare il comportamento di RPC quando si effettuano le connessioni HTTP. Il valore **UseHttpProxy** indica a RPC di instradare il traffico attraverso il proxy http sempre, anche quando le opzioni Internet del client sono impostate in Internet Explorer su "Ignora server proxy per indirizzi locali".

    Questa opzione è supportata in Windows 7, Windows Server 2008 R2, Windows 8.1 e Windows Server 2012 R2 con KB2916915 installato. Questa opzione non è supportata in Windows 8 e Windows Server 2012. Le applicazioni possono determinare se questa opzione è supportata dal runtime RPC controllando il valore del registro di sistema **ConnectionOptionsFlag** che si trova nella seguente chiave del registro di sistema:

    **HKEY \_ \_ computer locale \\ software \\ Microsoft \\ RPC**

    Se viene impostato il bit 0 (LSB) del valore del registro di sistema, questa opzione specifica è supportata. in caso contrario, questa opzione non è supportata dal runtime RPC nel sistema.

Per ulteriori informazioni sulla creazione di associazioni di stringa, vedere [Binding e handle](binding-and-handles.md).

Il programma server RPC può accettare chiamate RPC con tunneling ascoltando la \_ sequenza del protocollo http ncacn.

Microsoft dispone di due implementazioni principali di RPC su HTTP: versione 1 e versione 2.

La versione 1 (denominata RPC su HTTP V1) è supportata tramite Windows XP. La versione 1 del proxy RPC è supportata da Windows 2000.

La versione 2 (denominata RPC su HTTP v2) è la versione corrente.

Le due versioni hanno funzionalità diverse e un'interoperabilità limitata. Un riepilogo delle differenze è disponibile qui. Per considerazioni sull'interoperabilità, vedere [requisiti di sistema e interoperabilità per RPC su http](system-requirements-and-interoperability-for-rpc-over-http.md).

-   RPC su HTTP V1 richiede l'abilitazione del tunneling SSL su tutti i proxy/firewall HTTP tra il client RPC su HTTP e il proxy RPC. RPC su HTTP V1 tenta di creare un tunnel SSL sulla porta 80 anche se i dati inviati non sono effettivamente crittografati tramite SSL. Proxy e firewall in genere rifiutano tali richieste, a meno che non siano configurate in modo esplicito per consentirle. RPC su HTTP V2 non ha tale requisito.
-   RPC su HTTP V1 non è in grado di stabilire una sessione SSL per il proxy RPC. RPC su HTTP V2 può inviare tutto il traffico RPC su HTTP all'interno di una sessione SSL. per impostazione predefinita, la versione V2 richiede che i dati vengano inviati in una sessione SSL.
-   RPC su HTTP V1 non è in grado di eseguire l'autenticazione al proxy RPC. La RPC su HTTP V2 può eseguire l'autenticazione; per impostazione predefinita, la versione V2 richiede l'autenticazione al proxy RPC.
-   Il proxy RPC V1 non funziona correttamente quando il computer IIS in cui è installato fa parte di un Web farm. Il proxy RPC V2 funziona correttamente quando il computer IIS in cui è installato fa parte di un Web farm.

> [!Note]  
> Se Microsoft Internet Explorer è installato nel computer del programma client e il client non specifica un **HttpProxy** nell'associazione di stringhe, lo stub client RPC eseguirà la ricerca nel registro di sistema del computer client per una voce **HttpProxy** . Se ne trova una, utilizzerà il proxy specificato nella voce del registro di sistema.

 

Si supponga, ad esempio, che il programma client debba connettersi attraverso Internet a un server RPC in un computer denominato Server7.microsoft.com. Si supponga inoltre che il proxy RPC venga eseguito in Major7.microsoft.com. Il programma server RPC è in ascolto sulla porta 2225. Il client userà l'associazione di stringhe:

``` syntax
ncacn_http:Server7.microsoft.com[2225, RpcProxy=Major7.microsoft.com]
```

Se il proxy RPC può risolvere il nome del server come server7, senza richiedere un nome di dominio completo, è anche possibile specificare:

``` syntax
ncacn_http:Server7 [2225, RpcProxy=Major7.microsoft.com]
```

Se la rete client utilizza un firewall e un server proxy Internet denominato proxy e Internet Explorer sul client non è configurato per l'utilizzo del proxy, è necessario modificare il binding di stringa del client in:

``` syntax
ncacn_http:Server7.microsoft.com[,HttpProxy=myproxy:80,RpcProxy=Major7.microsoft.com:80]
```

In questo modo il client si connette al programma server RPC in Server7.microsoft.com. A tale scopo, il client utilizzerà prima la porta 80 (o la porta 443 se viene usato SSL) per connettersi a proxy. In questo modo, l'accesso al programma client viene fornito a Internet. Utilizzando Internet, il programma client si connette quindi al proxy RPC in Major7.microsoft.com. Tramite il proxy RPC viene stabilita una connessione al programma server RPC in esecuzione in Server7.microsoft.com.

Se la rete client utilizza un firewall e se non è possibile raggiungere il proxy RPC direttamente, per ottenere una connessione stabilita più velocemente, è possibile modificare l'associazione di stringhe client a:

``` syntax
ncacn_http:Server7.microsoft.com[RpcProxy=Major7.microsoft.com:80,HttpConnectionOption=UseHttpProxy]
```

**HttpConnectionOption** consente di indirizzare il comportamento di RPC quando si effettuano le connessioni HTTP. Il valore **UseHttpProxy** indica a RPC di instradare il traffico attraverso il proxy http sempre, anche quando le opzioni Internet del client sono impostate in Internet Explorer su "Ignora server proxy per indirizzi locali". Ciò indica al client di connettersi in modo forzato al proxy RPC tramite il proxy http. Questo consente di velocizzare il tempo necessario per stabilire una connessione poiché ignora eventuali ritardi di ricerca del server RPC direttamente prima di usare il proxy HTTP.

Se si usa l'opzione **HttpConnectionOption** e Internet Explorer nel client non è configurato per l'uso del proxy http, le connessioni potrebbero non riuscire con le **Opzioni di rete RPC non \_ \_ valide \_ \_**.

Attualmente la maggior parte dei computer è configurata per l'esplorazione Web. Non è pertanto necessario che la maggior parte dei client specifichi il **HttpProxy**, perché verrà recuperato dalle impostazioni di connettività Internet.

 

 




