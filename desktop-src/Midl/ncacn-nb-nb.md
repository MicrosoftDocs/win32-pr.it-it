---
title: attributo ncacn_nb_nb
description: La \_ \_ parola chiave ncacn NB NB identifica NetBEUI su NetBIOS come famiglia di protocolli per l'endpoint. Questa famiglia di protocolli è obsoleta e non deve essere utilizzata nelle nuove applicazioni.
ms.assetid: 8bab2784-44ba-4356-85c1-5bd17e75d6a8
keywords:
- attributo ncacn_nb_nb MIDL
topic_type:
- apiref
api_name:
- ncacn_nb_nb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c562bb0acd546fd2c8f92a92074e599c8a505dc9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299774"
---
# <a name="ncacn_nb_nb-attribute"></a><span data-ttu-id="51f4c-105">attributo NB ncacn \_ \_</span><span class="sxs-lookup"><span data-stu-id="51f4c-105">ncacn\_nb\_nb attribute</span></span>

<span data-ttu-id="51f4c-106">La parola chiave **ncacn \_ NB \_ NB** identifica NetBEUI su NetBIOS come famiglia di protocolli per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="51f4c-106">The **ncacn\_nb\_nb** keyword identifies NetBEUI over NetBIOS as the protocol family for the endpoint.</span></span> <span data-ttu-id="51f4c-107">Questa famiglia di protocolli è obsoleta e non deve essere utilizzata nelle nuove applicazioni.</span><span class="sxs-lookup"><span data-stu-id="51f4c-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_nb_nb:[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="51f4c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="51f4c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51f4c-109">*nome porta*</span><span class="sxs-lookup"><span data-stu-id="51f4c-109">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="51f4c-110">Specifica un valore facoltativo a 8 bit compreso tra 1 e 255.</span><span class="sxs-lookup"><span data-stu-id="51f4c-110">Specifies an optional 8-bit value ranging from 1 to 255.</span></span> <span data-ttu-id="51f4c-111">I valori minori di 0x20 sono riservati.</span><span class="sxs-lookup"><span data-stu-id="51f4c-111">Values of less than 0x20 are reserved.</span></span> <span data-ttu-id="51f4c-112">Se non si specifica il valore di *nome porta* , il servizio di mapping degli endpoint seleziona il valore di porta.</span><span class="sxs-lookup"><span data-stu-id="51f4c-112">If the *port-name* value is not specified, the endpoint-mapping service selects the port value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51f4c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="51f4c-113">Remarks</span></span>

<span data-ttu-id="51f4c-114">La sintassi della stringa di porta NetBIOS, come tutte le stringhe di porta, è definita dall'implementazione del trasporto ed è indipendente dalla specifica IDL.</span><span class="sxs-lookup"><span data-stu-id="51f4c-114">The syntax of the NetBIOS port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="51f4c-115">Il compilatore MIDL esegue un controllo della sintassi limitato, ma non garantisce che la specifica dell'endpoint sia corretta.</span><span class="sxs-lookup"><span data-stu-id="51f4c-115">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="51f4c-116">Alcune classi di errori possono essere segnalate in fase di esecuzione anziché in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="51f4c-116">Some classes of errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="51f4c-117">Questa famiglia di protocolli non è supportata in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="51f4c-117">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="51f4c-118">Esempi</span><span class="sxs-lookup"><span data-stu-id="51f4c-118">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_nb_nb:[100]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="51f4c-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="51f4c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51f4c-120">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="51f4c-120">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="51f4c-121">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="51f4c-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="51f4c-122">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="51f4c-122">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="51f4c-123">**ncacn \_ NB \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="51f4c-123">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="51f4c-124">**\_NP ncacn**</span><span class="sxs-lookup"><span data-stu-id="51f4c-124">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="51f4c-125">**\_SPX ncacn**</span><span class="sxs-lookup"><span data-stu-id="51f4c-125">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="51f4c-126">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="51f4c-126">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="51f4c-127">**Associazione stringa**</span><span class="sxs-lookup"><span data-stu-id="51f4c-127">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 