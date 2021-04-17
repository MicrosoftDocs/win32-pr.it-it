---
title: IAgentCommandEx SetHelpContextID
description: IAgentCommandEx SetHelpContextID
ms.assetid: 861d55dc-f584-495c-a148-016af8f7a3e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7539cef8e986db40ef94a8fd3d47073fbe489d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299800"
---
# <a name="iagentcommandexsethelpcontextid"></a><span data-ttu-id="ed700-103">IAgentCommandEx::SetHelpContextID</span><span class="sxs-lookup"><span data-stu-id="ed700-103">IAgentCommandEx::SetHelpContextID</span></span>

<span data-ttu-id="ed700-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ed700-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetHelpContextID(
   long ulID  //  ID for help topic
);
```

<span data-ttu-id="ed700-105">Imposta [**HelpContextID**](helpcontextid-property-com.md) per un oggetto [**comando**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="ed700-105">Sets the [**HelpContextID**](helpcontextid-property-com.md) for a [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

-   <span data-ttu-id="ed700-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="ed700-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="ed700-107"><span id="ulID"></span><span id="ulid"></span><span id="ULID"></span>*ulID*</span><span class="sxs-lookup"><span data-stu-id="ed700-107"><span id="ulID"></span><span id="ulid"></span><span id="ULID"></span>*ulID*</span></span>
</dt> <dd>

<span data-ttu-id="ed700-108">Il numero di contesto dell'argomento della Guida associato all'oggetto [**Command**](/windows/desktop/lwef/the-command-object) ; utilizzato per fornire la Guida sensibile al contesto per il comando.</span><span class="sxs-lookup"><span data-stu-id="ed700-108">The context number of the help topic associated with the [**Command**](/windows/desktop/lwef/the-command-object) object; used to provide context-sensitive Help for the command.</span></span>

</dd> </dl>

<span data-ttu-id="ed700-109">Se è stato creato un file della Guida di Windows per l'applicazione e questo è stato impostato [**nella proprietà**](helpfile-property.md) fileguida del carattere.</span><span class="sxs-lookup"><span data-stu-id="ed700-109">If you've created a Windows Help file for your application and set this in the character's [**HelpFile**](helpfile-property.md) property.</span></span> <span data-ttu-id="ed700-110">Microsoft Agent chiama automaticamente la guida quando [**HelpModeOn**](helpmodeon-property.md) è impostato su **true** e l'utente seleziona il comando.</span><span class="sxs-lookup"><span data-stu-id="ed700-110">Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the command.</span></span> <span data-ttu-id="ed700-111">Se è presente un numero di contesto in [**HelpContextID**](helpcontextid-property-com.md), Agent chiama la guida e cerca l'argomento identificato dal numero di contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="ed700-111">If there is a context number in the [**HelpContextID**](helpcontextid-property-com.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="ed700-112">Il numero di contesto corrente è il valore di **HelpContextID** per il comando.</span><span class="sxs-lookup"><span data-stu-id="ed700-112">The current context number is the value of **HelpContextID** for the command.</span></span>

> [!Note]  
> <span data-ttu-id="ed700-113">La compilazione di un file della guida richiede il compilatore della Guida di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ed700-113">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="ed700-114">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ed700-114">See Also</span></span>

<span data-ttu-id="ed700-115">[**IAgentCommandEx:: GetHelpContextID**](iagentcommandex--gethelpcontextid.md), [**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span><span class="sxs-lookup"><span data-stu-id="ed700-115">[**IAgentCommandEx::GetHelpContextID**](iagentcommandex--gethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 