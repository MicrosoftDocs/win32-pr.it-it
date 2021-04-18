---
title: funzione glEnable (GL. h)
description: Le funzioni glEnable e glDisable abilitano o disabilitano le funzionalità di OpenGL. | funzione glEnable (GL. h)
ms.assetid: cd4590dd-ae41-47c9-9861-10d72318840f
keywords:
- funzione glEnable OpenGL
topic_type:
- apiref
api_name:
- glEnable
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bc2d13233afec956c798805295c44c96df45d04
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321718"
---
# <a name="glenable-function"></a><span data-ttu-id="963ed-105">funzione glEnable</span><span class="sxs-lookup"><span data-stu-id="963ed-105">glEnable function</span></span>

<span data-ttu-id="963ed-106">Le funzioni **glEnable** e [**glDisable**](gldisable.md) abilitano o disabilitano le funzionalità di OpenGL.</span><span class="sxs-lookup"><span data-stu-id="963ed-106">The **glEnable** and [**glDisable**](gldisable.md) functions enable or disable OpenGL capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="963ed-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="963ed-107">Syntax</span></span>


```C++
void WINAPI glEnable(
   GLenum cap
);
```



## <a name="parameters"></a><span data-ttu-id="963ed-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="963ed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="963ed-109">*limite*</span><span class="sxs-lookup"><span data-stu-id="963ed-109">*cap*</span></span> 
</dt> <dd>

<span data-ttu-id="963ed-110">Costante simbolica che indica una funzionalità OpenGL.</span><span class="sxs-lookup"><span data-stu-id="963ed-110">A symbolic constant indicating an OpenGL capability.</span></span>

<span data-ttu-id="963ed-111">Per informazioni sui valori che possono essere accettati da *Cap* , vedere la sezione Osservazioni riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="963ed-111">For discussion of the values *cap* can take, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="963ed-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="963ed-112">Return value</span></span>

<span data-ttu-id="963ed-113">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="963ed-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="963ed-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="963ed-114">Error codes</span></span>

<span data-ttu-id="963ed-115">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="963ed-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="963ed-116">Nome</span><span class="sxs-lookup"><span data-stu-id="963ed-116">Name</span></span>                                                                                                  | <span data-ttu-id="963ed-117">Significato</span><span class="sxs-lookup"><span data-stu-id="963ed-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="963ed-118"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="963ed-118"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="963ed-119">*Cap* non è uno dei valori elencati nella sezione Osservazioni precedente.</span><span class="sxs-lookup"><span data-stu-id="963ed-119">*cap* was not one of the values listed in the preceding Remarks section.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="963ed-120"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="963ed-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="963ed-121">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="963ed-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="963ed-122">Remarks</span></span>

<span data-ttu-id="963ed-123">Le funzioni **glEnable** e **glDisable** abilitano e disabilitano diverse funzionalità grafiche OpenGL.</span><span class="sxs-lookup"><span data-stu-id="963ed-123">The **glEnable** and **glDisable** functions enable and disable various OpenGL graphics capabilities.</span></span> <span data-ttu-id="963ed-124">Usare [**glIsEnabled**](glisenabled.md) o [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) per determinare l'impostazione corrente di tutte le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="963ed-124">Use [**glIsEnabled**](glisenabled.md) or [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) to determine the current setting of any capability.</span></span>

<span data-ttu-id="963ed-125">Sia **glEnable** che **glDisable** accettano un solo argomento, *Cap*, che può assumere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="963ed-125">Both **glEnable** and **glDisable** take a single argument, *cap*, which can assume one of the following values:</span></span>



| <span data-ttu-id="963ed-126">Valore</span><span class="sxs-lookup"><span data-stu-id="963ed-126">Value</span></span>                       | <span data-ttu-id="963ed-127">Significato</span><span class="sxs-lookup"><span data-stu-id="963ed-127">Meaning</span></span>                                                                                                                                                                                                                                                     |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="963ed-128">\_test GL Alpha \_</span><span class="sxs-lookup"><span data-stu-id="963ed-128">GL\_ALPHA\_TEST</span></span>             | <span data-ttu-id="963ed-129">Se abilitata, eseguire il test alfa.</span><span class="sxs-lookup"><span data-stu-id="963ed-129">If enabled, do alpha testing.</span></span> <span data-ttu-id="963ed-130">Vedere [**glAlphaFunc**](glalphafunc.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-130">See [**glAlphaFunc**](glalphafunc.md).</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="963ed-131">GL \_ auto \_ normale</span><span class="sxs-lookup"><span data-stu-id="963ed-131">GL\_AUTO\_NORMAL</span></span>            | <span data-ttu-id="963ed-132">Se abilitata, calcola i vettori normali della superficie di calcolo in modo analitico quando i \_ vertici di GL map2 \_ Vertex \_ 3 o GL \_ map2 \_ sono stati \_ generati.</span><span class="sxs-lookup"><span data-stu-id="963ed-132">If enabled, compute surface normal vectors analytically when either GL\_MAP2\_VERTEX\_3 or GL\_MAP2\_VERTEX\_4 has generated vertices.</span></span> <span data-ttu-id="963ed-133">Vedere [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-133">See [**glMap2**](glmap2.md).</span></span>                                                                                        |
| <span data-ttu-id="963ed-134">\_Blend GL</span><span class="sxs-lookup"><span data-stu-id="963ed-134">GL\_BLEND</span></span>                   | <span data-ttu-id="963ed-135">Se abilitata, combina i valori dei colori RGBA in ingresso con i valori nei buffer dei colori.</span><span class="sxs-lookup"><span data-stu-id="963ed-135">If enabled, blend the incoming RGBA color values with the values in the color buffers.</span></span> <span data-ttu-id="963ed-136">Vedere [**glBlendFunc**](glblendfunc.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-136">See [**glBlendFunc**](glblendfunc.md).</span></span>                                                                                                                              |
| <span data-ttu-id="963ed-137">\_Piano di ritaglio GL \_ *i*</span><span class="sxs-lookup"><span data-stu-id="963ed-137">GL\_CLIP\_PLANE *i*</span></span>          | <span data-ttu-id="963ed-138">Se abilitata, ritagliare la geometria rispetto *al piano di* ritaglio definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="963ed-138">If enabled, clip geometry against user-defined clipping plane *i*.</span></span> <span data-ttu-id="963ed-139">Vedere [**glClipPlane**](glclipplane.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-139">See [**glClipPlane**](glclipplane.md).</span></span>                                                                                                                                                  |
| <span data-ttu-id="963ed-140">\_operazione di \_ logica \_ colori GL</span><span class="sxs-lookup"><span data-stu-id="963ed-140">GL\_COLOR\_LOGIC\_OP</span></span>        | <span data-ttu-id="963ed-141">Se abilitata, applicare l'operazione logica corrente ai valori del buffer dei colori e del colore RGBA in ingresso.</span><span class="sxs-lookup"><span data-stu-id="963ed-141">If enabled, apply the current logical operation to the incoming RGBA color and color buffer values.</span></span> <span data-ttu-id="963ed-142">Vedere [**glLogicOp**](gllogicop.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-142">See [**glLogicOp**](gllogicop.md).</span></span>                                                                                                                     |
| <span data-ttu-id="963ed-143">\_materiale colore \_ GL</span><span class="sxs-lookup"><span data-stu-id="963ed-143">GL\_COLOR\_MATERIAL</span></span>         | <span data-ttu-id="963ed-144">Se abilitata, avere uno o più parametri Material tenere traccia del colore corrente.</span><span class="sxs-lookup"><span data-stu-id="963ed-144">If enabled, have one or more material parameters track the current color.</span></span> <span data-ttu-id="963ed-145">Vedere [**glColorMaterial**](glcolormaterial.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-145">See [**glColorMaterial**](glcolormaterial.md).</span></span>                                                                                                                                   |
| <span data-ttu-id="963ed-146">superficie di selezione GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="963ed-146">GL\_CULL\_FACE</span></span>              | <span data-ttu-id="963ed-147">Se abilitata, i poligoni vengono raccolti in base al relativo avvolgimento nelle coordinate della finestra.</span><span class="sxs-lookup"><span data-stu-id="963ed-147">If enabled, cull polygons based on their winding in window coordinates.</span></span> <span data-ttu-id="963ed-148">Vedere [**glCullFace**](glcullface.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-148">See [**glCullFace**](glcullface.md).</span></span>                                                                                                                                               |
| <span data-ttu-id="963ed-149">\_test di profondità GL \_</span><span class="sxs-lookup"><span data-stu-id="963ed-149">GL\_DEPTH\_TEST</span></span>             | <span data-ttu-id="963ed-150">Se abilitata, eseguire confronti di profondità e aggiornare il buffer di profondità.</span><span class="sxs-lookup"><span data-stu-id="963ed-150">If enabled, do depth comparisons and update the depth buffer.</span></span> <span data-ttu-id="963ed-151">Vedere [**glDepthFunc**](gldepthfunc.md) e [**glDepthRange**](gldepthrange.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-151">See [**glDepthFunc**](gldepthfunc.md) and [**glDepthRange**](gldepthrange.md).</span></span>                                                                                                              |
| <span data-ttu-id="963ed-152">\_dithering GL</span><span class="sxs-lookup"><span data-stu-id="963ed-152">GL\_DITHER</span></span>                  | <span data-ttu-id="963ed-153">Se abilitata, i componenti di colore o gli indici di dithering prima che vengano scritti nel buffer dei colori.</span><span class="sxs-lookup"><span data-stu-id="963ed-153">If enabled, dither color components or indexes before they are written to the color buffer.</span></span>                                                                                                                                                                 |
| <span data-ttu-id="963ed-154">\_nebbia GL</span><span class="sxs-lookup"><span data-stu-id="963ed-154">GL\_FOG</span></span>                     | <span data-ttu-id="963ed-155">Se abilitata, fondere un colore di nebbia al colore di post-texturing.</span><span class="sxs-lookup"><span data-stu-id="963ed-155">If enabled, blend a fog color into the post-texturing color.</span></span> <span data-ttu-id="963ed-156">Vedere [**glFog**](glfog.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-156">See [**glFog**](glfog.md).</span></span>                                                                                                                                                                    |
| <span data-ttu-id="963ed-157">\_ \_ operazione logica indice \_ GL</span><span class="sxs-lookup"><span data-stu-id="963ed-157">GL\_INDEX\_LOGIC\_OP</span></span>        | <span data-ttu-id="963ed-158">Se abilitata, applicare l'operazione logica corrente agli indici indici in ingresso e al buffer dei colori.</span><span class="sxs-lookup"><span data-stu-id="963ed-158">If enabled, apply the current logical operation to the incoming index and color buffer indices.</span></span> <span data-ttu-id="963ed-159">Vedere [**glLogicOp**](gllogicop.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-159">See [**glLogicOp**](gllogicop.md).</span></span>                                                                                                                         |
| <span data-ttu-id="963ed-160">GL \_ Light *i*</span><span class="sxs-lookup"><span data-stu-id="963ed-160">GL\_LIGHT *i*</span></span>                | <span data-ttu-id="963ed-161">Se abilitata, includere la luce *i* nella valutazione dell'equazione di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="963ed-161">If enabled, include light *i* in the evaluation of the lighting equation.</span></span> <span data-ttu-id="963ed-162">Vedere [**glLightModel**](gllightmodel-functions.md) e [**glLight**](gllight-functions.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-162">See [**glLightModel**](gllightmodel-functions.md) and [**glLight**](gllight-functions.md).</span></span>                                                                                      |
| <span data-ttu-id="963ed-163">\_illuminazione GL</span><span class="sxs-lookup"><span data-stu-id="963ed-163">GL\_LIGHTING</span></span>                | <span data-ttu-id="963ed-164">Se abilitata, usare i parametri di illuminazione correnti per calcolare il colore o l'indice del vertice.</span><span class="sxs-lookup"><span data-stu-id="963ed-164">If enabled, use the current lighting parameters to compute the vertex color or index.</span></span> <span data-ttu-id="963ed-165">Se disabilitato, associare il colore o l'indice corrente a ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="963ed-165">If disabled, associate the current color or index with each vertex.</span></span> <span data-ttu-id="963ed-166">Vedere [**glMaterial**](glmaterial-functions.md), **glLightModel** e **glLight**.</span><span class="sxs-lookup"><span data-stu-id="963ed-166">See [**glMaterial**](glmaterial-functions.md), **glLightModel**, and **glLight**.</span></span>                |
| <span data-ttu-id="963ed-167">\_linea GL \_ smussata</span><span class="sxs-lookup"><span data-stu-id="963ed-167">GL\_LINE\_SMOOTH</span></span>            | <span data-ttu-id="963ed-168">Se abilitata, creare linee con filtri corretti.</span><span class="sxs-lookup"><span data-stu-id="963ed-168">If enabled, draw lines with correct filtering.</span></span> <span data-ttu-id="963ed-169">Se è disabilitata, creare linee con alias.</span><span class="sxs-lookup"><span data-stu-id="963ed-169">If disabled, draw aliased lines.</span></span> <span data-ttu-id="963ed-170">Vedere [**glLineWidth**](gllinewidth.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-170">See [**glLineWidth**](gllinewidth.md).</span></span>                                                                                                                                     |
| <span data-ttu-id="963ed-171">\_stipple linea \_ GL</span><span class="sxs-lookup"><span data-stu-id="963ed-171">GL\_LINE\_STIPPLE</span></span>           | <span data-ttu-id="963ed-172">Se abilitata, usare il modello stipple di riga corrente quando si disegnano le linee.</span><span class="sxs-lookup"><span data-stu-id="963ed-172">If enabled, use the current line stipple pattern when drawing lines.</span></span> <span data-ttu-id="963ed-173">Vedere [**glLineStipple**](gllinestipple.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-173">See [**glLineStipple**](gllinestipple.md).</span></span>                                                                                                                                            |
| <span data-ttu-id="963ed-174">\_op logica \_ GL</span><span class="sxs-lookup"><span data-stu-id="963ed-174">GL\_LOGIC\_OP</span></span>               | <span data-ttu-id="963ed-175">Se abilitata, applicare l'operazione logica attualmente selezionata agli indici del buffer di colore e in ingresso.</span><span class="sxs-lookup"><span data-stu-id="963ed-175">If enabled, apply the currently selected logical operation to the incoming and color-buffer indexes.</span></span> <span data-ttu-id="963ed-176">Vedere [**glLogicOp**](gllogicop.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-176">See [**glLogicOp**](gllogicop.md).</span></span>                                                                                                                    |
| <span data-ttu-id="963ed-177">\_Mappa1 \_ colore \_ 4 GL</span><span class="sxs-lookup"><span data-stu-id="963ed-177">GL\_MAP1\_COLOR\_4</span></span>          | <span data-ttu-id="963ed-178">Se abilitata, le chiamate a [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)e [**glEvalPoint1**](glevalpoint.md) generano valori RGBA.</span><span class="sxs-lookup"><span data-stu-id="963ed-178">If enabled, calls to [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md), and [**glEvalPoint1**](glevalpoint.md) generate RGBA values.</span></span> <span data-ttu-id="963ed-179">Vedere anche [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-179">See also [**glMap1**](glmap1.md).</span></span>                                           |
| <span data-ttu-id="963ed-180">\_Indice MAPPA1 \_ GL</span><span class="sxs-lookup"><span data-stu-id="963ed-180">GL\_MAP1\_INDEX</span></span>             | <span data-ttu-id="963ed-181">Se abilitata, le chiamate a **glEvalCoord1**, **glEvalMesh1** e **glEvalPoint1** generano indici colori.</span><span class="sxs-lookup"><span data-stu-id="963ed-181">If enabled, calls to **glEvalCoord1**, **glEvalMesh1**, and **glEvalPoint1** generate color indexes.</span></span> <span data-ttu-id="963ed-182">Vedere anche **glMap1**.</span><span class="sxs-lookup"><span data-stu-id="963ed-182">See also **glMap1**.</span></span>                                                                                                                                   |
| <span data-ttu-id="963ed-183">\_Normale MAPPA1 \_ GL</span><span class="sxs-lookup"><span data-stu-id="963ed-183">GL\_MAP1\_NORMAL</span></span>            | <span data-ttu-id="963ed-184">Se abilitata, le chiamate a [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)e [**glEvalPoint1**](glevalpoint.md) generano normali.</span><span class="sxs-lookup"><span data-stu-id="963ed-184">If enabled, calls to [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md), and [**glEvalPoint1**](glevalpoint.md) generate normals.</span></span> <span data-ttu-id="963ed-185">Vedere anche [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-185">See also [**glMap1**](glmap1.md).</span></span>                                               |
| <span data-ttu-id="963ed-186">\_Trama GL \_ Mappa1 \_ Coord \_ 1</span><span class="sxs-lookup"><span data-stu-id="963ed-186">GL\_MAP1\_TEXTURE\_COORD\_1</span></span> | <span data-ttu-id="963ed-187">Se abilitata, le chiamate a **glEvalCoord1**, **glEvalMesh1** e **glEvalPoint1** generano le coordinate di trama *s* .</span><span class="sxs-lookup"><span data-stu-id="963ed-187">If enabled, calls to **glEvalCoord1**, **glEvalMesh1**, and **glEvalPoint1** generate *s* texture coordinates.</span></span> <span data-ttu-id="963ed-188">Vedere anche **glMap1**.</span><span class="sxs-lookup"><span data-stu-id="963ed-188">See also **glMap1**.</span></span>                                                                                                                         |
| <span data-ttu-id="963ed-189">\_ \_ Coord trama GL \_ Mappa1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="963ed-189">GL\_MAP1\_TEXTURE\_COORD\_2</span></span> | <span data-ttu-id="963ed-190">Se abilitata, le chiamate a [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)e [**glEvalPoint1**](glevalpoint.md) generano le coordinate di trama *s* e *t* .</span><span class="sxs-lookup"><span data-stu-id="963ed-190">If enabled, calls to [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md), and [**glEvalPoint1**](glevalpoint.md) generate *s* and *t* texture coordinates.</span></span> <span data-ttu-id="963ed-191">Vedere anche [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-191">See also [**glMap1**](glmap1.md).</span></span>                       |
| <span data-ttu-id="963ed-192">\_Trama GL \_ Mappa1 \_ Coord \_ 3</span><span class="sxs-lookup"><span data-stu-id="963ed-192">GL\_MAP1\_TEXTURE\_COORD\_3</span></span> | <span data-ttu-id="963ed-193">Se abilitata, le chiamate a **glEvalCoord1**, **glEvalMesh1** e **glEvalPoint1** generano le coordinate di trama *s*, *t* e *r* .</span><span class="sxs-lookup"><span data-stu-id="963ed-193">If enabled, calls to **glEvalCoord1**, **glEvalMesh1**, and **glEvalPoint1** generate *s*, *t*, and *r* texture coordinates.</span></span> <span data-ttu-id="963ed-194">Vedere anche **glMap1**.</span><span class="sxs-lookup"><span data-stu-id="963ed-194">See also **glMap1**.</span></span>                                                                                                           |
| <span data-ttu-id="963ed-195">\_Trama GL \_ Mappa1 \_ Coord \_ 4</span><span class="sxs-lookup"><span data-stu-id="963ed-195">GL\_MAP1\_TEXTURE\_COORD\_4</span></span> | <span data-ttu-id="963ed-196">Se abilitata, le chiamate a [glEvalCoord1](glevalcoord-functions.md), [glEvalMesh1](glevalmesh-functions.md)e [**glEvalPoint1**](glevalpoint.md) generano le coordinate di trama *s*, *t*, *r* e *q* .</span><span class="sxs-lookup"><span data-stu-id="963ed-196">If enabled, calls to [glEvalCoord1](glevalcoord-functions.md), [glEvalMesh1](glevalmesh-functions.md), and [**glEvalPoint1**](glevalpoint.md) generate *s*, *t*, *r*, and *q* texture coordinates.</span></span> <span data-ttu-id="963ed-197">Vedere anche [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-197">See also [**glMap1**](glmap1.md).</span></span>                    |
| <span data-ttu-id="963ed-198">\_Vertice GL \_ Mappa1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="963ed-198">GL\_MAP1\_VERTEX\_3</span></span>         | <span data-ttu-id="963ed-199">Se abilitata, le chiamate a **glEvalCoord1**, **glEvalMesh1** e **glEvalPoint1** generano coordinate di vertice *x*, *y* e *z* .</span><span class="sxs-lookup"><span data-stu-id="963ed-199">If enabled, calls to **glEvalCoord1**, **glEvalMesh1**, and **glEvalPoint1** generate *x*, *y*, and *z* vertex coordinates.</span></span> <span data-ttu-id="963ed-200">Vedere anche **glMap1**.</span><span class="sxs-lookup"><span data-stu-id="963ed-200">See also **glMap1**.</span></span>                                                                                                            |
| <span data-ttu-id="963ed-201">\_Mappa1 \_ Vertex \_ 4</span><span class="sxs-lookup"><span data-stu-id="963ed-201">GL\_MAP1\_VERTEX\_4</span></span>         | <span data-ttu-id="963ed-202">Se abilitate, le chiamate a [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)e [**glEvalPoint1**](glevalpoint.md) generano coordinate di vertice *x*, *y*, *z* e *w* omogenee.</span><span class="sxs-lookup"><span data-stu-id="963ed-202">If enabled, calls to [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md), and [**glEvalPoint1**](glevalpoint.md) generate homogeneous *x*, *y*, *z*, and *w* vertex coordinates.</span></span> <span data-ttu-id="963ed-203">Vedere anche [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-203">See also [**glMap1**](glmap1.md).</span></span> |
| <span data-ttu-id="963ed-204">\_Map2 \_ colore \_ 4 GL</span><span class="sxs-lookup"><span data-stu-id="963ed-204">GL\_MAP2\_COLOR\_4</span></span>          | <span data-ttu-id="963ed-205">Se abilitata, le chiamate a [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)e [**glEvalPoint2**](glevalpoint.md) generano valori RGBA.</span><span class="sxs-lookup"><span data-stu-id="963ed-205">If enabled, calls to [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md), and [**glEvalPoint2**](glevalpoint.md) generate RGBA values.</span></span> <span data-ttu-id="963ed-206">Vedere anche [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-206">See also [**glMap2**](glmap2.md).</span></span>                                           |
| <span data-ttu-id="963ed-207">\_Indice map2 \_ GL</span><span class="sxs-lookup"><span data-stu-id="963ed-207">GL\_MAP2\_INDEX</span></span>             | <span data-ttu-id="963ed-208">Se abilitata, le chiamate a **glEvalCoord2**, **glEvalMesh2** e **glEvalPoint2** generano indici colori.</span><span class="sxs-lookup"><span data-stu-id="963ed-208">If enabled, calls to **glEvalCoord2**, **glEvalMesh2**, and **glEvalPoint2** generate color indexes.</span></span> <span data-ttu-id="963ed-209">Vedere anche **glMap2**.</span><span class="sxs-lookup"><span data-stu-id="963ed-209">See also **glMap2**.</span></span>                                                                                                                                   |
| <span data-ttu-id="963ed-210">\_Normale map2 \_ GL</span><span class="sxs-lookup"><span data-stu-id="963ed-210">GL\_MAP2\_NORMAL</span></span>            | <span data-ttu-id="963ed-211">Se abilitata, le chiamate a [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)e [**glEvalPoint2**](glevalpoint.md) generano normali.</span><span class="sxs-lookup"><span data-stu-id="963ed-211">If enabled, calls to [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md), and [**glEvalPoint2**](glevalpoint.md) generate normals.</span></span> <span data-ttu-id="963ed-212">Vedere anche [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-212">See also [**glMap2**](glmap2.md).</span></span>                                               |
| <span data-ttu-id="963ed-213">\_Trama GL \_ map2 \_ Coord \_ 1</span><span class="sxs-lookup"><span data-stu-id="963ed-213">GL\_MAP2\_TEXTURE\_COORD\_1</span></span> | <span data-ttu-id="963ed-214">Se abilitata, le chiamate a **glEvalCoord2**, **glEvalMesh2** e **glEvalPoint2** generano le coordinate di trama *s* .</span><span class="sxs-lookup"><span data-stu-id="963ed-214">If enabled, calls to **glEvalCoord2**, **glEvalMesh2**, and **glEvalPoint2** generate *s* texture coordinates.</span></span> <span data-ttu-id="963ed-215">Vedere anche **glMap2**.</span><span class="sxs-lookup"><span data-stu-id="963ed-215">See also **glMap2**.</span></span>                                                                                                                         |
| <span data-ttu-id="963ed-216">\_ \_ Coord trama GL \_ map2 \_ 2</span><span class="sxs-lookup"><span data-stu-id="963ed-216">GL\_MAP2\_TEXTURE\_COORD\_2</span></span> | <span data-ttu-id="963ed-217">Se abilitata, le chiamate a [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)e [**glEvalPoint2**](glevalpoint.md) generano le coordinate di trama *s* e *t* .</span><span class="sxs-lookup"><span data-stu-id="963ed-217">If enabled, calls to [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md), and [**glEvalPoint2**](glevalpoint.md) generate *s* and *t* texture coordinates.</span></span> <span data-ttu-id="963ed-218">Vedere anche [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-218">See also [**glMap2**](glmap2.md).</span></span>                       |
| <span data-ttu-id="963ed-219">\_Trama GL \_ map2 \_ Coord \_ 3</span><span class="sxs-lookup"><span data-stu-id="963ed-219">GL\_MAP2\_TEXTURE\_COORD\_3</span></span> | <span data-ttu-id="963ed-220">Se abilitata, le chiamate a **glEvalCoord2**, **glEvalMesh2** e **glEvalPoint2** generano le coordinate di trama *s*, *t* e *r* .</span><span class="sxs-lookup"><span data-stu-id="963ed-220">If enabled, calls to **glEvalCoord2**, **glEvalMesh2**, and **glEvalPoint2** generate *s*, *t*, and *r* texture coordinates.</span></span> <span data-ttu-id="963ed-221">Vedere anche **glMap2**.</span><span class="sxs-lookup"><span data-stu-id="963ed-221">See also **glMap2**.</span></span>                                                                                                           |
| <span data-ttu-id="963ed-222">\_Trama GL \_ map2 \_ Coord \_ 4</span><span class="sxs-lookup"><span data-stu-id="963ed-222">GL\_MAP2\_TEXTURE\_COORD\_4</span></span> | <span data-ttu-id="963ed-223">Se abilitata, le chiamate a [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)e [**glEvalPoint2**](glevalpoint.md) generano le coordinate di trama *s*, *t*, *r* e *q* .</span><span class="sxs-lookup"><span data-stu-id="963ed-223">If enabled, calls to [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md), and [**glEvalPoint2**](glevalpoint.md) generate *s*, *t*, *r*, and *q* texture coordinates.</span></span> <span data-ttu-id="963ed-224">Vedere anche [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-224">See also [**glMap2**](glmap2.md).</span></span>            |
| <span data-ttu-id="963ed-225">\_Vertice GL \_ map2 \_ 3</span><span class="sxs-lookup"><span data-stu-id="963ed-225">GL\_MAP2\_VERTEX\_3</span></span>         | <span data-ttu-id="963ed-226">Se abilitata, le chiamate a **glEvalCoord2**, **glEvalMesh2** e **glEvalPoint2** generano coordinate di vertice *x*, *y* e *z* .</span><span class="sxs-lookup"><span data-stu-id="963ed-226">If enabled, calls to **glEvalCoord2**, **glEvalMesh2**, and **glEvalPoint2** generate *x*, *y*, and *z* vertex coordinates.</span></span> <span data-ttu-id="963ed-227">Vedere anche **glMap2**.</span><span class="sxs-lookup"><span data-stu-id="963ed-227">See also **glMap2**.</span></span>                                                                                                            |
| <span data-ttu-id="963ed-228">\_Map2 \_ Vertex \_ 4</span><span class="sxs-lookup"><span data-stu-id="963ed-228">GL\_MAP2\_VERTEX\_4</span></span>         | <span data-ttu-id="963ed-229">Se abilitate, le chiamate a [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)e [**glEvalPoint2**](glevalpoint.md) generano coordinate di vertice *x*, *y*, *z* e *w* omogenee.</span><span class="sxs-lookup"><span data-stu-id="963ed-229">If enabled, calls to [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md), and [**glEvalPoint2**](glevalpoint.md) generate homogeneous *x*, *y*, *z*, and *w* vertex coordinates.</span></span> <span data-ttu-id="963ed-230">Vedere anche [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-230">See also [**glMap2**](glmap2.md).</span></span> |
| <span data-ttu-id="963ed-231">\_normalizzare GL</span><span class="sxs-lookup"><span data-stu-id="963ed-231">GL\_NORMALIZE</span></span>               | <span data-ttu-id="963ed-232">Se abilitata, i vettori normali specificati con **glNormal** vengono ridimensionati alla lunghezza dell'unità dopo la trasformazione.</span><span class="sxs-lookup"><span data-stu-id="963ed-232">If enabled, normal vectors specified with **glNormal** are scaled to unit length after transformation.</span></span> <span data-ttu-id="963ed-233">Vedere [**glNormal**](glnormal-functions.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-233">See [**glNormal**](glnormal-functions.md).</span></span>                                                                                                          |
| <span data-ttu-id="963ed-234">\_punto GL \_ smussato</span><span class="sxs-lookup"><span data-stu-id="963ed-234">GL\_POINT\_SMOOTH</span></span>           | <span data-ttu-id="963ed-235">Se abilitata, creare punti con filtro appropriato.</span><span class="sxs-lookup"><span data-stu-id="963ed-235">If enabled, draw points with proper filtering.</span></span> <span data-ttu-id="963ed-236">Se disabilitato, creare punti con alias.</span><span class="sxs-lookup"><span data-stu-id="963ed-236">If disabled, draw aliased points.</span></span> <span data-ttu-id="963ed-237">Vedere [**glPointSize**](glpointsize.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-237">See [**glPointSize**](glpointsize.md).</span></span>                                                                                                                                    |
| <span data-ttu-id="963ed-238">\_riempimento offset poligono GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="963ed-238">GL\_POLYGON\_OFFSET\_FILL</span></span>   | <span data-ttu-id="963ed-239">Se abilitata e se viene eseguito il rendering del poligono in \_ modalità di riempimento GL, viene aggiunto un offset ai valori di profondità dei frammenti di un poligono prima che venga eseguito il confronto di profondità.</span><span class="sxs-lookup"><span data-stu-id="963ed-239">If enabled, and if the polygon is rendered in GL\_FILL mode, an offset is added to depth values of a polygon's fragments before the depth comparison is performed.</span></span> <span data-ttu-id="963ed-240">Vedere [**glPolygonOffset**](glpolygonoffset.md)**.**</span><span class="sxs-lookup"><span data-stu-id="963ed-240">See [**glPolygonOffset**](glpolygonoffset.md)**.**</span></span>                                      |
| <span data-ttu-id="963ed-241">\_linea offset poligono GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="963ed-241">GL\_POLYGON\_OFFSET\_LINE</span></span>   | <span data-ttu-id="963ed-242">Se abilitata e se viene eseguito il rendering del poligono in \_ modalità linea GL, viene aggiunto un offset ai valori di profondità dei frammenti di un poligono prima che venga eseguito il confronto di profondità.</span><span class="sxs-lookup"><span data-stu-id="963ed-242">If enabled, and if the polygon is rendered in GL\_LINE mode, an offset is added to depth values of a polygon's fragments before the depth comparison is performed.</span></span> <span data-ttu-id="963ed-243">Vedere **glPolygonOffset**.</span><span class="sxs-lookup"><span data-stu-id="963ed-243">See **glPolygonOffset**.</span></span>                                                                 |
| <span data-ttu-id="963ed-244">\_punto di offset del poligono GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="963ed-244">GL\_POLYGON\_OFFSET\_POINT</span></span>  | <span data-ttu-id="963ed-245">Se abilitata, viene aggiunto un offset ai valori di profondità dei frammenti di un poligono prima che venga eseguito il confronto di profondità, se il poligono viene sottoposto a rendering in \_ modalità punto GL.</span><span class="sxs-lookup"><span data-stu-id="963ed-245">If enabled, an offset is added to depth values of a polygon's fragments before the depth comparison is performed, if the polygon is rendered in GL\_POINT mode.</span></span> <span data-ttu-id="963ed-246">Vedere [**glPolygonOffset**](glpolygonoffset.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-246">See [**glPolygonOffset**](glpolygonoffset.md).</span></span>                                             |
| <span data-ttu-id="963ed-247">\_poligono GL \_ smussato</span><span class="sxs-lookup"><span data-stu-id="963ed-247">GL\_POLYGON\_SMOOTH</span></span>         | <span data-ttu-id="963ed-248">Se abilitata, creare poligoni con filtri appropriati.</span><span class="sxs-lookup"><span data-stu-id="963ed-248">If enabled, draw polygons with proper filtering.</span></span> <span data-ttu-id="963ed-249">Se disabilitato, creare poligoni con alias.</span><span class="sxs-lookup"><span data-stu-id="963ed-249">If disabled, draw aliased polygons.</span></span> <span data-ttu-id="963ed-250">Vedere [**glPolygonMode**](glpolygonmode.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-250">See [**glPolygonMode**](glpolygonmode.md).</span></span>                                                                                                                            |
| <span data-ttu-id="963ed-251">\_stipple poligono GL \_</span><span class="sxs-lookup"><span data-stu-id="963ed-251">GL\_POLYGON\_STIPPLE</span></span>        | <span data-ttu-id="963ed-252">Se abilitata, usare il modello stipple del poligono corrente durante il rendering dei poligoni.</span><span class="sxs-lookup"><span data-stu-id="963ed-252">If enabled, use the current polygon stipple pattern when rendering polygons.</span></span> <span data-ttu-id="963ed-253">Vedere [**glPolygonStipple**](glpolygonstipple.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-253">See [**glPolygonStipple**](glpolygonstipple.md).</span></span>                                                                                                                              |
| <span data-ttu-id="963ed-254">\_test della forbice GL \_</span><span class="sxs-lookup"><span data-stu-id="963ed-254">GL\_SCISSOR\_TEST</span></span>           | <span data-ttu-id="963ed-255">Se abilitata, eliminare i frammenti esterni al rettangolo a forbice.</span><span class="sxs-lookup"><span data-stu-id="963ed-255">If enabled, discard fragments that are outside the scissor rectangle.</span></span> <span data-ttu-id="963ed-256">Vedere [**glScissor**](glscissor.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-256">See [**glScissor**](glscissor.md).</span></span>                                                                                                                                                   |
| <span data-ttu-id="963ed-257">\_test stencil \_ GL</span><span class="sxs-lookup"><span data-stu-id="963ed-257">GL\_STENCIL\_TEST</span></span>           | <span data-ttu-id="963ed-258">Se abilitata, eseguire il test dello stencil e aggiornare il buffer dello stencil.</span><span class="sxs-lookup"><span data-stu-id="963ed-258">If enabled, do stencil testing and update the stencil buffer.</span></span> <span data-ttu-id="963ed-259">Vedere [**glStencilFunc**](glstencilfunc.md) e [**glStencilOp**](glstencilop.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-259">See [**glStencilFunc**](glstencilfunc.md) and [**glStencilOp**](glstencilop.md).</span></span>                                                                                                            |
| <span data-ttu-id="963ed-260">\_Trama GL \_ 1D</span><span class="sxs-lookup"><span data-stu-id="963ed-260">GL\_TEXTURE\_1D</span></span>             | <span data-ttu-id="963ed-261">Se abilitata, viene eseguita la texturing unidimensionale (a meno che non sia abilitata anche la texturing bidimensionale).</span><span class="sxs-lookup"><span data-stu-id="963ed-261">If enabled, one-dimensional texturing is performed (unless two-dimensional texturing is also enabled).</span></span> <span data-ttu-id="963ed-262">Vedere [**glTexImage1D**](glteximage1d.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-262">See [**glTexImage1D**](glteximage1d.md).</span></span>                                                                                                            |
| <span data-ttu-id="963ed-263">\_Trama GL \_ 2D</span><span class="sxs-lookup"><span data-stu-id="963ed-263">GL\_TEXTURE\_2D</span></span>             | <span data-ttu-id="963ed-264">Se abilitata, viene eseguita la texturing bidimensionale.</span><span class="sxs-lookup"><span data-stu-id="963ed-264">If enabled, two-dimensional texturing is performed.</span></span> <span data-ttu-id="963ed-265">Vedere [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-265">See [**glTexImage2D**](glteximage2d.md).</span></span>                                                                                                                                                               |
| <span data-ttu-id="963ed-266">\_generazione trama \_ GL \_ Q</span><span class="sxs-lookup"><span data-stu-id="963ed-266">GL\_TEXTURE\_GEN\_Q</span></span>         | <span data-ttu-id="963ed-267">Se abilitata, la coordinata di trama *q* viene calcolata usando la funzione di generazione della trama definita con [**glTexGen**](gltexgen-functions.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-267">If enabled, the *q* texture coordinate is computed using the texture-generation function defined with [**glTexGen**](gltexgen-functions.md).</span></span> <span data-ttu-id="963ed-268">In caso contrario, viene utilizzata la coordinata di trama *q* corrente.</span><span class="sxs-lookup"><span data-stu-id="963ed-268">Otherwise, the current *q* texture coordinate is used.</span></span>                                                        |
| <span data-ttu-id="963ed-269">\_generazione trama \_ GL \_ R</span><span class="sxs-lookup"><span data-stu-id="963ed-269">GL\_TEXTURE\_GEN\_R</span></span>         | <span data-ttu-id="963ed-270">Se abilitata, la coordinata di trama *r* viene calcolata usando la funzione di generazione della trama definita con [**glTexGen**](gltexgen-functions.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-270">If enabled, the *r* texture coordinate is computed using the texture generation function defined with [**glTexGen**](gltexgen-functions.md).</span></span> <span data-ttu-id="963ed-271">Se è disabilitata, viene utilizzata la coordinata di trama *r* corrente.</span><span class="sxs-lookup"><span data-stu-id="963ed-271">If disabled, the current *r* texture coordinate is used.</span></span>                                                      |
| <span data-ttu-id="963ed-272">\_generazione trama \_ GL \_</span><span class="sxs-lookup"><span data-stu-id="963ed-272">GL\_TEXTURE\_GEN\_S</span></span>         | <span data-ttu-id="963ed-273">Se abilitata, la coordinata di trama *s* viene calcolata usando la funzione di generazione della trama definita con **glTexGen**.</span><span class="sxs-lookup"><span data-stu-id="963ed-273">If enabled, the *s* texture coordinate is computed using the texture generation function defined with **glTexGen**.</span></span> <span data-ttu-id="963ed-274">Se è disabilitata, viene utilizzata la coordinata *di trama corrente* .</span><span class="sxs-lookup"><span data-stu-id="963ed-274">If disabled, the current *s* texture coordinate is used.</span></span>                                                                                |
| <span data-ttu-id="963ed-275">\_gen trama \_ GL \_ T</span><span class="sxs-lookup"><span data-stu-id="963ed-275">GL\_TEXTURE\_GEN\_T</span></span>         | <span data-ttu-id="963ed-276">Se abilitata, la coordinata di trama *t* viene calcolata usando la funzione di generazione della trama definita con [**glTexGen**](gltexgen-functions.md).</span><span class="sxs-lookup"><span data-stu-id="963ed-276">If enabled, the *t* texture coordinate is computed using the texture generation function defined with [**glTexGen**](gltexgen-functions.md).</span></span> <span data-ttu-id="963ed-277">Se è disabilitata, viene utilizzata la coordinata di trama *t* corrente.</span><span class="sxs-lookup"><span data-stu-id="963ed-277">If disabled, the current *t* texture coordinate is used.</span></span>                                                      |



 

## <a name="requirements"></a><span data-ttu-id="963ed-278">Requisiti</span><span class="sxs-lookup"><span data-stu-id="963ed-278">Requirements</span></span>



| <span data-ttu-id="963ed-279">Requisito</span><span class="sxs-lookup"><span data-stu-id="963ed-279">Requirement</span></span> | <span data-ttu-id="963ed-280">Valore</span><span class="sxs-lookup"><span data-stu-id="963ed-280">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="963ed-281">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="963ed-281">Minimum supported client</span></span><br/> | <span data-ttu-id="963ed-282">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="963ed-282">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="963ed-283">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="963ed-283">Minimum supported server</span></span><br/> | <span data-ttu-id="963ed-284">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="963ed-284">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="963ed-285">Intestazione</span><span class="sxs-lookup"><span data-stu-id="963ed-285">Header</span></span><br/>                   | <dl> <span data-ttu-id="963ed-286"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="963ed-286"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="963ed-287">Libreria</span><span class="sxs-lookup"><span data-stu-id="963ed-287">Library</span></span><br/>                  | <dl> <span data-ttu-id="963ed-288"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="963ed-288"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="963ed-289">DLL</span><span class="sxs-lookup"><span data-stu-id="963ed-289">DLL</span></span><br/>                      | <dl> <span data-ttu-id="963ed-290"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="963ed-290"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="963ed-291">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="963ed-291">See also</span></span>

<dl> <dt>

[<span data-ttu-id="963ed-292">**glAlphaFunc**</span><span class="sxs-lookup"><span data-stu-id="963ed-292">**glAlphaFunc**</span></span>](glalphafunc.md)
</dt> <dt>

[<span data-ttu-id="963ed-293">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="963ed-293">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="963ed-294">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="963ed-294">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="963ed-295">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="963ed-295">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="963ed-296">**glClipPlane**</span><span class="sxs-lookup"><span data-stu-id="963ed-296">**glClipPlane**</span></span>](glclipplane.md)
</dt> <dt>

[<span data-ttu-id="963ed-297">**glColorMaterial**</span><span class="sxs-lookup"><span data-stu-id="963ed-297">**glColorMaterial**</span></span>](glcolormaterial.md)
</dt> <dt>

[<span data-ttu-id="963ed-298">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="963ed-298">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="963ed-299">**glCullFace**</span><span class="sxs-lookup"><span data-stu-id="963ed-299">**glCullFace**</span></span>](glcullface.md)
</dt> <dt>

[<span data-ttu-id="963ed-300">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="963ed-300">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="963ed-301">**glDepthRange**</span><span class="sxs-lookup"><span data-stu-id="963ed-301">**glDepthRange**</span></span>](gldepthrange.md)
</dt> <dt>

[<span data-ttu-id="963ed-302">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="963ed-302">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="963ed-303">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="963ed-303">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="963ed-304">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="963ed-304">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="963ed-305">**Remo**</span><span class="sxs-lookup"><span data-stu-id="963ed-305">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="963ed-306">**glEvalCoord1**</span><span class="sxs-lookup"><span data-stu-id="963ed-306">**glEvalCoord1**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="963ed-307">**glEvalMesh1**</span><span class="sxs-lookup"><span data-stu-id="963ed-307">**glEvalMesh1**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="963ed-308">**glEvalPoint1**</span><span class="sxs-lookup"><span data-stu-id="963ed-308">**glEvalPoint1**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="963ed-309">**glFog**</span><span class="sxs-lookup"><span data-stu-id="963ed-309">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="963ed-310">**glGet**</span><span class="sxs-lookup"><span data-stu-id="963ed-310">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="963ed-311">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="963ed-311">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="963ed-312">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="963ed-312">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="963ed-313">**glLight**</span><span class="sxs-lookup"><span data-stu-id="963ed-313">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="963ed-314">**glLightModel**</span><span class="sxs-lookup"><span data-stu-id="963ed-314">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> <dt>

[<span data-ttu-id="963ed-315">**glLineWidth**</span><span class="sxs-lookup"><span data-stu-id="963ed-315">**glLineWidth**</span></span>](gllinewidth.md)
</dt> <dt>

[<span data-ttu-id="963ed-316">**glLineStipple**</span><span class="sxs-lookup"><span data-stu-id="963ed-316">**glLineStipple**</span></span>](gllinestipple.md)
</dt> <dt>

[<span data-ttu-id="963ed-317">**glLogicOp**</span><span class="sxs-lookup"><span data-stu-id="963ed-317">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="963ed-318">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="963ed-318">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="963ed-319">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="963ed-319">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="963ed-320">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="963ed-320">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="963ed-321">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="963ed-321">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="963ed-322">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="963ed-322">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="963ed-323">**glPointSize**</span><span class="sxs-lookup"><span data-stu-id="963ed-323">**glPointSize**</span></span>](glpointsize.md)
</dt> <dt>

[<span data-ttu-id="963ed-324">**glPolygonMode**</span><span class="sxs-lookup"><span data-stu-id="963ed-324">**glPolygonMode**</span></span>](glpolygonmode.md)
</dt> <dt>

[<span data-ttu-id="963ed-325">**glPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="963ed-325">**glPolygonStipple**</span></span>](glpolygonstipple.md)
</dt> <dt>

[<span data-ttu-id="963ed-326">**glScissor**</span><span class="sxs-lookup"><span data-stu-id="963ed-326">**glScissor**</span></span>](glscissor.md)
</dt> <dt>

[<span data-ttu-id="963ed-327">**glStencilFunc**</span><span class="sxs-lookup"><span data-stu-id="963ed-327">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> <dt>

[<span data-ttu-id="963ed-328">**glStencilOp**</span><span class="sxs-lookup"><span data-stu-id="963ed-328">**glStencilOp**</span></span>](glstencilop.md)
</dt> <dt>

[<span data-ttu-id="963ed-329">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="963ed-329">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="963ed-330">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="963ed-330">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="963ed-331">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="963ed-331">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="963ed-332">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="963ed-332">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> </dl>

 

 





