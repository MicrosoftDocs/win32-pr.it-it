---
title: funzione glLightModeliv (GL. h)
description: La funzione glLightModeliv imposta i parametri del modello di illuminazione.
ms.assetid: 5998bb7e-d97a-47a0-b612-e6b0046aa5d2
keywords:
- funzione glLightModeliv OpenGL
topic_type:
- apiref
api_name:
- glLightModeliv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de61d53d3f4ceb9805ca5560c864379b18c65b3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743114"
---
# <a name="gllightmodeliv-function"></a><span data-ttu-id="c6f11-104">glLightModeliv (funzione)</span><span class="sxs-lookup"><span data-stu-id="c6f11-104">glLightModeliv function</span></span>

<span data-ttu-id="c6f11-105">La funzione [**glLightModeliv**](gllightiv.md) imposta i parametri del modello di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="c6f11-105">The [**glLightModeliv**](gllightiv.md) function sets lighting model parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6f11-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c6f11-106">Syntax</span></span>


```C++
void WINAPI glLightModeliv(
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="c6f11-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c6f11-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6f11-108">*pname*</span><span class="sxs-lookup"><span data-stu-id="c6f11-108">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="c6f11-109">Parametro del modello di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="c6f11-109">A lighting model parameter.</span></span> <span data-ttu-id="c6f11-110">Vengono accettati i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="c6f11-110">The following values are accepted.</span></span>



| <span data-ttu-id="c6f11-111">Valore</span><span class="sxs-lookup"><span data-stu-id="c6f11-111">Value</span></span>                                                                                                                                                                                                      | <span data-ttu-id="c6f11-112">Significato</span><span class="sxs-lookup"><span data-stu-id="c6f11-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span><dl> <span data-ttu-id="c6f11-113"><dt>**\_ \_ ambiente modello di luce GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c6f11-113"><dt>**GL\_LIGHT\_MODEL\_AMBIENT**</dt></span></span> </dl>                 | <span data-ttu-id="c6f11-114">Il parametro *params* contiene quattro valori integer che specificano l'intensità RGBA di ambiente dell'intera scena.</span><span class="sxs-lookup"><span data-stu-id="c6f11-114">The *params* parameter contains four integer values that specify the ambient RGBA intensity of the entire scene.</span></span> <span data-ttu-id="c6f11-115">Ai valori integer viene eseguito il mapping lineare, in modo che il valore rappresentabile più positivo sia mappato a 1,0 e il valore rappresentativo più negativo sia mappato a-1,0.</span><span class="sxs-lookup"><span data-stu-id="c6f11-115">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="c6f11-116">Ai valori a virgola mobile viene eseguito il mapping diretto.</span><span class="sxs-lookup"><span data-stu-id="c6f11-116">Floating-point values are mapped directly.</span></span> <span data-ttu-id="c6f11-117">Non vengono bloccati né i valori integer né i valori a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="c6f11-117">Neither integer nor floating-point values are clamped.</span></span> <span data-ttu-id="c6f11-118">L'intensità della scena di ambiente predefinita è (0,2, 0,2, 0,2, 1,0).</span><span class="sxs-lookup"><span data-stu-id="c6f11-118">The default ambient scene intensity is (0.2, 0.2, 0.2, 1.0).</span></span> <br/>                                                                                                                                                                                                                                                                                                     |
| <span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span><dl> <span data-ttu-id="c6f11-119"><dt>**\_ \_ \_ Visualizzatore locale del modello GL Light \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c6f11-119"><dt>**GL\_LIGHT\_MODEL\_LOCAL\_VIEWER**</dt></span></span> </dl> | <span data-ttu-id="c6f11-120">Il parametro *params* è un singolo valore integer che specifica il modo in cui vengono calcolati gli angoli di Reflection speculare.</span><span class="sxs-lookup"><span data-stu-id="c6f11-120">The *params* parameter is a single integer value that specifies how specular reflection angles are computed.</span></span> <span data-ttu-id="c6f11-121">Se *param* è 0 (o 0,0), gli angoli di Reflection speculari prendono la direzione di visualizzazione parallela a e nella direzione dell'asse-*z* , indipendentemente dalla posizione del vertice nelle coordinate oculari.</span><span class="sxs-lookup"><span data-stu-id="c6f11-121">If *param* is 0 (or 0.0), specular reflection angles take the view direction to be parallel to and in the direction of the -*z* axis, regardless of the location of the vertex in eye coordinates.</span></span> <span data-ttu-id="c6f11-122">In caso contrario, le riflessioni speculari vengono calcolate dall'origine del sistema di coordinate oculari.</span><span class="sxs-lookup"><span data-stu-id="c6f11-122">Otherwise, specular reflections are computed from the origin of the eye coordinate system.</span></span> <span data-ttu-id="c6f11-123">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="c6f11-123">The default is 0.</span></span> <br/>                                                                                                                                                                                                                                                                                                                |
| <span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span><dl> <span data-ttu-id="c6f11-124"><dt>**\_modello GL Light \_ Two- \_ \_ Side**</dt></span><span class="sxs-lookup"><span data-stu-id="c6f11-124"><dt>**GL\_LIGHT\_MODEL\_TWO\_SIDE**</dt></span></span> </dl>             | <span data-ttu-id="c6f11-125">Il parametro *params* è un singolo valore integer che specifica se vengono eseguiti calcoli di illuminazione unilaterali o bilaterali per i poligoni.</span><span class="sxs-lookup"><span data-stu-id="c6f11-125">The *params* parameter is a single integer value that specifies whether one-sided or two-sided lighting calculations are done for polygons.</span></span> <span data-ttu-id="c6f11-126">Non ha alcun effetto sui calcoli di illuminazione per punti, linee o bitmap.</span><span class="sxs-lookup"><span data-stu-id="c6f11-126">It has no effect on the lighting calculations for points, lines, or bitmaps.</span></span> <span data-ttu-id="c6f11-127">Se *param* è 0 (o 0,0), viene specificata un'illuminazione unilaterale e vengono usati solo i parametri del materiale anteriore nell'equazione di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="c6f11-127">If *param* is 0 (or 0.0), one-sided lighting is specified, and only the front material parameters are used in the lighting equation.</span></span> <span data-ttu-id="c6f11-128">In caso contrario, viene specificata l'illuminazione a due lati.</span><span class="sxs-lookup"><span data-stu-id="c6f11-128">Otherwise, two-sided lighting is specified.</span></span> <br/> <span data-ttu-id="c6f11-129">In questo caso, i vertici dei poligoni sottoposti a riattivazione vengono illuminati usando i parametri del materiale di back-end e le normali annullate prima della valutazione dell'equazione di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="c6f11-129">In this case, vertices of back-facing polygons are lighted using the back material parameters, and have their normals reversed before the lighting equation is evaluated.</span></span> <span data-ttu-id="c6f11-130">I vertici dei poligoni in primo piano sono sempre illuminati usando i parametri del materiale anteriore, senza apportare modifiche alle normali.</span><span class="sxs-lookup"><span data-stu-id="c6f11-130">Vertices of front-facing polygons are always lighted using the front material parameters, with no change to their normals.</span></span> <span data-ttu-id="c6f11-131">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="c6f11-131">The default is 0.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c6f11-132">*params*</span><span class="sxs-lookup"><span data-stu-id="c6f11-132">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="c6f11-133">Puntatore al valore o ai valori a cui verranno impostati i *parametri* .</span><span class="sxs-lookup"><span data-stu-id="c6f11-133">A pointer to the value or values to which *params* will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6f11-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c6f11-134">Return value</span></span>

<span data-ttu-id="c6f11-135">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="c6f11-135">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c6f11-136">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="c6f11-136">Error codes</span></span>

<span data-ttu-id="c6f11-137">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="c6f11-137">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="c6f11-138">Nome</span><span class="sxs-lookup"><span data-stu-id="c6f11-138">Name</span></span>                                                                                                  | <span data-ttu-id="c6f11-139">Significato</span><span class="sxs-lookup"><span data-stu-id="c6f11-139">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c6f11-140"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c6f11-140"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="c6f11-141">*pname* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="c6f11-141">*pname* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="c6f11-142"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c6f11-142"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="c6f11-143">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="c6f11-143">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c6f11-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="c6f11-144">Remarks</span></span>

<span data-ttu-id="c6f11-145">La funzione **glLightModeliv** imposta il parametro del modello di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="c6f11-145">The **glLightModeliv** function sets lighting model parameter.</span></span> <span data-ttu-id="c6f11-146">Il parametro *pname* denomina un parametro e *param* fornisce il nuovo valore. il valore o i valori dei singoli parametri della sorgente di luce.</span><span class="sxs-lookup"><span data-stu-id="c6f11-146">The *pname* parameter names a parameter and *param* gives the new value.the value or values of individual light source parameters.</span></span>

<span data-ttu-id="c6f11-147">In modalità RGBA, il colore chiaro di un vertice è costituito dalla somma dell'intensità di emissione del materiale, dal prodotto della riflettenza dell'ambiente del materiale e dall'intensità dell'ambiente a scena completa del modello di illuminazione e dal contributo di ogni sorgente di luce abilitata.</span><span class="sxs-lookup"><span data-stu-id="c6f11-147">In RGBA mode, the lighted color of a vertex is the sum of the material emission intensity, the product of the material ambient reflectance and the lighting model full-scene ambient intensity, and the contribution of each enabled light source.</span></span> <span data-ttu-id="c6f11-148">Ogni sorgente di luce contribuisce alla somma di tre termini: ambiente, diffuso e speculare.</span><span class="sxs-lookup"><span data-stu-id="c6f11-148">Each light source contributes the sum of three terms: ambient, diffuse, and specular.</span></span>

-   <span data-ttu-id="c6f11-149">Il contributo di origine luce di ambiente è il prodotto della riflettenza dell'ambiente del materiale e l'intensità di ambiente della luce.</span><span class="sxs-lookup"><span data-stu-id="c6f11-149">The ambient light source contribution is the product of the material ambient reflectance and the light's ambient intensity.</span></span>
-   <span data-ttu-id="c6f11-150">Il contributo Diffusion Light Source è il prodotto della riflettenza diffusa del materiale, l'intensità diffusa della luce e il prodotto punto della normale del vertice con il vettore normalizzato dal vertice alla sorgente di luce.</span><span class="sxs-lookup"><span data-stu-id="c6f11-150">The diffuse light source contribution is the product of the material diffuse reflectance, the light's diffuse intensity, and the dot product of the vertex's normal with the normalized vector from the vertex to the light source.</span></span>
-   <span data-ttu-id="c6f11-151">Il contributo della sorgente di luce speculare è il prodotto della riflettenza speculare del materiale, l'intensità speculare della luce e il prodotto a virgola dei vettori normalizzati da vertice a occhio e da vertice a chiaro, elevato alla potenza del lucentezza del materiale.</span><span class="sxs-lookup"><span data-stu-id="c6f11-151">The specular light source contribution is the product of the material specular reflectance, the light's specular intensity, and the dot product of the normalized vertex-to-eye and vertex-to-light vectors, raised to the power of the shininess of the material.</span></span>

<span data-ttu-id="c6f11-152">Tutti e tre i contributi della sorgente di luce vengono attenuati in modo uniforme in base alla distanza dal vertice alla sorgente di luce e alla direzione della sorgente di luce, all'esponente spread e all'angolo di taglio.</span><span class="sxs-lookup"><span data-stu-id="c6f11-152">All three light source contributions are attenuated equally based on the distance from the vertex to the light source and on light source direction, spread exponent, and spread cutoff angle.</span></span> <span data-ttu-id="c6f11-153">Tutti i prodotti a virgola vengono sostituiti da zero se restituiscono un valore negativo.</span><span class="sxs-lookup"><span data-stu-id="c6f11-153">All dot products are replaced with zero if they evaluate to a negative value.</span></span>

<span data-ttu-id="c6f11-154">Il componente alfa del colore chiaro risultante viene impostato sul valore alfa della riflettenza diffusa del materiale.</span><span class="sxs-lookup"><span data-stu-id="c6f11-154">The alpha component of the resulting lighted color is set to the alpha value of the material diffuse reflectance.</span></span>

<span data-ttu-id="c6f11-155">In modalità di indice dei colori, il valore dell'indice illuminato di un vertice spazia dall'ambiente ai valori speculari passati a [**glMaterial**](glmaterial-functions.md) usando gli \_ indici dei colori GL \_ .</span><span class="sxs-lookup"><span data-stu-id="c6f11-155">In color-index mode, the value of the lighted index of a vertex ranges from the ambient to the specular values passed to [**glMaterial**](glmaterial-functions.md) using GL\_COLOR\_INDEXES.</span></span> <span data-ttu-id="c6f11-156">Coefficienti, diffusi e speculari, calcolati con un valore (30, 59, .11) ponderazione dei colori della luce, il lucentezza del materiale e le stesse equazioni di reflection e attenuazione come nel caso di RGBA, determinano la quantità di spazio sopra l'indice risultante.</span><span class="sxs-lookup"><span data-stu-id="c6f11-156">Diffuse and specular coefficients, computed with a (.30, .59, .11) weighting of the light's colors, the shininess of the material, and the same reflection and attenuation equations as in the RGBA case, determine how much above ambient the resulting index is.</span></span>

<span data-ttu-id="c6f11-157">Le funzioni seguenti consentono di recuperare informazioni correlate alla funzione **glLightModeliv** :</span><span class="sxs-lookup"><span data-stu-id="c6f11-157">The following functions retrieve information related to the **glLightModeliv** function:</span></span>

<span data-ttu-id="c6f11-158">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Light \_ Model \_ \_ Visualizzatore locale</span><span class="sxs-lookup"><span data-stu-id="c6f11-158">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LIGHT\_MODEL\_LOCAL\_VIEWER</span></span>

<span data-ttu-id="c6f11-159">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Light \_ Model \_ Two \_ Side</span><span class="sxs-lookup"><span data-stu-id="c6f11-159">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LIGHT\_MODEL\_TWO\_SIDE</span></span>

<span data-ttu-id="c6f11-160">[**glIsEnabled**](glisenabled.md) con illuminazione GL argomento \_</span><span class="sxs-lookup"><span data-stu-id="c6f11-160">[**glIsEnabled**](glisenabled.md) with argument GL\_LIGHTING</span></span>

## <a name="requirements"></a><span data-ttu-id="c6f11-161">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6f11-161">Requirements</span></span>



| <span data-ttu-id="c6f11-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6f11-162">Requirement</span></span> | <span data-ttu-id="c6f11-163">Valore</span><span class="sxs-lookup"><span data-stu-id="c6f11-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6f11-164">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6f11-164">Minimum supported client</span></span><br/> | <span data-ttu-id="c6f11-165">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c6f11-165">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c6f11-166">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6f11-166">Minimum supported server</span></span><br/> | <span data-ttu-id="c6f11-167">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c6f11-167">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c6f11-168">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c6f11-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6f11-169"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6f11-169"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c6f11-170">Libreria</span><span class="sxs-lookup"><span data-stu-id="c6f11-170">Library</span></span><br/>                  | <dl> <span data-ttu-id="c6f11-171"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c6f11-171"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c6f11-172">DLL</span><span class="sxs-lookup"><span data-stu-id="c6f11-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6f11-173"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6f11-173"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6f11-174">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6f11-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6f11-175">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="c6f11-175">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="c6f11-176">**Remo**</span><span class="sxs-lookup"><span data-stu-id="c6f11-176">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="c6f11-177">**glLight**</span><span class="sxs-lookup"><span data-stu-id="c6f11-177">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="c6f11-178">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="c6f11-178">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> </dl>

 

 





