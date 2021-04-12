---
title: Gestione finestre desktop
description: .
ms.assetid: 79250d49-dad5-46c6-892d-b92dac14b417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73167b762a9952eb508f09e70f3d4183b3b7a018
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329791"
---
# <a name="the-desktop-window-manager"></a><span data-ttu-id="25aa2-103">Gestione finestre desktop</span><span class="sxs-lookup"><span data-stu-id="25aa2-103">The Desktop Window Manager</span></span>

<span data-ttu-id="25aa2-104">Prima di Windows Vista, un programma di Windows veniva disegnato direttamente sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="25aa2-104">Before Windows Vista, a Windows program would draw directly to the screen.</span></span> <span data-ttu-id="25aa2-105">In altre parole, il programma scrive direttamente nel buffer di memoria visualizzato dalla scheda video.</span><span class="sxs-lookup"><span data-stu-id="25aa2-105">In other words, the program would write directly to the memory buffer shown by the video card.</span></span> <span data-ttu-id="25aa2-106">Questo approccio può provocare artefatti visivi se una finestra non viene ridisegnata correttamente.</span><span class="sxs-lookup"><span data-stu-id="25aa2-106">This approach can cause visual artifacts if a window does not repaint itself correctly.</span></span> <span data-ttu-id="25aa2-107">Se, ad esempio, l'utente trascina una finestra su un'altra finestra e la finestra sottostante non viene ridisegnata abbastanza rapidamente, la finestra in primo piano può uscire da una traccia:</span><span class="sxs-lookup"><span data-stu-id="25aa2-107">For example, if the user drags one window over another window, and the window underneath does not repaint itself quickly enough, the top-most window can leave a trail:</span></span>

![screenshot che Mostra gli artefatti di ridisegno.](images/graphics04.png)

<span data-ttu-id="25aa2-109">Il percorso è dovuto al fatto che entrambe le finestre disegnano nella stessa area di memoria.</span><span class="sxs-lookup"><span data-stu-id="25aa2-109">The trail is caused because both windows paint to the same area of memory.</span></span> <span data-ttu-id="25aa2-110">Quando la finestra in primo piano viene trascinata, la finestra sottostante deve essere ridisegnata.</span><span class="sxs-lookup"><span data-stu-id="25aa2-110">As the top-most window is dragged, the window below it must be repainted.</span></span> <span data-ttu-id="25aa2-111">Se il ridisegno è troppo lento, causa gli artefatti mostrati nell'immagine precedente.</span><span class="sxs-lookup"><span data-stu-id="25aa2-111">If the repainting is too slow, it causes the artifacts shown in the previous image.</span></span>

<span data-ttu-id="25aa2-112">Windows Vista ha modificato in modo sostanziale il modo in cui vengono disegnate le finestre, introducendo il Gestione finestre desktop (DWM).</span><span class="sxs-lookup"><span data-stu-id="25aa2-112">Windows Vista fundamentally changed how windows are drawn, by introducing the Desktop Window Manager (DWM).</span></span> <span data-ttu-id="25aa2-113">Quando DWM è abilitato, una finestra non viene più disegnata direttamente nel buffer di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="25aa2-113">When the DWM is enabled, a window no longer draws directly to the display buffer.</span></span> <span data-ttu-id="25aa2-114">Ogni finestra viene invece disegnata in un buffer di memoria Offscreen, detto anche *superficie Offscreen*.</span><span class="sxs-lookup"><span data-stu-id="25aa2-114">Instead, each window draws to an offscreen memory buffer, also called an *offscreen surface*.</span></span> <span data-ttu-id="25aa2-115">DWM quindi compone queste superfici sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="25aa2-115">The DWM then composites these surfaces to the screen.</span></span>

![diagramma che illustra il modo in cui DWM compone il desktop.](images/graphics05.png)

<span data-ttu-id="25aa2-117">DWM offre diversi vantaggi rispetto all'architettura grafica precedente.</span><span class="sxs-lookup"><span data-stu-id="25aa2-117">The DWM provides several advantages over the old graphics architecture.</span></span>

-   <span data-ttu-id="25aa2-118">Meno messaggi di ridisegno.</span><span class="sxs-lookup"><span data-stu-id="25aa2-118">Fewer repaint messages.</span></span> <span data-ttu-id="25aa2-119">Quando una finestra è ostruita da un'altra finestra, non è necessario che la finestra ostruita venga ridisegnata.</span><span class="sxs-lookup"><span data-stu-id="25aa2-119">When a window is obstructed by another window, the obstructed window does not need to repaint itself.</span></span>
-   <span data-ttu-id="25aa2-120">Elementi ridotti.</span><span class="sxs-lookup"><span data-stu-id="25aa2-120">Reduced artifacts.</span></span> <span data-ttu-id="25aa2-121">In precedenza, il trascinamento di una finestra poteva creare artefatti visivi, come descritto.</span><span class="sxs-lookup"><span data-stu-id="25aa2-121">Previously, dragging a window could create visual artifacts, as described.</span></span>
-   <span data-ttu-id="25aa2-122">Effetti visivi.</span><span class="sxs-lookup"><span data-stu-id="25aa2-122">Visual effects.</span></span> <span data-ttu-id="25aa2-123">Poiché DWM è responsabile della composizione dello schermo, può eseguire il rendering delle aree trasparenti e sfocate della finestra.</span><span class="sxs-lookup"><span data-stu-id="25aa2-123">Because the DWM is in charge of compositing the screen, it can render translucent and blurred areas of the window.</span></span>
-   <span data-ttu-id="25aa2-124">Ridimensionamento automatico per valori DPI alti.</span><span class="sxs-lookup"><span data-stu-id="25aa2-124">Automatic scaling for high DPI.</span></span> <span data-ttu-id="25aa2-125">Sebbene il ridimensionamento non sia il modo ideale per gestire valori DPI elevati, è un fallback valido per le applicazioni meno recenti che non sono state progettate per impostazioni DPI elevate.</span><span class="sxs-lookup"><span data-stu-id="25aa2-125">Although scaling is not the ideal way to handle high DPI, it is a viable fallback for older applications that were not designed for high DPI settings.</span></span> <span data-ttu-id="25aa2-126">Si tornerà a questo argomento in un secondo momento, nella sezione [dpi e Device-Independent pixel](dpi-and-device-independent-pixels.md).</span><span class="sxs-lookup"><span data-stu-id="25aa2-126">(We will return to this topic later, in the section [DPI and Device-Independent Pixels](dpi-and-device-independent-pixels.md).)</span></span>
-   <span data-ttu-id="25aa2-127">Visualizzazioni alternative.</span><span class="sxs-lookup"><span data-stu-id="25aa2-127">Alternative views.</span></span> <span data-ttu-id="25aa2-128">DWM può utilizzare le superfici Offscreen in diversi modi interessanti.</span><span class="sxs-lookup"><span data-stu-id="25aa2-128">The DWM can use the offscreen surfaces in various interesting ways.</span></span> <span data-ttu-id="25aa2-129">Ad esempio, DWM è la tecnologia alla base di Windows Flip 3D, anteprime e transizioni animate.</span><span class="sxs-lookup"><span data-stu-id="25aa2-129">For example, the DWM is the technology behind Windows Flip 3D, thumbnails, and animated transitions.</span></span>

<span data-ttu-id="25aa2-130">Si noti, tuttavia, che non è garantita l'abilitazione di DWM.</span><span class="sxs-lookup"><span data-stu-id="25aa2-130">Note, however, that the DWM is not guaranteed to be enabled.</span></span> <span data-ttu-id="25aa2-131">La scheda grafica potrebbe non supportare i requisiti di sistema DWM e gli utenti possono disabilitare DWM tramite il pannello di controllo **Proprietà sistema** .</span><span class="sxs-lookup"><span data-stu-id="25aa2-131">The graphics card might not support the DWM system requirements, and users can disable the DWM through the **System Properties** control panel.</span></span> <span data-ttu-id="25aa2-132">Ciò significa che il programma non deve basarsi sul comportamento di ridisegno di DWM.</span><span class="sxs-lookup"><span data-stu-id="25aa2-132">That means your program should not rely on the repainting behavior of the DWM.</span></span> <span data-ttu-id="25aa2-133">Testare il programma con DWM disabilitato per assicurarsi che venga ridisegnato correttamente.</span><span class="sxs-lookup"><span data-stu-id="25aa2-133">Test your program with DWM disabled to make sure that it repaints correctly.</span></span>

## <a name="next"></a><span data-ttu-id="25aa2-134">Prossima</span><span class="sxs-lookup"><span data-stu-id="25aa2-134">Next</span></span>

[<span data-ttu-id="25aa2-135">Modalità mantenuta rispetto alla modalità immediata</span><span class="sxs-lookup"><span data-stu-id="25aa2-135">Retained Mode Versus Immediate Mode</span></span>](retained-mode-versus-immediate-mode.md)

 

 




