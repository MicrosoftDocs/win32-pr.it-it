---
title: GetGuid IAgentCharacterEx
description: GetGuid IAgentCharacterEx
ms.assetid: 25fb2531-a81c-4add-8134-77b1cd57cfe3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c9e0e14d0931774bf6ab5e1c8599bbebaadd0ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955673"
---
# <a name="iagentcharacterexgetguid"></a><span data-ttu-id="638c1-103">IAgentCharacterEx:: GetGuid</span><span class="sxs-lookup"><span data-stu-id="638c1-103">IAgentCharacterEx::GetGUID</span></span>

<span data-ttu-id="638c1-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="638c1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetGUID(
   BSTR * pbszGUID  // address of character's ID
);
```

<span data-ttu-id="638c1-105">Recupera l'ID univoco per il carattere.</span><span class="sxs-lookup"><span data-stu-id="638c1-105">Retrieves the unique ID for the character.</span></span>

-   <span data-ttu-id="638c1-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="638c1-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="638c1-107"><span id="pbszGUID"></span><span id="pbszguid"></span><span id="PBSZGUID"></span>*pbszGUID*</span><span class="sxs-lookup"><span data-stu-id="638c1-107"><span id="pbszGUID"></span><span id="pbszguid"></span><span id="PBSZGUID"></span>*pbszGUID*</span></span>
</dt> <dd>

<span data-ttu-id="638c1-108">Indirizzo di un BSTR che riceve l'ID per il carattere.</span><span class="sxs-lookup"><span data-stu-id="638c1-108">Address of a BSTR that receives the ID for the character.</span></span>

</dd> </dl>

<span data-ttu-id="638c1-109">La proprietà restituisce una rappresentazione di stringa del GUID (formattato con parentesi graffe e trattini) utilizzata dal server per identificare in modo univoco il carattere.</span><span class="sxs-lookup"><span data-stu-id="638c1-109">The property returns a string representation of the GUID (formatted with braces and dashes) that the server uses to uniquely identify the character.</span></span> <span data-ttu-id="638c1-110">Quando viene compilato con l'editor dei caratteri di Microsoft Agent, viene impostato un identificatore di caratteri.</span><span class="sxs-lookup"><span data-stu-id="638c1-110">A character identifier is set when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="638c1-111">la proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="638c1-111">The property is read-only.</span></span>

 

 




