---
description: In questo argomento viene descritto come controllare la visibilità del verbo.
title: Come escludere e controllare la visibilità del verbo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f689d8b93ce9facb62b654f3f8be62f665e001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227432"
---
# <a name="how-to-suppress-and-control-verb-visibility"></a><span data-ttu-id="cfef0-103">Come escludere e controllare la visibilità del verbo</span><span class="sxs-lookup"><span data-stu-id="cfef0-103">How to Suppress and Control Verb Visibility</span></span>

<span data-ttu-id="cfef0-104">In questo argomento viene descritto come controllare la visibilità del verbo.</span><span class="sxs-lookup"><span data-stu-id="cfef0-104">This topic tells you how to control verb visibility.</span></span>

## <a name="instructions"></a><span data-ttu-id="cfef0-105">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="cfef0-105">Instructions</span></span>


<span data-ttu-id="cfef0-106">È possibile utilizzare le impostazioni dei criteri di Windows per controllare la visibilità dei verbi.</span><span class="sxs-lookup"><span data-stu-id="cfef0-106">You can use Windows policy settings to control verb visibility.</span></span> <span data-ttu-id="cfef0-107">I verbi possono essere eliminati tramite le impostazioni dei criteri aggiungendo una sottochiave **SuppressionPolicy** o un valore GUID **SuppressionPolicyEx** alla sottochiave del registro di sistema del verbo.</span><span class="sxs-lookup"><span data-stu-id="cfef0-107">Verbs can be suppressed through policy settings by adding a **SuppressionPolicy** subkey or a **SuppressionPolicyEx** GUID value to the verb's registry subkey.</span></span> <span data-ttu-id="cfef0-108">Impostare il valore della sottochiave **SuppressionPolicy** sull'ID criterio.</span><span class="sxs-lookup"><span data-stu-id="cfef0-108">Set the value of the **SuppressionPolicy** subkey to the policy ID.</span></span> <span data-ttu-id="cfef0-109">Se il criterio è attivato, il verbo e la voce del menu di scelta rapida associato vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="cfef0-109">If the policy is turned on, the verb and its associated shortcut menu entry are suppressed.</span></span> <span data-ttu-id="cfef0-110">Per i possibili valori ID dei criteri, vedere l'enumerazione [**restrictions**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) .</span><span class="sxs-lookup"><span data-stu-id="cfef0-110">For possible policy ID values, see the [**RESTRICTIONS**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) enumeration.</span></span>

 

 



