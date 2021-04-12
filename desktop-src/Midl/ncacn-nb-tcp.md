---
title: attributo ncacn_nb_tcp
description: La \_ \_ parola chiave ncacn NB TCP viene utilizzata per identificare TCP su NetBIOS come famiglia di protocolli per l'endpoint. Questa famiglia di protocolli è obsoleta e non deve essere utilizzata nelle nuove applicazioni.
ms.assetid: 3633842c-d1f5-46d9-866e-e54f31415ea5
keywords:
- attributo ncacn_nb_tcp MIDL
topic_type:
- apiref
api_name:
- ncacn_nb_tcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d59a544c592643cffcb282ba8a0f3fdab48c03fd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337294"
---
# <a name="ncacn_nb_tcp-attribute"></a><span data-ttu-id="58517-105">ncacn \_ NB- \_ attributo TCP</span><span class="sxs-lookup"><span data-stu-id="58517-105">ncacn\_nb\_tcp attribute</span></span>

<span data-ttu-id="58517-106">La parola chiave **ncacn \_ NB \_ TCP** viene utilizzata per identificare TCP su NetBIOS come famiglia di protocolli per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="58517-106">The **ncacn\_nb\_tcp** keyword is used to identify TCP over NetBIOS as the protocol family for the endpoint.</span></span> <span data-ttu-id="58517-107">Questa famiglia di protocolli è obsoleta e non deve essere utilizzata nelle nuove applicazioni.</span><span class="sxs-lookup"><span data-stu-id="58517-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_nb_tcp:[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="58517-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="58517-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58517-109">*nome porta*</span><span class="sxs-lookup"><span data-stu-id="58517-109">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="58517-110">Specifica un valore facoltativo a 8 bit compreso tra 1 e 254.</span><span class="sxs-lookup"><span data-stu-id="58517-110">Specifies an optional 8-bit value ranging from 1 to 254.</span></span> <span data-ttu-id="58517-111">I valori minori di 0x20 sono riservati.</span><span class="sxs-lookup"><span data-stu-id="58517-111">Values of less than 0x20 are reserved.</span></span> <span data-ttu-id="58517-112">Se non si specifica il valore di *nome porta* , il servizio di mapping degli endpoint seleziona il valore di porta.</span><span class="sxs-lookup"><span data-stu-id="58517-112">If the *port-name* value is not specified, the endpoint-mapping service selects the port value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="58517-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="58517-113">Remarks</span></span>

<span data-ttu-id="58517-114">La sintassi della stringa di porta NetBIOS, come tutte le stringhe di porta, è definita dall'implementazione del trasporto ed è indipendente dalla specifica IDL.</span><span class="sxs-lookup"><span data-stu-id="58517-114">The syntax of the NetBIOS port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="58517-115">Il compilatore MIDL esegue un controllo della sintassi limitato, ma non garantisce che la specifica dell'endpoint sia corretta.</span><span class="sxs-lookup"><span data-stu-id="58517-115">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="58517-116">Alcune classi di errori possono essere segnalate in fase di esecuzione anziché in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="58517-116">Some classes of errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="58517-117">Questa famiglia di protocolli non è supportata in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="58517-117">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="58517-118">Esempi</span><span class="sxs-lookup"><span data-stu-id="58517-118">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_nb_tcp:[100]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="58517-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="58517-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58517-120">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="58517-120">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="58517-121">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="58517-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="58517-122">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="58517-122">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="58517-123">**ncacn \_ NB \_ NB**</span><span class="sxs-lookup"><span data-stu-id="58517-123">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="58517-124">**\_NP ncacn**</span><span class="sxs-lookup"><span data-stu-id="58517-124">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="58517-125">**\_SPX ncacn**</span><span class="sxs-lookup"><span data-stu-id="58517-125">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="58517-126">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="58517-126">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="58517-127">**Associazione stringa**</span><span class="sxs-lookup"><span data-stu-id="58517-127">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 