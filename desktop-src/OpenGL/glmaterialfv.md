---
title: funzione glMaterialfv (GL. h)
description: La funzione glMaterialfv specifica i parametri del materiale per il modello di illuminazione.
ms.assetid: cd357686-4d6f-49fd-a111-308b5485ac21
keywords:
- funzione glMaterialfv OpenGL
topic_type:
- apiref
api_name:
- glMaterialfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b44b200abe0588a657f770902a9a897329e1942a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400216"
---
# <a name="glmaterialfv-function"></a><span data-ttu-id="7f3e7-104">glMaterialfv (funzione)</span><span class="sxs-lookup"><span data-stu-id="7f3e7-104">glMaterialfv function</span></span>

<span data-ttu-id="7f3e7-105">La funzione **glMaterialfv** specifica i parametri del materiale per il modello di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-105">The **glMaterialfv** function specifies material parameters for the lighting model.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f3e7-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7f3e7-106">Syntax</span></span>


```C++
void WINAPI glMaterialfv(
         GLenum  face,
         GLenum  pname,
   const GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="7f3e7-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="7f3e7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f3e7-108">*faccia*</span><span class="sxs-lookup"><span data-stu-id="7f3e7-108">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="7f3e7-109">Il volto o i visi da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-109">The face or faces that are being updated.</span></span> <span data-ttu-id="7f3e7-110">Deve essere uno dei seguenti: GL \_ Front, GL \_ back o GL \_ front e GL \_ back.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-110">Must be one of the following: GL\_FRONT, GL\_BACK, or GL\_FRONT and GL\_BACK.</span></span>

</dd> <dt>

<span data-ttu-id="7f3e7-111">*pname*</span><span class="sxs-lookup"><span data-stu-id="7f3e7-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="7f3e7-112">Il parametro Material della faccia o dei visi da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-112">The material parameter of the face or faces being updated.</span></span> <span data-ttu-id="7f3e7-113">I parametri che possono essere specificati tramite **glMaterialfv** e le relative interpretazioni dall'equazione di illuminazione sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-113">The parameters that can be specified using **glMaterialfv**, and their interpretations by the lighting equation, are as follows.</span></span>



| <span data-ttu-id="7f3e7-114">Valore</span><span class="sxs-lookup"><span data-stu-id="7f3e7-114">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="7f3e7-115">Significato</span><span class="sxs-lookup"><span data-stu-id="7f3e7-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <span data-ttu-id="7f3e7-116"><dt>**\_ambiente GL**</dt></span><span class="sxs-lookup"><span data-stu-id="7f3e7-116"><dt>**GL\_AMBIENT**</dt></span></span> </dl>                                       | <span data-ttu-id="7f3e7-117">Il parametro params contiene quattro valori a virgola mobile che specificano la reflection RGBA di ambiente del materiale.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-117">The params parameter contains four floating-point values that specify the ambient RGBA reflectance of the material.</span></span> <span data-ttu-id="7f3e7-118">Ai valori integer viene eseguito il mapping lineare, in modo che il valore rappresentabile più positivo sia mappato a 1,0 e il valore rappresentativo più negativo sia mappato a-1,0.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-118">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="7f3e7-119">Ai valori a virgola mobile viene eseguito il mapping diretto.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-119">Floating-point values are mapped directly.</span></span> <span data-ttu-id="7f3e7-120">Non vengono bloccati né i valori integer né i valori a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-120">Neither integer nor floating-point values are clamped.</span></span> <span data-ttu-id="7f3e7-121">La reflection di ambiente predefinita per i materiali front-end e di back-end è (0,2, 0,2, 0,2, 1,0).</span><span class="sxs-lookup"><span data-stu-id="7f3e7-121">The default ambient reflectance for both front-facing and back-facing materials is (0.2, 0.2, 0.2, 1.0).</span></span> <br/>    |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <span data-ttu-id="7f3e7-122"><dt>**GL \_ diffuse**</dt></span><span class="sxs-lookup"><span data-stu-id="7f3e7-122"><dt>**GL\_DIFFUSE**</dt></span></span> </dl>                                       | <span data-ttu-id="7f3e7-123">Il parametro params contiene quattro valori a virgola mobile che specificano la reflection RGBA diffusa del materiale.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-123">The params parameter contains four floating-point values that specify the diffuse RGBA reflectance of the material.</span></span> <span data-ttu-id="7f3e7-124">Ai valori integer viene eseguito il mapping lineare, in modo che il valore rappresentabile più positivo sia mappato a 1,0 e il valore rappresentativo più negativo sia mappato a-1,0.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-124">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="7f3e7-125">Ai valori a virgola mobile viene eseguito il mapping diretto.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-125">Floating-point values are mapped directly.</span></span> <span data-ttu-id="7f3e7-126">Non vengono bloccati né i valori integer né i valori a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-126">Neither integer nor floating-point values are clamped.</span></span> <span data-ttu-id="7f3e7-127">La reflection predefinita diffusa sia per i materiali front-end che per quelli di back-end è (0,8, 0,8, 0,8, 1,0).</span><span class="sxs-lookup"><span data-stu-id="7f3e7-127">The default diffuse reflectance for both front-facing and back-facing materials is (0.8, 0.8, 0.8, 1.0).</span></span> <br/>    |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <span data-ttu-id="7f3e7-128"><dt>**\_speculare GL**</dt></span><span class="sxs-lookup"><span data-stu-id="7f3e7-128"><dt>**GL\_SPECULAR**</dt></span></span> </dl>                                    | <span data-ttu-id="7f3e7-129">Il parametro params contiene quattro valori a virgola mobile che specificano la reflection RGBA speculare del materiale.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-129">The params parameter contains four floating-point values that specify the specular RGBA reflectance of the material.</span></span> <span data-ttu-id="7f3e7-130">Ai valori integer viene eseguito il mapping lineare, in modo che il valore rappresentabile più positivo sia mappato a 1,0 e il valore rappresentativo più negativo sia mappato a-1,0.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-130">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="7f3e7-131">Ai valori a virgola mobile viene eseguito il mapping diretto.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-131">Floating-point values are mapped directly.</span></span> <span data-ttu-id="7f3e7-132">Non vengono bloccati né i valori integer né i valori a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-132">Neither integer nor floating-point values are clamped.</span></span> <span data-ttu-id="7f3e7-133">La reflection speculare predefinita sia per i materiali front-end che per quelli di back-end è (0,0, 0,0, 0,0, 1,0).</span><span class="sxs-lookup"><span data-stu-id="7f3e7-133">The default specular reflectance for both front-facing and back-facing materials is (0.0, 0.0, 0.0, 1.0).</span></span> <br/>  |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <span data-ttu-id="7f3e7-134"><dt>**\_emissione GL**</dt></span><span class="sxs-lookup"><span data-stu-id="7f3e7-134"><dt>**GL\_EMISSION**</dt></span></span> </dl>                                    | <span data-ttu-id="7f3e7-135">Il parametro params contiene quattro valori a virgola mobile che specificano l'intensità della luce emessa dal RGBA del materiale.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-135">The params parameter contains four floating-point values that specify the RGBA emitted light intensity of the material.</span></span> <span data-ttu-id="7f3e7-136">Ai valori integer viene eseguito il mapping lineare, in modo che il valore rappresentabile più positivo sia mappato a 1,0 e il valore rappresentativo più negativo sia mappato a-1,0.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-136">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="7f3e7-137">Ai valori a virgola mobile viene eseguito il mapping diretto.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-137">Floating-point values are mapped directly.</span></span> <span data-ttu-id="7f3e7-138">Non vengono bloccati né i valori integer né i valori a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-138">Neither integer nor floating-point values are clamped.</span></span> <span data-ttu-id="7f3e7-139">L'intensità di emissione predefinita per i materiali front-end e di back-end è (0,0, 0,0, 0,0, 1,0).</span><span class="sxs-lookup"><span data-stu-id="7f3e7-139">The default emission intensity for both front-facing and back-facing materials is (0.0, 0.0, 0.0, 1.0).</span></span> <br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <span data-ttu-id="7f3e7-140"><dt>**\_lucentezza GL**</dt></span><span class="sxs-lookup"><span data-stu-id="7f3e7-140"><dt>**GL\_SHININESS**</dt></span></span> </dl>                                 | <span data-ttu-id="7f3e7-141">Il parametro *param* è un singolo valore integer che specifica l'esponente speculare RGBA del materiale.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-141">The *param* parameter is a single integer value that specifies the RGBA specular exponent of the material.</span></span> <span data-ttu-id="7f3e7-142">Viene eseguito il mapping diretto dei valori integer.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-142">Integer values are mapped directly.</span></span> <span data-ttu-id="7f3e7-143">Sono accettati solo i valori nell'intervallo compreso tra \[ 0 e 128 \] .</span><span class="sxs-lookup"><span data-stu-id="7f3e7-143">Only values in the range \[0, 128\] are accepted.</span></span> <span data-ttu-id="7f3e7-144">L'esponente speculare predefinito per i materiali front-end e di back-end è 0.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-144">The default specular exponent for both front-facing and back-facing materials is 0.</span></span> <br/>                                                                                                                                                                                                      |
| <span id="GL_AMBIENT_AND_DIFFUSE"></span><span id="gl_ambient_and_diffuse"></span><dl> <span data-ttu-id="7f3e7-145"><dt>**\_ambiente GL \_ e \_ diffusa**</dt></span><span class="sxs-lookup"><span data-stu-id="7f3e7-145"><dt>**GL\_AMBIENT\_AND\_DIFFUSE**</dt></span></span> </dl> | <span data-ttu-id="7f3e7-146">Equivale a chiamare due volte [**glMaterial**](glmaterial-functions.md) con gli stessi valori di parametro, una volta con l' \_ ambiente GL e una volta con GL \_ Diffusion.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-146">Equivalent to calling [**glMaterial**](glmaterial-functions.md) twice with the same parameter values, once with GL\_AMBIENT and once with GL\_DIFFUSE.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                   |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <span data-ttu-id="7f3e7-147"><dt>**indici di \_ colore GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7f3e7-147"><dt>**GL\_COLOR\_INDEXES**</dt></span></span> </dl>                    | <span data-ttu-id="7f3e7-148">Il parametro params contiene tre valori a virgola mobile che specificano gli indici dei colori per l'illuminazione ambientale, diffusa e speculare.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-148">The params parameter contains three floating-point values specifying the color indexes for ambient, diffuse, and specular lighting.</span></span> <span data-ttu-id="7f3e7-149">Questi tre valori, e GL \_ lucentezza, sono gli unici valori di materiale usati dall'equazione di illuminazione della modalità di indice dei colori.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-149">These three values, and GL\_SHININESS, are the only material values used by the color-index mode lighting equation.</span></span> <span data-ttu-id="7f3e7-150">Per informazioni sull'illuminazione degli indici dei colori, vedere [**glLightModel**](gllightmodel-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="7f3e7-150">Refer to [**glLightModel**](gllightmodel-functions.md) for a discussion of color-index lighting.</span></span><br/>                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="7f3e7-151">*params*</span><span class="sxs-lookup"><span data-stu-id="7f3e7-151">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="7f3e7-152">Valore in cui verrà impostato il parametro GL \_ lucentezza.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-152">The value to which parameter GL\_SHININESS will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f3e7-153">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7f3e7-153">Return value</span></span>

<span data-ttu-id="7f3e7-154">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-154">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7f3e7-155">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="7f3e7-155">Error codes</span></span>

<span data-ttu-id="7f3e7-156">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="7f3e7-156">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="7f3e7-157">Nome</span><span class="sxs-lookup"><span data-stu-id="7f3e7-157">Name</span></span>                                                                                              | <span data-ttu-id="7f3e7-158">Significato</span><span class="sxs-lookup"><span data-stu-id="7f3e7-158">Meaning</span></span>                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7f3e7-159"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7f3e7-159"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="7f3e7-160">*Face* o *pname* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-160">Either *face* or *pname* was not an accepted value.</span></span><br/>                |
| <dl> <span data-ttu-id="7f3e7-161"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7f3e7-161"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="7f3e7-162">È stato specificato un esponente speculare non compreso nell'intervallo \[ 0, 128 \] .</span><span class="sxs-lookup"><span data-stu-id="7f3e7-162">A specular exponent outside the range of \[0, 128\] was specified.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7f3e7-163">Commenti</span><span class="sxs-lookup"><span data-stu-id="7f3e7-163">Remarks</span></span>

<span data-ttu-id="7f3e7-164">La funzione [**glMaterialfv**](glmaterialf.md) assegna valori ai parametri del materiale.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-164">The [**glMaterialfv**](glmaterialf.md) function assigns values to material parameters.</span></span> <span data-ttu-id="7f3e7-165">Sono disponibili due set di parametri Material corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-165">There are two matched sets of material parameters.</span></span> <span data-ttu-id="7f3e7-166">Uno, il set in *primo piano* , viene usato per ombreggiare punti, linee, bitmap e tutti i poligoni (quando l'illuminazione bilaterale è disabilitata) o solo i poligoni di fronte (quando è abilitata l'illuminazione bilaterale).</span><span class="sxs-lookup"><span data-stu-id="7f3e7-166">One, the *front-facing* set, is used to shade points, lines, bitmaps, and all polygons (when two-sided lighting is disabled), or just front-facing polygons (when two-sided lighting is enabled).</span></span> <span data-ttu-id="7f3e7-167">L'altro set, *back-facing*, viene usato per ombreggiare i poligoni di back-end solo quando è abilitata l'illuminazione a due lati.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-167">The other set, *back-facing*, is used to shade back-facing polygons only when two-sided lighting is enabled.</span></span> <span data-ttu-id="7f3e7-168">Per informazioni dettagliate sui calcoli di illuminazione unilaterale e bilaterale, vedere [**glLightModel**](gllightmodel-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="7f3e7-168">Refer to [**glLightModel**](gllightmodel-functions.md) for details concerning one-sided and two-sided lighting calculations.</span></span>

<span data-ttu-id="7f3e7-169">La funzione [**glMaterialfv**](glmaterialf.md) accetta tre argomenti.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-169">The [**glMaterialfv**](glmaterialf.md) function takes three arguments.</span></span> <span data-ttu-id="7f3e7-170">Il *primo, ovvero, specifica* se i materiali di contabilità GL \_ , i \_ materiali back GL o entrambi i \_ materiali GL front \_ e \_ back verranno modificati.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-170">The first, *face*, specifies whether the GL\_FRONT materials, the GL\_BACK materials, or both GL\_FRONT\_AND\_BACK materials will be modified.</span></span> <span data-ttu-id="7f3e7-171">Il secondo, *pname*, specifica quale dei diversi parametri in uno o entrambi i set verranno modificati.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-171">The second, *pname*, specifies which of several parameters in one or both sets will be modified.</span></span> <span data-ttu-id="7f3e7-172">Il *terzo parametro specifica* il valore che verrà assegnato al parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-172">The third, *param*, specifies what value will be assigned to the specified parameter.</span></span>

<span data-ttu-id="7f3e7-173">I parametri del materiale vengono usati nell'equazione di illuminazione applicata facoltativamente a ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-173">Material parameters are used in the lighting equation that is optionally applied to each vertex.</span></span> <span data-ttu-id="7f3e7-174">L'equazione viene illustrata in [**glLightModel**](gllightmodel-functions.md).</span><span class="sxs-lookup"><span data-stu-id="7f3e7-174">The equation is discussed in [**glLightModel**](gllightmodel-functions.md).</span></span>

<span data-ttu-id="7f3e7-175">I parametri Material possono essere aggiornati in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-175">The material parameters can be updated at any time.</span></span> <span data-ttu-id="7f3e7-176">In particolare, è possibile chiamare [**glMaterialfv**](glmaterialf.md) tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="7f3e7-176">In particular, [**glMaterialfv**](glmaterialf.md) can be called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="7f3e7-177">Se è necessario modificare un solo parametro Material per ogni vertice, tuttavia, [**glColorMaterial**](glcolormaterial.md) è preferibile rispetto a **glMaterialfv**.</span><span class="sxs-lookup"><span data-stu-id="7f3e7-177">If only a single material parameter is to be changed per vertex, however, [**glColorMaterial**](glcolormaterial.md) is preferred over **glMaterialfv**.</span></span>

<span data-ttu-id="7f3e7-178">La funzione seguente recupera le informazioni correlate a [**glMaterialfv**](glmaterialf.md):</span><span class="sxs-lookup"><span data-stu-id="7f3e7-178">The following function retrieves information related to [**glMaterialfv**](glmaterialf.md):</span></span>

[<span data-ttu-id="7f3e7-179">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="7f3e7-179">**glGetMaterial**</span></span>](glgetmaterial.md)

## <a name="requirements"></a><span data-ttu-id="7f3e7-180">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f3e7-180">Requirements</span></span>



| <span data-ttu-id="7f3e7-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f3e7-181">Requirement</span></span> | <span data-ttu-id="7f3e7-182">Valore</span><span class="sxs-lookup"><span data-stu-id="7f3e7-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f3e7-183">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f3e7-183">Minimum supported client</span></span><br/> | <span data-ttu-id="7f3e7-184">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7f3e7-184">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7f3e7-185">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f3e7-185">Minimum supported server</span></span><br/> | <span data-ttu-id="7f3e7-186">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7f3e7-186">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7f3e7-187">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7f3e7-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f3e7-188"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f3e7-188"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="7f3e7-189">Libreria</span><span class="sxs-lookup"><span data-stu-id="7f3e7-189">Library</span></span><br/>                  | <dl> <span data-ttu-id="7f3e7-190"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f3e7-190"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7f3e7-191">DLL</span><span class="sxs-lookup"><span data-stu-id="7f3e7-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f3e7-192"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f3e7-192"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f3e7-193">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f3e7-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f3e7-194">**glColorMaterial**</span><span class="sxs-lookup"><span data-stu-id="7f3e7-194">**glColorMaterial**</span></span>](glcolormaterial.md)
</dt> <dt>

[<span data-ttu-id="7f3e7-195">**glLight**</span><span class="sxs-lookup"><span data-stu-id="7f3e7-195">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="7f3e7-196">**glLightModel**</span><span class="sxs-lookup"><span data-stu-id="7f3e7-196">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> </dl>

 

 





