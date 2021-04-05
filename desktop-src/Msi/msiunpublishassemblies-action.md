---
description: L'azione MsiUnpublishAssemblies gestisce l'annuncio degli assembly Common Language Runtime e degli assembly Win32 da rimuovere.
ms.assetid: 199d72be-bbe1-4777-a913-2e4b92576bfa
title: Azione MsiUnpublishAssemblies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91d398c66781e6e356b110828c56de6f5e616775
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884113"
---
# <a name="msiunpublishassemblies-action"></a><span data-ttu-id="44866-103">Azione MsiUnpublishAssemblies</span><span class="sxs-lookup"><span data-stu-id="44866-103">MsiUnpublishAssemblies Action</span></span>

<span data-ttu-id="44866-104">L'azione MsiUnpublishAssemblies gestisce l'annuncio degli assembly Common Language Runtime e degli assembly Win32 da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="44866-104">The MsiUnpublishAssemblies action manages the advertisement of common language runtime assemblies and Win32 assemblies that are being removed.</span></span> <span data-ttu-id="44866-105">L'azione esegue una query sulla [tabella MsiAssembly](msiassembly-table.md) per determinare quali assembly hanno annunciato o installato funzionalità da rimuovere dal Global assembly cache e quali assembly hanno un componente padre annunciato o installato rimosso da un percorso isolato per una particolare applicazione.</span><span class="sxs-lookup"><span data-stu-id="44866-105">The action queries the [MsiAssembly table](msiassembly-table.md) to determine which assemblies have advertised or installed features being removed from the global assembly cache and which assemblies have an advertised or installed parent component being removed from a location isolated for a particular application.</span></span> <span data-ttu-id="44866-106">Per informazioni, vedere [installazione di assembly nella global assembly cache](installation-of-assemblies-to-the-global-assembly-cache.md) e [installazione di assembly Win32](installation-of-win32-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="44866-106">For information see, [Installation of Assemblies to the Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md) and [Installation of Win32 Assemblies](installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="44866-107">Nei sistemi che eseguono Windows XP e versioni successive Windows Installer possibile installare assembly Win32 come [assembly side-by-side](side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="44866-107">On systems running Windows XP and later, Windows Installer can install Win32 assemblies as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="44866-108">Per ulteriori informazioni, vedere [informazioni sulle applicazioni isolate e gli assembly affiancati](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="44866-108">For more information, see [About Isolated Applications and Side-by-side Assemblies](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="44866-109">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="44866-109">Sequence Restrictions</span></span>

<span data-ttu-id="44866-110">L'azione MsiUnpublishAssemblies deve essere successiva all' [azione InstallInitialize](installinitialize-action.md) nella [tabella InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="44866-110">The MsiUnpublishAssemblies action must come after the [InstallInitialize action](installinitialize-action.md) in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="44866-111">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="44866-111">ActionData Messages</span></span>



| <span data-ttu-id="44866-112">Campo</span><span class="sxs-lookup"><span data-stu-id="44866-112">Field</span></span> | <span data-ttu-id="44866-113">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="44866-113">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="44866-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="44866-114">\[1\]</span></span> | <span data-ttu-id="44866-115">Contesto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="44866-115">Application context.</span></span>       |
| <span data-ttu-id="44866-116">\[2\]</span><span class="sxs-lookup"><span data-stu-id="44866-116">\[2\]</span></span> | <span data-ttu-id="44866-117">Nome dell'assembly.</span><span class="sxs-lookup"><span data-stu-id="44866-117">Assembly name.</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="44866-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="44866-118">Remarks</span></span>

<span data-ttu-id="44866-119">L' [azione MsiPublishAssemblies](msipublishassemblies-action.md) gestisce l'annuncio degli assembly da annunciare o installare.</span><span class="sxs-lookup"><span data-stu-id="44866-119">The [MsiPublishAssemblies Action](msipublishassemblies-action.md) manages the advertisement of assemblies being advertised or installed.</span></span>

 

 
