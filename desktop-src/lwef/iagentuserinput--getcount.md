---
title: IAgentUserInput GetCount
description: IAgentUserInput GetCount
ms.assetid: 9c127387-b680-405a-9a62-ee08cc70813a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac4b597f7367eff10154bde256698ef371c3619
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220857"
---
# <a name="iagentuserinputgetcount"></a><span data-ttu-id="e41a4-103">IAgentUserInput:: GetCount</span><span class="sxs-lookup"><span data-stu-id="e41a4-103">IAgentUserInput::GetCount</span></span>

<span data-ttu-id="e41a4-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e41a4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetCount(
   long * pdwCount  // address of a variable for number of alternatives 
);
```

<span data-ttu-id="e41a4-105">Recupera il numero di alternative del [**comando**](command-event.md) passate a un callback [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="e41a4-105">Retrieves the number of [**Command**](command-event.md) alternatives passed to an [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

-   <span data-ttu-id="e41a4-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="e41a4-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e41a4-107"><span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*</span><span class="sxs-lookup"><span data-stu-id="e41a4-107"><span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*</span></span>
</dt> <dd>

<span data-ttu-id="e41a4-108">Indirizzo di una variabile che riceve il numero di [**comandi**](command-event.md) alternativi identificati dal server.</span><span class="sxs-lookup"><span data-stu-id="e41a4-108">Address of a variable that receives the count of [**Commands**](command-event.md) alternatives identified by the server.</span></span>

</dd> </dl>

<span data-ttu-id="e41a4-109">Se l'input vocale non è l'origine del comando, ad esempio se l'utente ha selezionato il comando dal menu di scelta rapida del carattere, **GetCount** restituisce 1.</span><span class="sxs-lookup"><span data-stu-id="e41a4-109">If voice input was not the source for the command, for example, if the user selected the command from the character's pop-up menu, **GetCount** returns 1.</span></span> <span data-ttu-id="e41a4-110">Se **GetCount** restituisce zero (0), il motore di riconoscimento vocale ha rilevato l'input parlato ma ha determinato che non esiste alcun comando corrispondente.</span><span class="sxs-lookup"><span data-stu-id="e41a4-110">If **GetCount** returns zero (0), the speech recognition engine detected spoken input but determined that there was no matching command.</span></span>

 

 




