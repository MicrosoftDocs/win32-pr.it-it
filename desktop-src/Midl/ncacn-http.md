---
title: attributo ncacn_http
description: La \_ parola chiave http ncacn identifica Microsoft Internet Information Server (IIS) come famiglia di protocolli per l'endpoint.
ms.assetid: 92d2b44c-2eab-4474-826b-ccafd26db124
keywords:
- attributo ncacn_http MIDL
topic_type:
- apiref
api_name:
- ncacn_http
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7043aaa3a011b37a4b593a03b2d74658caab6fde
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726338"
---
# <a name="ncacn_http-attribute"></a>\_attributo http ncacn

La parola chiave **\_ http ncacn** identifica Microsoft Internet Information Server (IIS) come famiglia di protocolli per l'endpoint.

``` syntax
ncacn_http:rpc_server[endpoint]
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*\_server RPC* 
</dt> <dd>

Indirizzo Internet o nome del computer su cui è in esecuzione il processo server RPC.

</dd> <dt>

*endpoint* 
</dt> <dd>

Porta TCP/IP nota (statica) su cui è in ascolto il processo del server RPC.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'identificazione di Microsoft Internet Information Server (IIS) come famiglia di protocolli consente alle applicazioni client e server di comunicare attraverso Internet utilizzando Microsoft Internet Information Server (IIS) come proxy. Poiché le chiamate vengono sottoposto a tunneling tramite una porta HTTP stabilita, possono attraversare i firewall.

Qualsiasi applicazione client e server RPC può supportare il **protocollo \_ http ncacn** , purché siano connessi a Internet Information Server. IIS Contatta il server RPC e stabilisce un socket TCP/IP, che gestisce per il client. IIS negozia una connessione TCP/IP con il server RPC e, una volta completata la negoziazione, funge da proxy RPC, inviando i dati tra il socket TCP/IP sul lato client e il socket TCP/IP lato server. Quando il proxy RPC IIS rileva una chiusura della sessione sul lato client o server, chiude il socket rimanente.

L'applicazione client utilizza in modo implicito l'associazione statica a IIS, ma il server può utilizzare gli endpoint dinamici, con il RPCSS del server (mapper di endpoint) che risolve la porta del server RPC. Se IIS si trova in un computer diverso rispetto al server RPC, IIS riceve la chiamata remota, Contatta RPCSS sul computer server RPC per ottenere l'endpoint del processo server, quindi inoltra la chiamata al server RPC appropriato.

Se Internet Explorer è installato, il trasporto controllerà il registro di sistema per verificare se è presente una configurazione per un proxy HTTP. Se esiste un proxy, il trasporto lo utilizzerà.

## <a name="examples"></a>Esempi

``` syntax
//RPC client accesses an RPC server application, which is listening on //endpoint 2225 of an IIS Web Server named major7.microsoft.com 
[   
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.0), 
    endpoint("ncacn_http:major7.microsoft.com[2225]") 
] 
interface iface
{
    // Interface definition statements.
}

//string binding format. 
//IIS Web server (websvr1)is on a different machine than the RPC
//server, and endpoints are dynamic
"obj_uuid@ncacn_http:major7.microsoft.com
    [,]"

//tells the transport to use proxysvr, port 80, as the outgoing http 
//server:
"obj_uuid@ncacn_http:major7.microsoft.com[,]"
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**endpoint**](endpoint.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Associazione stringa**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 