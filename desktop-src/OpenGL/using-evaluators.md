---
title: Utilizzo degli analizzatori
description: Utilizzo degli analizzatori
ms.assetid: a5a99d0a-526e-4492-90c4-a6b9fdbdff16
keywords:
- OpenGL, analizzatori
- analizzatori OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1aef70a7a854e16cf4992d9dd44c4931ad4d044
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329204"
---
# <a name="using-evaluators"></a><span data-ttu-id="3a903-105">Utilizzo degli analizzatori</span><span class="sxs-lookup"><span data-stu-id="3a903-105">Using Evaluators</span></span>

<span data-ttu-id="3a903-106">Le funzioni dell'analizzatore OpenGL consentono di usare un mapping polinomiale per produrre vertici, normali, coordinate di trama e colori.</span><span class="sxs-lookup"><span data-stu-id="3a903-106">The OpenGL evaluator functions allow you to use a polynomial mapping to produce vertices, normals, texture coordinates, and colors.</span></span> <span data-ttu-id="3a903-107">Questi valori calcolati vengono quindi passati alla pipeline di elaborazione come se fossero stati specificati direttamente.</span><span class="sxs-lookup"><span data-stu-id="3a903-107">These calculated values are then passed on to the processing pipeline as if they had been directly specified.</span></span> <span data-ttu-id="3a903-108">Le funzioni dell'analizzatore rappresentano anche la base per le funzioni NURBS (non-Uniform Rational B-spline), che consentono di definire curve e superfici, come descritto nella [libreria di utilità OpenGL](opengl-utility-library.md).</span><span class="sxs-lookup"><span data-stu-id="3a903-108">The evaluator functions are also the basis for the NURBS (Non-Uniform Rational B-Spline) functions, which allow you to define curves and surfaces, as described under [OpenGL Utility library](opengl-utility-library.md).</span></span>

<span data-ttu-id="3a903-109">Il primo passaggio nell'utilizzo degli analizzatori consiste nel definire il mapping polinomiale bidimensionale o bidimensionale appropriato utilizzando [**glMap \***](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="3a903-109">The first step in using evaluators is to define the appropriate one- or two-dimensional polynomial mapping using [**glMap\***](glmap1.md).</span></span> <span data-ttu-id="3a903-110">È quindi possibile specificare e valutare i valori di dominio per la mappa in uno dei due modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="3a903-110">You can then specify and evaluate the domain values for this map in one of two ways:</span></span>

-   <span data-ttu-id="3a903-111">Definire una serie di valori di dominio con spazi uniformi da mappare usando [**glMapGrid**](glmapgrid-functions.md) , quindi valutare un subset rettangolare della griglia con [**glEvalMesh**](glevalmesh-functions.md).</span><span class="sxs-lookup"><span data-stu-id="3a903-111">Define a series of evenly spaced domain values to be mapped using [**glMapGrid**](glmapgrid-functions.md) and then evaluate a rectangular subset of that grid with [**glEvalMesh**](glevalmesh-functions.md).</span></span> <span data-ttu-id="3a903-112">Un singolo punto della griglia può essere valutato usando [**glEvalPoint**](glevalpoint.md).</span><span class="sxs-lookup"><span data-stu-id="3a903-112">A single point of the grid can be evaluated using [**glEvalPoint**](glevalpoint.md).</span></span>
-   <span data-ttu-id="3a903-113">Specificare in modo esplicito un valore di dominio desiderato come argomento, che valuta le mappe in corrispondenza di tale valore.</span><span class="sxs-lookup"><span data-stu-id="3a903-113">Explicitly specify a desired domain value as an argument, which evaluates the maps at that value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a903-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3a903-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a903-115">Riferimento per gli analizzatori</span><span class="sxs-lookup"><span data-stu-id="3a903-115">Evaluators Reference</span></span>](evaluators-reference.md)
</dt> </dl>

 

 




