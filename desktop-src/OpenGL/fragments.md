---
title: Frammenti
description: Frammenti
ms.assetid: bc400251-32c4-4477-ba0c-a0046fe85327
keywords:
- OpenGL, frammenti
- Pipeline di elaborazione OpenGL, frammenti
- frammenti OpenGL
- framebuffer, frammenti che modificano i pixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00e2b4c2dc36e24c4fd9baa82b28fa4d336f69b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298437"
---
# <a name="fragments"></a><span data-ttu-id="ae4bd-107">Frammenti</span><span class="sxs-lookup"><span data-stu-id="ae4bd-107">Fragments</span></span>

<span data-ttu-id="ae4bd-108">Un frammento generato dalla rasterizzazione modifica il pixel corrispondente nel framebuffer solo se supera i test seguenti:</span><span class="sxs-lookup"><span data-stu-id="ae4bd-108">A fragment produced by rasterization modifies the corresponding pixel in the framebuffer only if it passes the following tests:</span></span>

-   [<span data-ttu-id="ae4bd-109">Test di proprietà pixel</span><span class="sxs-lookup"><span data-stu-id="ae4bd-109">Pixel ownership test</span></span>](pixel-ownership-test.md)
-   [<span data-ttu-id="ae4bd-110">Test Scissor</span><span class="sxs-lookup"><span data-stu-id="ae4bd-110">Scissor test</span></span>](scissor-test.md)
-   [<span data-ttu-id="ae4bd-111">Test alfa</span><span class="sxs-lookup"><span data-stu-id="ae4bd-111">Alpha test</span></span>](alpha-test.md)
-   [<span data-ttu-id="ae4bd-112">Test stencil</span><span class="sxs-lookup"><span data-stu-id="ae4bd-112">Stencil test</span></span>](stencil-test.md)
-   [<span data-ttu-id="ae4bd-113">Test del buffer di profondità</span><span class="sxs-lookup"><span data-stu-id="ae4bd-113">Depth-buffer test</span></span>](depth-buffer-test.md)

<span data-ttu-id="ae4bd-114">Se viene superato, i dati del frammento possono sostituire i valori del framebuffer esistenti oppure è possibile combinarli con i dati esistenti nel framebuffer, a seconda dello stato di determinate modalità.</span><span class="sxs-lookup"><span data-stu-id="ae4bd-114">If it passes, the fragment's data can replace the existing framebuffer values, or you can combine it with existing data in the framebuffer, depending on the state of certain modes.</span></span> <span data-ttu-id="ae4bd-115">È possibile combinare il frammento con i dati nel framebuffer:</span><span class="sxs-lookup"><span data-stu-id="ae4bd-115">You can combine the fragment with data in the framebuffer by:</span></span>

-   [<span data-ttu-id="ae4bd-116">Fusione</span><span class="sxs-lookup"><span data-stu-id="ae4bd-116">Blending</span></span>](blending.md)
-   [<span data-ttu-id="ae4bd-117">Dithering</span><span class="sxs-lookup"><span data-stu-id="ae4bd-117">Dithering</span></span>](dithering.md)
-   [<span data-ttu-id="ae4bd-118">Operazioni logiche</span><span class="sxs-lookup"><span data-stu-id="ae4bd-118">Logical operations</span></span>](logical-operations.md)

 

 




