---
title: IAgentCommand GetEnabled
description: IAgentCommand GetEnabled
ms.assetid: b4ec25d2-b2e0-4b1b-8dc5-10fbb44149b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238844a70ea7fde3ef0c07cad1a6f3abab5613d1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472931"
---
# <a name="iagentcommandgetenabled"></a><span data-ttu-id="64c0e-103">IAgentCommand:: GetEnabled</span><span class="sxs-lookup"><span data-stu-id="64c0e-103">IAgentCommand::GetEnabled</span></span>

<span data-ttu-id="64c0e-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="64c0e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetEnabled(
   long * pbEnabled  // address of Enabled setting for Command
);
```

<span data-ttu-id="64c0e-105">Recupera il valore della proprietà [**Enabled**](enabled-property.md) per un [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="64c0e-105">Retrieves the value of the [**Enabled**](enabled-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="64c0e-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="64c0e-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="64c0e-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span><span class="sxs-lookup"><span data-stu-id="64c0e-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="64c0e-108">Indirizzo di una variabile che riceve **true** se il [**comando**](/windows/desktop/lwef/the-command-object) è abilitato oppure **false** se è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="64c0e-108">The address of a variable that receives **True** if the [**Command**](/windows/desktop/lwef/the-command-object) is enabled, or **False** if it is disabled.</span></span> <span data-ttu-id="64c0e-109">Non è possibile selezionare un **comando** disabilitato.</span><span class="sxs-lookup"><span data-stu-id="64c0e-109">A disabled **Command** cannot be selected.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="64c0e-110">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="64c0e-110">See Also</span></span>

<span data-ttu-id="64c0e-111">[**IAgentCommand:: Caption**](iagentcommand--setcaption.md), [**IAgentCommand:: sevisible**](iagentcommand--setvisible.md), [**IAgentCommand:: sevoice**](iagentcommand--setvoice.md), [**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="64c0e-111">[**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 