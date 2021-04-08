---
description: L'azione PatchFiles esegue una query sulla tabella patch per individuare le patch da applicare. L'azione PatchFiles esegue anche l'applicazione di patch per byte dei file.
ms.assetid: 4026755e-a006-40c0-8816-de5358f4582e
title: Azione PatchFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53583a93089444f014d9cc837fb18acf21cec82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881857"
---
# <a name="patchfiles-action"></a><span data-ttu-id="ce0e9-104">Azione PatchFiles</span><span class="sxs-lookup"><span data-stu-id="ce0e9-104">PatchFiles Action</span></span>

<span data-ttu-id="ce0e9-105">L'azione PatchFiles esegue una query sulla [tabella patch](patch-table.md) per individuare le patch da applicare.</span><span class="sxs-lookup"><span data-stu-id="ce0e9-105">The PatchFiles action queries the [Patch table](patch-table.md) to determine which patches are to be applied.</span></span> <span data-ttu-id="ce0e9-106">L'azione PatchFiles esegue anche l'applicazione di patch per byte dei file.</span><span class="sxs-lookup"><span data-stu-id="ce0e9-106">The PatchFiles action also performs the byte-wise patching of the files.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="ce0e9-107">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="ce0e9-107">Sequence Restrictions</span></span>

<span data-ttu-id="ce0e9-108">Se il file di cui eseguire la patch non è installato, l'azione PatchFiles deve provenire dopo l' [azione InstallFiles](installfiles-action.md) che installa il file.</span><span class="sxs-lookup"><span data-stu-id="ce0e9-108">If the file that is to be patched is not installed, the PatchFiles action must come after the [InstallFiles action](installfiles-action.md) that installs the file.</span></span> <span data-ttu-id="ce0e9-109">I file installati in precedenza possono essere corretti in qualsiasi punto della sequenza di azione.</span><span class="sxs-lookup"><span data-stu-id="ce0e9-109">Previously installed files may be patched at any point in the action sequence.</span></span> <span data-ttu-id="ce0e9-110">L' [azione DuplicateFiles](duplicatefiles-action.md) deve essere successiva all'azione PatchFiles per impedire la duplicazione della versione senza patch del file.</span><span class="sxs-lookup"><span data-stu-id="ce0e9-110">The [DuplicateFiles Action](duplicatefiles-action.md) must come after the PatchFiles action to prevent duplicating the unpatched version of the file.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="ce0e9-111">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="ce0e9-111">ActionData Messages</span></span>



| <span data-ttu-id="ce0e9-112">Campo</span><span class="sxs-lookup"><span data-stu-id="ce0e9-112">Field</span></span> | <span data-ttu-id="ce0e9-113">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="ce0e9-113">Description of action data</span></span>                    |
|-------|-----------------------------------------------|
| <span data-ttu-id="ce0e9-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="ce0e9-114">\[1\]</span></span> | <span data-ttu-id="ce0e9-115">Identificatore del file con patch.</span><span class="sxs-lookup"><span data-stu-id="ce0e9-115">Identifier of patched file.</span></span>                   |
| <span data-ttu-id="ce0e9-116">\[2\]</span><span class="sxs-lookup"><span data-stu-id="ce0e9-116">\[2\]</span></span> | <span data-ttu-id="ce0e9-117">Identificatore della directory contenente il file con patch.</span><span class="sxs-lookup"><span data-stu-id="ce0e9-117">Identifier of directory holding patched file.</span></span> |
| <span data-ttu-id="ce0e9-118">\[3\]</span><span class="sxs-lookup"><span data-stu-id="ce0e9-118">\[3\]</span></span> | <span data-ttu-id="ce0e9-119">Dimensioni in byte della patch.</span><span class="sxs-lookup"><span data-stu-id="ce0e9-119">Size of patch in bytes.</span></span>                       |



 

 

 



