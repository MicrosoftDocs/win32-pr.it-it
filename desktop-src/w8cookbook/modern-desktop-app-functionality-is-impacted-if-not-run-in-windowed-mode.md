---
title: La funzionalità dell'app desktop è interessata se non viene eseguita in modalità finestra
description: In Windows 10, le app di Windows non sono più a schermo intero per impostazione predefinita, ma sono a finestra e le operazioni come la riduzione, il ripristino, l'ottimizzazione, il ridimensionamento e qualsiasi altra operazione che è sempre stato possibile eseguire in qualsiasi altra finestra dell'applicazione Windows classica sono ora possibili.
ms.assetid: 435E85DA-008B-437E-92CB-AC105855760A
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aae44fda5847e5b86616b40ab1bf4ab8cbd206b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396547"
---
# <a name="desktop-app-functionality-is-impacted-if-not-run-in-windowed-mode"></a><span data-ttu-id="6dfc0-103">La funzionalità dell'app desktop è interessata se non viene eseguita in modalità finestra</span><span class="sxs-lookup"><span data-stu-id="6dfc0-103">Desktop App functionality is impacted if not run in Windowed Mode</span></span>

<span data-ttu-id="6dfc0-104">In Windows 10, le app di Windows non sono più a schermo intero per impostazione predefinita, ma sono a finestra e le operazioni come la riduzione, il ripristino, l'ottimizzazione, il ridimensionamento e qualsiasi altra operazione che è sempre stato possibile eseguire in qualsiasi altra finestra dell'applicazione Windows classica sono ora possibili.</span><span class="sxs-lookup"><span data-stu-id="6dfc0-104">In Windows 10, Windows apps are no longer full-screen by default – instead, they are windowed and operations like minimizing, restoring, maximizing, resizing (and any other operation that you’ve always been able to do to any other Classic Windows application window) is now possible.</span></span>

## <a name="manifestations"></a><span data-ttu-id="6dfc0-105">Manifestazioni</span><span class="sxs-lookup"><span data-stu-id="6dfc0-105">Manifestations</span></span>

<span data-ttu-id="6dfc0-106">La modifica più evidente ora è che è possibile ottenere dimensioni arbitrarie che non sono solo le dimensioni della schermata o dell'altezza dello schermo.</span><span class="sxs-lookup"><span data-stu-id="6dfc0-106">The most noticeable change now is that you can get sized to arbitrary sizes that are not just the size of the screen/height of the screen.</span></span> <span data-ttu-id="6dfc0-107">Un utente può ridimensionare continuamente la finestra dell'app a piacimento (fino alla dimensione minima della finestra dell'app).</span><span class="sxs-lookup"><span data-stu-id="6dfc0-107">A user can continuously resize the app window to their liking (down to the app’s minimal window size).</span></span> <span data-ttu-id="6dfc0-108">Questo comportamento è diverso da Windows 8,0 o Windows 8.1, in cui l'azione di ridimensionamento di una finestra era un'azione discreta (gli utenti ridimensionavano un'anteprima della finestra, causando il ridimensionamento della finestra dopo che l'utente ha eseguito il commit dell'azione).</span><span class="sxs-lookup"><span data-stu-id="6dfc0-108">This is different from Windows 8.0 or Windows 8.1, where the act of resizing a window was a discrete action (users resized a thumbnail of the window, which then caused the window to resize once the user committed the action).</span></span> <span data-ttu-id="6dfc0-109">Attualmente, invece, quando l'utente trascina la finestra dall'angolo inferiore (o da un'altra posizione del bordo), si tratta di un ridimensionamento continuo e l'app riceve i messaggi di ridimensionamento in una riga, anziché la modifica delle dimensioni.</span><span class="sxs-lookup"><span data-stu-id="6dfc0-109">Today instead when the user drags the window by the bottom corner (or other border location) it is a continuous resize, and the app receives resize messages in a row, rather than size change.</span></span>

## <a name="mitigations"></a><span data-ttu-id="6dfc0-110">Soluzioni di prevenzione</span><span class="sxs-lookup"><span data-stu-id="6dfc0-110">Mitigations</span></span>

<span data-ttu-id="6dfc0-111">Per attenuare questo problema per le app di Windows 8,0 e 8,1:</span><span class="sxs-lookup"><span data-stu-id="6dfc0-111">To mitigate this for Windows 8.0 and 8.1 apps:</span></span>

-   <span data-ttu-id="6dfc0-112">Se la funzionalità prevista all'interno della funzionalità dell'app è interruppe, la mitigazione dell'utente consiste nell'inserire l'app in modalità schermo intero (usando il pulsante "Vai a schermo intero" nell'angolo superiore destro della barra del titolo).</span><span class="sxs-lookup"><span data-stu-id="6dfc0-112">If the expected feature within the app functionality is broken, then the user mitigation is to place the app into full screen mode (by using the “go full screen button” in the upper right corner of the title bar).</span></span>
-   <span data-ttu-id="6dfc0-113">Se l'avvio dell'app è influenzato dal fatto che non si apre come previsto, l'utente deve comunque essere in grado di passare alla modalità tablet per forzare l'avvio dell'app in modalità schermo intero senza l'intervento dell'utente.</span><span class="sxs-lookup"><span data-stu-id="6dfc0-113">If app start-up is impacted that it does not open as expected, then the user should still be able to switch to Tablet Mode to force the app to start in full-screen mode without user intervention.</span></span>

<span data-ttu-id="6dfc0-114">Il modo migliore per gestire questa situazione consiste nel modificare l'app in modo che sia consapevole del fatto che può essere ridimensionata in posizioni/altezze di dimensioni non monitorate (ovvero non avere una tabella hardcoded di altezza/larghezza e prevedere solo i rapporti hardcoded).</span><span class="sxs-lookup"><span data-stu-id="6dfc0-114">The best way to handle this is to change the app to be aware of the fact that it can be sized to non-monitor sized places/heights (i.e. don’t have a hardcoded table of height/widths and only expect those, or expect hardcoded ratios as well).</span></span> <span data-ttu-id="6dfc0-115">Gli sviluppatori di app dovrebbero prevedere che, durante il ridimensionamento dell'app, un altro messaggio di ridimensionamento possa essere eseguito subito dopo il recapito del messaggio di ridimensionamento. di conseguenza, se l'app avvia animazioni durante il ridimensionamento, è possibile che l'app riceva un altro messaggio di ridimensionamento subito dopo, quindi è importante assicurarsi che questo tipo di situazione non provochi l'arresto anomalo dell'</span><span class="sxs-lookup"><span data-stu-id="6dfc0-115">App developers should expect that as the app is being resized, that another resizing message can happen right after the current resize message gets delivered – as a result, if the app starts animations during resize, it’s possible that the app may receive another resize message right after (so it’s important to ensure that this type of situation doesn’t lead to the app crashing).</span></span>

 

 




