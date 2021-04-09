---
description: Windows Installer possibile ottimizzare l'applicazione di patch per ridurre il tempo necessario per applicare le patch alle applicazioni installate.
ms.assetid: 2bb1c94a-55b6-4aee-b86d-ee9e1f8ed290
title: Ottimizzazione patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86215855bb02314d7eb54c774541b0a2086c7c99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880722"
---
# <a name="patch-optimization"></a><span data-ttu-id="77650-103">Ottimizzazione patch</span><span class="sxs-lookup"><span data-stu-id="77650-103">Patch Optimization</span></span>

<span data-ttu-id="77650-104">Windows Installer possibile ottimizzare l'applicazione di patch per ridurre il tempo necessario per applicare le patch alle applicazioni installate.</span><span class="sxs-lookup"><span data-stu-id="77650-104">Windows Installer can optimize patching to reduce the time that is required to apply patches to installed applications.</span></span>

<span data-ttu-id="77650-105">**Windows Installer 2,0:** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="77650-105">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="77650-106">Per le versioni di Windows Installer rilasciate prima Windows Installer 3,0, l'applicazione di patch esegue un'installazione completa del ripristino dell'applicazione, che può richiedere molto più tempo.</span><span class="sxs-lookup"><span data-stu-id="77650-106">For versions of Windows Installer released before Windows Installer 3.0, patching runs a complete repair installation of the application, which can take significantly more time.</span></span>

<span data-ttu-id="77650-107">**Windows Installer 3,0 e versioni successive:** Il processo di applicazione delle patch modifica solo le parti di un'applicazione modificate da una patch.</span><span class="sxs-lookup"><span data-stu-id="77650-107">**Windows Installer 3.0 and later:** The patching process only changes the parts of an application that are modified by a patch.</span></span>

<span data-ttu-id="77650-108">**Windows Installer 3,1 e versioni successive:** A partire da Windows Installer 3,1, per l'ottimizzazione della patch è necessario che in tutte le patch della transazione la proprietà OptimizedInstallMode sia impostata su 1 (una) nella [tabella MsiPatchMetadata](msipatchmetadata-table.md).</span><span class="sxs-lookup"><span data-stu-id="77650-108">**Windows Installer 3.1 and later:** Beginning with Windows Installer 3.1, patch optimization requires that all patches in the transaction have the OptimizedInstallMode property set to 1 (one) in the [MsiPatchMetadata Table](msipatchmetadata-table.md).</span></span>

<span data-ttu-id="77650-109">Se una patch modifica solo le tabelle seguenti, Windows Installer 3,0 o versioni successive ignora le azioni associate a tutte le altre tabelle, anche se tali azioni sono elencate nelle tabelle di sequenza del pacchetto di installazione dell'applicazione originale (file con estensione msi).</span><span class="sxs-lookup"><span data-stu-id="77650-109">If a patch only modifies the following tables, Windows Installer 3.0 or later skips the actions that are associated with all the other tables, even if those actions are listed in the sequence tables of the original application installation package (.msi file).</span></span>

-   [<span data-ttu-id="77650-110">AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="77650-110">AdminExecuteSequence</span></span>](adminexecutesequence-table.md)
-   [<span data-ttu-id="77650-111">AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="77650-111">AdminUISequence</span></span>](adminuisequence-table.md)
-   [<span data-ttu-id="77650-112">Condition</span><span class="sxs-lookup"><span data-stu-id="77650-112">Condition</span></span>](condition-table.md)
-   [<span data-ttu-id="77650-113">CustomAction</span><span class="sxs-lookup"><span data-stu-id="77650-113">CustomAction</span></span>](customaction-table.md)
-   [<span data-ttu-id="77650-114">File</span><span class="sxs-lookup"><span data-stu-id="77650-114">File</span></span>](file-table.md)
-   [<span data-ttu-id="77650-115">FileSFPCatalog</span><span class="sxs-lookup"><span data-stu-id="77650-115">FileSFPCatalog</span></span>](filesfpcatalog-table.md)
-   [<span data-ttu-id="77650-116">InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="77650-116">InstallExecuteSequence</span></span>](installexecutesequence-table.md)
-   [<span data-ttu-id="77650-117">InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="77650-117">InstallUISequence</span></span>](installuisequence-table.md)
-   [<span data-ttu-id="77650-118">Supporti</span><span class="sxs-lookup"><span data-stu-id="77650-118">Media</span></span>](media-table.md)
-   [<span data-ttu-id="77650-119">MoveFile</span><span class="sxs-lookup"><span data-stu-id="77650-119">MoveFile</span></span>](movefile-table.md)
-   [<span data-ttu-id="77650-120">MsiAssembly</span><span class="sxs-lookup"><span data-stu-id="77650-120">MsiAssembly</span></span>](msiassembly-table.md)
-   [<span data-ttu-id="77650-121">MsiDigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="77650-121">MsiDigitalCertificate</span></span>](msidigitalcertificate-table.md)
-   [<span data-ttu-id="77650-122">MsiDigitalSignature</span><span class="sxs-lookup"><span data-stu-id="77650-122">MsiDigitalSignature</span></span>](msidigitalsignature-table.md)
-   [<span data-ttu-id="77650-123">MsiFileHash</span><span class="sxs-lookup"><span data-stu-id="77650-123">MsiFileHash</span></span>](msifilehash-table.md)
-   [<span data-ttu-id="77650-124">MsiPatchHeaders</span><span class="sxs-lookup"><span data-stu-id="77650-124">MsiPatchHeaders</span></span>](msipatchheaders-table.md)
-   [<span data-ttu-id="77650-125">Patch</span><span class="sxs-lookup"><span data-stu-id="77650-125">Patch</span></span>](patch-table.md)
-   [<span data-ttu-id="77650-126">PacchettoPatch</span><span class="sxs-lookup"><span data-stu-id="77650-126">PatchPackage</span></span>](patchpackage-table.md)
-   [<span data-ttu-id="77650-127">Proprietà</span><span class="sxs-lookup"><span data-stu-id="77650-127">Property</span></span>](property-table.md)
-   [<span data-ttu-id="77650-128">Registro</span><span class="sxs-lookup"><span data-stu-id="77650-128">Registry</span></span>](registry-table.md)
-   [<span data-ttu-id="77650-129">SFPCatalog</span><span class="sxs-lookup"><span data-stu-id="77650-129">SFPCatalog</span></span>](sfpcatalog-table.md)
-   [<span data-ttu-id="77650-130">TypeLib</span><span class="sxs-lookup"><span data-stu-id="77650-130">TypeLib</span></span>](typelib-table.md)
-   [<span data-ttu-id="77650-131">\_Colonne</span><span class="sxs-lookup"><span data-stu-id="77650-131">\_Columns</span></span>](-columns-table.md)
-   [<span data-ttu-id="77650-132">\_Depositi</span><span class="sxs-lookup"><span data-stu-id="77650-132">\_Storages</span></span>](-storages-table.md)
-   [<span data-ttu-id="77650-133">\_Flussi</span><span class="sxs-lookup"><span data-stu-id="77650-133">\_Streams</span></span>](-streams-table.md)
-   [<span data-ttu-id="77650-134">\_Tabelle</span><span class="sxs-lookup"><span data-stu-id="77650-134">\_Tables</span></span>](-tables-table.md)
-   [<span data-ttu-id="77650-135">\_Tabella transformview</span><span class="sxs-lookup"><span data-stu-id="77650-135">\_TransformView Table</span></span>](-transformview-table.md)
-   [<span data-ttu-id="77650-136">\_Convalida</span><span class="sxs-lookup"><span data-stu-id="77650-136">\_Validation</span></span>](-validation-table.md)

<span data-ttu-id="77650-137">Per disattivare l'opzione di ottimizzazione della patch, usare il criterio [DisableFlyWeightPatching](disableflyweightpatching.md) .</span><span class="sxs-lookup"><span data-stu-id="77650-137">To turn off the patch optimization option, use the [DisableFlyWeightPatching](disableflyweightpatching.md) policy.</span></span>

 

 



