---
title: Uso delle funzioni di query
description: Uso delle funzioni di query
ms.assetid: 5f874a0e-77c0-4009-a18f-a852d7ffe891
keywords:
- OpenGL, funzioni di query
- funzioni di query OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14804b260451d4b51b0146b1cb2f796ba6b6778e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298300"
---
# <a name="using-the-query-functions"></a><span data-ttu-id="5960a-105">Uso delle funzioni di query</span><span class="sxs-lookup"><span data-stu-id="5960a-105">Using the Query Functions</span></span>

<span data-ttu-id="5960a-106">Sono disponibili quattro funzioni di query per ottenere semplici variabili di stato e una per determinare se un determinato stato è abilitato o disabilitato:</span><span class="sxs-lookup"><span data-stu-id="5960a-106">There are four query functions for obtaining simple state variables and one for determining whether a particular state is enabled or disabled:</span></span>

-   [<span data-ttu-id="5960a-107">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="5960a-107">**glGetBooleanv**</span></span>](glgetbooleanv.md)
-   [<span data-ttu-id="5960a-108">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="5960a-108">**glGetIntegerv**</span></span>](glgetintegerv.md)
-   [<span data-ttu-id="5960a-109">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="5960a-109">**glGetFloatv**</span></span>](glgetfloatv.md)
-   [<span data-ttu-id="5960a-110">**glGetDoublev**</span><span class="sxs-lookup"><span data-stu-id="5960a-110">**glGetDoublev**</span></span>](glgetdoublev.md)
-   [<span data-ttu-id="5960a-111">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="5960a-111">**glIsEnabled**</span></span>](glisenabled.md)

<span data-ttu-id="5960a-112">I prototipi per le funzioni di query sono:</span><span class="sxs-lookup"><span data-stu-id="5960a-112">The prototypes for the query functions are:</span></span>

<span data-ttu-id="5960a-113">**void** **glGetBooleanv**(**GLEnum** *pname* , **GLboolean \*** *params* );</span><span class="sxs-lookup"><span data-stu-id="5960a-113">**void** **glGetBooleanv**(**GLenum** *pname* , **GLboolean \*** *params* );</span></span>

<span data-ttu-id="5960a-114">**void** **glGetIntegerv**(**GLEnum** *pname* , **riflesso \*** *params* );</span><span class="sxs-lookup"><span data-stu-id="5960a-114">**void** **glGetIntegerv**(**GLenum** *pname* , **GLint \*** *params* );</span></span>

<span data-ttu-id="5960a-115">**void** **glGetFloatv**(**GLEnum** *pname* , **GLfloat \*** *params* );</span><span class="sxs-lookup"><span data-stu-id="5960a-115">**void** **glGetFloatv**(**GLenum** *pname* , **GLfloat \*** *params* );</span></span>

<span data-ttu-id="5960a-116">**void** **glGetDoublev**(**GLEnum** *pname* , **GLdouble \*** *params* );</span><span class="sxs-lookup"><span data-stu-id="5960a-116">**void** **glGetDoublev**(**GLenum** *pname* , **GLdouble \*** *params* );</span></span>

<span data-ttu-id="5960a-117">Le funzioni di query ottengono rispettivamente variabili di stato booleane, Integer, a virgola mobile o a precisione doppia.</span><span class="sxs-lookup"><span data-stu-id="5960a-117">Respectively, the query functions obtain Boolean, integer, floating-point, or double-precision state variables.</span></span> <span data-ttu-id="5960a-118">Il parametro *pname* è una costante simbolica che indica la variabile di stato da restituire e *params* è un puntatore a una matrice del tipo indicato in cui inserire i dati restituiti.</span><span class="sxs-lookup"><span data-stu-id="5960a-118">The *pname* parameter is a symbolic constant indicating the state variable to return, and *params* is a pointer to an array of the indicated type in which to place the returned data.</span></span> <span data-ttu-id="5960a-119">I valori possibili per *pname* sono elencati in [variabili di stato OpenGL](opengl-state-variables.md).</span><span class="sxs-lookup"><span data-stu-id="5960a-119">The possible values for *pname* are listed in [OpenGL State Variables](opengl-state-variables.md).</span></span> <span data-ttu-id="5960a-120">Se necessario, viene eseguita una conversione di tipi per restituire la variabile desiderata come tipo di dati richiesto.</span><span class="sxs-lookup"><span data-stu-id="5960a-120">A type conversion is performed if necessary to return the desired variable as the requested data type.</span></span>

<span data-ttu-id="5960a-121">Il prototipo per [**glIsEnabled**](glisenabled.md) è:</span><span class="sxs-lookup"><span data-stu-id="5960a-121">The prototype for [**glIsEnabled**](glisenabled.md) is:</span></span>

<span data-ttu-id="5960a-122">**GLboolean** **glIsEnabled**(GLEnum *Cap* );</span><span class="sxs-lookup"><span data-stu-id="5960a-122">**GLboolean** **glIsEnabled**(GLenum *cap* );</span></span>

<span data-ttu-id="5960a-123">Se la modalità specificata da *Cap* è abilitata, **glIsEnabled** restituisce GL \_ true.</span><span class="sxs-lookup"><span data-stu-id="5960a-123">If the mode specified by *cap* is enabled, **glIsEnabled** returns GL\_TRUE.</span></span> <span data-ttu-id="5960a-124">Se la modalità specificata da *Cap* è disabilitata, **glIsEnabled** restituisce GL \_ false.</span><span class="sxs-lookup"><span data-stu-id="5960a-124">If the mode specified by *cap* is disabled, **glIsEnabled** returns GL\_FALSE.</span></span> <span data-ttu-id="5960a-125">I valori possibili per *Cap* sono elencati in [variabili di stato OpenGL](opengl-state-variables.md).</span><span class="sxs-lookup"><span data-stu-id="5960a-125">The possible values for *cap* are listed in [OpenGL State Variables](opengl-state-variables.md).</span></span>

<span data-ttu-id="5960a-126">Altre funzioni specializzate restituiscono variabili di stato specifiche.</span><span class="sxs-lookup"><span data-stu-id="5960a-126">Other specialized functions return specific state variables.</span></span> <span data-ttu-id="5960a-127">Per informazioni sull'uso di queste funzioni, vedere le variabili di stato OpenGL e il *Manuale di riferimento di OpenGL*.</span><span class="sxs-lookup"><span data-stu-id="5960a-127">To find out when to use these functions, see OpenGL State Variables and the *OpenGL Reference Manual*.</span></span> <span data-ttu-id="5960a-128">Per ulteriori informazioni sulla funzionalità di gestione degli errori di OpenGL e sulla funzione **glGetError** , vedere [gestione degli errori](error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="5960a-128">For more information on OpenGL's error handling facility and the **glGetError** function, see [Error Handling](error-handling.md).</span></span>

<span data-ttu-id="5960a-129">Le funzioni che restituiscono variabili di stato specifiche sono:</span><span class="sxs-lookup"><span data-stu-id="5960a-129">The functions that return specific state variables are:</span></span>

-   [<span data-ttu-id="5960a-130">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="5960a-130">**glGetClipPlane**</span></span>](glgetclipplane.md)
-   [<span data-ttu-id="5960a-131">**glGetError**</span><span class="sxs-lookup"><span data-stu-id="5960a-131">**glGetError**</span></span>](glgeterror.md)
-   [<span data-ttu-id="5960a-132">**glGetLight**</span><span class="sxs-lookup"><span data-stu-id="5960a-132">**glGetLight**</span></span>](glgetlight.md)
-   [<span data-ttu-id="5960a-133">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="5960a-133">**glGetMap**</span></span>](glgetmap.md)
-   [<span data-ttu-id="5960a-134">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="5960a-134">**glGetMaterial**</span></span>](glgetmaterial.md)
-   [<span data-ttu-id="5960a-135">**glGetPixelMap**</span><span class="sxs-lookup"><span data-stu-id="5960a-135">**glGetPixelMap**</span></span>](glgetpixelmap.md)
-   [<span data-ttu-id="5960a-136">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="5960a-136">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md)
-   [<span data-ttu-id="5960a-137">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="5960a-137">**glGetString**</span></span>](glgetstring.md)
-   [<span data-ttu-id="5960a-138">**glGetTexEnv**</span><span class="sxs-lookup"><span data-stu-id="5960a-138">**glGetTexEnv**</span></span>](glgettexenv.md)
-   [<span data-ttu-id="5960a-139">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="5960a-139">**glGetTexGen**</span></span>](glgettexgen.md)
-   [<span data-ttu-id="5960a-140">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="5960a-140">**glGetTexImage**</span></span>](glgetteximage.md)
-   [<span data-ttu-id="5960a-141">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="5960a-141">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md)
-   [<span data-ttu-id="5960a-142">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="5960a-142">**glGetTexParameter**</span></span>](glgettexparameter.md)

 

 




