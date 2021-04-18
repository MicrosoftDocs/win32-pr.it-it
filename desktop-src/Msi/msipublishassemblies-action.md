---
description: L'azione MsiPublishAssemblies gestisce l'annuncio degli assembly Common Language Runtime e degli assembly Win32.
ms.assetid: 4bc67f43-7a7e-4bd3-aa83-610b46a54e11
title: Azione MsiPublishAssemblies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24e1787aeb87cf00eb82aefab375771c7c1ddc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318655"
---
# <a name="msipublishassemblies-action"></a><span data-ttu-id="eefe8-103">Azione MsiPublishAssemblies</span><span class="sxs-lookup"><span data-stu-id="eefe8-103">MsiPublishAssemblies Action</span></span>

<span data-ttu-id="eefe8-104">L'azione MsiPublishAssemblies gestisce l'annuncio degli assembly Common Language Runtime e degli assembly Win32.</span><span class="sxs-lookup"><span data-stu-id="eefe8-104">The MsiPublishAssemblies action manages the advertisement of common language runtime assemblies and Win32 assemblies.</span></span> <span data-ttu-id="eefe8-105">L'azione esegue una query sulla [tabella MsiAssembly](msiassembly-table.md) per determinare quali assembly hanno funzionalità annunciate o installate nel Global assembly cache e quali assembly dispongono di un componente padre annunciato o installato in un percorso isolato per una particolare applicazione.</span><span class="sxs-lookup"><span data-stu-id="eefe8-105">The action queries the [MsiAssembly table](msiassembly-table.md) to determine which assemblies have features being advertised or installed to the global assembly cache and which assemblies have a parent component being advertised or installed to a location isolated for a particular application.</span></span> <span data-ttu-id="eefe8-106">Per informazioni, vedere [installazione di assembly nella global assembly cache](installation-of-assemblies-to-the-global-assembly-cache.md) e [installazione di assembly Win32](installation-of-win32-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="eefe8-106">For information see, [Installation of Assemblies to the Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md) and [Installation of Win32 Assemblies](installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="eefe8-107">Nei sistemi Microsoft Windows XP e versioni successive Windows Installer possibile installare assembly Win32 come [assembly side-by-side](side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="eefe8-107">On Microsoft Windows XP and later systems, Windows Installer can install Win32 assemblies as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="eefe8-108">Per ulteriori informazioni, vedere [informazioni sulle applicazioni isolate e gli assembly affiancati](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="eefe8-108">For more information, see [About Isolated Applications and Side-by-side Assemblies](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="eefe8-109">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="eefe8-109">Sequence Restrictions</span></span>

<span data-ttu-id="eefe8-110">L'azione MsiPublishAssemblies deve essere successiva all' [azione InstallInitialize](installinitialize-action.md) nella tabella [InstallExecuteSequence](installexecutesequence-table.md) o [AdvtExecuteSequence](advtexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="eefe8-110">The MsiPublishAssemblies action must come after the [InstallInitialize action](installinitialize-action.md) in the [InstallExecuteSequence table](installexecutesequence-table.md) or [AdvtExecuteSequence table](advtexecutesequence-table.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="eefe8-111">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="eefe8-111">ActionData Messages</span></span>



| <span data-ttu-id="eefe8-112">Campo</span><span class="sxs-lookup"><span data-stu-id="eefe8-112">Field</span></span> | <span data-ttu-id="eefe8-113">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="eefe8-113">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="eefe8-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="eefe8-114">\[1\]</span></span> | <span data-ttu-id="eefe8-115">Contesto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="eefe8-115">Application context.</span></span>       |
| <span data-ttu-id="eefe8-116">\[2\]</span><span class="sxs-lookup"><span data-stu-id="eefe8-116">\[2\]</span></span> | <span data-ttu-id="eefe8-117">Nome dell'assembly.</span><span class="sxs-lookup"><span data-stu-id="eefe8-117">Assembly name.</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="eefe8-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="eefe8-118">Remarks</span></span>

<span data-ttu-id="eefe8-119">Per ulteriori informazioni, vedere [assembly](assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="eefe8-119">For more information, see [Assemblies](assemblies.md).</span></span>

<span data-ttu-id="eefe8-120">L' [azione MsiUnpublishAssemblies](msiunpublishassemblies-action.md) gestisce l'annuncio degli assembly da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="eefe8-120">The [MsiUnpublishAssemblies Action](msiunpublishassemblies-action.md) manages the advertisement of assemblies being removed.</span></span>

 

 
