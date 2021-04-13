---
title: Lettura o copia dei pixel
description: È possibile leggere i pixel dal framebuffer in memoria, codificarli in diversi modi e archiviare il risultato codificato in memoria con glReadPixels.
ms.assetid: 6a6a710e-4d19-4fbf-9f25-abf22635c806
keywords:
- Pipeline di elaborazione OpenGL, lettura dei pixel
- Pipeline di elaborazione OpenGL, copia dei pixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35600f3fb803d4453a24f9c5a051859ac159bad6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395635"
---
# <a name="reading-or-copying-pixels"></a><span data-ttu-id="c5cbe-105">Lettura o copia dei pixel</span><span class="sxs-lookup"><span data-stu-id="c5cbe-105">Reading or Copying Pixels</span></span>

<span data-ttu-id="c5cbe-106">È possibile leggere i pixel dal framebuffer in memoria, codificarli in diversi modi e archiviare il risultato codificato in memoria con [**glReadPixels**](glreadpixels.md).</span><span class="sxs-lookup"><span data-stu-id="c5cbe-106">You can read pixels from the framebuffer into memory, encode them in various ways, and store the encoded result in memory with [**glReadPixels**](glreadpixels.md).</span></span> <span data-ttu-id="c5cbe-107">Inoltre, è possibile copiare un rettangolo di valori pixel da un'area del framebuffer a un'altra con [**glCopyPixels**](glcopypixels.md).</span><span class="sxs-lookup"><span data-stu-id="c5cbe-107">In addition, you can copy a rectangle of pixel values from one region of the framebuffer to another with [**glCopyPixels**](glcopypixels.md).</span></span> <span data-ttu-id="c5cbe-108">La funzione [**glReadBuffer**](glreadbuffer.md) controlla il buffer dei colori da cui vengono letti o copiati i pixel.</span><span class="sxs-lookup"><span data-stu-id="c5cbe-108">The function [**glReadBuffer**](glreadbuffer.md) controls which color buffer the pixels are read or copied from.</span></span>

 

 




