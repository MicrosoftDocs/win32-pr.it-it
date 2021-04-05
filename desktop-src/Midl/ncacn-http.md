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
# <a name="ncacn_http-attribute"></a><span data-ttu-id="593b8-104">\_attributo http ncacn</span><span class="sxs-lookup"><span data-stu-id="593b8-104">ncacn\_http attribute</span></span>

<span data-ttu-id="593b8-105">La parola chiave **\_ http ncacn** identifica Microsoft Internet Information Server (IIS) come famiglia di protocolli per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="593b8-105">The **ncacn\_http** keyword identifies the Microsoft Internet Information Server (IIS) as the protocol family for the endpoint.</span></span>

``` syntax
ncacn_http:rpc_server[endpoint]
```

## <a name="parameters"></a><span data-ttu-id="593b8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="593b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="593b8-107">*\_server RPC*</span><span class="sxs-lookup"><span data-stu-id="593b8-107">*rpc\_server*</span></span> 
</dt> <dd>

<span data-ttu-id="593b8-108">Indirizzo Internet o nome del computer su cui è in esecuzione il processo server RPC.</span><span class="sxs-lookup"><span data-stu-id="593b8-108">The Internet address or name of the machine that the RPC server process is running on.</span></span>

</dd> <dt>

<span data-ttu-id="593b8-109">*endpoint*</span><span class="sxs-lookup"><span data-stu-id="593b8-109">*endpoint*</span></span> 
</dt> <dd>

<span data-ttu-id="593b8-110">Porta TCP/IP nota (statica) su cui è in ascolto il processo del server RPC.</span><span class="sxs-lookup"><span data-stu-id="593b8-110">The well-known (static) TCP/IP port that the RPC server process is listening on.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="593b8-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="593b8-111">Remarks</span></span>

<span data-ttu-id="593b8-112">L'identificazione di Microsoft Internet Information Server (IIS) come famiglia di protocolli consente alle applicazioni client e server di comunicare attraverso Internet utilizzando Microsoft Internet Information Server (IIS) come proxy.</span><span class="sxs-lookup"><span data-stu-id="593b8-112">Identifying the Microsoft Internet Information Server (IIS) as the protocol family allows client and server applications to communicate across the internet by using the Microsoft Internet Information Server (IIS) as a proxy.</span></span> <span data-ttu-id="593b8-113">Poiché le chiamate vengono sottoposto a tunneling tramite una porta HTTP stabilita, possono attraversare i firewall.</span><span class="sxs-lookup"><span data-stu-id="593b8-113">Because calls are tunneled through an established HTTP port, they can cross firewalls.</span></span>

<span data-ttu-id="593b8-114">Qualsiasi applicazione client e server RPC può supportare il **protocollo \_ http ncacn** , purché siano connessi a Internet Information Server.</span><span class="sxs-lookup"><span data-stu-id="593b8-114">Any RPC client and server applications can support the **ncacn\_http** protocol as long as they are networked to an Internet Information Server.</span></span> <span data-ttu-id="593b8-115">IIS Contatta il server RPC e stabilisce un socket TCP/IP, che gestisce per il client.</span><span class="sxs-lookup"><span data-stu-id="593b8-115">The IIS contacts the RPC server and establishes a TCP/IP socket, which it maintains for the client.</span></span> <span data-ttu-id="593b8-116">IIS negozia una connessione TCP/IP con il server RPC e, una volta completata la negoziazione, funge da proxy RPC, inviando i dati tra il socket TCP/IP sul lato client e il socket TCP/IP lato server.</span><span class="sxs-lookup"><span data-stu-id="593b8-116">The IIS negotiates a TCP/IP connection with the RPC server, and once the negotiation is complete, acts as an RPC proxy, forwarding data between the client-side TCP/IP socket and the server-side TCP/IP socket.</span></span> <span data-ttu-id="593b8-117">Quando il proxy RPC IIS rileva una chiusura della sessione sul lato client o server, chiude il socket rimanente.</span><span class="sxs-lookup"><span data-stu-id="593b8-117">When the IIS RPC proxy detects a session close on either the client or the server side, it closes the remaining socket.</span></span>

<span data-ttu-id="593b8-118">L'applicazione client utilizza in modo implicito l'associazione statica a IIS, ma il server può utilizzare gli endpoint dinamici, con il RPCSS del server (mapper di endpoint) che risolve la porta del server RPC.</span><span class="sxs-lookup"><span data-stu-id="593b8-118">The client application implicitly uses static binding to the IIS, but the server can use dynamic endpoints, with the server's RPCSS (endpoint mapper) resolving the RPC server port.</span></span> <span data-ttu-id="593b8-119">Se IIS si trova in un computer diverso rispetto al server RPC, IIS riceve la chiamata remota, Contatta RPCSS sul computer server RPC per ottenere l'endpoint del processo server, quindi inoltra la chiamata al server RPC appropriato.</span><span class="sxs-lookup"><span data-stu-id="593b8-119">If the IIS is on a different machine than the RPC server, the IIS receives the remote call, contacts RPCSS on the RPC server machine to get the server process endpoint, and then forwards the call to the appropriate RPC server.</span></span>

<span data-ttu-id="593b8-120">Se Internet Explorer è installato, il trasporto controllerà il registro di sistema per verificare se è presente una configurazione per un proxy HTTP.</span><span class="sxs-lookup"><span data-stu-id="593b8-120">If Internet Explorer is installed, the transport will check the registry to see if there is a configuration for an HTTP proxy.</span></span> <span data-ttu-id="593b8-121">Se esiste un proxy, il trasporto lo utilizzerà.</span><span class="sxs-lookup"><span data-stu-id="593b8-121">If a proxy exists, the transport will use it.</span></span>

## <a name="examples"></a><span data-ttu-id="593b8-122">Esempi</span><span class="sxs-lookup"><span data-stu-id="593b8-122">Examples</span></span>

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

## <a name="see-also"></a><span data-ttu-id="593b8-123">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="593b8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="593b8-124">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="593b8-124">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="593b8-125">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="593b8-125">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="593b8-126">**Associazione stringa**</span><span class="sxs-lookup"><span data-stu-id="593b8-126">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 