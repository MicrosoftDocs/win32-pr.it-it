---
title: Associazione di stringhe
description: L'associazione di stringhe è una stringa di caratteri senza segno composta da stringhe che rappresentano l'UUID dell'oggetto di associazione, la sequenza del protocollo RPC, l'indirizzo di rete e le opzioni dell'endpoint e dell'endpoint.
ms.assetid: 5e55ddd0-d71c-42ef-90cc-dd1f0b9ed305
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b3f925c03c85be3c47ab174a85f31e72e40d828
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386980"
---
# <a name="string-binding"></a>Associazione di stringhe

L'associazione di stringhe è una stringa di caratteri senza segno composta da stringhe che rappresentano l'UUID dell'oggetto di associazione, la sequenza del protocollo RPC, l'indirizzo di rete e le opzioni dell'endpoint e dell'endpoint.

*ObjectUUID* @ *ProtocolSequence:**Endpoint NetworkAddress,* \[ *opzione*\]

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="ObjectUUID"></span><span id="objectuuid"></span><span id="OBJECTUUID"></span>*ObjectUUID*
</dt> <dd>

[UUID dell'oggetto](/windows/desktop/Midl/uuid) gestito dalla chiamata di procedura remota. Nel server, la libreria di runtime RPC esegue il mapping del tipo di oggetto a un vettore del punto di ingresso del gestore (una matrice di puntatori a funzione) per richiamare la routine di gestione corretta. Per informazioni su come eseguire il mapping degli UUID degli oggetti ai vettori del punto di ingresso di gestione, vedere [Registrazione di interfacce](registering-interfaces.md).

</dd> <dt>

<span id="ProtocolSequence"></span><span id="protocolsequence"></span><span id="PROTOCOLSEQUENCE"></span>*ProtocolSequence*
</dt> <dd>

Stringa di caratteri che rappresenta una combinazione valida di un protocollo RPC (ad esempio ncacn), di un protocollo di trasporto (ad esempio TCP) e di un protocollo di rete (ad esempio IP). Rpc Microsoft supporta i protocolli seguenti specificati in [Costanti della sequenza di protocollo](protocol-sequence-constants.md).

</dd> <dt>

<span id="NetworkAddress"></span><span id="networkaddress"></span><span id="NETWORKADDRESS"></span>*NetworkAddress*
</dt> <dd>

Indirizzo di rete del sistema per ricevere chiamate di procedura remota.

> [!Note]  
> Le sequenze di protocollo seguenti non sono supportate a livello di Windows XP:

 

-   [ncacn \_ nb \_ tcp](/windows/desktop/Midl/ncacn-nb-tcp)
-   [ncacn \_ nb \_ nb](/windows/desktop/Midl/ncacn-nb-nb)
-   [ncacn \_ nb \_ ipx](/windows/desktop/Midl/ncacn-nb-ipx)
-   [ncacn \_ dnet \_ nsp](/windows/desktop/Midl/ncacn-dnet-nsp)
-   [ncacn \_ vns \_ spp](/windows/desktop/Midl/ncacn-vns-spp)
-   [ncadg \_ mq](/windows/desktop/Midl/ncadg-mq)
-   [ncadg \_ ipx](/windows/desktop/Midl/ncadg-ipx)

Il formato e il contenuto dell'indirizzo di rete dipendono dalla sequenza di protocollo specificata, come indicato di seguito.



| Sequenza di protocollo                       | Indirizzo di rete                                                                                                                                  | Esempio                                               |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [ncacn \_ nb \_ tcp](/windows/desktop/Midl/ncacn-nb-tcp)     | Nome computer                                                                                                                                    | Myserver                                               |
| [ncacn \_ nb \_ ipx](/windows/desktop/Midl/ncacn-nb-ipx)     | Nome computer                                                                                                                                    | Myserver                                               |
| [ncacn \_ nb \_ nb](/windows/desktop/Midl/ncacn-nb-nb)       | Nome computer                                                                                                                                    | Myserver                                               |
| [ncacn \_ ip \_ tcp](/windows/desktop/Midl/ncacn-ip-tcp)     | Indirizzo Internet a quattro ottetti o nome host. Se lo stack di rete IPv6 è installato, IPv6 è completamente supportato e viene accettato anche un indirizzo IPv6. | 128.10.2.30 anynode.microsoft.com                      |
| [ncacn \_ np](/windows/desktop/Midl/ncacn-np)              | Nome del server (le barre rovesciate doppie iniziali sono facoltative)                                                                                            | myserver \\ \\ myotherserver                             |
| [ncacn \_ spx](/windows/desktop/Midl/ncacn-spx)            | Indirizzo IpX Internet o nome del server                                                                                                             | ~0000000108002B30612C myserver                         |
| [ncacn \_ dnet \_ nsp](/windows/desktop/Midl/ncacn-dnet-nsp) | Sintassi di area e nodo                                                                                                                             | 4.120                                                  |
| [ncacn \_ in \_ dsp](/windows/desktop/Midl/ncacn-at-dsp)     | Nome computer, facoltativamente seguito da @ e dal nome della zona AppleTalk. Il valore predefinito è @ \* , la zona del client, se non viene specificata alcuna zona                     | servername@zonename Nomeserver                         |
| [ncacn \_ vns \_ spp](/windows/desktop/Midl/ncacn-vns-spp)   | Nome del server StreetTalk nel modulo item@group@organization                                                                                       | printserver@sdkdocs@microsoft                          |
| [ncadg \_ mq](/windows/desktop/Midl/ncadg-mq)              | Nome server                                                                                                                                      | Myserver                                               |
| [ncacn \_ http](/windows/desktop/Midl/ncacn-http)          | Indirizzo Internet (quattro ottetti o nome descrittivo o nome del server locale)                                                                       | 128.10.2.30 somesvr@anywhere.com mylocalsvr<br/> |
| [ncadg \_ ip \_ udp](/windows/desktop/Midl/ncadg-ip-udp)     | Indirizzo Internet a quattro ottetti o nome host                                                                                                        | 128.10.2.30 anynode.microsoft.com                      |
| [ncadg \_ ipx](/windows/desktop/Midl/ncadg-ipx)            | Indirizzo IpX Internet o nome del server                                                                                                             | ~0000000108002B30612C myserver                         |
| [ncalrpc](/windows/desktop/Midl/ncalrpc)                 | Nome computer                                                                                                                                     | thismachine                                            |



 

Il campo network-address è facoltativo. Quando non si specifica un indirizzo di rete, l'associazione di stringhe fa riferimento all'host locale. È possibile specificare il nome del computer locale quando si usa la sequenza di protocollo **ncalrpc,** ma questa operazione non è completamente necessaria.

</dd> <dt>

<span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>*Endpoint*
</dt> <dd>

Endpoint, o indirizzo, del processo per ricevere chiamate di procedura remota. Un endpoint può essere preceduto dalla parola chiave **endpoint=**. Specificare l'endpoint è facoltativo se il server ha registrato le associazioni con il mapper dell'endpoint. Vedere [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister).

Il formato e il contenuto di un endpoint dipendono dalla sequenza di protocollo specificata, come illustrato nella tabella endpoint/opzione seguente.

</dd> <dt>

<span id="Option"></span><span id="option"></span><span id="OPTION"></span>*Opzione*
</dt> <dd>

Opzioni specifiche del protocollo. Il campo dell'opzione non è obbligatorio. Ogni opzione viene specificata da una coppia {name, value} che usa il valore dell'opzione syntax *option* = *name*. Le opzioni vengono definite per ogni sequenza di protocollo, come illustrato nella tabella Endpoint/Opzione seguente.



| Sequenza di protocollo                       | Endpoint                                                                                           | Esempio             | Nome opzione                                            |
|-----------------------------------------|----------------------------------------------------------------------------------------------------|----------------------|--------------------------------------------------------|
| [ncacn \_ nb \_ tcp](/windows/desktop/Midl/ncacn-nb-tcp)     | Numero intero compreso tra 1 e 254. Molti valori compresi tra 0 e 32 sono riservati da Microsoft.                 | 100                  | Nessuno                                                   |
| [ncacn \_ nb \_ ipx](/windows/desktop/Midl/ncacn-nb-ipx)     | (come sopra)                                                                                         | (come sopra)           | Nessuno                                                   |
| [ncacn \_ nb \_ nb](/windows/desktop/Midl/ncacn-nb-nb)       | (come sopra)                                                                                         | (come sopra)           | Nessuno                                                   |
| [ncacn \_ ip \_ tcp](/windows/desktop/Midl/ncacn-ip-tcp)     | Numero di porta Internet.                                                                              | 1025                 | Nessuno                                                   |
| [ncacn \_ np](/windows/desktop/Midl/ncacn-np)              | Named pipe. Il nome deve iniziare con \\ \\ "pipe".                                                       | \\\\pipe \\ \\ pipename | Security                                               |
| [ncacn \_ spx](/windows/desktop/Midl/ncacn-spx)            | Numero intero compreso tra 1 e 65535.                                                                       | 5000                 | Nessuno                                                   |
| [ncacn \_ dnet \_ nsp](/windows/desktop/Midl/ncacn-dnet-nsp) | DeCnet fase IV numero di oggetto (deve essere preceduto dal \# carattere) o nome dell'oggetto.              | mailserver \# 17      | Nessuno                                                   |
| [ncacn \_ at \_ dsp](/windows/desktop/Midl/ncacn-at-dsp)     | Stringa di caratteri con lunghezza fino a 22 byte.                                                           | myservicesendpoint   | Nessuno                                                   |
| [ncacn \_ vns \_ spp](/windows/desktop/Midl/ncacn-vns-spp)   | Numero di porta SPP vines compreso tra 250 e 511.                                                         | 500                  | Nessuno                                                   |
| [ncadg \_ mq](/windows/desktop/Midl/ncadg-mq)              | Numero intero compreso tra 1 e 65535.                                                                       | 5000                 | Nessuno                                                   |
| [ncacn \_ http](/windows/desktop/Midl/ncacn-http)          | Numero di porta Internet.                                                                              | 2215                 | Nomi dei server proxy HTTP e RPC, opzione HttpConnection |
| [ncadg \_ ip \_ udp](/windows/desktop/Midl/ncadg-ip-udp)     | Numero di porta Internet.                                                                              | 1025                 | Nessuno                                                   |
| [ncadg \_ ipx](/windows/desktop/Midl/ncadg-ipx)            | Numero intero compreso tra 1 e 65535.                                                                       | 5000                 | Nessuno                                                   |
| [ncalrpc](/windows/desktop/Midl/ncalrpc)                 | Stringa che specifica il nome dell'applicazione o del servizio. La stringa non può includere caratteri barra rovesciata. | my \_ printer          | Security                                               |



 

Il **nome dell'opzione HttpConnectionOption,** supportato per la sequenza di protocollo HTTP ncacn, \_ accetta il valore seguente.



| Nome opzione       | Valore            |
|-------------------|------------------|
| HttpConnectOption | **UseHttpProxy** |



 

**HttpConnectionOption consente** di indirizzare il comportamento di RPC quando si effettuano connessioni HTTP. Il **valore UseHttpProxy** indica a RPC di instradare il traffico attraverso il proxy HTTP in qualsiasi momento, anche quando nel client le opzioni Internet sono impostate in Internet Explorer su Ignora il server proxy per gli indirizzi locali.  Questa opzione indica al client di connettersi in modo forzato al proxy RPC tramite il proxy HTTP. In questo modo si accelera il tempo necessario per stabilire una connessione, in quanto vengono ignorati eventuali ritardi nella ricerca del server RPC direttamente prima di usare il proxy HTTP.

Se si **usa questa opzione HttpConnectionOption** e Internet Explorer nel client non è configurato per l'uso di tale proxy HTTP, le connessioni potrebbero non riuscire con **RPC S INVALID NETWORK \_ \_ \_ \_ OPTIONS**.

``` syntax
HttpConnectOption=UseHttpProxy
```

Per altre informazioni su **HttpConnectionOption,** vedere [Uso di HTTP come trasporto RPC.](using-http-as-an-rpc-transport.md)

Il **nome** dell'opzione di sicurezza, supportato per le sequenze di protocollo ncalrpc, ncacn \_ np, ncadg ip udp e \_ \_ ncadg ipx, accetta i valori di opzione \_ seguenti.



| Nome opzione  | Valore opzione                                                                               |
|--------------|--------------------------------------------------------------------------------------------|
| **Sicurezza** | {identification \| anonymous \| impersonation} {dynamic \| static} {**true** \| **false**} |



 

Se si specifica il nome dell'opzione di sicurezza, è necessario specificare anche una voce di ogni set di valori di opzioni di sicurezza. I valori delle opzioni devono essere separati da uno spazio singolo. Ad esempio, i campi *Option* seguenti sono validi:

``` syntax
Security=identification dynamic true
Security=impersonation static true
```

I valori delle opzioni di sicurezza hanno i significati seguenti.



| Valore dell'opzione di sicurezza | Descrizione                                                                                                                                                                                                                                                                                                                                              |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Anonimo             | Il client è anonimo per il server.                                                                                                                                                                                                                                                                                                                   |
| Dynamic               | Le modifiche all'identità di sicurezza client vengono viste dal server quando il server utilizza la sicurezza del trasporto. Si tratta della modalità predefinita per la sicurezza a livello di trasporto LRPC (ncalrpc) e per la sicurezza a livello di trasporto named pipe (ncacn \_ np).                                                                                                             |
| **False**             | Effective = **FALSE**; tutte le impostazioni dei privilegi del token, incluse quelle impostate su OFF, sono incluse nel token nel server e possono essere abilitate dal server. I privilegi sono rilevanti solo per le chiamate RPC dello stesso computer.                                                                                                                                     |
| **Identificazione**    | Il server dispone di informazioni sul client, ma non può rappresentare.                                                                                                                                                                                                                                                                                      |
| **Rappresentazione**     | Il server può agire per conto del client all'interno del sistema locale (la sicurezza a livello di trasporto non supporta la delega).                                                                                                                                                                                                                               |
| **Statico**            | Le modifiche all'identità di sicurezza client non vengono viste dal server quando il server utilizza la sicurezza del trasporto. Questa è l'unica modalità disponibile per la sicurezza a livello named pipe remoto (ncacn \_ np). L'identità del chiamante viene salvata durante la prima chiamata di procedura remota su tale handle di associazione, non al momento della creazione dell'handle di associazione. |
| **True**              | Effective = **TRUE**; solo le impostazioni dei privilegi del token impostate su ON sono incluse nel token nel server. I privilegi impostati su OFF non possono essere attivati dal server se si usa questa opzione. I privilegi sono rilevanti solo per le chiamate RPC dello stesso computer.                                                                                                         |



 

Per altre informazioni sulle opzioni di sicurezza, [vedere Sicurezza.](security.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

Gli spazi vuoti non sono consentiti nelle associazioni di stringhe tranne quando richiesto dalla *sintassi Option.* Le impostazioni predefinite per *i campi NetworkAddress,* *Endpoint* e *Option* variano in base al valore del *membro ProtocolSequence.*

Per tutti i campi di associazione di stringhe, un singolo carattere barra rovesciata ( \\ ) viene interpretato come carattere di escape. Per specificare un singolo carattere barra rovesciata letterale, è necessario specificare due caratteri barra rovesciata ( \\ \\ ).

Un'associazione di stringhe contiene la rappresentazione di caratteri di un handle di associazione e occasionalmente parti di un handle di associazione. Le associazioni di stringhe sono utili per rappresentare parti di un handle di associazione, ma non possono essere usate per effettuare chiamate di procedura remota. Devono prima essere convertiti in un handle di associazione chiamando [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding).

Inoltre, un'associazione di stringhe non contiene tutte le informazioni di un handle di associazione. Ad esempio, le eventuali informazioni di autenticazione associate a un handle di associazione non vengono convertite nell'associazione di stringhe restituita chiamando [**RpcBindingToStringBinding.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding)

Durante lo sviluppo di un'applicazione distribuita, i server possono comunicare le informazioni di associazione ai client usando associazioni di stringa per stabilire una relazione client-server senza usare il database di mapping degli endpoint o il database name-service. Per stabilire una relazione di questo tipo, usare la funzione [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding) per convertire uno o più handle di associazione da un vettore di handle di associazione in un'associazione di stringhe e fornire l'associazione di stringhe al client.

## <a name="examples"></a>Esempio

Di seguito sono riportati esempi di associazioni di stringhe valide. In questi esempi *obj-uuid* viene usato per comodità per rappresentare un UUID valido in formato stringa. Invece di visualizzare l'UUID 308FB580-1EB2-11CA-923B-08002B1075A7, gli esempi mostrano *obj-uuid*.

``` syntax
obj-uuid@ncadg_mq:mymqserver
obj-uuid@ncacn_http:major7.microsoft.com[2225]
obj_uuid@ncacn_http:major7.microsoft.com[,HttpProxy=proxysvr:80,
    RpcProxy=websvr1.microsoft.com:80]
obj_uuid@ncacn_http:major7.microsoft.com[,HttpProxy=proxysvr:80,
    RpcProxy=websvr1.microsoft.com:80,HttpConnectOption=UseHttpProxy]
obj-uuid@ncacn_ip_tcp:16.20.16.27[2001]
obj-uuid@ncacn_ip_tcp:16.20.16.27[endpoint=2001]
obj-uuid@ncacn_nb_nb:
obj-uuid@ncacn_nb_nb:[100]
obj-uuid@ncacn_np:
obj-uuid@ncacn_np:[\\pipe\\p3,Security=impersonation static true]
obj-uuid@ncacn_np:\\\\marketing[\\pipe\\p2\\p3\\p4]
obj-uuid@ncacn_np:\\\\marketing[endpoint=\\pipe\\p2\\p3\\p4]
obj-uuid@ncacn_np:\\\\sales
obj-uuid@ncacn_np:\\\\sales[\\pipe\\p1,Security=identification dynamic true]
obj-uuid@ncalrpc:
obj-uuid@ncalrpc:[object1_name_demonstrating_that_these_can_be_lengthy]
obj-uuid@ncalrpc:[object2_name,Security=anonymous static true]
obj-uuid@ncacn_vns_spp:server@group@org[500]
obj-uuid@ncacn_dnet_nsp:took[elf_server]
obj-uuid@ncacn_dnet_nsp:took[endpoint=elf_server]
obj-uuid@ncadg_ip_udp:128.10.2.30
obj-uuid@ncadg_ip_udp:maryos.microsoft.com[1025]
obj-uuid@ncadg_ipx: ~0000000108002B30612C[5000]
obj-uuid@ncadg_ipx:printserver
obj-uuid@ncacn_spx:annaw[4390]
obj-uuid@ncacn_spx:~0000000108002B30612C
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding)
</dt> <dt>

[**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding)
</dt> <dt>

[**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister)
</dt> <dt>

[Utilizzo di HTTP come trasporto RPC](using-http-as-an-rpc-transport.md)
</dt> </dl>

 

