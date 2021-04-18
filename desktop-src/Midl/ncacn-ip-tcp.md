---
title: attributo ncacn_ip_tcp
description: La \_ \_ parola chiave TCP IP ncacn identifica TCP/IP come famiglia di protocolli per l'endpoint.
ms.assetid: 8142c667-9a5f-4066-a36d-1bb5ce551d21
keywords:
- attributo ncacn_ip_tcp MIDL
topic_type:
- apiref
api_name:
- ncacn_ip_tcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1adb57951e862ebcdfa6889aae170bfdf5a14f96
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299776"
---
# <a name="ncacn_ip_tcp-attribute"></a><span data-ttu-id="a4cfa-104">\_ \_ attributo TCP IP ncacn</span><span class="sxs-lookup"><span data-stu-id="a4cfa-104">ncacn\_ip\_tcp attribute</span></span>

<span data-ttu-id="a4cfa-105">La parola chiave **\_ \_ TCP IP ncacn** identifica TCP/IP come famiglia di protocolli per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="a4cfa-105">The **ncacn\_ip\_tcp** keyword identifies TCP/IP as the protocol family for the endpoint.</span></span>

``` syntax
endpoint("ncacn_ip_tcp:server-name[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="a4cfa-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a4cfa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4cfa-107">*nome server*</span><span class="sxs-lookup"><span data-stu-id="a4cfa-107">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a4cfa-108">Specifica il nome o l'indirizzo Internet per il server, o host, computer.</span><span class="sxs-lookup"><span data-stu-id="a4cfa-108">Specifies the name or Internet address for the server, or host, computer.</span></span> <span data-ttu-id="a4cfa-109">Il nome è una stringa di caratteri.</span><span class="sxs-lookup"><span data-stu-id="a4cfa-109">The name is a character string.</span></span> <span data-ttu-id="a4cfa-110">L'indirizzo Internet è una nota comune di indirizzo Internet.</span><span class="sxs-lookup"><span data-stu-id="a4cfa-110">The Internet address is a common Internet address notation.</span></span>

</dd> <dt>

<span data-ttu-id="a4cfa-111">*nome porta*</span><span class="sxs-lookup"><span data-stu-id="a4cfa-111">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a4cfa-112">Specifica un numero facoltativo a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="a4cfa-112">Specifies an optional 16-bit number.</span></span> <span data-ttu-id="a4cfa-113">I valori minori di 1024 sono generalmente riservati.</span><span class="sxs-lookup"><span data-stu-id="a4cfa-113">Values of less than 1024 are usually reserved.</span></span> <span data-ttu-id="a4cfa-114">Se non viene specificato alcun valore, il servizio di mapping degli endpoint seleziona un valore valido per il *nome di porta* .</span><span class="sxs-lookup"><span data-stu-id="a4cfa-114">If no value is specified, the endpoint-mapping service selects a valid *port-name* value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a4cfa-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="a4cfa-115">Remarks</span></span>

<span data-ttu-id="a4cfa-116">La sintassi della stringa della porta di trasporto TCP/IP, come tutte le stringhe di porta, viene definita indipendentemente dalla specifica IDL.</span><span class="sxs-lookup"><span data-stu-id="a4cfa-116">The syntax of the TCP/IP transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="a4cfa-117">Il compilatore esegue alcune verifiche della sintassi, ma non garantisce che la specifica dell'endpoint sia corretta.</span><span class="sxs-lookup"><span data-stu-id="a4cfa-117">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="a4cfa-118">È possibile che alcuni errori vengano segnalati in fase di esecuzione anziché in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="a4cfa-118">Some errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="a4cfa-119">Esempi</span><span class="sxs-lookup"><span data-stu-id="a4cfa-119">Examples</span></span>

``` syntax
[   
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_ip_tcp:rainier[1404]") 
]
interface iface
{
    // Interface definition statements.
}

 
endpoint("ncacn_ip_tcp:128.10.2.30[1404]")
```

## <a name="see-also"></a><span data-ttu-id="a4cfa-120">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a4cfa-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4cfa-121">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="a4cfa-121">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="a4cfa-122">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="a4cfa-122">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="a4cfa-123">**ncacn \_ NB \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="a4cfa-123">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="a4cfa-124">**\_NP ncacn**</span><span class="sxs-lookup"><span data-stu-id="a4cfa-124">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="a4cfa-125">**\_SPX ncacn**</span><span class="sxs-lookup"><span data-stu-id="a4cfa-125">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="a4cfa-126">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="a4cfa-126">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="a4cfa-127">**Associazione stringa**</span><span class="sxs-lookup"><span data-stu-id="a4cfa-127">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 