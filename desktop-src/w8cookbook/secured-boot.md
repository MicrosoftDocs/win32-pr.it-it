---
title: Antimalware ad esecuzione anticipata
description: Antimalware ad esecuzione anticipata
ms.assetid: 4064CD44-FC50-48DE-8490-F592ED21CB7E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34c3e51d7fb009ffa0e85a59990b321fb38ad196
ms.sourcegitcommit: a93d3abaf4d6d45a6f0b87faed3f576b222b1745
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "104058402"
---
# <a name="early-launch-antimalware"></a><span data-ttu-id="9579c-103">Antimalware ad esecuzione anticipata</span><span class="sxs-lookup"><span data-stu-id="9579c-103">Early launch antimalware</span></span>

## <a name="platforms"></a><span data-ttu-id="9579c-104">Piattaforme</span><span class="sxs-lookup"><span data-stu-id="9579c-104">Platforms</span></span>

 <span data-ttu-id="9579c-105">**Client** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="9579c-105">**Clients** - Windows 8</span></span>  
<span data-ttu-id="9579c-106">**Server** -Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9579c-106">**Servers** - Windows Server 2012</span></span>  

## <a name="description"></a><span data-ttu-id="9579c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9579c-107">Description</span></span>

<span data-ttu-id="9579c-108">Poiché il software antimalware (AM) è diventato migliore e migliore nel rilevamento del malware di runtime, anche gli utenti malintenzionati stanno migliorando la creazione di rootkit che possono nascondere il rilevamento.</span><span class="sxs-lookup"><span data-stu-id="9579c-108">As antimalware (AM) software has become better and better at detecting runtime malware, attackers are also becoming better at creating rootkits that can hide from detection.</span></span> <span data-ttu-id="9579c-109">Il rilevamento di malware che inizia nelle prime fasi del ciclo di avvio è una sfida che la maggior parte dei fornitori di AM deve affrontare diligentemente.</span><span class="sxs-lookup"><span data-stu-id="9579c-109">Detecting malware that starts early in the boot cycle is a challenge that most AM vendors address diligently.</span></span> <span data-ttu-id="9579c-110">In genere, creano hack di sistema non supportati dal sistema operativo host e possono effettivamente comportare il posizionamento del computer in uno stato instabile.</span><span class="sxs-lookup"><span data-stu-id="9579c-110">Typically, they create system hacks that are not supported by the host operating system and can actually result in placing the computer in an unstable state.</span></span> <span data-ttu-id="9579c-111">Fino a questo punto, Windows non ha fornito un metodo efficace per rilevare e risolvere queste minacce iniziali di avvio.</span><span class="sxs-lookup"><span data-stu-id="9579c-111">Up to this point, Windows has not provided a good way for AM to detect and resolve these early boot threats.</span></span>

<span data-ttu-id="9579c-112">In Windows 8 è stata introdotta una nuova funzionalità denominata avvio protetto, che protegge i componenti e la configurazione di avvio di Windows, e carica un driver anti-malware (ELAM) con avvio rapido.</span><span class="sxs-lookup"><span data-stu-id="9579c-112">Windows 8 introduces a new feature called Secure Boot, which protects the Windows boot configuration and components, and loads an Early Launch Anti-malware (ELAM) driver.</span></span> <span data-ttu-id="9579c-113">Questo driver viene avviato prima di altri driver di avvio e consente la valutazione di tali driver e consente al kernel di Windows di decidere se deve essere inizializzato.</span><span class="sxs-lookup"><span data-stu-id="9579c-113">This driver starts before other boot-start drivers and enables the evaluation of those drivers and helps the Windows kernel decide whether they should be initialized.</span></span>

## <a name="manifestation"></a><span data-ttu-id="9579c-114">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="9579c-114">Manifestation</span></span>

<span data-ttu-id="9579c-115">Quando viene avviato per primo dal kernel, ELAM è sicuro di essere avviato prima di qualsiasi software di terze parti ed è quindi in grado di rilevare malware nel processo di avvio e di impedirne l'inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="9579c-115">By being launched first by the kernel, ELAM is ensured to be launched before any third-party software, and is therefore able to detect malware in the boot process and prevent it from initializing.</span></span>

## <a name="mitigation"></a><span data-ttu-id="9579c-116">Strategia di riduzione del rischio</span><span class="sxs-lookup"><span data-stu-id="9579c-116">Mitigation</span></span>

<span data-ttu-id="9579c-117">I driver di avvio vengono inizializzati in base alla classificazione restituita dal driver ELAM in base ai criteri di inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="9579c-117">Boot drivers are initialized based on the classification that is returned from the ELAM driver according to an initialization policy.</span></span> <span data-ttu-id="9579c-118">Per impostazione predefinita, i criteri inizializzano i driver noti e sconosciuti, ma non inizializzano i driver noti non validi.</span><span class="sxs-lookup"><span data-stu-id="9579c-118">By default, the policy initializes known good and unknown drivers, but will not initialize known bad drivers.</span></span> <span data-ttu-id="9579c-119">Un amministratore di sistema può specificare un criterio personalizzato tramite Criteri di gruppo in grado di impedire l'inizializzazione di driver sconosciuti o l'abilitazione di driver critici per il processo di avvio, ma che sono stati manomessi, l'avvio deve essere inizializzato.</span><span class="sxs-lookup"><span data-stu-id="9579c-119">A system administrator can specify a custom policy through Group Policy that can prevent unknown drivers from initializing or can enable drivers that are critical to the boot process, but have been tampered with, boot to be initialized.</span></span>

## <a name="solution"></a><span data-ttu-id="9579c-120">Soluzione</span><span class="sxs-lookup"><span data-stu-id="9579c-120">Solution</span></span>

<span data-ttu-id="9579c-121">È necessario registrare un driver ELAM per le richiamate del kernel per ottenere informazioni su ogni driver di avvio che viene inizializzato.</span><span class="sxs-lookup"><span data-stu-id="9579c-121">An ELAM driver must register for kernel callbacks to get info about each boot-start driver as it is initializing.</span></span> <span data-ttu-id="9579c-122">Il driver ELAM può quindi restituire una classificazione per ogni driver.</span><span class="sxs-lookup"><span data-stu-id="9579c-122">The ELAM driver can then return a classification for each driver.</span></span> <span data-ttu-id="9579c-123">Queste funzioni sono obbligatorie:</span><span class="sxs-lookup"><span data-stu-id="9579c-123">These functions are required:</span></span>

-   [<span data-ttu-id="9579c-124">IoRegisterBootDriverCallback</span><span class="sxs-lookup"><span data-stu-id="9579c-124">IoRegisterBootDriverCallback</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-ioregisterbootdrivercallback)
-   [<span data-ttu-id="9579c-125">IoUnRegisterBootDriverCallback</span><span class="sxs-lookup"><span data-stu-id="9579c-125">IoUnRegisterBootDriverCallback</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-iounregisterbootdrivercallback)

<span data-ttu-id="9579c-126">Un driver ELAM può anche registrarsi per i callback del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="9579c-126">An ELAM driver can also register for registry callbacks.</span></span> <span data-ttu-id="9579c-127">Questa operazione consente al driver ELAM di ispezionare i dati di configurazione usati da ogni driver di avvio.</span><span class="sxs-lookup"><span data-stu-id="9579c-127">Doing so enables the ELAM driver to inspect the configuration data that is used by each boot-start driver.</span></span> <span data-ttu-id="9579c-128">Il driver ELAM può quindi bloccare o modificare i dati prima che vengano usati dai driver di avvio, se necessario.</span><span class="sxs-lookup"><span data-stu-id="9579c-128">The ELAM driver can then block or modify the data before it is used by the boot-start drivers, if necessary.</span></span> <span data-ttu-id="9579c-129">Queste funzioni sono obbligatorie:</span><span class="sxs-lookup"><span data-stu-id="9579c-129">These functions are required:</span></span>

-   [<span data-ttu-id="9579c-130">CmRegisterCallbackEx</span><span class="sxs-lookup"><span data-stu-id="9579c-130">CmRegisterCallbackEx</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmregistercallbackex)
-   [<span data-ttu-id="9579c-131">CmUnRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="9579c-131">CmUnRegisterCallback</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmunregistercallback)

<span data-ttu-id="9579c-132">Per altre informazioni sui requisiti dei driver ELAM e sull'utilizzo delle API, vedere [antimalware ad esecuzione anticipata](/windows-hardware/drivers/install/early-launch-antimalware).</span><span class="sxs-lookup"><span data-stu-id="9579c-132">For more details about ELAM driver requirements and API usage, see [Early Launch Antimalware](/windows-hardware/drivers/install/early-launch-antimalware).</span></span>

## <a name="tests"></a><span data-ttu-id="9579c-133">Test</span><span class="sxs-lookup"><span data-stu-id="9579c-133">Tests</span></span>

<span data-ttu-id="9579c-134">I driver ELAM devono essere firmati appositamente da Microsoft per assicurarsi che vengano avviati dal kernel di Windows nelle fasi iniziali del processo di avvio.</span><span class="sxs-lookup"><span data-stu-id="9579c-134">ELAM drivers must be specially signed by Microsoft to ensure they are started by the Windows kernel early in the boot process.</span></span> <span data-ttu-id="9579c-135">Per ottenere la firma, i driver ELAM devono passare un set di test di certificazione per verificare le prestazioni e altri comportamenti.</span><span class="sxs-lookup"><span data-stu-id="9579c-135">To get the signature, ELAM drivers must pass a set of certification tests to verify performance and other behavior.</span></span> <span data-ttu-id="9579c-136">Questi test sono inclusi nel kit di certificazione hardware di Windows.</span><span class="sxs-lookup"><span data-stu-id="9579c-136">These tests are included in the Windows Hardware Certification Kit.</span></span>

## <a name="resources"></a><span data-ttu-id="9579c-137">Risorse</span><span class="sxs-lookup"><span data-stu-id="9579c-137">Resources</span></span>

-   [<span data-ttu-id="9579c-138">Antimalware ad esecuzione anticipata</span><span class="sxs-lookup"><span data-stu-id="9579c-138">Early Launch Antimalware</span></span>](/windows-hardware/drivers/install/early-launch-antimalware)
-   [<span data-ttu-id="9579c-139">CmRegisterCallbackEx</span><span class="sxs-lookup"><span data-stu-id="9579c-139">CmRegisterCallbackEx</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmregistercallbackex)
-   [<span data-ttu-id="9579c-140">CmUnRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="9579c-140">CmUnRegisterCallback</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmunregistercallback)
-   [<span data-ttu-id="9579c-141">IoRegisterBootDriverCallback</span><span class="sxs-lookup"><span data-stu-id="9579c-141">IoRegisterBootDriverCallback</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-ioregisterbootdrivercallback)
-   [<span data-ttu-id="9579c-142">IoUnRegisterBootDriverCallback</span><span class="sxs-lookup"><span data-stu-id="9579c-142">IoUnRegisterBootDriverCallback</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-iounregisterbootdrivercallback)
-   [<span data-ttu-id="9579c-143">Certificazione dell'hardware con Windows Hardware Certification Kit Build Conference Presentation</span><span class="sxs-lookup"><span data-stu-id="9579c-143">Certifying hardware with the Windows Hardware Certification Kit Build Conference presentation</span></span>](https://channel9.msdn.com/events/BUILD/BUILD2011/HW-659T)
-   [<span data-ttu-id="9579c-144">Scarica kit e strumenti</span><span class="sxs-lookup"><span data-stu-id="9579c-144">Download Kits and Tools</span></span>](https://msdn.microsoft.com/windows/hardware/br259105)

 

 
