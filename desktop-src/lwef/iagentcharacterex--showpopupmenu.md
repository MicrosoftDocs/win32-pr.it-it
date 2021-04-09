---
title: ShowPopupMenu IAgentCharacterEx
description: ShowPopupMenu IAgentCharacterEx
ms.assetid: f93c4c9e-5ef8-42d1-8f22-d6625af7978f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 535a86496f3553e0927ebe67d2c9823b738fb901
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856478"
---
# <a name="iagentcharacterexshowpopupmenu"></a><span data-ttu-id="08557-103">IAgentCharacterEx:: ShowPopupMenu</span><span class="sxs-lookup"><span data-stu-id="08557-103">IAgentCharacterEx::ShowPopupMenu</span></span>

<span data-ttu-id="08557-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="08557-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT ShowPopupMenu(
   short x,  // x-coordinate of pop-up menu
   short y   // y-coordinate of pop-up menu
);
```

<span data-ttu-id="08557-105">Consente di visualizzare il menu di scelta rapida per il carattere.</span><span class="sxs-lookup"><span data-stu-id="08557-105">Displays the pop-up menu for the character.</span></span>

-   <span data-ttu-id="08557-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="08557-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="08557-107"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="08557-107"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="08557-108">Coordinata x del menu di scelta rapida del carattere in pixel rispetto all'origine dello schermo (in alto a sinistra).</span><span class="sxs-lookup"><span data-stu-id="08557-108">The x-coordinate of the character's pop-up menu in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="08557-109"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="08557-109"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="08557-110">Coordinata y del menu di scelta rapida del carattere in pixel rispetto all'origine dello schermo (in alto a sinistra).</span><span class="sxs-lookup"><span data-stu-id="08557-110">The y-coordinate of the character's pop-up menu in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="08557-111">Quando si imposta [**IAgentCharacterEx:: SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md) su **false**, il server non Visualizza più automaticamente il menu quando si fa clic con il pulsante destro del mouse sull'icona del carattere o della barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="08557-111">When you set [**IAgentCharacterEx::SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md) to **False**, the server no longer automatically displays the menu when the character or its taskbar icon is right-clicked.</span></span> <span data-ttu-id="08557-112">È possibile utilizzare questo metodo per visualizzare il menu.</span><span class="sxs-lookup"><span data-stu-id="08557-112">You can use this method to display the menu.</span></span>

<span data-ttu-id="08557-113">Il menu viene visualizzato fino a quando l'utente non seleziona un comando o Visualizza un altro menu.</span><span class="sxs-lookup"><span data-stu-id="08557-113">The menu displays until the user selects a command or displays another menu.</span></span> <span data-ttu-id="08557-114">È possibile visualizzare un solo menu popup alla volta; Pertanto, le chiamate a questo metodo cancelleranno (rimuovere) il menu precedente.</span><span class="sxs-lookup"><span data-stu-id="08557-114">Only one pop-up menu can be displayed at a time; therefore, calls to this method will cancel (remove) the former menu.</span></span>

<span data-ttu-id="08557-115">Questo metodo deve essere chiamato solo quando l'applicazione client è il client attivo del carattere; in caso contrario, avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="08557-115">This method should only be called when your client application is the active client of the character; otherwise it fails.</span></span>

[<span data-ttu-id="08557-116">**IAgentCharacterEx::SetAutoPopupMenu**</span><span class="sxs-lookup"><span data-stu-id="08557-116">**IAgentCharacterEx::SetAutoPopupMenu**</span></span>](iagentcharacterex--setautopopupmenu.md)

 

 




