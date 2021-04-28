---
description: Memoria dinamica
ms.assetid: 0ea1de35-34ea-4e94-b90d-0f89503cb3fb
title: Memoria dinamica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfcc54a1b85f4fc39bf6383e05a2e6e535edd1d4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088469"
---
# <a name="dynamic-memory"></a><span data-ttu-id="b0bac-103">Memoria dinamica</span><span class="sxs-lookup"><span data-stu-id="b0bac-103">Dynamic Memory</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="b0bac-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="b0bac-104">Affected Platforms</span></span>

<span data-ttu-id="b0bac-105">**Client (in esecuzione come macchine virtuali)** - Windows Vista \| Windows 7</span><span class="sxs-lookup"><span data-stu-id="b0bac-105">**Clients (running as virtual machines)** - Windows Vista \| Windows 7</span></span>  
<span data-ttu-id="b0bac-106">**Server** - Windows Server 2008 R2 Hyper-V SP1</span><span class="sxs-lookup"><span data-stu-id="b0bac-106">**Servers** - Windows Server 2008 R2 Hyper-V SP1</span></span>  


## <a name="feature-impact"></a><span data-ttu-id="b0bac-107">Impatto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="b0bac-107">Feature Impact</span></span>

 <span data-ttu-id="b0bac-108">**Gravità** - Bassa</span><span class="sxs-lookup"><span data-stu-id="b0bac-108">**Severity** - Low</span></span>  
<span data-ttu-id="b0bac-109">**Frequenza** - Alta</span><span class="sxs-lookup"><span data-stu-id="b0bac-109">**Frequency** - High</span></span>  






## <a name="description"></a><span data-ttu-id="b0bac-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0bac-110">Description</span></span>

<span data-ttu-id="b0bac-111">A livello elevato, Hyper-V memoria dinamica un miglioramento della gestione della memoria per il ruolo Hyper-V incluso in Windows Server 2008 R2 SP1.</span><span class="sxs-lookup"><span data-stu-id="b0bac-111">At a high level, Hyper-V Dynamic Memory is a memory management enhancement for the Hyper-V role included in Windows Server 2008 R2 SP1.</span></span> <span data-ttu-id="b0bac-112">È progettato per l'uso in produzione e consente ai clienti di ottenere rapporti di consolidamento/densità di macchine virtuali (VM) più elevati, ottimizzando al tempo stesso l'utilizzo della memoria nel computer fisico.</span><span class="sxs-lookup"><span data-stu-id="b0bac-112">It is designed for production use and enables customers to achieve higher consolidation/virtual machine (VM) density ratios while optimizing the memory utilization in the physical machine.</span></span> <span data-ttu-id="b0bac-113">L'allocazione di memoria statica viene ridotta e la memoria aggiuntiva viene allocata in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="b0bac-113">The static memory allocation is reduced and additional memory is allocated on an as needed basis.</span></span> <span data-ttu-id="b0bac-114">memoria dinamica influisce sugli sviluppatori di software che vogliono garantire il corretto funzionamento del software in un ambiente di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="b0bac-114">Dynamic Memory impacts software developers who want to ensure that their software works correctly in a virtual machine environment.</span></span>

## <a name="usage-scenario"></a><span data-ttu-id="b0bac-115">Scenario di utilizzo</span><span class="sxs-lookup"><span data-stu-id="b0bac-115">Usage Scenario</span></span>

<span data-ttu-id="b0bac-116">Esistono due scenari di utilizzo chiave in cui memoria dinamica in gioco, le applicazioni sul lato host e le applicazioni sul lato guest.</span><span class="sxs-lookup"><span data-stu-id="b0bac-116">There are two key usage scenarios where Dynamic Memory comes into play, host-side applications and guest-side applications.</span></span>

<span data-ttu-id="b0bac-117">**Applicazioni lato host (strumenti di gestione)**</span><span class="sxs-lookup"><span data-stu-id="b0bac-117">**Host-side applications (management tools)**</span></span>

<span data-ttu-id="b0bac-118">I vecchi strumenti che gestiscono un nuovo server Windows Server 2008 R2 SP1 non saranno in grado di accedere alle nuove memoria dinamica predefinite.</span><span class="sxs-lookup"><span data-stu-id="b0bac-118">Old tools managing a new Windows Server 2008 R2 SP1 server will not be able to access the new Dynamic Memory settings.</span></span> <span data-ttu-id="b0bac-119">Sono stati sviluppati nuovi contatori delle prestazioni e API WMI per gestire le nuove memoria dinamica per le macchine virtuali Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="b0bac-119">New WMI APIs and performance counters have been developed to manage the new Dynamic Memory settings for Hyper-V virtual machines.</span></span> <span data-ttu-id="b0bac-120">Gli sviluppatori di software che usano gli strumenti di gestione devono sfruttare queste API e contatori per l'uso con Windows Server 2008 R2 SP1 con il ruolo Hyper-V installato.</span><span class="sxs-lookup"><span data-stu-id="b0bac-120">Software developers working on management tools should take advantage of these APIs and counters for use with Windows Server 2008 R2 SP1 with the Hyper-V role installed.</span></span> <span data-ttu-id="b0bac-121">I dettagli su queste nuove API saranno disponibili tramite la documentazione del [provider WMI Hyper-V in MSDN.](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider)</span><span class="sxs-lookup"><span data-stu-id="b0bac-121">Details about these new APIs will be available via [Hyper-V WMI Provider documentation on MSDN](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider).</span></span>

<span data-ttu-id="b0bac-122">**Applicazioni lato guest**</span><span class="sxs-lookup"><span data-stu-id="b0bac-122">**Guest-side applications**</span></span>

<span data-ttu-id="b0bac-123">Gli sviluppatori che scrivono software da usare all'interno di una macchina virtuale configurata memoria dinamica devono tenere presente che la memoria di sistema della macchina virtuale non è più costante.</span><span class="sxs-lookup"><span data-stu-id="b0bac-123">Developers writing software for use inside a virtual machine configured to use Dynamic Memory need to keep in mind that VM system memory is no longer constant.</span></span> <span data-ttu-id="b0bac-124">Di conseguenza, l'applicazione deve liberare memoria quando non è più necessaria per consentire ad altre applicazioni di sfruttare i vantaggi della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b0bac-124">Consequently, their application should free memory when it is no longer needed to allow other applications to take advantage of the resource.</span></span>

<span data-ttu-id="b0bac-125">Le allocazioni di memoria e le deallocazione continuano a funzionare normalmente per le applicazioni utente.</span><span class="sxs-lookup"><span data-stu-id="b0bac-125">Memory allocations and de-allocations continue to work as normal for user applications.</span></span> <span data-ttu-id="b0bac-126">memoria dinamica è completamente trasparente per la maggior parte delle applicazioni degli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="b0bac-126">Dynamic Memory is completely transparent to most end user applications.</span></span> <span data-ttu-id="b0bac-127">Tuttavia, se il software in fase di sviluppo usa contatori delle prestazioni di memoria nella macchina virtuale, è necessario eseguire test accurati in un ambiente abilitato per memoria dinamica per assicurarsi che il software prende in considerazione le modifiche apportate all'allocazione di memoria del sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="b0bac-127">However if the software being developed makes use of memory performance counters in the virtual machine then careful testing should be performed in a Dynamic Memory enabled environment to ensure that the software takes the changes that are made to the Guest operating system memory allocation into account.</span></span> <span data-ttu-id="b0bac-128">La memoria disponibile non è più "statica" dal punto di vista della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b0bac-128">Available memory is no longer "static" from the virtual machine?s perspective.</span></span>

## <a name="solutions"></a><span data-ttu-id="b0bac-129">Soluzioni</span><span class="sxs-lookup"><span data-stu-id="b0bac-129">Solutions</span></span>

<span data-ttu-id="b0bac-130">Le macchine virtuali devono avere installato Integration Services (SP1) aggiornato per poter sfruttare memoria dinamica.</span><span class="sxs-lookup"><span data-stu-id="b0bac-130">Virtual machines must have updated integration services (SP1) installed in order to take advantage of Dynamic Memory.</span></span> <span data-ttu-id="b0bac-131">Assicurarsi che tutti i computer usati nella gestione delle macchine virtuali Hyper-V utilizzino i bit più recenti di Windows Server 2008 R2 SP1.</span><span class="sxs-lookup"><span data-stu-id="b0bac-131">Ensure that all machines used in the management of Hyper-V virtual machines are using the latest Windows Server 2008 R2 SP1 bits.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="b0bac-132">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="b0bac-132">Links to Other Resources</span></span>

-   [<span data-ttu-id="b0bac-133">memoria dinamica blog su Hyper-V</span><span class="sxs-lookup"><span data-stu-id="b0bac-133">Dynamic Memory Coming To Hyper-V blog</span></span>](https://blogs.technet.com/b/virtualization/archive/2010/03/18/dynamic-memory-coming-to-hyper-v.aspx)
-   [<span data-ttu-id="b0bac-134">Uso del provider WMI Hyper-V</span><span class="sxs-lookup"><span data-stu-id="b0bac-134">Using the Hyper-V WMI Provider</span></span>](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider)

## <a name="disclaimer"></a><span data-ttu-id="b0bac-135">Dichiarazione di non responsabilità</span><span class="sxs-lookup"><span data-stu-id="b0bac-135">Disclaimer</span></span>

<span data-ttu-id="b0bac-136">Le informazioni contenute in questo documento riguardano prodotti software non definitive che possono essere modificati in modo sostanziale prima della prima versione commerciale.</span><span class="sxs-lookup"><span data-stu-id="b0bac-136">The information contained in this document relates to prerelease software product that may be substantially modified before its first commercial release.</span></span> <span data-ttu-id="b0bac-137">Di conseguenza, le informazioni potrebbero non descrivere o riflettere in modo accurato il prodotto software al primo rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="b0bac-137">Accordingly, the information may not accurately describe or reflect the software product when first commercially released.</span></span> <span data-ttu-id="b0bac-138">Questo documento è esclusivamente a scopo informativo.</span><span class="sxs-lookup"><span data-stu-id="b0bac-138">This document is for informational purposes only.</span></span> <span data-ttu-id="b0bac-139">MICROSOFT MAKES NO WARRANTIES, EXPRESS OR IMPLIED, IN THIS DOCUMENT.</span><span class="sxs-lookup"><span data-stu-id="b0bac-139">MICROSOFT MAKES NO WARRANTIES, EXPRESS OR IMPLIED, IN THIS DOCUMENT.</span></span>

 

 
