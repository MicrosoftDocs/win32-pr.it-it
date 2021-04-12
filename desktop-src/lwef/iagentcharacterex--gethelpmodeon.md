---
title: IAgentCharacterEx GetHelpModeOn
description: IAgentCharacterEx GetHelpModeOn
ms.assetid: 848c9e75-6e4c-487c-b01c-36ec6314d0c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 072f657ba5ac93d057474f062f73101f2559aed0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221940"
---
# <a name="iagentcharacterexgethelpmodeon"></a><span data-ttu-id="606a0-103">IAgentCharacterEx::GetHelpModeOn</span><span class="sxs-lookup"><span data-stu-id="606a0-103">IAgentCharacterEx::GetHelpModeOn</span></span>

<span data-ttu-id="606a0-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="606a0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetHelpModeOn(
   long * pbHelpModeOn  // address of help mode setting
);
```

<span data-ttu-id="606a0-105">Recupera un valore che indica se la modalità della Guida sensibile al contesto è attiva per il carattere.</span><span class="sxs-lookup"><span data-stu-id="606a0-105">Retrieves whether context-sensitive Help mode is on for the character.</span></span>

-   <span data-ttu-id="606a0-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="606a0-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="606a0-107"><span id="pbHelpModeOn"></span><span id="pbhelpmodeon"></span><span id="PBHELPMODEON"></span>*pbHelpModeOn*</span><span class="sxs-lookup"><span data-stu-id="606a0-107"><span id="pbHelpModeOn"></span><span id="pbhelpmodeon"></span><span id="PBHELPMODEON"></span>*pbHelpModeOn*</span></span>
</dt> <dd>

<span data-ttu-id="606a0-108">Indirizzo di una variabile che riceve **true** se la modalità della guida è impostata su on per il carattere e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="606a0-108">Address of a variable that receives **True** if Help mode is on for the character and **False** if not.</span></span>

</dd> </dl>

<span data-ttu-id="606a0-109">Quando questa proprietà è impostata su **true**, il puntatore del mouse assume la forma dell'immagine della Guida sensibile al contesto quando viene spostato sul carattere o sul menu di scelta rapida per il carattere.</span><span class="sxs-lookup"><span data-stu-id="606a0-109">When this property is set to **True**, the mouse pointer changes to the context-sensitive Help image when moved over the character or over the pop-up menu for the character.</span></span> <span data-ttu-id="606a0-110">Quando l'utente fa clic o trascina il carattere o fa clic su un elemento nel menu popup del carattere, il server attiva l'evento [**IAgentNotifySinkEx:: HelpComplete**](https://www.bing.com/search?q=**IAgentNotifySinkEx::HelpComplete**) e chiude la modalità della guida.</span><span class="sxs-lookup"><span data-stu-id="606a0-110">When the user clicks or drags the character or clicks an item in the character's pop-up menu, the server triggers the [**IAgentNotifySinkEx::HelpComplete**](https://www.bing.com/search?q=**IAgentNotifySinkEx::HelpComplete**) event and exits Help mode.</span></span>

<span data-ttu-id="606a0-111">In modalità guida, il server non invia gli eventi [**IAgentNotifySink:: click**](iagentnotifysink--click.md), [**IAgentNotifySink::D ragstart**](iagentnotifysink--dragstart.md), [**IAgentNotifySink::D Ragcomplete**](iagentnotifysink--dragcomplete.md)e [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) , a meno che la proprietà [**GetAutoPopupMenu**](https://www.bing.com/search?q=**GetAutoPopupMenu**) non restituisca **true**.</span><span class="sxs-lookup"><span data-stu-id="606a0-111">In Help mode, the server does not send the [**IAgentNotifySink::Click**](iagentnotifysink--click.md), [**IAgentNotifySink::DragStart**](iagentnotifysink--dragstart.md), [**IAgentNotifySink::DragComplete**](iagentnotifysink--dragcomplete.md), and [**IAgentNotifySink::Command**](iagentnotifysink--command.md) events, unless [**GetAutoPopupMenu**](https://www.bing.com/search?q=**GetAutoPopupMenu**) property returns **True**.</span></span> <span data-ttu-id="606a0-112">In tal caso, il server invierà l'evento **IAgentNotifySink:: click** (non esce dalla modalità guida), ma solo per il pulsante destro del mouse per consentire la visualizzazione del menu a comparsa.</span><span class="sxs-lookup"><span data-stu-id="606a0-112">In that case, the server will send the **IAgentNotifySink::Click** event (does not exit Help mode), but only for the right mouse button to enable you to display the pop-up menu.</span></span>

<span data-ttu-id="606a0-113">Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="606a0-113">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="606a0-114">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="606a0-114">See Also</span></span>

[<span data-ttu-id="606a0-115">**IAgentCharacterEx::SetHelpModeOn**</span><span class="sxs-lookup"><span data-stu-id="606a0-115">**IAgentCharacterEx::SetHelpModeOn**</span></span>](iagentcharacterex--sethelpmodeon.md)


 

 




