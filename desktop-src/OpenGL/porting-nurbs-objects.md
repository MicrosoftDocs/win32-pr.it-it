---
title: Porting di oggetti NURBS
description: OpenGL considera NURBS come oggetti, in modo analogo al modo in cui tratta quadriche si crea un oggetto NURBS e quindi si specifica come deve essere eseguito il rendering. La tabella seguente elenca le funzioni OpenGL GLU per la gestione degli oggetti NURBS.
ms.assetid: baddf81b-219f-44bb-aa17-37404028b258
keywords:
- Porting di IRIS GL, oggetti NURBS
- porting da IRIS GL, oggetti NURBS
- porting in OpenGL da IRIS GL, oggetti NURBS
- Porting OpenGL da IRIS GL, oggetti NURBS
- Oggetti NURBS
- NURBS (B-spline razionale non uniforme)
- B-spline razionale non uniforme (NURBS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0e56c06eea4e4a9a48f9062205277f8b999499
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396334"
---
# <a name="porting-nurbs-objects"></a><span data-ttu-id="3b74c-111">Porting di oggetti NURBS</span><span class="sxs-lookup"><span data-stu-id="3b74c-111">Porting NURBS Objects</span></span>

<span data-ttu-id="3b74c-112">OpenGL considera le NURBS come oggetti, in modo analogo al modo in cui tratta quadriche: si crea un oggetto NURBS e quindi si specifica come deve essere eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="3b74c-112">OpenGL treats NURBS as objects, similar to the way it treats quadrics: you create a NURBS object and then specify how it should be rendered.</span></span> <span data-ttu-id="3b74c-113">La tabella seguente elenca le funzioni OpenGL GLU per la gestione degli oggetti NURBS.</span><span class="sxs-lookup"><span data-stu-id="3b74c-113">The following table lists the OpenGL GLU functions for managing NURBS objects.</span></span>



| <span data-ttu-id="3b74c-114">Funzione OpenGL GLU</span><span class="sxs-lookup"><span data-stu-id="3b74c-114">OpenGL GLU function</span></span>                                      | <span data-ttu-id="3b74c-115">Significato</span><span class="sxs-lookup"><span data-stu-id="3b74c-115">Meaning</span></span>                                                        |
|----------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="3b74c-116">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="3b74c-116">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)       | <span data-ttu-id="3b74c-117">Crea un nuovo oggetto NURBS.</span><span class="sxs-lookup"><span data-stu-id="3b74c-117">Creates a new NURBS object.</span></span>                                    |
| [<span data-ttu-id="3b74c-118">**gluDeleteNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="3b74c-118">**gluDeleteNurbsRenderer**</span></span>](gludeletenurbsrenderer.md) | <span data-ttu-id="3b74c-119">Elimina un oggetto NURBS.</span><span class="sxs-lookup"><span data-stu-id="3b74c-119">Deletes a NURBS object.</span></span>                                        |
| [<span data-ttu-id="3b74c-120">*gluNurbsCallback*</span><span class="sxs-lookup"><span data-stu-id="3b74c-120">*gluNurbsCallback*</span></span>](glunurbs.md)                       | <span data-ttu-id="3b74c-121">Associa un callback a un oggetto NURBS, per la gestione degli errori.</span><span class="sxs-lookup"><span data-stu-id="3b74c-121">Associates a callback with a NURBS object, for error handling.</span></span> |



 

<span data-ttu-id="3b74c-122">Quando si esegue il porting del codice NURBS IRIS GL in OpenGL, tenere presente quanto segue:</span><span class="sxs-lookup"><span data-stu-id="3b74c-122">When porting IRIS GL NURBS code to OpenGL, keep the following points in mind:</span></span>

-   <span data-ttu-id="3b74c-123">I punti di controllo NURBS sono float, non doppi.</span><span class="sxs-lookup"><span data-stu-id="3b74c-123">NURBS control points are floats, not doubles.</span></span>
-   <span data-ttu-id="3b74c-124">Il parametro stride viene conteggiato in float, non in byte.</span><span class="sxs-lookup"><span data-stu-id="3b74c-124">The stride parameter is counted in floats, not bytes.</span></span>
-   <span data-ttu-id="3b74c-125">Se si usa l'illuminazione e non si specificano i normali, chiamare [**glEnable**](glenable.md) con GL \_ auto \_ Normal come parametro per generare automaticamente le normali.</span><span class="sxs-lookup"><span data-stu-id="3b74c-125">If you're using lighting and you're not specifying normals, call [**glEnable**](glenable.md) with GL\_AUTO\_NORMAL as the parameter to generate normals automatically.</span></span>

<span data-ttu-id="3b74c-126">??</span><span class="sxs-lookup"><span data-stu-id="3b74c-126">??</span></span>

 

 




