---
title: Modulo 3. Grafica di Windows
description: Il modulo 1 di questa serie ha illustrato come creare una finestra vuota.
ms.assetid: 02416d36-519e-49bd-8a52-bd3afde2be34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bbe0e7afe882180a056f4c77d72de16df0ef943
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044316"
---
# <a name="module-3-windows-graphics"></a><span data-ttu-id="a9b43-104">Modulo 3.</span><span class="sxs-lookup"><span data-stu-id="a9b43-104">Module 3.</span></span> <span data-ttu-id="a9b43-105">Grafica di Windows</span><span class="sxs-lookup"><span data-stu-id="a9b43-105">Windows Graphics</span></span>

<span data-ttu-id="a9b43-106">Il [modulo 1](your-first-windows-program.md) di questa serie ha illustrato come creare una finestra vuota.</span><span class="sxs-lookup"><span data-stu-id="a9b43-106">[Module 1](your-first-windows-program.md) of this series showed how to create a blank window.</span></span> <span data-ttu-id="a9b43-107">Il [modulo 2](module-2--using-com-in-your-windows-program.md) ha preso una lieve deviazione attraverso la Component Object Model (com), che costituisce la base per molte delle moderne API Windows.</span><span class="sxs-lookup"><span data-stu-id="a9b43-107">[Module 2](module-2--using-com-in-your-windows-program.md) took a slight detour through the Component Object Model (COM), which is the foundation for many of the modern Windows APIs.</span></span> <span data-ttu-id="a9b43-108">A questo punto è possibile aggiungere elementi grafici alla finestra vuota creata nel modulo 1.</span><span class="sxs-lookup"><span data-stu-id="a9b43-108">Now it is time to add graphics to the blank window that we created in Module 1.</span></span>

<span data-ttu-id="a9b43-109">Questo modulo inizia con una panoramica di alto livello dell'architettura grafica di Windows.</span><span class="sxs-lookup"><span data-stu-id="a9b43-109">This module starts with a high-level overview of the Windows graphics architecture.</span></span> <span data-ttu-id="a9b43-110">Si esaminerà quindi Direct2D, un'API di grafica avanzata introdotta in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a9b43-110">We then look at Direct2D, a powerful graphics API that was introduced in Windows 7.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a9b43-111">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="a9b43-111">In this section</span></span>

-   [<span data-ttu-id="a9b43-112">Panoramica dell'architettura grafica di Windows</span><span class="sxs-lookup"><span data-stu-id="a9b43-112">Overview of the Windows Graphics Architecture</span></span>](overview-of-the-windows-graphics-architecture.md)
-   [<span data-ttu-id="a9b43-113">Gestione finestre desktop</span><span class="sxs-lookup"><span data-stu-id="a9b43-113">The Desktop Window Manager</span></span>](the-desktop-window-manager.md)
-   [<span data-ttu-id="a9b43-114">Modalità mantenuta rispetto alla modalità immediata</span><span class="sxs-lookup"><span data-stu-id="a9b43-114">Retained Mode Versus Immediate Mode</span></span>](retained-mode-versus-immediate-mode.md)
-   [<span data-ttu-id="a9b43-115">Primo programma Direct2D</span><span class="sxs-lookup"><span data-stu-id="a9b43-115">Your First Direct2D Program</span></span>](your-first-direct2d-program.md)
-   [<span data-ttu-id="a9b43-116">Destinazioni di rendering, dispositivi e risorse</span><span class="sxs-lookup"><span data-stu-id="a9b43-116">Render Targets, Devices, and Resources</span></span>](render-targets--devices--and-resources.md)
-   [<span data-ttu-id="a9b43-117">Disegno con Direct2D</span><span class="sxs-lookup"><span data-stu-id="a9b43-117">Drawing with Direct2D</span></span>](drawing-with-direct2d.md)
-   [<span data-ttu-id="a9b43-118">DPI e Device-Independent pixel</span><span class="sxs-lookup"><span data-stu-id="a9b43-118">DPI and Device-Independent Pixels</span></span>](dpi-and-device-independent-pixels.md)
-   [<span data-ttu-id="a9b43-119">Uso del colore in Direct2D</span><span class="sxs-lookup"><span data-stu-id="a9b43-119">Using Color in Direct2D</span></span>](using-color-in-direct2d.md)
-   [<span data-ttu-id="a9b43-120">Applicazione di trasformazioni in Direct2D</span><span class="sxs-lookup"><span data-stu-id="a9b43-120">Applying Transforms in Direct2D</span></span>](applying-transforms-in-direct2d.md)
-   [<span data-ttu-id="a9b43-121">Appendice: trasformazioni matrice</span><span class="sxs-lookup"><span data-stu-id="a9b43-121">Appendix: Matrix Transforms</span></span>](appendix--matrix-transforms.md)

## <a name="related-topics"></a><span data-ttu-id="a9b43-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a9b43-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9b43-123">Impara a programmare per Windows in C++</span><span class="sxs-lookup"><span data-stu-id="a9b43-123">Learn to Program for Windows in C++</span></span>](learn-to-program-for-windows.md)
</dt> </dl>

 

 




