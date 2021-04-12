---
title: Esecuzione di selezioni e commenti
description: Esecuzione di selezioni e commenti
ms.assetid: 908114b3-ac0e-4fd5-ad28-137e6af7ffc7
keywords:
- OpenGL, selezione
- OpenGL, commenti e suggerimenti
- OpenGL, rendering
- modalità di selezione OpenGL
- modalità feedback OpenGL
- modalità di rendering OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be13ae103d33039c996851582823c23c30316731
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329996"
---
# <a name="performing-selection-and-feedback"></a><span data-ttu-id="381c1-109">Esecuzione di selezioni e commenti</span><span class="sxs-lookup"><span data-stu-id="381c1-109">Performing Selection and Feedback</span></span>

<span data-ttu-id="381c1-110">Selezione, feedback e rendering si escludono a vicenda modalità di funzionamento.</span><span class="sxs-lookup"><span data-stu-id="381c1-110">Selection, feedback, and rendering are mutually exclusive modes of operation.</span></span> <span data-ttu-id="381c1-111">Il rendering è la modalità standard predefinita durante la quale i frammenti vengono prodotti dalla rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="381c1-111">Rendering is the normal, default mode during which fragments are produced by rasterization.</span></span>

<span data-ttu-id="381c1-112">Nelle modalità selezione e feedback non viene prodotto alcun frammento; Pertanto, non si verifica alcuna modifica del framebuffer.</span><span class="sxs-lookup"><span data-stu-id="381c1-112">In selection and feedback modes, no fragments are produced; therefore, no framebuffer modification occurs.</span></span> <span data-ttu-id="381c1-113">In modalità di selezione è possibile determinare quali primitive verranno disegnate in una determinata area di una finestra; in modalità feedback, le informazioni sulle primitive che verranno rasterizzate vengono riportate all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="381c1-113">In selection mode, you can determine which primitives will be drawn into some region of a window; in feedback mode, information about primitives that will be rasterized is fed back to the application.</span></span>

<span data-ttu-id="381c1-114">È possibile scegliere tra queste tre modalità con [**glRenderMode**](glrendermode.md).</span><span class="sxs-lookup"><span data-stu-id="381c1-114">You select among these three modes with [**glRenderMode**](glrendermode.md).</span></span>

-   [<span data-ttu-id="381c1-115">Selezione</span><span class="sxs-lookup"><span data-stu-id="381c1-115">Selection</span></span>](selection.md)
-   [<span data-ttu-id="381c1-116">Commenti e suggerimenti</span><span class="sxs-lookup"><span data-stu-id="381c1-116">Feedback</span></span>](feedback.md)
-   [<span data-ttu-id="381c1-117">Guida di riferimento a selezione e feedback</span><span class="sxs-lookup"><span data-stu-id="381c1-117">Selection and Feedback Reference</span></span>](selection-and-feedback-reference.md)

 

 




