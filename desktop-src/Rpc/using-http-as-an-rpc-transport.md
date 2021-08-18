---
title: Utilizzo di HTTP come trasporto RPC
description: RPC su HTTP consente ai programmi client di utilizzare Internet per eseguire le procedure fornite dai programmi server in reti distanti.
ms.assetid: b5062d70-7625-4a9f-a8c1-025ef8342fcb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8775aab1771dcc6da9cade97d36c7141d6d66d8bc8172a20c8263ef64b8ed7ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010785"
---
# <a name="using-http-as-an-rpc-transport"></a>Utilizzo di HTTP come trasporto RPC

RPC su HTTP consente ai programmi client di utilizzare Internet per eseguire le procedure fornite dai programmi server in reti distanti. RPC su HTTP tunnela le chiamate tramite una porta HTTP stabilita. Di conseguenza, le chiamate possono attraversare i firewall di rete nelle reti client e server.

RPC su HTTP instrada le chiamate al proxy RPC situato nella rete del server RPC. Il proxy RPC stabilisce e gestisce una connessione al server RPC. Funge da proxy, inviando chiamate di procedura remota al server RPC e inviando le risposte del server attraverso Internet all'applicazione client. Questo processo è illustrato nel diagramma seguente.

![interazione tra un server RPC e Internet Information Server per rpc http](images/httprpc1.png)

Il diagramma mostra un firewall nella rete dell'applicazione client. Questa operazione non è necessaria per il funzionamento di RPC su HTTP. Tuttavia, se la rete client ha un firewall, sarà necessario anche un programma server proxy, ad esempio Microsoft Proxy Server.

Quando il programma client esegue una chiamata di procedura remota utilizzando HTTP come trasporto, la libreria di runtime RPC sul client contatta il proxy RPC. A seconda che al client RPC sia stato richiesto di usare rispettivamente la porta HTTP o HTTPS (HTTP con SSL) 80 o la porta 443. Il proxy RPC contatta il programma del server RPC e stabilisce una connessione TCP/IP. Il client e il proxy RPC mantengono la connessione HTTP o HTTPS su Internet. La connessione HTTP o HTTPS del client al proxy RPC può passare attraverso un firewall (soggetto alle autorizzazioni di accesso appropriate), se presente. Il server può quindi eseguire la chiamata di procedura remota e utilizzare la connessione tramite il proxy RPC per rispondere al client. Il proxy RPC è un'estensione ISAPI in esecuzione nel contesto di IIS.

Se il client o il server si disconnette per qualsiasi motivo, il proxy RPC lo rileverà e terminerà la sessione RPC. Finché la sessione continua, il proxy RPC manterrà le connessioni al client e al server. Inoltrerà le chiamate di procedura remota dal client al server e invierà le risposte dal server al client.

Il programma client RPC può eseguire il tunneling delle chiamate RPC tramite Internet creando un'associazione di stringhe nel formato seguente:

``` syntax
[object_uuid@]ncacn_http:rpc_server[endpoint,HttpProxy=proxy_server:http_port,RpcProxy=rpc_proxy:rpc_port,HttpConnectionOption=UseHttpProxy]
```

Dove:

-   *\_ L'uuid* dell'oggetto specifica un UUID dell'oggetto RPC. Per altre informazioni, vedere [Generating Interface UUIDs (Generazione di UUID di interfaccia)](generating-interface-uuids.md) e [String UUID (UUID stringa).](string-uuid.md)
-   **ncacn \_ http** seleziona la specifica della sequenza del protocollo per RPC su HTTP. Per altre informazioni, vedere [Costanti della sequenza di protocollo e](protocol-sequence-constants.md) Associazione di [stringhe.](string-binding.md)
-   *rpc \_ server* è l'indirizzo di rete del computer che esegue il processo del server RPC. L'indirizzo del server deve essere specificato in un formato visibile e comprensibile dal computer proxy RPC, non dal client. Poiché il client non si connette direttamente al server, non deve essere in grado di risolvere il nome del server o stabilire una connessione. Il proxy RPC stabilirà la connessione per conto del client e pertanto il *\_ server RPC* deve essere un nome riconoscibile dal proxy RPC.
-   *endpoint* specifica la porta TCP/IP su cui il processo del server RPC è in ascolto per le chiamate di procedura remota. Per altre informazioni, vedere [Ricerca di endpoint.](finding-endpoints.md)
-   **HttpProxy** specifica facoltativamente un server proxy HTTP nella rete del client RPC, ad esempio Microsoft Proxy Server. Se si seleziona un server proxy, non viene specificato alcun numero di porta, lo stub RPC usa la porta 80 per impostazione predefinita se non è richiesto SSL e la porta 443 se è specificato SSL.
-   **RpcProxy** specifica l'indirizzo e il numero di porta del computer IIS che funge da proxy per il server RPC. È necessario specificare questa opzione solo se il processo del server RPC si trova in un computer diverso da quello del proxy RPC. Se non si specifica un numero di porta, per impostazione predefinita lo stub del client RPC usa la porta 80 se ssl non è specificato e usa la porta 443 se è specificato SSL (HTTPS).
-   **HttpConnectionOption consente** facoltativamente di indirizzare il comportamento di RPC quando si effettuano connessioni HTTP. Il **valore UseHttpProxy** indica a RPC di instradare il traffico attraverso il proxy HTTP in qualsiasi momento, anche quando le opzioni Internet del client sono impostate in Internet Explorer su "Ignora server proxy per indirizzi locali".

    Questa opzione è supportata in Windows 7, Windows Server 2008 R2, Windows 8.1 e Windows Server 2012 R2 con KB2916915 installato. Questa opzione non è supportata in Windows 8 e Windows Server 2012. Le applicazioni possono determinare se questa opzione è supportata dal runtime RPC controllando il valore del Registro di sistema **ConnectionOptionsFlag** nella chiave del Registro di sistema seguente:

    **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Rpc**

    Se è impostato il bit 0 (LSB) di questo valore del Registro di sistema, questa opzione specifica è supportata. In caso contrario, questa opzione non è supportata dal runtime RPC nel sistema.

Per altre informazioni sulla creazione di associazioni di stringhe, vedere [Binding e handle.](binding-and-handles.md)

Il programma server RPC può accettare chiamate RPC con tunneling in ascolto sulla sequenza del protocollo HTTP ncacn. \_

Microsoft ha due implementazioni principali di RPC su HTTP: versione 1 e versione 2.

La versione 1 (chiamata RPC su HTTP v1) è supportata tramite Windows XP. La versione 1 del proxy RPC è supportata Windows 2000.

La versione 2 (chiamata RPC su HTTP v2) è la versione corrente.

Le due versioni hanno funzionalità diverse e interoperabilità limitata. Un riepilogo delle differenze è disponibile qui. Per considerazioni sull'interoperabilità, vedere [Requisiti di sistema e Interoperabilità per RPC su HTTP.](system-requirements-and-interoperability-for-rpc-over-http.md)

-   RPC su HTTP v1 richiede che il tunneling SSL sia abilitato in tutti i proxy/firewall HTTP tra il client RPC su HTTP e il proxy RPC. RPC su HTTP v1 tenta di compilare un Tunnel SSL sulla porta 80 anche se i dati inviati non sono effettivamente crittografati con SSL. Proxy e firewall rifiutano in genere tali richieste, a meno che non siano configurate in modo esplicito per consentirle. RPC su HTTP v2 non presenta alcun requisito di questo tipo.
-   RPC su HTTP v1 non è in grado di stabilire una sessione SSL per il proxy RPC. RPC su HTTP v2 può inviare tutto il traffico RPC su HTTP all'interno di una sessione SSL. Per impostazione predefinita, v2 richiede che i dati siano inviati all'interno di una sessione SSL.
-   RPC su HTTP v1 non è in grado di eseguire l'autenticazione al proxy RPC. RPC su HTTP v2 può eseguire l'autenticazione. per impostazione predefinita v2 richiede l'autenticazione al proxy RPC.
-   Il proxy RPC v1 non funziona correttamente quando il computer IIS in cui è installato fa parte di una Web farm. Il proxy RPC v2 funziona correttamente quando il computer IIS in cui è installato fa parte di una Web farm.

> [!Note]  
> Se Microsoft Internet Explorer è installato nel computer del programma client e il client non specifica **httpProxy** nell'associazione di stringhe, lo stub del client RPC cerca una voce **HttpProxy** nel Registro di sistema del computer client. Se ne trova uno, userà il proxy specificato nella voce del Registro di sistema.

 

Si supponga, ad esempio, che il programma client deve connettersi tramite Internet a un server RPC in un computer denominato Server7.microsoft.com. Si supponga inoltre che il proxy RPC venga eseguito Major7.microsoft.com. Il programma server RPC è in ascolto sulla porta 2225. Il client userebbe l'associazione di stringhe:

``` syntax
ncacn_http:Server7.microsoft.com[2225, RpcProxy=Major7.microsoft.com]
```

Se il proxy RPC è in grado di risolvere il nome del server come Server7, senza richiedere un nome di dominio completo, è anche possibile specificare:

``` syntax
ncacn_http:Server7 [2225, RpcProxy=Major7.microsoft.com]
```

Se la rete client usa un firewall e un server proxy Internet denominato myproxy e Internet Explorer nel client non è configurato per l'uso di tale proxy, è necessario modificare l'associazione di stringa del client in:

``` syntax
ncacn_http:Server7.microsoft.com[,HttpProxy=myproxy:80,RpcProxy=Major7.microsoft.com:80]
```

Questo indica al client di connettersi al programma del server RPC Server7.microsoft.com. A tale scopo, il client userà prima la porta 80 (o la porta 443 se si usa SSL) per connettersi a myproxy. In questo modo il programma client avrà accesso a Internet. Tramite Internet, il programma client si connette quindi al proxy RPC Major7.microsoft.com. Il proxy RPC stabilirà una connessione al programma del server RPC in esecuzione Server7.microsoft.com.

Se la rete client usa un firewall e se il proxy RPC non può essere raggiunto direttamente, per stabilire più rapidamente una connessione, l'associazione della stringa client può essere modificata in:

``` syntax
ncacn_http:Server7.microsoft.com[RpcProxy=Major7.microsoft.com:80,HttpConnectionOption=UseHttpProxy]
```

**HttpConnectionOption consente** di indirizzare il comportamento di RPC quando si effettuano connessioni HTTP. Il **valore UseHttpProxy** indica a RPC di instradare il traffico attraverso il proxy HTTP in qualsiasi momento, anche quando le opzioni Internet del client sono impostate in Internet Explorer su "Ignora server proxy per indirizzi locali". Questo indica al client di connettersi in modo forzato al proxy RPC tramite il proxy HTTP. In questo modo si accelera il tempo necessario per stabilire una connessione, in quanto vengono ignorati eventuali ritardi nella ricerca del server RPC direttamente prima di usare il proxy HTTP.

Se si **usa l'opzione HttpConnectionOption** e Internet Explorer nel client non è configurato per l'uso di tale proxy HTTP, le connessioni potrebbero non riuscire con **RPC S INVALID NETWORK \_ \_ \_ \_ OPTIONS**.

La maggior parte dei computer attualmente è configurata per Web browser. Pertanto, la maggior parte dei client non deve specificare **HttpProxy**, perché verrà recuperato dalle impostazioni di connettività Internet.

 

 




