---
title: IAgentCharacter GetVisible
description: IAgentCharacter GetVisible
ms.assetid: 6e8e3a68-a7bb-4afb-a753-836fe82a0b24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0593b9b3a193b9d5910888b81b4ecba90469b1e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117595"
---
# <a name="iagentcharactergetvisible"></a><span data-ttu-id="7c9ee-103">IAgentCharacter:: GetVisible</span><span class="sxs-lookup"><span data-stu-id="7c9ee-103">IAgentCharacter::GetVisible</span></span>

<span data-ttu-id="7c9ee-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7c9ee-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for character Visible setting
);
```

<span data-ttu-id="7c9ee-105">Determina se il frame di animazione del carattere è attualmente visibile.</span><span class="sxs-lookup"><span data-stu-id="7c9ee-105">Determines whether the character's animation frame is currently visible.</span></span>

-   <span data-ttu-id="7c9ee-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="7c9ee-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="7c9ee-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span><span class="sxs-lookup"><span data-stu-id="7c9ee-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span></span>
</dt> <dd>

<span data-ttu-id="7c9ee-108">Indirizzo di una variabile che riceve **true** se il frame del carattere è visibile e **false** se è nascosto.</span><span class="sxs-lookup"><span data-stu-id="7c9ee-108">Address of a variable that receives **True** if the character's frame is visible and **False** if hidden.</span></span>

</dd> </dl>

<span data-ttu-id="7c9ee-109">È possibile utilizzare questo metodo per determinare se il frame del carattere è attualmente visibile.</span><span class="sxs-lookup"><span data-stu-id="7c9ee-109">You can use this method to determine whether the character's frame is currently visible.</span></span> <span data-ttu-id="7c9ee-110">Per rendere visibile un carattere, usare il metodo [**show**](/windows/desktop/lwef/iagentcharacter--show) .</span><span class="sxs-lookup"><span data-stu-id="7c9ee-110">To make a character visible, use the [**Show**](/windows/desktop/lwef/iagentcharacter--show) method.</span></span> <span data-ttu-id="7c9ee-111">Per nascondere un carattere, usare il metodo [**Hide**](/windows/desktop/lwef/iagentcharacter--hide) .</span><span class="sxs-lookup"><span data-stu-id="7c9ee-111">To hide a character, use the [**Hide**](/windows/desktop/lwef/iagentcharacter--hide) method.</span></span>

 

 