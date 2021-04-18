---
title: funzione glTexGendv (GL. h)
description: Controlla la generazione delle coordinate di trama. | funzione glTexGendv (GL. h)
ms.assetid: fe0e28e4-50d3-473f-a290-7745a1718618
keywords:
- funzione glTexGendv OpenGL
topic_type:
- apiref
api_name:
- glTexGendv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eccae96a6289d2172115763b6b6117bf184e2eb8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104565001"
---
# <a name="gltexgendv-function"></a><span data-ttu-id="465f5-105">glTexGendv (funzione)</span><span class="sxs-lookup"><span data-stu-id="465f5-105">glTexGendv function</span></span>

<span data-ttu-id="465f5-106">Controlla la generazione delle coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="465f5-106">Controls the generation of texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="465f5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="465f5-107">Syntax</span></span>


```C++
void WINAPI glTexGendv(
         GLenum   coord,
         GLenum   pname,
   const GLdouble *params
);
```



## <a name="parameters"></a><span data-ttu-id="465f5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="465f5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="465f5-109">*Coord*</span><span class="sxs-lookup"><span data-stu-id="465f5-109">*coord*</span></span> 
</dt> <dd>

<span data-ttu-id="465f5-110">Coordinata di trama.</span><span class="sxs-lookup"><span data-stu-id="465f5-110">A texture coordinate.</span></span> <span data-ttu-id="465f5-111">Deve essere uno dei seguenti: GL \_ S, GL \_ T, GL \_ R o GL \_ Q.</span><span class="sxs-lookup"><span data-stu-id="465f5-111">Must be one of the following: GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span>

</dd> <dt>

<span data-ttu-id="465f5-112">**pname**</span><span class="sxs-lookup"><span data-stu-id="465f5-112">**pname**</span></span> 
</dt> <dd>

<span data-ttu-id="465f5-113">Nome simbolico della funzione di generazione delle coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="465f5-113">The symbolic name of the texture coordinate generation function.</span></span>

</dd> <dt>

<span data-ttu-id="465f5-114">*params*</span><span class="sxs-lookup"><span data-stu-id="465f5-114">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="465f5-115">Matrice che contiene i coefficienti per la funzione di generazione della trama corrispondente.</span><span class="sxs-lookup"><span data-stu-id="465f5-115">An array that contains the coefficients for the corresponding texture generation function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="465f5-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="465f5-116">Return value</span></span>

<span data-ttu-id="465f5-117">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="465f5-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="465f5-118">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="465f5-118">Error codes</span></span>

<span data-ttu-id="465f5-119">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="465f5-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="465f5-120">Nome</span><span class="sxs-lookup"><span data-stu-id="465f5-120">Name</span></span>                                                                                                  | <span data-ttu-id="465f5-121">Significato</span><span class="sxs-lookup"><span data-stu-id="465f5-121">Meaning</span></span>                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="465f5-122"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="465f5-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="465f5-123">*Coord* o *pname* non è un valore definito accettato oppure *pname* è la \_ \_ modalità di generazione della trama GL \_ e *params* non è un valore definito accettato.</span><span class="sxs-lookup"><span data-stu-id="465f5-123">*coord* or *pname* was not an accepted defined value, or *pname* was GL\_TEXTURE\_GEN\_MODE and *params* was not an accepted defined value.</span></span><br/> |
| <dl> <span data-ttu-id="465f5-124"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="465f5-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="465f5-125">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="465f5-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <br/>                 |



## <a name="remarks"></a><span data-ttu-id="465f5-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="465f5-126">Remarks</span></span>

<span data-ttu-id="465f5-127">La funzione **glTexGen** seleziona una funzione di generazione della coordinata di trama o fornisce coefficienti per una delle funzioni.</span><span class="sxs-lookup"><span data-stu-id="465f5-127">The **glTexGen** function selects a texture-coordinate generation function or supplies coefficients for one of the functions.</span></span> <span data-ttu-id="465f5-128">Il parametro *Coord* denomina una delle coordinate di trama (s, t, r, q) e deve essere uno dei simboli seguenti: GL \_ s, GL \_ t, GL \_ r o GL \_ q.</span><span class="sxs-lookup"><span data-stu-id="465f5-128">The *coord* parameter names one of the (s,t,r,q) texture coordinates, and it must be one of these symbols: GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span> <span data-ttu-id="465f5-129">Il parametro *pname* deve essere una delle tre costanti simboliche, ovvero la \_ modalità gen della trama GL, il piano dell' \_ \_ oggetto GL o il \_ \_ piano GL \_ Eye \_ .</span><span class="sxs-lookup"><span data-stu-id="465f5-129">The *pname* parameter must be one of three symbolic constants: GL\_TEXTURE\_GEN\_MODE, GL\_OBJECT\_PLANE, or GL\_EYE\_PLANE.</span></span> <span data-ttu-id="465f5-130">Se *pname* è un piano \_ di oggetti GL \_ o \_ \_ un piano con occhio GL, *param* contiene coefficienti per la funzione di generazione della trama corrispondente.</span><span class="sxs-lookup"><span data-stu-id="465f5-130">If *pname* is either GL\_OBJECT\_PLANE or GL\_EYE\_PLANE, *param* contains coefficients for the corresponding texture generation function.</span></span>

<span data-ttu-id="465f5-131">Se la funzione di generazione della trama è un \_ oggetto GL \_ lineare, la funzione</span><span class="sxs-lookup"><span data-stu-id="465f5-131">If the texture generation function is GL\_OBJECT\_LINEAR, the function</span></span>

<span data-ttu-id="465f5-132">! [Equazione che mostra la funzione glTexGen quando la funzione di generazione della trama è GL_OBJECT_LINEAR.]</span><span class="sxs-lookup"><span data-stu-id="465f5-132">![Equation showing the glTexGen function when the texture generation function is GL_OBJECT_LINEAR.]</span></span>

<span data-ttu-id="465f5-133">viene usato, dove g è il valore calcolato per la coordinata denominata in Coord; P1, P2, P3 e P4 sono i quattro valori specificati nei parametri; e x?, y?, z? e w? sono le coordinate dell'oggetto del vertice.</span><span class="sxs-lookup"><span data-stu-id="465f5-133">is used, where g is the value computed for the coordinate named in coord; p1, p2, p3, and p4 are the four values supplied in params; and x?, y?, z?, and w? are the object coordinates of the vertex.</span></span> <span data-ttu-id="465f5-134">È possibile usare questa funzione per mappare il terreno usando il livello Sea come piano di riferimento (definito da P1, P2, P3 e P4).</span><span class="sxs-lookup"><span data-stu-id="465f5-134">You can use this function to texture-map terrain by using sea level as a reference plane (defined by p1, p2, p3, and p4).</span></span> <span data-ttu-id="465f5-135">La \_ \_ funzione di generazione delle coordinate lineari dell'oggetto GL calcola l'altitudine di un vertice del terreno come distanza dal livello Sea. tale altitudine viene utilizzata per indicizzare l'immagine della trama per eseguire il mapping della neve bianca ai picchi e all'erba verde sui piedi, ad esempio.</span><span class="sxs-lookup"><span data-stu-id="465f5-135">The GL\_OBJECT\_LINEAR coordinate generation function computes the altitude of a terrain vertex as its distance from sea level; that altitude is used to index the texture image to map white snow onto peaks and green grass onto foothills, for example.</span></span>

<span data-ttu-id="465f5-136">Se la funzione di generazione della trama è GL \_ Eye \_ lineare, la funzione</span><span class="sxs-lookup"><span data-stu-id="465f5-136">If the texture generation function is GL\_EYE\_LINEAR, the function</span></span>

<span data-ttu-id="465f5-137">! [Equazione che mostra la funzione glTexGen quando la funzione di generazione della trama è GL_EYE_LINEAR.]</span><span class="sxs-lookup"><span data-stu-id="465f5-137">![Equation showing the glTexGen function when the texture generation function is GL_EYE_LINEAR.]</span></span>

<span data-ttu-id="465f5-138">viene usato, dove</span><span class="sxs-lookup"><span data-stu-id="465f5-138">is used, where</span></span>

![Equazione che mostra le coordinate oculari del vertice.](images/tex03.png)

<span data-ttu-id="465f5-140">e x?, y?, z? e w? le coordinate oculari dei vertici, P1, P2, P3 e P4 sono i valori specificati in *param* e M è la matrice Modelview quando si **callglTexGen**.</span><span class="sxs-lookup"><span data-stu-id="465f5-140">and x?, y?, z?, and w? are the eye coordinates of the vertex, p1, p2, p3, and p4 are the values supplied in *param*, and M is the modelview matrix when you **callglTexGen**.</span></span> <span data-ttu-id="465f5-141">Se M è scarsamente condizionato o singolare, le coordinate di trama generate dalla funzione risultante possono non essere accurate o indefinite.</span><span class="sxs-lookup"><span data-stu-id="465f5-141">If M is poorly conditioned or singular, texture coordinates generated by the resulting function can be inaccurate or undefined.</span></span>

<span data-ttu-id="465f5-142">Si noti che i valori in *param* definiscono un piano di riferimento in coordinate oculari.</span><span class="sxs-lookup"><span data-stu-id="465f5-142">Note that the values in *param* define a reference plane in eye coordinates.</span></span> <span data-ttu-id="465f5-143">La matrice Modelview applicata a esse potrebbe non essere la stessa in vigore quando i vertici del poligono sono trasformati.</span><span class="sxs-lookup"><span data-stu-id="465f5-143">The modelview matrix that is applied to them may not be the same one in effect when the polygon vertices are transformed.</span></span> <span data-ttu-id="465f5-144">Questa funzione stabilisce un campo di coordinate di trama che può produrre linee di contorno dinamiche sullo stato degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="465f5-144">This function establishes a field of texture coordinates that can produce dynamic contour lines on moving objects.</span></span>

<span data-ttu-id="465f5-145">Se *pname* è \_ \_ una mappa GL Sphere e *Coord* è GL \_ S o GL \_ T, le coordinate di trama S e T vengono generate come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="465f5-145">If *pname* is GL\_SPHERE\_MAP and *coord* is either GL\_S or GL\_T, s and t texture coordinates are generated as follows.</span></span> <span data-ttu-id="465f5-146">Consentire a u il vettore di unità che punta dall'origine al vertice del poligono (in coordinate oculari).</span><span class="sxs-lookup"><span data-stu-id="465f5-146">Let u be the unit vector pointing from the origin to the polygon vertex (in eye coordinates).</span></span> <span data-ttu-id="465f5-147">Let n è il normale corrente, dopo la trasformazione in coordinate oculari.</span><span class="sxs-lookup"><span data-stu-id="465f5-147">Let n  be the current normal, after transformation to eye coordinates.</span></span> <span data-ttu-id="465f5-148">Let f = (FX () FY () FZ) T è il vettore di reflection in modo che</span><span class="sxs-lookup"><span data-stu-id="465f5-148">Let f = (fx ( ) fy ( ) fz)T be the reflection vector such that</span></span>

![Equazione che mostra il vettore di reflection come funzione del vettore di unità e della normale corrente.](images/tex05.png)

<span data-ttu-id="465f5-150">Infine, Let</span><span class="sxs-lookup"><span data-stu-id="465f5-150">Finally, let</span></span>

![Equazione che Mostra m come funzione del vettore di Reflection.](images/tex07.png)

<span data-ttu-id="465f5-152">Quindi i valori assegnati alle coordinate di trama i e t sono</span><span class="sxs-lookup"><span data-stu-id="465f5-152">Then the values assigned to the i and t texture coordinates are</span></span>

![Equazione che mostra i valori assegnati alle coordinate di trama i e t.](images/tex06.png)

<span data-ttu-id="465f5-154">È possibile abilitare o disabilitare una funzione di generazione della coordinata di trama usando [**glEnable**](glenable.md) o [**glDisable**](gldisable.md) con uno dei nomi di coordinati di trama simbolici (GL texture gen \_ \_ \_ S, GL \_ texture \_ gen \_ T, GL \_ texture \_ gen \_ R o GL \_ texture \_ gen \_ Q) come argomento.</span><span class="sxs-lookup"><span data-stu-id="465f5-154">You can enable or disable a texture-coordinate generation function by using [**glEnable**](glenable.md) or [**glDisable**](gldisable.md) with one of the symbolic texture-coordinate names (GL\_TEXTURE\_GEN\_S, GL\_TEXTURE\_GEN\_T, GL\_TEXTURE\_GEN\_R, or GL\_TEXTURE\_GEN\_Q) as the argument.</span></span> <span data-ttu-id="465f5-155">Quando questa funzione è abilitata, la coordinata di trama specificata viene calcolata in base alla funzione di generazione associata a tale coordinata.</span><span class="sxs-lookup"><span data-stu-id="465f5-155">When this function is enabled, the specified texture coordinate is computed according to the generating function associated with that coordinate.</span></span> <span data-ttu-id="465f5-156">Quando questa funzione è disabilitata, i vertici successivi accettano la coordinata di trama specificata dal set corrente di coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="465f5-156">When this function is disabled, subsequent vertices take the specified texture coordinate from the current set of texture coordinates.</span></span> <span data-ttu-id="465f5-157">Inizialmente, tutte le funzioni di generazione di trama sono impostate su GL \_ Eye \_ Linear e sono disabilitate.</span><span class="sxs-lookup"><span data-stu-id="465f5-157">Initially, all texture generation functions are set to GL\_EYE\_LINEAR and are disabled.</span></span> <span data-ttu-id="465f5-158">Entrambe le equazioni del piano s sono (1, 0, 0, 0); entrambe le equazioni del piano t sono (0, 1, 0, 0); e tutte le equazioni del piano r e q sono (0, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="465f5-158">Both s plane equations are (1,0,0,0); both t plane equations are (0,1,0,0); and all r and q plane equations are (0,0,0,0).</span></span>

<span data-ttu-id="465f5-159">Le funzioni seguenti consentono di recuperare informazioni correlate a glTexGen:</span><span class="sxs-lookup"><span data-stu-id="465f5-159">The following functions retrieve information related to glTexGen:</span></span>

<dl>

[<span data-ttu-id="465f5-160">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="465f5-160">**glGetTexGen**</span></span>](glgettexgen.md)  
<span data-ttu-id="465f5-161">[**glIsEnabled**](glisenabled.md) con argomento GL \_ texture \_ gen \_ S</span><span class="sxs-lookup"><span data-stu-id="465f5-161">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_S</span></span>  
<span data-ttu-id="465f5-162">[**glIsEnabled**](glisenabled.md) con argomento GL \_ texture \_ gen \_ T</span><span class="sxs-lookup"><span data-stu-id="465f5-162">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_T</span></span>  
<span data-ttu-id="465f5-163">[**glIsEnabled**](glisenabled.md) con argomento GL \_ texture \_ gen \_ R</span><span class="sxs-lookup"><span data-stu-id="465f5-163">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_R</span></span>  
<span data-ttu-id="465f5-164">[**glIsEnabled**](glisenabled.md) con argomento GL \_ texture \_ gen \_ Q</span><span class="sxs-lookup"><span data-stu-id="465f5-164">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_Q</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="465f5-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="465f5-165">Requirements</span></span>



| <span data-ttu-id="465f5-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="465f5-166">Requirement</span></span> | <span data-ttu-id="465f5-167">Valore</span><span class="sxs-lookup"><span data-stu-id="465f5-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="465f5-168">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="465f5-168">Minimum supported client</span></span><br/> | <span data-ttu-id="465f5-169">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="465f5-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="465f5-170">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="465f5-170">Minimum supported server</span></span><br/> | <span data-ttu-id="465f5-171">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="465f5-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="465f5-172">Intestazione</span><span class="sxs-lookup"><span data-stu-id="465f5-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="465f5-173"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="465f5-173"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="465f5-174">Libreria</span><span class="sxs-lookup"><span data-stu-id="465f5-174">Library</span></span><br/>                  | <dl> <span data-ttu-id="465f5-175"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="465f5-175"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="465f5-176">DLL</span><span class="sxs-lookup"><span data-stu-id="465f5-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="465f5-177"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="465f5-177"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="465f5-178">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="465f5-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="465f5-179">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="465f5-179">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="465f5-180">**Remo**</span><span class="sxs-lookup"><span data-stu-id="465f5-180">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="465f5-181">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="465f5-181">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="465f5-182">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="465f5-182">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="465f5-183">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="465f5-183">**glGetTexGen**</span></span>](glgettexgen.md)
</dt> <dt>

[<span data-ttu-id="465f5-184">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="465f5-184">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="465f5-185">glTexEnv</span><span class="sxs-lookup"><span data-stu-id="465f5-185">glTexEnv</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="465f5-186">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="465f5-186">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="465f5-187">glTexParameter</span><span class="sxs-lookup"><span data-stu-id="465f5-187">glTexParameter</span></span>](gltexparameter-functions.md)
</dt> <dt>

[<span data-ttu-id="465f5-188">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="465f5-188">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="465f5-189">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="465f5-189">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> </dl>

 

 





