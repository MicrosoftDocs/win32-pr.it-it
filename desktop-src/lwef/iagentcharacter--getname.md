---
title: GetName IAgentCharacter
description: GetName IAgentCharacter
ms.assetid: 6c013a18-8c56-42a8-8723-31d83b3230cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33679577cfb5179a799ee61207f7ecd9b2be8a21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332764"
---
# <a name="iagentcharactergetname"></a><span data-ttu-id="18c08-103">IAgentCharacter:: GetName</span><span class="sxs-lookup"><span data-stu-id="18c08-103">IAgentCharacter::GetName</span></span>

<span data-ttu-id="18c08-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="18c08-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetName(
   BSTR * pbszName   // address of buffer for character name
);
```

<span data-ttu-id="18c08-105">Recupera il nome del carattere.</span><span class="sxs-lookup"><span data-stu-id="18c08-105">Retrieves the name of the character.</span></span>

-   <span data-ttu-id="18c08-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="18c08-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="18c08-107"><span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*pbszName*</span><span class="sxs-lookup"><span data-stu-id="18c08-107"><span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*pbszName*</span></span>
</dt> <dd>

<span data-ttu-id="18c08-108">Indirizzo di un BSTR che riceve il valore del nome per il carattere.</span><span class="sxs-lookup"><span data-stu-id="18c08-108">The address of a BSTR that receives the value of the name for the character.</span></span>

</dd> </dl>

<span data-ttu-id="18c08-109">Il nome predefinito di un carattere viene definito quando viene compilato con l'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="18c08-109">A character's default name is defined when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="18c08-110">Il nome di un carattere può variare in base all'ID lingua del carattere.</span><span class="sxs-lookup"><span data-stu-id="18c08-110">A character's name may vary based on the character's language ID.</span></span> <span data-ttu-id="18c08-111">I caratteri possono essere compilati con nomi diversi per le diverse lingue.</span><span class="sxs-lookup"><span data-stu-id="18c08-111">Characters can be compiled with different names for different languages.</span></span>

<span data-ttu-id="18c08-112">È anche possibile impostare il nome del carattere usando **IAgentCharacter: Sename**; Tuttavia, modifica il nome per tutti i client correnti del carattere.</span><span class="sxs-lookup"><span data-stu-id="18c08-112">You can also set the character's name using **IAgentCharacter:SetName**; however, this changes the name for all current clients of the character.</span></span>

## <a name="see-also"></a><span data-ttu-id="18c08-113">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="18c08-113">See Also</span></span>

[<span data-ttu-id="18c08-114">**IAgentCharacter:: nome**</span><span class="sxs-lookup"><span data-stu-id="18c08-114">**IAgentCharacter::SetName**</span></span>](iagentcharacter--setname.md)


 

 




