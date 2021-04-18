---
title: Conversione di texgen
description: Il texgen della funzione IRIS GL viene convertito in glTexGen per OpenGL.
ms.assetid: ddf398ed-37d4-4fb6-97be-20fe0564cb77
keywords:
- Porting di IRIS GL, trama
- porting da IRIS GL, trama
- porting in OpenGL da IRIS GL, trama
- Porting OpenGL da IRIS GL, trama
- trama
- Porting di IRIS GL, texgen
- porting da IRIS GL, texgen
- porting in OpenGL da IRIS GL, texgen
- Porting OpenGL da IRIS GL, texgen
- texgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07654fc35e20096ed71c3fe74ff9279214eb45c8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298813"
---
# <a name="translating-texgen"></a><span data-ttu-id="d27f7-113">Conversione di texgen</span><span class="sxs-lookup"><span data-stu-id="d27f7-113">Translating texgen</span></span>

<span data-ttu-id="d27f7-114">Il **texgen** della funzione IRIS GL viene convertito in [glTexGen](gltexgen-functions.md) per OpenGL.</span><span class="sxs-lookup"><span data-stu-id="d27f7-114">The IRIS GL function **texgen** is translated to [glTexGen](gltexgen-functions.md) for OpenGL.</span></span>

<span data-ttu-id="d27f7-115">Con IRIS GL, si chiama **texgen** due volte: una volta per impostare la modalità e l'equazione del piano contemporaneamente e una volta per abilitare la generazione della coordinata della trama.</span><span class="sxs-lookup"><span data-stu-id="d27f7-115">With IRIS GL, you call **texgen** twice: once to set the mode and plane equation simultaneously, and once to enable texture-coordinate generation.</span></span> <span data-ttu-id="d27f7-116">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="d27f7-116">For example:</span></span>


```C++
texgen(TX_S, TG_LINEAR, planeParams); 
texgen(TX_S, TG_ON, NULL);
```



<span data-ttu-id="d27f7-117">Con OpenGL si effettuano tre chiamate: due a **glTexGen** (una volta per impostare la modalità e una volta per impostare l'equazione del piano) e una a [**glEnable**](glenable.md).</span><span class="sxs-lookup"><span data-stu-id="d27f7-117">With OpenGL, you make three calls: two to **glTexGen** (once to set the mode and once to set the plane equation), and one to [**glEnable**](glenable.md).</span></span> <span data-ttu-id="d27f7-118">Ad esempio, l'equivalente OpenGL al codice IRIS GL precedente è:</span><span class="sxs-lookup"><span data-stu-id="d27f7-118">For example, the OpenGL equivalent to the IRIS GL code above is:</span></span>


```C++
glTexGen(GL_S, GLTEXTURE_GEN_MODE, modeName); 
glTextGen(GL_S, GL_OBJECT_PLANE, planeParameters); 
glEnable(GL_TEXTURE_GEN_S);
```



<span data-ttu-id="d27f7-119">La tabella seguente elenca i nomi delle coordinate di trama IRIS GL e i rispettivi equivalenti OpenGL.</span><span class="sxs-lookup"><span data-stu-id="d27f7-119">The following table lists the IRIS GL texture-coordinate names and their OpenGL equivalents.</span></span>



| <span data-ttu-id="d27f7-120">Coordinata di trama IRIS GL</span><span class="sxs-lookup"><span data-stu-id="d27f7-120">IRIS GL texture coordinate</span></span> | <span data-ttu-id="d27f7-121">Coordinata trama OpenGL</span><span class="sxs-lookup"><span data-stu-id="d27f7-121">OpenGL texture coordinate</span></span> | <span data-ttu-id="d27f7-122">argomento glEnable</span><span class="sxs-lookup"><span data-stu-id="d27f7-122">glEnable argument</span></span>   |
|----------------------------|---------------------------|---------------------|
| <span data-ttu-id="d27f7-123">TX \_ S</span><span class="sxs-lookup"><span data-stu-id="d27f7-123">TX\_S</span></span>                      | <span data-ttu-id="d27f7-124">GL \_ S</span><span class="sxs-lookup"><span data-stu-id="d27f7-124">GL\_S</span></span>                     | <span data-ttu-id="d27f7-125">\_generazione trama \_ GL \_</span><span class="sxs-lookup"><span data-stu-id="d27f7-125">GL\_TEXTURE\_GEN\_S</span></span> |
| <span data-ttu-id="d27f7-126">TX \_ T</span><span class="sxs-lookup"><span data-stu-id="d27f7-126">TX\_T</span></span>                      | <span data-ttu-id="d27f7-127">GL \_ T</span><span class="sxs-lookup"><span data-stu-id="d27f7-127">GL\_T</span></span>                     | <span data-ttu-id="d27f7-128">\_gen trama \_ GL \_ T</span><span class="sxs-lookup"><span data-stu-id="d27f7-128">GL\_TEXTURE\_GEN\_T</span></span> |
| <span data-ttu-id="d27f7-129">TX \_ R</span><span class="sxs-lookup"><span data-stu-id="d27f7-129">TX\_R</span></span>                      | <span data-ttu-id="d27f7-130">GL \_ R</span><span class="sxs-lookup"><span data-stu-id="d27f7-130">GL\_R</span></span>                     | <span data-ttu-id="d27f7-131">\_generazione trama \_ GL \_ R</span><span class="sxs-lookup"><span data-stu-id="d27f7-131">GL\_TEXTURE\_GEN\_R</span></span> |
| <span data-ttu-id="d27f7-132">TX \_ Q</span><span class="sxs-lookup"><span data-stu-id="d27f7-132">TX\_Q</span></span>                      | <span data-ttu-id="d27f7-133">GL \_ Q</span><span class="sxs-lookup"><span data-stu-id="d27f7-133">GL\_Q</span></span>                     | <span data-ttu-id="d27f7-134">\_generazione trama \_ GL \_ Q</span><span class="sxs-lookup"><span data-stu-id="d27f7-134">GL\_TEXTURE\_GEN\_Q</span></span> |



 

<span data-ttu-id="d27f7-135">La tabella seguente elenca le modalità di generazione della trama di IRIS GL e le modalità di trama OpenGL equivalenti e i nomi dei piani.</span><span class="sxs-lookup"><span data-stu-id="d27f7-135">The following table lists the IRIS GL texture-generation modes and their equivalent OpenGL texture modes and plane names.</span></span>



| <span data-ttu-id="d27f7-136">Modalità trama di IRIS GL</span><span class="sxs-lookup"><span data-stu-id="d27f7-136">IRIS GL texture mode</span></span> | <span data-ttu-id="d27f7-137">Modalità trama OpenGL</span><span class="sxs-lookup"><span data-stu-id="d27f7-137">OpenGL texture mode</span></span> | <span data-ttu-id="d27f7-138">Nome del piano OpenGL</span><span class="sxs-lookup"><span data-stu-id="d27f7-138">OpenGL plane name</span></span> |
|----------------------|---------------------|-------------------|
| <span data-ttu-id="d27f7-139">TG \_ lineare</span><span class="sxs-lookup"><span data-stu-id="d27f7-139">TG\_LINEAR</span></span>           | <span data-ttu-id="d27f7-140">\_oggetto GL \_ lineare</span><span class="sxs-lookup"><span data-stu-id="d27f7-140">GL\_OBJECT\_LINEAR</span></span>  | <span data-ttu-id="d27f7-141">\_piano oggetto \_ GL</span><span class="sxs-lookup"><span data-stu-id="d27f7-141">GL\_OBJECT\_PLANE</span></span> |
| <span data-ttu-id="d27f7-142">\_profilo TG</span><span class="sxs-lookup"><span data-stu-id="d27f7-142">TG\_CONTOUR</span></span>          | <span data-ttu-id="d27f7-143">GL \_ occhio \_ lineare</span><span class="sxs-lookup"><span data-stu-id="d27f7-143">GL\_EYE\_LINEAR</span></span>     | <span data-ttu-id="d27f7-144">\_piano d'occhio GL \_</span><span class="sxs-lookup"><span data-stu-id="d27f7-144">GL\_EYE\_PLANE</span></span>    |
| <span data-ttu-id="d27f7-145">\_SPHEREMAP TG</span><span class="sxs-lookup"><span data-stu-id="d27f7-145">TG\_SPHEREMAP</span></span>        | <span data-ttu-id="d27f7-146">\_mappa della sfera GL \_</span><span class="sxs-lookup"><span data-stu-id="d27f7-146">GL\_SPHERE\_MAP</span></span>     |                   |



 

 

 




