---
title: IAgentCommand visibile
description: IAgentCommand visibile
ms.assetid: 58a383f4-6c98-4037-b469-ae68f06c852d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b583f79a93a5b13914486fb3e1a9cb513a682e63
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299769"
---
# <a name="iagentcommandsetvisible"></a><span data-ttu-id="dc4c9-103">IAgentCommand:: sevisible</span><span class="sxs-lookup"><span data-stu-id="dc4c9-103">IAgentCommand::SetVisible</span></span>

<span data-ttu-id="dc4c9-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="dc4c9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVisible(
   long bVisible  // Visible setting for Command
);
```

<span data-ttu-id="dc4c9-105">Imposta il valore della proprietà [**Visible**](visible-property.md) per un [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="dc4c9-105">Sets the value of the [**Visible**](visible-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="dc4c9-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="dc4c9-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="dc4c9-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="dc4c9-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="dc4c9-108">Valore booleano che determina la proprietà [**Visible**](visible-property.md) di un [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="dc4c9-108">A Boolean value that determines the [**Visible**](visible-property.md) property of a [**Command**](/windows/desktop/lwef/the-command-object).</span></span> <span data-ttu-id="dc4c9-109">**True** Mostra il **comando**; **False** lo nasconde.</span><span class="sxs-lookup"><span data-stu-id="dc4c9-109">**True** shows the **Command**; **False** hides it.</span></span>

</dd> </dl>

<span data-ttu-id="dc4c9-110">Un [**comando**](/windows/desktop/lwef/the-command-object) deve avere la proprietà [**Visible**](visible-property.md) impostata su **true** e la relativa proprietà [**Caption**](caption-property.md) impostata su viene visualizzata nel menu di scelta rapida del carattere.</span><span class="sxs-lookup"><span data-stu-id="dc4c9-110">A [**Command**](/windows/desktop/lwef/the-command-object) must have its [**Visible**](visible-property.md) property set to **True** and its [**Caption**](caption-property.md) property set to appear in the character's pop-up menu.</span></span>

## <a name="see-also"></a><span data-ttu-id="dc4c9-111">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="dc4c9-111">See Also</span></span>

<span data-ttu-id="dc4c9-112">[**IAgentCommand:: getVisible**](iagentcommand--getvisible.md), [**IAgentCommand:: Caption**](iagentcommand--setcaption.md), [**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="dc4c9-112">[**IAgentCommand::GetVisible**](iagentcommand--getvisible.md), [**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 