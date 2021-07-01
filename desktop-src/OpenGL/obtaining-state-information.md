---
title: Recupero di informazioni sullo stato
description: Recupero di informazioni sullo stato
ms.assetid: 86fc8503-92b9-4b5b-8a28-4c9783983ac6
keywords:
- OpenGL, informazioni sullo stato
- OpenGL, variabili di stato
- informazioni sullo stato OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8329fd34fc68122be8d63e4dc28756f88faf7797
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120686"
---
# <a name="obtaining-state-information"></a><span data-ttu-id="ef7ae-106">Recupero di informazioni sullo stato</span><span class="sxs-lookup"><span data-stu-id="ef7ae-106">Obtaining State Information</span></span>

<span data-ttu-id="ef7ae-107">OpenGL gestisce molte variabili di stato che influiscono sul comportamento di molte funzioni.</span><span class="sxs-lookup"><span data-stu-id="ef7ae-107">OpenGL maintains many state variables that affect the behavior of many functions.</span></span> <span data-ttu-id="ef7ae-108">Alcune di queste variabili hanno funzioni di query specializzate.</span><span class="sxs-lookup"><span data-stu-id="ef7ae-108">Some of these variables have specialized query functions.</span></span>

:::row:::
    :::column:::
        [<span data-ttu-id="ef7ae-109">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="ef7ae-109">**glGetClipPlane**</span></span>](glgetclipplane.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="ef7ae-110">**glGetPixelMap**</span><span class="sxs-lookup"><span data-stu-id="ef7ae-110">**glGetPixelMap**</span></span>](glgetpixelmap.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="ef7ae-111">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="ef7ae-111">**glGetTexImage**</span></span>](glgetteximage.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [<span data-ttu-id="ef7ae-112">**glGetLight**</span><span class="sxs-lookup"><span data-stu-id="ef7ae-112">**glGetLight**</span></span>](glgetlight.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="ef7ae-113">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="ef7ae-113">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="ef7ae-114">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="ef7ae-114">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [<span data-ttu-id="ef7ae-115">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="ef7ae-115">**glGetMap**</span></span>](glgetmap.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="ef7ae-116">**glGetTexEnv**</span><span class="sxs-lookup"><span data-stu-id="ef7ae-116">**glGetTexEnv**</span></span>](glgettexenv.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="ef7ae-117">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="ef7ae-117">**glGetTexParameter**</span></span>](glgettexparameter.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [<span data-ttu-id="ef7ae-118">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="ef7ae-118">**glGetMaterial**</span></span>](glgetmaterial.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="ef7ae-119">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="ef7ae-119">**glGetTexGen**</span></span>](glgettexgen.md)
    :::column-end:::
    :::column:::

    :::column-end:::
:::row-end:::

<span data-ttu-id="ef7ae-120">Per ottenere il valore di altre variabili di stato, usare [**glGetBooleanv**](glgetbooleanv.md), [**glGetDoublev**](glgetdoublev.md), [**glGetFloatv**](glgetfloatv.md)o [**glGetIntegerv**](glgetintegerv.md), in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="ef7ae-120">To obtain the value of other state variables, use [**glGetBooleanv**](glgetbooleanv.md), [**glGetDoublev**](glgetdoublev.md), [**glGetFloatv**](glgetfloatv.md), or [**glGetIntegerv**](glgetintegerv.md), as appropriate.</span></span> <span data-ttu-id="ef7ae-121">Per informazioni su come usare queste funzioni, vedere [**glGet.**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)</span><span class="sxs-lookup"><span data-stu-id="ef7ae-121">See [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) for information about how to use these functions.</span></span> <span data-ttu-id="ef7ae-122">Altre funzioni di query che è possibile usare sono [**glGetError**](glgeterror.md), [**glGetString**](glgetstring.md)e [**glIsEnabled**](glisenabled.md).</span><span class="sxs-lookup"><span data-stu-id="ef7ae-122">Other query functions you might want to use are [**glGetError**](glgeterror.md), [**glGetString**](glgetstring.md), and [**glIsEnabled**](glisenabled.md).</span></span> <span data-ttu-id="ef7ae-123">Per altre [informazioni sulle funzioni correlate alla gestione degli](handling-errors.md) errori, vedere Gestione degli errori. Per salvare e ripristinare set di variabili di stato, usare [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="ef7ae-123">(See [Handling Errors](handling-errors.md) for more information about functions related to error handling.) To save and restore sets of state variables, use [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md).</span></span>

-   [<span data-ttu-id="ef7ae-124">Uso delle funzioni di query</span><span class="sxs-lookup"><span data-stu-id="ef7ae-124">Using the Query Functions</span></span>](using-the-query-functions.md)
-   [<span data-ttu-id="ef7ae-125">Gestione degli errori</span><span class="sxs-lookup"><span data-stu-id="ef7ae-125">Error Handling</span></span>](error-handling.md)
-   [<span data-ttu-id="ef7ae-126">Codici di errore OpenGL</span><span class="sxs-lookup"><span data-stu-id="ef7ae-126">OpenGL Error Codes</span></span>](opengl-error-codes.md)
-   [<span data-ttu-id="ef7ae-127">Salvataggio e ripristino di set di variabili di stato</span><span class="sxs-lookup"><span data-stu-id="ef7ae-127">Saving and Restoring Sets of State Variables</span></span>](saving-and-restoring-sets-of-state-variables.md)
-   [<span data-ttu-id="ef7ae-128">Variabili di stato OpenGL</span><span class="sxs-lookup"><span data-stu-id="ef7ae-128">OpenGL State Variables</span></span>](opengl-state-variables.md)
-   [<span data-ttu-id="ef7ae-129">Informazioni di riferimento sullo stato</span><span class="sxs-lookup"><span data-stu-id="ef7ae-129">State Information Reference</span></span>](state-information-reference.md)

 

 




