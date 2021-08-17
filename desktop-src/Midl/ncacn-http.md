---
title: ncacn_http attributo
description: La parola chiave http ncacn \_ identifica Microsoft Internet Information Server (IIS) come famiglia di protocolli per l'endpoint.
ms.assetid: 92d2b44c-2eab-4474-826b-ccafd26db124
keywords:
- ncacn_http attributo MIDL
topic_type:
- apiref
api_name:
- ncacn_http
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb7eed41849f59e497000e9ad56ae7c3166cf2d0212986fa9ba5f5ea910ed364
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642212"
---
# <a name="ncacn_http-attribute"></a>Attributo HTTP ncacn \_

La **parola chiave \_ http ncacn** identifica Microsoft Internet Information Server (IIS) come famiglia di protocolli per l'endpoint.

``` syntax
ncacn_http:rpc_server[endpoint]
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*\_server rpc* 
</dt> <dd>

Indirizzo Internet o nome del computer in cui è in esecuzione il processo del server RPC.

</dd> <dt>

*Endpoint* 
</dt> <dd>

Porta TCP/IP nota (statica) su cui è in ascolto il processo del server RPC.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'identificazione di Microsoft Internet Information Server (IIS) come famiglia di protocolli consente alle applicazioni client e server di comunicare attraverso Internet usando Microsoft Internet Information Server (IIS) come proxy. Poiché le chiamate vengono tunnelate tramite una porta HTTP stabilita, possono attraversare i firewall.

Tutte le applicazioni client e server RPC possono supportare il protocollo **\_ HTTP ncacn** purché siano in rete a Internet Information Server. IIS contatta il server RPC e stabilisce un socket TCP/IP, che gestisce per il client. IIS negozia una connessione TCP/IP con il server RPC e al termine della negoziazione funge da proxy RPC, inoltrando i dati tra il socket TCP/IP sul lato client e il socket TCP/IP sul lato server. Quando il proxy RPC IIS rileva la chiusura di una sessione sul lato client o sul lato server, chiude il socket rimanente.

L'applicazione client usa in modo implicito l'associazione statica a IIS, ma il server può usare endpoint dinamici, con RPCSS (mapper di endpoint) del server che risolve la porta del server RPC. Se IIS si trova in un computer diverso dal server RPC, IIS riceve la chiamata remota, contatta RPCSS nel computer server RPC per ottenere l'endpoint del processo server e quindi inoltra la chiamata al server RPC appropriato.

Se Internet Explorer installato, il trasporto controlla il Registro di sistema per verificare se è presente una configurazione per un proxy HTTP. Se esiste un proxy, il trasporto lo userà.

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

[**Endpoint**](endpoint.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**associazione di stringhe**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 