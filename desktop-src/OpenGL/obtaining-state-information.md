---
title: Acquisizione delle informazioni sullo stato
description: Acquisizione delle informazioni sullo stato
ms.assetid: 86fc8503-92b9-4b5b-8a28-4c9783983ac6
keywords:
- OpenGL, informazioni sullo stato
- OpenGL, variabili di stato
- informazioni sullo stato OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfac92233e971104fd4d343970a9ecc79496ed54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709718"
---
# <a name="obtaining-state-information"></a><span data-ttu-id="3f662-106">Acquisizione delle informazioni sullo stato</span><span class="sxs-lookup"><span data-stu-id="3f662-106">Obtaining State Information</span></span>

<span data-ttu-id="3f662-107">OpenGL gestisce molte variabili di stato che influiscono sul comportamento di molte funzioni.</span><span class="sxs-lookup"><span data-stu-id="3f662-107">OpenGL maintains many state variables that affect the behavior of many functions.</span></span> <span data-ttu-id="3f662-108">Alcune di queste variabili hanno funzioni di query specializzate.</span><span class="sxs-lookup"><span data-stu-id="3f662-108">Some of these variables have specialized query functions.</span></span>



|                                          |                                                    |                                                          |
|------------------------------------------|----------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="3f662-109">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="3f662-109">**glGetClipPlane**</span></span>](glgetclipplane.md) | [<span data-ttu-id="3f662-110">**glGetPixelMap**</span><span class="sxs-lookup"><span data-stu-id="3f662-110">**glGetPixelMap**</span></span>](glgetpixelmap.md)             | [<span data-ttu-id="3f662-111">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="3f662-111">**glGetTexImage**</span></span>](glgetteximage.md)                   |
| [<span data-ttu-id="3f662-112">**glGetLight**</span><span class="sxs-lookup"><span data-stu-id="3f662-112">**glGetLight**</span></span>](glgetlight.md)         | [<span data-ttu-id="3f662-113">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="3f662-113">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md) | [<span data-ttu-id="3f662-114">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="3f662-114">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |
| [<span data-ttu-id="3f662-115">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="3f662-115">**glGetMap**</span></span>](glgetmap.md)             | [<span data-ttu-id="3f662-116">**glGetTexEnv**</span><span class="sxs-lookup"><span data-stu-id="3f662-116">**glGetTexEnv**</span></span>](glgettexenv.md)                 | [<span data-ttu-id="3f662-117">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="3f662-117">**glGetTexParameter**</span></span>](glgettexparameter.md)           |
| [<span data-ttu-id="3f662-118">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="3f662-118">**glGetMaterial**</span></span>](glgetmaterial.md)   | [<span data-ttu-id="3f662-119">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="3f662-119">**glGetTexGen**</span></span>](glgettexgen.md)                 |                                                          |



 

<span data-ttu-id="3f662-120">Per ottenere il valore di altre variabili di stato, usare [**glGetBooleanv**](glgetbooleanv.md), [**glGetDoublev**](glgetdoublev.md), [**glGetFloatv**](glgetfloatv.md)o [**glGetIntegerv**](glgetintegerv.md), a seconda dei casi.</span><span class="sxs-lookup"><span data-stu-id="3f662-120">To obtain the value of other state variables, use [**glGetBooleanv**](glgetbooleanv.md), [**glGetDoublev**](glgetdoublev.md), [**glGetFloatv**](glgetfloatv.md), or [**glGetIntegerv**](glgetintegerv.md), as appropriate.</span></span> <span data-ttu-id="3f662-121">Per informazioni sull'uso di queste funzioni, vedere [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) .</span><span class="sxs-lookup"><span data-stu-id="3f662-121">See [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) for information about how to use these functions.</span></span> <span data-ttu-id="3f662-122">Altre funzioni di query che è possibile usare sono [**glGetError**](glgeterror.md), [**glGetString**](glgetstring.md)e [**glIsEnabled**](glisenabled.md).</span><span class="sxs-lookup"><span data-stu-id="3f662-122">Other query functions you might want to use are [**glGetError**](glgeterror.md), [**glGetString**](glgetstring.md), and [**glIsEnabled**](glisenabled.md).</span></span> <span data-ttu-id="3f662-123">Per ulteriori informazioni sulle funzioni correlate alla gestione degli errori, vedere [gestione degli errori](handling-errors.md) . Per salvare e ripristinare set di variabili di stato, usare [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="3f662-123">(See [Handling Errors](handling-errors.md) for more information about functions related to error handling.) To save and restore sets of state variables, use [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md).</span></span>

-   [<span data-ttu-id="3f662-124">Uso delle funzioni di query</span><span class="sxs-lookup"><span data-stu-id="3f662-124">Using the Query Functions</span></span>](using-the-query-functions.md)
-   [<span data-ttu-id="3f662-125">Gestione degli errori</span><span class="sxs-lookup"><span data-stu-id="3f662-125">Error Handling</span></span>](error-handling.md)
-   [<span data-ttu-id="3f662-126">Codici di errore OpenGL</span><span class="sxs-lookup"><span data-stu-id="3f662-126">OpenGL Error Codes</span></span>](opengl-error-codes.md)
-   [<span data-ttu-id="3f662-127">Salvataggio e ripristino di set di variabili di stato</span><span class="sxs-lookup"><span data-stu-id="3f662-127">Saving and Restoring Sets of State Variables</span></span>](saving-and-restoring-sets-of-state-variables.md)
-   [<span data-ttu-id="3f662-128">Variabili di stato OpenGL</span><span class="sxs-lookup"><span data-stu-id="3f662-128">OpenGL State Variables</span></span>](opengl-state-variables.md)
-   [<span data-ttu-id="3f662-129">Riferimento alle informazioni sullo stato</span><span class="sxs-lookup"><span data-stu-id="3f662-129">State Information Reference</span></span>](state-information-reference.md)

 

 




