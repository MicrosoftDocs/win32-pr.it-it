---
title: funzione glFogfv (GL. h)
description: La funzione glFogfv specifica i parametri di nebbia. | funzione glFogfv (GL. h)
ms.assetid: a2243ff4-4f3a-4b8c-b4fb-ce2cd74815e4
keywords:
- funzione glFogfv OpenGL
topic_type:
- apiref
api_name:
- glFogfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b407dd9b9c984a744e903a2c269d21028d32977a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234896"
---
# <a name="glfogfv-function"></a><span data-ttu-id="853eb-105">glFogfv (funzione)</span><span class="sxs-lookup"><span data-stu-id="853eb-105">glFogfv function</span></span>

<span data-ttu-id="853eb-106">La funzione **glFogfv** specifica i parametri di nebbia.</span><span class="sxs-lookup"><span data-stu-id="853eb-106">The **glFogfv** function specifies fog parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="853eb-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="853eb-107">Syntax</span></span>


```C++
void WINAPI glFogfv(
         GLenum  pname,
   const GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="853eb-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="853eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="853eb-109">*pname*</span><span class="sxs-lookup"><span data-stu-id="853eb-109">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="853eb-110">Specifica un parametro Fog.</span><span class="sxs-lookup"><span data-stu-id="853eb-110">Specifies a fog parameter.</span></span>

<span data-ttu-id="853eb-111">Accetta uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="853eb-111">Accepts one of the following values.</span></span>



| <span data-ttu-id="853eb-112">Valore</span><span class="sxs-lookup"><span data-stu-id="853eb-112">Value</span></span>                                                                                                                                                             | <span data-ttu-id="853eb-113">Significato</span><span class="sxs-lookup"><span data-stu-id="853eb-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_MODE"></span><span id="gl_fog_mode"></span><dl> <span data-ttu-id="853eb-114"><dt>**\_modalità di nebbia GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="853eb-114"><dt>**GL\_FOG\_MODE**</dt></span></span> </dl>          | <span data-ttu-id="853eb-115">Il parametro *params* è un valore a virgola mobile che specifica l'equazione da usare per calcolare il fattore di Blend di nebbia, *f*.</span><span class="sxs-lookup"><span data-stu-id="853eb-115">The *params* parameter is a floating-point value that specifies the equation to be used to compute the fog blend factor, *f*.</span></span> <span data-ttu-id="853eb-116">Sono accettate tre costanti simboliche: GL \_ Linear, GL \_ exp e GL \_ exp2.</span><span class="sxs-lookup"><span data-stu-id="853eb-116">Three symbolic constants are accepted: GL\_LINEAR, GL\_EXP, and GL\_EXP2.</span></span> <span data-ttu-id="853eb-117">Le equazioni corrispondenti a queste costanti simboliche sono definite nella sezione Osservazioni riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="853eb-117">The equations corresponding to these symbolic constants are defined in the following Remarks section.</span></span> <span data-ttu-id="853eb-118">La modalità di nebbia predefinita è GL \_ Exp.</span><span class="sxs-lookup"><span data-stu-id="853eb-118">The default fog mode is GL\_EXP.</span></span><br/>                                                                           |
| <span id="GL_FOG_DENSITY"></span><span id="gl_fog_density"></span><dl> <span data-ttu-id="853eb-119"><dt>**\_densità di nebbia GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="853eb-119"><dt>**GL\_FOG\_DENSITY**</dt></span></span> </dl> | <span data-ttu-id="853eb-120">Il parametro *params* è un valore a virgola mobile che specifica la *densità*, la densità di nebbia usata in entrambe le equazioni di nebbia esponenziale.</span><span class="sxs-lookup"><span data-stu-id="853eb-120">The *params* parameter is a floating-point value that specifies *density*, the fog density used in both exponential fog equations.</span></span> <span data-ttu-id="853eb-121">Vengono accettate solo le densità non negative.</span><span class="sxs-lookup"><span data-stu-id="853eb-121">Only nonnegative densities are accepted.</span></span> <span data-ttu-id="853eb-122">La densità di nebbia predefinita è 1,0.</span><span class="sxs-lookup"><span data-stu-id="853eb-122">The default fog density is 1.0.</span></span><br/>                                                                                                                                                                                                              |
| <span id="GL_FOG_START"></span><span id="gl_fog_start"></span><dl> <span data-ttu-id="853eb-123"><dt>**\_inizio di nebbia GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="853eb-123"><dt>**GL\_FOG\_START**</dt></span></span> </dl>       | <span data-ttu-id="853eb-124">Il parametro *params* è un valore a virgola mobile che specifica *Start*, la distanza vicina utilizzata nell'equazione Linear Fog.</span><span class="sxs-lookup"><span data-stu-id="853eb-124">The *params* parameter is a floating-point value that specifies *start*, the near distance used in the linear fog equation.</span></span> <span data-ttu-id="853eb-125">La distanza quasi predefinita è 0,0.</span><span class="sxs-lookup"><span data-stu-id="853eb-125">The default near distance is 0.0.</span></span><br/>                                                                                                                                                                                                                                                            |
| <span id="GL_FOG_END"></span><span id="gl_fog_end"></span><dl> <span data-ttu-id="853eb-126"><dt>**\_fine nebbia \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="853eb-126"><dt>**GL\_FOG\_END**</dt></span></span> </dl>             | <span data-ttu-id="853eb-127">Il parametro *params* è un valore a virgola mobile che specifica *end*, la distanza distante utilizzata nell'equazione lineare di nebbia.</span><span class="sxs-lookup"><span data-stu-id="853eb-127">The *params* parameter is a floating-point value that specifies *end*, the far distance used in the linear fog equation.</span></span> <span data-ttu-id="853eb-128">La distanza predefinita è 1,0.</span><span class="sxs-lookup"><span data-stu-id="853eb-128">The default far distance is 1.0.</span></span><br/>                                                                                                                                                                                                                                                                |
| <span id="GL_FOG_INDEX"></span><span id="gl_fog_index"></span><dl> <span data-ttu-id="853eb-129"><dt>**\_indice di nebbia GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="853eb-129"><dt>**GL\_FOG\_INDEX**</dt></span></span> </dl>       | <span data-ttu-id="853eb-130">Il parametro *params* è un valore a virgola mobile che specifica *i*<sub>f</sub> , ovvero l'indice dei colori di nebbia.</span><span class="sxs-lookup"><span data-stu-id="853eb-130">The *params* parameter is a floating-point value that specifies *i*<sub>f</sub> , the fog color index.</span></span> <span data-ttu-id="853eb-131">L'indice di nebbia predefinito è 0,0.</span><span class="sxs-lookup"><span data-stu-id="853eb-131">The default fog index is 0.0.</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <span id="GL_FOG_COLOR"></span><span id="gl_fog_color"></span><dl> <span data-ttu-id="853eb-132"><dt>**\_colore di nebbia GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="853eb-132"><dt>**GL\_FOG\_COLOR**</dt></span></span> </dl>       | <span data-ttu-id="853eb-133">Il parametro *params* contiene quattro valori a virgola mobile che specificano *C*<sub>f</sub> , il colore di nebbia.</span><span class="sxs-lookup"><span data-stu-id="853eb-133">The *params* parameter contains four floating-point values that specify *C*<sub>f</sub> , the fog color.</span></span> <span data-ttu-id="853eb-134">Ai valori integer viene eseguito il mapping lineare, in modo che il valore rappresentabile più positivo sia mappato a 1,0 e il valore rappresentativo più negativo sia mappato a-1,0.</span><span class="sxs-lookup"><span data-stu-id="853eb-134">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="853eb-135">Ai valori a virgola mobile viene eseguito il mapping diretto.</span><span class="sxs-lookup"><span data-stu-id="853eb-135">Floating-point values are mapped directly.</span></span> <span data-ttu-id="853eb-136">Dopo la conversione, tutti i componenti dei colori vengono bloccati nell'intervallo compreso tra \[ 0 e 1 \] .</span><span class="sxs-lookup"><span data-stu-id="853eb-136">After conversion, all color components are clamped to the range \[0,1\].</span></span> <span data-ttu-id="853eb-137">Il colore di nebbia predefinito è (0, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="853eb-137">The default fog color is (0,0,0,0).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="853eb-138">*params*</span><span class="sxs-lookup"><span data-stu-id="853eb-138">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="853eb-139">Specifica il valore o i valori da assegnare a *pname*.</span><span class="sxs-lookup"><span data-stu-id="853eb-139">Specifies the value or values to be assigned to *pname*.</span></span> <span data-ttu-id="853eb-140">Il \_ \_ colore della nebbia GL richiede una matrice di quattro valori.</span><span class="sxs-lookup"><span data-stu-id="853eb-140">GL\_FOG\_COLOR requires an array of four values.</span></span> <span data-ttu-id="853eb-141">Tutti gli altri parametri accettano una matrice contenente solo un valore singolo.</span><span class="sxs-lookup"><span data-stu-id="853eb-141">All other parameters accept an array containing only a single value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="853eb-142">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="853eb-142">Return value</span></span>

<span data-ttu-id="853eb-143">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="853eb-143">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="853eb-144">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="853eb-144">Error codes</span></span>

<span data-ttu-id="853eb-145">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="853eb-145">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="853eb-146">Nome</span><span class="sxs-lookup"><span data-stu-id="853eb-146">Name</span></span>                                                                                                  | <span data-ttu-id="853eb-147">Significato</span><span class="sxs-lookup"><span data-stu-id="853eb-147">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="853eb-148"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="853eb-148"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="853eb-149">*pname* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="853eb-149">*pname* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="853eb-150"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="853eb-150"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="853eb-151">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="853eb-151">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="853eb-152">Commenti</span><span class="sxs-lookup"><span data-stu-id="853eb-152">Remarks</span></span>

<span data-ttu-id="853eb-153">Per abilitare e disabilitare Fog con [**glEnable**](glenable.md) e [**glDisable**](gldisable.md), è possibile usare l'argomento per la \_ nebbia.</span><span class="sxs-lookup"><span data-stu-id="853eb-153">You enable and disable fog with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md), using the argument GL\_FOG.</span></span> <span data-ttu-id="853eb-154">Se abilitata, la nebbia interessa la geometria rasterizzata, le bitmap e i blocchi pixel, ma non le operazioni di cancellazione del buffer.</span><span class="sxs-lookup"><span data-stu-id="853eb-154">While enabled, fog affects rasterized geometry, bitmaps, and pixel blocks, but not buffer-clear operations.</span></span>

<span data-ttu-id="853eb-155">La funzione **glFogfv** assegna il valore o i valori in *params* al parametro Fog specificato da *pname*.</span><span class="sxs-lookup"><span data-stu-id="853eb-155">The **glFogfv** function assigns the value or values in *params* to the fog parameter specified by *pname*.</span></span>

<span data-ttu-id="853eb-156">Nebbia combina un colore di nebbia con ogni colore di post-texturing del frammento di pixel rasterizzato usando un fattore di fusione *f*.</span><span class="sxs-lookup"><span data-stu-id="853eb-156">Fog blends a fog color with each rasterized pixel fragment's posttexturing color using a blending factor *f*.</span></span> <span data-ttu-id="853eb-157">Il fattore *f* viene calcolato in uno dei tre modi seguenti, a seconda della modalità di nebbia.</span><span class="sxs-lookup"><span data-stu-id="853eb-157">Factor *f* is computed in one of three ways, depending on the fog mode.</span></span> <span data-ttu-id="853eb-158">Lasciare che *z* sia la distanza nelle coordinate oculari dall'origine al frammento a cui si sta eseguendo la nebbia.</span><span class="sxs-lookup"><span data-stu-id="853eb-158">Let *z* be the distance in eye coordinates from the origin to the fragment being fogged.</span></span> <span data-ttu-id="853eb-159">L'equazione per GL \_ Linear Fog è:</span><span class="sxs-lookup"><span data-stu-id="853eb-159">The equation for GL\_LINEAR fog is:</span></span>

![Equazione che mostra il valore di GL_LINEAR nebbia.](images/fog01.png)

<span data-ttu-id="853eb-161">L'equazione per GL \_ Exp Fog è:</span><span class="sxs-lookup"><span data-stu-id="853eb-161">The equation for GL\_EXP fog is:</span></span>

![Equazione che mostra il valore del fattore di fusione in modalità GL_EXP nebbia.](images/fog02.png)

<span data-ttu-id="853eb-163">L'equazione per GL \_ exp2 Fog è:</span><span class="sxs-lookup"><span data-stu-id="853eb-163">The equation for GL\_EXP2 fog is:</span></span>

![Equazione che mostra il valore del fattore di fusione in modalità GL_EXP2 nebbia.](images/fog03.png)

<span data-ttu-id="853eb-165">Indipendentemente dalla modalità di nebbia, *f* viene bloccato nell'intervallo \[ 0, 1 dopo il \] calcolo.</span><span class="sxs-lookup"><span data-stu-id="853eb-165">Regardless of the fog mode, *f* is clamped to the range \[0,1\] after it is computed.</span></span> <span data-ttu-id="853eb-166">Quindi, se OpenGL è in modalità colore RGBA, il colore *C*<sub>r</sub> del frammento viene sostituito da</span><span class="sxs-lookup"><span data-stu-id="853eb-166">Then, if OpenGL is in RGBA color mode, the fragment's color *C*<sub>r</sub> is replaced by</span></span>

![Equazione che mostra il colore del frammento offuscato come funzione di combinazione del fattore e del colore nebbia.](images/fog04.png)

<span data-ttu-id="853eb-168">In modalità di indice dei colori, l'indice di colore del frammento *i*<sub>r</sub> viene sostituito da</span><span class="sxs-lookup"><span data-stu-id="853eb-168">In color-index mode, the fragment's color index *i*<sub>r</sub> is replaced by</span></span>

![Equazione che mostra l'indice dei colori del frammento con offuscamento come funzione del fattore di fusione e del colore indicizzato.](images/fog05.png)

<span data-ttu-id="853eb-170">Le funzioni seguenti consentono di recuperare informazioni correlate alle funzioni **glFog** :</span><span class="sxs-lookup"><span data-stu-id="853eb-170">The following functions retrieve information related to the **glFog** functions:</span></span>

<span data-ttu-id="853eb-171">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento del \_ colore della nebbia GL \_</span><span class="sxs-lookup"><span data-stu-id="853eb-171">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_FOG\_COLOR</span></span>

<span data-ttu-id="853eb-172">**glGet** con argument GL \_ Fog \_ index</span><span class="sxs-lookup"><span data-stu-id="853eb-172">**glGet** with argument GL\_FOG\_INDEX</span></span>

<span data-ttu-id="853eb-173">**glGet** con densità di \_ nebbia argomento GL \_</span><span class="sxs-lookup"><span data-stu-id="853eb-173">**glGet** with argument GL\_FOG\_DENSITY</span></span>

<span data-ttu-id="853eb-174">**glGet** con argument GL \_ Fog \_ Start</span><span class="sxs-lookup"><span data-stu-id="853eb-174">**glGet** with argument GL\_FOG\_START</span></span>

<span data-ttu-id="853eb-175">**glGet** con argomento di \_ \_ fine nebbia</span><span class="sxs-lookup"><span data-stu-id="853eb-175">**glGet** with argument GL\_FOG\_END</span></span>

<span data-ttu-id="853eb-176">**glGet** con argomento della \_ modalità di nebbia GL \_</span><span class="sxs-lookup"><span data-stu-id="853eb-176">**glGet** with argument GL\_FOG\_MODE</span></span>

<span data-ttu-id="853eb-177">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Fog</span><span class="sxs-lookup"><span data-stu-id="853eb-177">[**glIsEnabled**](glisenabled.md) with argument GL\_FOG</span></span>

## <a name="requirements"></a><span data-ttu-id="853eb-178">Requisiti</span><span class="sxs-lookup"><span data-stu-id="853eb-178">Requirements</span></span>



| <span data-ttu-id="853eb-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="853eb-179">Requirement</span></span> | <span data-ttu-id="853eb-180">Valore</span><span class="sxs-lookup"><span data-stu-id="853eb-180">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="853eb-181">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="853eb-181">Minimum supported client</span></span><br/> | <span data-ttu-id="853eb-182">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="853eb-182">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="853eb-183">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="853eb-183">Minimum supported server</span></span><br/> | <span data-ttu-id="853eb-184">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="853eb-184">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="853eb-185">Intestazione</span><span class="sxs-lookup"><span data-stu-id="853eb-185">Header</span></span><br/>                   | <dl> <span data-ttu-id="853eb-186"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="853eb-186"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="853eb-187">Libreria</span><span class="sxs-lookup"><span data-stu-id="853eb-187">Library</span></span><br/>                  | <dl> <span data-ttu-id="853eb-188"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="853eb-188"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="853eb-189">DLL</span><span class="sxs-lookup"><span data-stu-id="853eb-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="853eb-190"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="853eb-190"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="853eb-191">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="853eb-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="853eb-192">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="853eb-192">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="853eb-193">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="853eb-193">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="853eb-194">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="853eb-194">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="853eb-195">**Remo**</span><span class="sxs-lookup"><span data-stu-id="853eb-195">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="853eb-196">**glGet**</span><span class="sxs-lookup"><span data-stu-id="853eb-196">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="853eb-197">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="853eb-197">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





