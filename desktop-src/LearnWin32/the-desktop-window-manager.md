---
title: Oggetto Gestione finestre desktop
description: La Gestione finestre desktop
ms.assetid: 79250d49-dad5-46c6-892d-b92dac14b417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fca8550134ba0c1cdafe0bd5c349061ef900a9e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103899"
---
# <a name="the-desktop-window-manager"></a><span data-ttu-id="11d8f-103">La Gestione finestre desktop</span><span class="sxs-lookup"><span data-stu-id="11d8f-103">The Desktop Window Manager</span></span>

<span data-ttu-id="11d8f-104">Prima di Windows Vista, un programma Windows disegnava direttamente sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="11d8f-104">Before Windows Vista, a Windows program would draw directly to the screen.</span></span> <span data-ttu-id="11d8f-105">In altre parole, il programma scriverà direttamente nel buffer di memoria mostrato dalla scheda video.</span><span class="sxs-lookup"><span data-stu-id="11d8f-105">In other words, the program would write directly to the memory buffer shown by the video card.</span></span> <span data-ttu-id="11d8f-106">Questo approccio può causare artefatti visivi se una finestra non si ridisegna correttamente.</span><span class="sxs-lookup"><span data-stu-id="11d8f-106">This approach can cause visual artifacts if a window does not repaint itself correctly.</span></span> <span data-ttu-id="11d8f-107">Ad esempio, se l'utente trascina una finestra su un'altra finestra e la finestra sottostante non si ridisegna abbastanza rapidamente, la finestra in alto può lasciare una traccia:</span><span class="sxs-lookup"><span data-stu-id="11d8f-107">For example, if the user drags one window over another window, and the window underneath does not repaint itself quickly enough, the top-most window can leave a trail:</span></span>

![screenshot che mostra gli artefatti ridisegnati.](images/graphics04.png)

<span data-ttu-id="11d8f-109">La traccia è causata dal fatto che entrambe le finestre disegnano nella stessa area di memoria.</span><span class="sxs-lookup"><span data-stu-id="11d8f-109">The trail is caused because both windows paint to the same area of memory.</span></span> <span data-ttu-id="11d8f-110">Mentre la finestra in alto viene trascinata, la finestra sottostante deve essere ridisegnata.</span><span class="sxs-lookup"><span data-stu-id="11d8f-110">As the top-most window is dragged, the window below it must be repainted.</span></span> <span data-ttu-id="11d8f-111">Se il ridisegno è troppo lento, causa gli artefatti visualizzati nell'immagine precedente.</span><span class="sxs-lookup"><span data-stu-id="11d8f-111">If the repainting is too slow, it causes the artifacts shown in the previous image.</span></span>

<span data-ttu-id="11d8f-112">Windows Vista ha cambiato fondamentalmente il modo in cui vengono disegnate le finestre, introducendo il Gestione finestre desktop (DWM).</span><span class="sxs-lookup"><span data-stu-id="11d8f-112">Windows Vista fundamentally changed how windows are drawn, by introducing the Desktop Window Manager (DWM).</span></span> <span data-ttu-id="11d8f-113">Quando DWM è abilitato, una finestra non viene più disegnata direttamente nel buffer di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="11d8f-113">When the DWM is enabled, a window no longer draws directly to the display buffer.</span></span> <span data-ttu-id="11d8f-114">Al contrario, ogni finestra viene disegnata in un buffer di memoria offscreen, detto anche *superficie offscreen.*</span><span class="sxs-lookup"><span data-stu-id="11d8f-114">Instead, each window draws to an offscreen memory buffer, also called an *offscreen surface*.</span></span> <span data-ttu-id="11d8f-115">DWM quindi composite queste superfici sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="11d8f-115">The DWM then composites these surfaces to the screen.</span></span>

![diagramma che mostra come il dwm composita il desktop.](images/graphics05.png)

<span data-ttu-id="11d8f-117">DWM offre diversi vantaggi rispetto all'architettura grafica precedente.</span><span class="sxs-lookup"><span data-stu-id="11d8f-117">The DWM provides several advantages over the old graphics architecture.</span></span>

-   <span data-ttu-id="11d8f-118">Meno messaggi ridisegnati.</span><span class="sxs-lookup"><span data-stu-id="11d8f-118">Fewer repaint messages.</span></span> <span data-ttu-id="11d8f-119">Quando una finestra è ostruito da un'altra finestra, non è necessario ridisegnarsi.</span><span class="sxs-lookup"><span data-stu-id="11d8f-119">When a window is obstructed by another window, the obstructed window does not need to repaint itself.</span></span>
-   <span data-ttu-id="11d8f-120">Artefatti ridotti.</span><span class="sxs-lookup"><span data-stu-id="11d8f-120">Reduced artifacts.</span></span> <span data-ttu-id="11d8f-121">In precedenza, il trascinamento di una finestra poteva creare elementi visivi, come descritto.</span><span class="sxs-lookup"><span data-stu-id="11d8f-121">Previously, dragging a window could create visual artifacts, as described.</span></span>
-   <span data-ttu-id="11d8f-122">Effetti visivi.</span><span class="sxs-lookup"><span data-stu-id="11d8f-122">Visual effects.</span></span> <span data-ttu-id="11d8f-123">Poiché il DWM è responsabile della composizione dello schermo, può eseguire il rendering di aree traslucidi e sfocate della finestra.</span><span class="sxs-lookup"><span data-stu-id="11d8f-123">Because the DWM is in charge of compositing the screen, it can render translucent and blurred areas of the window.</span></span>
-   <span data-ttu-id="11d8f-124">Ridimensionamento automatico per valori DPI elevati.</span><span class="sxs-lookup"><span data-stu-id="11d8f-124">Automatic scaling for high DPI.</span></span> <span data-ttu-id="11d8f-125">Anche se il ridimensionamento non è il modo ideale per gestire valori DPI elevati, si tratta di un fallback praticabile per le applicazioni meno recenti che non sono state progettate per le impostazioni DPI elevate.</span><span class="sxs-lookup"><span data-stu-id="11d8f-125">Although scaling is not the ideal way to handle high DPI, it is a viable fallback for older applications that were not designed for high DPI settings.</span></span> <span data-ttu-id="11d8f-126">Questo argomento verrà illustrato più avanti, nella sezione [DPI e Device-Independent Pixel.](dpi-and-device-independent-pixels.md)</span><span class="sxs-lookup"><span data-stu-id="11d8f-126">(We will return to this topic later, in the section [DPI and Device-Independent Pixels](dpi-and-device-independent-pixels.md).)</span></span>
-   <span data-ttu-id="11d8f-127">Visualizzazioni alternative.</span><span class="sxs-lookup"><span data-stu-id="11d8f-127">Alternative views.</span></span> <span data-ttu-id="11d8f-128">Il DWM può usare le superfici offscreen in vari modi interessanti.</span><span class="sxs-lookup"><span data-stu-id="11d8f-128">The DWM can use the offscreen surfaces in various interesting ways.</span></span> <span data-ttu-id="11d8f-129">Ad esempio, DWM è la tecnologia alla base di Scorrimento finestre 3D, anteprime e transizioni animate.</span><span class="sxs-lookup"><span data-stu-id="11d8f-129">For example, the DWM is the technology behind Windows Flip 3D, thumbnails, and animated transitions.</span></span>

<span data-ttu-id="11d8f-130">Si noti, tuttavia, che il DWM non è garantito per essere abilitato.</span><span class="sxs-lookup"><span data-stu-id="11d8f-130">Note, however, that the DWM is not guaranteed to be enabled.</span></span> <span data-ttu-id="11d8f-131">La scheda grafica potrebbe non supportare i requisiti di sistema DWM e gli utenti possono disabilitare DWM tramite il pannello **di controllo Proprietà** del sistema.</span><span class="sxs-lookup"><span data-stu-id="11d8f-131">The graphics card might not support the DWM system requirements, and users can disable the DWM through the **System Properties** control panel.</span></span> <span data-ttu-id="11d8f-132">Ciò significa che il programma non deve basarsi sul comportamento di ridisegno del DWM.</span><span class="sxs-lookup"><span data-stu-id="11d8f-132">That means your program should not rely on the repainting behavior of the DWM.</span></span> <span data-ttu-id="11d8f-133">Testare il programma con DWM disabilitato per assicurarsi che venga ridisegnato correttamente.</span><span class="sxs-lookup"><span data-stu-id="11d8f-133">Test your program with DWM disabled to make sure that it repaints correctly.</span></span>

## <a name="next"></a><span data-ttu-id="11d8f-134">Prossima</span><span class="sxs-lookup"><span data-stu-id="11d8f-134">Next</span></span>

[<span data-ttu-id="11d8f-135">Modalità mantenuta e modalità immediata</span><span class="sxs-lookup"><span data-stu-id="11d8f-135">Retained Mode Versus Immediate Mode</span></span>](retained-mode-versus-immediate-mode.md)

 

 




