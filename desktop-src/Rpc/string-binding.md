---
title: Associazione stringa
description: Il binding di stringa è una stringa di caratteri senza segno composta da stringhe che rappresentano l'UUID dell'oggetto di binding, la sequenza del protocollo RPC, l'indirizzo di rete e le opzioni endpoint ed endpoint.
ms.assetid: 5e55ddd0-d71c-42ef-90cc-dd1f0b9ed305
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d804fe614185b054b8041e13069e900501342a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399507"
---
# <a name="string-binding"></a>Associazione stringa

Il binding di stringa è una stringa di caratteri senza segno composta da stringhe che rappresentano l'UUID dell'oggetto di binding, la sequenza del protocollo RPC, l'indirizzo di rete e le opzioni endpoint ed endpoint.

*ObjectUUID* @ *ProtocolSequence*:*networkAddress* \[ *endpoint*,*opzione*\]

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="ObjectUUID"></span><span id="objectuuid"></span><span id="OBJECTUUID"></span>*ObjectUUID*
</dt> <dd>

[UUID](/windows/desktop/Midl/uuid) dell'oggetto utilizzato dalla chiamata RPC. Nel server la libreria di runtime RPC esegue il mapping del tipo di oggetto a un vettore del punto di ingresso di gestione (una matrice di puntatori a funzione) per richiamare la routine di gestione corretta. Per informazioni su come eseguire il mapping degli UUID degli oggetti a vettori di punti di ingresso di gestione, vedere [registrazione di interfacce](registering-interfaces.md).

</dd> <dt>

<span id="ProtocolSequence"></span><span id="protocolsequence"></span><span id="PROTOCOLSEQUENCE"></span>*ProtocolSequence*
</dt> <dd>

Stringa di caratteri che rappresenta una combinazione valida di un protocollo RPC (ad esempio ncacn), un protocollo di trasporto (ad esempio TCP) e un protocollo di rete (ad esempio IP). Microsoft RPC supporta i protocolli seguenti specificati nelle [costanti della sequenza del protocollo](protocol-sequence-constants.md).

</dd> <dt>

<span id="NetworkAddress"></span><span id="networkaddress"></span><span id="NETWORKADDRESS"></span>*NetworkAddress*
</dt> <dd>

Indirizzo di rete del sistema per la ricezione di chiamate a procedure remote.

> [!Note]  
> Le sequenze di protocollo seguenti non sono supportate a partire da Windows XP:

 

-   [ncacn \_ NB \_ TCP](/windows/desktop/Midl/ncacn-nb-tcp)
-   [ncacn \_ NB \_ NB](/windows/desktop/Midl/ncacn-nb-nb)
-   [ncacn \_ NB \_ IPX](/windows/desktop/Midl/ncacn-nb-ipx)
-   [ncacn \_ DNET \_ NSP](/windows/desktop/Midl/ncacn-dnet-nsp)
-   [ncacn \_ le reti virtuali \_ spp](/windows/desktop/Midl/ncacn-vns-spp)
-   [ncadg \_ mq](/windows/desktop/Midl/ncadg-mq)
-   [ncadg \_ IPX](/windows/desktop/Midl/ncadg-ipx)

Il formato e il contenuto dell'indirizzo di rete dipendono dalla sequenza di protocolli specificata, come indicato di seguito.



| Sequenza di protocollo                       | Indirizzo di rete                                                                                                                                  | Esempio                                               |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [ncacn \_ NB \_ TCP](/windows/desktop/Midl/ncacn-nb-tcp)     | Nome computer                                                                                                                                    | MyServer                                               |
| [ncacn \_ NB \_ IPX](/windows/desktop/Midl/ncacn-nb-ipx)     | Nome computer                                                                                                                                    | MyServer                                               |
| [ncacn \_ NB \_ NB](/windows/desktop/Midl/ncacn-nb-nb)       | Nome computer                                                                                                                                    | MyServer                                               |
| [\_TCP IP \_ ncacn](/windows/desktop/Midl/ncacn-ip-tcp)     | Indirizzo Internet a quattro ottetti o nome host. Se lo stack di rete IPv6 è installato, IPv6 è completamente supportato e viene accettato anche un indirizzo IPv6. | anynode.microsoft.com 128.10.2.30                      |
| [\_NP ncacn](/windows/desktop/Midl/ncacn-np)              | Nome del server (le barre rovesciate doppie iniziali sono facoltative)                                                                                            | Server \\ \\ viene ALTROSERVER                             |
| [\_SPX ncacn](/windows/desktop/Midl/ncacn-spx)            | Indirizzo Internet IPX o nome server                                                                                                             | ~ 0000000108002B30612C MyServer                         |
| [ncacn \_ DNET \_ NSP](/windows/desktop/Midl/ncacn-dnet-nsp) | Sintassi di area e nodo                                                                                                                             | 4,120                                                  |
| [ncacn \_ in \_ DSP](/windows/desktop/Midl/ncacn-at-dsp)     | Nome del computer, seguito facoltativamente da @ e dal nome della zona AppleTalk. Il valore predefinito \* è @, ovvero la zona del client, se non è stata specificata alcuna zona                     | servername@zonename nomeserver                         |
| [ncacn \_ le reti virtuali \_ spp](/windows/desktop/Midl/ncacn-vns-spp)   | Nome del Server StreetTalk del modulo item@group@organization                                                                                       | printserver@sdkdocs@microsoft                          |
| [ncadg \_ mq](/windows/desktop/Midl/ncadg-mq)              | Nome server                                                                                                                                      | MyServer                                               |
| [\_http ncacn](/windows/desktop/Midl/ncacn-http)          | Indirizzo Internet (nome descrittivo o a quattro ottetti oppure nome del server locale                                                                       | somesvr@anywhere.commylocalsvr 128.10.2.30<br/> |
| [\_UDP IP \_ ncadg](/windows/desktop/Midl/ncadg-ip-udp)     | Indirizzo Internet a quattro ottetti o nome host                                                                                                        | anynode.microsoft.com 128.10.2.30                      |
| [ncadg \_ IPX](/windows/desktop/Midl/ncadg-ipx)            | Indirizzo Internet IPX o nome server                                                                                                             | ~ 0000000108002B30612C MyServer                         |
| [ncalrpc](/windows/desktop/Midl/ncalrpc)                 | Nome computer                                                                                                                                     | thismachine                                            |



 

Il campo indirizzo di rete è facoltativo. Quando non si specifica un indirizzo di rete, l'associazione di stringhe si riferisce all'host locale. È possibile specificare il nome del computer locale quando si usa la sequenza del protocollo **ncalrpc** , ma questa operazione non è completamente necessaria.

</dd> <dt>

<span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>*Endpoint*
</dt> <dd>

Endpoint o indirizzo del processo per la ricezione di chiamate di procedure remote. Un endpoint può essere preceduto dalla parola chiave **endpoint =**. La specifica dell'endpoint è facoltativa se il server ha registrato le associazioni con il mapper di endpoint. Vedere [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister).

Il formato e il contenuto di un endpoint dipendono dalla sequenza di protocolli specificata, come illustrato nella seguente tabella di opzioni/endpoint.

</dd> <dt>

<span id="Option"></span><span id="option"></span><span id="OPTION"></span>*Opzione*
</dt> <dd>

Opzioni specifiche del protocollo. Il campo dell'opzione non è obbligatorio. Ogni opzione è specificata da una coppia {Name, value} che usa il valore dell'opzione del *nome dell'opzione* di sintassi = . Le opzioni sono definite per ogni sequenza di protocollo, come illustrato nella tabella di opzioni/endpoint seguente.



| Sequenza di protocollo                       | Endpoint                                                                                           | Esempio             | Nome opzione                                            |
|-----------------------------------------|----------------------------------------------------------------------------------------------------|----------------------|--------------------------------------------------------|
| [ncacn \_ NB \_ TCP](/windows/desktop/Midl/ncacn-nb-tcp)     | Intero compreso tra 1 e 254. Molti valori compresi tra 0 e 32 sono riservati da Microsoft.                 | 100                  | nessuno                                                   |
| [ncacn \_ NB \_ IPX](/windows/desktop/Midl/ncacn-nb-ipx)     | (come sopra)                                                                                         | (come sopra)           | nessuno                                                   |
| [ncacn \_ NB \_ NB](/windows/desktop/Midl/ncacn-nb-nb)       | (come sopra)                                                                                         | (come sopra)           | nessuno                                                   |
| [\_TCP IP \_ ncacn](/windows/desktop/Midl/ncacn-ip-tcp)     | Numero di porta Internet.                                                                              | 1025                 | nessuno                                                   |
| [\_NP ncacn](/windows/desktop/Midl/ncacn-np)              | Named pipe. Il nome deve iniziare con " \\ \\ pipe".                                                       | \\\\\\pipeName pipe \\ | Sicurezza                                               |
| [\_SPX ncacn](/windows/desktop/Midl/ncacn-spx)            | Intero compreso tra 1 e 65535.                                                                       | 5000                 | nessuno                                                   |
| [ncacn \_ DNET \_ NSP](/windows/desktop/Midl/ncacn-dnet-nsp) | Il numero dell'oggetto della fase IV di DECnet (deve essere preceduto dal \# carattere) o il nome dell'oggetto.              | mailserver \# 17      | nessuno                                                   |
| [ncacn \_ in \_ DSP](/windows/desktop/Midl/ncacn-at-dsp)     | Una stringa di caratteri, fino a 22 byte di lunghezza.                                                           | myservicesendpoint   | nessuno                                                   |
| [ncacn \_ le reti virtuali \_ spp](/windows/desktop/Midl/ncacn-vns-spp)   | Numero di porta SPPs SPP compreso tra 250 e 511.                                                         | 500                  | nessuno                                                   |
| [ncadg \_ mq](/windows/desktop/Midl/ncadg-mq)              | Intero compreso tra 1 e 65535.                                                                       | 5000                 | nessuno                                                   |
| [\_http ncacn](/windows/desktop/Midl/ncacn-http)          | Numero di porta Internet.                                                                              | 2215                 | Nomi dei server proxy HTTP e RPC, opzione HttpConnection |
| [\_UDP IP \_ ncadg](/windows/desktop/Midl/ncadg-ip-udp)     | Numero di porta Internet.                                                                              | 1025                 | nessuno                                                   |
| [ncadg \_ IPX](/windows/desktop/Midl/ncadg-ipx)            | Intero compreso tra 1 e 65535.                                                                       | 5000                 | nessuno                                                   |
| [ncalrpc](/windows/desktop/Midl/ncalrpc)                 | Stringa che specifica il nome dell'applicazione o del servizio. La stringa non può includere caratteri barra rovesciata. | \_stampante personale          | Sicurezza                                               |



 

Il nome dell'opzione **HttpConnectionOption** , supportato per la \_ sequenza del protocollo http ncacn, accetta il valore seguente.



| Nome opzione       | Valore            |
|-------------------|------------------|
| HttpConnectOption | **UseHttpProxy** |



 

**HttpConnectionOption** consente di indirizzare il comportamento di RPC durante la creazione di connessioni HTTP. Il valore **UseHttpProxy** indica a RPC di instradare il traffico attraverso il proxy http sempre, anche quando il client dispone delle opzioni Internet impostate in Internet Explorer per ignorare il server proxy per gli indirizzi locali.  Questa opzione indica al client di connettersi in modo forzato al proxy RPC tramite il proxy http. Questo consente di velocizzare il tempo necessario per stabilire una connessione poiché ignora eventuali ritardi di ricerca del server RPC direttamente prima di usare il proxy HTTP.

Se si usa questa opzione **HttpConnectionOption** e Internet Explorer nel client non è configurato per l'uso del proxy http, le connessioni potrebbero non riuscire con le **Opzioni di rete RPC non \_ \_ valide \_ \_**.

``` syntax
HttpConnectOption=UseHttpProxy
```

Per ulteriori informazioni su **HttpConnectionOption**, vedere [utilizzo di http come trasporto RPC](using-http-as-an-rpc-transport.md).

Il nome dell'opzione di **sicurezza** , supportato per le sequenze di protocollo ncalrpc, ncacn \_ NP, ncadg \_ IP \_ UDP e ncadg \_ IPX, accetta i valori di opzione seguenti.



| Nome opzione  | Valore opzione                                                                               |
|--------------|--------------------------------------------------------------------------------------------|
| **Sicurezza** | {identificazione \| anonima della \| rappresentazione} {Dynamic \| static} {**true** \| **false**} |



 

Se viene specificato il nome dell'opzione di sicurezza, è necessario fornire anche una voce di ogni set di valori di opzioni di sicurezza. I valori delle opzioni devono essere separati da un carattere a spazio singolo. Ad esempio, i campi di *Opzioni* seguenti sono validi:

``` syntax
Security=identification dynamic true
Security=impersonation static true
```

I valori delle opzioni di sicurezza hanno i significati seguenti.



| Valore dell'opzione di sicurezza | Descrizione                                                                                                                                                                                                                                                                                                                                              |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Anonima             | Il client è anonimo per il server.                                                                                                                                                                                                                                                                                                                   |
| Dynamic               | Le modifiche apportate all'identità di sicurezza del client vengono visualizzate dal server quando il server utilizza la sicurezza del trasporto. Questa è la modalità predefinita per la sicurezza a livello di trasporto LRPC (ncalrpc) e per la sicurezza a livello di trasporto named pipe locale (ncacn \_ NP).                                                                                                             |
| **False**             | Effettivo = **false**; tutte le impostazioni dei privilegi dei token, incluse quelle impostate su OFF, sono incluse nel token sul server e possono essere abilitate dal server. I privilegi sono rilevanti solo per le chiamate RPC con lo stesso computer.                                                                                                                                     |
| **Identificazione**    | Il server contiene informazioni sul client, ma non può essere rappresentato.                                                                                                                                                                                                                                                                                      |
| **Rappresentazione**     | Il server può agire per conto del client all'interno del sistema locale (la protezione a livello di trasporto non supporta la delega).                                                                                                                                                                                                                               |
| **Statico**            | Le modifiche apportate all'identità di sicurezza client non vengono visualizzate dal server quando il server utilizza la sicurezza del trasporto. Questa è l'unica modalità disponibile per la sicurezza a livello di trasporto named pipe remoto (ncacn \_ NP). L'identità del chiamante viene salvata durante la prima chiamata di procedura remota su tale handle di associazione, non al momento della creazione dell'handle di associazione. |
| **True**              | Effettivo = **true**; solo le impostazioni dei privilegi del token impostate su ON sono incluse nel token sul server. I privilegi impostati su disattivato non possono essere attivati dal server se si utilizza questa opzione. I privilegi sono rilevanti solo per le chiamate RPC con lo stesso computer.                                                                                                         |



 

Per ulteriori informazioni sulle opzioni di sicurezza, [sicurezza](security.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Gli spazi vuoti non sono consentiti nelle associazioni di stringa, tranne quando richiesto dalla sintassi dell' *opzione* . Le impostazioni predefinite per i campi *networkAddress*, *endpoint* e *Option* variano in base al valore del membro *ProtocolSequence* .

Per tutti i campi di associazione di stringhe, un singolo carattere barra rovesciata ( \) viene interpretato come carattere di escape. Per specificare un singolo carattere barra rovesciata letterale, è necessario fornire due caratteri di barra rovesciata ( \\ \) .

Un'associazione di stringa contiene la rappresentazione di caratteri di un handle di associazione e occasionalmente parti di un handle di associazione. Le associazioni di stringa sono utili per rappresentare parti di un handle di associazione, ma non possono essere usate per eseguire chiamate a procedure remote. Devono innanzitutto essere convertiti in un handle di binding chiamando [**errore in RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding).

Inoltre, un'associazione di stringa non contiene tutte le informazioni provenienti da un handle di associazione. Ad esempio, le informazioni di autenticazione, se presenti, associate a un handle di associazione non vengono convertite nell'associazione di stringa restituita dalla chiamata a [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding).

Durante lo sviluppo di un'applicazione distribuita, i server possono comunicare le informazioni di binding ai client utilizzando le associazioni di stringa per stabilire una relazione client-server senza utilizzare il database della mappa endpoint o il database del servizio nome. Per stabilire una relazione di questo tipo, usare la funzione [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding) per convertire uno o più handle di binding da un vettore di handle di associazione a un'associazione di stringa e fornire il binding di stringa al client.

## <a name="examples"></a>Esempio

Di seguito sono riportati alcuni esempi di associazioni di stringa valide. In questi esempi, *obj-UUID* viene usato per agevolare la rappresentazione di un UUID valido in formato stringa. Anziché visualizzare UUID 308FB580-1EB2-11CA-923B-08002B1075A7, gli esempi mostrano *obj-UUID*.

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

[**Errore in RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding)
</dt> <dt>

[**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding)
</dt> <dt>

[**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister)
</dt> <dt>

[Utilizzo di HTTP come trasporto RPC](using-http-as-an-rpc-transport.md)
</dt> </dl>

 

