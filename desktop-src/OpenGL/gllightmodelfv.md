---
title: funzione glLightModelfv (GL. h)
description: La funzione glLightModelfv imposta i parametri del modello di illuminazione.
ms.assetid: a62bcf3b-1769-48a3-8121-8f2b41266183
keywords:
- funzione glLightModelfv OpenGL
topic_type:
- apiref
api_name:
- glLightModelfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7c20aea0851c542fd0d2c81de26da21a692fdb5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517379"
---
# <a name="gllightmodelfv-function"></a><span data-ttu-id="b5389-104">glLightModelfv (funzione)</span><span class="sxs-lookup"><span data-stu-id="b5389-104">glLightModelfv function</span></span>

<span data-ttu-id="b5389-105">La funzione [**glLightModelfv**](gllightfv.md) imposta i parametri del modello di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="b5389-105">The [**glLightModelfv**](gllightfv.md) function sets lighting model parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5389-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5389-106">Syntax</span></span>


```C++
void WINAPI glLightModelfv(
         GLenum  pname,
   const GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="b5389-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5389-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5389-108">*pname*</span><span class="sxs-lookup"><span data-stu-id="b5389-108">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="b5389-109">Parametro del modello di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="b5389-109">A lighting model parameter.</span></span> <span data-ttu-id="b5389-110">Vengono accettati i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="b5389-110">The following values are accepted.</span></span>



| <span data-ttu-id="b5389-111">Valore</span><span class="sxs-lookup"><span data-stu-id="b5389-111">Value</span></span>                                                                                                                                                                                                      | <span data-ttu-id="b5389-112">Significato</span><span class="sxs-lookup"><span data-stu-id="b5389-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span><dl> <span data-ttu-id="b5389-113"><dt>**\_ \_ ambiente modello di luce GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b5389-113"><dt>**GL\_LIGHT\_MODEL\_AMBIENT**</dt></span></span> </dl>                 | <span data-ttu-id="b5389-114">Il parametro *params* contiene quattro valori a virgola mobile che specificano l'intensità RGBA di ambiente dell'intera scena.</span><span class="sxs-lookup"><span data-stu-id="b5389-114">The *params* parameter contains four floating-point values that specify the ambient RGBA intensity of the entire scene.</span></span> <span data-ttu-id="b5389-115">Ai valori integer viene eseguito il mapping lineare, in modo che il valore rappresentabile più positivo sia mappato a 1,0 e il valore rappresentativo più negativo sia mappato a-1,0.</span><span class="sxs-lookup"><span data-stu-id="b5389-115">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="b5389-116">Ai valori a virgola mobile viene eseguito il mapping diretto.</span><span class="sxs-lookup"><span data-stu-id="b5389-116">Floating-point values are mapped directly.</span></span> <span data-ttu-id="b5389-117">Non vengono bloccati né i valori integer né i valori a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="b5389-117">Neither integer nor floating-point values are clamped.</span></span> <span data-ttu-id="b5389-118">L'intensità della scena di ambiente predefinita è (0,2, 0,2, 0,2, 1,0).</span><span class="sxs-lookup"><span data-stu-id="b5389-118">The default ambient scene intensity is (0.2, 0.2, 0.2, 1.0).</span></span> <br/>                                                                                                                                                                                                                                                                                                     |
| <span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span><dl> <span data-ttu-id="b5389-119"><dt>**\_ \_ \_ Visualizzatore locale del modello GL Light \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b5389-119"><dt>**GL\_LIGHT\_MODEL\_LOCAL\_VIEWER**</dt></span></span> </dl> | <span data-ttu-id="b5389-120">Il parametro *params* è un singolo valore a virgola mobile che specifica il modo in cui vengono calcolati gli angoli di Reflection speculare.</span><span class="sxs-lookup"><span data-stu-id="b5389-120">The *params* parameter is a single floating-point value that specifies how specular reflection angles are computed.</span></span> <span data-ttu-id="b5389-121">Se *param* è 0 (o 0,0), gli angoli di Reflection speculari prendono la direzione di visualizzazione parallela a e nella direzione dell'asse-*z* , indipendentemente dalla posizione del vertice nelle coordinate oculari.</span><span class="sxs-lookup"><span data-stu-id="b5389-121">If *param* is 0 (or 0.0), specular reflection angles take the view direction to be parallel to and in the direction of the -*z* axis, regardless of the location of the vertex in eye coordinates.</span></span> <span data-ttu-id="b5389-122">In caso contrario, le riflessioni speculari vengono calcolate dall'origine del sistema di coordinate oculari.</span><span class="sxs-lookup"><span data-stu-id="b5389-122">Otherwise, specular reflections are computed from the origin of the eye coordinate system.</span></span> <span data-ttu-id="b5389-123">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="b5389-123">The default is 0.</span></span> <br/>                                                                                                                                                                                                                                                                                                                |
| <span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span><dl> <span data-ttu-id="b5389-124"><dt>**\_modello GL Light \_ Two- \_ \_ Side**</dt></span><span class="sxs-lookup"><span data-stu-id="b5389-124"><dt>**GL\_LIGHT\_MODEL\_TWO\_SIDE**</dt></span></span> </dl>             | <span data-ttu-id="b5389-125">Il parametro *params* è un singolo valore a virgola mobile che specifica se vengono eseguiti calcoli di illuminazione unilaterali o bilaterali per i poligoni.</span><span class="sxs-lookup"><span data-stu-id="b5389-125">The *params* parameter is a single floating-point value that specifies whether one-sided or two-sided lighting calculations are done for polygons.</span></span> <span data-ttu-id="b5389-126">Non ha alcun effetto sui calcoli di illuminazione per punti, linee o bitmap.</span><span class="sxs-lookup"><span data-stu-id="b5389-126">It has no effect on the lighting calculations for points, lines, or bitmaps.</span></span> <span data-ttu-id="b5389-127">Se *param* è 0 (o 0,0), viene specificata un'illuminazione unilaterale e vengono usati solo i parametri del materiale anteriore nell'equazione di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="b5389-127">If *param* is 0 (or 0.0), one-sided lighting is specified, and only the front material parameters are used in the lighting equation.</span></span> <span data-ttu-id="b5389-128">In caso contrario, viene specificata l'illuminazione a due lati.</span><span class="sxs-lookup"><span data-stu-id="b5389-128">Otherwise, two-sided lighting is specified.</span></span> <br/> <span data-ttu-id="b5389-129">In questo caso, i vertici dei poligoni sottoposti a riattivazione vengono illuminati usando i parametri del materiale di back-end e le normali annullate prima della valutazione dell'equazione di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="b5389-129">In this case, vertices of back-facing polygons are lighted using the back material parameters, and have their normals reversed before the lighting equation is evaluated.</span></span> <span data-ttu-id="b5389-130">I vertici dei poligoni in primo piano sono sempre illuminati usando i parametri del materiale anteriore, senza apportare modifiche alle normali.</span><span class="sxs-lookup"><span data-stu-id="b5389-130">Vertices of front-facing polygons are always lighted using the front material parameters, with no change to their normals.</span></span> <span data-ttu-id="b5389-131">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="b5389-131">The default is 0.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b5389-132">*params*</span><span class="sxs-lookup"><span data-stu-id="b5389-132">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="b5389-133">Puntatore al valore o ai valori a cui verranno impostati i *parametri* .</span><span class="sxs-lookup"><span data-stu-id="b5389-133">A pointer to the value or values to which *params* will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5389-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5389-134">Return value</span></span>

<span data-ttu-id="b5389-135">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="b5389-135">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b5389-136">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="b5389-136">Error codes</span></span>

<span data-ttu-id="b5389-137">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="b5389-137">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b5389-138">Nome</span><span class="sxs-lookup"><span data-stu-id="b5389-138">Name</span></span>                                                                                                  | <span data-ttu-id="b5389-139">Significato</span><span class="sxs-lookup"><span data-stu-id="b5389-139">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b5389-140"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b5389-140"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="b5389-141">*pname* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="b5389-141">*pname* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="b5389-142"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b5389-142"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b5389-143">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="b5389-143">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b5389-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="b5389-144">Remarks</span></span>

<span data-ttu-id="b5389-145">La funzione **glLightModelfv** imposta il parametro del modello di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="b5389-145">The **glLightModelfv** function sets lighting model parameter.</span></span> <span data-ttu-id="b5389-146">Il parametro *pname* denomina un parametro e *param* fornisce il nuovo valore. il valore o i valori dei singoli parametri della sorgente di luce.</span><span class="sxs-lookup"><span data-stu-id="b5389-146">The *pname* parameter names a parameter and *param* gives the new value.the value or values of individual light source parameters.</span></span>

<span data-ttu-id="b5389-147">In modalità RGBA, il colore chiaro di un vertice è costituito dalla somma dell'intensità di emissione del materiale, dal prodotto della riflettenza dell'ambiente del materiale e dall'intensità dell'ambiente a scena completa del modello di illuminazione e dal contributo di ogni sorgente di luce abilitata.</span><span class="sxs-lookup"><span data-stu-id="b5389-147">In RGBA mode, the lighted color of a vertex is the sum of the material emission intensity, the product of the material ambient reflectance and the lighting model full-scene ambient intensity, and the contribution of each enabled light source.</span></span> <span data-ttu-id="b5389-148">Ogni sorgente di luce contribuisce alla somma di tre termini: ambiente, diffuso e speculare.</span><span class="sxs-lookup"><span data-stu-id="b5389-148">Each light source contributes the sum of three terms: ambient, diffuse, and specular.</span></span>

-   <span data-ttu-id="b5389-149">Il contributo di origine luce di ambiente è il prodotto della riflettenza dell'ambiente del materiale e l'intensità di ambiente della luce.</span><span class="sxs-lookup"><span data-stu-id="b5389-149">The ambient light source contribution is the product of the material ambient reflectance and the light's ambient intensity.</span></span>
-   <span data-ttu-id="b5389-150">Il contributo Diffusion Light Source è il prodotto della riflettenza diffusa del materiale, l'intensità diffusa della luce e il prodotto punto della normale del vertice con il vettore normalizzato dal vertice alla sorgente di luce.</span><span class="sxs-lookup"><span data-stu-id="b5389-150">The diffuse light source contribution is the product of the material diffuse reflectance, the light's diffuse intensity, and the dot product of the vertex's normal with the normalized vector from the vertex to the light source.</span></span>
-   <span data-ttu-id="b5389-151">Il contributo della sorgente di luce speculare è il prodotto della riflettenza speculare del materiale, l'intensità speculare della luce e il prodotto a virgola dei vettori normalizzati da vertice a occhio e da vertice a chiaro, elevato alla potenza del lucentezza del materiale.</span><span class="sxs-lookup"><span data-stu-id="b5389-151">The specular light source contribution is the product of the material specular reflectance, the light's specular intensity, and the dot product of the normalized vertex-to-eye and vertex-to-light vectors, raised to the power of the shininess of the material.</span></span>

<span data-ttu-id="b5389-152">Tutti e tre i contributi della sorgente di luce vengono attenuati in modo uniforme in base alla distanza dal vertice alla sorgente di luce e alla direzione della sorgente di luce, all'esponente spread e all'angolo di taglio.</span><span class="sxs-lookup"><span data-stu-id="b5389-152">All three light source contributions are attenuated equally based on the distance from the vertex to the light source and on light source direction, spread exponent, and spread cutoff angle.</span></span> <span data-ttu-id="b5389-153">Tutti i prodotti a virgola vengono sostituiti da zero se restituiscono un valore negativo.</span><span class="sxs-lookup"><span data-stu-id="b5389-153">All dot products are replaced with zero if they evaluate to a negative value.</span></span>

<span data-ttu-id="b5389-154">Il componente alfa del colore chiaro risultante viene impostato sul valore alfa della riflettenza diffusa del materiale.</span><span class="sxs-lookup"><span data-stu-id="b5389-154">The alpha component of the resulting lighted color is set to the alpha value of the material diffuse reflectance.</span></span>

<span data-ttu-id="b5389-155">In modalità di indice dei colori, il valore dell'indice illuminato di un vertice spazia dall'ambiente ai valori speculari passati a [**glMaterial**](glmaterial-functions.md) usando gli \_ indici dei colori GL \_ .</span><span class="sxs-lookup"><span data-stu-id="b5389-155">In color-index mode, the value of the lighted index of a vertex ranges from the ambient to the specular values passed to [**glMaterial**](glmaterial-functions.md) using GL\_COLOR\_INDEXES.</span></span> <span data-ttu-id="b5389-156">Coefficienti, diffusi e speculari, calcolati con un valore (30, 59, .11) ponderazione dei colori della luce, il lucentezza del materiale e le stesse equazioni di reflection e attenuazione come nel caso di RGBA, determinano la quantità di spazio sopra l'indice risultante.</span><span class="sxs-lookup"><span data-stu-id="b5389-156">Diffuse and specular coefficients, computed with a (.30, .59, .11) weighting of the light's colors, the shininess of the material, and the same reflection and attenuation equations as in the RGBA case, determine how much above ambient the resulting index is.</span></span>

<span data-ttu-id="b5389-157">Le funzioni seguenti consentono di recuperare informazioni correlate alla funzione **glLightModelfv** :</span><span class="sxs-lookup"><span data-stu-id="b5389-157">The following functions retrieve information related to the **glLightModelfv** function:</span></span>

<span data-ttu-id="b5389-158">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Light \_ Model \_ \_ Visualizzatore locale</span><span class="sxs-lookup"><span data-stu-id="b5389-158">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LIGHT\_MODEL\_LOCAL\_VIEWER</span></span>

<span data-ttu-id="b5389-159">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Light \_ Model \_ Two \_ Side</span><span class="sxs-lookup"><span data-stu-id="b5389-159">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LIGHT\_MODEL\_TWO\_SIDE</span></span>

<span data-ttu-id="b5389-160">[**glIsEnabled**](glisenabled.md) con illuminazione GL argomento \_</span><span class="sxs-lookup"><span data-stu-id="b5389-160">[**glIsEnabled**](glisenabled.md) with argument GL\_LIGHTING</span></span>

## <a name="requirements"></a><span data-ttu-id="b5389-161">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5389-161">Requirements</span></span>



| <span data-ttu-id="b5389-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5389-162">Requirement</span></span> | <span data-ttu-id="b5389-163">Valore</span><span class="sxs-lookup"><span data-stu-id="b5389-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5389-164">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5389-164">Minimum supported client</span></span><br/> | <span data-ttu-id="b5389-165">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b5389-165">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b5389-166">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5389-166">Minimum supported server</span></span><br/> | <span data-ttu-id="b5389-167">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b5389-167">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b5389-168">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b5389-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5389-169"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5389-169"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b5389-170">Libreria</span><span class="sxs-lookup"><span data-stu-id="b5389-170">Library</span></span><br/>                  | <dl> <span data-ttu-id="b5389-171"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5389-171"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b5389-172">DLL</span><span class="sxs-lookup"><span data-stu-id="b5389-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5389-173"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5389-173"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5389-174">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5389-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5389-175">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b5389-175">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b5389-176">**Remo**</span><span class="sxs-lookup"><span data-stu-id="b5389-176">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b5389-177">**glLight**</span><span class="sxs-lookup"><span data-stu-id="b5389-177">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="b5389-178">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="b5389-178">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> </dl>

 

 





