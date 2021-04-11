---
title: IAgentCharacterEx SetHelpFileName
description: IAgentCharacterEx SetHelpFileName
ms.assetid: 1f8d2bd7-5821-46c0-b371-7ecbc526df72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1342baecc1e059d4fcb5d1323c0c714bd6bf7087
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116828"
---
# <a name="iagentcharacterexsethelpfilename"></a><span data-ttu-id="cea60-103">IAgentCharacterEx::SetHelpFileName</span><span class="sxs-lookup"><span data-stu-id="cea60-103">IAgentCharacterEx::SetHelpFileName</span></span>

<span data-ttu-id="cea60-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cea60-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetHelpFileName(
   BSTR bszName  // Help filename
);
```

<span data-ttu-id="cea60-105">Imposta HelpFileName per un carattere.</span><span class="sxs-lookup"><span data-stu-id="cea60-105">Sets the HelpFileName for a character.</span></span>

-   <span data-ttu-id="cea60-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="cea60-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="cea60-107"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span><span class="sxs-lookup"><span data-stu-id="cea60-107"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span></span>
</dt> <dd>

<span data-ttu-id="cea60-108">Nome file della Guida per il carattere.</span><span class="sxs-lookup"><span data-stu-id="cea60-108">The Help filename for the character.</span></span>

</dd> </dl>

<span data-ttu-id="cea60-109">Se è stato creato un file della Guida di Windows per l'applicazione e si è impostata [**la proprietà filecommand del carattere**](helpfile-property.md) , l'agente Microsoft chiama automaticamente la guida quando [**HelpModeOn**](helpmodeon-property.md) è impostato su **true** e l'utente fa clic sul carattere oppure seleziona un comando dal menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="cea60-109">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user clicks the character or selects a command from its pop-up menu.</span></span> <span data-ttu-id="cea60-110">Se è presente un numero di contesto nella proprietà [**HelpContextID**](helpcontextid-property.md) del comando selezionato, nella Guida viene visualizzato un argomento corrispondente al contesto della Guida corrente. in caso contrario, viene visualizzato "nessun argomento della Guida associato a questo elemento".</span><span class="sxs-lookup"><span data-stu-id="cea60-110">If there is a context number in the [**HelpContextID**](helpcontextid-property.md) property of the selected command, Help displays a topic corresponding to the current Help context; otherwise it displays "No Help topic associated with this item."</span></span>

<span data-ttu-id="cea60-111">Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="cea60-111">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="cea60-112">La compilazione di un file della guida richiede il compilatore della Guida di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="cea60-112">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="cea60-113">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="cea60-113">See Also</span></span>

<span data-ttu-id="cea60-114">[**IAgentCommandsEx:: SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: GetHelpFileName**](iagentcharacterex--gethelpfilename.md)</span><span class="sxs-lookup"><span data-stu-id="cea60-114">[**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::GetHelpFileName**](iagentcharacterex--gethelpfilename.md)</span></span>


 

 




