---
title: Modalità di trasporto individuazione negoziazione in modalità limite
description: La modalità trasporto per l'individuazione della negoziazione in modalità limite IPsec richiede la protezione della modalità trasporto IPsec per tutto il traffico corrispondente.
ms.assetid: 36ae74b3-30f5-49bd-8855-6f3c0fb04d70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9869be61923bff1c392c5abe2bd98099a0c3c89f
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314594"
---
# <a name="negotiation-discovery-transport-mode-in-boundary-mode"></a><span data-ttu-id="ea841-103">Modalità di trasporto individuazione negoziazione in modalità limite</span><span class="sxs-lookup"><span data-stu-id="ea841-103">Negotiation Discovery Transport Mode in Boundary Mode</span></span>

<span data-ttu-id="ea841-104">La modalità trasporto per l'individuazione della negoziazione in modalità limite IPsec richiede la protezione della modalità trasporto IPsec per tutto il traffico corrispondente.</span><span class="sxs-lookup"><span data-stu-id="ea841-104">The Negotiation Discovery Transport Mode in Boundary Mode IPsec policy scenario requests IPsec transport mode protection for all matching traffic.</span></span> <span data-ttu-id="ea841-105">Se la negoziazione IKE/AuthIP ha esito negativo, le connessioni in ingresso e in uscita possono eseguire il fallback a testo non crittografato.</span><span class="sxs-lookup"><span data-stu-id="ea841-105">If the IKE/AuthIP negotiation fails, both inbound and outbound connections are allowed to fallback to clear-text .</span></span>

<span data-ttu-id="ea841-106">Questo criterio IPsec viene in genere usato nei computer a cui è possibile accedere sia da computer che supportano IPsec che da computer non IPsec.</span><span class="sxs-lookup"><span data-stu-id="ea841-106">This IPsec policy is typically used on machines that are accessed by both IPsec capable and non-IPsec capable machines.</span></span>

<span data-ttu-id="ea841-107">Un esempio di scenario della modalità di trasporto per l'individuazione delle negoziazioni è "proteggere tutto il traffico dati unicast, tranne ICMP, usando la modalità di trasporto IPsec e abilitare l'individuazione della negoziazione in modalità limite".</span><span class="sxs-lookup"><span data-stu-id="ea841-107">An example of a potential Negotiation Discovery Transport Mode scenario is "Secure all unicast data traffic, except ICMP, using IPsec transport mode and enable negotiation discovery in boundary mode."</span></span>

<span data-ttu-id="ea841-108">Per implementare questo esempio a livello di codice, utilizzare la seguente configurazione di Pam.</span><span class="sxs-lookup"><span data-stu-id="ea841-108">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="ea841-109">**Ai \_ criteri di negoziazione FWPM layer \_ IKEEXT \_ V {4 \| 6} Setup mm**</span><span class="sxs-lookup"><span data-stu-id="ea841-109">**At FWPM\_LAYER\_IKEEXT\_V{4\|6} setup MM negotiation policy**</span></span>  

1.  <span data-ttu-id="ea841-110">Aggiungere uno o entrambi i contesti di provider di criteri MM seguenti.</span><span class="sxs-lookup"><span data-stu-id="ea841-110">Add one or both of the following MM policy provider contexts.</span></span>  
    -   <span data-ttu-id="ea841-111">Per IKE, un contesto del provider di criteri di tipo FWPM \_ IPSec \_ IKE \_ mm \_ context.</span><span class="sxs-lookup"><span data-stu-id="ea841-111">For IKE, a policy provider context of type FWPM\_IPSEC\_IKE\_MM\_CONTEXT.</span></span>
    -   <span data-ttu-id="ea841-112">Per AuthIP, un contesto del provider di criteri di tipo FWPM \_ IPSec \_ AuthIP \_ mm \_ context.</span><span class="sxs-lookup"><span data-stu-id="ea841-112">For AuthIP, a policy provider context of type FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT.</span></span>

    > [!Note]  
    > <span data-ttu-id="ea841-113">Verrà negoziato un modulo di trasparenza comune e verranno applicati i criteri di MM corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="ea841-113">A common keying module will be negotiated and the corresponding MM policy will be applied.</span></span> <span data-ttu-id="ea841-114">AuthIP è il modulo di chiavi preferito se sono supportati sia IKE che AuthIP.</span><span class="sxs-lookup"><span data-stu-id="ea841-114">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="ea841-115">Per ognuno dei contesti aggiunti nel passaggio 1, aggiungere un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="ea841-115">For each of the contexts added in step 1, add a filter with the following properties.</span></span>

    | <span data-ttu-id="ea841-116">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="ea841-116">Filter property</span></span>        | <span data-ttu-id="ea841-117">Valore</span><span class="sxs-lookup"><span data-stu-id="ea841-117">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="ea841-118">Condizioni di filtro</span><span class="sxs-lookup"><span data-stu-id="ea841-118">Filtering conditions</span></span>   | <span data-ttu-id="ea841-119">Vuoto.</span><span class="sxs-lookup"><span data-stu-id="ea841-119">Empty.</span></span> <span data-ttu-id="ea841-120">Tutto il traffico corrisponderà al filtro.</span><span class="sxs-lookup"><span data-stu-id="ea841-120">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="ea841-121">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="ea841-121">**providerContextKey**</span></span> | <span data-ttu-id="ea841-122">GUID del contesto del provider MM aggiunto nel passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="ea841-122">GUID of the MM provider context added in step 1.</span></span> |

        

<span data-ttu-id="ea841-123">**A FWPM \_ Layer \_ IPSec \_ V {4 \| 6} installazione di QM e criteri di negoziazione em**</span><span class="sxs-lookup"><span data-stu-id="ea841-123">**At FWPM\_LAYER\_IPSEC\_V{4\|6} setup QM and EM negotiation policy**</span></span>  

1.  <span data-ttu-id="ea841-124">Aggiungere uno o entrambi i contesti del provider di criteri per la modalità trasporto QM seguenti e impostare il flag del [**\_ criterio IPSec \_ \_ ND \_ limite**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) .</span><span class="sxs-lookup"><span data-stu-id="ea841-124">Add one or both of the following QM transport mode policy provider contexts and set the [**IPSEC\_POLICY\_FLAG\_ND\_BOUNDARY**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) flag.</span></span>  
    -   <span data-ttu-id="ea841-125">Per IKE, un contesto del provider di criteri di tipo **FWPM \_ IPSec \_ IKE \_ \_ trasporto \_ context**.</span><span class="sxs-lookup"><span data-stu-id="ea841-125">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_QM\_TRANSPORT\_CONTEXT**.</span></span>
    -   <span data-ttu-id="ea841-126">Per AuthIP, un contesto del provider di criteri di tipo **FWPM \_ IPSec \_ AuthIP \_ mq \_ \_ context**.</span><span class="sxs-lookup"><span data-stu-id="ea841-126">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_QM\_TRANSPORT\_CONTEXT**.</span></span> <span data-ttu-id="ea841-127">Questo contesto può facoltativamente contenere i criteri di negoziazione della modalità estesa AuthIP (EM).</span><span class="sxs-lookup"><span data-stu-id="ea841-127">This context can optionally contain the AuthIP Extended Mode (EM) negotiation policy.</span></span>

    > [!Note]  
    > <span data-ttu-id="ea841-128">Verrà negoziato un modulo di trasparenza comune e verranno applicati i criteri di QM corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="ea841-128">A common keying module will be negotiated and the corresponding QM policy will be applied.</span></span> <span data-ttu-id="ea841-129">AuthIP è il modulo di chiavi preferito se sono supportati sia IKE che AuthIP.</span><span class="sxs-lookup"><span data-stu-id="ea841-129">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="ea841-130">Per ognuno dei contesti aggiunti nel passaggio 1, aggiungere un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="ea841-130">For each of the contexts added in step 1, add a filter with the following properties.</span></span>

    | <span data-ttu-id="ea841-131">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="ea841-131">Filter property</span></span>        | <span data-ttu-id="ea841-132">Valore</span><span class="sxs-lookup"><span data-stu-id="ea841-132">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="ea841-133">Condizioni di filtro</span><span class="sxs-lookup"><span data-stu-id="ea841-133">Filtering conditions</span></span>   | <span data-ttu-id="ea841-134">Vuoto.</span><span class="sxs-lookup"><span data-stu-id="ea841-134">Empty.</span></span> <span data-ttu-id="ea841-135">Tutto il traffico corrisponderà al filtro.</span><span class="sxs-lookup"><span data-stu-id="ea841-135">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="ea841-136">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="ea841-136">**providerContextKey**</span></span> | <span data-ttu-id="ea841-137">GUID del contesto del provider QM aggiunto nel passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="ea841-137">GUID of the QM provider context added in step 1.</span></span> |

        

<span data-ttu-id="ea841-138">**Al \_ trasporto in ingresso FWPM layer \_ \_ \_ V {4 \| 6} Configurare le regole di filtro in ingresso per pacchetto**</span><span class="sxs-lookup"><span data-stu-id="ea841-138">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="ea841-139">Aggiungere un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="ea841-139">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="ea841-140">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="ea841-140">Filter property</span></span>                                                   | <span data-ttu-id="ea841-141">Valore</span><span class="sxs-lookup"><span data-stu-id="ea841-141">Value</span></span>                                                                                              |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="ea841-142">**FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="ea841-142">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="ea841-143">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="ea841-143">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | <span data-ttu-id="ea841-144">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="ea841-144">**action.type**</span></span>                                                   | <span data-ttu-id="ea841-145">**\_ \_ terminazione CALLOUT azione FWP \_**</span><span class="sxs-lookup"><span data-stu-id="ea841-145">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                              |
    | <span data-ttu-id="ea841-146">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="ea841-146">**action.calloutKey**</span></span>                                             | <span data-ttu-id="ea841-147">**\_Trasporto in \_ ingresso IPSec di CALLOUT FWPM \_ \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="ea841-147">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                              |
    | <span data-ttu-id="ea841-148">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="ea841-148">**rawContext**</span></span>                                                    | [<span data-ttu-id="ea841-149">**sicurezza della connessione per il \_ \_ \_ \_ salvataggio permanente in ingresso IPSec \_ del contesto FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="ea841-149">**FWPM\_CONTEXT\_IPSEC\_INBOUND\_PERSIST\_CONNECTION\_SECURITY**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="ea841-150">Esentare il traffico ICMP da IPsec aggiungendo un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="ea841-150">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="ea841-151">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="ea841-151">Filter property</span></span>                                                   | <span data-ttu-id="ea841-152">Valore</span><span class="sxs-lookup"><span data-stu-id="ea841-152">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="ea841-153">**FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="ea841-153">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="ea841-154">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="ea841-154">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="ea841-155">**FWPM \_ Condizione di filtro \_ \_ protocollo IP condizione**</span><span class="sxs-lookup"><span data-stu-id="ea841-155">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="ea841-156">**IPPROTO \_ ICMP {V6}** queste costanti sono definite in Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="ea841-156">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="ea841-157">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="ea841-157">**action.type**</span></span>                                                   | <span data-ttu-id="ea841-158">\_permesso azione \_ FWP</span><span class="sxs-lookup"><span data-stu-id="ea841-158">FWP\_ACTION\_PERMIT</span></span>                                                        |
    | <span data-ttu-id="ea841-159">**weight**</span><span class="sxs-lookup"><span data-stu-id="ea841-159">**weight**</span></span>                                                        | [<span data-ttu-id="ea841-160">**\_ \_ \_ esenzioni IKE per FWPM Weight Range \_**</span><span class="sxs-lookup"><span data-stu-id="ea841-160">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="ea841-161">**Al \_ trasporto in uscita FWPM layer \_ \_ \_ V {4 \| 6} Configurare le regole di filtro in uscita per pacchetto**</span><span class="sxs-lookup"><span data-stu-id="ea841-161">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="ea841-162">Aggiungere un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="ea841-162">Add a filter with the following properties.</span></span>

    | <span data-ttu-id="ea841-163">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="ea841-163">Filter property</span></span>                                                   | <span data-ttu-id="ea841-164">Valore</span><span class="sxs-lookup"><span data-stu-id="ea841-164">Value</span></span>                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | <span data-ttu-id="ea841-165">**FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="ea841-165">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="ea841-166">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="ea841-166">NlatUnicast</span></span>                                                                               |
    | <span data-ttu-id="ea841-167">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="ea841-167">**action.type**</span></span>                                                   | <span data-ttu-id="ea841-168">**\_ \_ terminazione CALLOUT azione FWP \_**</span><span class="sxs-lookup"><span data-stu-id="ea841-168">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                     |
    | <span data-ttu-id="ea841-169">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="ea841-169">**action.calloutKey**</span></span>                                             | <span data-ttu-id="ea841-170">**\_Trasporto in \_ uscita IPSec di CALLOUT FWPM \_ \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="ea841-170">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                    |
    | <span data-ttu-id="ea841-171">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="ea841-171">**rawContext**</span></span>                                                    | [<span data-ttu-id="ea841-172">**\_ \_ \_ \_ individuazione negoziazioni in uscita IPSec del contesto FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="ea841-172">**FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_NEGOTIATE\_DISCOVER**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="ea841-173">Esentare il traffico ICMP da IPsec aggiungendo un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="ea841-173">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="ea841-174">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="ea841-174">Filter property</span></span>                                                   | <span data-ttu-id="ea841-175">Valore</span><span class="sxs-lookup"><span data-stu-id="ea841-175">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="ea841-176">**FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="ea841-176">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="ea841-177">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="ea841-177">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="ea841-178">**FWPM \_ Condizione di filtro \_ \_ protocollo IP condizione**</span><span class="sxs-lookup"><span data-stu-id="ea841-178">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="ea841-179">**IPPROTO \_ ICMP {V6}** queste costanti sono definite in Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="ea841-179">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="ea841-180">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="ea841-180">**action.type**</span></span>                                                   | <span data-ttu-id="ea841-181">**\_permesso azione \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="ea841-181">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="ea841-182">**weight**</span><span class="sxs-lookup"><span data-stu-id="ea841-182">**weight**</span></span>                                                        | <span data-ttu-id="ea841-183">**\_ \_ \_ esenzioni IKE per FWPM Weight Range \_**</span><span class="sxs-lookup"><span data-stu-id="ea841-183">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

</dl>

> [!Note]  
> <span data-ttu-id="ea841-184">A differenza della modalità di trasporto per l'individuazione della negoziazione, per la modalità di trasporto di individuazione della negoziazione nei criteri della modalità limite non è necessario aggiungere un filtro a **livello di FWPM \_ livello \_ ale \_ \_ ricezione \_ accetta \_ V {4 \| 6}** livelli perché questo criterio consente connessioni non protette in ingresso non protette.</span><span class="sxs-lookup"><span data-stu-id="ea841-184">As opposed to Negotiation Discovery Transport Mode, for Negotiation Discovery Transport Mode in Boundary Mode policy there is no need to add a filter at the **FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}** layers because this policy allows inbound unprotected clear-text connections.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ea841-185">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ea841-185">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea841-186">Codice di esempio: utilizzo della modalità di trasporto</span><span class="sxs-lookup"><span data-stu-id="ea841-186">Sample code: Using Transport Mode</span></span>](using-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="ea841-187">Livelli ALE</span><span class="sxs-lookup"><span data-stu-id="ea841-187">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="ea841-188">**Identificatori di callout predefiniti**</span><span class="sxs-lookup"><span data-stu-id="ea841-188">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="ea841-189">Condizioni di filtro</span><span class="sxs-lookup"><span data-stu-id="ea841-189">Filtering Conditions</span></span>](filtering-conditions.md)
</dt> <dt>

[<span data-ttu-id="ea841-190">**Filtraggio degli identificatori del livello**</span><span class="sxs-lookup"><span data-stu-id="ea841-190">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="ea841-191">**\_ACTION0 FWPM**</span><span class="sxs-lookup"><span data-stu-id="ea841-191">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[<span data-ttu-id="ea841-192">**\_tipo di \_ contesto del provider FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="ea841-192">**FWPM\_PROVIDER\_CONTEXT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

