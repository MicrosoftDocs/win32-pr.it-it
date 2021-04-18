---
title: IAgentCommandWindow GetVisible
description: IAgentCommandWindow GetVisible
ms.assetid: a69a2aaa-5a3a-46b8-b505-49609a2aa5ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c66c6d7bf2ee59512f478fd8daa7cee882515690
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298015"
---
# <a name="iagentcommandwindowgetvisible"></a><span data-ttu-id="bf664-103">IAgentCommandWindow:: GetVisible</span><span class="sxs-lookup"><span data-stu-id="bf664-103">IAgentCommandWindow::GetVisible</span></span>

<span data-ttu-id="bf664-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bf664-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for Visible setting for 
);                   // Voice Commands Window
```

<span data-ttu-id="bf664-105">Determina se la finestra dei comandi vocali è visibile o nascosta.</span><span class="sxs-lookup"><span data-stu-id="bf664-105">Determines whether the Voice Commands Window is visible or hidden.</span></span>

-   <span data-ttu-id="bf664-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="bf664-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="bf664-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span><span class="sxs-lookup"><span data-stu-id="bf664-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span></span>
</dt> <dd>

<span data-ttu-id="bf664-108">Indirizzo di una variabile che riceve **true** se la finestra dei comandi vocali è visibile oppure **false** se nascosta.</span><span class="sxs-lookup"><span data-stu-id="bf664-108">Address of a variable that receives **True** if the Voice Commands Window is visible, or **False** if hidden.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="bf664-109">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="bf664-109">See Also</span></span>

[<span data-ttu-id="bf664-110">**IAgentCommandWindow:: sevisible**</span><span class="sxs-lookup"><span data-stu-id="bf664-110">**IAgentCommandWindow::SetVisible**</span></span>](iagentcommandwindow--setvisible.md)


 

 




