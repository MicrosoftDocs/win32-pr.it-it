---
title: IAgentCharacterEx GetVersion
description: IAgentCharacterEx GetVersion
ms.assetid: 78f6d7b6-f72d-4af8-a014-3acd185926f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5c72d9304aa689cda83117d57f26c2da776c9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044527"
---
# <a name="iagentcharacterexgetversion"></a><span data-ttu-id="cb0ab-103">IAgentCharacterEx:: GetVersion</span><span class="sxs-lookup"><span data-stu-id="cb0ab-103">IAgentCharacterEx::GetVersion</span></span>

<span data-ttu-id="cb0ab-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cb0ab-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVersion(
   short * psMajor,  // address of major version
   short * psMinor   // address of minor version
);
```

<span data-ttu-id="cb0ab-105">Recupera il numero di versione del set di animazioni standard dei caratteri.</span><span class="sxs-lookup"><span data-stu-id="cb0ab-105">Retrieves the version number of the character standard animation set.</span></span>

-   <span data-ttu-id="cb0ab-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="cb0ab-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="cb0ab-107"><span id="psMajor"></span><span id="psmajor"></span><span id="PSMAJOR"></span>*psMajor*</span><span class="sxs-lookup"><span data-stu-id="cb0ab-107"><span id="psMajor"></span><span id="psmajor"></span><span id="PSMAJOR"></span>*psMajor*</span></span>
</dt> <dd>

<span data-ttu-id="cb0ab-108">Indirizzo di una variabile che riceve la versione principale.</span><span class="sxs-lookup"><span data-stu-id="cb0ab-108">Address of a variable that receives the major version.</span></span>

</dd> <dt>

<span data-ttu-id="cb0ab-109"><span id="psMinor"></span><span id="psminor"></span><span id="PSMINOR"></span>*psMinor*</span><span class="sxs-lookup"><span data-stu-id="cb0ab-109"><span id="psMinor"></span><span id="psminor"></span><span id="PSMINOR"></span>*psMinor*</span></span>
</dt> <dd>

<span data-ttu-id="cb0ab-110">Indirizzo di una variabile che riceve la versione secondaria.</span><span class="sxs-lookup"><span data-stu-id="cb0ab-110">Address of a variable that receives the minor version.</span></span>

</dd> </dl>

<span data-ttu-id="cb0ab-111">Il numero di versione del set di animazioni standard viene impostato automaticamente quando lo si compila con l'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="cb0ab-111">The standard animation set version number is automatically set when you build it with the Microsoft Agent Character Editor.</span></span>

 

 




