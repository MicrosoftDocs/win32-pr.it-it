---
title: IAgentNotifySink BalloonVisibleState
description: IAgentNotifySink BalloonVisibleState
ms.assetid: 240e049c-7167-41b7-b092-95ed2a83aad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2dd63d8eef3a7f1a70af81e13506a7e92ad84f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298494"
---
# <a name="iagentnotifysinkballoonvisiblestate"></a><span data-ttu-id="86d66-103">IAgentNotifySink::BalloonVisibleState</span><span class="sxs-lookup"><span data-stu-id="86d66-103">IAgentNotifySink::BalloonVisibleState</span></span>

<span data-ttu-id="86d66-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="86d66-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT BalloonVisibleState(
   long dwCharID,  // character ID
   long bVisible   // visibility flag
);                          
```

<span data-ttu-id="86d66-105">Notifica a un'applicazione client quando viene modificato lo stato di visibilità del fumetto di parole del carattere.</span><span class="sxs-lookup"><span data-stu-id="86d66-105">Notifies a client application when the visibility state of the character's word balloon changes.</span></span>

-   <span data-ttu-id="86d66-106">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="86d66-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="86d66-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="86d66-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="86d66-108">Identificatore del carattere il cui stato di visibilità del fumetto di parola è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="86d66-108">Identifier of the character whose word balloon's visibility state has changed.</span></span>

</dd> <dt>

<span data-ttu-id="86d66-109"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="86d66-109"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="86d66-110">Flag di visibilità.</span><span class="sxs-lookup"><span data-stu-id="86d66-110">Visibility flag.</span></span> <span data-ttu-id="86d66-111">Questo valore booleano è **true** quando il fumetto di parola del carattere diventa visibile; e **false** quando viene nascosta.</span><span class="sxs-lookup"><span data-stu-id="86d66-111">This Boolean value is **True** when character's word balloon becomes visible; and **False** when it becomes hidden.</span></span>

</dd> </dl>

<span data-ttu-id="86d66-112">Questo evento viene inviato a tutti i client del carattere.</span><span class="sxs-lookup"><span data-stu-id="86d66-112">This event is sent to all clients of the character.</span></span>

 

 




