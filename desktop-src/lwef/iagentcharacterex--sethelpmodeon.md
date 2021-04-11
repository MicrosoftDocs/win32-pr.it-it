---
title: IAgentCharacterEx SetHelpModeOn
description: IAgentCharacterEx SetHelpModeOn
ms.assetid: d4d42122-3d27-40c4-8770-0de105e5d933
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674fc8dcca3bca2f44c0928474d8684e77fc6e9b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117607"
---
# <a name="iagentcharacterexsethelpmodeon"></a><span data-ttu-id="23814-103">IAgentCharacterEx::SetHelpModeOn</span><span class="sxs-lookup"><span data-stu-id="23814-103">IAgentCharacterEx::SetHelpModeOn</span></span>

<span data-ttu-id="23814-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="23814-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetHelpModeOn(
   long bHelpModeOn  // help mode setting
);
```

<span data-ttu-id="23814-105">Imposta la modalità della Guida sensibile al contesto per il carattere.</span><span class="sxs-lookup"><span data-stu-id="23814-105">Sets context-sensitive Help mode on for the character.</span></span>

-   <span data-ttu-id="23814-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="23814-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="23814-107"><span id="bHelpModeOn"></span><span id="bhelpmodeon"></span><span id="BHELPMODEON"></span>*bHelpModeOn*</span><span class="sxs-lookup"><span data-stu-id="23814-107"><span id="bHelpModeOn"></span><span id="bhelpmodeon"></span><span id="BHELPMODEON"></span>*bHelpModeOn*</span></span>
</dt> <dd>

<span data-ttu-id="23814-108">Flag della modalità della guida.</span><span class="sxs-lookup"><span data-stu-id="23814-108">Help mode flag.</span></span> <span data-ttu-id="23814-109">Se questo parametro è **true**, Microsoft Agent attiva la modalità della Guida per il carattere.</span><span class="sxs-lookup"><span data-stu-id="23814-109">If this parameter is **True**, Microsoft Agent turns on Help mode for the character.</span></span>

</dd> </dl>

<span data-ttu-id="23814-110">Quando si imposta questa proprietà su **true**, il puntatore del mouse assume la forma dell'immagine della Guida sensibile al contesto quando viene spostato sul carattere o sul menu di scelta rapida per il carattere.</span><span class="sxs-lookup"><span data-stu-id="23814-110">When you set this property to **True**, the mouse pointer changes to the context-sensitive Help image when moved over the character or over the pop-up menu for the character.</span></span> <span data-ttu-id="23814-111">Quando l'utente fa clic o trascina il carattere o fa clic su un elemento nel menu popup del carattere, il server attiva l'evento [**IAgentNotifySinkEx:: HelpComplete**](iagentnotifysinkex--helpcomplete.md) e chiude la modalità della guida.</span><span class="sxs-lookup"><span data-stu-id="23814-111">When the user clicks or drags the character or clicks an item in the character's pop-up menu, the server triggers the [**IAgentNotifySinkEx::HelpComplete**](iagentnotifysinkex--helpcomplete.md) event and exits Help mode.</span></span>

<span data-ttu-id="23814-112">In modalità guida, il server non invia gli eventi [**Click**](click-event.md), [**DragStart**](/windows/desktop/lwef/dragstart-event), [**DragComplete**](https://www.bing.com/search?q=**DragComplete**)e [**Command**](command-event.md) , a meno che la proprietà [**GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md) non restituisca **true**.</span><span class="sxs-lookup"><span data-stu-id="23814-112">In Help mode, the server does not send the [**Click**](click-event.md), [**DragStart**](/windows/desktop/lwef/dragstart-event), [**DragComplete**](https://www.bing.com/search?q=**DragComplete**), and [**Command**](command-event.md) events, unless the [**GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md) property returns **True**.</span></span> <span data-ttu-id="23814-113">In tal caso, il server invierà l'evento **Click** (non esce dalla modalità guida), ma solo per il pulsante destro del mouse, in modo da poter visualizzare il menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="23814-113">In that case, the server will send the **Click** event (does not exit Help mode), but only for the right mouse button so you can display the pop-up menu.</span></span>

<span data-ttu-id="23814-114">Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="23814-114">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="23814-115">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="23814-115">See Also</span></span>

<span data-ttu-id="23814-116">[**IAgentCharacterEx:: GetHelpModeOn**](iagentcharacterex--gethelpmodeon.md), [ **IAgentNotifySinkEx:: HelpComplete**](iagentnotifysinkex--helpcomplete.md)</span><span class="sxs-lookup"><span data-stu-id="23814-116">[**IAgentCharacterEx::GetHelpModeOn**](iagentcharacterex--gethelpmodeon.md), [**IAgentNotifySinkEx::HelpComplete**](iagentnotifysinkex--helpcomplete.md)</span></span>


 

 