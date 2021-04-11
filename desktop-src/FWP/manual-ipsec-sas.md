---
title: SA manuale
description: Lo scenario di criteri IPsec dell'associazione di sicurezza manuale consente ai chiamanti di ignorare i moduli di chiavi IPSec predefiniti (IKE e AuthIP) specificando direttamente le associazioni di sicurezza IPsec per proteggere il traffico di rete.
ms.assetid: 2bcc0b40-ca43-43c6-b1e4-b64426ef7ff4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7161447ff5cfd98878ab4ee0f4b18cbcc3a53643
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956401"
---
# <a name="manual-sa"></a><span data-ttu-id="dc296-103">SA manuale</span><span class="sxs-lookup"><span data-stu-id="dc296-103">Manual SA</span></span>

<span data-ttu-id="dc296-104">Lo scenario di criteri IPsec dell'associazione di sicurezza manuale consente ai chiamanti di ignorare i moduli di chiavi IPSec predefiniti (IKE e AuthIP) specificando direttamente le associazioni di sicurezza IPsec per proteggere il traffico di rete.</span><span class="sxs-lookup"><span data-stu-id="dc296-104">The Manual Security Association (SA) IPsec policy scenario allows callers to bypass the built-in IPsec keying modules (IKE and AuthIP) by directly specifying IPsec SAs to secure any network traffic.</span></span>

<span data-ttu-id="dc296-105">Un esempio di uno scenario SA manuale è "aggiungere una coppia di SA IPsec per proteggere il traffico dati unicast tra gli indirizzi IP 1.1.1.1 & 2.2.2.2, tranne ICMP, usando la modalità di trasporto IPsec".</span><span class="sxs-lookup"><span data-stu-id="dc296-105">An example of a possible Manual SA scenario is "Add an IPsec SA pair to secure all unicast data traffic between IP addresses 1.1.1.1 & 2.2.2.2, except ICMP, using IPsec transport mode."</span></span>

> [!Note]  
> <span data-ttu-id="dc296-106">La procedura seguente deve essere eseguita su entrambi i computer con indirizzi IP impostati in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="dc296-106">The following steps must be executed on both machines with IP addresses appropriately set.</span></span>

 

<span data-ttu-id="dc296-107">Per implementare questo esempio a livello di codice, utilizzare la seguente configurazione di Pam.</span><span class="sxs-lookup"><span data-stu-id="dc296-107">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="dc296-108">**Al \_ trasporto in ingresso FWPM layer \_ \_ \_ V {4 \| 6} Configurare le regole di filtro in ingresso per pacchetto**</span><span class="sxs-lookup"><span data-stu-id="dc296-108">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="dc296-109">Aggiungere un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="dc296-109">Add a filter with the following properties.</span></span> 
    | <span data-ttu-id="dc296-110">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="dc296-110">Filter property</span></span>                                                   | <span data-ttu-id="dc296-111">Valore</span><span class="sxs-lookup"><span data-stu-id="dc296-111">Value</span></span>                                                         |
    |-------------------------------------------------------------------|---------------------------------------------------------------|
    | <span data-ttu-id="dc296-112">**FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="dc296-112">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="dc296-113">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="dc296-113">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type) |
    | <span data-ttu-id="dc296-114">**\_ \_ \_ indirizzo IP locale \_ della condizione FWPM**</span><span class="sxs-lookup"><span data-stu-id="dc296-114">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS**</span></span>                           | <span data-ttu-id="dc296-115">Indirizzo locale appropriato (1.1.1.1 o 2.2.2.2).</span><span class="sxs-lookup"><span data-stu-id="dc296-115">The appropriate local address (1.1.1.1 or 2.2.2.2).</span></span>           |
    | <span data-ttu-id="dc296-116">**\_ \_ \_ indirizzo IP remoto \_ della condizione FWPM**</span><span class="sxs-lookup"><span data-stu-id="dc296-116">**FWPM\_CONDITION\_IP\_REMOTE\_ADDRESS**</span></span>                          | <span data-ttu-id="dc296-117">Indirizzo remoto appropriato (1.1.1.1 o 2.2.2.2).</span><span class="sxs-lookup"><span data-stu-id="dc296-117">The appropriate remote address (1.1.1.1 or 2.2.2.2).</span></span>          |
    | <span data-ttu-id="dc296-118">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="dc296-118">**action.type**</span></span>                                                   | <span data-ttu-id="dc296-119">**\_ \_ terminazione CALLOUT azione FWP \_**</span><span class="sxs-lookup"><span data-stu-id="dc296-119">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                         |
    | <span data-ttu-id="dc296-120">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="dc296-120">**action.calloutKey**</span></span>                                             | <span data-ttu-id="dc296-121">**\_Trasporto in \_ ingresso IPSec di CALLOUT FWPM \_ \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="dc296-121">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>         |

        
2.  <span data-ttu-id="dc296-122">Esentare il traffico ICMP da IPsec aggiungendo un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="dc296-122">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 
    | <span data-ttu-id="dc296-123">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="dc296-123">Filter property</span></span>                                                   | <span data-ttu-id="dc296-124">Valore</span><span class="sxs-lookup"><span data-stu-id="dc296-124">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="dc296-125">**FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="dc296-125">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="dc296-126">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="dc296-126">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="dc296-127">**FWPM \_ Condizione di filtro \_ \_ protocollo IP condizione**</span><span class="sxs-lookup"><span data-stu-id="dc296-127">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="dc296-128">**IPPROTO \_ ICMP {V6}** queste costanti sono definite in Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="dc296-128">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="dc296-129">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="dc296-129">**action.type**</span></span>                                                   | <span data-ttu-id="dc296-130">**\_permesso azione \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="dc296-130">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="dc296-131">**weight**</span><span class="sxs-lookup"><span data-stu-id="dc296-131">**weight**</span></span>                                                        | [<span data-ttu-id="dc296-132">**\_ \_ \_ esenzioni IKE per FWPM Weight Range \_**</span><span class="sxs-lookup"><span data-stu-id="dc296-132">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="dc296-133">**Al \_ trasporto in uscita FWPM layer \_ \_ \_ V {4 \| 6} Configurare le regole di filtro in uscita per pacchetto**</span><span class="sxs-lookup"><span data-stu-id="dc296-133">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="dc296-134">Aggiungere un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="dc296-134">Add a filter with the following properties.</span></span> 
    | <span data-ttu-id="dc296-135">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="dc296-135">Filter property</span></span>                                                   | <span data-ttu-id="dc296-136">Valore</span><span class="sxs-lookup"><span data-stu-id="dc296-136">Value</span></span>                                                  |
    |-------------------------------------------------------------------|--------------------------------------------------------|
    | <span data-ttu-id="dc296-137">**FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="dc296-137">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="dc296-138">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="dc296-138">NlatUnicast</span></span>                                            |
    | <span data-ttu-id="dc296-139">**FWPM \_ Condizione di filtro degli \_ \_ \_ indirizzi locali IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="dc296-139">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS** filtering condition</span></span>       | <span data-ttu-id="dc296-140">Indirizzo locale appropriato (1.1.1.1 o 2.2.2.2).</span><span class="sxs-lookup"><span data-stu-id="dc296-140">The appropriate local address (1.1.1.1 or 2.2.2.2).</span></span>    |
    | <span data-ttu-id="dc296-141">**FWPM \_ Condizione di filtro \_ \_ \_ indirizzo remoto IP condizione**</span><span class="sxs-lookup"><span data-stu-id="dc296-141">**FWPM\_CONDITION\_IP\_REMOTE\_ADDRESS** filtering condition</span></span>      | <span data-ttu-id="dc296-142">Indirizzo remoto appropriato (1.1.1.1 o 2.2.2.2).</span><span class="sxs-lookup"><span data-stu-id="dc296-142">The appropriate remote address (1.1.1.1 or 2.2.2.2).</span></span>   |
    | <span data-ttu-id="dc296-143">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="dc296-143">**action.type**</span></span>                                                   | <span data-ttu-id="dc296-144">**\_ \_ terminazione CALLOUT azione FWP \_**</span><span class="sxs-lookup"><span data-stu-id="dc296-144">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                  |
    | <span data-ttu-id="dc296-145">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="dc296-145">**action.calloutKey**</span></span>                                             | <span data-ttu-id="dc296-146">**\_Trasporto in \_ uscita IPSec di CALLOUT FWPM \_ \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="dc296-146">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span> |

        
2.  <span data-ttu-id="dc296-147">Esentare il traffico ICMP da IPsec aggiungendo un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="dc296-147">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 
    | <span data-ttu-id="dc296-148">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="dc296-148">Filter property</span></span>                                                   | <span data-ttu-id="dc296-149">Valore</span><span class="sxs-lookup"><span data-stu-id="dc296-149">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="dc296-150">**FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="dc296-150">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="dc296-151">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="dc296-151">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="dc296-152">**FWPM \_ Condizione di filtro \_ \_ protocollo IP condizione**</span><span class="sxs-lookup"><span data-stu-id="dc296-152">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="dc296-153">**IPPROTO \_ ICMP {V6}** queste costanti sono definite in Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="dc296-153">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="dc296-154">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="dc296-154">**action.type**</span></span>                                                   | <span data-ttu-id="dc296-155">**\_permesso azione \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="dc296-155">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="dc296-156">**weight**</span><span class="sxs-lookup"><span data-stu-id="dc296-156">**weight**</span></span>                                                        | <span data-ttu-id="dc296-157">**\_ \_ \_ esenzioni IKE per FWPM Weight Range \_**</span><span class="sxs-lookup"><span data-stu-id="dc296-157">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

<span data-ttu-id="dc296-158">**Configurare associazioni di sicurezza in ingresso e in uscita**</span><span class="sxs-lookup"><span data-stu-id="dc296-158">**Setup inbound and outbound security associations**</span></span>

1.  <span data-ttu-id="dc296-159">Chiamare [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)con il parametro *outboundTraffic* che contiene gli indirizzi IP come 1.1.1.1 & 2.2.2.2 e **ipsecFilterId** come LUID del filtro di callout IPSec del livello trasporto in uscita aggiunto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="dc296-159">Call [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), with the *outboundTraffic* parameter containing the IP addresses as 1.1.1.1 & 2.2.2.2, and **ipsecFilterId** as the LUID of the outbound transport layer IPsec callout filter added above.</span></span>
2.  <span data-ttu-id="dc296-160">Chiamare [**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)con il parametro *ID* contenente l'ID di contesto restituito da [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)e il parametro *getSpi* contenente gli indirizzi IP come 1.1.1.1 & 2.2.2.2 e **ipsecFilterId** come LUID del filtro di callout IPSec a livello trasporto in ingresso aggiunto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="dc296-160">Call [**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0), with the *id* parameter containing the context ID returned from [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), and the *getSpi* parameter containing the IP addresses as 1.1.1.1 & 2.2.2.2, and **ipsecFilterId** as the LUID of the inbound transport layer IPsec callout filter added above.</span></span> <span data-ttu-id="dc296-161">Il valore SPI restituito deve essere usato come SA SPI in ingresso dal computer locale e come SA in uscita dal computer remoto corrispondente.</span><span class="sxs-lookup"><span data-stu-id="dc296-161">The returned SPI value is meant to be used as the inbound SA SPI by the local machine and as the outbound SA SPI by the corresponding remote machine.</span></span> <span data-ttu-id="dc296-162">Per scambiare i valori SPI, è necessario che entrambi i computer usino un certo mezzo fuori banda.</span><span class="sxs-lookup"><span data-stu-id="dc296-162">Both machines must use some out-of-band means to exchange the SPI values.</span></span>
3.  <span data-ttu-id="dc296-163">Chiamare [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0), con il parametro *ID* contenente l'ID di contesto restituito da [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)e il parametro *INBOUNDBUNDLE* che descrive le proprietà del bundle SA in ingresso (ad esempio, l'associazione SA, il tipo di trasformazione, i tipi di algoritmo, le chiavi e così via).</span><span class="sxs-lookup"><span data-stu-id="dc296-163">Call [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0), with the *id* parameter containing the context ID returned from [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), and the *inboundBundle* parameter describing the properties of the inbound SA bundle (such as the inbound SA SPI, transform type, algorithm types, keys, etc).</span></span>
4.  <span data-ttu-id="dc296-164">Chiamare [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0), con il parametro *ID* contenente l'ID di contesto restituito da [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)e il parametro *OUTBOUNDBUNDLE* che descrive le proprietà del bundle SA in uscita (ad esempio, l'associazione SA in uscita, il tipo di trasformazione, i tipi di algoritmo, le chiavi e così via).</span><span class="sxs-lookup"><span data-stu-id="dc296-164">Call [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0), with the *id* parameter containing the context ID returned from [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), and the *outboundBundle* parameter describing the properties of the outbound SA bundle (such as the outbound SA SPI, transform type, algorithm types, keys, etc).</span></span>

  
</dl>

## <a name="related-topics"></a><span data-ttu-id="dc296-165">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dc296-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc296-166">Codice di esempio: digitazione manuale SA</span><span class="sxs-lookup"><span data-stu-id="dc296-166">Sample code: Manual SA Keying</span></span>](manual-sa-keying.md)
</dt> <dt>

[<span data-ttu-id="dc296-167">**Identificatori di callout predefiniti**</span><span class="sxs-lookup"><span data-stu-id="dc296-167">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="dc296-168">**Filtraggio degli identificatori del livello**</span><span class="sxs-lookup"><span data-stu-id="dc296-168">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="dc296-169">**\_ACTION0 FWPM**</span><span class="sxs-lookup"><span data-stu-id="dc296-169">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> </dl>

 

