---
title: GetItemText IAgentUserInput
description: GetItemText IAgentUserInput
ms.assetid: 69653806-c001-4015-bd05-3c261a312ede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7010172147f86282903641c46aa5137ce69c80be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104043976"
---
# <a name="iagentuserinputgetitemtext"></a><span data-ttu-id="49083-103">IAgentUserInput:: GetItemText</span><span class="sxs-lookup"><span data-stu-id="49083-103">IAgentUserInput::GetItemText</span></span>

<span data-ttu-id="49083-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="49083-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetItemText(
   Long dwItemIndex,  // index of Command alternative
   BSTR * pbszText    // address of voice text for Command 
);
```

<span data-ttu-id="49083-105">Recupera il testo vocale per un'alternativa del [**comando**](command-event.md) passata al callback [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="49083-105">Retrieves the voice text for a [**Command**](command-event.md) alternative passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

-   <span data-ttu-id="49083-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="49083-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="49083-107"><span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*</span><span class="sxs-lookup"><span data-stu-id="49083-107"><span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*</span></span>
</dt> <dd>

<span data-ttu-id="49083-108">Indice di un'alternativa del [**comando**](command-event.md) passato al callback [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="49083-108">The index of a [**Command**](command-event.md) alternative passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> <dt>

<span data-ttu-id="49083-109"><span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*</span><span class="sxs-lookup"><span data-stu-id="49083-109"><span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*</span></span>
</dt> <dd>

<span data-ttu-id="49083-110">Indirizzo di un BSTR che riceve il valore del testo vocale per il [**comando**](command-event.md).</span><span class="sxs-lookup"><span data-stu-id="49083-110">Address of a BSTR that receives the value of the voice text for the [**Command**](command-event.md).</span></span>

</dd> </dl>

<span data-ttu-id="49083-111">Se l'input vocale non è l'origine del comando, ad esempio se l'utente ha selezionato il comando dal menu di scelta rapida del carattere, il server restituisce **null** per il testo vocale del [**comando**](command-event.md).</span><span class="sxs-lookup"><span data-stu-id="49083-111">If voice input was not the source for the command, for example, if the user selected the command from the character's pop-up menu, the server returns **NULL** for the [**Command**](command-event.md)'s voice text.</span></span>

## <a name="see-also"></a><span data-ttu-id="49083-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="49083-112">See Also</span></span>

<span data-ttu-id="49083-113">[**IAgentUserInput:: GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput:: GetItemID**](iagentuserinput--getitemid.md), [**IAgentUserInput:: GetAllItemData**](iagentuserinput--getallitemdata.md)</span><span class="sxs-lookup"><span data-stu-id="49083-113">[**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput::GetItemID**](iagentuserinput--getitemid.md), [**IAgentUserInput::GetAllItemData**](iagentuserinput--getallitemdata.md)</span></span>


 

 




