---
title: Pixel
description: I frammenti vengono convertiti in pixel nel framebuffer.
ms.assetid: 1925b455-ae6e-4f95-899c-4bcac641f549
keywords:
- OpenGL, pixel
- Pipeline di elaborazione OpenGL, pixel
- pixel OpenGL
- framebuffer, conversione di frammenti in pixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb6660452930683943da780fad3aeb001e531711
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396831"
---
# <a name="pixels"></a><span data-ttu-id="e50cd-107">Pixel</span><span class="sxs-lookup"><span data-stu-id="e50cd-107">Pixels</span></span>

<span data-ttu-id="e50cd-108">I frammenti vengono convertiti in pixel nel framebuffer.</span><span class="sxs-lookup"><span data-stu-id="e50cd-108">Fragments are converted to pixels in the framebuffer.</span></span> <span data-ttu-id="e50cd-109">Il framebuffer è organizzato in un set di buffer logici nei buffer di colore, profondità, stencil e accumulo.</span><span class="sxs-lookup"><span data-stu-id="e50cd-109">The framebuffer is organized into a set of logical buffers the color, depth, stencil, and accumulation buffers.</span></span> <span data-ttu-id="e50cd-110">Il buffer dei colori è costituito da un lato sinistro, anteriore destro, a sinistra, a destra e un certo numero di buffer ausiliari.</span><span class="sxs-lookup"><span data-stu-id="e50cd-110">The color buffer itself consists of a front left, front right, back left, back right, and some number of auxiliary buffers.</span></span> <span data-ttu-id="e50cd-111">È possibile emettere funzioni per controllare questi buffer e leggere o copiare i pixel direttamente da essi.</span><span class="sxs-lookup"><span data-stu-id="e50cd-111">You can issue functions to control these buffers, and directly read or copy pixels from them.</span></span> <span data-ttu-id="e50cd-112">Si noti che il contesto OpenGL specifico in uso potrebbe non fornire tutti questi buffer.</span><span class="sxs-lookup"><span data-stu-id="e50cd-112">(Note that the particular OpenGL context you're using may not provide all these buffers.)</span></span>

-   [<span data-ttu-id="e50cd-113">Operazioni framebuffer</span><span class="sxs-lookup"><span data-stu-id="e50cd-113">Framebuffer Operations</span></span>](framebuffer-operations.md)
-   [<span data-ttu-id="e50cd-114">Lettura o copia dei pixel</span><span class="sxs-lookup"><span data-stu-id="e50cd-114">Reading or Copying Pixels</span></span>](reading-or-copying-pixels.md)
-   [<span data-ttu-id="e50cd-115">Riferimento pixel</span><span class="sxs-lookup"><span data-stu-id="e50cd-115">Pixels Reference</span></span>](pixels-reference.md)

 

 




