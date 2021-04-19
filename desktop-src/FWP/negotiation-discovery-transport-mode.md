---
title: Modalità trasporto individuazione negoziazione
description: Lo scenario dei criteri IPsec della modalità trasporto di individuazione negoziazione richiede la protezione della modalità trasporto IPsec per tutto il traffico in ingresso corrispondente e richiede la protezione IPsec per il traffico in uscita corrispondente.
ms.assetid: c08d9d03-7d77-43c2-8468-964b498b45f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 216fec869eca28dc0661a37d44cce3a1fd05b80a
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314814"
---
# <a name="negotiation-discovery-transport-mode"></a><span data-ttu-id="37f56-103">Modalità trasporto individuazione negoziazione</span><span class="sxs-lookup"><span data-stu-id="37f56-103">Negotiation Discovery Transport Mode</span></span>

<span data-ttu-id="37f56-104">Lo scenario dei criteri IPsec della modalità trasporto di individuazione negoziazione richiede la protezione della modalità trasporto IPsec per tutto il traffico in ingresso corrispondente e richiede la protezione IPsec per il traffico in uscita corrispondente.</span><span class="sxs-lookup"><span data-stu-id="37f56-104">The Negotiation Discovery Transport Mode IPsec policy scenario requires IPsec transport mode protection for all matching inbound traffic, and requests IPsec protection for matching outbound traffic.</span></span> <span data-ttu-id="37f56-105">Pertanto, le connessioni in uscita possono eseguire il fallback al testo non crittografato mentre le connessioni in ingresso non lo sono.</span><span class="sxs-lookup"><span data-stu-id="37f56-105">Therefore, outbound connections are allowed to fallback to clear-text while inbound connections are not.</span></span>

<span data-ttu-id="37f56-106">Con questi criteri, quando il computer host tenta una nuova connessione in uscita e non esiste una SA IPsec esistente corrispondente al traffico, l'host invia contemporaneamente i pacchetti in testo non crittografato e avvia una negoziazione IKE o AuthIP.</span><span class="sxs-lookup"><span data-stu-id="37f56-106">With this policy, when the host machine attempts a new outbound connection and there is no existing IPsec SA matching the traffic, the host simultaneously sends the packets in clear-text and starts an IKE or AuthIP negotiation.</span></span> <span data-ttu-id="37f56-107">Se la negoziazione ha esito positivo, la connessione viene aggiornata a protetta da IPsec.</span><span class="sxs-lookup"><span data-stu-id="37f56-107">If the negotiation succeeds, the connection is upgraded to IPsec-protected.</span></span> <span data-ttu-id="37f56-108">In caso contrario, la connessione rimane in testo non crittografato.</span><span class="sxs-lookup"><span data-stu-id="37f56-108">Otherwise, the connection stays in clear-text.</span></span> <span data-ttu-id="37f56-109">Una volta protetto da IPsec, una connessione non può mai essere sottoposto a downgrade a testo non crittografato.</span><span class="sxs-lookup"><span data-stu-id="37f56-109">Once IPsec-protected, a connection can never be downgraded to clear-text.</span></span>

<span data-ttu-id="37f56-110">La modalità di trasporto per l'individuazione della negoziazione viene in genere utilizzata in ambienti che includono sia computer idonei per IPsec che non IPsec.</span><span class="sxs-lookup"><span data-stu-id="37f56-110">Negotiation Discovery Transport Mode is typically used in environments that include both IPsec capable and non-IPsec capable machines.</span></span>

<span data-ttu-id="37f56-111">Un esempio di possibile scenario di modalità trasporto di individuazione negoziazione è "proteggere tutto il traffico dati unicast, tranne ICMP, usando la modalità di trasporto IPsec e abilitare l'individuazione della negoziazione".</span><span class="sxs-lookup"><span data-stu-id="37f56-111">An example of a possible Negotiation Discovery Transport Mode scenario is "Secure all unicast data traffic, except ICMP, using IPsec transport mode, and enable negotiation discovery."</span></span>

<span data-ttu-id="37f56-112">Per implementare questo esempio a livello di codice, utilizzare la seguente configurazione di Pam.</span><span class="sxs-lookup"><span data-stu-id="37f56-112">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="37f56-113">**Al \_ livello FWPM \_ IKEEXT \_ V {4 \| 6} impostare i criteri di negoziazione mm**</span><span class="sxs-lookup"><span data-stu-id="37f56-113">**At FWPM\_LAYER\_IKEEXT\_V{4\|6} set up MM negotiation policy**</span></span>  

1.  <span data-ttu-id="37f56-114">Aggiungere uno o entrambi i contesti di provider di criteri MM seguenti.</span><span class="sxs-lookup"><span data-stu-id="37f56-114">Add one or both of the following MM policy provider contexts.</span></span>  
    -   <span data-ttu-id="37f56-115">Per IKE, un contesto del provider di criteri di tipo **FWPM \_ IPSec \_ IKE \_ mm \_ context**.</span><span class="sxs-lookup"><span data-stu-id="37f56-115">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_MM\_CONTEXT**.</span></span>
    -   <span data-ttu-id="37f56-116">Per AuthIP, un contesto del provider di criteri di tipo **FWPM \_ IPSec \_ AuthIP \_ mm \_ context**.</span><span class="sxs-lookup"><span data-stu-id="37f56-116">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT**.</span></span>

    > [!Note]  
    > <span data-ttu-id="37f56-117">Verrà negoziato un modulo di trasparenza comune e verranno applicati i criteri di MM corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="37f56-117">A common keying module will be negotiated and the corresponding MM policy will be applied.</span></span> <span data-ttu-id="37f56-118">AuthIP è il modulo di chiavi preferito se sono supportati sia IKE che AuthIP.</span><span class="sxs-lookup"><span data-stu-id="37f56-118">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="37f56-119">Per ognuno dei contesti aggiunti nel passaggio 1, aggiungere un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="37f56-119">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 

    | <span data-ttu-id="37f56-120">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="37f56-120">Filter property</span></span>        | <span data-ttu-id="37f56-121">Valore</span><span class="sxs-lookup"><span data-stu-id="37f56-121">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="37f56-122">Condizioni di filtro</span><span class="sxs-lookup"><span data-stu-id="37f56-122">Filtering conditions</span></span>   | <span data-ttu-id="37f56-123">Vuoto.</span><span class="sxs-lookup"><span data-stu-id="37f56-123">Empty.</span></span> <span data-ttu-id="37f56-124">Tutto il traffico corrisponderà al filtro.</span><span class="sxs-lookup"><span data-stu-id="37f56-124">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="37f56-125">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="37f56-125">**providerContextKey**</span></span> | <span data-ttu-id="37f56-126">GUID del contesto del provider MM aggiunto nel passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="37f56-126">GUID of the MM provider context added in step 1.</span></span> |

        

<span data-ttu-id="37f56-127">**In FWPM \_ Layer \_ IPSec \_ V {4 \| 6} configurare i criteri di negoziazione di mq e em**</span><span class="sxs-lookup"><span data-stu-id="37f56-127">**At FWPM\_LAYER\_IPSEC\_V{4\|6} set up QM and EM negotiation policy**</span></span>  

1.  <span data-ttu-id="37f56-128">Aggiungere uno o entrambi i contesti del provider di criteri per la modalità di trasporto QM seguenti e impostare il flag di [**\_ criteri IPSec \_ \_ ND \_ Secure**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) flag.</span><span class="sxs-lookup"><span data-stu-id="37f56-128">Add one or both of the following QM transport mode policy provider contexts and set the [**IPSEC\_POLICY\_FLAG\_ND\_SECURE**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) flag.</span></span>  
    -   <span data-ttu-id="37f56-129">Per IKE, un contesto del provider di criteri di tipo FWPM \_ IPSec \_ IKE \_ \_ trasporto \_ context.</span><span class="sxs-lookup"><span data-stu-id="37f56-129">For IKE, a policy provider context of type FWPM\_IPSEC\_IKE\_QM\_TRANSPORT\_CONTEXT.</span></span>
    -   <span data-ttu-id="37f56-130">Per AuthIP, un contesto del provider di criteri di tipo FWPM \_ IPSec \_ AuthIP \_ mq \_ \_ context.</span><span class="sxs-lookup"><span data-stu-id="37f56-130">For AuthIP, a policy provider context of type FWPM\_IPSEC\_AUTHIP\_QM\_TRANSPORT\_CONTEXT.</span></span> <span data-ttu-id="37f56-131">Questo contesto può facoltativamente contenere i criteri di negoziazione della modalità estesa AuthIP (EM).</span><span class="sxs-lookup"><span data-stu-id="37f56-131">This context can optionally contain the AuthIP Extended Mode (EM) negotiation policy.</span></span>

    > [!Note]  
    > <span data-ttu-id="37f56-132">Verrà negoziato un modulo di trasparenza comune e verranno applicati i criteri di QM corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="37f56-132">A common keying module will be negotiated and the corresponding QM policy will be applied.</span></span> <span data-ttu-id="37f56-133">AuthIP è il modulo di chiavi preferito se sono supportati sia IKE che AuthIP.</span><span class="sxs-lookup"><span data-stu-id="37f56-133">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="37f56-134">Per ognuno dei contesti aggiunti nel passaggio 1, aggiungere un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="37f56-134">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 

    | <span data-ttu-id="37f56-135">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="37f56-135">Filter property</span></span>        | <span data-ttu-id="37f56-136">Valore</span><span class="sxs-lookup"><span data-stu-id="37f56-136">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="37f56-137">Condizioni di filtro</span><span class="sxs-lookup"><span data-stu-id="37f56-137">Filtering conditions</span></span>   | <span data-ttu-id="37f56-138">Vuoto.</span><span class="sxs-lookup"><span data-stu-id="37f56-138">Empty.</span></span> <span data-ttu-id="37f56-139">Tutto il traffico corrisponderà al filtro.</span><span class="sxs-lookup"><span data-stu-id="37f56-139">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="37f56-140">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="37f56-140">**providerContextKey**</span></span> | <span data-ttu-id="37f56-141">GUID del contesto del provider QM aggiunto nel passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="37f56-141">GUID of the QM provider context added in step 1.</span></span> |

        

<span data-ttu-id="37f56-142">**Al \_ trasporto in ingresso FWPM layer \_ \_ \_ V {4 \| 6} Configurare le regole di filtro in ingresso per pacchetto**</span><span class="sxs-lookup"><span data-stu-id="37f56-142">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} set up inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="37f56-143">Aggiungere un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="37f56-143">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="37f56-144">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="37f56-144">Filter property</span></span>                                                   | <span data-ttu-id="37f56-145">Valore</span><span class="sxs-lookup"><span data-stu-id="37f56-145">Value</span></span>                                                                                              |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="37f56-146">**FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="37f56-146">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="37f56-147">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="37f56-147">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | <span data-ttu-id="37f56-148">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="37f56-148">**action.type**</span></span>                                                   | <span data-ttu-id="37f56-149">**\_ \_ terminazione CALLOUT azione FWP \_**</span><span class="sxs-lookup"><span data-stu-id="37f56-149">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                              |
    | <span data-ttu-id="37f56-150">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="37f56-150">**action.calloutKey**</span></span>                                             | <span data-ttu-id="37f56-151">**\_Trasporto in \_ ingresso IPSec di CALLOUT FWPM \_ \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="37f56-151">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                              |
    | <span data-ttu-id="37f56-152">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="37f56-152">**rawContext**</span></span>                                                    | [<span data-ttu-id="37f56-153">**sicurezza della connessione per il \_ \_ \_ \_ salvataggio permanente in ingresso IPSec \_ del contesto FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="37f56-153">**FWPM\_CONTEXT\_IPSEC\_INBOUND\_PERSIST\_CONNECTION\_SECURITY**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="37f56-154">Esentare il traffico ICMP da IPsec aggiungendo un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="37f56-154">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="37f56-155">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="37f56-155">Filter property</span></span>                                                   | <span data-ttu-id="37f56-156">Valore</span><span class="sxs-lookup"><span data-stu-id="37f56-156">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="37f56-157">**FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="37f56-157">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="37f56-158">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="37f56-158">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="37f56-159">**FWPM \_ Condizione di filtro \_ \_ protocollo IP condizione**</span><span class="sxs-lookup"><span data-stu-id="37f56-159">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="37f56-160">**IPPROTO \_ ICMP {V6}** queste costanti sono definite in Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="37f56-160">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="37f56-161">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="37f56-161">**action.type**</span></span>                                                   | <span data-ttu-id="37f56-162">**\_permesso azione \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="37f56-162">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="37f56-163">**weight**</span><span class="sxs-lookup"><span data-stu-id="37f56-163">**weight**</span></span>                                                        | [<span data-ttu-id="37f56-164">**\_ \_ \_ esenzioni IKE per FWPM Weight Range \_**</span><span class="sxs-lookup"><span data-stu-id="37f56-164">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="37f56-165">**Al \_ trasporto in uscita FWPM layer \_ \_ \_ V {4 \| 6} Configurare le regole di filtro per pacchetto in uscita**</span><span class="sxs-lookup"><span data-stu-id="37f56-165">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} set up outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="37f56-166">Aggiungere un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="37f56-166">Add a filter with the following properties.</span></span>

    | <span data-ttu-id="37f56-167">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="37f56-167">Filter property</span></span>                                                   | <span data-ttu-id="37f56-168">Valore</span><span class="sxs-lookup"><span data-stu-id="37f56-168">Value</span></span>                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | <span data-ttu-id="37f56-169">**FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="37f56-169">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="37f56-170">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="37f56-170">NlatUnicast</span></span>                                                                               |
    | <span data-ttu-id="37f56-171">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="37f56-171">**action.type**</span></span>                                                   | <span data-ttu-id="37f56-172">**\_ \_ terminazione CALLOUT azione FWP \_**</span><span class="sxs-lookup"><span data-stu-id="37f56-172">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                     |
    | <span data-ttu-id="37f56-173">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="37f56-173">**action.calloutKey**</span></span>                                             | <span data-ttu-id="37f56-174">**\_Trasporto in \_ uscita IPSec di CALLOUT FWPM \_ \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="37f56-174">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                    |
    | <span data-ttu-id="37f56-175">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="37f56-175">**rawContext**</span></span>                                                    | [<span data-ttu-id="37f56-176">**\_ \_ \_ \_ individuazione negoziazioni in uscita IPSec del contesto FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="37f56-176">**FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_NEGOTIATE\_DISCOVER**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="37f56-177">Esentare il traffico ICMP da IPsec aggiungendo un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="37f56-177">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="37f56-178">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="37f56-178">Filter property</span></span>                                                   | <span data-ttu-id="37f56-179">Valore</span><span class="sxs-lookup"><span data-stu-id="37f56-179">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="37f56-180">**FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="37f56-180">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="37f56-181">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="37f56-181">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="37f56-182">**FWPM \_ Condizione di filtro \_ \_ protocollo IP condizione**</span><span class="sxs-lookup"><span data-stu-id="37f56-182">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="37f56-183">**IPPROTO \_ ICMP {V6}** queste costanti sono definite in Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="37f56-183">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="37f56-184">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="37f56-184">**action.type**</span></span>                                                   | <span data-ttu-id="37f56-185">**\_permesso azione \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="37f56-185">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="37f56-186">**weight**</span><span class="sxs-lookup"><span data-stu-id="37f56-186">**weight**</span></span>                                                        | <span data-ttu-id="37f56-187">**\_ \_ \_ esenzioni IKE per FWPM Weight Range \_**</span><span class="sxs-lookup"><span data-stu-id="37f56-187">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

<span data-ttu-id="37f56-188">**At FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ Accept \_ V {4 \| 6} Configurare le regole di filtro in ingresso per connessione**</span><span class="sxs-lookup"><span data-stu-id="37f56-188">**At FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6} set up inbound per-connection filtering rules**</span></span>  

1.  <span data-ttu-id="37f56-189">Aggiungere un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="37f56-189">Add a filter with the following properties.</span></span> <span data-ttu-id="37f56-190">Questo filtro consente solo i tentativi di connessione in ingresso se sono protetti da IPsec.</span><span class="sxs-lookup"><span data-stu-id="37f56-190">This filter will only allow inbound connection attempts if they are secured by IPsec.</span></span> 

    | <span data-ttu-id="37f56-191">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="37f56-191">Filter property</span></span>                                                   | <span data-ttu-id="37f56-192">Valore</span><span class="sxs-lookup"><span data-stu-id="37f56-192">Value</span></span>                                                        |
    |-------------------------------------------------------------------|--------------------------------------------------------------|
    | <span data-ttu-id="37f56-193">**FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="37f56-193">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="37f56-194">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="37f56-194">NlatUnicast</span></span>                                                  |
    | <span data-ttu-id="37f56-195">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="37f56-195">**action.type**</span></span>                                                   | <span data-ttu-id="37f56-196">**\_ \_ terminazione CALLOUT azione FWP \_**</span><span class="sxs-lookup"><span data-stu-id="37f56-196">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                        |
    | <span data-ttu-id="37f56-197">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="37f56-197">**action.calloutKey**</span></span>                                             | <span data-ttu-id="37f56-198">**FWPM \_ CALLOUT \_ IPSec in \_ ingresso \_ avvio \_ sicuro \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="37f56-198">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V{4\|6}**</span></span> |

        
2.  <span data-ttu-id="37f56-199">Esentare il traffico ICMP da IPsec aggiungendo un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="37f56-199">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="37f56-200">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="37f56-200">Filter property</span></span>                                                   | <span data-ttu-id="37f56-201">Valore</span><span class="sxs-lookup"><span data-stu-id="37f56-201">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="37f56-202">**FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="37f56-202">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="37f56-203">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="37f56-203">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="37f56-204">**FWPM \_ Condizione di filtro \_ \_ protocollo IP condizione**</span><span class="sxs-lookup"><span data-stu-id="37f56-204">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="37f56-205">**IPPROTO \_ ICMP {V6}** queste costanti sono definite in Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="37f56-205">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="37f56-206">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="37f56-206">**action.type**</span></span>                                                   | <span data-ttu-id="37f56-207">**\_permesso azione \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="37f56-207">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="37f56-208">**weight**</span><span class="sxs-lookup"><span data-stu-id="37f56-208">**weight**</span></span>                                                        | <span data-ttu-id="37f56-209">**\_ \_ \_ esenzioni IKE per FWPM Weight Range \_**</span><span class="sxs-lookup"><span data-stu-id="37f56-209">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

</dl>

## <a name="related-topics"></a><span data-ttu-id="37f56-210">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="37f56-210">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37f56-211">Codice di esempio: utilizzo della modalità di trasporto</span><span class="sxs-lookup"><span data-stu-id="37f56-211">Sample code: Using Transport Mode</span></span>](using-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="37f56-212">Livelli ALE</span><span class="sxs-lookup"><span data-stu-id="37f56-212">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="37f56-213">**Identificatori di callout predefiniti**</span><span class="sxs-lookup"><span data-stu-id="37f56-213">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="37f56-214">Condizioni di filtro</span><span class="sxs-lookup"><span data-stu-id="37f56-214">Filtering Conditions</span></span>](filtering-conditions.md)
</dt> <dt>

[<span data-ttu-id="37f56-215">**Filtraggio degli identificatori del livello**</span><span class="sxs-lookup"><span data-stu-id="37f56-215">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="37f56-216">**\_ACTION0 FWPM**</span><span class="sxs-lookup"><span data-stu-id="37f56-216">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[<span data-ttu-id="37f56-217">**\_tipo di \_ contesto del provider FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="37f56-217">**FWPM\_PROVIDER\_CONTEXT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

