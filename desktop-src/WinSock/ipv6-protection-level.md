---
description: L' \_ \_ opzione socket del livello di protezione IPv6 consente agli sviluppatori di inserire restrizioni di accesso sui socket IPv6.
ms.assetid: bfb934b3-1e86-431f-a21c-880048d32d35
title: IPV6_PROTECTION_LEVEL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e2a8dd70bb1fb5b21f74f8939f11da0d9e2a3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306938"
---
# <a name="ipv6_protection_level"></a><span data-ttu-id="ec323-103">\_Livello di protezione IPv6 \_</span><span class="sxs-lookup"><span data-stu-id="ec323-103">IPV6\_PROTECTION\_LEVEL</span></span>

<span data-ttu-id="ec323-104">L' \_ \_ opzione socket del livello di protezione IPv6 consente agli sviluppatori di inserire restrizioni di accesso sui socket IPv6.</span><span class="sxs-lookup"><span data-stu-id="ec323-104">The IPV6\_PROTECTION\_LEVEL socket option enables developers to place access restrictions on IPv6 sockets.</span></span> <span data-ttu-id="ec323-105">Tali restrizioni consentono a un'applicazione in esecuzione su una LAN privata di proteggersi in modo semplice e affidabile da attacchi esterni.</span><span class="sxs-lookup"><span data-stu-id="ec323-105">Such restrictions enable an application running on a private LAN to simply and robustly harden itself against external attacks.</span></span> <span data-ttu-id="ec323-106">L' \_ \_ opzione socket del livello di protezione IPv6 allarga o restringe l'ambito di un socket in ascolto, abilitando l'accesso illimitato da parte di utenti pubblici e privati, quando appropriato, o limitando l'accesso solo allo stesso sito, in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="ec323-106">The IPV6\_PROTECTION\_LEVEL socket option widens or narrows the scope of a listening socket, enabling unrestricted access from public and private users when appropriate, or restricting access only to the same site, as required.</span></span>

<span data-ttu-id="ec323-107">Il \_ livello di protezione IPv6 \_ dispone attualmente di tre livelli di protezione definiti.</span><span class="sxs-lookup"><span data-stu-id="ec323-107">IPV6\_PROTECTION\_LEVEL currently has three defined protection levels.</span></span>



| <span data-ttu-id="ec323-108">Livello di protezione</span><span class="sxs-lookup"><span data-stu-id="ec323-108">Protection level</span></span>                                                                                                                                 | <span data-ttu-id="ec323-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec323-109">Description</span></span>                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec323-110"><span id="PROTECTION_LEVEL_UNRESTRICTED"></span><span id="protection_level_unrestricted"></span>livello di protezione \_ \_ senza restrizioni</span><span class="sxs-lookup"><span data-stu-id="ec323-110"><span id="PROTECTION_LEVEL_UNRESTRICTED"></span><span id="protection_level_unrestricted"></span>PROTECTION\_LEVEL\_UNRESTRICTED</span></span><br/>       | <span data-ttu-id="ec323-111">Usato dalle applicazioni progettate per operare su Internet, incluse le applicazioni che sfruttano le funzionalità di attraversamento NAT IPv6 incorporate in Windows (ad esempio, Teredo).</span><span class="sxs-lookup"><span data-stu-id="ec323-111">Used by applications designed to operate across the Internet, including applications taking advantage of IPv6 NAT traversal capabilities built into Windows (Teredo, for example).</span></span> <span data-ttu-id="ec323-112">Tali applicazioni possono aggirare i firewall IPv4 e pertanto le applicazioni devono essere protette contro gli attacchi provenienti da Internet diretti alla porta aperta.</span><span class="sxs-lookup"><span data-stu-id="ec323-112">These applications may bypass IPv4 firewalls, so applications must be hardened against Internet attacks directed at the opened port.</span></span><br/> |
| <span data-ttu-id="ec323-113"><span id="PROTECTION_LEVEL_EDGERESTRICTED"></span><span id="protection_level_edgerestricted"></span>livello di protezione \_ \_ EDGERESTRICTED</span><span class="sxs-lookup"><span data-stu-id="ec323-113"><span id="PROTECTION_LEVEL_EDGERESTRICTED"></span><span id="protection_level_edgerestricted"></span>PROTECTION\_LEVEL\_EDGERESTRICTED</span></span><br/> | <span data-ttu-id="ec323-114">Utilizzato dalle applicazioni progettate per operare in Internet.</span><span class="sxs-lookup"><span data-stu-id="ec323-114">Used by applications designed to operate across the Internet.</span></span> <span data-ttu-id="ec323-115">Questa impostazione non consente l'attraversamento NAT tramite l'implementazione di Windows Teredo.</span><span class="sxs-lookup"><span data-stu-id="ec323-115">This setting does not allow NAT traversal using the Windows Teredo implementation.</span></span> <span data-ttu-id="ec323-116">Tali applicazioni possono aggirare i firewall IPv4 e pertanto le applicazioni devono essere protette contro gli attacchi provenienti da Internet diretti alla porta aperta.</span><span class="sxs-lookup"><span data-stu-id="ec323-116">These applications may bypass IPv4 firewalls, so applications must be hardened against Internet attacks directed at the opened port.</span></span><br/>                                   |
| <span data-ttu-id="ec323-117"><span id="PROTECTION_LEVEL_RESTRICTED"></span><span id="protection_level_restricted"></span>livello di protezione \_ \_ limitato</span><span class="sxs-lookup"><span data-stu-id="ec323-117"><span id="PROTECTION_LEVEL_RESTRICTED"></span><span id="protection_level_restricted"></span>PROTECTION\_LEVEL\_RESTRICTED</span></span><br/>             | <span data-ttu-id="ec323-118">Utilizzato dalle applicazioni Intranet che non implementano scenari Internet.</span><span class="sxs-lookup"><span data-stu-id="ec323-118">Used by intranet applications that do not implement Internet scenarios.</span></span> <span data-ttu-id="ec323-119">Queste applicazioni non sono in genere testate o protette da attacchi analoghi a quelli provenienti da Internet.</span><span class="sxs-lookup"><span data-stu-id="ec323-119">These applications are generally not tested or hardened against Internet-style attacks.</span></span><br/> <span data-ttu-id="ec323-120">Questa impostazione limiterà il traffico ricevuto solo a quello locale rispetto al collegamento.</span><span class="sxs-lookup"><span data-stu-id="ec323-120">This setting will limit the received traffic to link-local only.</span></span><br/>                                                                             |



 

<span data-ttu-id="ec323-121">Nell'esempio di codice seguente vengono forniti i valori definiti per ogni:</span><span class="sxs-lookup"><span data-stu-id="ec323-121">The following code example provides the defined values for each:</span></span>

``` syntax
#define PROTECTION_LEVEL_UNRESTRICTED   10  /* for peer-to-peer apps */
#define PROTECTION_LEVEL_EDGERESTRICTED 20  /* Same as unrestricted, except for Teredo  */
#define PROTECTION_LEVEL_RESTRICTED     30  /* for Intranet apps     */
```

<span data-ttu-id="ec323-122">Questi valori si escludono reciprocamente e non possono essere combinati in una singola chiamata di funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) .</span><span class="sxs-lookup"><span data-stu-id="ec323-122">These values are mutually exclusive, and cannot be combined in a single [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function call.</span></span> <span data-ttu-id="ec323-123">Gli altri valori per questa opzione socket sono riservati.</span><span class="sxs-lookup"><span data-stu-id="ec323-123">Other values for this socket option are reserved.</span></span> <span data-ttu-id="ec323-124">I livelli di protezione sono validi solo per le connessioni in ingresso.</span><span class="sxs-lookup"><span data-stu-id="ec323-124">These protection levels apply only to incoming connections.</span></span> <span data-ttu-id="ec323-125">L'impostazione di questa opzione socket non ha alcun effetto sui pacchetti o le connessioni in uscita.</span><span class="sxs-lookup"><span data-stu-id="ec323-125">Setting this socket option has no effect on outbound packets or connections.</span></span>

<span data-ttu-id="ec323-126">In Windows 7 e Windows Server 2008 R2, il valore predefinito per il \_ livello di protezione IPv6 non \_ è specificato e il **livello di protezione \_ \_ predefinito** è impostato su-1, un valore non valido per il \_ livello di protezione IPv6 \_ .</span><span class="sxs-lookup"><span data-stu-id="ec323-126">On Windows 7 and Windows Server 2008 R2, the default value for IPV6\_PROTECTION\_LEVEL is unspecified and **PROTECTION\_LEVEL\_DEFAULT** is defined to -1, an illegal value for IPV6\_PROTECTION\_LEVEL.</span></span>

<span data-ttu-id="ec323-127">In Windows Vista e Windows Server 2008, il valore predefinito per il \_ livello di protezione IPv6 \_ è **\_ \_ senza restrizioni** e **il \_ livello \_ di protezione predefinito** è impostato su-1, un valore non valido per il \_ livello di protezione IPv6 \_ .</span><span class="sxs-lookup"><span data-stu-id="ec323-127">On Windows Vista and Windows Server 2008, the default value for IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_UNRESTRICTED** and **PROTECTION\_LEVEL\_DEFAULT** is defined to -1, an illegal value for IPV6\_PROTECTION\_LEVEL.</span></span>

<span data-ttu-id="ec323-128">In Windows Server 2003 e Windows XP, il valore predefinito per il livello di protezione IPV6 è il livello \_ \_ di protezione **\_ \_ EDGERESTRICTED** e il **livello di protezione \_ \_ predefinito** è definito come **\_ \_ EDGERESTRICTED** del livello di protezione.</span><span class="sxs-lookup"><span data-stu-id="ec323-128">On Windows Server 2003 and Windows XP, the default value for IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_EDGERESTRICTED** and **PROTECTION\_LEVEL\_DEFAULT** is defined to be **PROTECTION\_LEVEL\_EDGERESTRICTED**.</span></span>

> [!Note]  
> <span data-ttu-id="ec323-129">\_ \_ È necessario impostare l'opzione socket del livello di protezione IPv6 prima che il socket venga associato.</span><span class="sxs-lookup"><span data-stu-id="ec323-129">The IPV6\_PROTECTION\_LEVEL socket option should be set before the socket is bound.</span></span> <span data-ttu-id="ec323-130">In caso contrario, i pacchetti ricevuti tra le chiamate [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) e [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) saranno conformi al **livello di protezione \_ \_ EDGERESTRICTED** e possono essere recapitati all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ec323-130">Otherwise, packets received between [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) and [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) calls will conform to **PROTECTION\_LEVEL\_EDGERESTRICTED**, and may be delivered to the application.</span></span>

 

<span data-ttu-id="ec323-131">Nella tabella seguente viene descritto l'effetto dell'applicazione di ogni livello di protezione a un socket in ascolto.</span><span class="sxs-lookup"><span data-stu-id="ec323-131">The following table describes the effect of applying each protection level to a listening socket.</span></span>

<span data-ttu-id="ec323-132">Livello di protezione</span><span class="sxs-lookup"><span data-stu-id="ec323-132">Protection level</span></span>

<span data-ttu-id="ec323-133">Traffico in ingresso consentito</span><span class="sxs-lookup"><span data-stu-id="ec323-133">Incoming traffic permitted</span></span>

<span data-ttu-id="ec323-134">Stesso sito</span><span class="sxs-lookup"><span data-stu-id="ec323-134">Same site</span></span>

<span data-ttu-id="ec323-135">Esterno</span><span class="sxs-lookup"><span data-stu-id="ec323-135">External</span></span>

<span data-ttu-id="ec323-136">Attraversamento NAT (Teredo)</span><span class="sxs-lookup"><span data-stu-id="ec323-136">NAT traversal (Teredo)</span></span>

<span data-ttu-id="ec323-137">livello di protezione \_ \_ limitato</span><span class="sxs-lookup"><span data-stu-id="ec323-137">PROTECTION\_LEVEL\_RESTRICTED</span></span>

<span data-ttu-id="ec323-138">Sì</span><span class="sxs-lookup"><span data-stu-id="ec323-138">Yes</span></span>

<span data-ttu-id="ec323-139">No</span><span class="sxs-lookup"><span data-stu-id="ec323-139">No</span></span>

<span data-ttu-id="ec323-140">No</span><span class="sxs-lookup"><span data-stu-id="ec323-140">No</span></span>

<span data-ttu-id="ec323-141">livello di protezione \_ \_ EDGERESTRICTED</span><span class="sxs-lookup"><span data-stu-id="ec323-141">PROTECTION\_LEVEL\_EDGERESTRICTED</span></span>

<span data-ttu-id="ec323-142">Sì</span><span class="sxs-lookup"><span data-stu-id="ec323-142">Yes</span></span>

<span data-ttu-id="ec323-143">Sì</span><span class="sxs-lookup"><span data-stu-id="ec323-143">Yes</span></span>

<span data-ttu-id="ec323-144">No</span><span class="sxs-lookup"><span data-stu-id="ec323-144">No</span></span>

<span data-ttu-id="ec323-145">livello di protezione \_ \_ senza restrizioni</span><span class="sxs-lookup"><span data-stu-id="ec323-145">PROTECTION\_LEVEL\_UNRESTRICTED</span></span>

<span data-ttu-id="ec323-146">Sì</span><span class="sxs-lookup"><span data-stu-id="ec323-146">Yes</span></span>

<span data-ttu-id="ec323-147">Sì</span><span class="sxs-lookup"><span data-stu-id="ec323-147">Yes</span></span>

<span data-ttu-id="ec323-148">Sì</span><span class="sxs-lookup"><span data-stu-id="ec323-148">Yes</span></span>



 

<span data-ttu-id="ec323-149">Nella tabella precedente la stessa colonna del **sito** è una combinazione dei seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="ec323-149">In the table above, the **Same site** column is a combination of the following:</span></span>

-   <span data-ttu-id="ec323-150">Collega indirizzi locali</span><span class="sxs-lookup"><span data-stu-id="ec323-150">Link local addresses</span></span>
-   <span data-ttu-id="ec323-151">Indirizzi locali del sito</span><span class="sxs-lookup"><span data-stu-id="ec323-151">Site Local addresses</span></span>
-   <span data-ttu-id="ec323-152">Indirizzi globali noti come appartenenti allo stesso sito (che corrisponde alla tabella del prefisso del sito)</span><span class="sxs-lookup"><span data-stu-id="ec323-152">Global addresses known to belong to the same site (matching the site prefix table)</span></span>

<span data-ttu-id="ec323-153">In Windows 7 e Windows Server 2008 R2, il valore predefinito per il \_ livello di protezione IPv6 non \_ è specificato.</span><span class="sxs-lookup"><span data-stu-id="ec323-153">On Windows 7 and Windows Server 2008 R2, the default value for IPV6\_PROTECTION\_LEVEL is unspecified.</span></span> <span data-ttu-id="ec323-154">Se sul computer locale non è installato alcun software firewall compatibile con l'attraversamento del perimetro (Windows Firewall è disabilitato o è installato un altro firewall che ignora il traffico Teredo), si riceverà il traffico Teredo solo se si imposta l' \_ opzione del socket del livello di protezione IPv6 sul \_ **livello di protezione \_ \_ senza restrizioni**.</span><span class="sxs-lookup"><span data-stu-id="ec323-154">If there is no edge-traversal aware firewall software installed on the local computer (Windows firewall is disabled or some other firewall is installed that ignores Teredo traffic), you will receive Teredo traffic only if you set the IPV6\_PROTECTION\_LEVEL socket option to **PROTECTION\_LEVEL\_UNRESTRICTED**.</span></span> <span data-ttu-id="ec323-155">Tuttavia, Windows Firewall o qualsiasi criterio del firewall compatibile con attraversamento del perimetro potrebbe ignorare questa opzione in base alle impostazioni dei criteri per il firewall.</span><span class="sxs-lookup"><span data-stu-id="ec323-155">However, Windows firewall or any edge-traversal aware firewall policy may ignore this option based on policy settings for the firewall.</span></span> <span data-ttu-id="ec323-156">Impostando questa opzione del socket **sul \_ livello di protezione \_ senza restrizioni**, l'applicazione comunica l'intento esplicito di ricevere il traffico attraversato da Edge dal firewall host installato nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="ec323-156">By setting this socket option to **PROTECTION\_LEVEL\_UNRESTRICTED**, the application is communicating its explicit intent to receive edge traversed traffic by the host firewall installed on the local machine.</span></span> <span data-ttu-id="ec323-157">Quindi, se è installato un firewall host compatibile con l'attraversamento del perimetro, avrà la decisione finale sull'accettazione di un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="ec323-157">So if there is an edge-traversal aware host firewall installed, it will have the final decision on accepting a packet.</span></span> <span data-ttu-id="ec323-158">Per impostazione predefinita, senza set di opzioni socket:</span><span class="sxs-lookup"><span data-stu-id="ec323-158">By default, without any socket option set:</span></span>

-   <span data-ttu-id="ec323-159">o se Windows Firewall è abilitato (o se è installato un altro firewall host che supporta l'attraversamento del perimetro) nel computer locale, qualunque sia l'applicazione applicata verrà osservato.</span><span class="sxs-lookup"><span data-stu-id="ec323-159">o If Windows firewall is enabled (or another edge-traversal aware host firewall is installed) on the local computer, whatever it enforces will be observed.</span></span> <span data-ttu-id="ec323-160">Il firewall host in grado di riconoscere il bordo tipico bloccherà il traffico Teredo per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="ec323-160">Typical edge-traversal aware host firewall will block Teredo traffic by default.</span></span> <span data-ttu-id="ec323-161">Pertanto, le applicazioni osserveranno il valore predefinito come se si trattasse di un **livello di protezione \_ \_ EDGERESTRICTED**.</span><span class="sxs-lookup"><span data-stu-id="ec323-161">Therefore applications will observe the default as if it was **PROTECTION\_LEVEL\_EDGERESTRICTED**.</span></span>
-   <span data-ttu-id="ec323-162">o se Windows Firewall non è abilitato e nessun altro firewall host compatibile con l'attraversamento del perimetro è installato nel sistema locale, il valore predefinito sarà il **livello di protezione \_ \_ EDGERESTRICTED**.</span><span class="sxs-lookup"><span data-stu-id="ec323-162">o If Windows firewall is not enabled and no other edge-traversal aware host firewall is installed on the local system, the default will be **PROTECTION\_LEVEL\_EDGERESTRICTED**.</span></span>

<span data-ttu-id="ec323-163">In Windows Vista e Windows Server 2008, il valore predefinito per il \_ livello di protezione IPv6 \_ è **\_ \_ Unrestricted Level Protection**.</span><span class="sxs-lookup"><span data-stu-id="ec323-163">On Windows Vista and Windows Server 2008, the default value for IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_UNRESTRICTED**.</span></span> <span data-ttu-id="ec323-164">Tuttavia, il valore effettivo varia a seconda che Windows Firewall sia abilitato o meno.</span><span class="sxs-lookup"><span data-stu-id="ec323-164">But the effective value depends on whether Windows firewall is enabled.</span></span> <span data-ttu-id="ec323-165">Windows Firewall è compatibile con l'attraversamento del perimetro (compatibile con Teredo), indipendentemente dal valore impostato per il livello di protezione IPV6 e ignora se il livello di protezione \_ \_ IPv6 \_ \_ è **\_ \_ senza restrizioni**.</span><span class="sxs-lookup"><span data-stu-id="ec323-165">The Windows firewall is edge-traversal aware (Teredo aware), no matter what value is set for the IPV6\_PROTECTION\_LEVEL and ignores if IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_UNRESTRICTED**.</span></span> <span data-ttu-id="ec323-166">Il valore effettivo dipende quindi dal criterio del firewall.</span><span class="sxs-lookup"><span data-stu-id="ec323-166">So the effective value depends on the firewall policy.</span></span> <span data-ttu-id="ec323-167">Quando Windows Firewall è disabilitato e nel computer locale non è installato altro firewall per l'attraversamento del perimetro, il valore predefinito per il \_ livello di protezione IPv6 \_ è senza **\_ \_ restrizioni**.</span><span class="sxs-lookup"><span data-stu-id="ec323-167">When Windows firewall is disabled and no other edge-traversal aware firewall is installed on the local computer, the default value for IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_UNRESTRICTED**.</span></span>

<span data-ttu-id="ec323-168">In Windows Server 2003 e Windows XP, il valore predefinito per il \_ livello di protezione IPv6 \_ è il livello di **protezione \_ \_ EDGERESTRICTED**.</span><span class="sxs-lookup"><span data-stu-id="ec323-168">On Windows Server 2003 and Windows XP, the default value for IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_EDGERESTRICTED**.</span></span> <span data-ttu-id="ec323-169">A meno che non sia stata impostata \_ l' \_ opzione socket del livello di protezione IPv6 sul **livello di protezione senza \_ \_ restrizioni**, non si riceverà alcun traffico Teredo.</span><span class="sxs-lookup"><span data-stu-id="ec323-169">Unless you have set the IPV6\_PROTECTION\_LEVEL socket option to **PROTECTION\_LEVEL\_UNRESTRICTED**, you would not receive any Teredo traffic.</span></span>

<span data-ttu-id="ec323-170">A seconda del \_ \_ livello di protezione IPv6, un'applicazione che richiede traffico non richiesto da Internet potrebbe non essere in grado di ricevere traffico non richiesto.</span><span class="sxs-lookup"><span data-stu-id="ec323-170">Depending on the IPV6\_PROTECTION\_LEVEL, an application that requires unsolicited traffic from the Internet may not be capable of receiving unsolicited traffic.</span></span> <span data-ttu-id="ec323-171">Tuttavia, questi requisiti non sono necessari per la ricezione di traffico richiesto sull'interfaccia Teredo di Windows.</span><span class="sxs-lookup"><span data-stu-id="ec323-171">However, these requirements are not necessary for receiving solicited traffic over the Windows Teredo interface.</span></span> <span data-ttu-id="ec323-172">Per altri dettagli sull'interazione con Teredo, vedere [ricezione di traffico richiesto su Teredo](../teredo/receiving-solicited-traffic-over-teredo.md).</span><span class="sxs-lookup"><span data-stu-id="ec323-172">For more details on the interaction with Teredo, see [Receiving Solicited Traffic Over Teredo](../teredo/receiving-solicited-traffic-over-teredo.md).</span></span>

<span data-ttu-id="ec323-173">Quando i pacchetti in ingresso o le connessioni vengono rifiutate a causa del livello di protezione impostato, il rifiuto viene gestito come se nessuna applicazione fosse in ascolto su tale socket.</span><span class="sxs-lookup"><span data-stu-id="ec323-173">When incoming packets or connections are refused due to the set protection level, rejection is handled as if no application was listening on that socket.</span></span>

> [!Note]
>
> <span data-ttu-id="ec323-174">L' \_ \_ opzione socket del livello di protezione IPv6 non pone necessariamente restrizioni di accesso sui socket IPv6 o limita l'attraversamento NAT usando un metodo diverso da Windows Teredo o persino usando un'altra implementazione di Teredo da parte di un altro fornitore.</span><span class="sxs-lookup"><span data-stu-id="ec323-174">The IPV6\_PROTECTION\_LEVEL socket option does not necessarily place access restrictions on IPv6 sockets or restrict NAT traversal using some method other than Windows Teredo or even using another implementation of Teredo by another vendor.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ec323-175">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ec323-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec323-176">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="ec323-176">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="ec323-177">Ricezione di traffico richiesto su Teredo</span><span class="sxs-lookup"><span data-stu-id="ec323-177">Receiving Solicited Traffic Over Teredo</span></span>](../teredo/receiving-solicited-traffic-over-teredo.md)
</dt> <dt>

[<span data-ttu-id="ec323-178">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="ec323-178">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> </dl>

 

 
