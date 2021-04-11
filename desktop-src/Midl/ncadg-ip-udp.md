---
title: attributo ncadg_ip_udp
description: La \_ \_ parola chiave UDP IP di ncadg identifica la versione del datagramma di TCP/IP come famiglia di protocolli per l'endpoint. Questa famiglia di protocolli è obsoleta e non deve essere utilizzata nelle nuove applicazioni.
ms.assetid: c9133fcc-6dc2-49da-9c6f-5ce3c51090d5
keywords:
- attributo ncadg_ip_udp MIDL
topic_type:
- apiref
api_name:
- ncadg_ip_udp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 173ccd0b81eb5fa7d84a6fa4d2821162b852303d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117639"
---
# <a name="ncadg_ip_udp-attribute"></a><span data-ttu-id="137a0-105">\_ \_ attributo UDP IP ncadg</span><span class="sxs-lookup"><span data-stu-id="137a0-105">ncadg\_ip\_udp attribute</span></span>

<span data-ttu-id="137a0-106">La parola chiave **\_ \_ UDP IP di ncadg** identifica la versione del datagramma di TCP/IP come famiglia di protocolli per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="137a0-106">The **ncadg\_ip\_udp** keyword identifies the datagram version of TCP/IP as the protocol family for the endpoint.</span></span> <span data-ttu-id="137a0-107">Questa famiglia di protocolli è obsoleta e non deve essere utilizzata nelle nuove applicazioni.</span><span class="sxs-lookup"><span data-stu-id="137a0-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncadg_ip_udp:server-name[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="137a0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="137a0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="137a0-109">*nome server*</span><span class="sxs-lookup"><span data-stu-id="137a0-109">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="137a0-110">Specifica il nome o l'indirizzo Internet per il server, o host, computer.</span><span class="sxs-lookup"><span data-stu-id="137a0-110">Specifies the name or internet address for the server, or host, computer.</span></span> <span data-ttu-id="137a0-111">Il nome è una stringa di caratteri e può essere un nome di dominio completo.</span><span class="sxs-lookup"><span data-stu-id="137a0-111">The name is a character string and may be a fully qualified domain name.</span></span> <span data-ttu-id="137a0-112">L'indirizzo Internet è una nota comune di indirizzo Internet.</span><span class="sxs-lookup"><span data-stu-id="137a0-112">The internet address is a common internet address notation.</span></span>

</dd> <dt>

<span data-ttu-id="137a0-113">*nome porta*</span><span class="sxs-lookup"><span data-stu-id="137a0-113">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="137a0-114">Specifica un numero facoltativo a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="137a0-114">Specifies an optional 16-bit number.</span></span> <span data-ttu-id="137a0-115">I valori minori di 1024 sono generalmente riservati.</span><span class="sxs-lookup"><span data-stu-id="137a0-115">Values of less than 1024 are usually reserved.</span></span> <span data-ttu-id="137a0-116">Se non viene specificato alcun valore, il servizio di mapping degli endpoint seleziona un valore valido per il *nome di porta* .</span><span class="sxs-lookup"><span data-stu-id="137a0-116">If no value is specified, the endpoint-mapping service selects a valid *port-name* value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="137a0-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="137a0-117">Remarks</span></span>

<span data-ttu-id="137a0-118">Si applicano le restrizioni seguenti ai protocolli di datagramma, [**ncadg \_ IPX**](ncadg-ipx.md) e **ncadg \_ IP \_ UDP**:</span><span class="sxs-lookup"><span data-stu-id="137a0-118">The following restrictions apply to the datagram protocols, [**ncadg\_ipx**](ncadg-ipx.md) and **ncadg\_ip\_udp**:</span></span>

-   <span data-ttu-id="137a0-119">Non supportano i callback.</span><span class="sxs-lookup"><span data-stu-id="137a0-119">They do not support callbacks.</span></span> <span data-ttu-id="137a0-120">Tutte le funzioni che utilizzano l'attributo di **\[** [**callback**](callback.md) **\]** avranno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="137a0-120">Any functions using the **\[**[**callback**](callback.md)**\]** attribute will fail.</span></span>
-   <span data-ttu-id="137a0-121">Non supportano l'uso del costruttore del tipo di [**pipe**](pipe.md) .</span><span class="sxs-lookup"><span data-stu-id="137a0-121">They do not support use of the [**pipe**](pipe.md) type constructor.</span></span>

<span data-ttu-id="137a0-122">La sintassi della stringa della porta di trasporto TCP/IP, come tutte le stringhe di porta, viene definita indipendentemente dalla specifica IDL.</span><span class="sxs-lookup"><span data-stu-id="137a0-122">The syntax of the TCP/IP transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="137a0-123">Il compilatore esegue alcune verifiche della sintassi, ma non garantisce che la specifica dell'endpoint sia corretta.</span><span class="sxs-lookup"><span data-stu-id="137a0-123">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="137a0-124">È possibile che alcuni errori vengano segnalati in fase di esecuzione anziché in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="137a0-124">Some errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="137a0-125">Esempi</span><span class="sxs-lookup"><span data-stu-id="137a0-125">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ip_udp:rainier[1404]") 
]
interface iface1
{
    // Interface definition statements.
}

[
    uuid(87654321-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ip_udp:128.10.2.30[1404]") 
]
interface iface2
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="137a0-126">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="137a0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="137a0-127">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="137a0-127">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="137a0-128">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="137a0-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="137a0-129">**ncacn \_ in \_ DSP**</span><span class="sxs-lookup"><span data-stu-id="137a0-129">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="137a0-130">**ncacn \_ DNET \_ NSP**</span><span class="sxs-lookup"><span data-stu-id="137a0-130">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="137a0-131">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="137a0-131">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="137a0-132">**ncacn \_ NB \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="137a0-132">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="137a0-133">**\_SPX ncacn**</span><span class="sxs-lookup"><span data-stu-id="137a0-133">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="137a0-134">**ncacn \_ NB \_ NB**</span><span class="sxs-lookup"><span data-stu-id="137a0-134">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="137a0-135">**ncacn \_ NB \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="137a0-135">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="137a0-136">**\_NP ncacn**</span><span class="sxs-lookup"><span data-stu-id="137a0-136">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="137a0-137">**ncacn \_ le reti virtuali \_ spp**</span><span class="sxs-lookup"><span data-stu-id="137a0-137">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="137a0-138">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="137a0-138">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="137a0-139">**ncadg \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="137a0-139">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="137a0-140">Associazione stringa</span><span class="sxs-lookup"><span data-stu-id="137a0-140">String Binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 