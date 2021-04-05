---
title: Funzioni di porting che ottengono matrici e trasformazioni
description: La tabella seguente elenca le funzioni di IRIS GL che ottengono lo stato delle matrici e delle trasformazioni e dei rispettivi equivalenti OpenGL.
ms.assetid: 53546bc0-ce1d-47e0-ab5e-5d6789c6db2a
keywords:
- Porting di IRIS GL, matrici
- porting da IRIS GL, matrici
- porting in OpenGL da IRIS GL, matrici
- Porting OpenGL da IRIS GL, matrici
- matrici
- Porting, trasformazioni di IRIS GL
- porting da IRIS GL, trasformazioni
- porting in OpenGL da IRIS GL, trasformazioni
- Porting OpenGL da IRIS GL, trasformazioni
- trasformazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b32ab017e81c9875666785786b29d9c94c7fd1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955576"
---
# <a name="porting-functions-that-get-matrices-and-transformations"></a><span data-ttu-id="0d4bb-113">Funzioni di porting che ottengono matrici e trasformazioni</span><span class="sxs-lookup"><span data-stu-id="0d4bb-113">Porting Functions that Get Matrices and Transformations</span></span>

<span data-ttu-id="0d4bb-114">La tabella seguente elenca le funzioni di IRIS GL che ottengono lo stato delle matrici e delle trasformazioni e dei rispettivi equivalenti OpenGL.</span><span class="sxs-lookup"><span data-stu-id="0d4bb-114">The following table lists the IRIS GL functions that get the state of matrices and transformations and their OpenGL equivalents.</span></span>



| <span data-ttu-id="0d4bb-115">Query matrice GL IRIS</span><span class="sxs-lookup"><span data-stu-id="0d4bb-115">IRIS GL matrix query</span></span>                  | <span data-ttu-id="0d4bb-116">Query della matrice glGet OpenGL</span><span class="sxs-lookup"><span data-stu-id="0d4bb-116">OpenGL glGet matrix query</span></span>         | <span data-ttu-id="0d4bb-117">Significato</span><span class="sxs-lookup"><span data-stu-id="0d4bb-117">Meaning</span></span>                                                         |
|---------------------------------------|-----------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="0d4bb-118">**getmmode**</span><span class="sxs-lookup"><span data-stu-id="0d4bb-118">**getmmode**</span></span>                          | <span data-ttu-id="0d4bb-119">\_modalità matrice \_ GL</span><span class="sxs-lookup"><span data-stu-id="0d4bb-119">GL\_MATRIX\_MODE</span></span>                  | <span data-ttu-id="0d4bb-120">Restituisce la modalità della matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="0d4bb-120">Returns the current matrix mode.</span></span>                                |
| <span data-ttu-id="0d4bb-121">**getMatrix** in modalità **MVIEWING**</span><span class="sxs-lookup"><span data-stu-id="0d4bb-121">**getmatrix** in **MVIEWING** mode</span></span>    | <span data-ttu-id="0d4bb-122">\_matrice GL MODELVIEW \_</span><span class="sxs-lookup"><span data-stu-id="0d4bb-122">GL\_MODELVIEW\_MATRIX</span></span>             | <span data-ttu-id="0d4bb-123">Restituisce una copia della matrice di visualizzazione modello corrente.</span><span class="sxs-lookup"><span data-stu-id="0d4bb-123">Returns a copy of the current model-view matrix.</span></span>                |
| <span data-ttu-id="0d4bb-124">**getMatrix** in modalità **MPROJECTION**</span><span class="sxs-lookup"><span data-stu-id="0d4bb-124">**getmatrix** in **MPROJECTION** mode</span></span> | <span data-ttu-id="0d4bb-125">\_matrice di proiezione GL \_</span><span class="sxs-lookup"><span data-stu-id="0d4bb-125">GL\_PROJECTION\_MATRIX</span></span>            | <span data-ttu-id="0d4bb-126">Restituisce una copia della matrice di proiezione corrente.</span><span class="sxs-lookup"><span data-stu-id="0d4bb-126">Returns a copy of the current projection matrix.</span></span>                |
| <span data-ttu-id="0d4bb-127">**getMatrix** in modalità **MTEXTURE**</span><span class="sxs-lookup"><span data-stu-id="0d4bb-127">**getmatrix** in **MTEXTURE** mode</span></span>    | <span data-ttu-id="0d4bb-128">\_matrice di trama GL \_</span><span class="sxs-lookup"><span data-stu-id="0d4bb-128">GL\_TEXTURE\_MATRIX</span></span>               | <span data-ttu-id="0d4bb-129">Restituisce una copia della matrice di trama corrente.</span><span class="sxs-lookup"><span data-stu-id="0d4bb-129">Returns a copy of the current texture matrix.</span></span>                   |
| <span data-ttu-id="0d4bb-130">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="0d4bb-130">Not applicable.</span></span>                       | <span data-ttu-id="0d4bb-131">\_ \_ \_ profondità dello stack MODELVIEW max per GL \_</span><span class="sxs-lookup"><span data-stu-id="0d4bb-131">GL\_MAX\_MODELVIEW\_STACK\_DEPTH</span></span>  | <span data-ttu-id="0d4bb-132">Restituisce la profondità massima supportata dello stack della matrice di visualizzazione del modello.</span><span class="sxs-lookup"><span data-stu-id="0d4bb-132">Returns maximum supported depth of the model-view matrix stack.</span></span> |
| <span data-ttu-id="0d4bb-133">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="0d4bb-133">Not applicable.</span></span>                       | <span data-ttu-id="0d4bb-134">\_ \_ \_ profondità dello stack di proiezione max GL \_</span><span class="sxs-lookup"><span data-stu-id="0d4bb-134">GL\_MAX\_PROJECTION\_STACK\_DEPTH</span></span> | <span data-ttu-id="0d4bb-135">Restituisce la profondità massima supportata dello stack della matrice di proiezione.</span><span class="sxs-lookup"><span data-stu-id="0d4bb-135">Returns maximum supported depth of the projection matrix stack.</span></span> |
| <span data-ttu-id="0d4bb-136">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="0d4bb-136">Not applicable.</span></span>                       | <span data-ttu-id="0d4bb-137">\_ \_ \_ profondità stack trama massimo \_ GL</span><span class="sxs-lookup"><span data-stu-id="0d4bb-137">GL\_MAX\_TEXTURE\_STACK\_DEPTH</span></span>    | <span data-ttu-id="0d4bb-138">Restituisce la profondità massima supportata dello stack della matrice di trame.</span><span class="sxs-lookup"><span data-stu-id="0d4bb-138">Returns maximum supported depth of the texture matrix stack.</span></span>    |
| <span data-ttu-id="0d4bb-139">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="0d4bb-139">Not applicable.</span></span>                       | <span data-ttu-id="0d4bb-140">\_ \_ profondità dello stack MODELVIEW GL \_</span><span class="sxs-lookup"><span data-stu-id="0d4bb-140">GL\_MODELVIEW\_STACK\_DEPTH</span></span>       | <span data-ttu-id="0d4bb-141">Restituisce il numero di matrici nello stack della visualizzazione del modello.</span><span class="sxs-lookup"><span data-stu-id="0d4bb-141">Returns number of matrices on the model view stack.</span></span>             |
| <span data-ttu-id="0d4bb-142">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="0d4bb-142">Not applicable.</span></span>                       | <span data-ttu-id="0d4bb-143">\_ \_ profondità dello stack di proiezione GL \_</span><span class="sxs-lookup"><span data-stu-id="0d4bb-143">GL\_PROJECTION\_STACK\_DEPTH</span></span>      | <span data-ttu-id="0d4bb-144">Restituisce il numero di matrici nello stack di proiezione.</span><span class="sxs-lookup"><span data-stu-id="0d4bb-144">Returns number of matrices on the projection stack.</span></span>             |
| <span data-ttu-id="0d4bb-145">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="0d4bb-145">Not applicable.</span></span>                       | <span data-ttu-id="0d4bb-146">\_ \_ profondità dello stack di trama GL \_</span><span class="sxs-lookup"><span data-stu-id="0d4bb-146">GL\_TEXTURE\_STACK\_DEPTH</span></span>         | <span data-ttu-id="0d4bb-147">Restituisce il numero di matrici nello stack di trame.</span><span class="sxs-lookup"><span data-stu-id="0d4bb-147">Returns number of matrices on the texture stack.</span></span>                |



 

<span data-ttu-id="0d4bb-148">??</span><span class="sxs-lookup"><span data-stu-id="0d4bb-148">??</span></span>

 

 




