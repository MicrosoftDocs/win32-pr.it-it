---
title: attributo ncacn_nb_ipx
description: La \_ \_ parola chiave IPX ncacn NB identifica NetBIOS su IPX come famiglia di protocolli per l'endpoint. Questa famiglia di protocolli è obsoleta e non deve essere utilizzata nelle nuove applicazioni.
ms.assetid: 641471d4-eba4-4d4a-a3fe-1e40b3751e38
keywords:
- attributo ncacn_nb_ipx MIDL
topic_type:
- apiref
api_name:
- ncacn_nb_ipx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 156b5c460c4cc8638640e7eb3500ec9a7a9fa0b0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299775"
---
# <a name="ncacn_nb_ipx-attribute"></a><span data-ttu-id="ee4a8-105">ncacn \_ NB- \_ attributo IPX</span><span class="sxs-lookup"><span data-stu-id="ee4a8-105">ncacn\_nb\_ipx attribute</span></span>

<span data-ttu-id="ee4a8-106">La parola chiave **\_ \_ IPX ncacn NB** identifica NetBIOS su IPX come famiglia di protocolli per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="ee4a8-106">The **ncacn\_nb\_ipx** keyword identifies NetBIOS over IPX as the protocol family for the endpoint.</span></span> <span data-ttu-id="ee4a8-107">Questa famiglia di protocolli è obsoleta e non deve essere utilizzata nelle nuove applicazioni.</span><span class="sxs-lookup"><span data-stu-id="ee4a8-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_nb_ipx:[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="ee4a8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ee4a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee4a8-109">*nome porta*</span><span class="sxs-lookup"><span data-stu-id="ee4a8-109">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ee4a8-110">Specifica un valore facoltativo a 8 bit compreso tra 1 e 254.</span><span class="sxs-lookup"><span data-stu-id="ee4a8-110">Specifies an optional 8-bit value ranging from 1 to 254.</span></span> <span data-ttu-id="ee4a8-111">I valori minori di 0x20 sono riservati.</span><span class="sxs-lookup"><span data-stu-id="ee4a8-111">Values of less than 0x20 are reserved.</span></span> <span data-ttu-id="ee4a8-112">Se non si specifica il valore di *nome porta* , il servizio di mapping degli endpoint seleziona il valore di porta.</span><span class="sxs-lookup"><span data-stu-id="ee4a8-112">If the *port-name* value is not specified, the endpoint-mapping service selects the port value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ee4a8-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee4a8-113">Remarks</span></span>

<span data-ttu-id="ee4a8-114">La sintassi della stringa di porta NetBIOS, come tutte le stringhe di porta, è definita dall'implementazione del trasporto ed è indipendente dalla specifica IDL.</span><span class="sxs-lookup"><span data-stu-id="ee4a8-114">The syntax of the NetBIOS port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="ee4a8-115">Il compilatore MIDL esegue un controllo della sintassi limitato, ma non garantisce che la specifica dell'endpoint sia corretta.</span><span class="sxs-lookup"><span data-stu-id="ee4a8-115">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="ee4a8-116">Alcune classi di errori possono essere segnalate in fase di esecuzione anziché in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="ee4a8-116">Some classes of errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="ee4a8-117">Questa famiglia di protocolli non è supportata in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ee4a8-117">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="ee4a8-118">Esempi</span><span class="sxs-lookup"><span data-stu-id="ee4a8-118">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_nb_ipx:[100]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="ee4a8-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ee4a8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee4a8-120">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="ee4a8-120">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="ee4a8-121">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="ee4a8-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="ee4a8-122">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="ee4a8-122">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="ee4a8-123">**ncacn \_ NB \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="ee4a8-123">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="ee4a8-124">**ncacn \_ NB \_ NB**</span><span class="sxs-lookup"><span data-stu-id="ee4a8-124">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="ee4a8-125">**ncacn \_ in \_ DSP**</span><span class="sxs-lookup"><span data-stu-id="ee4a8-125">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="ee4a8-126">**\_SPX ncacn**</span><span class="sxs-lookup"><span data-stu-id="ee4a8-126">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="ee4a8-127">**\_NP ncacn**</span><span class="sxs-lookup"><span data-stu-id="ee4a8-127">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="ee4a8-128">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="ee4a8-128">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="ee4a8-129">**\_UDP IP \_ ncadg**</span><span class="sxs-lookup"><span data-stu-id="ee4a8-129">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="ee4a8-130">**ncadg \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="ee4a8-130">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="ee4a8-131">**Associazione stringa**</span><span class="sxs-lookup"><span data-stu-id="ee4a8-131">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 