---
title: funzione glDisable (GL. h)
description: Le funzioni glEnable e glDisable abilitano o disabilitano le funzionalità di OpenGL. | funzione glDisable (GL. h)
ms.assetid: 094f730e-5e2b-485e-8d9d-fee2902d3d5f
keywords:
- funzione glDisable OpenGL
topic_type:
- apiref
api_name:
- glDisable
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eff5c12e53eb060777f75ad537bed265401a7a26
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321854"
---
# <a name="gldisable-function"></a><span data-ttu-id="70820-105">glDisable (funzione)</span><span class="sxs-lookup"><span data-stu-id="70820-105">glDisable function</span></span>

<span data-ttu-id="70820-106">Le funzioni [**glEnable**](glenable.md) e **glDisable** abilitano o disabilitano le funzionalità di OpenGL.</span><span class="sxs-lookup"><span data-stu-id="70820-106">The [**glEnable**](glenable.md) and **glDisable** functions enable or disable OpenGL capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="70820-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="70820-107">Syntax</span></span>


```C++
void WINAPI glDisable(
   GLenum cap
);
```



## <a name="parameters"></a><span data-ttu-id="70820-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="70820-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70820-109">*limite*</span><span class="sxs-lookup"><span data-stu-id="70820-109">*cap*</span></span> 
</dt> <dd>

<span data-ttu-id="70820-110">Costante simbolica che indica una funzionalità OpenGL.</span><span class="sxs-lookup"><span data-stu-id="70820-110">A symbolic constant indicating an OpenGL capability.</span></span>

<span data-ttu-id="70820-111">Per informazioni sui valori che possono essere accettati da *Cap* , vedere la sezione Osservazioni riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="70820-111">For discussion of the values *cap* can take, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70820-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="70820-112">Return value</span></span>

<span data-ttu-id="70820-113">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="70820-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="70820-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="70820-114">Error codes</span></span>

<span data-ttu-id="70820-115">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="70820-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="70820-116">Nome</span><span class="sxs-lookup"><span data-stu-id="70820-116">Name</span></span>                                                                                                  | <span data-ttu-id="70820-117">Significato</span><span class="sxs-lookup"><span data-stu-id="70820-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="70820-118"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="70820-118"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="70820-119">*Cap* non è uno dei valori elencati nella sezione Osservazioni precedente.</span><span class="sxs-lookup"><span data-stu-id="70820-119">*cap* was not one of the values listed in the preceding Remarks section.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="70820-120"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="70820-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="70820-121">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="70820-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="70820-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="70820-122">Remarks</span></span>

<span data-ttu-id="70820-123">Le funzioni [**glEnable**](glenable.md) e **glDisable** abilitano e disabilitano diverse funzionalità grafiche OpenGL.</span><span class="sxs-lookup"><span data-stu-id="70820-123">The [**glEnable**](glenable.md) and **glDisable** functions enable and disable various OpenGL graphics capabilities.</span></span> <span data-ttu-id="70820-124">Usare [**glIsEnabled**](glisenabled.md) o [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) per determinare l'impostazione corrente di tutte le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="70820-124">Use [**glIsEnabled**](glisenabled.md) or [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) to determine the current setting of any capability.</span></span>

<span data-ttu-id="70820-125">Sia [**glEnable**](glenable.md) che **glDisable** accettano un solo argomento, *Cap*, che può assumere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="70820-125">Both [**glEnable**](glenable.md) and **glDisable** take a single argument, *cap*, which can assume one of the following values:</span></span>



| <span data-ttu-id="70820-126">Valore</span><span class="sxs-lookup"><span data-stu-id="70820-126">Value</span></span>                       | <span data-ttu-id="70820-127">Significato</span><span class="sxs-lookup"><span data-stu-id="70820-127">Meaning</span></span>                                                                                                                                                                                                                                                     |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70820-128">\_test GL Alpha \_</span><span class="sxs-lookup"><span data-stu-id="70820-128">GL\_ALPHA\_TEST</span></span>             | <span data-ttu-id="70820-129">Se abilitata, eseguire il test alfa.</span><span class="sxs-lookup"><span data-stu-id="70820-129">If enabled, do alpha testing.</span></span> <span data-ttu-id="70820-130">Vedere [**glAlphaFunc**](glalphafunc.md).</span><span class="sxs-lookup"><span data-stu-id="70820-130">See [**glAlphaFunc**](glalphafunc.md).</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="70820-131">GL \_ auto \_ normale</span><span class="sxs-lookup"><span data-stu-id="70820-131">GL\_AUTO\_NORMAL</span></span>            | <span data-ttu-id="70820-132">Se abilitata, calcola i vettori normali della superficie di calcolo in modo analitico quando i \_ vertici di GL map2 \_ Vertex \_ 3 o GL \_ map2 \_ sono stati \_ generati.</span><span class="sxs-lookup"><span data-stu-id="70820-132">If enabled, compute surface normal vectors analytically when either GL\_MAP2\_VERTEX\_3 or GL\_MAP2\_VERTEX\_4 has generated vertices.</span></span> <span data-ttu-id="70820-133">Vedere [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="70820-133">See [**glMap2**](glmap2.md).</span></span>                                                                                        |
| <span data-ttu-id="70820-134">\_Blend GL</span><span class="sxs-lookup"><span data-stu-id="70820-134">GL\_BLEND</span></span>                   | <span data-ttu-id="70820-135">Se abilitata, combina i valori dei colori RGBA in ingresso con i valori nei buffer dei colori.</span><span class="sxs-lookup"><span data-stu-id="70820-135">If enabled, blend the incoming RGBA color values with the values in the color buffers.</span></span> <span data-ttu-id="70820-136">Vedere [**glBlendFunc**](glblendfunc.md).</span><span class="sxs-lookup"><span data-stu-id="70820-136">See [**glBlendFunc**](glblendfunc.md).</span></span>                                                                                                                              |
| <span data-ttu-id="70820-137">\_Piano di ritaglio GL \_ *i*</span><span class="sxs-lookup"><span data-stu-id="70820-137">GL\_CLIP\_PLANE *i*</span></span>          | <span data-ttu-id="70820-138">Se abilitata, ritagliare la geometria rispetto *al piano di* ritaglio definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="70820-138">If enabled, clip geometry against user-defined clipping plane *i*.</span></span> <span data-ttu-id="70820-139">Vedere [**glClipPlane**](glclipplane.md).</span><span class="sxs-lookup"><span data-stu-id="70820-139">See [**glClipPlane**](glclipplane.md).</span></span>                                                                                                                                                  |
| <span data-ttu-id="70820-140">\_operazione di \_ logica \_ colori GL</span><span class="sxs-lookup"><span data-stu-id="70820-140">GL\_COLOR\_LOGIC\_OP</span></span>        | <span data-ttu-id="70820-141">Se abilitata, applicare l'operazione logica corrente ai valori del buffer dei colori e del colore RGBA in ingresso.</span><span class="sxs-lookup"><span data-stu-id="70820-141">If enabled, apply the current logical operation to the incoming RGBA color and color buffer values.</span></span> <span data-ttu-id="70820-142">Vedere [**glLogicOp**](gllogicop.md).</span><span class="sxs-lookup"><span data-stu-id="70820-142">See [**glLogicOp**](gllogicop.md).</span></span>                                                                                                                     |
| <span data-ttu-id="70820-143">\_materiale colore \_ GL</span><span class="sxs-lookup"><span data-stu-id="70820-143">GL\_COLOR\_MATERIAL</span></span>         | <span data-ttu-id="70820-144">Se abilitata, avere uno o più parametri Material tenere traccia del colore corrente.</span><span class="sxs-lookup"><span data-stu-id="70820-144">If enabled, have one or more material parameters track the current color.</span></span> <span data-ttu-id="70820-145">Vedere [**glColorMaterial**](glcolormaterial.md).</span><span class="sxs-lookup"><span data-stu-id="70820-145">See [**glColorMaterial**](glcolormaterial.md).</span></span>                                                                                                                                   |
| <span data-ttu-id="70820-146">superficie di selezione GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="70820-146">GL\_CULL\_FACE</span></span>              | <span data-ttu-id="70820-147">Se abilitata, i poligoni vengono raccolti in base al relativo avvolgimento nelle coordinate della finestra.</span><span class="sxs-lookup"><span data-stu-id="70820-147">If enabled, cull polygons based on their winding in window coordinates.</span></span> <span data-ttu-id="70820-148">Vedere [**glCullFace**](glcullface.md).</span><span class="sxs-lookup"><span data-stu-id="70820-148">See [**glCullFace**](glcullface.md).</span></span>                                                                                                                                               |
| <span data-ttu-id="70820-149">\_test di profondità GL \_</span><span class="sxs-lookup"><span data-stu-id="70820-149">GL\_DEPTH\_TEST</span></span>             | <span data-ttu-id="70820-150">Se abilitata, eseguire confronti di profondità e aggiornare il buffer di profondità.</span><span class="sxs-lookup"><span data-stu-id="70820-150">If enabled, do depth comparisons and update the depth buffer.</span></span> <span data-ttu-id="70820-151">Vedere [**glDepthFunc**](gldepthfunc.md) e [**glDepthRange**](gldepthrange.md).</span><span class="sxs-lookup"><span data-stu-id="70820-151">See [**glDepthFunc**](gldepthfunc.md) and [**glDepthRange**](gldepthrange.md).</span></span>                                                                                                              |
| <span data-ttu-id="70820-152">\_dithering GL</span><span class="sxs-lookup"><span data-stu-id="70820-152">GL\_DITHER</span></span>                  | <span data-ttu-id="70820-153">Se abilitata, i componenti di colore o gli indici di dithering prima che vengano scritti nel buffer dei colori.</span><span class="sxs-lookup"><span data-stu-id="70820-153">If enabled, dither color components or indexes before they are written to the color buffer.</span></span>                                                                                                                                                                 |
| <span data-ttu-id="70820-154">\_nebbia GL</span><span class="sxs-lookup"><span data-stu-id="70820-154">GL\_FOG</span></span>                     | <span data-ttu-id="70820-155">Se abilitata, fondere un colore di nebbia al colore di post-texturing.</span><span class="sxs-lookup"><span data-stu-id="70820-155">If enabled, blend a fog color into the post-texturing color.</span></span> <span data-ttu-id="70820-156">Vedere [**glFog**](glfog.md).</span><span class="sxs-lookup"><span data-stu-id="70820-156">See [**glFog**](glfog.md).</span></span>                                                                                                                                                                    |
| <span data-ttu-id="70820-157">\_ \_ operazione logica indice \_ GL</span><span class="sxs-lookup"><span data-stu-id="70820-157">GL\_INDEX\_LOGIC\_OP</span></span>        | <span data-ttu-id="70820-158">Se abilitata, applicare l'operazione logica corrente agli indici indici in ingresso e al buffer dei colori.</span><span class="sxs-lookup"><span data-stu-id="70820-158">If enabled, apply the current logical operation to the incoming index and color buffer indices.</span></span> <span data-ttu-id="70820-159">Vedere [**glLogicOp**](gllogicop.md).</span><span class="sxs-lookup"><span data-stu-id="70820-159">See [**glLogicOp**](gllogicop.md).</span></span>                                                                                                                         |
| <span data-ttu-id="70820-160">GL \_ Light *i*</span><span class="sxs-lookup"><span data-stu-id="70820-160">GL\_LIGHT *i*</span></span>                | <span data-ttu-id="70820-161">Se abilitata, includere la luce *i* nella valutazione dell'equazione di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="70820-161">If enabled, include light *i* in the evaluation of the lighting equation.</span></span> <span data-ttu-id="70820-162">Vedere [**glLightModel**](gllightmodel-functions.md) e [**glLight**](gllight-functions.md).</span><span class="sxs-lookup"><span data-stu-id="70820-162">See [**glLightModel**](gllightmodel-functions.md) and [**glLight**](gllight-functions.md).</span></span>                                                                                      |
| <span data-ttu-id="70820-163">\_illuminazione GL</span><span class="sxs-lookup"><span data-stu-id="70820-163">GL\_LIGHTING</span></span>                | <span data-ttu-id="70820-164">Se abilitata, usare i parametri di illuminazione correnti per calcolare il colore o l'indice del vertice.</span><span class="sxs-lookup"><span data-stu-id="70820-164">If enabled, use the current lighting parameters to compute the vertex color or index.</span></span> <span data-ttu-id="70820-165">Se disabilitato, associare il colore o l'indice corrente a ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="70820-165">If disabled, associate the current color or index with each vertex.</span></span> <span data-ttu-id="70820-166">Vedere [**glMaterial**](glmaterial-functions.md), **glLightModel** e **glLight**.</span><span class="sxs-lookup"><span data-stu-id="70820-166">See [**glMaterial**](glmaterial-functions.md), **glLightModel**, and **glLight**.</span></span>                |
| <span data-ttu-id="70820-167">\_linea GL \_ smussata</span><span class="sxs-lookup"><span data-stu-id="70820-167">GL\_LINE\_SMOOTH</span></span>            | <span data-ttu-id="70820-168">Se abilitata, creare linee con filtri corretti.</span><span class="sxs-lookup"><span data-stu-id="70820-168">If enabled, draw lines with correct filtering.</span></span> <span data-ttu-id="70820-169">Se è disabilitata, creare linee con alias.</span><span class="sxs-lookup"><span data-stu-id="70820-169">If disabled, draw aliased lines.</span></span> <span data-ttu-id="70820-170">Vedere [**glLineWidth**](gllinewidth.md).</span><span class="sxs-lookup"><span data-stu-id="70820-170">See [**glLineWidth**](gllinewidth.md).</span></span>                                                                                                                                     |
| <span data-ttu-id="70820-171">\_stipple linea \_ GL</span><span class="sxs-lookup"><span data-stu-id="70820-171">GL\_LINE\_STIPPLE</span></span>           | <span data-ttu-id="70820-172">Se abilitata, usare il modello stipple di riga corrente quando si disegnano le linee.</span><span class="sxs-lookup"><span data-stu-id="70820-172">If enabled, use the current line stipple pattern when drawing lines.</span></span> <span data-ttu-id="70820-173">Vedere [**glLineStipple**](gllinestipple.md).</span><span class="sxs-lookup"><span data-stu-id="70820-173">See [**glLineStipple**](gllinestipple.md).</span></span>                                                                                                                                            |
| <span data-ttu-id="70820-174">\_op logica \_ GL</span><span class="sxs-lookup"><span data-stu-id="70820-174">GL\_LOGIC\_OP</span></span>               | <span data-ttu-id="70820-175">Se abilitata, applicare l'operazione logica attualmente selezionata agli indici del buffer di colore e in ingresso.</span><span class="sxs-lookup"><span data-stu-id="70820-175">If enabled, apply the currently selected logical operation to the incoming and color-buffer indexes.</span></span> <span data-ttu-id="70820-176">Vedere [**glLogicOp**](gllogicop.md).</span><span class="sxs-lookup"><span data-stu-id="70820-176">See [**glLogicOp**](gllogicop.md).</span></span>                                                                                                                    |
| <span data-ttu-id="70820-177">\_Mappa1 \_ colore \_ 4 GL</span><span class="sxs-lookup"><span data-stu-id="70820-177">GL\_MAP1\_COLOR\_4</span></span>          | <span data-ttu-id="70820-178">Se abilitata, le chiamate a [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)e [**glEvalPoint1**](glevalpoint.md) generano valori RGBA.</span><span class="sxs-lookup"><span data-stu-id="70820-178">If enabled, calls to [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md), and [**glEvalPoint1**](glevalpoint.md) generate RGBA values.</span></span> <span data-ttu-id="70820-179">Vedere anche [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="70820-179">See also [**glMap1**](glmap1.md).</span></span>                                           |
| <span data-ttu-id="70820-180">\_Indice MAPPA1 \_ GL</span><span class="sxs-lookup"><span data-stu-id="70820-180">GL\_MAP1\_INDEX</span></span>             | <span data-ttu-id="70820-181">Se abilitata, le chiamate a **glEvalCoord1**, **glEvalMesh1** e **glEvalPoint1** generano indici colori.</span><span class="sxs-lookup"><span data-stu-id="70820-181">If enabled, calls to **glEvalCoord1**, **glEvalMesh1**, and **glEvalPoint1** generate color indexes.</span></span> <span data-ttu-id="70820-182">Vedere anche **glMap1**.</span><span class="sxs-lookup"><span data-stu-id="70820-182">See also **glMap1**.</span></span>                                                                                                                                   |
| <span data-ttu-id="70820-183">\_Normale MAPPA1 \_ GL</span><span class="sxs-lookup"><span data-stu-id="70820-183">GL\_MAP1\_NORMAL</span></span>            | <span data-ttu-id="70820-184">Se abilitata, le chiamate a [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)e [**glEvalPoint1**](glevalpoint.md) generano normali.</span><span class="sxs-lookup"><span data-stu-id="70820-184">If enabled, calls to [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md), and [**glEvalPoint1**](glevalpoint.md) generate normals.</span></span> <span data-ttu-id="70820-185">Vedere anche [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="70820-185">See also [**glMap1**](glmap1.md).</span></span>                                               |
| <span data-ttu-id="70820-186">\_Trama GL \_ Mappa1 \_ Coord \_ 1</span><span class="sxs-lookup"><span data-stu-id="70820-186">GL\_MAP1\_TEXTURE\_COORD\_1</span></span> | <span data-ttu-id="70820-187">Se abilitata, le chiamate a **glEvalCoord1**, **glEvalMesh1** e **glEvalPoint1** generano le coordinate di trama *s* .</span><span class="sxs-lookup"><span data-stu-id="70820-187">If enabled, calls to **glEvalCoord1**, **glEvalMesh1**, and **glEvalPoint1** generate *s* texture coordinates.</span></span> <span data-ttu-id="70820-188">Vedere anche **glMap1**.</span><span class="sxs-lookup"><span data-stu-id="70820-188">See also **glMap1**.</span></span>                                                                                                                         |
| <span data-ttu-id="70820-189">\_ \_ Coord trama GL \_ Mappa1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="70820-189">GL\_MAP1\_TEXTURE\_COORD\_2</span></span> | <span data-ttu-id="70820-190">Se abilitata, le chiamate a [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)e [**glEvalPoint1**](glevalpoint.md) generano le coordinate di trama *s* e *t* .</span><span class="sxs-lookup"><span data-stu-id="70820-190">If enabled, calls to [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md), and [**glEvalPoint1**](glevalpoint.md) generate *s* and *t* texture coordinates.</span></span> <span data-ttu-id="70820-191">Vedere anche [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="70820-191">See also [**glMap1**](glmap1.md).</span></span>                       |
| <span data-ttu-id="70820-192">\_Trama GL \_ Mappa1 \_ Coord \_ 3</span><span class="sxs-lookup"><span data-stu-id="70820-192">GL\_MAP1\_TEXTURE\_COORD\_3</span></span> | <span data-ttu-id="70820-193">Se abilitata, le chiamate a **glEvalCoord1**, **glEvalMesh1** e **glEvalPoint1** generano le coordinate di trama *s*, *t* e *r* .</span><span class="sxs-lookup"><span data-stu-id="70820-193">If enabled, calls to **glEvalCoord1**, **glEvalMesh1**, and **glEvalPoint1** generate *s*, *t*, and *r* texture coordinates.</span></span> <span data-ttu-id="70820-194">Vedere anche **glMap1**.</span><span class="sxs-lookup"><span data-stu-id="70820-194">See also **glMap1**.</span></span>                                                                                                           |
| <span data-ttu-id="70820-195">\_Trama GL \_ Mappa1 \_ Coord \_ 4</span><span class="sxs-lookup"><span data-stu-id="70820-195">GL\_MAP1\_TEXTURE\_COORD\_4</span></span> | <span data-ttu-id="70820-196">Se abilitata, le chiamate a [glEvalCoord1](glevalcoord-functions.md), [glEvalMesh1](glevalmesh-functions.md)e [**glEvalPoint1**](glevalpoint.md) generano le coordinate di trama *s*, *t*, *r* e *q* .</span><span class="sxs-lookup"><span data-stu-id="70820-196">If enabled, calls to [glEvalCoord1](glevalcoord-functions.md), [glEvalMesh1](glevalmesh-functions.md), and [**glEvalPoint1**](glevalpoint.md) generate *s*, *t*, *r*, and *q* texture coordinates.</span></span> <span data-ttu-id="70820-197">Vedere anche [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="70820-197">See also [**glMap1**](glmap1.md).</span></span>                    |
| <span data-ttu-id="70820-198">\_Vertice GL \_ Mappa1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="70820-198">GL\_MAP1\_VERTEX\_3</span></span>         | <span data-ttu-id="70820-199">Se abilitata, le chiamate a **glEvalCoord1**, **glEvalMesh1** e **glEvalPoint1** generano coordinate di vertice *x*, *y* e *z* .</span><span class="sxs-lookup"><span data-stu-id="70820-199">If enabled, calls to **glEvalCoord1**, **glEvalMesh1**, and **glEvalPoint1** generate *x*, *y*, and *z* vertex coordinates.</span></span> <span data-ttu-id="70820-200">Vedere anche **glMap1**.</span><span class="sxs-lookup"><span data-stu-id="70820-200">See also **glMap1**.</span></span>                                                                                                            |
| <span data-ttu-id="70820-201">\_Mappa1 \_ Vertex \_ 4</span><span class="sxs-lookup"><span data-stu-id="70820-201">GL\_MAP1\_VERTEX\_4</span></span>         | <span data-ttu-id="70820-202">Se abilitate, le chiamate a [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)e [**glEvalPoint1**](glevalpoint.md) generano coordinate di vertice *x*, *y*, *z* e *w* omogenee.</span><span class="sxs-lookup"><span data-stu-id="70820-202">If enabled, calls to [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md), and [**glEvalPoint1**](glevalpoint.md) generate homogeneous *x*, *y*, *z*, and *w* vertex coordinates.</span></span> <span data-ttu-id="70820-203">Vedere anche [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="70820-203">See also [**glMap1**](glmap1.md).</span></span> |
| <span data-ttu-id="70820-204">\_Map2 \_ colore \_ 4 GL</span><span class="sxs-lookup"><span data-stu-id="70820-204">GL\_MAP2\_COLOR\_4</span></span>          | <span data-ttu-id="70820-205">Se abilitata, le chiamate a [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)e [**glEvalPoint2**](glevalpoint.md) generano valori RGBA.</span><span class="sxs-lookup"><span data-stu-id="70820-205">If enabled, calls to [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md), and [**glEvalPoint2**](glevalpoint.md) generate RGBA values.</span></span> <span data-ttu-id="70820-206">Vedere anche [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="70820-206">See also [**glMap2**](glmap2.md).</span></span>                                           |
| <span data-ttu-id="70820-207">\_Indice map2 \_ GL</span><span class="sxs-lookup"><span data-stu-id="70820-207">GL\_MAP2\_INDEX</span></span>             | <span data-ttu-id="70820-208">Se abilitata, le chiamate a **glEvalCoord2**, **glEvalMesh2** e **glEvalPoint2** generano indici colori.</span><span class="sxs-lookup"><span data-stu-id="70820-208">If enabled, calls to **glEvalCoord2**, **glEvalMesh2**, and **glEvalPoint2** generate color indexes.</span></span> <span data-ttu-id="70820-209">Vedere anche **glMap2**.</span><span class="sxs-lookup"><span data-stu-id="70820-209">See also **glMap2**.</span></span>                                                                                                                                   |
| <span data-ttu-id="70820-210">\_Normale map2 \_ GL</span><span class="sxs-lookup"><span data-stu-id="70820-210">GL\_MAP2\_NORMAL</span></span>            | <span data-ttu-id="70820-211">Se abilitata, le chiamate a [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)e [**glEvalPoint2**](glevalpoint.md) generano normali.</span><span class="sxs-lookup"><span data-stu-id="70820-211">If enabled, calls to [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md), and [**glEvalPoint2**](glevalpoint.md) generate normals.</span></span> <span data-ttu-id="70820-212">Vedere anche [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="70820-212">See also [**glMap2**](glmap2.md).</span></span>                                               |
| <span data-ttu-id="70820-213">\_Trama GL \_ map2 \_ Coord \_ 1</span><span class="sxs-lookup"><span data-stu-id="70820-213">GL\_MAP2\_TEXTURE\_COORD\_1</span></span> | <span data-ttu-id="70820-214">Se abilitata, le chiamate a **glEvalCoord2**, **glEvalMesh2** e **glEvalPoint2** generano le coordinate di trama *s* .</span><span class="sxs-lookup"><span data-stu-id="70820-214">If enabled, calls to **glEvalCoord2**, **glEvalMesh2**, and **glEvalPoint2** generate *s* texture coordinates.</span></span> <span data-ttu-id="70820-215">Vedere anche **glMap2**.</span><span class="sxs-lookup"><span data-stu-id="70820-215">See also **glMap2**.</span></span>                                                                                                                         |
| <span data-ttu-id="70820-216">\_ \_ Coord trama GL \_ map2 \_ 2</span><span class="sxs-lookup"><span data-stu-id="70820-216">GL\_MAP2\_TEXTURE\_COORD\_2</span></span> | <span data-ttu-id="70820-217">Se abilitata, le chiamate a [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)e [**glEvalPoint2**](glevalpoint.md) generano le coordinate di trama *s* e *t* .</span><span class="sxs-lookup"><span data-stu-id="70820-217">If enabled, calls to [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md), and [**glEvalPoint2**](glevalpoint.md) generate *s* and *t* texture coordinates.</span></span> <span data-ttu-id="70820-218">Vedere anche [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="70820-218">See also [**glMap2**](glmap2.md).</span></span>                       |
| <span data-ttu-id="70820-219">\_Trama GL \_ map2 \_ Coord \_ 3</span><span class="sxs-lookup"><span data-stu-id="70820-219">GL\_MAP2\_TEXTURE\_COORD\_3</span></span> | <span data-ttu-id="70820-220">Se abilitata, le chiamate a **glEvalCoord2**, **glEvalMesh2** e **glEvalPoint2** generano le coordinate di trama *s*, *t* e *r* .</span><span class="sxs-lookup"><span data-stu-id="70820-220">If enabled, calls to **glEvalCoord2**, **glEvalMesh2**, and **glEvalPoint2** generate *s*, *t*, and *r* texture coordinates.</span></span> <span data-ttu-id="70820-221">Vedere anche **glMap2**.</span><span class="sxs-lookup"><span data-stu-id="70820-221">See also **glMap2**.</span></span>                                                                                                           |
| <span data-ttu-id="70820-222">\_Trama GL \_ map2 \_ Coord \_ 4</span><span class="sxs-lookup"><span data-stu-id="70820-222">GL\_MAP2\_TEXTURE\_COORD\_4</span></span> | <span data-ttu-id="70820-223">Se abilitata, le chiamate a [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)e [**glEvalPoint2**](glevalpoint.md) generano le coordinate di trama *s*, *t*, *r* e *q* .</span><span class="sxs-lookup"><span data-stu-id="70820-223">If enabled, calls to [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md), and [**glEvalPoint2**](glevalpoint.md) generate *s*, *t*, *r*, and *q* texture coordinates.</span></span> <span data-ttu-id="70820-224">Vedere anche [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="70820-224">See also [**glMap2**](glmap2.md).</span></span>            |
| <span data-ttu-id="70820-225">\_Vertice GL \_ map2 \_ 3</span><span class="sxs-lookup"><span data-stu-id="70820-225">GL\_MAP2\_VERTEX\_3</span></span>         | <span data-ttu-id="70820-226">Se abilitata, le chiamate a **glEvalCoord2**, **glEvalMesh2** e **glEvalPoint2** generano coordinate di vertice *x*, *y* e *z* .</span><span class="sxs-lookup"><span data-stu-id="70820-226">If enabled, calls to **glEvalCoord2**, **glEvalMesh2**, and **glEvalPoint2** generate *x*, *y*, and *z* vertex coordinates.</span></span> <span data-ttu-id="70820-227">Vedere anche **glMap2**.</span><span class="sxs-lookup"><span data-stu-id="70820-227">See also **glMap2**.</span></span>                                                                                                            |
| <span data-ttu-id="70820-228">\_Map2 \_ Vertex \_ 4</span><span class="sxs-lookup"><span data-stu-id="70820-228">GL\_MAP2\_VERTEX\_4</span></span>         | <span data-ttu-id="70820-229">Se abilitate, le chiamate a [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)e [**glEvalPoint2**](glevalpoint.md) generano coordinate di vertice *x*, *y*, *z* e *w* omogenee.</span><span class="sxs-lookup"><span data-stu-id="70820-229">If enabled, calls to [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md), and [**glEvalPoint2**](glevalpoint.md) generate homogeneous *x*, *y*, *z*, and *w* vertex coordinates.</span></span> <span data-ttu-id="70820-230">Vedere anche [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="70820-230">See also [**glMap2**](glmap2.md).</span></span> |
| <span data-ttu-id="70820-231">\_normalizzare GL</span><span class="sxs-lookup"><span data-stu-id="70820-231">GL\_NORMALIZE</span></span>               | <span data-ttu-id="70820-232">Se abilitata, i vettori normali specificati con **glNormal** vengono ridimensionati alla lunghezza dell'unità dopo la trasformazione.</span><span class="sxs-lookup"><span data-stu-id="70820-232">If enabled, normal vectors specified with **glNormal** are scaled to unit length after transformation.</span></span> <span data-ttu-id="70820-233">Vedere [**glNormal**](glnormal-functions.md).</span><span class="sxs-lookup"><span data-stu-id="70820-233">See [**glNormal**](glnormal-functions.md).</span></span>                                                                                                          |
| <span data-ttu-id="70820-234">\_punto GL \_ smussato</span><span class="sxs-lookup"><span data-stu-id="70820-234">GL\_POINT\_SMOOTH</span></span>           | <span data-ttu-id="70820-235">Se abilitata, creare punti con filtro appropriato.</span><span class="sxs-lookup"><span data-stu-id="70820-235">If enabled, draw points with proper filtering.</span></span> <span data-ttu-id="70820-236">Se disabilitato, creare punti con alias.</span><span class="sxs-lookup"><span data-stu-id="70820-236">If disabled, draw aliased points.</span></span> <span data-ttu-id="70820-237">Vedere [**glPointSize**](glpointsize.md).</span><span class="sxs-lookup"><span data-stu-id="70820-237">See [**glPointSize**](glpointsize.md).</span></span>                                                                                                                                    |
| <span data-ttu-id="70820-238">\_riempimento offset poligono GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="70820-238">GL\_POLYGON\_OFFSET\_FILL</span></span>   | <span data-ttu-id="70820-239">Se abilitata e se viene eseguito il rendering del poligono in \_ modalità di riempimento GL, viene aggiunto un offset ai valori di profondità dei frammenti di un poligono prima che venga eseguito il confronto di profondità.</span><span class="sxs-lookup"><span data-stu-id="70820-239">If enabled, and if the polygon is rendered in GL\_FILL mode, an offset is added to depth values of a polygon's fragments before the depth comparison is performed.</span></span> <span data-ttu-id="70820-240">Vedere [**glPolygonOffset**](glpolygonoffset.md)**.**</span><span class="sxs-lookup"><span data-stu-id="70820-240">See [**glPolygonOffset**](glpolygonoffset.md)**.**</span></span>                                      |
| <span data-ttu-id="70820-241">\_linea offset poligono GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="70820-241">GL\_POLYGON\_OFFSET\_LINE</span></span>   | <span data-ttu-id="70820-242">Se abilitata e se viene eseguito il rendering del poligono in \_ modalità linea GL, viene aggiunto un offset ai valori di profondità dei frammenti di un poligono prima che venga eseguito il confronto di profondità.</span><span class="sxs-lookup"><span data-stu-id="70820-242">If enabled, and if the polygon is rendered in GL\_LINE mode, an offset is added to depth values of a polygon's fragments before the depth comparison is performed.</span></span> <span data-ttu-id="70820-243">Vedere **glPolygonOffset**.</span><span class="sxs-lookup"><span data-stu-id="70820-243">See **glPolygonOffset**.</span></span>                                                                 |
| <span data-ttu-id="70820-244">\_punto di offset del poligono GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="70820-244">GL\_POLYGON\_OFFSET\_POINT</span></span>  | <span data-ttu-id="70820-245">Se abilitata, viene aggiunto un offset ai valori di profondità dei frammenti di un poligono prima che venga eseguito il confronto di profondità, se il poligono viene sottoposto a rendering in \_ modalità punto GL.</span><span class="sxs-lookup"><span data-stu-id="70820-245">If enabled, an offset is added to depth values of a polygon's fragments before the depth comparison is performed, if the polygon is rendered in GL\_POINT mode.</span></span> <span data-ttu-id="70820-246">Vedere [**glPolygonOffset**](glpolygonoffset.md).</span><span class="sxs-lookup"><span data-stu-id="70820-246">See [**glPolygonOffset**](glpolygonoffset.md).</span></span>                                             |
| <span data-ttu-id="70820-247">\_poligono GL \_ smussato</span><span class="sxs-lookup"><span data-stu-id="70820-247">GL\_POLYGON\_SMOOTH</span></span>         | <span data-ttu-id="70820-248">Se abilitata, creare poligoni con filtri appropriati.</span><span class="sxs-lookup"><span data-stu-id="70820-248">If enabled, draw polygons with proper filtering.</span></span> <span data-ttu-id="70820-249">Se disabilitato, creare poligoni con alias.</span><span class="sxs-lookup"><span data-stu-id="70820-249">If disabled, draw aliased polygons.</span></span> <span data-ttu-id="70820-250">Vedere [**glPolygonMode**](glpolygonmode.md).</span><span class="sxs-lookup"><span data-stu-id="70820-250">See [**glPolygonMode**](glpolygonmode.md).</span></span>                                                                                                                            |
| <span data-ttu-id="70820-251">\_stipple poligono GL \_</span><span class="sxs-lookup"><span data-stu-id="70820-251">GL\_POLYGON\_STIPPLE</span></span>        | <span data-ttu-id="70820-252">Se abilitata, usare il modello stipple del poligono corrente durante il rendering dei poligoni.</span><span class="sxs-lookup"><span data-stu-id="70820-252">If enabled, use the current polygon stipple pattern when rendering polygons.</span></span> <span data-ttu-id="70820-253">Vedere [**glPolygonStipple**](glpolygonstipple.md).</span><span class="sxs-lookup"><span data-stu-id="70820-253">See [**glPolygonStipple**](glpolygonstipple.md).</span></span>                                                                                                                              |
| <span data-ttu-id="70820-254">\_test della forbice GL \_</span><span class="sxs-lookup"><span data-stu-id="70820-254">GL\_SCISSOR\_TEST</span></span>           | <span data-ttu-id="70820-255">Se abilitata, eliminare i frammenti esterni al rettangolo a forbice.</span><span class="sxs-lookup"><span data-stu-id="70820-255">If enabled, discard fragments that are outside the scissor rectangle.</span></span> <span data-ttu-id="70820-256">Vedere [**glScissor**](glscissor.md).</span><span class="sxs-lookup"><span data-stu-id="70820-256">See [**glScissor**](glscissor.md).</span></span>                                                                                                                                                   |
| <span data-ttu-id="70820-257">\_test stencil \_ GL</span><span class="sxs-lookup"><span data-stu-id="70820-257">GL\_STENCIL\_TEST</span></span>           | <span data-ttu-id="70820-258">Se abilitata, eseguire il test dello stencil e aggiornare il buffer dello stencil.</span><span class="sxs-lookup"><span data-stu-id="70820-258">If enabled, do stencil testing and update the stencil buffer.</span></span> <span data-ttu-id="70820-259">Vedere [**glStencilFunc**](glstencilfunc.md) e [**glStencilOp**](glstencilop.md).</span><span class="sxs-lookup"><span data-stu-id="70820-259">See [**glStencilFunc**](glstencilfunc.md) and [**glStencilOp**](glstencilop.md).</span></span>                                                                                                            |
| <span data-ttu-id="70820-260">\_Trama GL \_ 1D</span><span class="sxs-lookup"><span data-stu-id="70820-260">GL\_TEXTURE\_1D</span></span>             | <span data-ttu-id="70820-261">Se abilitata, viene eseguita la texturing unidimensionale (a meno che non sia abilitata anche la texturing bidimensionale).</span><span class="sxs-lookup"><span data-stu-id="70820-261">If enabled, one-dimensional texturing is performed (unless two-dimensional texturing is also enabled).</span></span> <span data-ttu-id="70820-262">Vedere [**glTexImage1D**](glteximage1d.md).</span><span class="sxs-lookup"><span data-stu-id="70820-262">See [**glTexImage1D**](glteximage1d.md).</span></span>                                                                                                            |
| <span data-ttu-id="70820-263">\_Trama GL \_ 2D</span><span class="sxs-lookup"><span data-stu-id="70820-263">GL\_TEXTURE\_2D</span></span>             | <span data-ttu-id="70820-264">Se abilitata, viene eseguita la texturing bidimensionale.</span><span class="sxs-lookup"><span data-stu-id="70820-264">If enabled, two-dimensional texturing is performed.</span></span> <span data-ttu-id="70820-265">Vedere [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="70820-265">See [**glTexImage2D**](glteximage2d.md).</span></span>                                                                                                                                                               |
| <span data-ttu-id="70820-266">\_generazione trama \_ GL \_ Q</span><span class="sxs-lookup"><span data-stu-id="70820-266">GL\_TEXTURE\_GEN\_Q</span></span>         | <span data-ttu-id="70820-267">Se abilitata, la coordinata di trama *q* viene calcolata usando la funzione di generazione della trama definita con [**glTexGen**](gltexgen-functions.md).</span><span class="sxs-lookup"><span data-stu-id="70820-267">If enabled, the *q* texture coordinate is computed using the texture-generation function defined with [**glTexGen**](gltexgen-functions.md).</span></span> <span data-ttu-id="70820-268">In caso contrario, viene utilizzata la coordinata di trama *q* corrente.</span><span class="sxs-lookup"><span data-stu-id="70820-268">Otherwise, the current *q* texture coordinate is used.</span></span>                                                        |
| <span data-ttu-id="70820-269">\_generazione trama \_ GL \_ R</span><span class="sxs-lookup"><span data-stu-id="70820-269">GL\_TEXTURE\_GEN\_R</span></span>         | <span data-ttu-id="70820-270">Se abilitata, la coordinata di trama *r* viene calcolata usando la funzione di generazione della trama definita con [**glTexGen**](gltexgen-functions.md).</span><span class="sxs-lookup"><span data-stu-id="70820-270">If enabled, the *r* texture coordinate is computed using the texture generation function defined with [**glTexGen**](gltexgen-functions.md).</span></span> <span data-ttu-id="70820-271">Se è disabilitata, viene utilizzata la coordinata di trama *r* corrente.</span><span class="sxs-lookup"><span data-stu-id="70820-271">If disabled, the current *r* texture coordinate is used.</span></span>                                                      |
| <span data-ttu-id="70820-272">\_generazione trama \_ GL \_</span><span class="sxs-lookup"><span data-stu-id="70820-272">GL\_TEXTURE\_GEN\_S</span></span>         | <span data-ttu-id="70820-273">Se abilitata, la coordinata di trama *s* viene calcolata usando la funzione di generazione della trama definita con **glTexGen**.</span><span class="sxs-lookup"><span data-stu-id="70820-273">If enabled, the *s* texture coordinate is computed using the texture generation function defined with **glTexGen**.</span></span> <span data-ttu-id="70820-274">Se è disabilitata, viene utilizzata la coordinata *di trama corrente* .</span><span class="sxs-lookup"><span data-stu-id="70820-274">If disabled, the current *s* texture coordinate is used.</span></span>                                                                                |
| <span data-ttu-id="70820-275">\_gen trama \_ GL \_ T</span><span class="sxs-lookup"><span data-stu-id="70820-275">GL\_TEXTURE\_GEN\_T</span></span>         | <span data-ttu-id="70820-276">Se abilitata, la coordinata di trama *t* viene calcolata usando la funzione di generazione della trama definita con [**glTexGen**](gltexgen-functions.md).</span><span class="sxs-lookup"><span data-stu-id="70820-276">If enabled, the *t* texture coordinate is computed using the texture generation function defined with [**glTexGen**](gltexgen-functions.md).</span></span> <span data-ttu-id="70820-277">Se è disabilitata, viene utilizzata la coordinata di trama *t* corrente.</span><span class="sxs-lookup"><span data-stu-id="70820-277">If disabled, the current *t* texture coordinate is used.</span></span>                                                      |



 

## <a name="requirements"></a><span data-ttu-id="70820-278">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70820-278">Requirements</span></span>



| <span data-ttu-id="70820-279">Requisito</span><span class="sxs-lookup"><span data-stu-id="70820-279">Requirement</span></span> | <span data-ttu-id="70820-280">Valore</span><span class="sxs-lookup"><span data-stu-id="70820-280">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70820-281">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70820-281">Minimum supported client</span></span><br/> | <span data-ttu-id="70820-282">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="70820-282">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="70820-283">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70820-283">Minimum supported server</span></span><br/> | <span data-ttu-id="70820-284">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="70820-284">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="70820-285">Intestazione</span><span class="sxs-lookup"><span data-stu-id="70820-285">Header</span></span><br/>                   | <dl> <span data-ttu-id="70820-286"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="70820-286"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="70820-287">Libreria</span><span class="sxs-lookup"><span data-stu-id="70820-287">Library</span></span><br/>                  | <dl> <span data-ttu-id="70820-288"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70820-288"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="70820-289">DLL</span><span class="sxs-lookup"><span data-stu-id="70820-289">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70820-290"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70820-290"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70820-291">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="70820-291">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70820-292">**glAlphaFunc**</span><span class="sxs-lookup"><span data-stu-id="70820-292">**glAlphaFunc**</span></span>](glalphafunc.md)
</dt> <dt>

[<span data-ttu-id="70820-293">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="70820-293">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="70820-294">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="70820-294">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="70820-295">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="70820-295">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="70820-296">**glClipPlane**</span><span class="sxs-lookup"><span data-stu-id="70820-296">**glClipPlane**</span></span>](glclipplane.md)
</dt> <dt>

[<span data-ttu-id="70820-297">**glColorMaterial**</span><span class="sxs-lookup"><span data-stu-id="70820-297">**glColorMaterial**</span></span>](glcolormaterial.md)
</dt> <dt>

[<span data-ttu-id="70820-298">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="70820-298">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="70820-299">**glCullFace**</span><span class="sxs-lookup"><span data-stu-id="70820-299">**glCullFace**</span></span>](glcullface.md)
</dt> <dt>

[<span data-ttu-id="70820-300">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="70820-300">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="70820-301">**glDepthRange**</span><span class="sxs-lookup"><span data-stu-id="70820-301">**glDepthRange**</span></span>](gldepthrange.md)
</dt> <dt>

[<span data-ttu-id="70820-302">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="70820-302">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="70820-303">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="70820-303">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="70820-304">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="70820-304">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="70820-305">**Remo**</span><span class="sxs-lookup"><span data-stu-id="70820-305">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="70820-306">**glEvalCoord1**</span><span class="sxs-lookup"><span data-stu-id="70820-306">**glEvalCoord1**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="70820-307">**glEvalMesh1**</span><span class="sxs-lookup"><span data-stu-id="70820-307">**glEvalMesh1**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="70820-308">**glEvalPoint1**</span><span class="sxs-lookup"><span data-stu-id="70820-308">**glEvalPoint1**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="70820-309">**glFog**</span><span class="sxs-lookup"><span data-stu-id="70820-309">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="70820-310">**glGet**</span><span class="sxs-lookup"><span data-stu-id="70820-310">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="70820-311">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="70820-311">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="70820-312">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="70820-312">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="70820-313">**glLight**</span><span class="sxs-lookup"><span data-stu-id="70820-313">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="70820-314">**glLightModel**</span><span class="sxs-lookup"><span data-stu-id="70820-314">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> <dt>

[<span data-ttu-id="70820-315">**glLineWidth**</span><span class="sxs-lookup"><span data-stu-id="70820-315">**glLineWidth**</span></span>](gllinewidth.md)
</dt> <dt>

[<span data-ttu-id="70820-316">**glLineStipple**</span><span class="sxs-lookup"><span data-stu-id="70820-316">**glLineStipple**</span></span>](gllinestipple.md)
</dt> <dt>

[<span data-ttu-id="70820-317">**glLogicOp**</span><span class="sxs-lookup"><span data-stu-id="70820-317">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="70820-318">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="70820-318">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="70820-319">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="70820-319">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="70820-320">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="70820-320">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="70820-321">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="70820-321">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="70820-322">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="70820-322">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="70820-323">**glPointSize**</span><span class="sxs-lookup"><span data-stu-id="70820-323">**glPointSize**</span></span>](glpointsize.md)
</dt> <dt>

[<span data-ttu-id="70820-324">**glPolygonMode**</span><span class="sxs-lookup"><span data-stu-id="70820-324">**glPolygonMode**</span></span>](glpolygonmode.md)
</dt> <dt>

[<span data-ttu-id="70820-325">**glPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="70820-325">**glPolygonStipple**</span></span>](glpolygonstipple.md)
</dt> <dt>

[<span data-ttu-id="70820-326">**glScissor**</span><span class="sxs-lookup"><span data-stu-id="70820-326">**glScissor**</span></span>](glscissor.md)
</dt> <dt>

[<span data-ttu-id="70820-327">**glStencilFunc**</span><span class="sxs-lookup"><span data-stu-id="70820-327">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> <dt>

[<span data-ttu-id="70820-328">**glStencilOp**</span><span class="sxs-lookup"><span data-stu-id="70820-328">**glStencilOp**</span></span>](glstencilop.md)
</dt> <dt>

[<span data-ttu-id="70820-329">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="70820-329">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="70820-330">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="70820-330">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="70820-331">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="70820-331">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="70820-332">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="70820-332">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> </dl>

 

 





