---
title: attributo ncacn_spx
description: La \_ parola chiave SPX ncacn identifica SPX come la famiglia di protocolli per l'endpoint. Questa famiglia di protocolli è obsoleta e non deve essere utilizzata nelle nuove applicazioni.
ms.assetid: 45e93e25-e84d-4242-80b0-c4b61e80f716
keywords:
- attributo ncacn_spx MIDL
topic_type:
- apiref
api_name:
- ncacn_spx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09d27cc746df906ff6b1a3290e41d860c76dc362
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299766"
---
# <a name="ncacn_spx-attribute"></a><span data-ttu-id="3c292-105">ncacn \_ attributo SPX</span><span class="sxs-lookup"><span data-stu-id="3c292-105">ncacn\_spx attribute</span></span>

<span data-ttu-id="3c292-106">La parola chiave **\_ SPX ncacn** identifica SPX come la famiglia di protocolli per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="3c292-106">The **ncacn\_spx** keyword identifies SPX as the protocol family for the endpoint.</span></span> <span data-ttu-id="3c292-107">Questa famiglia di protocolli è obsoleta e non deve essere utilizzata nelle nuove applicazioni.</span><span class="sxs-lookup"><span data-stu-id="3c292-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_spx:link-address[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="3c292-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c292-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c292-109">*Indirizzo collegamento*</span><span class="sxs-lookup"><span data-stu-id="3c292-109">*link-address*</span></span> 
</dt> <dd>

<span data-ttu-id="3c292-110">Specifica il server host.</span><span class="sxs-lookup"><span data-stu-id="3c292-110">Specifies the host server.</span></span> <span data-ttu-id="3c292-111">Può trattarsi di una stringa di caratteri (il nome del server) o di un numero esadecimale di 20 cifre costituito dall'indirizzo di rete del server host (8 cifre) concatenato con l'indirizzo del nodo (12 cifre).</span><span class="sxs-lookup"><span data-stu-id="3c292-111">This may be either a character string (the server name), or a 20-digit hexadecimal number that consists of the host server's network address (8 digits) concatenated with the node address (12 digits).</span></span> <span data-ttu-id="3c292-112">Per istruzioni su come ottenere l'indirizzo di rete e l'indirizzo del nodo, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="3c292-112">See Remarks for instructions on how to obtain the network address and node address.</span></span> <span data-ttu-id="3c292-113">Una stringa **null** specifica il computer locale.</span><span class="sxs-lookup"><span data-stu-id="3c292-113">A **NULL** string specifies the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="3c292-114">*nome porta*</span><span class="sxs-lookup"><span data-stu-id="3c292-114">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="3c292-115">Specifica un numero a 16 bit facoltativo che rappresenta l'indirizzo del socket.</span><span class="sxs-lookup"><span data-stu-id="3c292-115">Specifies an optional 16-bit number that represents the socket address.</span></span> <span data-ttu-id="3c292-116">I valori possono variare da 1 a 65.535.</span><span class="sxs-lookup"><span data-stu-id="3c292-116">Values can range from 1 to 65,535.</span></span> <span data-ttu-id="3c292-117">Quando non viene specificato alcun valore, il servizio di mapping degli endpoint seleziona un valore valido per il *nome di porta* .</span><span class="sxs-lookup"><span data-stu-id="3c292-117">When no value is specified, the endpoint-mapping service selects a valid *port-name* value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3c292-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="3c292-118">Remarks</span></span>

<span data-ttu-id="3c292-119">Quando si usa il **trasporto \_ SPX ncacn** , il nome del server corrisponde esattamente al nome di Windows a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="3c292-119">When you use the **ncacn\_spx** transport, the server name is exactly the same as the 32-bit Windows name.</span></span> <span data-ttu-id="3c292-120">Tuttavia, poiché i nomi vengono distribuiti usando i protocolli Novell, devono essere conformi alle convenzioni di denominazione Novell.</span><span class="sxs-lookup"><span data-stu-id="3c292-120">However, since the names are distributed using Novell protocols, they must conform to the Novell naming conventions.</span></span> <span data-ttu-id="3c292-121">Se il nome di un server non è un nome Novell valido, i server non saranno in grado di creare endpoint con il trasporto **\_ SPX ncacn** .</span><span class="sxs-lookup"><span data-stu-id="3c292-121">If a server name is not a valid Novell name, servers will not be able to create endpoints with the **ncacn\_spx** transport.</span></span> <span data-ttu-id="3c292-122">Di seguito è riportato un elenco parziale di caratteri non consentiti nei nomi dei server Novell:</span><span class="sxs-lookup"><span data-stu-id="3c292-122">The following is a partial list of characters prohibited in Novell server names:</span></span>

<span data-ttu-id="3c292-123">" \* + .</span><span class="sxs-lookup"><span data-stu-id="3c292-123">" \* + .</span></span> <span data-ttu-id="3c292-124">/ : ; < = >?</span><span class="sxs-lookup"><span data-stu-id="3c292-124">/ : ; < = > ?</span></span> <span data-ttu-id="3c292-125">\[ \] \\ \|</span><span class="sxs-lookup"><span data-stu-id="3c292-125">\[ \] \\ \|</span></span>

<span data-ttu-id="3c292-126">Il **trasporto \_ SPX ncacn** non è supportato dalla versione di NWLink fornita con MS client 3,0.</span><span class="sxs-lookup"><span data-stu-id="3c292-126">The **ncacn\_spx** transport is not supported by the version of NWLink supplied with MS Client 3.0.</span></span>

<span data-ttu-id="3c292-127">per le applicazioni client Windows a 16 bit che usano il trasporto **ncacn \_ SPX** è necessario che il file Nwipxspx.dll sia installato per l'esecuzione nel sottosistema WOW.</span><span class="sxs-lookup"><span data-stu-id="3c292-127">16-bit Windows client applications that use the **ncacn\_spx** transport require that the file Nwipxspx.dll be installed in order to run under the WOW subsystem.</span></span> <span data-ttu-id="3c292-128">Per ottenere questo file, contattare Novell.</span><span class="sxs-lookup"><span data-stu-id="3c292-128">Contact Novell to obtain this file.</span></span>

> [!Note]  
> <span data-ttu-id="3c292-129">Per ottenere gli indirizzi di rete e di nodo, usare l'utilità **ComCheck** di Novell o l'API **IPXGetInternetAddress** definita da Novell.</span><span class="sxs-lookup"><span data-stu-id="3c292-129">To obtain the network and node addresses, use Novell's **comcheck** utility, or the Novell-defined API **IPXGetInternetAddress**.</span></span> <span data-ttu-id="3c292-130">In Windows è inoltre possibile ottenere questi indirizzi con il comando di **configurazione Ipxroute** .</span><span class="sxs-lookup"><span data-stu-id="3c292-130">On Windows, you can also obtain these addresses with the **ipxroute config** command.</span></span>

 

<span data-ttu-id="3c292-131">La sintassi della stringa della porta di trasporto SPX, come tutte le stringhe di porta, viene definita indipendentemente dalla specifica IDL.</span><span class="sxs-lookup"><span data-stu-id="3c292-131">The syntax of the SPX transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="3c292-132">Il compilatore esegue alcune verifiche della sintassi, ma non garantisce che la specifica dell'endpoint sia corretta.</span><span class="sxs-lookup"><span data-stu-id="3c292-132">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="3c292-133">È possibile che alcuni errori vengano segnalati in fase di esecuzione anziché in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="3c292-133">Some errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="3c292-134">Esempi</span><span class="sxs-lookup"><span data-stu-id="3c292-134">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_spx:[1000]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="3c292-135">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3c292-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c292-136">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="3c292-136">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="3c292-137">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="3c292-137">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="3c292-138">**ncacn \_ in \_ DSP**</span><span class="sxs-lookup"><span data-stu-id="3c292-138">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="3c292-139">**ncacn \_ DNET \_ NSP**</span><span class="sxs-lookup"><span data-stu-id="3c292-139">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="3c292-140">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="3c292-140">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="3c292-141">**ncacn \_ NB \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="3c292-141">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="3c292-142">**ncacn \_ NB \_ NB**</span><span class="sxs-lookup"><span data-stu-id="3c292-142">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="3c292-143">**ncacn \_ NB \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="3c292-143">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="3c292-144">**\_NP ncacn**</span><span class="sxs-lookup"><span data-stu-id="3c292-144">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="3c292-145">**ncacn \_ le reti virtuali \_ spp**</span><span class="sxs-lookup"><span data-stu-id="3c292-145">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="3c292-146">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="3c292-146">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="3c292-147">**ncadg \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="3c292-147">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="3c292-148">**\_UDP IP \_ ncadg**</span><span class="sxs-lookup"><span data-stu-id="3c292-148">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="3c292-149">Associazione stringa</span><span class="sxs-lookup"><span data-stu-id="3c292-149">string binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 