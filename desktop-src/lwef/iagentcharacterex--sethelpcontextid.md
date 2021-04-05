---
title: IAgentCharacterEx SetHelpContextID
description: IAgentCharacterEx SetHelpContextID
ms.assetid: 218e970e-825e-441d-8947-30ec6a2845bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 500187bf04babbecf7577ff933dd0adcc53609f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708962"
---
# <a name="iagentcharacterexsethelpcontextid"></a><span data-ttu-id="ed544-103">IAgentCharacterEx::SetHelpContextID</span><span class="sxs-lookup"><span data-stu-id="ed544-103">IAgentCharacterEx::SetHelpContextID</span></span>

<span data-ttu-id="ed544-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ed544-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetHelpContextID(
   long ulHelpID  // ID for help topic
);
```

<span data-ttu-id="ed544-105">Imposta [**HelpContextID**](helpcontextid-property.md) per il carattere.</span><span class="sxs-lookup"><span data-stu-id="ed544-105">Sets the [**HelpContextID**](helpcontextid-property.md) for the character.</span></span>

-   <span data-ttu-id="ed544-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="ed544-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="ed544-107"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*</span><span class="sxs-lookup"><span data-stu-id="ed544-107"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*</span></span>
</dt> <dd>

<span data-ttu-id="ed544-108">Il numero di contesto dell'argomento della Guida per associato a un carattere; utilizzato per fornire la Guida sensibile al contesto per il carattere.</span><span class="sxs-lookup"><span data-stu-id="ed544-108">The context number of the help topic for associated with a character; used to provide context-sensitive Help for the character.</span></span>

</dd> </dl>

<span data-ttu-id="ed544-109">Se è stato creato un file della Guida di Windows per l'applicazione e questo è stato impostato [**nella proprietà**](helpfile-property.md) fileguida del carattere, l'agente Microsoft chiama automaticamente la guida quando [**HelpModeOn**](helpmodeon-property.md) è impostato su **true** e l'utente seleziona il carattere.</span><span class="sxs-lookup"><span data-stu-id="ed544-109">If you've created a Windows Help file for your application and set this in the character's [**HelpFile**](helpfile-property.md) property, Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the character.</span></span> <span data-ttu-id="ed544-110">Se è presente un numero di contesto in [**HelpContextID**](helpcontextid-property.md), Agent chiama la guida e cerca l'argomento identificato dal numero di contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="ed544-110">If there is a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="ed544-111">Il numero di contesto corrente è il valore di **HelpContextID** per il carattere.</span><span class="sxs-lookup"><span data-stu-id="ed544-111">The current context number is the value of **HelpContextID** for the character.</span></span> <span data-ttu-id="ed544-112">Se è presente un numero di contesto nella proprietà **HelpContextID** , help Visualizza un argomento corrispondente al contesto della Guida corrente. in caso contrario, viene visualizzato "nessun argomento della Guida associato a questo elemento".</span><span class="sxs-lookup"><span data-stu-id="ed544-112">If there is a context number in the **HelpContextID** property, Help displays a topic corresponding to the current Help context; otherwise it displays "No Help topic associated with this item."</span></span>

<span data-ttu-id="ed544-113">Questa impostazione si applica solo se l'applicazione client è il client attivo del carattere di primo livello.</span><span class="sxs-lookup"><span data-stu-id="ed544-113">This setting applies only when your client application is the active client of the topmost character.</span></span> <span data-ttu-id="ed544-114">Non influisce su altri client del carattere o di altri caratteri utilizzati dall'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="ed544-114">It does not affect other clients of the character or other characters that your client application is using.</span></span>

> [!Note]  
> <span data-ttu-id="ed544-115">La compilazione di un file della guida richiede il compilatore della Guida di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ed544-115">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="ed544-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ed544-116">See Also</span></span>

<span data-ttu-id="ed544-117">[**IAgentCharacterEx:: GetHelpContextID**](iagentcharacterex--gethelpcontextid.md), [**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span><span class="sxs-lookup"><span data-stu-id="ed544-117">[**IAgentCharacterEx::GetHelpContextID**](iagentcharacterex--gethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 




