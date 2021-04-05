---
title: IAgentCharacter GetIdleOn
description: IAgentCharacter GetIdleOn
ms.assetid: e5371326-33d0-4ecc-bda7-28f36f46ddeb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fdaf3ea460a76549112741ac77f83e10ec37cd9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714593"
---
# <a name="iagentcharactergetidleon"></a><span data-ttu-id="6324f-103">IAgentCharacter::GetIdleOn</span><span class="sxs-lookup"><span data-stu-id="6324f-103">IAgentCharacter::GetIdleOn</span></span>

<span data-ttu-id="6324f-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6324f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetIdleOn(
   long * pbOn  // address of idle processing flag
);
```

<span data-ttu-id="6324f-105">Indica lo stato di elaborazione automatico inattivo per un carattere.</span><span class="sxs-lookup"><span data-stu-id="6324f-105">Indicates the automatic idle processing state for a character.</span></span>

-   <span data-ttu-id="6324f-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="6324f-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="6324f-107"><span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*</span><span class="sxs-lookup"><span data-stu-id="6324f-107"><span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*</span></span>
</dt> <dd>

<span data-ttu-id="6324f-108">Indirizzo di una variabile che riceve **true** se il server Microsoft Agent esegue automaticamente le animazioni di stato al **minimo** per un carattere e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6324f-108">Address of a variable that receives **True** if the Microsoft Agent server automatically plays **Idling** state animations for a character and **False** if not.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="6324f-109">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="6324f-109">See Also</span></span>

[<span data-ttu-id="6324f-110">**IAgentCharacter::SetIdleOn**</span><span class="sxs-lookup"><span data-stu-id="6324f-110">**IAgentCharacter::SetIdleOn**</span></span>](iagentcharacter--setidleon.md)


 

 




