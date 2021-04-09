---
title: Thin provisioning di unità logiche
description: Thin provisioning di unità logiche
ms.assetid: D64ECA7B-62AC-4C14-BE4B-84DA2E20C16B
keywords:
- LUN
- LBA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4abb6fa3cec112737b23e3cd658a48984cb0fcd1
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "104047499"
---
# <a name="thin-provisioning-of-logical-units"></a><span data-ttu-id="7e294-105">Thin provisioning di unità logiche</span><span class="sxs-lookup"><span data-stu-id="7e294-105">Thin provisioning of logical units</span></span>

## <a name="platforms"></a><span data-ttu-id="7e294-106">Piattaforme</span><span class="sxs-lookup"><span data-stu-id="7e294-106">Platforms</span></span>

<span data-ttu-id="7e294-107">**Client** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="7e294-107">**Clients** – Windows 8</span></span>  
<span data-ttu-id="7e294-108">**Server** : Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7e294-108">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="7e294-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e294-109">Description</span></span>

<span data-ttu-id="7e294-110">Il thin provisioning di Windows è un'interfaccia per la soluzione di provisioning dell'archiviazione end-to-end.</span><span class="sxs-lookup"><span data-stu-id="7e294-110">Windows Thin Provisioning is an interface to the end-to-end storage provisioning solution.</span></span> <span data-ttu-id="7e294-111">Per offrire un servizio di provisioning di archiviazione estremamente disponibile, scalabile e intuitivo, richiede implementazioni affidabili dall'host server al dispositivo di destinazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7e294-111">To deliver a highly available, scalable and user-friendly storage provisioning service requires robust implementations from the server host to the storage target device.</span></span> <span data-ttu-id="7e294-112">La funzionalità Windows Thin provisioning fornisce una visualizzazione sincrona dei dispositivi di archiviazione con thin provisioning all'amministratore di sistema, al responsabile IT e all'amministratore dell'archiviazione tramite l'identificazione dell'unità logica (LUN) con thin provisioning, la notifica delle soglie, la gestione dell'esaurimento delle risorse, il recupero dello spazio e il recupero dello stato del blocco logico (LBA).</span><span class="sxs-lookup"><span data-stu-id="7e294-112">The Windows thin provisioning feature provides a synchronous view of the thin provisioning storage devices to the system administrator, IT manager, and storage administrator through the thinly provisioned logical unit’s (LUN’s) identification, threshold notification, resource exhaustion handling, space reclamation, and logical block addressing (LBA) state retrieval.</span></span> <span data-ttu-id="7e294-113">La funzionalità Windows Thin provisioning presenta un modello di servizio di provisioning dell'archiviazione affidabile che può essere applicato ai sistemi di archiviazione client-server, all'archiviazione di virtualizzazione e ai servizi di archiviazione cloud.</span><span class="sxs-lookup"><span data-stu-id="7e294-113">The Windows thin provisioning feature presents a robust storage provisioning service model that can be applied to client-server storage systems, virtualization storage, and cloud storage services.</span></span> <span data-ttu-id="7e294-114">Microsoft assicurerà la qualità elevata della funzionalità di thin provisioning imponendo i requisiti del kit di certificazione hardware di Windows Thin provisioning per i prodotti array di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7e294-114">Microsoft will ensure the high quality of the thin provisioning feature by enforcing the Windows Thin Provisioning Hardware Certification Kit requirements for storage array products.</span></span>

<span data-ttu-id="7e294-115">Soluzione di archiviazione thin provisioning di Windows:</span><span class="sxs-lookup"><span data-stu-id="7e294-115">The Windows Thin Provisioning storage solution:</span></span>

-   <span data-ttu-id="7e294-116">Consente agli amministratori di archiviazione di creare un LUN più grande con meno risorse disco fisico</span><span class="sxs-lookup"><span data-stu-id="7e294-116">Allows storage administrators to create a larger LUN with fewer physical disk resources</span></span>
-   <span data-ttu-id="7e294-117">Aggiunge o rimuove una risorsa disco fisico senza interrompere il servizio di provisioning dell'archiviazione</span><span class="sxs-lookup"><span data-stu-id="7e294-117">Adds or removes physical disk resource without interrupting the storage provisioning service</span></span>
-   <span data-ttu-id="7e294-118">Avvisa gli utenti dell'utilizzo del volume di archiviazione tramite l'impostazione della soglia</span><span class="sxs-lookup"><span data-stu-id="7e294-118">Alerts users to the storage volume usage through the threshold setting</span></span>
-   <span data-ttu-id="7e294-119">Supporta il provisioning dell'archiviazione tramite la configurazione del pool di archiviazione condiviso</span><span class="sxs-lookup"><span data-stu-id="7e294-119">Supports storage provisioning through the shared storage pool configuration</span></span>
-   <span data-ttu-id="7e294-120">Aumenta o diminuisce le dimensioni del pool di archiviazione in base alla domanda e all'utilizzo dello spazio di archiviazione</span><span class="sxs-lookup"><span data-stu-id="7e294-120">Increases or decreases the size of the storage pool according to the demand and usage of storage space</span></span>

<span data-ttu-id="7e294-121">Riepilogo delle funzionalità di Windows Thin provisioning:</span><span class="sxs-lookup"><span data-stu-id="7e294-121">Summary of the Windows Thin Provisioning features:</span></span>

-   <span data-ttu-id="7e294-122">Identificazione del LUN con thin provisioning</span><span class="sxs-lookup"><span data-stu-id="7e294-122">Thin Provisioning LUN identification</span></span>
-   <span data-ttu-id="7e294-123">Handle per la notifica delle soglie, l'esaurimento delle risorse temporanee e l'esaurimento delle risorse permanente</span><span class="sxs-lookup"><span data-stu-id="7e294-123">Handles for threshold notification, temporary resource exhaustion, and permanent resource exhaustion</span></span>
-   <span data-ttu-id="7e294-124">Recupero dello spazio di archiviazione</span><span class="sxs-lookup"><span data-stu-id="7e294-124">Storage space reclamation</span></span>
-   <span data-ttu-id="7e294-125">Query sullo stato del mapping di blocchi logici</span><span class="sxs-lookup"><span data-stu-id="7e294-125">Mapping state queries of logical blocks</span></span>

## <a name="manifestation"></a><span data-ttu-id="7e294-126">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="7e294-126">Manifestation</span></span>

<span data-ttu-id="7e294-127">Senza la conoscenza corretta degli handle di Windows per il thin provisioning LUN, l'app potrebbe non riuscire con un comportamento imprevisto o per una ragione sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="7e294-127">Without the proper understanding of the Windows handles for thin provisioning LUN, the app could fail with unexpected behavior or for an unknown cause.</span></span>

## <a name="using-thin-provisioning-luns"></a><span data-ttu-id="7e294-128">Uso di LUN con thin provisioning</span><span class="sxs-lookup"><span data-stu-id="7e294-128">Using thin provisioning LUNs</span></span>

<span data-ttu-id="7e294-129">Per usare i LUN con thin provisioning in Windows 8 o Windows Server 2012, gli amministratori di sistema e di archiviazione devono essere a conoscenza di questi aspetti:</span><span class="sxs-lookup"><span data-stu-id="7e294-129">To use thinly provisioned LUNs in Windows 8 or Windows Server 2012, system and storage administrators should be aware of these matters:</span></span>

-   <span data-ttu-id="7e294-130">Identificazione del LUN con thin provisioning; gli amministratori di sistema o gli utenti finali possono usare Defrag e l'utilità di ottimizzazione archiviazione per identificare il tipo di supporto del dispositivo di archiviazione</span><span class="sxs-lookup"><span data-stu-id="7e294-130">Thin provisioning LUN identification; system administrators or end users can use Defrag and the Storage Optimizer utility to identify the media type of the storage device</span></span>
-   <span data-ttu-id="7e294-131">Quando viene raggiunta una soglia o un evento di esaurimento delle risorse permanente, Windows registrerà un evento di sistema per avvisare l'amministratore di sistema</span><span class="sxs-lookup"><span data-stu-id="7e294-131">When a threshold or a permanent resource exhaustion event is hit, Windows will log a system event to alert the system administrator</span></span>
-   <span data-ttu-id="7e294-132">Il recupero dello spazio di archiviazione può essere eseguito manualmente o automaticamente tramite la notifica di eliminazione file o l'utilità di pianificazione di storage Optimizer</span><span class="sxs-lookup"><span data-stu-id="7e294-132">Storage space reclamation can be performed manually or automatically by file delete notification or the scheduler of the storage optimizer</span></span>
-   <span data-ttu-id="7e294-133">L'amministratore di archiviazione deve implementare la notifica delle soglie per avvisare l'amministratore del sistema o l'utente finale ed evitare interruzioni impreviste del servizio di archiviazione</span><span class="sxs-lookup"><span data-stu-id="7e294-133">Storage administrator should implement the threshold notification to alert system administrator or end user and avoid any unexpected storage service interruption</span></span>

## <a name="tests"></a><span data-ttu-id="7e294-134">Test</span><span class="sxs-lookup"><span data-stu-id="7e294-134">Tests</span></span>

-   <span data-ttu-id="7e294-135">Array di archiviazione deve ricevere il certificato di thin provisioning di Windows 8 per supportare le funzionalità di thin provisioning di Windows</span><span class="sxs-lookup"><span data-stu-id="7e294-135">Storage array must receive Windows 8 Thin Provisioning certificate to support Windows Thin Provisioning features</span></span>
-   <span data-ttu-id="7e294-136">Il kit di certificazione hardware di Windows Thin provisioning per array di archiviazione sarà uno strumento di test utile per verificare la funzionalità dell'array di archiviazione per il supporto delle funzionalità thin provisioning di Windows</span><span class="sxs-lookup"><span data-stu-id="7e294-136">Windows Thin Provisioning Hardware Certification Kit for storage array will be a useful test tool to verify storage array’s capability for Windows Thin Provisioning feature support</span></span>
-   <span data-ttu-id="7e294-137">Windows prevede che il LUN di thin provisioning e il LUN di provisioning completo funzionino nello stesso sistema senza problemi</span><span class="sxs-lookup"><span data-stu-id="7e294-137">Windows expects the Thin Provisioning LUN and Full Provisioning LUN to work in the same system without any issue</span></span>

## <a name="resources"></a><span data-ttu-id="7e294-138">Risorse</span><span class="sxs-lookup"><span data-stu-id="7e294-138">Resources</span></span>

-   [<span data-ttu-id="7e294-139">Specifica del comando di blocco SCSI T10 (SBC3r27)</span><span class="sxs-lookup"><span data-stu-id="7e294-139">T10 SCSI Block Command Spec (SBC3r27)</span></span>](https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r27.pdf)
-   [<span data-ttu-id="7e294-140">Servizi dashboard hardware</span><span class="sxs-lookup"><span data-stu-id="7e294-140">Hardware Dashboard Services</span></span>](/windows-hardware/drivers/dashboard/)

 

 