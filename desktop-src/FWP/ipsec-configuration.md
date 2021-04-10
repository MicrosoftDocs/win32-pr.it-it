---
title: Configurazione IPsec
description: Windows Filtering Platform (WFP) è la piattaforma sottostante per Windows Firewall con sicurezza avanzata.
ms.assetid: d54b5caa-daea-4231-9909-7a8d388df661
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78af8e3d0a23713c0505082555fe260bc562dfa4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963025"
---
# <a name="ipsec-configuration"></a><span data-ttu-id="14bc0-103">Configurazione IPsec</span><span class="sxs-lookup"><span data-stu-id="14bc0-103">IPsec Configuration</span></span>

<span data-ttu-id="14bc0-104">Windows Filtering Platform (WFP) è la piattaforma sottostante per Windows Firewall con sicurezza avanzata.</span><span class="sxs-lookup"><span data-stu-id="14bc0-104">Windows Filtering Platform (WFP) is the underlying platform for Windows Firewall with Advanced Security.</span></span> <span data-ttu-id="14bc0-105">Il WFP viene usato per configurare le regole di filtro di rete, che includono regole che regolano la protezione del traffico di rete con IPsec.</span><span class="sxs-lookup"><span data-stu-id="14bc0-105">WFP is used to configure network filtering rules, which include rules that govern securing network traffic with IPsec.</span></span> <span data-ttu-id="14bc0-106">Gli sviluppatori di applicazioni possono configurare IPsec direttamente tramite l'API WFP, per sfruttare i vantaggi di un modello di filtro del traffico di rete più granulare rispetto al modello esposto tramite lo snap-in MMC (Microsoft Management Console) per Windows Firewall con sicurezza avanzata.</span><span class="sxs-lookup"><span data-stu-id="14bc0-106">Application developers may configure IPsec directly using the WFP API, in order to take advantage of a more granular network traffic filtering model than the model exposed through the Microsoft Management Console (MMC) snap-in for Windows Firewall with Advanced Security.</span></span>

## <a name="what-is-ipsec"></a><span data-ttu-id="14bc0-107">Informazioni su IPsec</span><span class="sxs-lookup"><span data-stu-id="14bc0-107">What is IPsec</span></span>

<span data-ttu-id="14bc0-108">Internet Protocol Security (IPsec) è un set di protocolli di sicurezza usati per trasferire i pacchetti IP in modo riservato in Internet.</span><span class="sxs-lookup"><span data-stu-id="14bc0-108">Internet Protocol Security (IPsec) is a set of security protocols used to transfer IP packets confidentially across the Internet.</span></span> <span data-ttu-id="14bc0-109">IPsec è obbligatorio per tutte le implementazioni IPv6 e facoltativo per IPv4.</span><span class="sxs-lookup"><span data-stu-id="14bc0-109">IPsec is mandatory for all IPv6 implementations and optional for IPv4.</span></span>

<span data-ttu-id="14bc0-110">Il traffico IP protetto presenta due intestazioni IPsec facoltative, che identificano i tipi di protezione crittografica applicati al pacchetto IP e includono informazioni per la decodifica del pacchetto protetto.</span><span class="sxs-lookup"><span data-stu-id="14bc0-110">Secured IP traffic has two optional IPsec headers, which identify the types of cryptographic protection applied to the IP packet and include information for decoding the protected packet.</span></span>

<span data-ttu-id="14bc0-111">L'intestazione ESP (Encapsulating Security Payload) viene utilizzata per la privacy e la protezione da modifiche dannose eseguendo l'autenticazione e la crittografia facoltativa.</span><span class="sxs-lookup"><span data-stu-id="14bc0-111">The Encapsulating Security Payload (ESP) header is used for privacy and protection against malicious modification by performing authentication and optional encryption.</span></span> <span data-ttu-id="14bc0-112">Può essere usato per il traffico che attraversa i router NAT (Network Address Translation).</span><span class="sxs-lookup"><span data-stu-id="14bc0-112">It can be used for traffic that traverses Network Address Translation (NAT) routers.</span></span>

<span data-ttu-id="14bc0-113">L'intestazione di autenticazione (AH) viene utilizzata solo per la protezione da modifiche dannose eseguendo l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="14bc0-113">The Authentication Header (AH) is used only for protection against malicious modification by performing authentication.</span></span> <span data-ttu-id="14bc0-114">Non può essere usato per il traffico che attraversa i router NAT.</span><span class="sxs-lookup"><span data-stu-id="14bc0-114">It cannot be used for traffic that traverses NAT routers.</span></span>

<span data-ttu-id="14bc0-115">Per ulteriori informazioni su IPsec, vedere anche:</span><span class="sxs-lookup"><span data-stu-id="14bc0-115">For more information on IPsec, see also:</span></span>

<dl>

<span data-ttu-id="14bc0-116">[Riferimento tecnico per IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc740240(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="14bc0-116">[IPsec Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc740240(v=ws.10))</span></span>  
</dl>

## <a name="what-is-ike"></a><span data-ttu-id="14bc0-117">Che cos'è IKE</span><span class="sxs-lookup"><span data-stu-id="14bc0-117">What is IKE</span></span>

<span data-ttu-id="14bc0-118">Protocollo IKE (IKE) è un protocollo di scambio di chiave che fa parte del set di protocolli IPsec.</span><span class="sxs-lookup"><span data-stu-id="14bc0-118">Internet Key Exchange (IKE) is a key exchange protocol that is part of the IPsec protocol set.</span></span> <span data-ttu-id="14bc0-119">IKE viene usato durante la configurazione di una connessione protetta ed esegue lo scambio sicuro di chiavi segrete e altri parametri correlati alla protezione senza l'intervento dell'utente.</span><span class="sxs-lookup"><span data-stu-id="14bc0-119">IKE is used while setting up a secure connection and accomplishes the safe exchange of secret keys and other protection-related parameters without the intervention of the user.</span></span>

<span data-ttu-id="14bc0-120">Per ulteriori informazioni su IKE, vedere anche:</span><span class="sxs-lookup"><span data-stu-id="14bc0-120">For more information on IKE, see also:</span></span>

<dl>

<span data-ttu-id="14bc0-121">[protocollo IKE](/previous-versions/windows/it-pro/windows-server-2003/cc784994(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="14bc0-121">[Internet Key Exchange](/previous-versions/windows/it-pro/windows-server-2003/cc784994(v=ws.10))</span></span>  
</dl>

## <a name="what-is-authip"></a><span data-ttu-id="14bc0-122">Informazioni su AuthIP</span><span class="sxs-lookup"><span data-stu-id="14bc0-122">What is AuthIP</span></span>

<span data-ttu-id="14bc0-123">Authenticated Internet Protocol (AuthIP) è un nuovo protocollo di scambio delle chiavi che espande IKE come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="14bc0-123">Authenticated Internet Protocol (AuthIP) is a new key exchange protocol that expands IKE as follows.</span></span>

<dl> <span data-ttu-id="14bc0-124">Sebbene IKE supporti solo le credenziali di autenticazione del computer, AuthIP supporta anche:</span><span class="sxs-lookup"><span data-stu-id="14bc0-124">While IKE only supports computer authentication credentials, AuthIP also supports:</span></span>

-   <span data-ttu-id="14bc0-125">Credenziali utente: NTLM, Kerberos, certificati.</span><span class="sxs-lookup"><span data-stu-id="14bc0-125">User credentials: NTLM, Kerberos, certificates.</span></span>
-   <span data-ttu-id="14bc0-126">Certificati di integrità di protezione accesso alla rete (NAP).</span><span class="sxs-lookup"><span data-stu-id="14bc0-126">Network Access Protection (NAP) health certificates.</span></span>
-   <span data-ttu-id="14bc0-127">Credenziali anonime, usate per l'autenticazione facoltativa.</span><span class="sxs-lookup"><span data-stu-id="14bc0-127">Anonymous credential, used for optional authentication.</span></span>
-   <span data-ttu-id="14bc0-128">Combinazione di credenziali; ad esempio, una combinazione di credenziali Kerberos del computer e dell'utente.</span><span class="sxs-lookup"><span data-stu-id="14bc0-128">Combination of credentials; for example, a combination of machine and user Kerberos credentials.</span></span>

  
<span data-ttu-id="14bc0-129">AuthIP dispone di un meccanismo di tentativi di autenticazione che verifica tutti i metodi di autenticazione configurati prima di eseguire la connessione.</span><span class="sxs-lookup"><span data-stu-id="14bc0-129">AuthIP has an authentication-retry mechanism that verifies all configured authentication methods before failing the connection.</span></span>  
<span data-ttu-id="14bc0-130">AuthIP può essere usato con socket protetti per implementare il traffico protetto con IPsec basato sull'applicazione.</span><span class="sxs-lookup"><span data-stu-id="14bc0-130">AuthIP can be used with secure sockets to implement application-based IPsec secured traffic.</span></span> <span data-ttu-id="14bc0-131">Fornisce:</span><span class="sxs-lookup"><span data-stu-id="14bc0-131">It provides:</span></span>

-   <span data-ttu-id="14bc0-132">Autenticazione e crittografia per socket.</span><span class="sxs-lookup"><span data-stu-id="14bc0-132">Per-socket authentication and encryption.</span></span> <span data-ttu-id="14bc0-133">Per ulteriori informazioni, vedere [**WSASetSocketSecurity**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) .</span><span class="sxs-lookup"><span data-stu-id="14bc0-133">See [**WSASetSocketSecurity**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) for more information.</span></span>
-   <span data-ttu-id="14bc0-134">Rappresentazione client.</span><span class="sxs-lookup"><span data-stu-id="14bc0-134">Client impersonation.</span></span> <span data-ttu-id="14bc0-135">(IPsec rappresenta il contesto di sicurezza in cui viene creato il socket).</span><span class="sxs-lookup"><span data-stu-id="14bc0-135">(IPsec impersonates the security context under which the socket is created.)</span></span>
-   <span data-ttu-id="14bc0-136">Convalida del nome peer in ingresso e in uscita.</span><span class="sxs-lookup"><span data-stu-id="14bc0-136">Inbound and outbound peer name validation.</span></span> <span data-ttu-id="14bc0-137">Per ulteriori informazioni, vedere [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) .</span><span class="sxs-lookup"><span data-stu-id="14bc0-137">See [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) for more information.</span></span>

  
</dl>

<span data-ttu-id="14bc0-138">Per ulteriori informazioni su AuthIP, vedere anche:</span><span class="sxs-lookup"><span data-stu-id="14bc0-138">For more information on AuthIP, see also:</span></span>

<dl>

[<span data-ttu-id="14bc0-139">AuthIP in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="14bc0-139">AuthIP in Windows Vista</span></span>](https://www.microsoft.com/technet/community/columns/cableguy/cg0806.mspx)  
</dl>

## <a name="what-is-an-ipsec-policy"></a><span data-ttu-id="14bc0-140">Informazioni sui criteri IPsec</span><span class="sxs-lookup"><span data-stu-id="14bc0-140">What is an IPsec Policy</span></span>

<span data-ttu-id="14bc0-141">Un criterio IPsec è un set di regole che determinano il tipo di traffico IP che deve essere protetto tramite IPsec e come proteggere il traffico.</span><span class="sxs-lookup"><span data-stu-id="14bc0-141">An IPsec policy is a set of rules that determine which type of IP traffic needs to be secured using IPsec and how to secure that traffic.</span></span> <span data-ttu-id="14bc0-142">Solo un criterio IPsec è attivo in un computer contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="14bc0-142">Only one IPsec policy is active on a computer at one time.</span></span>

<span data-ttu-id="14bc0-143">Per ulteriori informazioni sull'implementazione dei criteri IPsec, aprire lo snap-in MMC Criteri di sicurezza locali (secpol. msc), premere F1 per visualizzare la guida, quindi selezionare Creazione e utilizzo di criteri IPsec dal sommario.</span><span class="sxs-lookup"><span data-stu-id="14bc0-143">To learn more about implementing IPsec policies, open the Local Security Policy MMC snap-in (secpol.msc), press F1 to display the Help, and then select Creating and Using IPsec Policies from the table of contents.</span></span>

<span data-ttu-id="14bc0-144">Per ulteriori informazioni sui criteri IPsec, vedere anche:</span><span class="sxs-lookup"><span data-stu-id="14bc0-144">For more information on IPsec policies, see also:</span></span>

<dl>

<span data-ttu-id="14bc0-145">[Panoramica dei concetti relativi ai criteri IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="14bc0-145">[Overview of IPsec Policy Concepts](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))</span></span>  
<span data-ttu-id="14bc0-146">[Descrizione di un criterio IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc781593(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="14bc0-146">[Description of an IPsec Policy](/previous-versions/windows/it-pro/windows-server-2003/cc781593(v=ws.10))</span></span>  
</dl>

## <a name="how-to-use-wfp-to-configure-ipsec-policies"></a><span data-ttu-id="14bc0-147">Come utilizzare WFP per configurare i criteri IPsec</span><span class="sxs-lookup"><span data-stu-id="14bc0-147">How to Use WFP to Configure IPsec Policies</span></span>

<span data-ttu-id="14bc0-148">L'implementazione Microsoft di IPsec usa la piattaforma filtro Windows per configurare i criteri IPsec.</span><span class="sxs-lookup"><span data-stu-id="14bc0-148">The Microsoft implementation of IPsec uses Windows Filtering Platform to setup IPsec policies.</span></span> <span data-ttu-id="14bc0-149">I criteri IPsec vengono implementati aggiungendo filtri a diversi livelli di PAM come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="14bc0-149">IPsec policies are implemented by adding filters at various WFP layers as follows.</span></span>

-   <span data-ttu-id="14bc0-150">Ai livelli FWPM \_ Layer \_ IKEEXT \_ V {4 \| 6} aggiungere filtri che specificano i criteri di negoziazione usati dai moduli di chiavi (IKE/AuthIP) durante gli scambi in modalità principale (mm).</span><span class="sxs-lookup"><span data-stu-id="14bc0-150">At the FWPM\_LAYER\_IKEEXT\_V{4\|6} layers add filters that specify the negotiation policies used by the keying modules (IKE/AuthIP) during Main Mode (MM) exchanges.</span></span> <span data-ttu-id="14bc0-151">I metodi di autenticazione e gli algoritmi di crittografia vengono specificati a livello di questi livelli.</span><span class="sxs-lookup"><span data-stu-id="14bc0-151">Authentication methods and cryptographic algorithms are specified at these layers.</span></span>
-   <span data-ttu-id="14bc0-152">Ai livelli FWPM \_ Layer \_ IPSec \_ V {4 \| 6} aggiungere filtri che specificano i criteri di negoziazione usati dai moduli di chiave in modalità rapida (QM) e gli scambi in modalità estesa (em).</span><span class="sxs-lookup"><span data-stu-id="14bc0-152">At the FWPM\_LAYER\_IPSEC\_V{4\|6} layers add filters that specify the negotiation policies used by the keying modules during Quick Mode (QM) and Extended Mode (EM) exchanges.</span></span> <span data-ttu-id="14bc0-153">Le intestazioni IPsec (AH/ESP) e gli algoritmi di crittografia vengono specificati a questi livelli.</span><span class="sxs-lookup"><span data-stu-id="14bc0-153">IPsec headers (AH/ESP) and cryptographic algorithms are specified at these layers.</span></span>

    <span data-ttu-id="14bc0-154">Un criterio di negoziazione viene specificato come contesto del provider di criteri associato al filtro.</span><span class="sxs-lookup"><span data-stu-id="14bc0-154">A negotiation policy is specified as a policy provider context associated with the filter.</span></span> <span data-ttu-id="14bc0-155">Il modulo di trasparenza enumera i contesti del provider di criteri in base alle caratteristiche del traffico e ottiene il criterio da utilizzare per la negoziazione di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="14bc0-155">The keying module enumerates the policy provider contexts based on the traffic characteristics and obtains the policy to use for the security negotiation.</span></span>

    > [!Note]  
    > <span data-ttu-id="14bc0-156">L'API PAM può essere usata per specificare direttamente le associazioni di sicurezza (SAs) e pertanto ignorare i criteri di negoziazione del modulo di chiave.</span><span class="sxs-lookup"><span data-stu-id="14bc0-156">The WFP API can be used to specify the Security Associations (SAs) directly and therefore to ignore the keying module negotiation policy.</span></span>

     

-   <span data-ttu-id="14bc0-157">Ai livelli del \_ trasporto in ingresso FWPM layer \_ \_ \_ v {4 \| 6} e FWPM \_ Layer trasporto in \_ uscita \_ \_ v {4 \| 6} livelli aggiungere filtri che richiamano i callout e determinano il flusso del traffico da proteggere.</span><span class="sxs-lookup"><span data-stu-id="14bc0-157">At the FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} and FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} layers add filters that invoke callouts and determine which traffic flow should be secured.</span></span>
-   <span data-ttu-id="14bc0-158">A livello di FWPM level \_ \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6} livelli Aggiungi filtri che implementano il filtro delle identità e i criteri per ogni applicazione.</span><span class="sxs-lookup"><span data-stu-id="14bc0-158">At the FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6} layers add filters that implement identity filtering and per-application policy.</span></span>

<span data-ttu-id="14bc0-159">Nel diagramma seguente viene illustrata l'interazione tra i vari componenti di WFP, rispetto all'operazione IPsec.</span><span class="sxs-lookup"><span data-stu-id="14bc0-159">The following diagram illustrates the interaction of the various WFP components, with respect to IPsec operation.</span></span>![configurazione IPSec con Windows Filtering Platform](images/ipsec-configuration.jpg)

<span data-ttu-id="14bc0-161">Una volta configurato IPsec, si integra con WFP ed estende le funzionalità di filtro WFP fornendo le informazioni da usare come condizioni di filtro ai livelli di autorizzazione di Application Layer Enforcement (ALE).</span><span class="sxs-lookup"><span data-stu-id="14bc0-161">Once IPsec is configured, it integrates with WFP and extends the WFP filtering capabilities by providing information to be used as filtering conditions at the Application Layer Enforcement (ALE) authorization layers.</span></span> <span data-ttu-id="14bc0-162">IPsec, ad esempio, fornisce l'utente remoto e l'identità del computer remoto, che viene esposta da WFP in ALE Connect e accettano i livelli di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="14bc0-162">For example, IPsec provides the remote user and remote machine identity, which WFP exposes at the ALE connect and accept authorization layers.</span></span> <span data-ttu-id="14bc0-163">Queste informazioni possono essere usate per l'autorizzazione di identità remota con granularità fine da un'implementazione del firewall basata su PAM.</span><span class="sxs-lookup"><span data-stu-id="14bc0-163">This information can be used for fine-grained remote identity authorization by a WFP-based firewall implementation.</span></span>

<span data-ttu-id="14bc0-164">Di seguito sono riportati i criteri di isolamento di esempio che possono essere implementati tramite IPsec:</span><span class="sxs-lookup"><span data-stu-id="14bc0-164">Below is a sample isolation policy that may be implemented using IPsec:</span></span>

-   <span data-ttu-id="14bc0-165">FWPM \_ Layer \_ IKEEXT \_ V {4 \| 6} livelli: autenticazione Kerberos.</span><span class="sxs-lookup"><span data-stu-id="14bc0-165">FWPM\_LAYER\_IKEEXT\_V{4\|6} layers – Kerberos authentication.</span></span>
-   <span data-ttu-id="14bc0-166">FWPM \_ Layer \_ IPSec \_ V {4 \| 6} livelli-Ah/SHA-1.</span><span class="sxs-lookup"><span data-stu-id="14bc0-166">FWPM\_LAYER\_IPSEC\_V{4\|6} layers – AH/SHA-1.</span></span>
-   <span data-ttu-id="14bc0-167">FWPM \_ Layer \_ \_ trasporto in ingresso \_ v {4 \| 6} e FWPM \_ Layer \_ \_ trasporto in uscita \_ v {4 \| 6} livelli-individuazione negoziazione per tutto il traffico di rete.</span><span class="sxs-lookup"><span data-stu-id="14bc0-167">FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} and FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} layers - negotiation discovery for all network traffic.</span></span>
-   <span data-ttu-id="14bc0-168">FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6} livelli-IPSec obbligatorio per tutto il traffico di rete.</span><span class="sxs-lookup"><span data-stu-id="14bc0-168">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6} layers - IPsec required for all network traffic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="14bc0-169">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="14bc0-169">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="14bc0-170">**Livelli WFP**</span><span class="sxs-lookup"><span data-stu-id="14bc0-170">**WFP Layers**</span></span>
</dt> <dt>

[<span data-ttu-id="14bc0-171">**Filtraggio degli identificatori del livello**</span><span class="sxs-lookup"><span data-stu-id="14bc0-171">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="14bc0-172">Livelli ALE</span><span class="sxs-lookup"><span data-stu-id="14bc0-172">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

<span data-ttu-id="14bc0-173">**Scenari di criteri IPsec implementati tramite l'API PAM:**</span><span class="sxs-lookup"><span data-stu-id="14bc0-173">**IPsec Policy Scenarios Implemented using WFP API:**</span></span>
</dt> <dt>

[<span data-ttu-id="14bc0-174">modalità di sicurezza trasporto</span><span class="sxs-lookup"><span data-stu-id="14bc0-174">Transport Mode</span></span>](regular-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="14bc0-175">Modalità trasporto individuazione negoziazione</span><span class="sxs-lookup"><span data-stu-id="14bc0-175">Negotiation Discovery Transport Mode</span></span>](negotiation-discovery-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="14bc0-176">Modalità di trasporto individuazione negoziazione in modalità limite</span><span class="sxs-lookup"><span data-stu-id="14bc0-176">Negotiation Discovery Transport Mode in Boundary Mode</span></span>](negotiation-discovery-transport-mode-in-boundary-mode.md)
</dt> <dt>

[<span data-ttu-id="14bc0-177">Modalità tunnel</span><span class="sxs-lookup"><span data-stu-id="14bc0-177">Tunnel Mode</span></span>](tunnel-mode.md)
</dt> <dt>

[<span data-ttu-id="14bc0-178">Crittografia garantita</span><span class="sxs-lookup"><span data-stu-id="14bc0-178">Guaranteed Encryption</span></span>](guaranteed-encryption.md)
</dt> <dt>

[<span data-ttu-id="14bc0-179">Autorizzazione identità remota</span><span class="sxs-lookup"><span data-stu-id="14bc0-179">Remote Identity Authorization</span></span>](remote-identity-authorization.md)
</dt> <dt>

[<span data-ttu-id="14bc0-180">SAs manuale IPsec</span><span class="sxs-lookup"><span data-stu-id="14bc0-180">Manual IPsec SAs</span></span>](manual-ipsec-sas.md)
</dt> <dt>

[<span data-ttu-id="14bc0-181">Esenzioni IKE/AuthIP</span><span class="sxs-lookup"><span data-stu-id="14bc0-181">IKE/AuthIP Exemptions</span></span>](ike-exemptions.md)
</dt> <dt>

<span data-ttu-id="14bc0-182">**Soluzioni IPsec:**</span><span class="sxs-lookup"><span data-stu-id="14bc0-182">**IPsec Solutions:**</span></span>
</dt> <dt>

<span data-ttu-id="14bc0-183">[Isolamento del dominio e del server](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="14bc0-183">[Server and Domain Isolation](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))</span></span>
</dt> </dl>

 

 