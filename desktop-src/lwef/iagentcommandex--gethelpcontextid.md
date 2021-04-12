---
title: IAgentCommandEx GetHelpContextID
description: IAgentCommandEx GetHelpContextID
ms.assetid: 97b390f3-ab24-4c09-aa87-d76076eba995
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f330e8ae8cd8bdaff5e27ccd00352b41b07be2b6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104399002"
---
# <a name="iagentcommandexgethelpcontextid"></a><span data-ttu-id="cd312-103">IAgentCommandEx::GetHelpContextID</span><span class="sxs-lookup"><span data-stu-id="cd312-103">IAgentCommandEx::GetHelpContextID</span></span>

<span data-ttu-id="cd312-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cd312-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetHelpContextID(
   long * pulID  //  address of command's help topic ID
);
```

<span data-ttu-id="cd312-105">Recupera [**HelpContextID**](helpcontextid-property-com.md) per un oggetto [**comando**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="cd312-105">Retrieves the [**HelpContextID**](helpcontextid-property-com.md) for a [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

-   <span data-ttu-id="cd312-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="cd312-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="cd312-107"><span id="pulID"></span><span id="pulid"></span><span id="PULID"></span>*pulID*</span><span class="sxs-lookup"><span data-stu-id="cd312-107"><span id="pulID"></span><span id="pulid"></span><span id="PULID"></span>*pulID*</span></span>
</dt> <dd>

<span data-ttu-id="cd312-108">Indirizzo di una variabile che riceve il numero di contesto dell'argomento della Guida associato all'oggetto [**Command**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="cd312-108">Address of a variable that receives the context number of the help topic associated with the [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

</dd> </dl>

<span data-ttu-id="cd312-109">Se è stato creato un file della Guida di Windows per l'applicazione e si imposta [**la proprietà**](helpfile-property.md) filecommand del carattere su questo file, l'agente Microsoft chiama automaticamente la guida quando [**HelpModeOn**](helpmodeon-property.md) è impostato su **true** e l'utente seleziona il comando.</span><span class="sxs-lookup"><span data-stu-id="cd312-109">If you've created a Windows Help file for your application and set your character's [**HelpFile**](helpfile-property.md) property to this file, Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the command.</span></span> <span data-ttu-id="cd312-110">Se è presente un numero di contesto in [**HelpContextID**](helpcontextid-property-com.md), Agent chiama la guida e cerca l'argomento identificato dal numero di contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="cd312-110">If there is a context number in the [**HelpContextID**](helpcontextid-property-com.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="cd312-111">Il numero di contesto corrente è il valore di **HelpContextID** per il comando.</span><span class="sxs-lookup"><span data-stu-id="cd312-111">The current context number is the value of **HelpContextID** for the command.</span></span>

> [!Note]  
> <span data-ttu-id="cd312-112">La compilazione di un file della guida richiede il compilatore della Guida di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="cd312-112">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="cd312-113">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="cd312-113">See Also</span></span>

<span data-ttu-id="cd312-114">[**IAgentCommandEx:: SetHelpContextID**](iagentcommandex--sethelpcontextid.md), [**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span><span class="sxs-lookup"><span data-stu-id="cd312-114">[**IAgentCommandEx::SetHelpContextID**](iagentcommandex--sethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 