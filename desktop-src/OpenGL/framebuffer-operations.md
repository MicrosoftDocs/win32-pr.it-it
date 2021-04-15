---
title: Operazioni framebuffer
description: Per selezionare il buffer in cui vengono scritti i valori dei colori, utilizzare glDrawBuffer.
ms.assetid: 5469a183-1dc0-4ec2-bd7e-54060b5a2876
keywords:
- Pipeline di elaborazione OpenGL, operazioni framebuffer
- framebuffer, operazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6199700d00a6628548404870dd6ef6ce3e2c825
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515598"
---
# <a name="framebuffer-operations"></a><span data-ttu-id="fbe61-105">Operazioni framebuffer</span><span class="sxs-lookup"><span data-stu-id="fbe61-105">Framebuffer Operations</span></span>

<span data-ttu-id="fbe61-106">Per selezionare il buffer in cui vengono scritti i valori dei colori, utilizzare [**glDrawBuffer**](gldrawbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="fbe61-106">To select the buffer into which color values are written, use [**glDrawBuffer**](gldrawbuffer.md).</span></span> <span data-ttu-id="fbe61-107">È possibile utilizzare quattro funzioni diverse per mascherare la scrittura di bit in ogni framebuffer logico dopo che sono state eseguite tutte le operazioni per frammento:</span><span class="sxs-lookup"><span data-stu-id="fbe61-107">You use four different functions to mask the writing of bits to each of the logical framebuffers after all per-fragment operations have been performed:</span></span>

-   [<span data-ttu-id="fbe61-108">**glIndexMask**</span><span class="sxs-lookup"><span data-stu-id="fbe61-108">**glIndexMask**</span></span>](glindexmask.md)
-   [<span data-ttu-id="fbe61-109">**glColorMask**</span><span class="sxs-lookup"><span data-stu-id="fbe61-109">**glColorMask**</span></span>](glcolormask.md)
-   [<span data-ttu-id="fbe61-110">**glDepthMask**</span><span class="sxs-lookup"><span data-stu-id="fbe61-110">**glDepthMask**</span></span>](gldepthmask.md)
-   [<span data-ttu-id="fbe61-111">**glStencilMask**</span><span class="sxs-lookup"><span data-stu-id="fbe61-111">**glStencilMask**</span></span>](glstencilmask.md)

<span data-ttu-id="fbe61-112">La funzione [**glAccum**](glaccum.md) controlla l'operazione del buffer di accumulo.</span><span class="sxs-lookup"><span data-stu-id="fbe61-112">The [**glAccum**](glaccum.md) function controls the operation of the accumulation buffer.</span></span> <span data-ttu-id="fbe61-113">Infine, [**glClear**](glclear.md) imposta ogni pixel in un subset specificato di buffer sul valore specificato con [**glClearColor**](glclearcolor.md), [**glClearIndex**](glclearindex.md), [**glClearDepth**](glcleardepth.md), [**glClearStencil**](glclearstencil.md)o [**glClearAccum**](glclearaccum.md).</span><span class="sxs-lookup"><span data-stu-id="fbe61-113">Finally, [**glClear**](glclear.md) sets every pixel in a specified subset of the buffers to the value specified with [**glClearColor**](glclearcolor.md), [**glClearIndex**](glclearindex.md), [**glClearDepth**](glcleardepth.md), [**glClearStencil**](glclearstencil.md), or [**glClearAccum**](glclearaccum.md).</span></span>

 

 




