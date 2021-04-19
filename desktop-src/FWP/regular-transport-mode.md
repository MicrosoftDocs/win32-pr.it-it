---
title: modalità di sicurezza trasporto
description: Lo scenario dei criteri IPsec in modalità trasporto richiede la protezione della modalità trasporto IPsec per tutto il traffico corrispondente.
ms.assetid: 303f7cdc-fb7a-4e5c-8291-cadcb45035cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8335854c80850e44b860530bbebab05aa3f14273
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314934"
---
# <a name="transport-mode"></a><span data-ttu-id="427e5-103">modalità di sicurezza trasporto</span><span class="sxs-lookup"><span data-stu-id="427e5-103">Transport Mode</span></span>

<span data-ttu-id="427e5-104">Lo scenario dei criteri IPsec in modalità trasporto richiede la protezione della modalità trasporto IPsec per tutto il traffico corrispondente.</span><span class="sxs-lookup"><span data-stu-id="427e5-104">The Transport Mode IPsec policy scenario requires IPsec transport mode protection for all matching traffic.</span></span> <span data-ttu-id="427e5-105">Qualsiasi traffico con testo non crittografato corrispondente viene eliminato fino a quando la negoziazione IKE o AuthIP non è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="427e5-105">Any matching clear text traffic is dropped until the IKE or AuthIP negotiation has completed successfully.</span></span> <span data-ttu-id="427e5-106">Se la negoziazione ha esito negativo, la connettività con l'indirizzo IP corrispondente rimarrà interrotta.</span><span class="sxs-lookup"><span data-stu-id="427e5-106">If the negotiation fails, connectivity with the corresponding IP address will remain broken.</span></span>

<span data-ttu-id="427e5-107">Un esempio di un possibile scenario della modalità di trasporto è "proteggere tutto il traffico dati unicast, tranne ICMP, usando la modalità di trasporto IPsec".</span><span class="sxs-lookup"><span data-stu-id="427e5-107">An example of a possible Transport Mode scenario is "Secure all unicast data traffic, except ICMP, using IPsec transport mode."</span></span>

<span data-ttu-id="427e5-108">Per implementare questo esempio a livello di codice, utilizzare la seguente configurazione di Pam.</span><span class="sxs-lookup"><span data-stu-id="427e5-108">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="427e5-109">**Ai \_ criteri di negoziazione FWPM layer \_ IKEEXT \_ V {4 \| 6} Setup mm**</span><span class="sxs-lookup"><span data-stu-id="427e5-109">**At FWPM\_LAYER\_IKEEXT\_V{4\|6} setup MM negotiation policy**</span></span>  

1.  <span data-ttu-id="427e5-110">Aggiungere uno o entrambi i contesti di provider di criteri MM seguenti.</span><span class="sxs-lookup"><span data-stu-id="427e5-110">Add one or both of the following MM policy provider contexts.</span></span>  
    -   <span data-ttu-id="427e5-111">Per IKE, un contesto del provider di criteri di tipo **FWPM \_ IPSec \_ IKE \_ mm \_ context**.</span><span class="sxs-lookup"><span data-stu-id="427e5-111">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_MM\_CONTEXT**.</span></span>
    -   <span data-ttu-id="427e5-112">Per AuthIP, un contesto del provider di criteri di tipo **FWPM \_ IPSec \_ AuthIP \_ mm \_ context**.</span><span class="sxs-lookup"><span data-stu-id="427e5-112">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT**.</span></span>

    > [!Note]  
    > <span data-ttu-id="427e5-113">Verrà negoziato un modulo di trasparenza comune e verranno applicati i criteri di MM corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="427e5-113">A common keying module will be negotiated and the corresponding MM policy will be applied.</span></span> <span data-ttu-id="427e5-114">AuthIP è il modulo di chiavi preferito se sono supportati sia IKE che AuthIP.</span><span class="sxs-lookup"><span data-stu-id="427e5-114">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="427e5-115">Per ognuno dei contesti aggiunti nel passaggio 1, aggiungere un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="427e5-115">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 

    | <span data-ttu-id="427e5-116">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="427e5-116">Filter property</span></span>        | <span data-ttu-id="427e5-117">Valore</span><span class="sxs-lookup"><span data-stu-id="427e5-117">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="427e5-118">Condizioni di filtro</span><span class="sxs-lookup"><span data-stu-id="427e5-118">Filtering conditions</span></span>   | <span data-ttu-id="427e5-119">Vuoto.</span><span class="sxs-lookup"><span data-stu-id="427e5-119">Empty.</span></span> <span data-ttu-id="427e5-120">Tutto il traffico corrisponderà al filtro.</span><span class="sxs-lookup"><span data-stu-id="427e5-120">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="427e5-121">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="427e5-121">**providerContextKey**</span></span> | <span data-ttu-id="427e5-122">GUID del contesto del provider MM aggiunto nel passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="427e5-122">GUID of the MM provider context added in step 1.</span></span> |

        

<span data-ttu-id="427e5-123">**A FWPM \_ Layer \_ IPSec \_ V {4 \| 6} installazione di QM e criteri di negoziazione em**</span><span class="sxs-lookup"><span data-stu-id="427e5-123">**At FWPM\_LAYER\_IPSEC\_V{4\|6} setup QM and EM negotiation policy**</span></span>  

1.  <span data-ttu-id="427e5-124">Aggiungere uno o entrambi i contesti del provider di criteri per la modalità di trasporto QM seguenti.</span><span class="sxs-lookup"><span data-stu-id="427e5-124">Add one or both of the following QM transport mode policy provider contexts.</span></span>  
    -   <span data-ttu-id="427e5-125">Per IKE, un contesto del provider di criteri di tipo **FWPM \_ IPSec \_ IKE \_ \_ trasporto \_ context**.</span><span class="sxs-lookup"><span data-stu-id="427e5-125">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_QM\_TRANSPORT\_CONTEXT**.</span></span>
    -   <span data-ttu-id="427e5-126">Per AuthIP, un contesto del provider di criteri di tipo **FWPM \_ IPSec \_ AuthIP \_ mq \_ \_ context**.</span><span class="sxs-lookup"><span data-stu-id="427e5-126">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_QM\_TRANSPORT\_CONTEXT**.</span></span> <span data-ttu-id="427e5-127">Questo contesto può facoltativamente contenere i criteri di negoziazione della modalità estesa AuthIP (EM).</span><span class="sxs-lookup"><span data-stu-id="427e5-127">This context can optionally contain the AuthIP Extended Mode (EM) negotiation policy.</span></span>

    > [!Note]  
    > <span data-ttu-id="427e5-128">Verrà negoziato un modulo di trasparenza comune e verranno applicati i criteri di QM corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="427e5-128">A common keying module will be negotiated and the corresponding QM policy will be applied.</span></span> <span data-ttu-id="427e5-129">AuthIP è il modulo di chiavi preferito se sono supportati sia IKE che AuthIP.</span><span class="sxs-lookup"><span data-stu-id="427e5-129">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="427e5-130">Per ognuno dei contesti aggiunti nel passaggio 1, aggiungere un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="427e5-130">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 

    | <span data-ttu-id="427e5-131">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="427e5-131">Filter property</span></span>        | <span data-ttu-id="427e5-132">Valore</span><span class="sxs-lookup"><span data-stu-id="427e5-132">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="427e5-133">Condizioni di filtro</span><span class="sxs-lookup"><span data-stu-id="427e5-133">Filtering conditions</span></span>   | <span data-ttu-id="427e5-134">Vuoto.</span><span class="sxs-lookup"><span data-stu-id="427e5-134">Empty.</span></span> <span data-ttu-id="427e5-135">Tutto il traffico corrisponderà al filtro.</span><span class="sxs-lookup"><span data-stu-id="427e5-135">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="427e5-136">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="427e5-136">**providerContextKey**</span></span> | <span data-ttu-id="427e5-137">GUID del contesto del provider QM aggiunto nel passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="427e5-137">GUID of the QM provider context added in step 1.</span></span> |

        

<span data-ttu-id="427e5-138">**Al \_ trasporto in ingresso FWPM layer \_ \_ \_ V {4 \| 6} Configurare le regole di filtro in ingresso per pacchetto**</span><span class="sxs-lookup"><span data-stu-id="427e5-138">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="427e5-139">Aggiungere un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="427e5-139">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="427e5-140">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="427e5-140">Filter property</span></span>                                                   | <span data-ttu-id="427e5-141">Valore</span><span class="sxs-lookup"><span data-stu-id="427e5-141">Value</span></span>                                                         |
    |-------------------------------------------------------------------|---------------------------------------------------------------|
    | <span data-ttu-id="427e5-142">**FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="427e5-142">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="427e5-143">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="427e5-143">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type) |
    | <span data-ttu-id="427e5-144">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="427e5-144">**action.type**</span></span>                                                   | <span data-ttu-id="427e5-145">\_ \_ terminazione CALLOUT azione FWP \_</span><span class="sxs-lookup"><span data-stu-id="427e5-145">FWP\_ACTION\_CALLOUT\_TERMINATING</span></span>                             |
    | <span data-ttu-id="427e5-146">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="427e5-146">**action.calloutKey**</span></span>                                             | <span data-ttu-id="427e5-147">\_Trasporto in \_ ingresso IPSec di CALLOUT FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="427e5-147">FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}</span></span>             |

        
2.  <span data-ttu-id="427e5-148">Esentare il traffico ICMP da IPsec aggiungendo un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="427e5-148">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="427e5-149">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="427e5-149">Filter property</span></span>                                                  | <span data-ttu-id="427e5-150">Valore</span><span class="sxs-lookup"><span data-stu-id="427e5-150">Value</span></span>                                                                     |
    |------------------------------------------------------------------|---------------------------------------------------------------------------|
    | <span data-ttu-id="427e5-151">**FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="427e5-151">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="427e5-152">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="427e5-152">NlatUnicast</span></span>                                                               |
    | <span data-ttu-id="427e5-153">**FWPM \_ Condizione di filtro \_ \_ protocollo IP condizione**</span><span class="sxs-lookup"><span data-stu-id="427e5-153">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>            | <span data-ttu-id="427e5-154">IPPROTO \_ ICMP {V6} queste costanti sono definite in Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="427e5-154">IPPROTO\_ICMP{V6}These constants are defined in winsock2.h.</span></span><br/>    |
    | <span data-ttu-id="427e5-155">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="427e5-155">**action.type**</span></span>                                                  | <span data-ttu-id="427e5-156">\_permesso azione \_ FWP</span><span class="sxs-lookup"><span data-stu-id="427e5-156">FWP\_ACTION\_PERMIT</span></span>                                                       |
    | <span data-ttu-id="427e5-157">**weight**</span><span class="sxs-lookup"><span data-stu-id="427e5-157">**weight**</span></span>                                                       | [<span data-ttu-id="427e5-158">**\_ \_ \_ esenzioni IKE per FWPM Weight Range \_**</span><span class="sxs-lookup"><span data-stu-id="427e5-158">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md) |

        

<span data-ttu-id="427e5-159">**Al \_ trasporto in uscita FWPM layer \_ \_ \_ V {4 \| 6} Configurare le regole di filtro in uscita per pacchetto**</span><span class="sxs-lookup"><span data-stu-id="427e5-159">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="427e5-160">Aggiungere un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="427e5-160">Add a filter with the following properties.</span></span>

    | <span data-ttu-id="427e5-161">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="427e5-161">Filter property</span></span>                                                   | <span data-ttu-id="427e5-162">Valore</span><span class="sxs-lookup"><span data-stu-id="427e5-162">Value</span></span>                                              |
    |-------------------------------------------------------------------|----------------------------------------------------|
    | <span data-ttu-id="427e5-163">**FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="427e5-163">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="427e5-164">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="427e5-164">NlatUnicast</span></span>                                        |
    | <span data-ttu-id="427e5-165">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="427e5-165">**action.type**</span></span>                                                   | <span data-ttu-id="427e5-166">**\_ \_ terminazione CALLOUT azione FWP \_**</span><span class="sxs-lookup"><span data-stu-id="427e5-166">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>              |
    | <span data-ttu-id="427e5-167">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="427e5-167">**action.calloutKey**</span></span>                                             | <span data-ttu-id="427e5-168">\_Trasporto in \_ uscita IPSec di CALLOUT FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="427e5-168">FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}</span></span> |

        
2.  <span data-ttu-id="427e5-169">Esentare il traffico ICMP da IPsec aggiungendo un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="427e5-169">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="427e5-170">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="427e5-170">Filter property</span></span>                                                   | <span data-ttu-id="427e5-171">Valore</span><span class="sxs-lookup"><span data-stu-id="427e5-171">Value</span></span>                                                                  |
    |-------------------------------------------------------------------|------------------------------------------------------------------------|
    | <span data-ttu-id="427e5-172">**FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="427e5-172">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="427e5-173">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="427e5-173">NlatUnicast</span></span>                                                            |
    | <span data-ttu-id="427e5-174">**FWPM \_ Condizione di filtro \_ \_ protocollo IP condizione**</span><span class="sxs-lookup"><span data-stu-id="427e5-174">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="427e5-175">IPPROTO \_ ICMP {V6} queste costanti sono definite in Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="427e5-175">IPPROTO\_ICMP{V6}These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="427e5-176">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="427e5-176">**action.type**</span></span>                                                   | <span data-ttu-id="427e5-177">\_permesso azione \_ FWP</span><span class="sxs-lookup"><span data-stu-id="427e5-177">FWP\_ACTION\_PERMIT</span></span>                                                    |
    | <span data-ttu-id="427e5-178">**weight**</span><span class="sxs-lookup"><span data-stu-id="427e5-178">**weight**</span></span>                                                        | <span data-ttu-id="427e5-179">\_ \_ \_ esenzioni IKE per FWPM Weight Range \_</span><span class="sxs-lookup"><span data-stu-id="427e5-179">FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS</span></span>                                   |

        

</dl>

## <a name="related-topics"></a><span data-ttu-id="427e5-180">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="427e5-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="427e5-181">Codice di esempio: utilizzo della modalità di trasporto</span><span class="sxs-lookup"><span data-stu-id="427e5-181">Sample code: Using Transport Mode</span></span>](using-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="427e5-182">**Filtraggio degli identificatori del livello**</span><span class="sxs-lookup"><span data-stu-id="427e5-182">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="427e5-183">**Tipi di contesto del provider**</span><span class="sxs-lookup"><span data-stu-id="427e5-183">**Provider Context Types**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> <dt>

[<span data-ttu-id="427e5-184">Condizioni di filtro</span><span class="sxs-lookup"><span data-stu-id="427e5-184">Filtering Conditions</span></span>](filtering-conditions.md)
</dt> <dt>

[<span data-ttu-id="427e5-185">**\_ACTION0 FWPM**</span><span class="sxs-lookup"><span data-stu-id="427e5-185">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[<span data-ttu-id="427e5-186">**Identificatori di callout predefiniti**</span><span class="sxs-lookup"><span data-stu-id="427e5-186">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> </dl>

 

