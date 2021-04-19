---
title: Crittografia garantita
description: Lo scenario dei criteri IPsec di crittografia garantita richiede la crittografia IPsec per tutto il traffico corrispondente. Questo criterio deve essere specificato insieme a una delle opzioni dei criteri della modalità di trasporto.
ms.assetid: 68758f0c-f134-4b7a-820a-313e2a82f280
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbffa3d78a9e178850f3afaa4d6b7fa9831be875
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314644"
---
# <a name="guaranteed-encryption"></a><span data-ttu-id="dfdcf-104">Crittografia garantita</span><span class="sxs-lookup"><span data-stu-id="dfdcf-104">Guaranteed Encryption</span></span>

<span data-ttu-id="dfdcf-105">Lo scenario dei criteri IPsec di crittografia garantita richiede la crittografia IPsec per tutto il traffico corrispondente.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-105">The Guaranteed Encryption IPsec policy scenario requires IPsec encryption for all matching traffic.</span></span> <span data-ttu-id="dfdcf-106">Questo criterio deve essere specificato insieme a una delle opzioni dei criteri della modalità di trasporto.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-106">This policy must be specified in conjunction with one of the transport mode policy options.</span></span>

<span data-ttu-id="dfdcf-107">La crittografia garantita viene in genere usata per crittografare il traffico sensibile per ogni singola applicazione.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-107">Guaranteed Encryption is typically used to encrypt sensitive traffic on a per application basis.</span></span>

<span data-ttu-id="dfdcf-108">Un esempio di uno scenario di crittografia garantita è "proteggere tutto il traffico dati unicast, tranne ICMP, usando la modalità di trasporto IPsec, abilitare l'individuazione della negoziazione e richiedere la crittografia garantita per tutto il traffico unicast corrispondente alla porta TCP locale 5555".</span><span class="sxs-lookup"><span data-stu-id="dfdcf-108">An example of a possible Guaranteed Encryption scenario is "Secure all unicast data traffic, except ICMP, using IPsec transport mode, enable negotiation discovery, and require guaranteed encryption for all unicast traffic corresponding to TCP local port 5555."</span></span>

<span data-ttu-id="dfdcf-109">Per implementare questo esempio a livello di codice, utilizzare la seguente configurazione di Pam.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-109">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="dfdcf-110">**Ai \_ criteri di negoziazione FWPM layer \_ IKEEXT \_ V {4 \| 6} Setup mm**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-110">**At FWPM\_LAYER\_IKEEXT\_V{4\|6} setup MM negotiation policy**</span></span>  

1.  <span data-ttu-id="dfdcf-111">Aggiungere uno o entrambi i contesti di provider di criteri MM seguenti.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-111">Add one or both of the following MM policy provider contexts.</span></span>  
    -   <span data-ttu-id="dfdcf-112">Per IKE, un contesto del provider di criteri di tipo FWPM \_ IPSec \_ IKE \_ mm \_ context.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-112">For IKE, a policy provider context of type FWPM\_IPSEC\_IKE\_MM\_CONTEXT.</span></span>
    -   <span data-ttu-id="dfdcf-113">Per AuthIP, un contesto del provider di criteri di tipo FWPM \_ IPSec \_ AuthIP \_ mm \_ context.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-113">For AuthIP, a policy provider context of type FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT.</span></span>

    > [!Note]  
    > <span data-ttu-id="dfdcf-114">Verrà negoziato un modulo di trasparenza comune e verranno applicati i criteri di MM corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-114">A common keying module will be negotiated and the corresponding MM policy will be applied.</span></span> <span data-ttu-id="dfdcf-115">AuthIP è il modulo di chiavi preferito se sono supportati sia IKE che AuthIP.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-115">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="dfdcf-116">Per ognuno dei contesti aggiunti nel passaggio 1, aggiungere un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-116">For each of the contexts added in step 1, add a filter with the following properties.</span></span>

    | <span data-ttu-id="dfdcf-117">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="dfdcf-117">Filter property</span></span>        | <span data-ttu-id="dfdcf-118">Valore</span><span class="sxs-lookup"><span data-stu-id="dfdcf-118">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="dfdcf-119">Condizioni di filtro</span><span class="sxs-lookup"><span data-stu-id="dfdcf-119">Filtering conditions</span></span>   | <span data-ttu-id="dfdcf-120">Vuoto.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-120">Empty.</span></span> <span data-ttu-id="dfdcf-121">Tutto il traffico corrisponderà al filtro.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-121">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="dfdcf-122">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-122">**providerContextKey**</span></span> | <span data-ttu-id="dfdcf-123">GUID del contesto del provider MM aggiunto nel passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-123">GUID of the MM provider context added in step 1.</span></span> |

        

<span data-ttu-id="dfdcf-124">**A FWPM \_ Layer \_ IPSec \_ V {4 \| 6} installazione di QM e criteri di negoziazione em**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-124">**At FWPM\_LAYER\_IPSEC\_V{4\|6} setup QM and EM negotiation policy**</span></span>  

1.  <span data-ttu-id="dfdcf-125">Aggiungere uno o entrambi i contesti del provider di criteri per la modalità di trasporto QM seguenti e impostare il flag di [**\_ criteri IPSec \_ \_ ND \_ Secure**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) flag.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-125">Add one or both of the following QM transport mode policy provider contexts and set the [**IPSEC\_POLICY\_FLAG\_ND\_SECURE**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) flag.</span></span>  
    -   <span data-ttu-id="dfdcf-126">Per IKE, un contesto del provider di criteri di tipo **FWPM \_ IPSec \_ IKE \_ \_ trasporto \_ context**.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-126">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_QM\_TRANSPORT\_CONTEXT**.</span></span>
    -   <span data-ttu-id="dfdcf-127">Per AuthIP, un contesto del provider di criteri di tipo **FWPM \_ IPSec \_ AuthIP \_ mq \_ \_ context**.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-127">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_QM\_TRANSPORT\_CONTEXT**.</span></span> <span data-ttu-id="dfdcf-128">Questo contesto può facoltativamente contenere i criteri di negoziazione della modalità estesa AuthIP (EM).</span><span class="sxs-lookup"><span data-stu-id="dfdcf-128">This context can optionally contain the AuthIP Extended Mode (EM) negotiation policy.</span></span>

    > [!Note]  
    > <span data-ttu-id="dfdcf-129">Verrà negoziato un modulo di trasparenza comune e verranno applicati i criteri di QM corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-129">A common keying module will be negotiated and the corresponding QM policy will be applied.</span></span> <span data-ttu-id="dfdcf-130">AuthIP è il modulo di chiavi preferito se sono supportati sia IKE che AuthIP.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-130">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="dfdcf-131">Per ognuno dei contesti aggiunti nel passaggio 1, aggiungere un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-131">For each of the contexts added in step 1, add a filter with the following properties.</span></span>

    | <span data-ttu-id="dfdcf-132">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="dfdcf-132">Filter property</span></span>        | <span data-ttu-id="dfdcf-133">Valore</span><span class="sxs-lookup"><span data-stu-id="dfdcf-133">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="dfdcf-134">Condizioni di filtro</span><span class="sxs-lookup"><span data-stu-id="dfdcf-134">Filtering conditions</span></span>   | <span data-ttu-id="dfdcf-135">Vuoto.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-135">Empty.</span></span> <span data-ttu-id="dfdcf-136">Tutto il traffico corrisponderà al filtro.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-136">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="dfdcf-137">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-137">**providerContextKey**</span></span> | <span data-ttu-id="dfdcf-138">GUID del contesto del provider QM aggiunto nel passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-138">GUID of the QM provider context added in step 1.</span></span> |

        

<span data-ttu-id="dfdcf-139">**Al \_ trasporto in ingresso FWPM layer \_ \_ \_ V {4 \| 6} Configurare le regole di filtro in ingresso per pacchetto**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-139">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="dfdcf-140">Aggiungere un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-140">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="dfdcf-141">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="dfdcf-141">Filter property</span></span>                                               | <span data-ttu-id="dfdcf-142">Valore</span><span class="sxs-lookup"><span data-stu-id="dfdcf-142">Value</span></span>                                                                                              |
    |---------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="dfdcf-143">\_Condizione di \_ \_ filtro del \_ tipo di indirizzo locale IP della condizione FWPM \_</span><span class="sxs-lookup"><span data-stu-id="dfdcf-143">FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE filtering condition</span></span> | [<span data-ttu-id="dfdcf-144">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="dfdcf-144">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | <span data-ttu-id="dfdcf-145">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-145">**action.type**</span></span>                                               | <span data-ttu-id="dfdcf-146">**\_ \_ terminazione CALLOUT azione FWP \_**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-146">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                              |
    | <span data-ttu-id="dfdcf-147">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-147">**action.calloutKey**</span></span>                                         | <span data-ttu-id="dfdcf-148">**\_Trasporto in \_ ingresso IPSec di CALLOUT FWPM \_ \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-148">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                              |
    | <span data-ttu-id="dfdcf-149">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-149">**rawContext**</span></span>                                                | [<span data-ttu-id="dfdcf-150">**sicurezza della connessione per il \_ \_ \_ \_ salvataggio permanente in ingresso IPSec \_ del contesto FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-150">**FWPM\_CONTEXT\_IPSEC\_INBOUND\_PERSIST\_CONNECTION\_SECURITY**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="dfdcf-151">Esentare il traffico ICMP da IPsec aggiungendo un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-151">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="dfdcf-152">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="dfdcf-152">Filter property</span></span>                                                   | <span data-ttu-id="dfdcf-153">Valore</span><span class="sxs-lookup"><span data-stu-id="dfdcf-153">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="dfdcf-154">**FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-154">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="dfdcf-155">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="dfdcf-155">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="dfdcf-156">**FWPM \_ Condizione di filtro \_ \_ protocollo IP condizione**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-156">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="dfdcf-157">**IPPROTO \_ ICMP {V6}** queste costanti sono definite in Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-157">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="dfdcf-158">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-158">**action.type**</span></span>                                                   | <span data-ttu-id="dfdcf-159">**\_permesso azione \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-159">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="dfdcf-160">**weight**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-160">**weight**</span></span>                                                        | [<span data-ttu-id="dfdcf-161">**\_ \_ \_ esenzioni IKE per FWPM Weight Range \_**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-161">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="dfdcf-162">**Al \_ trasporto in uscita FWPM layer \_ \_ \_ V {4 \| 6} Configurare le regole di filtro in uscita per pacchetto**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-162">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="dfdcf-163">Aggiungere un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-163">Add a filter with the following properties.</span></span>

    | <span data-ttu-id="dfdcf-164">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="dfdcf-164">Filter property</span></span>                                                   | <span data-ttu-id="dfdcf-165">Valore</span><span class="sxs-lookup"><span data-stu-id="dfdcf-165">Value</span></span>                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | <span data-ttu-id="dfdcf-166">**FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-166">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="dfdcf-167">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="dfdcf-167">NlatUnicast</span></span>                                                                               |
    | <span data-ttu-id="dfdcf-168">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-168">**action.type**</span></span>                                                   | <span data-ttu-id="dfdcf-169">**\_ \_ terminazione CALLOUT azione FWP \_**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-169">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                     |
    | <span data-ttu-id="dfdcf-170">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-170">**action.calloutKey**</span></span>                                             | <span data-ttu-id="dfdcf-171">**\_Trasporto in \_ uscita IPSec di CALLOUT FWPM \_ \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-171">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                    |
    | <span data-ttu-id="dfdcf-172">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-172">**rawContext**</span></span>                                                    | [<span data-ttu-id="dfdcf-173">**\_ \_ \_ \_ individuazione negoziazioni in uscita IPSec del contesto FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-173">**FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_NEGOTIATE\_DISCOVER**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="dfdcf-174">Esentare il traffico ICMP da IPsec aggiungendo un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-174">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="dfdcf-175">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="dfdcf-175">Filter property</span></span>                                                   | <span data-ttu-id="dfdcf-176">Valore</span><span class="sxs-lookup"><span data-stu-id="dfdcf-176">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="dfdcf-177">**FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-177">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="dfdcf-178">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="dfdcf-178">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="dfdcf-179">**FWPM \_ Condizione di filtro \_ \_ protocollo IP condizione**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-179">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="dfdcf-180">**IPPROTO \_ ICMP {V6}** queste costanti sono definite in Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-180">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="dfdcf-181">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-181">**action.type**</span></span>                                                   | <span data-ttu-id="dfdcf-182">**\_permesso azione \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-182">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="dfdcf-183">**weight**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-183">**weight**</span></span>                                                        | <span data-ttu-id="dfdcf-184">**\_ \_ \_ esenzioni IKE per FWPM Weight Range \_**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-184">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

<span data-ttu-id="dfdcf-185">**A FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6} Configurare le regole di filtro in ingresso per connessione**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-185">**At FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6} setup inbound per-connection filtering rules**</span></span>  

1.  <span data-ttu-id="dfdcf-186">Aggiungere un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-186">Add a filter with the following properties.</span></span> <span data-ttu-id="dfdcf-187">Questo filtro consente solo i tentativi di connessione in ingresso se sono protetti da IPsec.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-187">This filter will only allow inbound connection attempts if they are secured by IPsec.</span></span> 

    | <span data-ttu-id="dfdcf-188">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="dfdcf-188">Filter property</span></span>                                                   | <span data-ttu-id="dfdcf-189">Valore</span><span class="sxs-lookup"><span data-stu-id="dfdcf-189">Value</span></span>                                                        |
    |-------------------------------------------------------------------|--------------------------------------------------------------|
    | <span data-ttu-id="dfdcf-190">**FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-190">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="dfdcf-191">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="dfdcf-191">NlatUnicast</span></span>                                                  |
    | <span data-ttu-id="dfdcf-192">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-192">**action.type**</span></span>                                                   | <span data-ttu-id="dfdcf-193">**\_ \_ terminazione CALLOUT azione FWP \_**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-193">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                        |
    | <span data-ttu-id="dfdcf-194">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-194">**action.calloutKey**</span></span>                                             | <span data-ttu-id="dfdcf-195">**FWPM \_ CALLOUT \_ IPSec in \_ ingresso \_ avvio \_ sicuro \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-195">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V{4\|6}**</span></span> |

        
2.  <span data-ttu-id="dfdcf-196">Esentare il traffico ICMP da IPsec aggiungendo un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-196">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="dfdcf-197">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="dfdcf-197">Filter property</span></span>                                                   | <span data-ttu-id="dfdcf-198">Valore</span><span class="sxs-lookup"><span data-stu-id="dfdcf-198">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="dfdcf-199">**FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-199">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="dfdcf-200">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="dfdcf-200">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="dfdcf-201">**FWPM \_ Condizione di filtro \_ \_ protocollo IP condizione**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-201">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="dfdcf-202">**IPPROTO \_ ICMP {V6}** queste costanti sono definite in Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-202">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="dfdcf-203">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-203">**action.type**</span></span>                                                   | <span data-ttu-id="dfdcf-204">**\_permesso azione \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-204">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="dfdcf-205">**weight**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-205">**weight**</span></span>                                                        | <span data-ttu-id="dfdcf-206">**\_ \_ \_ esenzioni IKE per FWPM Weight Range \_**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-206">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        
3.  <span data-ttu-id="dfdcf-207">Aggiungere un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-207">Add a filter with the following properties.</span></span> <span data-ttu-id="dfdcf-208">Questo filtro consentirà solo le connessioni in ingresso alla porta TCP 5555, se crittografate.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-208">This filter will only permit inbound connections to TCP port 5555 if they are encrypted.</span></span>

    | <span data-ttu-id="dfdcf-209">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="dfdcf-209">Filter property</span></span>                                                   | <span data-ttu-id="dfdcf-210">Valore</span><span class="sxs-lookup"><span data-stu-id="dfdcf-210">Value</span></span>                                                                                                 |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="dfdcf-211">**FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-211">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="dfdcf-212">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="dfdcf-212">NlatUnicast</span></span>                                                                                           |
    | <span data-ttu-id="dfdcf-213">**FWPM \_ Condizione di filtro \_ \_ protocollo IP condizione**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-213">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="dfdcf-214">**IPPROTO \_ TCP** questa costante è definita in Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-214">**IPPROTO\_TCP** This constant is defined in winsock2.h.</span></span><br/>                                    |
    | <span data-ttu-id="dfdcf-215">**FWPM \_ Condizione di filtro della \_ \_ \_ porta locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-215">**FWPM\_CONDITION\_IP\_LOCAL\_PORT** filtering condition</span></span>          | <span data-ttu-id="dfdcf-216">5555</span><span class="sxs-lookup"><span data-stu-id="dfdcf-216">5555</span></span>                                                                                                  |
    | <span data-ttu-id="dfdcf-217">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-217">**action.type**</span></span>                                                   | <span data-ttu-id="dfdcf-218">**\_ \_ terminazione CALLOUT azione FWP \_**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-218">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                                 |
    | <span data-ttu-id="dfdcf-219">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-219">**action.calloutKey**</span></span>                                             | <span data-ttu-id="dfdcf-220">**FWPM \_ CALLOUT \_ IPSec in \_ ingresso \_ avvio \_ sicuro \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-220">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V{4\|6}**</span></span>                                          |
    | <span data-ttu-id="dfdcf-221">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-221">**rawContext**</span></span>                                                    | [<span data-ttu-id="dfdcf-222">**per la connessione a FWPM \_ Context \_ ale è richiesta la \_ \_ \_ \_ \_ crittografia IPSec**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-222">**FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_REQUIRE\_IPSEC\_ENCRYPTION**</span></span>](filter-context-identifiers.md) |

        

<span data-ttu-id="dfdcf-223">**A FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6} Configurare le regole di filtro in uscita per connessione**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-223">**At FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6} setup outbound per-connection filtering rules**</span></span>

-   <span data-ttu-id="dfdcf-224">Aggiungere un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-224">Add a filter with the following properties.</span></span> <span data-ttu-id="dfdcf-225">Questo filtro consente solo le connessioni in uscita dalla porta TCP 5555, se crittografate.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-225">This filter will only permit outbound connections from TCP port 5555 if they are encrypted.</span></span>

    | <span data-ttu-id="dfdcf-226">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="dfdcf-226">Filter property</span></span>                                                   | <span data-ttu-id="dfdcf-227">Valore</span><span class="sxs-lookup"><span data-stu-id="dfdcf-227">Value</span></span>                                                                                                 |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="dfdcf-228">**FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-228">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="dfdcf-229">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="dfdcf-229">NlatUnicast</span></span>                                                                                           |
    | <span data-ttu-id="dfdcf-230">**FWPM \_ Condizione di filtro \_ \_ protocollo IP condizione**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-230">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="dfdcf-231">**IPPROTO \_ TCP** questa costante è definita in Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="dfdcf-231">**IPPROTO\_TCP** This constant is defined in winsock2.h.</span></span><br/>                                    |
    | <span data-ttu-id="dfdcf-232">**FWPM \_ Condizione di filtro della \_ \_ \_ porta locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-232">**FWPM\_CONDITION\_IP\_LOCAL\_PORT** filtering condition</span></span>          | <span data-ttu-id="dfdcf-233">5555</span><span class="sxs-lookup"><span data-stu-id="dfdcf-233">5555</span></span>                                                                                                  |
    | <span data-ttu-id="dfdcf-234">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-234">**action.type**</span></span>                                                   | <span data-ttu-id="dfdcf-235">**\_ \_ terminazione CALLOUT azione FWP \_**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-235">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                                 |
    | <span data-ttu-id="dfdcf-236">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-236">**action.calloutKey**</span></span>                                             | <span data-ttu-id="dfdcf-237">**FWPM \_ CALLOUT \_ IPSec \_ ale \_ Connect \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-237">**FWPM\_CALLOUT\_IPSEC\_ALE\_CONNECT\_V{4\|6}**</span></span>                                                       |
    | <span data-ttu-id="dfdcf-238">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-238">**rawContext**</span></span>                                                    | [<span data-ttu-id="dfdcf-239">**per la connessione a FWPM \_ Context \_ ale è richiesta la \_ \_ \_ \_ \_ crittografia IPSec**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-239">**FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_REQUIRE\_IPSEC\_ENCRYPTION**</span></span>](filter-context-identifiers.md) |

      

  
</dl>

## <a name="related-topics"></a><span data-ttu-id="dfdcf-240">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dfdcf-240">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfdcf-241">Codice di esempio: utilizzo della modalità di trasporto</span><span class="sxs-lookup"><span data-stu-id="dfdcf-241">Sample code: Using Transport Mode</span></span>](using-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="dfdcf-242">Livelli ALE</span><span class="sxs-lookup"><span data-stu-id="dfdcf-242">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="dfdcf-243">**Identificatori di callout predefiniti**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-243">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="dfdcf-244">Condizioni di filtro</span><span class="sxs-lookup"><span data-stu-id="dfdcf-244">Filtering Conditions</span></span>](filtering-conditions.md)
</dt> <dt>

[<span data-ttu-id="dfdcf-245">**Filtraggio degli identificatori del livello**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-245">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="dfdcf-246">**\_ACTION0 FWPM**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-246">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[<span data-ttu-id="dfdcf-247">**\_tipo di \_ contesto del provider FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="dfdcf-247">**FWPM\_PROVIDER\_CONTEXT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

