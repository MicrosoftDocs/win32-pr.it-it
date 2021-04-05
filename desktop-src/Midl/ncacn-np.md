---
title: attributo ncacn_np
description: La \_ parola chiave ncacn NP identifica le named pipe come famiglia di protocolli per l'endpoint.
ms.assetid: 02961bb8-faf0-42e5-b134-dd2983e6d146
keywords:
- attributo ncacn_np MIDL
topic_type:
- apiref
api_name:
- ncacn_np
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84634e6bb5d2b634439be767ad44749291cffe11
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726735"
---
# <a name="ncacn_np-attribute"></a><span data-ttu-id="3e0b0-104">\_attributo NP ncacn</span><span class="sxs-lookup"><span data-stu-id="3e0b0-104">ncacn\_np attribute</span></span>

<span data-ttu-id="3e0b0-105">La parola chiave **ncacn \_ NP** identifica le named pipe come famiglia di protocolli per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="3e0b0-105">The **ncacn\_np** keyword identifies named pipes as the protocol family for the endpoint.</span></span>

``` syntax
endpoint("ncacn_np:server-name[\\pipe\\pipe-name]")
```

## <a name="parameters"></a><span data-ttu-id="3e0b0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3e0b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e0b0-107">*nome server*</span><span class="sxs-lookup"><span data-stu-id="3e0b0-107">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="3e0b0-108">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="3e0b0-108">Optional.</span></span> <span data-ttu-id="3e0b0-109">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="3e0b0-109">Specifies the name of the server.</span></span> <span data-ttu-id="3e0b0-110">I caratteri barra rovesciata sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="3e0b0-110">Backslash characters are optional.</span></span>

</dd> <dt>

<span data-ttu-id="3e0b0-111">*Nome pipe*</span><span class="sxs-lookup"><span data-stu-id="3e0b0-111">*pipe-name*</span></span> 
</dt> <dd>

<span data-ttu-id="3e0b0-112">Specifica un nome di pipe valido.</span><span class="sxs-lookup"><span data-stu-id="3e0b0-112">Specifies a valid pipe name.</span></span> <span data-ttu-id="3e0b0-113">Un nome di pipe valido è una stringa contenente gli identificatori separati da una barra rovesciata.</span><span class="sxs-lookup"><span data-stu-id="3e0b0-113">A valid pipe name is a string containing identifiers separated by backslash characters.</span></span> <span data-ttu-id="3e0b0-114">Il primo identificatore deve essere [**pipe**](pipe.md).</span><span class="sxs-lookup"><span data-stu-id="3e0b0-114">The first identifier must be [**pipe**](pipe.md).</span></span> <span data-ttu-id="3e0b0-115">Ogni identificatore deve essere separato da due caratteri di barra rovesciata.</span><span class="sxs-lookup"><span data-stu-id="3e0b0-115">Each identifier must be separated by two backslash characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e0b0-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="3e0b0-116">Remarks</span></span>

<span data-ttu-id="3e0b0-117">Un server crea un'istanza di un named pipe che è quindi disponibile per tutti i client.</span><span class="sxs-lookup"><span data-stu-id="3e0b0-117">A server creates an instance of a named pipe that is then available to any client.</span></span> <span data-ttu-id="3e0b0-118">Quando un client tenta di connettersi, l'istanza esistente è associata a tale client.</span><span class="sxs-lookup"><span data-stu-id="3e0b0-118">When a client attempts to connect, the existing instance is associated with that client.</span></span> <span data-ttu-id="3e0b0-119">Prima che un altro client possa connettersi, il server deve creare un'altra istanza del named pipe.</span><span class="sxs-lookup"><span data-stu-id="3e0b0-119">Before another client can connect, the server must create another instance of the named pipe.</span></span> <span data-ttu-id="3e0b0-120">Se un client tenta di eseguire l'associazione al server prima della creazione della nuova istanza, la chiamata di binding, [**errore in RpcBindingFromStringBinding**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding), potrebbe non riuscire e il server RPC del messaggio di errore è \_ \_ \_ troppo \_ occupato.</span><span class="sxs-lookup"><span data-stu-id="3e0b0-120">If a client tries to bind to the server before the new instance is created, the binding call, [**RpcBindingFromStringBinding**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding), may fail with the error message RPC\_S\_SERVER\_TOO\_BUSY.</span></span> <span data-ttu-id="3e0b0-121">Pertanto, è necessario assicurarsi che l'applicazione client gestisca il caso in cui il server è troppo occupato per accettare una connessione.</span><span class="sxs-lookup"><span data-stu-id="3e0b0-121">Therefore, you need to make sure that your client application handles the case where the server is too busy to accept a connection.</span></span> <span data-ttu-id="3e0b0-122">Il client deve riprovare automaticamente, richiedere all'utente una linea di condotta o non riuscire normalmente.</span><span class="sxs-lookup"><span data-stu-id="3e0b0-122">The client should automatically retry, prompt the user for a course of action, or fail gracefully.</span></span>

<span data-ttu-id="3e0b0-123">La sintassi della stringa della porta named pipe, come tutte le stringhe di porta, viene definita dall'implementazione del trasporto ed è indipendente dalla specifica IDL.</span><span class="sxs-lookup"><span data-stu-id="3e0b0-123">The syntax of the named-pipe port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="3e0b0-124">Il compilatore MIDL esegue un controllo della sintassi limitato, ma non garantisce che la specifica dell'endpoint sia corretta.</span><span class="sxs-lookup"><span data-stu-id="3e0b0-124">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="3e0b0-125">Alcune classi di errori possono essere segnalate in fase di esecuzione anziché in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="3e0b0-125">Some classes of errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="3e0b0-126">Esempi</span><span class="sxs-lookup"><span data-stu-id="3e0b0-126">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_np:[\\pipe\\stove\\hat]") 
] 
interface iface1
{
    // Interface definition statements.
}

[
    uuid(87654321-4000-2006-0000-20000000001b), 
    version(1.1), 
    endpoint("ncacn_np:\\\\myotherserver[\\pipe\\corncob]") 
] 
interface iface2
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="3e0b0-127">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3e0b0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e0b0-128">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="3e0b0-128">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="3e0b0-129">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="3e0b0-129">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="3e0b0-130">**ncacn \_ in \_ DSP**</span><span class="sxs-lookup"><span data-stu-id="3e0b0-130">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="3e0b0-131">**ncacn \_ DNET \_ NSP**</span><span class="sxs-lookup"><span data-stu-id="3e0b0-131">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="3e0b0-132">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="3e0b0-132">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="3e0b0-133">**ncacn \_ NB \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="3e0b0-133">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="3e0b0-134">**\_SPX ncacn**</span><span class="sxs-lookup"><span data-stu-id="3e0b0-134">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="3e0b0-135">**ncacn \_ NB \_ NB**</span><span class="sxs-lookup"><span data-stu-id="3e0b0-135">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="3e0b0-136">**ncacn \_ NB \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="3e0b0-136">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="3e0b0-137">**ncacn \_ le reti virtuali \_ spp**</span><span class="sxs-lookup"><span data-stu-id="3e0b0-137">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="3e0b0-138">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="3e0b0-138">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="3e0b0-139">**ncadg \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="3e0b0-139">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="3e0b0-140">**\_UDP IP \_ ncadg**</span><span class="sxs-lookup"><span data-stu-id="3e0b0-140">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="3e0b0-141">**Associazione stringa**</span><span class="sxs-lookup"><span data-stu-id="3e0b0-141">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 