---
title: GetBackColor IAgentBalloon
description: GetBackColor IAgentBalloon
ms.assetid: 278ed645-0e6c-4a5d-bd85-3e3b7a1e3333
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cce886c9929892c89b56f162f784dc27a472209
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044912"
---
# <a name="iagentballoongetbackcolor"></a><span data-ttu-id="0acb4-103">IAgentBalloon:: GetBackColor</span><span class="sxs-lookup"><span data-stu-id="0acb4-103">IAgentBalloon::GetBackColor</span></span>

<span data-ttu-id="0acb4-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0acb4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetBackColor(
   long * plBGColor  // address of variable for background color displayed
);                   // in word balloon
```

<span data-ttu-id="0acb4-105">Recupera il valore per il colore di sfondo visualizzato in un fumetto di Word.</span><span class="sxs-lookup"><span data-stu-id="0acb4-105">Retrieves the value for the background color displayed in a word balloon.</span></span>

-   <span data-ttu-id="0acb4-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="0acb4-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="0acb4-107"><span id="plBGColor"></span><span id="plbgcolor"></span><span id="PLBGCOLOR"></span>*plBGColor*</span><span class="sxs-lookup"><span data-stu-id="0acb4-107"><span id="plBGColor"></span><span id="plbgcolor"></span><span id="PLBGCOLOR"></span>*plBGColor*</span></span>
</dt> <dd>

<span data-ttu-id="0acb4-108">Indirizzo di una variabile che riceve l'impostazione del colore per lo sfondo del fumetto.</span><span class="sxs-lookup"><span data-stu-id="0acb4-108">The address of a variable that receives the color setting for the balloon background.</span></span>

</dd> </dl>

<span data-ttu-id="0acb4-109">Il colore di sfondo utilizzato in un fumetto di parole è definito nell'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="0acb4-109">The background color used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="0acb4-110">Non può essere modificato da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0acb4-110">It cannot be changed by an application.</span></span> <span data-ttu-id="0acb4-111">Tuttavia, l'utente può modificare il colore di sfondo delle parole Balloon per tutti i caratteri tramite la finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="0acb4-111">However, the user can change the background color of the word balloons for all characters through the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="0acb4-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="0acb4-112">See Also</span></span>

[<span data-ttu-id="0acb4-113">**IAgentBalloon:: GetForeColor**</span><span class="sxs-lookup"><span data-stu-id="0acb4-113">**IAgentBalloon::GetForeColor**</span></span>](iagentballoon--getforecolor.md)


 

 




