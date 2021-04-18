---
title: IAgentUserInput GetItemID
description: IAgentUserInput GetItemID
ms.assetid: 3afd4d9d-51bb-4086-bf7b-7c9a2ddcd807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716ae1386d87fa6051111801c5603837519eeb4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297597"
---
# <a name="iagentuserinputgetitemid"></a><span data-ttu-id="d2a19-103">IAgentUserInput:: GetItemID</span><span class="sxs-lookup"><span data-stu-id="d2a19-103">IAgentUserInput::GetItemID</span></span>

<span data-ttu-id="d2a19-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d2a19-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetItemID(
   long dwItemIndex,    // index of Command alternative
   long * pdwCommandID  // address of a variable for number of alternatives 
);
```

<span data-ttu-id="d2a19-105">Recupera l'identificatore di un'alternativa del [**comando**](command-event.md) passata a un callback [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="d2a19-105">Retrieves the identifier of a [**Command**](command-event.md) alternative passed to an [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

-   <span data-ttu-id="d2a19-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="d2a19-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="d2a19-107"><span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*</span><span class="sxs-lookup"><span data-stu-id="d2a19-107"><span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*</span></span>
</dt> <dd>

<span data-ttu-id="d2a19-108">Indice dell'alternativa del [**comando**](command-event.md) passato al callback [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="d2a19-108">The index of the [**Command**](command-event.md) alternative passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> <dt>

<span data-ttu-id="d2a19-109"><span id="pdwCommandID"></span><span id="pdwcommandid"></span><span id="PDWCOMMANDID"></span>*pdwCommandID*</span><span class="sxs-lookup"><span data-stu-id="d2a19-109"><span id="pdwCommandID"></span><span id="pdwcommandid"></span><span id="PDWCOMMANDID"></span>*pdwCommandID*</span></span>
</dt> <dd>

<span data-ttu-id="d2a19-110">Indirizzo di una variabile che riceve l'ID di un [**comando**](command-event.md).</span><span class="sxs-lookup"><span data-stu-id="d2a19-110">Address of a variable that receives the ID of a [**Command**](command-event.md).</span></span>

</dd> </dl>

<span data-ttu-id="d2a19-111">Se l'input vocale attiva il callback [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) , il server restituisce gli ID per tutti i [**comandi**](command-event.md) corrispondenti definiti dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d2a19-111">If voice input triggers the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback, the server returns the IDs for any matching [**Commands**](command-event.md) defined by your application.</span></span>

## <a name="see-also"></a><span data-ttu-id="d2a19-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="d2a19-112">See Also</span></span>

<span data-ttu-id="d2a19-113">[**IAgentUserInput:: GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput:: GetItemText**](iagentuserinput--getitemtext.md), [**IAgentUserInput:: GetAllItemData**](iagentuserinput--getallitemdata.md)</span><span class="sxs-lookup"><span data-stu-id="d2a19-113">[**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput::GetItemText**](iagentuserinput--getitemtext.md), [**IAgentUserInput::GetAllItemData**](iagentuserinput--getallitemdata.md)</span></span>


 

 




