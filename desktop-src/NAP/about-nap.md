---
title: Informazioni su NAP
description: Informazioni su NAP
ms.assetid: c5dc4956-dcb7-4fcf-b4cc-2fac016427dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac4227e1291945fa2d3b7876df27c2cc18cdfde2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707825"
---
# <a name="about-nap"></a><span data-ttu-id="4ca09-103">Informazioni su NAP</span><span class="sxs-lookup"><span data-stu-id="4ca09-103">About NAP</span></span>

> [!Note]  
> <span data-ttu-id="4ca09-104">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="4ca09-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="4ca09-105">Protezione accesso alla rete (NAP) è progettato per consentire agli amministratori di mantenere l'integrità dei computer nella rete, che a sua volta consente di mantenere l'integrità complessiva della rete.</span><span class="sxs-lookup"><span data-stu-id="4ca09-105">Network Access Protection (NAP) is designed to help administrators maintain the health of the computers on the network, which in turns helps maintain the overall integrity of the network.</span></span> <span data-ttu-id="4ca09-106">Non è progettato per proteggere una rete da utenti malintenzionati.</span><span class="sxs-lookup"><span data-stu-id="4ca09-106">It is not designed to secure a network from malicious users.</span></span> <span data-ttu-id="4ca09-107">Se, ad esempio, un computer dispone di tutto il software e le configurazioni necessarie per i criteri di accesso alla rete, il computer viene considerato integro o conforme e viene concesso l'accesso appropriato alla rete.</span><span class="sxs-lookup"><span data-stu-id="4ca09-107">For example, if a computer has all the software and configurations that the network access policy requires, the computer is considered healthy or compliant, and it will be granted the appropriate access to the network.</span></span> <span data-ttu-id="4ca09-108">NAP non impedisce a un utente autorizzato con un computer conforme di caricare un programma dannoso in rete o di impegnarsi in un altro comportamento non appropriato.</span><span class="sxs-lookup"><span data-stu-id="4ca09-108">NAP does not prevent an authorized user with a compliant computer from uploading a malicious program to the network or engaging in other inappropriate behavior.</span></span>

<span data-ttu-id="4ca09-109">Per proteggere l'accesso a una rete, un'infrastruttura di rete deve fornire le seguenti aree di funzionalità:</span><span class="sxs-lookup"><span data-stu-id="4ca09-109">To protect access to a network, a network infrastructure needs to provide the following areas of functionality:</span></span>

-   <span data-ttu-id="4ca09-110">Convalida dell'integrità: determina se i computer sono conformi ai requisiti di integrità del sistema.</span><span class="sxs-lookup"><span data-stu-id="4ca09-110">Health validation: Determines whether the computers are compliant with system health requirements.</span></span>
-   <span data-ttu-id="4ca09-111">Restrizione di rete: limita l'accesso alla rete o alla comunicazione per i client che non sono conformi ai requisiti di integrità del sistema.</span><span class="sxs-lookup"><span data-stu-id="4ca09-111">Network restriction: Restricts access to the network or communication for clients that do not comply with system health requirements.</span></span>
-   <span data-ttu-id="4ca09-112">Monitoraggio e aggiornamento: fornisce gli aggiornamenti necessari per consentire al computer di correggere lo stato di integrità non conforme.</span><span class="sxs-lookup"><span data-stu-id="4ca09-112">Remediation: Provides necessary updates to allow the computer to correct its noncompliant health state.</span></span>
-   <span data-ttu-id="4ca09-113">Conformità continua: consente l'accesso alla rete purché il computer dell'utente soddisfi i requisiti dei criteri di integrità.</span><span class="sxs-lookup"><span data-stu-id="4ca09-113">Ongoing compliance: Permits access to the network as long as the user's computer meets health policy requirements.</span></span>

<span data-ttu-id="4ca09-114">Windows XP con Service Pack 3 (SP3), Windows Vista e Windows Server 2008 forniscono metodi di imposizione di protezione accesso alla rete per la configurazione dell'indirizzo Dynamic Host Configuration Protocol (DHCP), connessioni VPN (Virtual Private Network) basate sull'accesso remoto, connessioni cablate e wireless autenticate tramite IEEE 802.1 X e comunicazioni basate su Internet Protocol Security (IPsec).</span><span class="sxs-lookup"><span data-stu-id="4ca09-114">Windows XP with Service Pack 3 (SP3), Windows Vista, and Windows Server 2008 provide NAP enforcement methods for Dynamic Host Configuration Protocol (DHCP) address configuration, remote access-based virtual private network (VPN) connections, IEEE 802.1X-authenticated wired and wireless connections, and Internet Protocol security (IPsec)-based communications.</span></span> <span data-ttu-id="4ca09-115">La piattaforma NAP supporta inoltre un'architettura in cui la convalida dell'integrità, la restrizione di rete, la correzione e la conformità continua sono supportate da componenti aggiuntivi che possono essere forniti da fornitori di software di terze parti o da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4ca09-115">The NAP platform additionally supports an architecture through which health validation, network restriction, remediation, and ongoing compliance are supported by additional components that can be supplied by third-party software vendors or by Microsoft.</span></span>

<span data-ttu-id="4ca09-116">La piattaforma NAP include i componenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="4ca09-116">The NAP platform includes the following components:</span></span>

-   [<span data-ttu-id="4ca09-117">Architettura client NAP</span><span class="sxs-lookup"><span data-stu-id="4ca09-117">NAP Client Architecture</span></span>](nap-client-architecture.md)
-   [<span data-ttu-id="4ca09-118">Architettura lato server NAP</span><span class="sxs-lookup"><span data-stu-id="4ca09-118">NAP Server-side Architecture</span></span>](nap-server-side-architecture.md)
-   [<span data-ttu-id="4ca09-119">Comunicazione tra client NAP e componenti lato server</span><span class="sxs-lookup"><span data-stu-id="4ca09-119">NAP Client and Server-side Component Communication</span></span>](nap-client-and-server-side-component-communication.md)

<span data-ttu-id="4ca09-120">Il client di protezione accesso alla rete richiede Windows Vista, Windows XP con SP3 o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="4ca09-120">The NAP client requires Windows Vista, Windows XP with SP3, or Windows Server 2008.</span></span> <span data-ttu-id="4ca09-121">Il server criteri di integrità protezione accesso alla rete e i punti di imposizione di protezione accesso alla rete per DHCP, VPN e IPsec richiedono Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="4ca09-121">The NAP health policy server and NAP enforcement points for DHCP, VPN, and IPsec enforcement require Windows Server 2008.</span></span>

 

 




