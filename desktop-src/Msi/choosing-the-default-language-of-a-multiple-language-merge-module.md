---
description: La lingua predefinita per un modulo merge è la lingua elencata nella tabella ModuleSignature del modulo prima dell'applicazione delle trasformazioni del linguaggio. Si tratta anche del primo linguaggio elencato nella proprietà di riepilogo del modello.
ms.assetid: 4d795727-684c-4dc1-8b46-d72b69c455c3
title: Scelta della lingua predefinita di un modulo merge a più lingue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758a3b47b7a41777652a11a1cdc1b7f380055cb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881061"
---
# <a name="choosing-the-default-language-of-a-multiple-language-merge-module"></a><span data-ttu-id="2e73f-104">Scelta della lingua predefinita di un modulo merge a più lingue</span><span class="sxs-lookup"><span data-stu-id="2e73f-104">Choosing the Default Language of a Multiple Language Merge Module</span></span>

<span data-ttu-id="2e73f-105">La lingua predefinita per un modulo merge è la lingua elencata nella [tabella ModuleSignature](modulesignature-table.md) del modulo prima dell'applicazione delle trasformazioni del linguaggio.</span><span class="sxs-lookup"><span data-stu-id="2e73f-105">The default language for a merge module is the language that is listed in the [ModuleSignature Table](modulesignature-table.md) of the module before language transforms are applied.</span></span> <span data-ttu-id="2e73f-106">Si tratta anche del primo linguaggio elencato nella proprietà di [**Riepilogo del modello**](template-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="2e73f-106">This is also the first language that is listed in the [**Template Summary**](template-summary.md) Property.</span></span>

<span data-ttu-id="2e73f-107">La lingua predefinita per il modulo deve essere uno dei linguaggi più specifici supportati, perché la lingua predefinita viene sempre controllata per prima e, se soddisfa la lingua richiesta, viene usata anche se un'altra lingua è una corrispondenza migliore.</span><span class="sxs-lookup"><span data-stu-id="2e73f-107">The default language for the module should be one of the most specific languages that you support, because the default language is always checked first, and if it satisfies the requested language, it is used even if another language is a better match.</span></span> <span data-ttu-id="2e73f-108">Se, ad esempio, un modulo supporta 1033 e 0, 1033 deve essere la lingua predefinita.</span><span class="sxs-lookup"><span data-stu-id="2e73f-108">For example, if a module supports 1033 and 0, 1033 should be the default language.</span></span> <span data-ttu-id="2e73f-109">Se 0 era la lingua predefinita, soddisfa sempre qualsiasi richiesta e la trasformazione 1033 non verrebbe mai utilizzata, anche se 1033 è la lingua esatta richiesta.</span><span class="sxs-lookup"><span data-stu-id="2e73f-109">If 0 were the default language, it would always satisfy any request, and the 1033 transform would never be used, even if 1033 is the exact language requested.</span></span>

 

 



