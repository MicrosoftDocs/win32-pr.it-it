---
title: funzione glTexGend (GL. h)
description: Controlla la generazione delle coordinate di trama. | funzione glTexGend (GL. h)
ms.assetid: 75ab3468-281d-4c8d-95cc-138d75646cdf
keywords:
- funzione glTexGend OpenGL
topic_type:
- apiref
api_name:
- glTexGend
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45854eb1e2070f334bfc906c249fbb4341ab74d0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104560330"
---
# <a name="gltexgend-function"></a><span data-ttu-id="1aa61-105">glTexGend (funzione)</span><span class="sxs-lookup"><span data-stu-id="1aa61-105">glTexGend function</span></span>

<span data-ttu-id="1aa61-106">Controlla la generazione delle coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="1aa61-106">Controls the generation of texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="1aa61-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1aa61-107">Syntax</span></span>


```C++
void WINAPI glTexGend(
   GLenum   coord,
   GLenum   pname,
   GLdouble param
);
```



## <a name="parameters"></a><span data-ttu-id="1aa61-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1aa61-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1aa61-109">*Coord*</span><span class="sxs-lookup"><span data-stu-id="1aa61-109">*coord*</span></span> 
</dt> <dd>

<span data-ttu-id="1aa61-110">Coordinata di trama.</span><span class="sxs-lookup"><span data-stu-id="1aa61-110">A texture coordinate.</span></span> <span data-ttu-id="1aa61-111">Deve essere uno dei seguenti: GL \_ S, GL \_ T, GL \_ R o GL \_ Q.</span><span class="sxs-lookup"><span data-stu-id="1aa61-111">Must be one of the following: GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span>

</dd> <dt>

<span data-ttu-id="1aa61-112">**pname**</span><span class="sxs-lookup"><span data-stu-id="1aa61-112">**pname**</span></span> 
</dt> <dd>

<span data-ttu-id="1aa61-113">Nome simbolico della funzione di generazione delle coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="1aa61-113">The symbolic name of the texture coordinate generation function.</span></span>

</dd> <dt>

<span data-ttu-id="1aa61-114">*param*</span><span class="sxs-lookup"><span data-stu-id="1aa61-114">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="1aa61-115">Un parametro di generazione della trama a valore singolo, uno tra GL \_ Object \_ Linear, GL \_ Eye \_ Linear o GL \_ Sphere \_ map.</span><span class="sxs-lookup"><span data-stu-id="1aa61-115">A single valued texture generation parameter, one of GL\_OBJECT\_LINEAR, GL\_EYE\_LINEAR, or GL\_SPHERE\_MAP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1aa61-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1aa61-116">Return value</span></span>

<span data-ttu-id="1aa61-117">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="1aa61-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1aa61-118">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="1aa61-118">Error codes</span></span>

<span data-ttu-id="1aa61-119">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="1aa61-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="1aa61-120">Nome</span><span class="sxs-lookup"><span data-stu-id="1aa61-120">Name</span></span>                                                                                                  | <span data-ttu-id="1aa61-121">Significato</span><span class="sxs-lookup"><span data-stu-id="1aa61-121">Meaning</span></span>                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1aa61-122"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1aa61-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="1aa61-123">*Coord* o *pname* non è un valore definito accettato oppure *pname* è la \_ \_ modalità di generazione della trama GL \_ e *params* non è un valore definito accettato.</span><span class="sxs-lookup"><span data-stu-id="1aa61-123">*coord* or *pname* was not an accepted defined value, or *pname* was GL\_TEXTURE\_GEN\_MODE and *params* was not an accepted defined value.</span></span><br/> |
| <dl> <span data-ttu-id="1aa61-124"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1aa61-124"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="1aa61-125">*pname* è la \_ modalità di generazione della trama GL \_ \_ , *params* è la \_ mappa GL sphere \_ e *Coord* è stato GL \_ R o GL \_ Q</span><span class="sxs-lookup"><span data-stu-id="1aa61-125">*pname* was GL\_TEXTURE\_GEN\_MODE, *params* was GL\_SPHERE\_MAP, and *coord* was either GL\_R or GL\_Q</span></span><br/>                                     |
| <dl> <span data-ttu-id="1aa61-126"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1aa61-126"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="1aa61-127">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="1aa61-127">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <br/>                 |



## <a name="remarks"></a><span data-ttu-id="1aa61-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="1aa61-128">Remarks</span></span>

<span data-ttu-id="1aa61-129">La funzione **glTexGen** seleziona una funzione di generazione della coordinata di trama o fornisce coefficienti per una delle funzioni.</span><span class="sxs-lookup"><span data-stu-id="1aa61-129">The **glTexGen** function selects a texture-coordinate generation function or supplies coefficients for one of the functions.</span></span> <span data-ttu-id="1aa61-130">Il parametro *Coord* denomina una delle coordinate di trama (s, t, r, q) e deve essere uno dei simboli seguenti: GL \_ s, GL \_ t, GL \_ r o GL \_ q.</span><span class="sxs-lookup"><span data-stu-id="1aa61-130">The *coord* parameter names one of the (s,t,r,q) texture coordinates, and it must be one of these symbols: GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span> <span data-ttu-id="1aa61-131">Il parametro *pname* deve essere una delle tre costanti simboliche, ovvero la \_ modalità gen della trama GL, il piano dell' \_ \_ oggetto GL o il \_ \_ piano GL \_ Eye \_ .</span><span class="sxs-lookup"><span data-stu-id="1aa61-131">The *pname* parameter must be one of three symbolic constants: GL\_TEXTURE\_GEN\_MODE, GL\_OBJECT\_PLANE, or GL\_EYE\_PLANE.</span></span> <span data-ttu-id="1aa61-132">Se *pname* è \_ la modalità di generazione della trama GL \_ \_ , *param* specifica una modalità, una della \_ mappa GL Object \_ Linear, GL \_ Eye \_ Linear o GL \_ Sphere \_ .</span><span class="sxs-lookup"><span data-stu-id="1aa61-132">If *pname* is GL\_TEXTURE\_GEN\_MODE, then *param* specifies a mode, one of GL\_OBJECT\_LINEAR, GL\_EYE\_LINEAR, or GL\_SPHERE\_MAP.</span></span> <span data-ttu-id="1aa61-133">Se *pname* è un piano \_ di oggetti GL \_ o \_ \_ un piano con occhio GL, *param* contiene coefficienti per la funzione di generazione della trama corrispondente.</span><span class="sxs-lookup"><span data-stu-id="1aa61-133">If *pname* is either GL\_OBJECT\_PLANE or GL\_EYE\_PLANE, *param* contains coefficients for the corresponding texture generation function.</span></span>

<span data-ttu-id="1aa61-134">Se la funzione di generazione della trama è un \_ oggetto GL \_ lineare, la funzione</span><span class="sxs-lookup"><span data-stu-id="1aa61-134">If the texture generation function is GL\_OBJECT\_LINEAR, the function</span></span>

![Equazione che mostra la funzione glTexGen quando viene GL_OBJECT_LINEAR la funzione di generazione della trama.](images/tex02.png)

<span data-ttu-id="1aa61-136">viene usato, dove g è il valore calcolato per la coordinata denominata in Coord; P1, P2, P3 e P4 sono i quattro valori specificati nei parametri; e x?, y?, z? e w? sono le coordinate dell'oggetto del vertice.</span><span class="sxs-lookup"><span data-stu-id="1aa61-136">is used, where g is the value computed for the coordinate named in coord; p1, p2, p3, and p4 are the four values supplied in params; and x?, y?, z?, and w? are the object coordinates of the vertex.</span></span> <span data-ttu-id="1aa61-137">È possibile usare questa funzione per mappare il terreno usando il livello Sea come piano di riferimento (definito da P1, P2, P3 e P4).</span><span class="sxs-lookup"><span data-stu-id="1aa61-137">You can use this function to texture-map terrain by using sea level as a reference plane (defined by p1, p2, p3, and p4).</span></span> <span data-ttu-id="1aa61-138">La \_ \_ funzione di generazione delle coordinate lineari dell'oggetto GL calcola l'altitudine di un vertice del terreno come distanza dal livello Sea. tale altitudine viene utilizzata per indicizzare l'immagine della trama per eseguire il mapping della neve bianca ai picchi e all'erba verde sui piedi, ad esempio.</span><span class="sxs-lookup"><span data-stu-id="1aa61-138">The GL\_OBJECT\_LINEAR coordinate generation function computes the altitude of a terrain vertex as its distance from sea level; that altitude is used to index the texture image to map white snow onto peaks and green grass onto foothills, for example.</span></span>

<span data-ttu-id="1aa61-139">Se la funzione di generazione della trama è GL \_ Eye \_ lineare, la funzione</span><span class="sxs-lookup"><span data-stu-id="1aa61-139">If the texture generation function is GL\_EYE\_LINEAR, the function</span></span>

![Equazione che mostra la funzione glTexGen quando viene GL_EYE_LINEAR la funzione di generazione della trama.](images/tex02.png)

<span data-ttu-id="1aa61-141">viene usato, dove</span><span class="sxs-lookup"><span data-stu-id="1aa61-141">is used, where</span></span>

![Equazione che mostra le coordinate oculari del vertice.](images/tex03.png)

<span data-ttu-id="1aa61-143">e x?, y?, z? e w? sono le coordinate oculari dei vertici, P1, P2, P3 e P4 sono i valori specificati in *param* e M è la matrice Modelview quando si chiama **glTexGen**.</span><span class="sxs-lookup"><span data-stu-id="1aa61-143">and x?, y?, z?, and w? are the eye coordinates of the vertex, p1, p2, p3, and p4 are the values supplied in *param*, and M is the modelview matrix when you call **glTexGen**.</span></span> <span data-ttu-id="1aa61-144">Se M è scarsamente condizionato o singolare, le coordinate di trama generate dalla funzione risultante possono non essere accurate o indefinite.</span><span class="sxs-lookup"><span data-stu-id="1aa61-144">If M is poorly conditioned or singular, texture coordinates generated by the resulting function can be inaccurate or undefined.</span></span>

<span data-ttu-id="1aa61-145">I valori in *param* definiscono un piano di riferimento in coordinate oculari.</span><span class="sxs-lookup"><span data-stu-id="1aa61-145">The values in *param* define a reference plane in eye coordinates.</span></span> <span data-ttu-id="1aa61-146">La matrice Modelview che viene applicata a tali elementi non può essere la stessa in vigore quando i vertici del poligono sono trasformati.</span><span class="sxs-lookup"><span data-stu-id="1aa61-146">The modelview matrix that is applied to them cannot be the same one in effect when the polygon vertices are transformed.</span></span> <span data-ttu-id="1aa61-147">Questa funzione stabilisce un campo di coordinate di trama che può produrre linee di contorno dinamiche sullo stato degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="1aa61-147">This function establishes a field of texture coordinates that can produce dynamic contour lines on moving objects.</span></span>

<span data-ttu-id="1aa61-148">Se *pname* è \_ \_ una mappa GL Sphere e *Coord* è GL \_ S o GL \_ T, le coordinate di trama S e T vengono generate come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="1aa61-148">If *pname* is GL\_SPHERE\_MAP and *coord* is either GL\_S or GL\_T, s and t texture coordinates are generated as follows.</span></span> <span data-ttu-id="1aa61-149">Consentire a u il vettore di unità che punta dall'origine al vertice del poligono (in coordinate oculari).</span><span class="sxs-lookup"><span data-stu-id="1aa61-149">Let u be the unit vector pointing from the origin to the polygon vertex (in eye coordinates).</span></span> <span data-ttu-id="1aa61-150">Let n è il normale corrente, dopo la trasformazione in coordinate oculari.</span><span class="sxs-lookup"><span data-stu-id="1aa61-150">Let n  be the current normal, after transformation to eye coordinates.</span></span> <span data-ttu-id="1aa61-151">Let f = (FX () FY () FZ) T è il vettore di reflection in modo che</span><span class="sxs-lookup"><span data-stu-id="1aa61-151">Let f = (fx ( ) fy ( ) fz)T be the reflection vector such that</span></span>

![Equazione che mostra il vettore di reflection come funzione del vettore di unità e della normale corrente.](images/tex05.png)

<span data-ttu-id="1aa61-153">Infine, Let</span><span class="sxs-lookup"><span data-stu-id="1aa61-153">Finally, let</span></span>

![Equazione che Mostra m come funzione del vettore di Reflection.](images/tex07.png)

<span data-ttu-id="1aa61-155">Quindi i valori assegnati alle coordinate di trama i e t sono</span><span class="sxs-lookup"><span data-stu-id="1aa61-155">Then the values assigned to the i and t texture coordinates are</span></span>

![Equazione che mostra i valori assegnati alle coordinate di trama i e t.](images/tex06.png)

<span data-ttu-id="1aa61-157">È possibile abilitare o disabilitare una funzione di generazione della coordinata di trama usando [**glEnable**](glenable.md) o [**glDisable**](gldisable.md) con uno dei nomi di coordinati di trama simbolici (GL texture gen \_ \_ \_ S, GL \_ texture \_ gen \_ T, GL \_ texture \_ gen \_ R o GL \_ texture \_ gen \_ Q) come argomento.</span><span class="sxs-lookup"><span data-stu-id="1aa61-157">You can enable or disable a texture-coordinate generation function by using [**glEnable**](glenable.md) or [**glDisable**](gldisable.md) with one of the symbolic texture-coordinate names (GL\_TEXTURE\_GEN\_S, GL\_TEXTURE\_GEN\_T, GL\_TEXTURE\_GEN\_R, or GL\_TEXTURE\_GEN\_Q) as the argument.</span></span> <span data-ttu-id="1aa61-158">Quando questa funzione è abilitata, la coordinata di trama specificata viene calcolata in base alla funzione di generazione associata a tale coordinata.</span><span class="sxs-lookup"><span data-stu-id="1aa61-158">When this function is enabled, the specified texture coordinate is computed according to the generating function associated with that coordinate.</span></span> <span data-ttu-id="1aa61-159">Quando la funzione è disabilitata, i vertici successivi accettano la coordinata di trama specificata dal set corrente di coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="1aa61-159">When the function is disabled, subsequent vertices take the specified texture coordinate from the current set of texture coordinates.</span></span> <span data-ttu-id="1aa61-160">Inizialmente, tutte le funzioni di generazione di trama sono impostate su GL \_ Eye \_ Linear e sono disabilitate.</span><span class="sxs-lookup"><span data-stu-id="1aa61-160">Initially, all texture generation functions are set to GL\_EYE\_LINEAR and are disabled.</span></span> <span data-ttu-id="1aa61-161">Entrambe le equazioni del piano s sono (1, 0, 0, 0); entrambe le equazioni del piano t sono (0, 1, 0, 0); e tutte le equazioni del piano r e q sono (0, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="1aa61-161">Both s plane equations are (1,0,0,0); both t plane equations are (0,1,0,0); and all r and q plane equations are (0,0,0,0).</span></span>

<span data-ttu-id="1aa61-162">Le funzioni seguenti consentono di recuperare informazioni correlate a glTexGen:</span><span class="sxs-lookup"><span data-stu-id="1aa61-162">The following functions retrieve information related to glTexGen:</span></span>

<dl>

[<span data-ttu-id="1aa61-163">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="1aa61-163">**glGetTexGen**</span></span>](glgettexgen.md)  
<span data-ttu-id="1aa61-164">[**glIsEnabled**](glisenabled.md) con argomento GL \_ texture \_ gen \_ S</span><span class="sxs-lookup"><span data-stu-id="1aa61-164">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_S</span></span>  
<span data-ttu-id="1aa61-165">[**glIsEnabled**](glisenabled.md) con argomento GL \_ texture \_ gen \_ T</span><span class="sxs-lookup"><span data-stu-id="1aa61-165">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_T</span></span>  
<span data-ttu-id="1aa61-166">[**glIsEnabled**](glisenabled.md) con argomento GL \_ texture \_ gen \_ R</span><span class="sxs-lookup"><span data-stu-id="1aa61-166">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_R</span></span>  
<span data-ttu-id="1aa61-167">[**glIsEnabled**](glisenabled.md) con argomento GL \_ texture \_ gen \_ Q</span><span class="sxs-lookup"><span data-stu-id="1aa61-167">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_Q</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="1aa61-168">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1aa61-168">Requirements</span></span>



| <span data-ttu-id="1aa61-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="1aa61-169">Requirement</span></span> | <span data-ttu-id="1aa61-170">Valore</span><span class="sxs-lookup"><span data-stu-id="1aa61-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1aa61-171">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1aa61-171">Minimum supported client</span></span><br/> | <span data-ttu-id="1aa61-172">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1aa61-172">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1aa61-173">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1aa61-173">Minimum supported server</span></span><br/> | <span data-ttu-id="1aa61-174">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1aa61-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1aa61-175">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1aa61-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="1aa61-176"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="1aa61-176"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1aa61-177">Libreria</span><span class="sxs-lookup"><span data-stu-id="1aa61-177">Library</span></span><br/>                  | <dl> <span data-ttu-id="1aa61-178"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1aa61-178"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1aa61-179">DLL</span><span class="sxs-lookup"><span data-stu-id="1aa61-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1aa61-180"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1aa61-180"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1aa61-181">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1aa61-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1aa61-182">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="1aa61-182">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="1aa61-183">**Remo**</span><span class="sxs-lookup"><span data-stu-id="1aa61-183">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="1aa61-184">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="1aa61-184">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="1aa61-185">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="1aa61-185">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="1aa61-186">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="1aa61-186">**glGetTexGen**</span></span>](glgettexgen.md)
</dt> <dt>

[<span data-ttu-id="1aa61-187">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="1aa61-187">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="1aa61-188">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="1aa61-188">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="1aa61-189">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="1aa61-189">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="1aa61-190">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="1aa61-190">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> <dt>

[<span data-ttu-id="1aa61-191">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="1aa61-191">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="1aa61-192">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="1aa61-192">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> </dl>

 

 





