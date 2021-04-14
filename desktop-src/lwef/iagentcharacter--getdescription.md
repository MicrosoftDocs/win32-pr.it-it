---
title: IAgentCharacter GetDescription
description: IAgentCharacter GetDescription
ms.assetid: 729f54ac-1c60-4a7b-b993-5682a6ea2b3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423cd1f5c799cc1f0177f6d3d7922d5d14de1dbe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396994"
---
# <a name="iagentcharactergetdescription"></a><span data-ttu-id="bdf5b-103">IAgentCharacter:: GetDescription</span><span class="sxs-lookup"><span data-stu-id="bdf5b-103">IAgentCharacter::GetDescription</span></span>

<span data-ttu-id="bdf5b-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bdf5b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetDescription(
   BSTR * pbszDescription   // address of buffer for character description
); 
```

<span data-ttu-id="bdf5b-105">Recupera la descrizione del carattere.</span><span class="sxs-lookup"><span data-stu-id="bdf5b-105">Retrieves the description of the character.</span></span>

-   <span data-ttu-id="bdf5b-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="bdf5b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="bdf5b-107"><span id="pbszDescription"></span><span id="pbszdescription"></span><span id="PBSZDESCRIPTION"></span>*pbszDescription*</span><span class="sxs-lookup"><span data-stu-id="bdf5b-107"><span id="pbszDescription"></span><span id="pbszdescription"></span><span id="PBSZDESCRIPTION"></span>*pbszDescription*</span></span>
</dt> <dd>

<span data-ttu-id="bdf5b-108">Indirizzo di un BSTR che riceve il valore della descrizione per il carattere.</span><span class="sxs-lookup"><span data-stu-id="bdf5b-108">The address of a BSTR that receives the value of the description for the character.</span></span> <span data-ttu-id="bdf5b-109">La descrizione di un carattere viene definita quando viene compilata con l'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="bdf5b-109">A character's description is defined when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="bdf5b-110">L'impostazione della descrizione è facoltativa e non può essere specificata per tutti i caratteri.</span><span class="sxs-lookup"><span data-stu-id="bdf5b-110">The description setting is optional and may not be supplied for all characters.</span></span>

</dd> </dl>

 

 




