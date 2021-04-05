---
title: Protezione accesso alla rete
description: Nota la piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10, protezione accesso alla rete (NAP) è un set di componenti del sistema operativo che forniscono una piattaforma per l'accesso protetto alle reti private.
ms.assetid: f562f5f1-c05a-4e4e-bcd9-a302c61f2a5e
keywords:
- Protezione accesso alla rete
- Protezione accesso alla rete, pagina iniziale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b99348428a867be5bf846fd40b030b844460cdc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709802"
---
# <a name="network-access-protection"></a><span data-ttu-id="5167c-105">Protezione accesso alla rete</span><span class="sxs-lookup"><span data-stu-id="5167c-105">Network Access Protection</span></span>

## <a name="purpose"></a><span data-ttu-id="5167c-106">Scopo</span><span class="sxs-lookup"><span data-stu-id="5167c-106">Purpose</span></span>

> [!Note]  
> <span data-ttu-id="5167c-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="5167c-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5167c-108">Protezione accesso alla rete (NAP) è un set di componenti del sistema operativo che forniscono una piattaforma per l'accesso protetto alle reti private.</span><span class="sxs-lookup"><span data-stu-id="5167c-108">Network Access Protection (NAP) is a set of operating system components that provide a platform for protected access to private networks.</span></span> <span data-ttu-id="5167c-109">La piattaforma NAP fornisce un modo integrato per valutare lo stato di integrità del sistema di un client di rete che tenta di connettersi a una rete o di comunicare in una rete e di limitare l'accesso del client di rete fino a quando non sono stati soddisfatti i requisiti dei criteri di integrità.</span><span class="sxs-lookup"><span data-stu-id="5167c-109">The NAP platform provides an integrated way of evaluating the system health state of a network client that is attempting to connect to or communicate on a network and restricting the access of the network client until health policy requirements have been met.</span></span>

<span data-ttu-id="5167c-110">NAP è una piattaforma estendibile che fornisce un'infrastruttura e un set di API per l'aggiunta di componenti che archiviano, segnalano, convalidano e correggono lo stato di integrità del sistema di un computer.</span><span class="sxs-lookup"><span data-stu-id="5167c-110">NAP is an extensible platform that provides an infrastructure and an API set for adding components that store, report, validate, and correct a computer's system health state.</span></span> <span data-ttu-id="5167c-111">La piattaforma NAP non fornisce componenti per accumulare e valutare gli attributi dello stato di integrità di un computer.</span><span class="sxs-lookup"><span data-stu-id="5167c-111">By itself, the NAP platform does not provide components to accumulate and evaluate attributes of a computer's health state.</span></span> <span data-ttu-id="5167c-112">Altri componenti, noti come System Health Agent (SHAs) e convalida integrità sistema (SHV), forniscono la convalida dei criteri di rete e la conformità dei criteri di rete.</span><span class="sxs-lookup"><span data-stu-id="5167c-112">Other components, known as system health agents (SHAs) and system health validators (SHVs), provide network policy validation and network policy compliance.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="5167c-113">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="5167c-113">Where applicable</span></span>

<span data-ttu-id="5167c-114">NAP è progettato per essere estendibile.</span><span class="sxs-lookup"><span data-stu-id="5167c-114">NAP is designed to be extensible.</span></span> <span data-ttu-id="5167c-115">Può interagire con qualsiasi software fornitore che fornisce SHAs e SHV o che riconosce il set di API pubblicate.</span><span class="sxs-lookup"><span data-stu-id="5167c-115">It can interoperate with any vendor software that provides SHAs and SHVs or that recognizes its published API set.</span></span> <span data-ttu-id="5167c-116">NAP consente di fornire una soluzione per gli scenari comuni seguenti:</span><span class="sxs-lookup"><span data-stu-id="5167c-116">NAP helps provide a solution for the following common scenarios:</span></span>

-   <span data-ttu-id="5167c-117">Controllare l'integrità e lo stato dei computer portatili mobili.</span><span class="sxs-lookup"><span data-stu-id="5167c-117">Check the health and status of roaming laptops.</span></span>
-   <span data-ttu-id="5167c-118">Verificare l'integrità dei computer desktop.</span><span class="sxs-lookup"><span data-stu-id="5167c-118">Ensure the health of desktop computers.</span></span>
-   <span data-ttu-id="5167c-119">Verificare la conformità e l'integrità dei computer in uffici remoti.</span><span class="sxs-lookup"><span data-stu-id="5167c-119">Verify the compliance and health of computers in remote offices.</span></span>
-   <span data-ttu-id="5167c-120">Determinare l'integrità dei portatili in visita.</span><span class="sxs-lookup"><span data-stu-id="5167c-120">Determine the health of visiting laptops.</span></span>
-   <span data-ttu-id="5167c-121">Verificare la conformità e l'integrità dei computer domestici non gestiti.</span><span class="sxs-lookup"><span data-stu-id="5167c-121">Verify the compliance and health of unmanaged home computers.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="5167c-122">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="5167c-122">Developer audience</span></span>

<span data-ttu-id="5167c-123">L'API NAP è progettata per gli sviluppatori C/C++.</span><span class="sxs-lookup"><span data-stu-id="5167c-123">The NAP API is designed for C/C++ developers.</span></span> <span data-ttu-id="5167c-124">Per i metodi di imposizione di protezione accesso alla rete, i programmatori devono conoscere i protocolli e le tecnologie di rete, ad esempio Remote Authentication Dial-in User Service (RADIUS), Dynamic Host Configuration Protocol (DHCP), reti private virtuali (VPN), lo standard IEEE 802.1 X per l'accesso cablato e wireless e l'Internet Protocol Security (IPsec).</span><span class="sxs-lookup"><span data-stu-id="5167c-124">For the NAP enforcement methods, programmers should be familiar with networking protocols and technologies such as Remote Authentication Dial-in User Service (RADIUS), Dynamic Host Configuration Protocol (DHCP), virtual private networks (VPNs), the IEEE 802.1X standard for wired and wireless access, and Internet Protocol security (IPsec).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="5167c-125">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="5167c-125">Run-time requirements</span></span>

<span data-ttu-id="5167c-126">La piattaforma NAP richiede server di infrastruttura NAP che eseguono Windows Server 2008 o versioni successive e client NAP che eseguono Windows XP con Service Pack 3 (SP3), Windows Vista o sistemi operativi successivi.</span><span class="sxs-lookup"><span data-stu-id="5167c-126">The NAP platform requires NAP infrastructure servers running Windows Server 2008 or later and NAP clients running Windows XP with Service Pack 3 (SP3), Windows Vista, or later operating systems.</span></span> <span data-ttu-id="5167c-127">Per informazioni specifiche sui sistemi operativi che supportano un particolare elemento di programmazione, vedere le sezioni requisiti delle API NAP nella documentazione di riferimento per NAP.</span><span class="sxs-lookup"><span data-stu-id="5167c-127">For specific information about which operating systems support a particular programming element, refer to the Requirements sections of the NAP APIs in the NAP Reference documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5167c-128">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="5167c-128">In this section</span></span>



| <span data-ttu-id="5167c-129">Argomento</span><span class="sxs-lookup"><span data-stu-id="5167c-129">Topic</span></span>                                         | <span data-ttu-id="5167c-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5167c-130">Description</span></span>                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="5167c-131">Informazioni su NAP</span><span class="sxs-lookup"><span data-stu-id="5167c-131">About NAP</span></span>](about-nap.md)<br/>         | <span data-ttu-id="5167c-132">Informazioni generali sull'API NAP.</span><span class="sxs-lookup"><span data-stu-id="5167c-132">General information about NAP API.</span></span><br/>                                     |
| [<span data-ttu-id="5167c-133">Uso di Protezione accesso alla rete</span><span class="sxs-lookup"><span data-stu-id="5167c-133">Using NAP</span></span>](using-nap.md)<br/>         | <span data-ttu-id="5167c-134">Esempi di utilizzo per l'API NAP.</span><span class="sxs-lookup"><span data-stu-id="5167c-134">Usage examples for NAP API.</span></span><br/>                                            |
| [<span data-ttu-id="5167c-135">Riferimento NAP</span><span class="sxs-lookup"><span data-stu-id="5167c-135">NAP Reference</span></span>](nap-reference.md)<br/> | <span data-ttu-id="5167c-136">Documentazione per le interfacce NAP, le strutture e altri elementi di codice.</span><span class="sxs-lookup"><span data-stu-id="5167c-136">Documentation for NAP interfaces, structures, and other code elements.</span></span><br/> |



 

 

 





