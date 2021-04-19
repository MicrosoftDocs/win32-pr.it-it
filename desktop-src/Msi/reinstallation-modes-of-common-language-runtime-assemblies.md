---
description: Gli assembly Common Language Runtime installati nel Global Assembly Cache devono disporre di file identici in tutte le occorrenze dell'assembly.
ms.assetid: 02b4ad60-d28d-44b8-955f-b367197e69c3
title: Modalità di reinstallazione degli assembly Common Language Runtime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8512e4c6e888c7d67b2ca252184fa4f748445fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311699"
---
# <a name="reinstallation-modes-of-common-language-runtime-assemblies"></a><span data-ttu-id="09161-103">Modalità di reinstallazione degli assembly Common Language Runtime</span><span class="sxs-lookup"><span data-stu-id="09161-103">Reinstallation Modes of Common Language Runtime Assemblies</span></span>

<span data-ttu-id="09161-104">Gli assembly Common Language Runtime installati nel Global Assembly Cache devono disporre di file identici in tutte le occorrenze dell'assembly.</span><span class="sxs-lookup"><span data-stu-id="09161-104">Common language runtime assemblies that are installed to the global assembly cache must have identical files in all occurrences of the assembly.</span></span> <span data-ttu-id="09161-105">Ciò significa che le modalità di reinstallazione utilizzate da [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea) e [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) devono avere significati diversi per i componenti regolari e gli assembly Common Language Runtime.</span><span class="sxs-lookup"><span data-stu-id="09161-105">This means that the reinstallation modes used by [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea) and [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) must have different meanings for regular components and common language runtime assemblies.</span></span> <span data-ttu-id="09161-106">Le seguenti definizioni di modalità di reinstallazione si applicano agli assembly Common Language Runtime.</span><span class="sxs-lookup"><span data-stu-id="09161-106">The following definitions of reinstall modes apply to common language runtime assemblies.</span></span>



| <span data-ttu-id="09161-107">Modalità di reinstallazione</span><span class="sxs-lookup"><span data-stu-id="09161-107">Reinstall mode</span></span>                  | <span data-ttu-id="09161-108">Significato per i componenti di Microsoft .NET</span><span class="sxs-lookup"><span data-stu-id="09161-108">Meaning for Microsoft .NET Components</span></span>                                                                                              |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09161-109">REINSTALLMODE \_ FILEmissing</span><span class="sxs-lookup"><span data-stu-id="09161-109">REINSTALLMODE\_FILEMISSING</span></span>      | <span data-ttu-id="09161-110">Installare o reinstallare il componente Common Language Runtime se è mancante o incompleto.</span><span class="sxs-lookup"><span data-stu-id="09161-110">Install or reinstall the common language runtime component if it is missing or incomplete.</span></span>                                         |
| <span data-ttu-id="09161-111">\_FILEOLDERVERSION REINSTALLMODE</span><span class="sxs-lookup"><span data-stu-id="09161-111">REINSTALLMODE\_FILEOLDERVERSION</span></span> | <span data-ttu-id="09161-112">Installare o reinstallare il componente Common Language Runtime se è mancante o incompleto.</span><span class="sxs-lookup"><span data-stu-id="09161-112">Install or reinstall the common language runtime component if it is missing or incomplete.</span></span>                                         |
| <span data-ttu-id="09161-113">\_FILEEQUALVERSION REINSTALLMODE</span><span class="sxs-lookup"><span data-stu-id="09161-113">REINSTALLMODE\_FILEEQUALVERSION</span></span> | <span data-ttu-id="09161-114">Installare o reinstallare il componente Common Language Runtime se è mancante o incompleto.</span><span class="sxs-lookup"><span data-stu-id="09161-114">Install or reinstall the common language runtime component if it is missing or incomplete.</span></span>                                         |
| <span data-ttu-id="09161-115">fileexact REINSTALLMODE \_</span><span class="sxs-lookup"><span data-stu-id="09161-115">REINSTALLMODE\_FILEEXACT</span></span>        | <span data-ttu-id="09161-116">Installare o reinstallare il componente Common Language Runtime se è mancante o incompleto.</span><span class="sxs-lookup"><span data-stu-id="09161-116">Install or reinstall the common language runtime component if it is missing or incomplete.</span></span>                                         |
| <span data-ttu-id="09161-117">REINSTALLMODE \_ FILEverify</span><span class="sxs-lookup"><span data-stu-id="09161-117">REINSTALLMODE\_FILEVERIFY</span></span>       | <span data-ttu-id="09161-118">Installare o reinstallare il componente Common Language Runtime se è mancante o se il componente esistente è incompleto o danneggiato.</span><span class="sxs-lookup"><span data-stu-id="09161-118">Install or reinstall the common language runtime component if it is missing or if the existing component is incomplete or corrupt.</span></span> |
| <span data-ttu-id="09161-119">REINSTALLMODE \_ FILEreplace</span><span class="sxs-lookup"><span data-stu-id="09161-119">REINSTALLMODE\_FILEREPLACE</span></span>      | <span data-ttu-id="09161-120">Installare o reinstallare sempre il componente Common Language Runtime.</span><span class="sxs-lookup"><span data-stu-id="09161-120">Always install or reinstall the common language runtime component.</span></span>                                                                 |



 

 

 



