---
title: attributo ncadg_ipx
description: La \_ parola chiave ncadg IPX identifica IPX come famiglia di protocolli per l'endpoint. Questa famiglia di protocolli è obsoleta e non deve essere utilizzata nelle nuove applicazioni.
ms.assetid: 6b136eb9-4e18-43ff-993b-a2ad005273f1
keywords:
- attributo ncadg_ipx MIDL
topic_type:
- apiref
api_name:
- ncadg_ipx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fa206902ae80e5218e1d5249da8a8fb1b9dfc04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725378"
---
# <a name="ncadg_ipx-attribute"></a><span data-ttu-id="4187f-105">\_attributo IPX ncadg</span><span class="sxs-lookup"><span data-stu-id="4187f-105">ncadg\_ipx attribute</span></span>

<span data-ttu-id="4187f-106">La parola chiave **ncadg \_ IPX** identifica IPX come famiglia di protocolli per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="4187f-106">The **ncadg\_ipx** keyword identifies IPX as the protocol family for the endpoint.</span></span> <span data-ttu-id="4187f-107">Questa famiglia di protocolli è obsoleta e non deve essere utilizzata nelle nuove applicazioni.</span><span class="sxs-lookup"><span data-stu-id="4187f-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncadg_ipx:link-address[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="4187f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4187f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4187f-109">*Indirizzo collegamento*</span><span class="sxs-lookup"><span data-stu-id="4187f-109">*link-address*</span></span> 
</dt> <dd>

<span data-ttu-id="4187f-110">Specifica il server host.</span><span class="sxs-lookup"><span data-stu-id="4187f-110">Specifies the host server.</span></span> <span data-ttu-id="4187f-111">Può trattarsi di una stringa di caratteri (il nome del server) o di un numero esadecimale di 20 cifre costituito dall'indirizzo di rete del server host (8 cifre) concatenato con l'indirizzo del nodo (12 cifre).</span><span class="sxs-lookup"><span data-stu-id="4187f-111">This may be either a character string (the server name), or a 20-digit hexadecimal number that consists of the host server's network address (8 digits) concatenated with the node address (12 digits).</span></span> <span data-ttu-id="4187f-112">Per istruzioni su come ottenere l'indirizzo di rete e l'indirizzo del nodo, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="4187f-112">See Remarks for instructions on how to obtain the network address and node address.</span></span> <span data-ttu-id="4187f-113">Una stringa **null** specifica il computer locale.</span><span class="sxs-lookup"><span data-stu-id="4187f-113">A **NULL** string specifies the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="4187f-114">*nome porta*</span><span class="sxs-lookup"><span data-stu-id="4187f-114">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="4187f-115">Specifica un numero a 16 bit facoltativo che rappresenta l'indirizzo del socket.</span><span class="sxs-lookup"><span data-stu-id="4187f-115">Specifies an optional 16-bit number that represents the socket address.</span></span> <span data-ttu-id="4187f-116">I valori possono variare da 1 a 65535.</span><span class="sxs-lookup"><span data-stu-id="4187f-116">Values can range from 1 to 65535.</span></span> <span data-ttu-id="4187f-117">Quando non viene specificato alcun valore, il servizio di mapping degli endpoint seleziona un valore valido per il *nome di porta* .</span><span class="sxs-lookup"><span data-stu-id="4187f-117">When no value is specified, the endpoint-mapping service selects a valid *port-name* value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4187f-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="4187f-118">Remarks</span></span>

<span data-ttu-id="4187f-119">Si applicano le restrizioni seguenti ai protocolli di datagramma, **ncadg \_ IPX** e [**ncadg \_ IP \_ UDP**](ncadg-ip-udp.md):</span><span class="sxs-lookup"><span data-stu-id="4187f-119">The following restrictions apply to the datagram protocols, **ncadg\_ipx** and [**ncadg\_ip\_udp**](ncadg-ip-udp.md):</span></span>

-   <span data-ttu-id="4187f-120">Non supportano i callback.</span><span class="sxs-lookup"><span data-stu-id="4187f-120">They do not support callbacks.</span></span> <span data-ttu-id="4187f-121">Tutte le funzioni che utilizzano l'attributo di **\[** [**callback**](callback.md) **\]** avranno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="4187f-121">Any functions using the **\[**[**callback**](callback.md)**\]** attribute will fail.</span></span>
-   <span data-ttu-id="4187f-122">Non supportano l'uso del costruttore del tipo di [**pipe**](pipe.md) .</span><span class="sxs-lookup"><span data-stu-id="4187f-122">They do not support use of the [**pipe**](pipe.md) type constructor.</span></span>

<span data-ttu-id="4187f-123">Quando si utilizza il trasporto **\_ IPX ncadg** , il nome del server è esattamente uguale al nome del server Windows a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="4187f-123">When using the **ncadg\_ipx** transport, the server name is exactly the same as the 32-bit Windows server name.</span></span> <span data-ttu-id="4187f-124">Tuttavia, poiché i nomi vengono distribuiti usando i protocolli Novell, devono essere conformi alle convenzioni di denominazione Novell.</span><span class="sxs-lookup"><span data-stu-id="4187f-124">However, since the names are distributed using Novell protocols, they must conform to the Novell naming conventions.</span></span> <span data-ttu-id="4187f-125">Se il nome di un server non è un nome Novell valido, i server non saranno in grado di creare endpoint con il trasporto **\_ IPX ncadg** .</span><span class="sxs-lookup"><span data-stu-id="4187f-125">If a server name is not a valid Novell name, servers will not be able to create endpoints with the **ncadg\_ipx** transport.</span></span> <span data-ttu-id="4187f-126">Di seguito è riportato un elenco parziale di caratteri non consentiti nei nomi dei server Novell:</span><span class="sxs-lookup"><span data-stu-id="4187f-126">The following is a partial list of characters prohibited in Novell server names:</span></span>

<span data-ttu-id="4187f-127">" \* + .</span><span class="sxs-lookup"><span data-stu-id="4187f-127">" \* + .</span></span> <span data-ttu-id="4187f-128">/ : ; < = >?</span><span class="sxs-lookup"><span data-stu-id="4187f-128">/ : ; < = > ?</span></span> <span data-ttu-id="4187f-129">\[ \] \\ \|</span><span class="sxs-lookup"><span data-stu-id="4187f-129">\[ \] \\ \|</span></span>

<span data-ttu-id="4187f-130">Il **trasporto \_ IPX ncadg** è supportato dalla versione di NWLink fornita con MS client 3,0.</span><span class="sxs-lookup"><span data-stu-id="4187f-130">The **ncadg\_ipx** transport is supported by the version of NWLink supplied with MS Client 3.0.</span></span>

<span data-ttu-id="4187f-131">per le applicazioni client Windows a 16 bit che usano il trasporto **\_ IPX ncadg** è necessario che il file Nwipxspx.dll sia installato per l'esecuzione nel sottosistema WOW.</span><span class="sxs-lookup"><span data-stu-id="4187f-131">16-bit Windows client applications that use the **ncadg\_ipx** transport require that the file Nwipxspx.dll be installed in order to run under the WOW subsystem.</span></span> <span data-ttu-id="4187f-132">Per ottenere questo file, contattare Novell.</span><span class="sxs-lookup"><span data-stu-id="4187f-132">Contact Novell to obtain this file.</span></span>

<span data-ttu-id="4187f-133">Per ottenere gli indirizzi di rete e di nodo, usare l'utilità **ComCheck** di Novell o l'API **IPXGetInternetAddress** definita da Novell.</span><span class="sxs-lookup"><span data-stu-id="4187f-133">To obtain the network and node addresses, use Novell's **comcheck** utility, or the Novell-defined API **IPXGetInternetAddress**.</span></span> <span data-ttu-id="4187f-134">In Windows è inoltre possibile ottenere questi indirizzi con il comando di **configurazione Ipxroute** .</span><span class="sxs-lookup"><span data-stu-id="4187f-134">On Windows, you can also obtain these addresses with the **ipxroute config** command.</span></span>

<span data-ttu-id="4187f-135">La sintassi della stringa della porta di trasporto TCP/IP, come tutte le stringhe di porta, viene definita indipendentemente dalla specifica IDL.</span><span class="sxs-lookup"><span data-stu-id="4187f-135">The syntax of the TCP/IP transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="4187f-136">Il compilatore esegue alcune verifiche della sintassi, ma non garantisce che la specifica dell'endpoint sia corretta.</span><span class="sxs-lookup"><span data-stu-id="4187f-136">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="4187f-137">È possibile che alcuni errori vengano segnalati in fase di esecuzione anziché in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="4187f-137">Some errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="4187f-138">Questa famiglia di protocolli non è supportata in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4187f-138">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="4187f-139">Esempi</span><span class="sxs-lookup"><span data-stu-id="4187f-139">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ipx:[1000]") 
]
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="4187f-140">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="4187f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4187f-141">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="4187f-141">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="4187f-142">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="4187f-142">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="4187f-143">**ncacn \_ in \_ DSP**</span><span class="sxs-lookup"><span data-stu-id="4187f-143">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="4187f-144">**ncacn \_ DNET \_ NSP**</span><span class="sxs-lookup"><span data-stu-id="4187f-144">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="4187f-145">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="4187f-145">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="4187f-146">**ncacn \_ NB \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="4187f-146">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="4187f-147">**\_SPX ncacn**</span><span class="sxs-lookup"><span data-stu-id="4187f-147">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="4187f-148">**ncacn \_ NB \_ NB**</span><span class="sxs-lookup"><span data-stu-id="4187f-148">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="4187f-149">**ncacn \_ NB \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="4187f-149">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="4187f-150">**\_NP ncacn**</span><span class="sxs-lookup"><span data-stu-id="4187f-150">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="4187f-151">**ncacn \_ le reti virtuali \_ spp**</span><span class="sxs-lookup"><span data-stu-id="4187f-151">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="4187f-152">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="4187f-152">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="4187f-153">**\_UDP IP \_ ncadg**</span><span class="sxs-lookup"><span data-stu-id="4187f-153">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="4187f-154">Associazione stringa</span><span class="sxs-lookup"><span data-stu-id="4187f-154">string binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 