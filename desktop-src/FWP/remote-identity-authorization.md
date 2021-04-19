---
title: Autorizzazione identità remota
description: Lo scenario dei criteri IPsec di autorizzazione dell'identità remota richiede che le connessioni in ingresso provengano da un set specifico di entità di sicurezza remote specificate in un elenco di controllo di accesso (ACL) di Windows Security Descriptor (SD).
ms.assetid: 4d9f83d6-6f56-4416-8c35-d0260f9e888c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57287a0dd9af4686b1a2dab162677912213559a7
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314834"
---
# <a name="remote-identity-authorization"></a><span data-ttu-id="1206c-103">Autorizzazione identità remota</span><span class="sxs-lookup"><span data-stu-id="1206c-103">Remote Identity Authorization</span></span>

<span data-ttu-id="1206c-104">Lo scenario dei criteri IPsec di autorizzazione dell'identità remota richiede che le connessioni in ingresso provengano da un set specifico di entità di sicurezza remote specificate in un elenco di controllo di accesso (ACL) di Windows Security Descriptor (SD).</span><span class="sxs-lookup"><span data-stu-id="1206c-104">The Remote Identity Authorization IPsec policy scenario requires that inbound connections come from a specific set of remote security principals which are specified in a Windows security descriptor (SD) access control list (ACL).</span></span> <span data-ttu-id="1206c-105">Se l'identità remota (come determinato da IPsec) non corrisponde al set di identità consentite, la connessione verrà eliminata.</span><span class="sxs-lookup"><span data-stu-id="1206c-105">If the remote identity (as determined by IPsec) does not match the set of allowed identities, the connection will be dropped.</span></span> <span data-ttu-id="1206c-106">Questo criterio deve essere specificato insieme a una delle opzioni dei criteri della modalità di trasporto.</span><span class="sxs-lookup"><span data-stu-id="1206c-106">This policy must be specified in conjunction with one of the transport mode policy options.</span></span>

<span data-ttu-id="1206c-107">Se AuthIP è abilitato, è possibile specificare due descrittori di sicurezza, uno corrispondente alla modalità principale AuthIP e l'altro corrispondente alla modalità estesa AuthIP.</span><span class="sxs-lookup"><span data-stu-id="1206c-107">If AuthIP is enabled, two security descriptors can be specified, one corresponding to AuthIP main mode, and the other corresponding to AuthIP extended mode.</span></span>

<span data-ttu-id="1206c-108">Un esempio di un possibile scenario di modalità di trasporto per l'individuazione della negoziazione è "proteggere tutto il traffico dati unicast, ad eccezione di ICMP, uso della modalità di trasporto IPsec, abilitazione dell'individuazione della negoziazione e limitazione dell'accesso in ingresso alle identità remote consentite in base al descrittore di sicurezza SD1 (corrispondente alla modalità principale IKE/AuthIP) e al descrittore di sicurezza SD2 (corrispondente alla modalità estesa AuthIP), per tutto il traffico unicast corrispondente alla porta TCP locale 5555".</span><span class="sxs-lookup"><span data-stu-id="1206c-108">An example of a possible Negotiation Discovery Transport Mode scenario is "Secure all unicast data traffic, except ICMP, using IPsec transport mode, enable negotiation discovery, and restrict inbound access to remote identities allowed as per security descriptor SD1 (corresponding to IKE/AuthIP main mode) and security descriptor SD2 (corresponding to AuthIP extended mode), for all unicast traffic corresponding to TCP local port 5555."</span></span>

<span data-ttu-id="1206c-109">Per implementare questo esempio a livello di codice, utilizzare la seguente configurazione di Pam.</span><span class="sxs-lookup"><span data-stu-id="1206c-109">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="1206c-110">**Ai \_ criteri di negoziazione FWPM layer \_ IKEEXT \_ V {4 \| 6} Setup mm**</span><span class="sxs-lookup"><span data-stu-id="1206c-110">**At FWPM\_LAYER\_IKEEXT\_V{4\|6} setup MM negotiation policy**</span></span>  

1.  <span data-ttu-id="1206c-111">Aggiungere uno o entrambi i contesti di provider di criteri MM seguenti.</span><span class="sxs-lookup"><span data-stu-id="1206c-111">Add one or both of the following MM policy provider contexts.</span></span>  
    -   <span data-ttu-id="1206c-112">Per IKE, un contesto del provider di criteri di tipo **FWPM \_ IPSec \_ IKE \_ mm \_ context**.</span><span class="sxs-lookup"><span data-stu-id="1206c-112">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_MM\_CONTEXT**.</span></span>
    -   <span data-ttu-id="1206c-113">Per AuthIP, un contesto del provider di criteri di tipo **FWPM \_ IPSec \_ AuthIP \_ mm \_ context**.</span><span class="sxs-lookup"><span data-stu-id="1206c-113">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT**.</span></span>

    > [!Note]  
    > <span data-ttu-id="1206c-114">Verrà negoziato un modulo di trasparenza comune e verranno applicati i criteri di MM corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="1206c-114">A common keying module will be negotiated and the corresponding MM policy will be applied.</span></span> <span data-ttu-id="1206c-115">AuthIP è il modulo di chiavi preferito se sono supportati sia IKE che AuthIP.</span><span class="sxs-lookup"><span data-stu-id="1206c-115">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="1206c-116">Per ognuno dei contesti aggiunti nel passaggio 1, aggiungere un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="1206c-116">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 

    | <span data-ttu-id="1206c-117">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="1206c-117">Filter property</span></span>        | <span data-ttu-id="1206c-118">Valore</span><span class="sxs-lookup"><span data-stu-id="1206c-118">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="1206c-119">Condizioni di filtro</span><span class="sxs-lookup"><span data-stu-id="1206c-119">Filtering conditions</span></span>   | <span data-ttu-id="1206c-120">Vuoto.</span><span class="sxs-lookup"><span data-stu-id="1206c-120">Empty.</span></span> <span data-ttu-id="1206c-121">Tutto il traffico corrisponderà al filtro.</span><span class="sxs-lookup"><span data-stu-id="1206c-121">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="1206c-122">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="1206c-122">**providerContextKey**</span></span> | <span data-ttu-id="1206c-123">GUID del contesto del provider MM aggiunto nel passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="1206c-123">GUID of the MM provider context added in step 1.</span></span> |

        

<span data-ttu-id="1206c-124">**A FWPM \_ Layer \_ IPSec \_ V {4 \| 6} installazione di QM e criteri di negoziazione em**</span><span class="sxs-lookup"><span data-stu-id="1206c-124">**At FWPM\_LAYER\_IPSEC\_V{4\|6} setup QM and EM negotiation policy**</span></span>  

1.  <span data-ttu-id="1206c-125">Aggiungere uno o entrambi i contesti del provider di criteri per la modalità di trasporto QM seguenti e impostare il flag di [**\_ criteri IPSec \_ \_ ND \_ Secure**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) flag.</span><span class="sxs-lookup"><span data-stu-id="1206c-125">Add one or both of the following QM transport mode policy provider contexts and set the [**IPSEC\_POLICY\_FLAG\_ND\_SECURE**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) flag.</span></span>  
    -   <span data-ttu-id="1206c-126">Per IKE, un contesto del provider di criteri di tipo **FWPM \_ IPSec \_ IKE \_ \_ trasporto \_ context**.</span><span class="sxs-lookup"><span data-stu-id="1206c-126">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_QM\_TRANSPORT\_CONTEXT**.</span></span>
    -   <span data-ttu-id="1206c-127">Per AuthIP, un contesto del provider di criteri di tipo **FWPM \_ IPSec \_ AuthIP \_ QM del \_ \_ contesto di trasporto** che contiene i criteri di negoziazione della modalità estesa (em) AuthIP.</span><span class="sxs-lookup"><span data-stu-id="1206c-127">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_QM\_TRANSPORT\_CONTEXT** that contains the AuthIP Extended Mode (EM) negotiation policy.</span></span>

    > [!Note]  
    > <span data-ttu-id="1206c-128">Verrà negoziato un modulo di trasparenza comune e verranno applicati i criteri di QM corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="1206c-128">A common keying module will be negotiated and the corresponding QM policy will be applied.</span></span> <span data-ttu-id="1206c-129">AuthIP è il modulo di chiavi preferito se sono supportati sia IKE che AuthIP.</span><span class="sxs-lookup"><span data-stu-id="1206c-129">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="1206c-130">Per ognuno dei contesti aggiunti nel passaggio 1, aggiungere un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="1206c-130">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 

    | <span data-ttu-id="1206c-131">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="1206c-131">Filter property</span></span>        | <span data-ttu-id="1206c-132">Valore</span><span class="sxs-lookup"><span data-stu-id="1206c-132">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="1206c-133">Condizioni di filtro</span><span class="sxs-lookup"><span data-stu-id="1206c-133">Filtering conditions</span></span>   | <span data-ttu-id="1206c-134">Vuoto.</span><span class="sxs-lookup"><span data-stu-id="1206c-134">Empty.</span></span> <span data-ttu-id="1206c-135">Tutto il traffico corrisponderà al filtro.</span><span class="sxs-lookup"><span data-stu-id="1206c-135">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="1206c-136">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="1206c-136">**providerContextKey**</span></span> | <span data-ttu-id="1206c-137">GUID del contesto del provider QM aggiunto nel passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="1206c-137">GUID of the QM provider context added in step 1.</span></span> |

        

<span data-ttu-id="1206c-138">**Al \_ trasporto in ingresso FWPM layer \_ \_ \_ V {4 \| 6} Configurare le regole di filtro in ingresso per pacchetto**</span><span class="sxs-lookup"><span data-stu-id="1206c-138">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="1206c-139">Aggiungere un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="1206c-139">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="1206c-140">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="1206c-140">Filter property</span></span>                                                   | <span data-ttu-id="1206c-141">Valore</span><span class="sxs-lookup"><span data-stu-id="1206c-141">Value</span></span>                                                                                              |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="1206c-142">**FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="1206c-142">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="1206c-143">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="1206c-143">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | <span data-ttu-id="1206c-144">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="1206c-144">**action.type**</span></span>                                                   | <span data-ttu-id="1206c-145">**\_ \_ terminazione CALLOUT azione FWP \_**</span><span class="sxs-lookup"><span data-stu-id="1206c-145">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                              |
    | <span data-ttu-id="1206c-146">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="1206c-146">**action.calloutKey**</span></span>                                             | <span data-ttu-id="1206c-147">**\_Trasporto in \_ ingresso IPSec di CALLOUT FWPM \_ \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="1206c-147">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                              |
    | <span data-ttu-id="1206c-148">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="1206c-148">**rawContext**</span></span>                                                    | [<span data-ttu-id="1206c-149">**sicurezza della connessione per il \_ \_ \_ \_ salvataggio permanente in ingresso IPSec \_ del contesto FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="1206c-149">**FWPM\_CONTEXT\_IPSEC\_INBOUND\_PERSIST\_CONNECTION\_SECURITY**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="1206c-150">Esentare il traffico ICMP da IPsec aggiungendo un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="1206c-150">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 

    | <span data-ttu-id="1206c-151">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="1206c-151">Filter property</span></span>                                                   | <span data-ttu-id="1206c-152">Valore</span><span class="sxs-lookup"><span data-stu-id="1206c-152">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="1206c-153">**FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="1206c-153">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="1206c-154">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="1206c-154">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="1206c-155">**FWPM \_ Condizione di filtro \_ \_ protocollo IP condizione**</span><span class="sxs-lookup"><span data-stu-id="1206c-155">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="1206c-156">**IPPROTO \_ ICMP {V6}** queste costanti sono definite in Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="1206c-156">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="1206c-157">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="1206c-157">**action.type**</span></span>                                                   | <span data-ttu-id="1206c-158">\_permesso azione \_ FWP</span><span class="sxs-lookup"><span data-stu-id="1206c-158">FWP\_ACTION\_PERMIT</span></span>                                                        |
    | <span data-ttu-id="1206c-159">**weight**</span><span class="sxs-lookup"><span data-stu-id="1206c-159">**weight**</span></span>                                                        | [<span data-ttu-id="1206c-160">**\_ \_ \_ esenzioni IKE per FWPM Weight Range \_**</span><span class="sxs-lookup"><span data-stu-id="1206c-160">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="1206c-161">**Al \_ trasporto in uscita FWPM layer \_ \_ \_ V {4 \| 6} Configurare le regole di filtro in uscita per pacchetto**</span><span class="sxs-lookup"><span data-stu-id="1206c-161">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="1206c-162">Aggiungere un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="1206c-162">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="1206c-163">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="1206c-163">Filter property</span></span>                                                   | <span data-ttu-id="1206c-164">Valore</span><span class="sxs-lookup"><span data-stu-id="1206c-164">Value</span></span>                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | <span data-ttu-id="1206c-165">**FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="1206c-165">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="1206c-166">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="1206c-166">NlatUnicast</span></span>                                                                               |
    | <span data-ttu-id="1206c-167">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="1206c-167">**action.type**</span></span>                                                   | <span data-ttu-id="1206c-168">**\_ \_ terminazione CALLOUT azione FWP \_**</span><span class="sxs-lookup"><span data-stu-id="1206c-168">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                     |
    | <span data-ttu-id="1206c-169">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="1206c-169">**action.calloutKey**</span></span>                                             | <span data-ttu-id="1206c-170">**\_Trasporto in \_ uscita IPSec di CALLOUT FWPM \_ \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="1206c-170">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                    |
    | <span data-ttu-id="1206c-171">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="1206c-171">**rawContext**</span></span>                                                    | [<span data-ttu-id="1206c-172">**\_ \_ \_ \_ individuazione negoziazioni in uscita IPSec del contesto FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="1206c-172">**FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_NEGOTIATE\_DISCOVER**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="1206c-173">Esentare il traffico ICMP da IPsec aggiungendo un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="1206c-173">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 

    | <span data-ttu-id="1206c-174">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="1206c-174">Filter property</span></span>                                                   | <span data-ttu-id="1206c-175">Valore</span><span class="sxs-lookup"><span data-stu-id="1206c-175">Value</span></span>                                                                  |
    |-------------------------------------------------------------------|------------------------------------------------------------------------|
    | <span data-ttu-id="1206c-176">**FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="1206c-176">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="1206c-177">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="1206c-177">NlatUnicast</span></span>                                                            |
    | <span data-ttu-id="1206c-178">**FWPM \_ Condizione di filtro \_ \_ protocollo IP condizione**</span><span class="sxs-lookup"><span data-stu-id="1206c-178">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="1206c-179">IPPROTO \_ ICMP {V6} queste costanti sono definite in Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="1206c-179">IPPROTO\_ICMP{V6}These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="1206c-180">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="1206c-180">**action.type**</span></span>                                                   | <span data-ttu-id="1206c-181">**\_permesso azione \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="1206c-181">**FWP\_ACTION\_PERMIT**</span></span>                                                |
    | <span data-ttu-id="1206c-182">**weight**</span><span class="sxs-lookup"><span data-stu-id="1206c-182">**weight**</span></span>                                                        | <span data-ttu-id="1206c-183">**\_ \_ \_ esenzioni IKE per FWPM Weight Range \_**</span><span class="sxs-lookup"><span data-stu-id="1206c-183">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                               |

        

<span data-ttu-id="1206c-184">**A FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6} Configurare le regole di filtro in ingresso per connessione**</span><span class="sxs-lookup"><span data-stu-id="1206c-184">**At FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6} setup inbound per-connection filtering rules**</span></span>  

1.  <span data-ttu-id="1206c-185">Aggiungere un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="1206c-185">Add a filter with the following properties.</span></span> <span data-ttu-id="1206c-186">Questo filtro consente solo i tentativi di connessione in ingresso se sono protetti da IPsec.</span><span class="sxs-lookup"><span data-stu-id="1206c-186">This filter will only allow inbound connection attempts if they are secured by IPsec.</span></span> 

    | <span data-ttu-id="1206c-187">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="1206c-187">Filter property</span></span>                                                   | <span data-ttu-id="1206c-188">Valore</span><span class="sxs-lookup"><span data-stu-id="1206c-188">Value</span></span>                                                        |
    |-------------------------------------------------------------------|--------------------------------------------------------------|
    | <span data-ttu-id="1206c-189">**FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="1206c-189">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="1206c-190">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="1206c-190">NlatUnicast</span></span>                                                  |
    | <span data-ttu-id="1206c-191">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="1206c-191">**action.type**</span></span>                                                   | <span data-ttu-id="1206c-192">**\_ \_ terminazione CALLOUT azione FWP \_**</span><span class="sxs-lookup"><span data-stu-id="1206c-192">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                        |
    | <span data-ttu-id="1206c-193">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="1206c-193">**action.calloutKey**</span></span>                                             | <span data-ttu-id="1206c-194">**FWPM \_ CALLOUT \_ IPSec in \_ ingresso \_ avvio \_ sicuro \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="1206c-194">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V{4\|6}**</span></span> |

        
2.  <span data-ttu-id="1206c-195">Esentare il traffico ICMP da IPsec aggiungendo un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="1206c-195">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 

    | <span data-ttu-id="1206c-196">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="1206c-196">Filter property</span></span>                                                   | <span data-ttu-id="1206c-197">Valore</span><span class="sxs-lookup"><span data-stu-id="1206c-197">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="1206c-198">**FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="1206c-198">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="1206c-199">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="1206c-199">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="1206c-200">**FWPM \_ Condizione di filtro \_ \_ protocollo IP condizione**</span><span class="sxs-lookup"><span data-stu-id="1206c-200">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="1206c-201">**IPPROTO \_ ICMP {V6}** queste costanti sono definite in Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="1206c-201">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="1206c-202">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="1206c-202">**action.type**</span></span>                                                   | <span data-ttu-id="1206c-203">**\_permesso azione \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="1206c-203">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="1206c-204">**weight**</span><span class="sxs-lookup"><span data-stu-id="1206c-204">**weight**</span></span>                                                        | <span data-ttu-id="1206c-205">**\_ \_ \_ esenzioni IKE per FWPM Weight Range \_**</span><span class="sxs-lookup"><span data-stu-id="1206c-205">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        
3.  <span data-ttu-id="1206c-206">Aggiungere un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="1206c-206">Add a filter with the following properties.</span></span> <span data-ttu-id="1206c-207">Questo filtro consente le connessioni in ingresso alla porta TCP 5555 se le identità Remote corrispondenti sono consentite sia da SD1 che da SD2.</span><span class="sxs-lookup"><span data-stu-id="1206c-207">This filter will permit inbound connections to TCP port 5555 if the corresponding remote identities are allowed by both SD1 and SD2.</span></span> 

    | <span data-ttu-id="1206c-208">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="1206c-208">Filter property</span></span>                                                   | <span data-ttu-id="1206c-209">Valore</span><span class="sxs-lookup"><span data-stu-id="1206c-209">Value</span></span>                                                              |
    |-------------------------------------------------------------------|--------------------------------------------------------------------|
    | <span data-ttu-id="1206c-210">**FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="1206c-210">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="1206c-211">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="1206c-211">NlatUnicast</span></span>                                                        |
    | <span data-ttu-id="1206c-212">**FWPM \_ Condizione di filtro \_ \_ protocollo IP condizione**</span><span class="sxs-lookup"><span data-stu-id="1206c-212">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="1206c-213">**IPPROTO \_ TCP** questa costante è definita in Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="1206c-213">**IPPROTO\_TCP** This constant is defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="1206c-214">**FWPM \_ Condizione di filtro della \_ \_ \_ porta locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="1206c-214">**FWPM\_CONDITION\_IP\_LOCAL\_PORT** filtering condition</span></span>          | <span data-ttu-id="1206c-215">5555</span><span class="sxs-lookup"><span data-stu-id="1206c-215">5555</span></span>                                                               |
    | <span data-ttu-id="1206c-216">**\_ \_ \_ \_ ID computer remoto ale Condition \_ FWPM**</span><span class="sxs-lookup"><span data-stu-id="1206c-216">**FWPM\_CONDITION\_ALE\_REMOTE\_MACHINE\_ID**</span></span>                     | <span data-ttu-id="1206c-217">SD1</span><span class="sxs-lookup"><span data-stu-id="1206c-217">SD1</span></span>                                                                |
    | <span data-ttu-id="1206c-218">**\_ \_ \_ \_ ID utente remoto di FWPM Condition ale \_**</span><span class="sxs-lookup"><span data-stu-id="1206c-218">**FWPM\_CONDITION\_ALE\_REMOTE\_USER\_ID**</span></span>                        | <span data-ttu-id="1206c-219">SD2</span><span class="sxs-lookup"><span data-stu-id="1206c-219">SD2</span></span>                                                                |
    | <span data-ttu-id="1206c-220">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="1206c-220">**action.type**</span></span>                                                   | <span data-ttu-id="1206c-221">**\_ \_ terminazione CALLOUT azione FWP \_**</span><span class="sxs-lookup"><span data-stu-id="1206c-221">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                              |
    | <span data-ttu-id="1206c-222">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="1206c-222">**action.calloutKey**</span></span>                                             | <span data-ttu-id="1206c-223">**FWPM \_ CALLOUT \_ IPSec in \_ ingresso \_ avvio \_ sicuro \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="1206c-223">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V{4\|6}**</span></span>       |

        
4.  <span data-ttu-id="1206c-224">Aggiungere un filtro con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="1206c-224">Add a filter with the following properties.</span></span> <span data-ttu-id="1206c-225">Questo filtro bloccherà qualsiasi altra connessione in ingresso alla porta TCP 5555 che non corrisponde al filtro precedente.</span><span class="sxs-lookup"><span data-stu-id="1206c-225">This filter will block any other inbound connections to TCP port 5555 that did not match the previous filter.</span></span> 

    | <span data-ttu-id="1206c-226">Filter (proprietà)</span><span class="sxs-lookup"><span data-stu-id="1206c-226">Filter property</span></span>                                                   | <span data-ttu-id="1206c-227">Valore</span><span class="sxs-lookup"><span data-stu-id="1206c-227">Value</span></span>                                                              |
    |-------------------------------------------------------------------|--------------------------------------------------------------------|
    | <span data-ttu-id="1206c-228">**FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="1206c-228">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="1206c-229">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="1206c-229">NlatUnicast</span></span>                                                        |
    | <span data-ttu-id="1206c-230">**FWPM \_ Condizione di filtro \_ \_ protocollo IP condizione**</span><span class="sxs-lookup"><span data-stu-id="1206c-230">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="1206c-231">**IPPROTO \_ TCP** questa costante è definita in Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="1206c-231">**IPPROTO\_TCP** This constant is defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="1206c-232">**FWPM \_ Condizione di filtro della \_ \_ \_ porta locale IP della condizione**</span><span class="sxs-lookup"><span data-stu-id="1206c-232">**FWPM\_CONDITION\_IP\_LOCAL\_PORT** filtering condition</span></span>          | <span data-ttu-id="1206c-233">5555</span><span class="sxs-lookup"><span data-stu-id="1206c-233">5555</span></span>                                                               |
    | <span data-ttu-id="1206c-234">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="1206c-234">**action.type**</span></span>                                                   | <span data-ttu-id="1206c-235">**\_blocco azione \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="1206c-235">**FWP\_ACTION\_BLOCK**</span></span>                                             |

        

</dl>

## <a name="related-topics"></a><span data-ttu-id="1206c-236">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1206c-236">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1206c-237">Codice di esempio: utilizzo della modalità di trasporto</span><span class="sxs-lookup"><span data-stu-id="1206c-237">Sample code: Using Transport Mode</span></span>](using-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="1206c-238">Livelli ALE</span><span class="sxs-lookup"><span data-stu-id="1206c-238">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="1206c-239">**Identificatori di callout predefiniti**</span><span class="sxs-lookup"><span data-stu-id="1206c-239">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="1206c-240">Condizioni di filtro</span><span class="sxs-lookup"><span data-stu-id="1206c-240">Filtering Conditions</span></span>](filtering-conditions.md)
</dt> <dt>

[<span data-ttu-id="1206c-241">**Filtraggio degli identificatori del livello**</span><span class="sxs-lookup"><span data-stu-id="1206c-241">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="1206c-242">**\_ACTION0 FWPM**</span><span class="sxs-lookup"><span data-stu-id="1206c-242">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[<span data-ttu-id="1206c-243">**\_tipo di \_ contesto del provider FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="1206c-243">**FWPM\_PROVIDER\_CONTEXT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

