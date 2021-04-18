---
title: Variabili di stato OpenGL
description: Negli argomenti seguenti vengono elencati i nomi delle variabili di stato su cui è possibile eseguire query
ms.assetid: f4bc4ec1-a529-4b9e-84af-94caa0ef7131
keywords:
- Variabili di stato OpenGL
- variabili di stato, OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36dee51ba7726277832d94eaf336d03d3c579189
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298206"
---
# <a name="opengl-state-variables"></a><span data-ttu-id="2c4b2-105">Variabili di stato OpenGL</span><span class="sxs-lookup"><span data-stu-id="2c4b2-105">OpenGL State Variables</span></span>

<span data-ttu-id="2c4b2-106">Negli argomenti seguenti vengono elencati i nomi delle variabili di stato su cui è possibile eseguire query:</span><span class="sxs-lookup"><span data-stu-id="2c4b2-106">The following topics list the names of state variables that can be queried:</span></span>

-   [<span data-ttu-id="2c4b2-107">**Variabili di stato per i valori correnti e i dati associati**</span><span class="sxs-lookup"><span data-stu-id="2c4b2-107">**State Variables for Current Values and Associated Data**</span></span>](state-variables-for-current-values-and-associated-data.md)
-   [<span data-ttu-id="2c4b2-108">**Variabili di stato della trasformazione**</span><span class="sxs-lookup"><span data-stu-id="2c4b2-108">**Transformation State Variables**</span></span>](transformation-state-variables.md)
-   [<span data-ttu-id="2c4b2-109">**Variabili di stato colorazione**</span><span class="sxs-lookup"><span data-stu-id="2c4b2-109">**Coloring State Variables**</span></span>](coloring-state-variables.md)
-   [<span data-ttu-id="2c4b2-110">**Variabili di stato di illuminazione**</span><span class="sxs-lookup"><span data-stu-id="2c4b2-110">**Lighting State Variables**</span></span>](lighting-state-variables.md)
-   [<span data-ttu-id="2c4b2-111">**Variabili di stato di rasterizzazione**</span><span class="sxs-lookup"><span data-stu-id="2c4b2-111">**Rasterization State Variables**</span></span>](rasterization-state-variables.md)
-   [<span data-ttu-id="2c4b2-112">**Variabili di stato di texturing**</span><span class="sxs-lookup"><span data-stu-id="2c4b2-112">**Texturing State Variables**</span></span>](texturing-state-variables.md)
-   [<span data-ttu-id="2c4b2-113">**Operazioni pixel**</span><span class="sxs-lookup"><span data-stu-id="2c4b2-113">**Pixel Operations**</span></span>](pixel-operations.md)
-   [<span data-ttu-id="2c4b2-114">**Variabili di stato del controllo framebuffer**</span><span class="sxs-lookup"><span data-stu-id="2c4b2-114">**Framebuffer Control State Variables**</span></span>](framebuffer-control-state-variables.md)
-   [<span data-ttu-id="2c4b2-115">**Variabili di stato pixel**</span><span class="sxs-lookup"><span data-stu-id="2c4b2-115">**Pixel State Variables**</span></span>](pixel-state-variables.md)
-   [<span data-ttu-id="2c4b2-116">**Variabili di stato dell'analizzatore**</span><span class="sxs-lookup"><span data-stu-id="2c4b2-116">**Evaluator State Variables**</span></span>](evaluator-state-variables.md)
-   [<span data-ttu-id="2c4b2-117">**Variabili di stato dell'hint**</span><span class="sxs-lookup"><span data-stu-id="2c4b2-117">**Hint State Variables**</span></span>](hint-state-variables.md)
-   [<span data-ttu-id="2c4b2-118">**Variabili di stato dipendenti dall'implementazione**</span><span class="sxs-lookup"><span data-stu-id="2c4b2-118">**Implementation-Dependent State Variables**</span></span>](implementation-dependent-state-variables.md)
-   [<span data-ttu-id="2c4b2-119">**Variabili di stato del Pixel-Depth dipendente dall'implementazione**</span><span class="sxs-lookup"><span data-stu-id="2c4b2-119">**Implementation-Dependent Pixel-Depth State Variables**</span></span>](implementation-dependent-pixel-depth-state-variables.md)
-   [<span data-ttu-id="2c4b2-120">**Variabili di stato varie**</span><span class="sxs-lookup"><span data-stu-id="2c4b2-120">**Miscellaneous State Variables**</span></span>](miscellaneous-state-variables.md)

<span data-ttu-id="2c4b2-121">Per ogni variabile, l'argomento elenca una descrizione, un gruppo di attributi, un valore iniziale o minimo e la funzione [**glGet \***](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) suggerita da usare per ottenerlo.</span><span class="sxs-lookup"><span data-stu-id="2c4b2-121">For each variable, the topic lists a description, attribute group, initial or minimum value, and the suggested [**glGet\***](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) function to use for obtaining it.</span></span>

<span data-ttu-id="2c4b2-122">Le variabili di stato che è possibile ottenere tramite [**glGetBooleanv**](glgetbooleanv.md), [**glGetIntegerv**](glgetintegerv.md), [**glGetFloatv**](glgetfloatv.md)o [**glGetDoublev**](glgetdoublev.md) sono elencate con una sola di queste functionsthe più appropriate per il tipo di dati da restituire.</span><span class="sxs-lookup"><span data-stu-id="2c4b2-122">State variables that you can obtain using [**glGetBooleanv**](glgetbooleanv.md), [**glGetIntegerv**](glgetintegerv.md), [**glGetFloatv**](glgetfloatv.md), or [**glGetDoublev**](glgetdoublev.md) are listed with just one of these functionsthe one that is most appropriate for the type of data to be returned.</span></span> <span data-ttu-id="2c4b2-123">Non è possibile ottenere queste variabili di stato usando [**glIsEnabled**](glisenabled.md).</span><span class="sxs-lookup"><span data-stu-id="2c4b2-123">You cannot obtain these state variables using [**glIsEnabled**](glisenabled.md).</span></span> <span data-ttu-id="2c4b2-124">È tuttavia possibile ottenere le variabili di stato per le quali **glIsEnabled** è elencato come funzione di query con **glGetBooleanv**, **glGetIntegerv**, **glGetFloatv** e **glGetDoublev**.</span><span class="sxs-lookup"><span data-stu-id="2c4b2-124">However, you can obtain state variables for which **glIsEnabled** is listed as the query function with **glGetBooleanv**, **glGetIntegerv**, **glGetFloatv**, and **glGetDoublev**.</span></span> <span data-ttu-id="2c4b2-125">È possibile ottenere le variabili di stato per le quali qualsiasi altra funzione è elencata come funzione di query solo usando tale funzione.</span><span class="sxs-lookup"><span data-stu-id="2c4b2-125">You can obtain state variables for which any other function is listed as the query function only by using that function.</span></span> <span data-ttu-id="2c4b2-126">Se non è elencato alcun gruppo di attributi, la variabile non appartiene ad alcun gruppo.</span><span class="sxs-lookup"><span data-stu-id="2c4b2-126">If no attribute group is listed, the variable doesn't belong to any group.</span></span> <span data-ttu-id="2c4b2-127">Tutte le variabili di stato su cui è possibile eseguire una query, ad eccezione di quelle che dipendono dall'implementazione, presentano valori iniziali.</span><span class="sxs-lookup"><span data-stu-id="2c4b2-127">All state variables that you can query, except those that are implementation dependent, have initial values.</span></span> <span data-ttu-id="2c4b2-128">Per determinare il valore iniziale di una variabile per la quale non è elencato alcun valore iniziale, vedere il riferimento della variabile o il</span><span class="sxs-lookup"><span data-stu-id="2c4b2-128">To determine the initial value of a variable for which no initial value is listed, see that variable's reference or the</span></span>

<span data-ttu-id="2c4b2-129">*Manuale di riferimento OpenGL*.</span><span class="sxs-lookup"><span data-stu-id="2c4b2-129">*OpenGL Reference Manual*.</span></span>

 

 




