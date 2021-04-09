---
description: Gli autori devono eseguire la convalida in ogni nuovo modulo unione, o appena modificato, prima di tentare di unire il modulo in un database di installazione per la prima volta.
ms.assetid: 8d6794af-403a-416e-8ace-1af3f193414b
title: Convalida di moduli merge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d8bbe7f1c1ea32baa39cadd7c729f3a8ca3ac17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129942"
---
# <a name="validating-merge-modules"></a><span data-ttu-id="e6c9e-103">Convalida di moduli merge</span><span class="sxs-lookup"><span data-stu-id="e6c9e-103">Validating Merge Modules</span></span>

<span data-ttu-id="e6c9e-104">Gli autori devono eseguire la convalida in ogni nuovo modulo unione, o appena modificato, prima di tentare di unire il modulo in un database di installazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="e6c9e-104">Authors should run validation on every new, or newly modified, merge module before attempting to merge the module into an installation database for the first time.</span></span> <span data-ttu-id="e6c9e-105">La convalida del modulo merge funziona allo stesso modo della [convalida dei pacchetti](package-validation.md) , ma usa un set diverso di [analizzatori di coerenza interni](internal-consistency-evaluators-ices.md) specifici dei moduli unione.</span><span class="sxs-lookup"><span data-stu-id="e6c9e-105">Merge module validation works in the same way as [package validation](package-validation.md) but uses a different set of [Internal Consistency Evaluators](internal-consistency-evaluators-ices.md) (ICEs) specific to merge modules.</span></span> <span data-ttu-id="e6c9e-106">Per ulteriori informazioni su questi moduli di merge, vedere la pagina relativa al [riferimento ghiaccio del modulo merge](merge-module-ice-reference.md).</span><span class="sxs-lookup"><span data-stu-id="e6c9e-106">For more information about these merge module ICEs, see [Merge Module ICE Reference](merge-module-ice-reference.md).</span></span>

<span data-ttu-id="e6c9e-107">I moduli CIEM di tipo merge vengono archiviati nel file con estensione cub del modulo merge, Mergemod. cub.</span><span class="sxs-lookup"><span data-stu-id="e6c9e-107">Merge module ICEs are stored in the merge module .cub file, Mergemod.cub.</span></span> <span data-ttu-id="e6c9e-108">L'installazione dello strumento Orca o MSIVal2 fornisce anche i file logo. cub, Darice. cub e Mergemod. cub.</span><span class="sxs-lookup"><span data-stu-id="e6c9e-108">The installation of the Orca tool or msival2 also provides the Logo.cub, Darice.cub, and Mergemod.cub files.</span></span>

<span data-ttu-id="e6c9e-109">Per ulteriori informazioni, vedere la pagina relativa al [riferimento ghiaccio del modulo merge](merge-module-ice-reference.md).</span><span class="sxs-lookup"><span data-stu-id="e6c9e-109">For more information, see [Merge Module ICE Reference](merge-module-ice-reference.md).</span></span>

 

 



