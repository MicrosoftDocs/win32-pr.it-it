---
title: attributo ncacn_vns_spp
description: La \_ \_ parola chiave ncacn le reti virtuali spp identifica Banyan VINES SPP come famiglia di protocolli per l'endpoint. Questa famiglia di protocolli è obsoleta e non deve essere utilizzata nelle nuove applicazioni.
ms.assetid: a2aff0a6-2e7e-43e4-a180-f1ddd0456843
keywords:
- attributo ncacn_vns_spp MIDL
topic_type:
- apiref
api_name:
- ncacn_vns_spp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e72cd17ae65fbffc2cef280f15d12ba0ddbdbe
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726079"
---
# <a name="ncacn_vns_spp-attribute"></a><span data-ttu-id="b9d98-105">\_attributo ncacn le reti virtuali \_ spp</span><span class="sxs-lookup"><span data-stu-id="b9d98-105">ncacn\_vns\_spp attribute</span></span>

<span data-ttu-id="b9d98-106">La parola chiave **ncacn \_ le reti virtuali \_ spp** identifica Banyan VINES SPP come famiglia di protocolli per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="b9d98-106">The **ncacn\_vns\_spp** keyword identifies Banyan Vines SPP as the protocol family for the endpoint.</span></span> <span data-ttu-id="b9d98-107">Questa famiglia di protocolli è obsoleta e non deve essere utilizzata nelle nuove applicazioni.</span><span class="sxs-lookup"><span data-stu-id="b9d98-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_vns_spp:server-name[port-address]")
```

## <a name="parameters"></a><span data-ttu-id="b9d98-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b9d98-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9d98-109">*nome server*</span><span class="sxs-lookup"><span data-stu-id="b9d98-109">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b9d98-110">Specifica il nome StreetTalk del server.</span><span class="sxs-lookup"><span data-stu-id="b9d98-110">Specifies the StreetTalk name of the server.</span></span> <span data-ttu-id="b9d98-111">Il nome è nel formato item@group @organization .</span><span class="sxs-lookup"><span data-stu-id="b9d98-111">The name is of the form item@group@organization.</span></span> <span data-ttu-id="b9d98-112">L'elemento può contenere un massimo di 31 caratteri e il gruppo e l'organizzazione possono avere un massimo di 15 caratteri.</span><span class="sxs-lookup"><span data-stu-id="b9d98-112">The item can be up to 31 characters long and the group and organization can be up to 15 characters.</span></span>

</dd> <dt>

<span data-ttu-id="b9d98-113">*nome porta*</span><span class="sxs-lookup"><span data-stu-id="b9d98-113">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b9d98-114">Specifica una porta Banyan VINES SPP.</span><span class="sxs-lookup"><span data-stu-id="b9d98-114">Specifies a Banyan Vines SPP port.</span></span> <span data-ttu-id="b9d98-115">L'intervallo valido per gli endpoint statici è 250-511.</span><span class="sxs-lookup"><span data-stu-id="b9d98-115">The valid range for static endpoints is 250– 511.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b9d98-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="b9d98-116">Remarks</span></span>

<span data-ttu-id="b9d98-117">Per usare il protocollo di trasporto **ncacn \_ le reti virtuali \_ spp** nelle applicazioni distribuite in esecuzione su Windows 2000, è necessario installare il software Banyan Enterprise client appropriato.</span><span class="sxs-lookup"><span data-stu-id="b9d98-117">In order to use the **ncacn\_vns\_spp** transport protocol in distributed applications running on Windows 2000, the appropriate Banyan Enterprise Client software must be installed.</span></span> <span data-ttu-id="b9d98-118">Al termine dell'installazione, aprire il **Pannello di controllo**, scegliere **configurazione e Aggiungi**, quindi selezionare **servizio \| \| servizi RPC di Banyan per Banyan**.</span><span class="sxs-lookup"><span data-stu-id="b9d98-118">After installation, open **Control Panel**, choose **Configuration and Add**, then select **Service \| Banyan \| RPC services for Banyan**.</span></span> <span data-ttu-id="b9d98-119">Il supporto per i client a 16 bit richiede il software VINES appropriato.</span><span class="sxs-lookup"><span data-stu-id="b9d98-119">Support for 16-bit clients requires appropriate Vines software.</span></span> <span data-ttu-id="b9d98-120">Per ulteriori informazioni sul prodotto Enterprise Client di Banyan e sul software a 16 bit Vines, contattare Banyan.</span><span class="sxs-lookup"><span data-stu-id="b9d98-120">For more information about Banyan's Enterprise Client product and 16-bit Vines software, contact Banyan.</span></span>

<span data-ttu-id="b9d98-121">La sintassi della stringa di porta del trasporto del Banyan VINES, come tutte le stringhe di porta, viene definita indipendentemente dalla specifica IDL.</span><span class="sxs-lookup"><span data-stu-id="b9d98-121">The syntax of the Banyan Vines SPP transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="b9d98-122">Il compilatore esegue alcune verifiche della sintassi, ma non garantisce che la specifica dell'endpoint sia corretta.</span><span class="sxs-lookup"><span data-stu-id="b9d98-122">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="b9d98-123">È possibile che alcuni errori vengano segnalati in fase di esecuzione anziché in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="b9d98-123">Some errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="b9d98-124">Questa famiglia di protocolli non è supportata in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b9d98-124">This protocol family is not supported in Windows XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="b9d98-125">Esempi</span><span class="sxs-lookup"><span data-stu-id="b9d98-125">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.1), 
    endpoint("ncacn_vns_spp:printer@sdkgrp@company[260]")
]
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="b9d98-126">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b9d98-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9d98-127">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="b9d98-127">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="b9d98-128">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="b9d98-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="b9d98-129">**ncacn \_ in \_ DSP**</span><span class="sxs-lookup"><span data-stu-id="b9d98-129">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="b9d98-130">**ncacn \_ DNET \_ NSP**</span><span class="sxs-lookup"><span data-stu-id="b9d98-130">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="b9d98-131">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="b9d98-131">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="b9d98-132">**ncacn \_ NB \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="b9d98-132">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="b9d98-133">**\_SPX ncacn**</span><span class="sxs-lookup"><span data-stu-id="b9d98-133">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="b9d98-134">**ncacn \_ NB \_ NB**</span><span class="sxs-lookup"><span data-stu-id="b9d98-134">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="b9d98-135">**ncacn \_ NB \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="b9d98-135">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="b9d98-136">**\_NP ncacn**</span><span class="sxs-lookup"><span data-stu-id="b9d98-136">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="b9d98-137">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="b9d98-137">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="b9d98-138">**ncadg \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="b9d98-138">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="b9d98-139">**\_UDP IP \_ ncadg**</span><span class="sxs-lookup"><span data-stu-id="b9d98-139">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="b9d98-140">Associazione stringa</span><span class="sxs-lookup"><span data-stu-id="b9d98-140">string binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 