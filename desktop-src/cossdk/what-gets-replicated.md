---
description: Cosa viene replicato
ms.assetid: d1f0bc92-37bc-4de2-876a-e6b8b09da58d
title: Cosa viene replicato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2739cb0ff615ddc38f30a7aa9b0a572be5e28a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304928"
---
# <a name="what-gets-replicated"></a><span data-ttu-id="c8288-103">Cosa viene replicato</span><span class="sxs-lookup"><span data-stu-id="c8288-103">What Gets Replicated</span></span>

## <a name="applications"></a><span data-ttu-id="c8288-104">Applicazioni</span><span class="sxs-lookup"><span data-stu-id="c8288-104">Applications</span></span>

<span data-ttu-id="c8288-105">Tutte le applicazioni installate nel computer di origine vengono replicate ad eccezione di quanto segue:</span><span class="sxs-lookup"><span data-stu-id="c8288-105">All applications installed on the source computer are replicated except for the following:</span></span>

<dl> <dt>

<span data-ttu-id="c8288-106"><span id="Non-COM__application_elements_and_dependencies"></span><span id="non-com__application_elements_and_dependencies"></span><span id="NON-COM__APPLICATION_ELEMENTS_AND_DEPENDENCIES"></span>Elementi e dipendenze dell'applicazione non COM +</span><span class="sxs-lookup"><span data-stu-id="c8288-106"><span id="Non-COM__application_elements_and_dependencies"></span><span id="non-com__application_elements_and_dependencies"></span><span id="NON-COM__APPLICATION_ELEMENTS_AND_DEPENDENCIES"></span>Non-COM+ application elements and dependencies</span></span>
</dt> <dd>

<span data-ttu-id="c8288-107">L'amministratore è responsabile della replica di qualsiasi elemento da cui dipende un'applicazione COM+, che non è parte integrante dell'applicazione stessa, ad esempio file di dati e dll.</span><span class="sxs-lookup"><span data-stu-id="c8288-107">The administrator is responsible for replicating anything that a COM+ application depends on but which is not properly part of the application itself, such as data files and DLLs.</span></span> <span data-ttu-id="c8288-108">COMREPL non eseguirà la replica di alcun elemento all'esterno degli elementi dell'applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="c8288-108">COMREPL will not replicate anything outside of COM+ application elements.</span></span>

</dd> <dt>

<span data-ttu-id="c8288-109"><span id="COM__preinstalled_applications"></span><span id="com__preinstalled_applications"></span><span id="COM__PREINSTALLED_APPLICATIONS"></span>Applicazioni preinstallate COM+</span><span class="sxs-lookup"><span data-stu-id="c8288-109"><span id="COM__preinstalled_applications"></span><span id="com__preinstalled_applications"></span><span id="COM__PREINSTALLED_APPLICATIONS"></span>COM+ preinstalled applications</span></span>
</dt> <dd>

<span data-ttu-id="c8288-110">Le applicazioni utilizzate internamente da COM+ e installate tramite il programma di installazione COM+ non vengono replicate.</span><span class="sxs-lookup"><span data-stu-id="c8288-110">Applications that are used internally by COM+ and are installed via the COM+ setup program are not replicated.</span></span> <span data-ttu-id="c8288-111">tra cui:</span><span class="sxs-lookup"><span data-stu-id="c8288-111">These include the following:</span></span>

-   <span data-ttu-id="c8288-112">Applicazione di sistema</span><span class="sxs-lookup"><span data-stu-id="c8288-112">System application</span></span>
-   <span data-ttu-id="c8288-113">Utilità COM+</span><span class="sxs-lookup"><span data-stu-id="c8288-113">COM+ utilities</span></span>
-   <span data-ttu-id="c8288-114">Listener coda messaggi non recapitabili di COM+ QC</span><span class="sxs-lookup"><span data-stu-id="c8288-114">COM+ QC Dead Letter Queue Listener</span></span>

</dd> <dt>

<span data-ttu-id="c8288-115"><span id="Applications_created_by_IIS"></span><span id="applications_created_by_iis"></span><span id="APPLICATIONS_CREATED_BY_IIS"></span>Applicazioni create da IIS</span><span class="sxs-lookup"><span data-stu-id="c8288-115"><span id="Applications_created_by_IIS"></span><span id="applications_created_by_iis"></span><span id="APPLICATIONS_CREATED_BY_IIS"></span>Applications created by IIS</span></span>
</dt> <dd>

<span data-ttu-id="c8288-116">Queste applicazioni non vengono replicate e includono quanto segue:</span><span class="sxs-lookup"><span data-stu-id="c8288-116">These applications are not replicated and include the following:</span></span>

-   <span data-ttu-id="c8288-117">Applicazioni IIS in-process</span><span class="sxs-lookup"><span data-stu-id="c8288-117">IIS in-process applications</span></span>
-   <span data-ttu-id="c8288-118">Utilità IIS</span><span class="sxs-lookup"><span data-stu-id="c8288-118">IIS utilities</span></span>
-   <span data-ttu-id="c8288-119">Tutte le applicazioni create per le radici virtuali isolate o in pool</span><span class="sxs-lookup"><span data-stu-id="c8288-119">All applications created for isolated or pooled virtual roots</span></span>

</dd> </dl>

## <a name="computer-list"></a><span data-ttu-id="c8288-120">Elenco computer</span><span class="sxs-lookup"><span data-stu-id="c8288-120">Computer List</span></span>

<span data-ttu-id="c8288-121">I computer remoti denominati nella cartella **computer** dello strumento di amministrazione Servizi componenti non verranno replicati dal computer di origine al computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c8288-121">The remote computers named in the **Computers** folder in the Component Services administration tool will not be replicated from source to target computer.</span></span>

## <a name="properties"></a><span data-ttu-id="c8288-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c8288-122">Properties</span></span>

<span data-ttu-id="c8288-123">Vengono replicate le seguenti proprietà della raccolta **LocalComputer** :</span><span class="sxs-lookup"><span data-stu-id="c8288-123">The following **LocalComputer** collection properties are replicated:</span></span>

-   <span data-ttu-id="c8288-124">TransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="c8288-124">TransactionTimeout</span></span>
-   <span data-ttu-id="c8288-125">ResourcePoolingEnabled</span><span class="sxs-lookup"><span data-stu-id="c8288-125">ResourcePoolingEnabled</span></span>
-   <span data-ttu-id="c8288-126">DCOMEnabled</span><span class="sxs-lookup"><span data-stu-id="c8288-126">DCOMEnabled</span></span>
-   <span data-ttu-id="c8288-127">DefaultAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="c8288-127">DefaultAuthenticationLevel</span></span>
-   <span data-ttu-id="c8288-128">DefaultImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="c8288-128">DefaultImpersonationLevel</span></span>
-   <span data-ttu-id="c8288-129">SecurityTrackingEnabled</span><span class="sxs-lookup"><span data-stu-id="c8288-129">SecurityTrackingEnabled</span></span>
-   <span data-ttu-id="c8288-130">CISEnabled</span><span class="sxs-lookup"><span data-stu-id="c8288-130">CISEnabled</span></span>
-   <span data-ttu-id="c8288-131">SecureReferencesEnabled</span><span class="sxs-lookup"><span data-stu-id="c8288-131">SecureReferencesEnabled</span></span>
-   <span data-ttu-id="c8288-132">InternetPortsListed</span><span class="sxs-lookup"><span data-stu-id="c8288-132">InternetPortsListed</span></span>
-   <span data-ttu-id="c8288-133">DeafultToInternetPorts</span><span class="sxs-lookup"><span data-stu-id="c8288-133">DeafultToInternetPorts</span></span>
-   <span data-ttu-id="c8288-134">Porte</span><span class="sxs-lookup"><span data-stu-id="c8288-134">Ports</span></span>
-   <span data-ttu-id="c8288-135">RpcProxyEnabled</span><span class="sxs-lookup"><span data-stu-id="c8288-135">RpcProxyEnabled</span></span>

<span data-ttu-id="c8288-136">Le seguenti proprietà della raccolta **LocalComputer** non vengono replicate:</span><span class="sxs-lookup"><span data-stu-id="c8288-136">The following **LocalComputer** collection properties are not replicated:</span></span>

-   <span data-ttu-id="c8288-137">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8288-137">Description</span></span>
-   <span data-ttu-id="c8288-138">ApplicationProxyRSN</span><span class="sxs-lookup"><span data-stu-id="c8288-138">ApplicationProxyRSN</span></span>
-   <span data-ttu-id="c8288-139">Routing</span><span class="sxs-lookup"><span data-stu-id="c8288-139">IsRouter</span></span>

<span data-ttu-id="c8288-140">Per le descrizioni delle proprietà della raccolta **LocalComputer** , vedere [**LocalComputer**](localcomputer.md).</span><span class="sxs-lookup"><span data-stu-id="c8288-140">For descriptions of the **LocalComputer** collection properties, see [**LocalComputer**](localcomputer.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8288-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c8288-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8288-142">Gestione dei file</span><span class="sxs-lookup"><span data-stu-id="c8288-142">File Management</span></span>](file-management.md)
</dt> <dt>

[<span data-ttu-id="c8288-143">Registrazione e segnalazione errori</span><span class="sxs-lookup"><span data-stu-id="c8288-143">Logging and Error Reporting</span></span>](logging-and-error-reporting.md)
</dt> <dt>

[<span data-ttu-id="c8288-144">Fasi di replica</span><span class="sxs-lookup"><span data-stu-id="c8288-144">Replication Phases</span></span>](replication-phases.md)
</dt> <dt>

[<span data-ttu-id="c8288-145">Uso di COMREPL</span><span class="sxs-lookup"><span data-stu-id="c8288-145">Using COMREPL</span></span>](using-comrepl.md)
</dt> </dl>

 

 



