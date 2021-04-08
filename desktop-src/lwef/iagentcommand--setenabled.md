---
title: IAgentCommand abilitato
description: IAgentCommand abilitato
ms.assetid: e0a724b4-3613-400f-a801-efc8bf66e355
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8377307d66257f7a9b74ac82512edc6e4ec64034
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046618"
---
# <a name="iagentcommandsetenabled"></a><span data-ttu-id="b5562-103">IAgentCommand:: IsEnabled</span><span class="sxs-lookup"><span data-stu-id="b5562-103">IAgentCommand::SetEnabled</span></span>

<span data-ttu-id="b5562-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b5562-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetEnabled(
   long bEnabled  // Enabled setting for Command
);
```

<span data-ttu-id="b5562-105">Imposta la proprietà [**Enabled**](enabled-property.md) per un [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="b5562-105">Sets the [**Enabled**](enabled-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="b5562-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="b5562-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="b5562-107"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span><span class="sxs-lookup"><span data-stu-id="b5562-107"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="b5562-108">Valore booleano che imposta il valore dell'impostazione [**Enabled**](enabled-property.md) di un [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="b5562-108">A Boolean value that sets the value of the [**Enabled**](enabled-property.md) setting of a [**Command**](/windows/desktop/lwef/the-command-object).</span></span> <span data-ttu-id="b5562-109">**True** Abilita il **comando**; **False** lo Disabilita.</span><span class="sxs-lookup"><span data-stu-id="b5562-109">**True** enables the **Command**; **False** disables it.</span></span> <span data-ttu-id="b5562-110">Non è possibile selezionare un **comando** disabilitato.</span><span class="sxs-lookup"><span data-stu-id="b5562-110">A disabled **Command** cannot be selected.</span></span>

</dd> </dl>

<span data-ttu-id="b5562-111">Un [**comando**](/windows/desktop/lwef/the-command-object) deve avere la proprietà [**Enabled**](enabled-property.md) impostata su **true** per essere selezionabile.</span><span class="sxs-lookup"><span data-stu-id="b5562-111">A [**Command**](/windows/desktop/lwef/the-command-object) must have its [**Enabled**](enabled-property.md) property set to **True** to be selectable.</span></span> <span data-ttu-id="b5562-112">È inoltre necessario impostare la relativa proprietà [**Caption**](caption-property.md) e la relativa proprietà [**Visible**](visible-property.md) su **true** per la visualizzazione nel menu popup del carattere.</span><span class="sxs-lookup"><span data-stu-id="b5562-112">It also must have its [**Caption**](caption-property.md) property set and its [**Visible**](visible-property.md) property set to **True** to appear in the character's pop-up menu.</span></span> <span data-ttu-id="b5562-113">Per fare in modo che il **comando** venga visualizzato nella **finestra comandi vocali**, è necessario impostare la relativa proprietà [**Voice**](voice-property.md).</span><span class="sxs-lookup"><span data-stu-id="b5562-113">To make the **Command** appear in the **Voice Commands Window**, you must set its [**Voice**](voice-property.md)property.</span></span>

## <a name="see-also"></a><span data-ttu-id="b5562-114">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b5562-114">See Also</span></span>

<span data-ttu-id="b5562-115">[**IAgentCommand:: GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand:: sevoice**](iagentcommand--setvoice.md), [**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="b5562-115">[**IAgentCommand::GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 