---
title: IAgentCharacterEx SetAutoPopupMenu
description: IAgentCharacterEx SetAutoPopupMenu
ms.assetid: f2402b1f-a39b-4fd5-a046-c0a3245d2af9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcfd1bd7ea0b02f226ed6f0365b466577807a193
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955528"
---
# <a name="iagentcharacterexsetautopopupmenu"></a><span data-ttu-id="80956-103">IAgentCharacterEx::SetAutoPopupMenu</span><span class="sxs-lookup"><span data-stu-id="80956-103">IAgentCharacterEx::SetAutoPopupMenu</span></span>

<span data-ttu-id="80956-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="80956-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetAutoPopupMenu(
   long bAutoPopupMenu,  // auto pop-up menu display setting
);
```

<span data-ttu-id="80956-105">Imposta un valore che indica se il server Visualizza automaticamente il menu di scelta rapida del carattere.</span><span class="sxs-lookup"><span data-stu-id="80956-105">Sets whether the server automatically displays the character's pop-up menu.</span></span>

-   <span data-ttu-id="80956-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="80956-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="80956-107"><span id="bAutoPopupMenu"></span><span id="bautopopupmenu"></span><span id="BAUTOPOPUPMENU"></span>*bAutoPopupMenu*</span><span class="sxs-lookup"><span data-stu-id="80956-107"><span id="bAutoPopupMenu"></span><span id="bautopopupmenu"></span><span id="BAUTOPOPUPMENU"></span>*bAutoPopupMenu*</span></span>
</dt> <dd>

<span data-ttu-id="80956-108">Flag di visualizzazione del menu a comparsa automatico.</span><span class="sxs-lookup"><span data-stu-id="80956-108">The automatic pop-up menu display flag.</span></span> <span data-ttu-id="80956-109">Se questo parametro è **true**, Microsoft Agent visualizzerà automaticamente il menu popup del carattere quando l'utente fa clic con il pulsante destro del mouse sull'icona della barra delle applicazioni del carattere o del carattere.</span><span class="sxs-lookup"><span data-stu-id="80956-109">If this parameter is **True**, Microsoft Agent automatically displays the character's pop-up menu when the user right-clicks the character or character's taskbar icon.</span></span>

</dd> </dl>

<span data-ttu-id="80956-110">Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="80956-110">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="80956-111">Impostando questa proprietà su **false**, è possibile creare un comportamento personalizzato per la gestione dei menu.</span><span class="sxs-lookup"><span data-stu-id="80956-111">By setting this property to **False**, you can create your own menu-handling behavior.</span></span> <span data-ttu-id="80956-112">Per visualizzare il menu dopo l'impostazione di questa proprietà su **false**, usare il metodo [**IAgentCharacterEx:: ShowPopupMenu**](iagentcharacterex--showpopupmenu.md) .</span><span class="sxs-lookup"><span data-stu-id="80956-112">To display the menu after setting this property to **False**, use the [**IAgentCharacterEx::ShowPopupMenu**](iagentcharacterex--showpopupmenu.md) method.</span></span>

## <a name="see-also"></a><span data-ttu-id="80956-113">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="80956-113">See Also</span></span>

<span data-ttu-id="80956-114">[**IAgentCharacterEx:: GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md), [ **IAgentCharacterEx:: ShowPopupMenu**](iagentcharacterex--showpopupmenu.md)</span><span class="sxs-lookup"><span data-stu-id="80956-114">[**IAgentCharacterEx::GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md), [**IAgentCharacterEx::ShowPopupMenu**](iagentcharacterex--showpopupmenu.md)</span></span>


 

 




