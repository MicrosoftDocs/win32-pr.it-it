---
title: IAgentNotifySinkEx AgentPropertyChange
description: IAgentNotifySinkEx AgentPropertyChange
ms.assetid: 8293cd77-320a-4b57-b3d8-52bc450d6aa0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e27fe9e2318af0642c2df680af3a279ab57253d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955481"
---
# <a name="iagentnotifysinkexagentpropertychange"></a><span data-ttu-id="04299-103">IAgentNotifySinkEx::AgentPropertyChange</span><span class="sxs-lookup"><span data-stu-id="04299-103">IAgentNotifySinkEx::AgentPropertyChange</span></span>

<span data-ttu-id="04299-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="04299-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT AgentPropertyChange(
);
```

<span data-ttu-id="04299-105">Notifica a un'applicazione client quando l'utente modifica un'impostazione della proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="04299-105">Notifies a client application when the user changes a Microsoft Agent property setting.</span></span>

-   <span data-ttu-id="04299-106">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="04299-106">No return value.</span></span>

<span data-ttu-id="04299-107">Quando l'utente modifica un'impostazione della proprietà agente Microsoft nella finestra delle proprietà di Microsoft Agent, il server invia questo evento a tutti i client a meno che il server non sia attualmente sospeso.</span><span class="sxs-lookup"><span data-stu-id="04299-107">When the user changes a Microsoft Agent property setting in the Microsoft Agent property sheet, the server sends this event to all clients unless the server is currently suspended.</span></span>

## <a name="see-also"></a><span data-ttu-id="04299-108">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="04299-108">See Also</span></span>

[<span data-ttu-id="04299-109">**IAgentNotifySinkEx::D efaultCharacterChange**</span><span class="sxs-lookup"><span data-stu-id="04299-109">**IAgentNotifySinkEx::DefaultCharacterChange**</span></span>](iagentnotifysinkex--defaultcharacterchange.md)


 

 




