---
title: Gestione finestre desktop
description: La funzionalità di composizione desktop, introdotta in Windows Vista, ha cambiato radicalmente il modo in cui le applicazioni visualizzano i pixel sullo schermo.
ms.assetid: VS|winui|~\winui\desktopwindowmanager\overviews\dwm_overview.htm
keywords:
- Gestione finestre desktop (DWM), informazioni
- DWM (Gestione finestre desktop), informazioni
- Gestione finestre desktop (DWM), composizione
- DWM (Gestione finestre desktop), composizione
- composizione del desktop
- Composizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8578001aebf1c73e6d400ffae383674a8432c399
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711191"
---
# <a name="desktop-window-manager"></a><span data-ttu-id="c0b87-109">Gestione finestre desktop</span><span class="sxs-lookup"><span data-stu-id="c0b87-109">Desktop Window Manager</span></span>

<span data-ttu-id="c0b87-110">La funzionalità di composizione desktop, introdotta in Windows Vista, ha cambiato radicalmente il modo in cui le applicazioni visualizzano i pixel sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="c0b87-110">The desktop composition feature, introduced in Windows Vista, fundamentally changed the way applications display pixels on the screen.</span></span> <span data-ttu-id="c0b87-111">Quando è abilitata la composizione del desktop, le singole finestre non vengono più riportate direttamente sullo schermo o sul dispositivo di visualizzazione principale come nelle versioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="c0b87-111">When desktop composition is enabled, individual windows no longer draw directly to the screen or primary display device as they did in previous versions of Windows.</span></span> <span data-ttu-id="c0b87-112">Il disegno viene invece reindirizzato alle superfici fuori schermo nella memoria video, che vengono quindi sottoposte a rendering in un'immagine desktop e visualizzate sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="c0b87-112">Instead, their drawing is redirected to off-screen surfaces in video memory, which are then rendered into a desktop image and presented on the display.</span></span>

<span data-ttu-id="c0b87-113">La composizione del desktop viene eseguita dal Gestione finestre desktop (DWM).</span><span class="sxs-lookup"><span data-stu-id="c0b87-113">Desktop composition is performed by the Desktop Window Manager (DWM).</span></span> <span data-ttu-id="c0b87-114">Grazie alla composizione del desktop, DWM consente effetti visivi sul desktop, nonché diverse funzionalità, ad esempio la cornice della finestra, le animazioni di transizione delle finestre 3D, Windows Flip e Windows Flip3D e un supporto ad alta risoluzione.</span><span class="sxs-lookup"><span data-stu-id="c0b87-114">Through desktop composition, DWM enables visual effects on the desktop as well as various features such as glass window frames, 3-D window transition animations, Windows Flip and Windows Flip3D, and high resolution support.</span></span>

<span data-ttu-id="c0b87-115">Il Gestione finestre desktop viene eseguito come servizio Windows.</span><span class="sxs-lookup"><span data-stu-id="c0b87-115">The Desktop Window Manager runs as a Windows service.</span></span> <span data-ttu-id="c0b87-116">Può essere abilitata e disabilitata tramite l'elemento del pannello di controllo strumenti di amministrazione, in servizi, come Gestione finestre desktop gestione sessioni.</span><span class="sxs-lookup"><span data-stu-id="c0b87-116">It can be enabled and disabled through the Administrative Tools Control Panel item, under Services, as Desktop Window Manager Session Manager.</span></span>

<span data-ttu-id="c0b87-117">Molte delle funzionalità di DWM possono essere controllate o accessibili da un'applicazione tramite le API di DWM.</span><span class="sxs-lookup"><span data-stu-id="c0b87-117">Many of the DWM features can be controlled or accessed by an application through the DWM APIs.</span></span> <span data-ttu-id="c0b87-118">Nella documentazione seguente vengono descritte le caratteristiche e i requisiti delle API DWM.</span><span class="sxs-lookup"><span data-stu-id="c0b87-118">The following documentation describes the features and requirements of the DWM APIs.</span></span>

-   [<span data-ttu-id="c0b87-119">Panoramica di DWM</span><span class="sxs-lookup"><span data-stu-id="c0b87-119">DWM Overviews</span></span>](desktop-window-manager-overviews.md)
-   [<span data-ttu-id="c0b87-120">Esempio di codice DWM</span><span class="sxs-lookup"><span data-stu-id="c0b87-120">DWM Sample Code</span></span>](dwm-samples.md)
-   [<span data-ttu-id="c0b87-121">Riferimento per DWM</span><span class="sxs-lookup"><span data-stu-id="c0b87-121">DWM Reference</span></span>](reference.md)

 

 




