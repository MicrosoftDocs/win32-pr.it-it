---
title: IAgentCommand getvoice
description: IAgentCommand getvoice
ms.assetid: 69f3c91b-2ccf-4bea-8034-0c3e0a5e4ec4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2365019f71447e9d9c5a560c6506ee1dae7423df
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299614"
---
# <a name="iagentcommandgetvoice"></a><span data-ttu-id="e3ea9-103">IAgentCommand:: getvoice</span><span class="sxs-lookup"><span data-stu-id="e3ea9-103">IAgentCommand::GetVoice</span></span>

<span data-ttu-id="e3ea9-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e3ea9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVoice(
   BSTR * pbszVoice  // address of Voice setting for Command
);
```

<span data-ttu-id="e3ea9-105">Recupera il valore della proprietà del testo [**vocale**](voice-property.md) per un [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="e3ea9-105">Retrieves the value of the [**Voice**](voice-property.md) text property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="e3ea9-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="e3ea9-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e3ea9-107"><span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszVoice*</span><span class="sxs-lookup"><span data-stu-id="e3ea9-107"><span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszVoice*</span></span>
</dt> <dd>

<span data-ttu-id="e3ea9-108">Indirizzo di un BSTR che riceve la proprietà del testo [**vocale**](voice-property.md) per un [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="e3ea9-108">The address of a BSTR that receives the [**Voice**](voice-property.md) text property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="e3ea9-109">Un [**comando**](/windows/desktop/lwef/the-command-object) con la relativa proprietà [**Voice**](voice-property.md) impostata e la relativa proprietà [**Enabled**](enabled-property.md) impostata su **true** saranno accessibili per la voce.</span><span class="sxs-lookup"><span data-stu-id="e3ea9-109">A [**Command**](/windows/desktop/lwef/the-command-object) with its [**Voice**](voice-property.md) property set and its [**Enabled**](enabled-property.md) property set to **True** will be voice-accessible.</span></span> <span data-ttu-id="e3ea9-110">Se anche la relativa proprietà [**Caption**](caption-property.md) è impostata, viene visualizzata nella finestra dei comandi vocali.</span><span class="sxs-lookup"><span data-stu-id="e3ea9-110">If its [**Caption**](caption-property.md) property is also set it appears in the Voice Commands Window.</span></span> <span data-ttu-id="e3ea9-111">Se la proprietà [**Visible**](visible-property.md) è impostata su **true**, viene visualizzata nel menu di scelta rapida del carattere.</span><span class="sxs-lookup"><span data-stu-id="e3ea9-111">If its [**Visible**](visible-property.md) property is set to **True**, it appears in the character's pop-up menu.</span></span>

## <a name="see-also"></a><span data-ttu-id="e3ea9-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e3ea9-112">See Also</span></span>

<span data-ttu-id="e3ea9-113">[**IAgentCommand:: sevoice**](iagentcommand--setvoice.md), [**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="e3ea9-113">[**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 