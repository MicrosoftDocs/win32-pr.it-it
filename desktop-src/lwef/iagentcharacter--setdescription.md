---
title: IAgentCharacter Descrizione
description: IAgentCharacter Descrizione
ms.assetid: ae01b9e6-1616-4806-9125-ceb4cb54aab1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9815e5c0e01537c7db2b400326f86da37af003
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396978"
---
# <a name="iagentcharactersetdescription"></a><span data-ttu-id="1bb95-103">IAgentCharacter:: FileDescription</span><span class="sxs-lookup"><span data-stu-id="1bb95-103">IAgentCharacter::SetDescription</span></span>

<span data-ttu-id="1bb95-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1bb95-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetDescription(
   BSTR bszDescription   // character description
); 
```

<span data-ttu-id="1bb95-105">Imposta la descrizione del carattere.</span><span class="sxs-lookup"><span data-stu-id="1bb95-105">Sets the description of the character.</span></span>

-   <span data-ttu-id="1bb95-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="1bb95-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="1bb95-107"><span id="bszDescription"></span><span id="bszdescription"></span><span id="BSZDESCRIPTION"></span>*bszDescription*</span><span class="sxs-lookup"><span data-stu-id="1bb95-107"><span id="bszDescription"></span><span id="bszdescription"></span><span id="BSZDESCRIPTION"></span>*bszDescription*</span></span>
</dt> <dd>

<span data-ttu-id="1bb95-108">BSTR che imposta la descrizione per il carattere.</span><span class="sxs-lookup"><span data-stu-id="1bb95-108">A BSTR that sets the description for the character.</span></span> <span data-ttu-id="1bb95-109">La descrizione predefinita di un carattere viene definita quando viene compilata con l'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="1bb95-109">A character's default description is defined when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="1bb95-110">L'impostazione della descrizione è facoltativa e non può essere specificata per tutti i caratteri.</span><span class="sxs-lookup"><span data-stu-id="1bb95-110">The description setting is optional and may not be supplied for all characters.</span></span> <span data-ttu-id="1bb95-111">È possibile modificare la descrizione del carattere usando **IAgentCharacter:: FileDescription**; Tuttavia, questo valore non è permanente (archiviato in modo permanente).</span><span class="sxs-lookup"><span data-stu-id="1bb95-111">You can change the character's description using **IAgentCharacter::setDescription**; however, this value is not persistent (stored permanently).</span></span> <span data-ttu-id="1bb95-112">La descrizione del carattere viene ripristinata l'impostazione predefinita ogni volta che il carattere viene caricato per la prima volta da un client.</span><span class="sxs-lookup"><span data-stu-id="1bb95-112">The character's description reverts to its default setting whenever the character is first loaded by a client.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="1bb95-113">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1bb95-113">See Also</span></span>

[<span data-ttu-id="1bb95-114">**IAgentCharacter:: GetDescription**</span><span class="sxs-lookup"><span data-stu-id="1bb95-114">**IAgentCharacter::GetDescription**</span></span>](iagentcharacter--getdescription.md)


 

 




