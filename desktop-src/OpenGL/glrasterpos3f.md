---
title: funzione glRasterPos3f (GL. h)
description: Specifica la posizione raster per le operazioni sui pixel. | funzione glRasterPos3f (GL. h)
ms.assetid: edb3b114-fd65-40f6-8fba-5306b8b89c11
keywords:
- funzione glRasterPos3f OpenGL
topic_type:
- apiref
api_name:
- glRasterPos3f
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16477623730f54f19d4f7596af4cb7e4e1dd92d7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321306"
---
# <a name="glrasterpos3f-function"></a><span data-ttu-id="6312a-105">glRasterPos3f (funzione)</span><span class="sxs-lookup"><span data-stu-id="6312a-105">glRasterPos3f function</span></span>

<span data-ttu-id="6312a-106">Specifica la posizione raster per le operazioni sui pixel.</span><span class="sxs-lookup"><span data-stu-id="6312a-106">Specifies the raster position for pixel operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="6312a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6312a-107">Syntax</span></span>


```C++
void WINAPI glRasterPos3f(
   GLfloat x,
   GLfloat y,
   GLfloat z
);
```



## <a name="parameters"></a><span data-ttu-id="6312a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6312a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6312a-109">*x*</span><span class="sxs-lookup"><span data-stu-id="6312a-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="6312a-110">Specifica la coordinata x della posizione raster corrente.</span><span class="sxs-lookup"><span data-stu-id="6312a-110">Specifies the x-coordinate for the current raster position.</span></span>

</dd> <dt>

<span data-ttu-id="6312a-111">*y*</span><span class="sxs-lookup"><span data-stu-id="6312a-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="6312a-112">Specifica la coordinata y della posizione raster corrente.</span><span class="sxs-lookup"><span data-stu-id="6312a-112">Specifies the y-coordinate for the current raster position.</span></span>

</dd> <dt>

<span data-ttu-id="6312a-113">*z*</span><span class="sxs-lookup"><span data-stu-id="6312a-113">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="6312a-114">Specifica la coordinata z per la posizione raster corrente.</span><span class="sxs-lookup"><span data-stu-id="6312a-114">Specifies the z-coordinate for the current raster position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6312a-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6312a-115">Return value</span></span>

<span data-ttu-id="6312a-116">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="6312a-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6312a-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="6312a-117">Remarks</span></span>

<span data-ttu-id="6312a-118">OpenGL mantiene una posizione 3D nelle coordinate della finestra.</span><span class="sxs-lookup"><span data-stu-id="6312a-118">OpenGL maintains a 3-D position in window coordinates.</span></span> <span data-ttu-id="6312a-119">Questa posizione, denominata posizione raster, viene mantenuta con l'accuratezza dei subpixel.</span><span class="sxs-lookup"><span data-stu-id="6312a-119">This position, called the raster position, is maintained with subpixel accuracy.</span></span> <span data-ttu-id="6312a-120">Viene usato per posizionare le operazioni di scrittura di pixel e bitmap.</span><span class="sxs-lookup"><span data-stu-id="6312a-120">It is used to position pixel and bitmap write operations.</span></span> <span data-ttu-id="6312a-121">Vedere [**glBitmap**](glbitmap.md), [**glDrawPixels**](gldrawpixels.md)e [**glCopyPixels**](glcopypixels.md).</span><span class="sxs-lookup"><span data-stu-id="6312a-121">See [**glBitmap**](glbitmap.md), [**glDrawPixels**](gldrawpixels.md), and [**glCopyPixels**](glcopypixels.md).</span></span>

<span data-ttu-id="6312a-122">La posizione raster corrente è costituita da tre coordinate della finestra (*x, y, z*), un valore di coordinata di ritaglio *w* , una distanza delle coordinate oculari, un bit valido e coordinate di trama e dati di colore associati.</span><span class="sxs-lookup"><span data-stu-id="6312a-122">The current raster position consists of three window coordinates (*x, y, z*), a clip coordinate *w* value, an eye coordinate distance, a valid bit, and associated color data and texture coordinates.</span></span> <span data-ttu-id="6312a-123">La coordinata *w* è una coordinata di ritaglio, perché *w* non è proiettata sulle coordinate della finestra.</span><span class="sxs-lookup"><span data-stu-id="6312a-123">The *w* coordinate is a clip coordinate, because *w* is not projected to window coordinates.</span></span> <span data-ttu-id="6312a-124">La funzione [glRasterPos4](glrasterpos-functions.md) specifica in modo esplicito le coordinate dell'oggetto *x, y, z* e *w* .</span><span class="sxs-lookup"><span data-stu-id="6312a-124">The [glRasterPos4](glrasterpos-functions.md) function specifies object coordinates *x, y, z*, and *w* explicitly.</span></span> <span data-ttu-id="6312a-125">La funzione glRasterPos3 specifica in modo esplicito le coordinate dell'oggetto *x, y* e *z* , mentre *w* viene impostato in modo implicito su uno.</span><span class="sxs-lookup"><span data-stu-id="6312a-125">The glRasterPos3 function specifies object coordinates *x, y,* and *z* explicitly, while *w* is implicitly set to one.</span></span> <span data-ttu-id="6312a-126">La funzione glRasterPos2 usa i valori degli argomenti per *x* e *y* , impostando in modo implicito *z* e *w* su zero e uno.</span><span class="sxs-lookup"><span data-stu-id="6312a-126">The glRasterPos2 function uses the argument values for *x* and *y* while implicitly setting *z* and *w* to zero and one.</span></span>

<span data-ttu-id="6312a-127">Le coordinate degli oggetti presentate da [glRasterPos](glrasterpos-functions.md) vengono gestite esattamente come quelle di un comando [glVertex](glvertex-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="6312a-127">The object coordinates presented by [glRasterPos](glrasterpos-functions.md) are treated just like those of a [glVertex](glvertex-functions.md) command.</span></span> <span data-ttu-id="6312a-128">Vengono trasformati dalle matrici Modelview e Projection correnti e passate alla fase di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="6312a-128">They are transformed by the current modelview and projection matrices and passed to the clipping stage.</span></span> <span data-ttu-id="6312a-129">Se il vertice non viene raccolto, viene proiettato e ridimensionato in base alle coordinate della finestra, che diventano la nuova posizione raster corrente e \_ \_ \_ viene impostato il flag valido della posizione raster corrente \_ .</span><span class="sxs-lookup"><span data-stu-id="6312a-129">If the vertex is not culled, then it is projected and scaled to window coordinates, which become the new current raster position, and the GL\_CURRENT\_RASTER\_POSITION\_VALID flag is set.</span></span> <span data-ttu-id="6312a-130">Se il vertice viene eliminato, viene cancellato il bit valido e la posizione raster corrente e le coordinate del colore e della trama associate non sono definite.</span><span class="sxs-lookup"><span data-stu-id="6312a-130">If the vertex is culled, then the valid bit is cleared and the current raster position and associated color and texture coordinates are undefined.</span></span>

<span data-ttu-id="6312a-131">La posizione raster corrente include anche alcuni dati di colore e coordinate di trama associati.</span><span class="sxs-lookup"><span data-stu-id="6312a-131">The current raster position also includes some associated color data and texture coordinates.</span></span> <span data-ttu-id="6312a-132">Se l'illuminazione è abilitata, il \_ colore raster corrente di GL, \_ \_ in modalità RGBA o \_ l' \_ Indice raster corrente GL \_ , in modalità di indice dei colori, viene impostato sul colore prodotto dal calcolo dell'illuminazione (vedere [glLight](gllight-functions.md), [glLightModel](gllightmodel-functions.md)e [**glShadeModel**](glshademodel.md)).</span><span class="sxs-lookup"><span data-stu-id="6312a-132">If lighting is enabled, then GL\_CURRENT\_RASTER\_COLOR, in RGBA mode, or the GL\_CURRENT\_RASTER\_INDEX, in color-index mode, is set to the color produced by the lighting calculation (see [glLight](gllight-functions.md), [glLightModel](gllightmodel-functions.md), and [**glShadeModel**](glshademodel.md)).</span></span> <span data-ttu-id="6312a-133">Se l'illuminazione è disabilitata, per aggiornare il colore raster corrente viene usato il colore corrente (in modalità RGBA, la variabile di stato GL \_ Current \_ Color) o l'indice dei colori (in modalità di indice colore, variabile di stato GL \_ Current \_ index).</span><span class="sxs-lookup"><span data-stu-id="6312a-133">If lighting is disabled, current color (in RGBA mode, state variable GL\_CURRENT\_COLOR) or color index (in color-index mode, state variable GL\_CURRENT\_INDEX) is used to update the current raster color.</span></span>

<span data-ttu-id="6312a-134">Analogamente, \_ le \_ \_ coordinate di trama raster correnti GL \_ vengono aggiornate come funzione di \_ coordinate di trama correnti GL \_ \_ , in base alla matrice di trama e alle funzioni di generazione della trama (vedere [glTexGen](gltexgen-functions.md)).</span><span class="sxs-lookup"><span data-stu-id="6312a-134">Likewise, GL\_CURRENT\_RASTER\_TEXTURE\_COORDS is updated as a function of GL\_CURRENT\_TEXTURE\_COORDS, based on the texture matrix and the texture generation functions (see [glTexGen](gltexgen-functions.md)).</span></span> <span data-ttu-id="6312a-135">Infine, la distanza dall'origine del sistema di coordinate oculari al vertice, come trasformato solo dalla matrice Modelview, sostituisce la \_ distanza raster corrente di GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="6312a-135">Finally, the distance from the origin of the eye coordinate system to the vertex, as transformed by only the modelview matrix, replaces GL\_CURRENT\_RASTER\_DISTANCE.</span></span>

<span data-ttu-id="6312a-136">Inizialmente, la posizione raster corrente è (0, 0, 0, 1), la distanza raster corrente è 0, è impostato il bit valido, il colore RGBA associato è (1, 1, 1, 1), l'indice colori associato è 1 e le coordinate di trama associate sono (0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="6312a-136">Initially, the current raster position is (0,0,0,1), the current raster distance is 0, the valid bit is set, the associated RGBA color is (1,1,1,1), the associated color index is 1, and the associated texture coordinates are (0, 0, 0, 1).</span></span> <span data-ttu-id="6312a-137">In modalità RGBA, GL \_ Current \_ raster \_ index è sempre 1; in modalità di indice dei colori, il colore RGBA raster corrente mantiene sempre il proprio valore iniziale.</span><span class="sxs-lookup"><span data-stu-id="6312a-137">In RGBA mode, GL\_CURRENT\_RASTER\_INDEX is always 1; in color-index mode, the current raster RGBA color always maintains its initial value.</span></span>

> [!Note]  
> <span data-ttu-id="6312a-138">La posizione raster viene modificata da [glRasterPos](glrasterpos-functions.md) e da [**glBitmap**](glbitmap.md).</span><span class="sxs-lookup"><span data-stu-id="6312a-138">The raster position is modified both by [glRasterPos](glrasterpos-functions.md) and by [**glBitmap**](glbitmap.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="6312a-139">Quando le coordinate della posizione raster non sono valide, i comandi di disegno basati sulla posizione raster vengono ignorati, ovvero non comportano modifiche allo stato di OpenGL.</span><span class="sxs-lookup"><span data-stu-id="6312a-139">When the raster position coordinates are invalid, drawing commands that are based on the raster position are ignored (that is, they do not result in changes to the OpenGL state).</span></span>

 

<span data-ttu-id="6312a-140">Le funzioni seguenti consentono di recuperare informazioni correlate a [glRasterPos](glrasterpos-functions.md):</span><span class="sxs-lookup"><span data-stu-id="6312a-140">The following functions retrieve information related to [glRasterPos](glrasterpos-functions.md):</span></span>

<dl>

<span data-ttu-id="6312a-141">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Current \_ raster \_ position</span><span class="sxs-lookup"><span data-stu-id="6312a-141">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION</span></span>  
<span data-ttu-id="6312a-142">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Current \_ raster \_ position \_ valido</span><span class="sxs-lookup"><span data-stu-id="6312a-142">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION\_VALID</span></span>  
<span data-ttu-id="6312a-143">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Current \_ raster \_ distance</span><span class="sxs-lookup"><span data-stu-id="6312a-143">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_DISTANCE</span></span>  
<span data-ttu-id="6312a-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Current \_ \_ color raster</span><span class="sxs-lookup"><span data-stu-id="6312a-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_COLOR</span></span>  
<span data-ttu-id="6312a-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Current \_ \_ index raster</span><span class="sxs-lookup"><span data-stu-id="6312a-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_INDEX</span></span>  
<span data-ttu-id="6312a-146">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento con \_ \_ coordinate di \_ trama \_ raster correnti</span><span class="sxs-lookup"><span data-stu-id="6312a-146">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_TEXTURE\_COORDS</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="6312a-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6312a-147">Requirements</span></span>



| <span data-ttu-id="6312a-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="6312a-148">Requirement</span></span> | <span data-ttu-id="6312a-149">Valore</span><span class="sxs-lookup"><span data-stu-id="6312a-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6312a-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6312a-150">Minimum supported client</span></span><br/> | <span data-ttu-id="6312a-151">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6312a-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6312a-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6312a-152">Minimum supported server</span></span><br/> | <span data-ttu-id="6312a-153">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6312a-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6312a-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6312a-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="6312a-155"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6312a-155"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6312a-156">Libreria</span><span class="sxs-lookup"><span data-stu-id="6312a-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="6312a-157"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6312a-157"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6312a-158">DLL</span><span class="sxs-lookup"><span data-stu-id="6312a-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6312a-159"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6312a-159"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6312a-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6312a-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6312a-161">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="6312a-161">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="6312a-162">**glBitmap**</span><span class="sxs-lookup"><span data-stu-id="6312a-162">**glBitmap**</span></span>](glbitmap.md)
</dt> <dt>

[<span data-ttu-id="6312a-163">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="6312a-163">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="6312a-164">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="6312a-164">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="6312a-165">**Remo**</span><span class="sxs-lookup"><span data-stu-id="6312a-165">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="6312a-166">glLight</span><span class="sxs-lookup"><span data-stu-id="6312a-166">glLight</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="6312a-167">glLightModel</span><span class="sxs-lookup"><span data-stu-id="6312a-167">glLightModel</span></span>](gllightmodel-functions.md)
</dt> <dt>

[<span data-ttu-id="6312a-168">**glShadeModel**</span><span class="sxs-lookup"><span data-stu-id="6312a-168">**glShadeModel**</span></span>](glshademodel.md)
</dt> <dt>

[<span data-ttu-id="6312a-169">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="6312a-169">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="6312a-170">glTexGen</span><span class="sxs-lookup"><span data-stu-id="6312a-170">glTexGen</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="6312a-171">glVertex</span><span class="sxs-lookup"><span data-stu-id="6312a-171">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





