---
title: Test stencil
description: Il test di stencil Elimina in modo condizionale un frammento in base al risultato di un confronto tra il valore nel buffer dello stencil e un valore di riferimento.
ms.assetid: 967be1e5-a9a2-45cc-aae7-c33cc257ade1
keywords:
- Pipeline di elaborazione OpenGL, test stencil
- test stencil OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e285c3dfb1591c5ed3d95969024d2350a7517a79
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713930"
---
# <a name="stencil-test"></a><span data-ttu-id="5d154-105">Test stencil</span><span class="sxs-lookup"><span data-stu-id="5d154-105">Stencil Test</span></span>

<span data-ttu-id="5d154-106">Il test di stencil Elimina in modo condizionale un frammento in base al risultato di un confronto tra il valore nel buffer dello stencil e un valore di riferimento.</span><span class="sxs-lookup"><span data-stu-id="5d154-106">The stencil test conditionally discards a fragment based on the outcome of a comparison between the value in the stencil buffer and a reference value.</span></span> <span data-ttu-id="5d154-107">La funzione [**glStencilFunc**](glstencilfunc.md) specifica la funzione di confronto e il valore di riferimento.</span><span class="sxs-lookup"><span data-stu-id="5d154-107">The [**glStencilFunc**](glstencilfunc.md) function specifies the comparison function and the reference value.</span></span> <span data-ttu-id="5d154-108">Se il frammento passa o non supera il test di stencil, il valore nel buffer dello stencil viene modificato in base alle istruzioni specificate con [**glStencilOp**](glstencilop.md).</span><span class="sxs-lookup"><span data-stu-id="5d154-108">Whether the fragment passes or fails the stencil test, the value in the stencil buffer is modified according to the instructions specified with [**glStencilOp**](glstencilop.md).</span></span>

 

 




