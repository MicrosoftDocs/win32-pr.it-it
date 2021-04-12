---
title: GetID IAgentCommand
description: GetID IAgentCommand
ms.assetid: 4d8d8be7-7003-4ef3-abba-b5232267c993
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d1f5887123df19496c0610c53fe59a3f64961cd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398865"
---
# <a name="iagentcommandgetid"></a><span data-ttu-id="57e4f-103">IAgentCommand:: GetID</span><span class="sxs-lookup"><span data-stu-id="57e4f-103">IAgentCommand::GetID</span></span>

<span data-ttu-id="57e4f-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="57e4f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetID(
   long * pdwID  // address of ID for Command
);
```

<span data-ttu-id="57e4f-105">Recupera l'ID per un [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="57e4f-105">Retrieves the ID for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="57e4f-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="57e4f-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="57e4f-107"><span id="pdwID"></span><span id="pdwid"></span><span id="PDWID"></span>*pdwID*</span><span class="sxs-lookup"><span data-stu-id="57e4f-107"><span id="pdwID"></span><span id="pdwid"></span><span id="PDWID"></span>*pdwID*</span></span>
</dt> <dd>

<span data-ttu-id="57e4f-108">Indirizzo di una variabile che riceve l'ID di un [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="57e4f-108">The address of a variable that receives the ID of a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="57e4f-109">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="57e4f-109">See Also</span></span>

<span data-ttu-id="57e4f-110">[**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md), [**IAgentCommands:: Remove**](iagentcommands--remove.md)</span><span class="sxs-lookup"><span data-stu-id="57e4f-110">[**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md), [**IAgentCommands::Remove**](iagentcommands--remove.md)</span></span>


 

 