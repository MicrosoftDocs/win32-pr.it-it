---
title: funzione glLightf (GL. h)
description: La funzione glLightf restituisce i valori dei parametri di origine chiaro.
ms.assetid: d9f93fd9-6674-486f-a3fc-c10255dd37e7
keywords:
- funzione glLightf OpenGL
topic_type:
- apiref
api_name:
- glLightf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 099490461f5fbf6feb009e98c0228165938326d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743122"
---
# <a name="gllightf-function"></a><span data-ttu-id="fdbe5-104">glLightf (funzione)</span><span class="sxs-lookup"><span data-stu-id="fdbe5-104">glLightf function</span></span>

<span data-ttu-id="fdbe5-105">La funzione **glLightf** restituisce i valori dei parametri di origine chiaro.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-105">The **glLightf** function returns light source parameter values.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdbe5-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fdbe5-106">Syntax</span></span>


```C++
void WINAPI glLightf(
   GLenum  light,
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a><span data-ttu-id="fdbe5-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="fdbe5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdbe5-108">*light*</span><span class="sxs-lookup"><span data-stu-id="fdbe5-108">*light*</span></span> 
</dt> <dd>

<span data-ttu-id="fdbe5-109">Identificatore di una luce.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-109">The identifier of a light.</span></span> <span data-ttu-id="fdbe5-110">Il numero di spie possibili dipende dall'implementazione, ma sono supportate almeno otto luci.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-110">The number of possible lights depends on the implementation, but at least eight lights are supported.</span></span> <span data-ttu-id="fdbe5-111">Sono identificati da nomi simbolici nel formato GL \_ Light *i* dove *i* è un valore: da 0 a GL \_ Max \_ Lights-1.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-111">They are identified by symbolic names of the form GL\_LIGHT *i* where *i* is a value: 0 to GL\_MAX\_LIGHTS - 1.</span></span>

</dd> <dt>

<span data-ttu-id="fdbe5-112">*pname*</span><span class="sxs-lookup"><span data-stu-id="fdbe5-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="fdbe5-113">Parametro della sorgente di luce a valore singolo per la *luce*.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-113">A single-valued light source parameter for *light*.</span></span> <span data-ttu-id="fdbe5-114">I nomi simbolici seguenti sono accettati.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-114">The following symbolic names are accepted.</span></span>



| <span data-ttu-id="fdbe5-115">Valore</span><span class="sxs-lookup"><span data-stu-id="fdbe5-115">Value</span></span>                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="fdbe5-116">Significato</span><span class="sxs-lookup"><span data-stu-id="fdbe5-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span><dl> <span data-ttu-id="fdbe5-117"><dt>**\_esponente spot GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fdbe5-117"><dt>**GL\_SPOT\_EXPONENT**</dt></span></span> </dl>                                                                                                                                                                             | <span data-ttu-id="fdbe5-118">Il parametro *param* è un singolo valore a virgola mobile che specifica la distribuzione dell'intensità della luce.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-118">The *param* parameter is a single floating-point value that specifies the intensity distribution of the light.</span></span> <span data-ttu-id="fdbe5-119">Ai valori a virgola mobile viene eseguito il mapping diretto.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-119">Floating-point values are mapped directly.</span></span> <span data-ttu-id="fdbe5-120">Sono accettati solo i valori nell'intervallo compreso tra \[ 0 e 128 \] .</span><span class="sxs-lookup"><span data-stu-id="fdbe5-120">Only values in the range \[0, 128\] are accepted.</span></span> <br/> <span data-ttu-id="fdbe5-121">L'intensità di luce effettiva viene attenuata in base al coseno dell'angolo tra la direzione della luce e la direzione dalla luce al vertice che viene illuminato, elevato alla potenza dell'esponente di spot.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-121">Effective light intensity is attenuated by the cosine of the angle between the direction of the light and the direction from the light to the vertex being lighted, raised to the power of the spot exponent.</span></span> <span data-ttu-id="fdbe5-122">Pertanto, gli esponenti di punti più elevati generano una fonte di luce più mirata, indipendentemente dall'angolo di taglio.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-122">Thus, higher spot exponents result in a more focused light source, regardless of the spot cutoff angle.</span></span> <span data-ttu-id="fdbe5-123">L'esponente spot predefinito è 0, ottenendo una distribuzione uniforme.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-123">The default spot exponent is 0, resulting in uniform light distribution.</span></span><br/> |
| <span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span><dl> <span data-ttu-id="fdbe5-124"><dt>**\_taglio GL spot \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fdbe5-124"><dt>**GL\_SPOT\_CUTOFF**</dt></span></span> </dl>                                                                                                                                                                                   | <span data-ttu-id="fdbe5-125">Il parametro *param* è un singolo valore a virgola mobile che specifica l'angolo di diffusione massimo di una sorgente di luce.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-125">The *param* parameter is a single floating-point value that specifies the maximum spread angle of a light source.</span></span> <span data-ttu-id="fdbe5-126">Ai valori a virgola mobile viene eseguito il mapping diretto.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-126">Floating-point values are mapped directly.</span></span> <span data-ttu-id="fdbe5-127">Vengono accettati solo i valori compresi tra \[ 0, 90 \] e il valore speciale 180.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-127">Only values in the range \[0, 90\], and the special value 180, are accepted.</span></span> <br/> <span data-ttu-id="fdbe5-128">Se l'angolo tra la direzione della luce e la direzione dalla luce al vertice che viene illuminato è maggiore dell'angolo di taglio, la luce viene mascherata completamente.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-128">If the angle between the direction of the light and the direction from the light to the vertex being lighted is greater than the spot cutoff angle, then the light is completely masked.</span></span> <span data-ttu-id="fdbe5-129">In caso contrario, l'intensità viene controllata dall'esponente spot e dai fattori di attenuazione.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-129">Otherwise, its intensity is controlled by the spot exponent and the attenuation factors.</span></span> <span data-ttu-id="fdbe5-130">Il valore predefinito per il punto di interruzione è 180, ottenendo una distribuzione chiara uniforme.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-130">The default spot cutoff is 180, resulting in uniform light distribution.</span></span><br/>       |
| <span id="GL_CONSTANT_ATTENUATION__GL_LINEAR_ATTENUATION__GL_QUADRATIC_ATTENUATION"></span><span id="gl_constant_attenuation__gl_linear_attenuation__gl_quadratic_attenuation"></span><dl> <span data-ttu-id="fdbe5-131"><dt>**\_ \_ attenuazione costante GL, \_ \_ attenuazione lineare GL, \_ attenuazione quadratica GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fdbe5-131"><dt>**GL\_CONSTANT\_ATTENUATION, GL\_LINEAR\_ATTENUATION, GL\_QUADRATIC\_ATTENUATION**</dt></span></span> </dl> | <span data-ttu-id="fdbe5-132">Il parametro *param* è un singolo valore a virgola mobile che specifica uno dei tre fattori di attenuazione della luce.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-132">The *param* parameter is a single floating-point value that specifies one of the three light attenuation factors.</span></span> <span data-ttu-id="fdbe5-133">Ai valori a virgola mobile viene eseguito il mapping diretto.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-133">Floating-point values are mapped directly.</span></span> <span data-ttu-id="fdbe5-134">Vengono accettati solo valori non negativi.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-134">Only nonnegative values are accepted.</span></span> <br/> <span data-ttu-id="fdbe5-135">Se la luce è posizionale, anziché direzionale, l'intensità viene attenuata dalla reciproca della somma di: il fattore costante, il fattore lineare moltiplicato per la distanza tra la luce e il vertice che viene illuminato e il fattore quadratico moltiplicato per il quadrato della stessa distanza.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-135">If the light is positional, rather than directional, its intensity is attenuated by the reciprocal of the sum of: the constant factor, the linear factor multiplied by the distance between the light and the vertex being lighted, and the quadratic factor multiplied by the square of the same distance.</span></span> <span data-ttu-id="fdbe5-136">I fattori di attenuazione predefiniti sono (1, 0, 0), con conseguente assenza di attenuazione.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-136">The default attenuation factors are (1,0,0), resulting in no attenuation.</span></span><br/>                   |



 

</dd> <dt>

<span data-ttu-id="fdbe5-137">*param*</span><span class="sxs-lookup"><span data-stu-id="fdbe5-137">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="fdbe5-138">Specifica il valore impostato per il parametro *pname* della *luce* sorgente chiara.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-138">Specifies the value that parameter *pname* of light source *light* will be set to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdbe5-139">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fdbe5-139">Return value</span></span>

<span data-ttu-id="fdbe5-140">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-140">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fdbe5-141">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="fdbe5-141">Error codes</span></span>

<span data-ttu-id="fdbe5-142">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="fdbe5-142">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="fdbe5-143">Nome</span><span class="sxs-lookup"><span data-stu-id="fdbe5-143">Name</span></span>                                                                                                  | <span data-ttu-id="fdbe5-144">Significato</span><span class="sxs-lookup"><span data-stu-id="fdbe5-144">Meaning</span></span>                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fdbe5-145"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fdbe5-145"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="fdbe5-146">*Light* o *pname* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-146">*light* or *pname* was not an accepted value.</span></span><br/>                                                                                                                                                                  |
| <dl> <span data-ttu-id="fdbe5-147"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fdbe5-147"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="fdbe5-148">Un valore dell'esponente spot è stato specificato al di fuori dell'intervallo compreso tra \[ 0, 128 o l'elemento \] cutoff è stato specificato al di fuori dell'intervallo \[ 0, 90 \] (ad eccezione del valore speciale 180) oppure è stato specificato un fattore di attenuazione negativo.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-148">A spot exponent value was specified outside the range \[0, 128\], or spot cutoff was specified outside the range \[0, 90\] (except for the special value 180), or a negative attenuation factor was specified.</span></span><br/> |
| <dl> <span data-ttu-id="fdbe5-149"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fdbe5-149"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="fdbe5-150">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="fdbe5-150">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                     |



## <a name="remarks"></a><span data-ttu-id="fdbe5-151">Commenti</span><span class="sxs-lookup"><span data-stu-id="fdbe5-151">Remarks</span></span>

<span data-ttu-id="fdbe5-152">La funzione **glLightf** imposta il valore o i valori dei singoli parametri della sorgente di luce.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-152">The **glLightf** function sets the value or values of individual light source parameters.</span></span> <span data-ttu-id="fdbe5-153">Il parametro *Light* denomina la luce e è un nome simbolico del formato GL \_ Light *i*, dove 0 = *i* < GL \_ Max \_ Lights.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-153">The *light* parameter names the light and is a symbolic name of the form GL\_LIGHT *i*, where 0 = *i* < GL\_MAX\_LIGHTS.</span></span>

<span data-ttu-id="fdbe5-154">Il parametro *pname* specifica uno dei parametri della sorgente di luce, di nuovo in base al nome simbolico.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-154">The *pname* parameter specifies one of the light source parameters, again by symbolic name.</span></span> <span data-ttu-id="fdbe5-155">Il parametro *param* può essere un singolo valore o un puntatore a una matrice che contiene i nuovi valori.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-155">The *param* parameter is either a single value or a pointer to an array that contains the new values.</span></span>

<span data-ttu-id="fdbe5-156">Il calcolo dell'illuminazione è abilitato e disabilitato usando [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) con l'illuminazione GL degli argomenti \_ .</span><span class="sxs-lookup"><span data-stu-id="fdbe5-156">Lighting calculation is enabled and disabled using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with argument GL\_LIGHTING.</span></span> <span data-ttu-id="fdbe5-157">Quando è abilitata l'illuminazione, le sorgenti luminose abilitate contribuiscono al calcolo dell'illuminazione.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-157">When lighting is enabled, light sources that are enabled contribute to the lighting calculation.</span></span> <span data-ttu-id="fdbe5-158">Source Light *i* è abilitato e disabilitato usando **glEnable** e **glDisable** con l'argomento GL \_ Light *i*.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-158">Light source *i* is enabled and disabled using **glEnable** and **glDisable** with argument GL\_LIGHT *i*.</span></span>

<span data-ttu-id="fdbe5-159">È sempre il caso GL \_ Light *i* = GL \_ LIGHT0 + *i*.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-159">It is always the case that GL\_LIGHT *i* = GL\_LIGHT0 + *i*.</span></span>

<span data-ttu-id="fdbe5-160">Le funzioni seguenti consentono di recuperare informazioni correlate alla funzione **glLightf** :</span><span class="sxs-lookup"><span data-stu-id="fdbe5-160">The following functions retrieve information related to the **glLightf** function:</span></span>

[<span data-ttu-id="fdbe5-161">**glGetLight**</span><span class="sxs-lookup"><span data-stu-id="fdbe5-161">**glGetLight**</span></span>](glgetlight.md)

<span data-ttu-id="fdbe5-162">[**glIsEnabled**](glisenabled.md) con illuminazione GL argomento \_</span><span class="sxs-lookup"><span data-stu-id="fdbe5-162">[**glIsEnabled**](glisenabled.md) with argument GL\_LIGHTING</span></span>

## <a name="requirements"></a><span data-ttu-id="fdbe5-163">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fdbe5-163">Requirements</span></span>



| <span data-ttu-id="fdbe5-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdbe5-164">Requirement</span></span> | <span data-ttu-id="fdbe5-165">Valore</span><span class="sxs-lookup"><span data-stu-id="fdbe5-165">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fdbe5-166">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fdbe5-166">Minimum supported client</span></span><br/> | <span data-ttu-id="fdbe5-167">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fdbe5-167">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fdbe5-168">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fdbe5-168">Minimum supported server</span></span><br/> | <span data-ttu-id="fdbe5-169">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fdbe5-169">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fdbe5-170">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fdbe5-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdbe5-171"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdbe5-171"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="fdbe5-172">Libreria</span><span class="sxs-lookup"><span data-stu-id="fdbe5-172">Library</span></span><br/>                  | <dl> <span data-ttu-id="fdbe5-173"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fdbe5-173"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="fdbe5-174">DLL</span><span class="sxs-lookup"><span data-stu-id="fdbe5-174">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fdbe5-175"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fdbe5-175"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdbe5-176">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fdbe5-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdbe5-177">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="fdbe5-177">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="fdbe5-178">**glColorMaterial**</span><span class="sxs-lookup"><span data-stu-id="fdbe5-178">**glColorMaterial**</span></span>](glcolormaterial.md)
</dt> <dt>

[<span data-ttu-id="fdbe5-179">**Remo**</span><span class="sxs-lookup"><span data-stu-id="fdbe5-179">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="fdbe5-180">**glLightModel**</span><span class="sxs-lookup"><span data-stu-id="fdbe5-180">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> <dt>

[<span data-ttu-id="fdbe5-181">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="fdbe5-181">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> </dl>

 

 





