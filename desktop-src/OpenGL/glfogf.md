---
title: funzione glFogf (GL. h)
description: GlFogf e Function specificano i parametri di nebbia.
ms.assetid: 69961d8f-385c-4353-aef3-38fb654c44f8
keywords:
- funzione glFogf OpenGL
topic_type:
- apiref
api_name:
- glFogf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfe0509b30e91797752604110068701fcedaa266
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "104058399"
---
# <a name="glfogf-function"></a><span data-ttu-id="6e0ea-104">glFogf (funzione)</span><span class="sxs-lookup"><span data-stu-id="6e0ea-104">glFogf function</span></span>

<span data-ttu-id="6e0ea-105">**GlFogf** e Function specificano i parametri di nebbia.</span><span class="sxs-lookup"><span data-stu-id="6e0ea-105">The **glFogf** and function specifies fog parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e0ea-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6e0ea-106">Syntax</span></span>


```C++
void WINAPI glFogf(
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a><span data-ttu-id="6e0ea-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="6e0ea-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e0ea-108">*pname*</span><span class="sxs-lookup"><span data-stu-id="6e0ea-108">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="6e0ea-109">Specifica un parametro di nebbia a valore singolo.</span><span class="sxs-lookup"><span data-stu-id="6e0ea-109">Specifies a single-valued fog parameter.</span></span>

<span data-ttu-id="6e0ea-110">Accetta uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="6e0ea-110">Accepts one of the following values.</span></span>



| <span data-ttu-id="6e0ea-111">Valore</span><span class="sxs-lookup"><span data-stu-id="6e0ea-111">Value</span></span>                                                                                                                                                             | <span data-ttu-id="6e0ea-112">Significato</span><span class="sxs-lookup"><span data-stu-id="6e0ea-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_MODE"></span><span id="gl_fog_mode"></span><dl> <span data-ttu-id="6e0ea-113"><dt>**\_modalità di nebbia GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6e0ea-113"><dt>**GL\_FOG\_MODE**</dt></span></span> </dl>          | <span data-ttu-id="6e0ea-114">Il parametro *params* è un singolo valore a virgola mobile che specifica l'equazione da usare per calcolare il fattore di Blend di nebbia, *f*.</span><span class="sxs-lookup"><span data-stu-id="6e0ea-114">The *params* parameter is a single floating-point value that specifies the equation to be used to compute the fog blend factor, *f*.</span></span> <span data-ttu-id="6e0ea-115">Sono accettate tre costanti simboliche: GL \_ Linear, GL \_ exp e GL \_ exp2.</span><span class="sxs-lookup"><span data-stu-id="6e0ea-115">Three symbolic constants are accepted: GL\_LINEAR, GL\_EXP, and GL\_EXP2.</span></span> <span data-ttu-id="6e0ea-116">Le equazioni corrispondenti a queste costanti simboliche sono definite nella sezione Osservazioni riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="6e0ea-116">The equations corresponding to these symbolic constants are defined in the following Remarks section.</span></span> <span data-ttu-id="6e0ea-117">La modalità di nebbia predefinita è GL \_ Exp.</span><span class="sxs-lookup"><span data-stu-id="6e0ea-117">The default fog mode is GL\_EXP.</span></span><br/> |
| <span id="GL_FOG_DENSITY"></span><span id="gl_fog_density"></span><dl> <span data-ttu-id="6e0ea-118"><dt>**\_densità di nebbia GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6e0ea-118"><dt>**GL\_FOG\_DENSITY**</dt></span></span> </dl> | <span data-ttu-id="6e0ea-119">Il parametro *params* è un singolo valore a virgola mobile che specifica la *densità*, la densità di nebbia usata in entrambe le equazioni di nebbia esponenziale.</span><span class="sxs-lookup"><span data-stu-id="6e0ea-119">The *params* parameter is a single floating-point value that specifies *density*, the fog density used in both exponential fog equations.</span></span> <span data-ttu-id="6e0ea-120">Vengono accettate solo le densità non negative.</span><span class="sxs-lookup"><span data-stu-id="6e0ea-120">Only nonnegative densities are accepted.</span></span> <span data-ttu-id="6e0ea-121">La densità di nebbia predefinita è 1,0.</span><span class="sxs-lookup"><span data-stu-id="6e0ea-121">The default fog density is 1.0.</span></span><br/>                                                                                                                                    |
| <span id="GL_FOG_START"></span><span id="gl_fog_start"></span><dl> <span data-ttu-id="6e0ea-122"><dt>**\_inizio di nebbia GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6e0ea-122"><dt>**GL\_FOG\_START**</dt></span></span> </dl>       | <span data-ttu-id="6e0ea-123">Il parametro *params* è un singolo valore a virgola mobile che specifica *Start*, la distanza vicina utilizzata nell'equazione Linear Fog.</span><span class="sxs-lookup"><span data-stu-id="6e0ea-123">The *params* parameter is a single floating-point value that specifies *start*, the near distance used in the linear fog equation.</span></span> <span data-ttu-id="6e0ea-124">La distanza quasi predefinita è 0,0.</span><span class="sxs-lookup"><span data-stu-id="6e0ea-124">The default near distance is 0.0.</span></span><br/>                                                                                                                                                                                  |
| <span id="GL_FOG_END"></span><span id="gl_fog_end"></span><dl> <span data-ttu-id="6e0ea-125"><dt>**\_fine nebbia \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="6e0ea-125"><dt>**GL\_FOG\_END**</dt></span></span> </dl>             | <span data-ttu-id="6e0ea-126">Il parametro *params* è un singolo valore a virgola mobile che specifica *end*, la distanza massima utilizzata nell'equazione Linear Fog.</span><span class="sxs-lookup"><span data-stu-id="6e0ea-126">The *params* parameter is a single floating-point value that specifies *end*, the far distance used in the linear fog equation.</span></span> <span data-ttu-id="6e0ea-127">La distanza predefinita è 1,0.</span><span class="sxs-lookup"><span data-stu-id="6e0ea-127">The default far distance is 1.0.</span></span><br/>                                                                                                                                                                                      |
| <span id="GL_FOG_INDEX"></span><span id="gl_fog_index"></span><dl> <span data-ttu-id="6e0ea-128"><dt>**\_indice di nebbia GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6e0ea-128"><dt>**GL\_FOG\_INDEX**</dt></span></span> </dl>       | <span data-ttu-id="6e0ea-129">Il parametro *params* è un singolo valore a virgola mobile che specifica *i*<sub>f</sub> , ovvero l'indice dei colori di nebbia.</span><span class="sxs-lookup"><span data-stu-id="6e0ea-129">The *params* parameter is a single floating-point value that specifies *i*<sub>f</sub> , the fog color index.</span></span> <span data-ttu-id="6e0ea-130">L'indice di nebbia predefinito è 0,0.</span><span class="sxs-lookup"><span data-stu-id="6e0ea-130">The default fog index is 0.0.</span></span><br/>                                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="6e0ea-131">*param*</span><span class="sxs-lookup"><span data-stu-id="6e0ea-131">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="6e0ea-132">Specifica il valore su cui verrà impostato *pname* .</span><span class="sxs-lookup"><span data-stu-id="6e0ea-132">Specifies the value that *pname* will be set to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e0ea-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6e0ea-133">Return value</span></span>

<span data-ttu-id="6e0ea-134">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="6e0ea-134">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6e0ea-135">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="6e0ea-135">Error codes</span></span>

<span data-ttu-id="6e0ea-136">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="6e0ea-136">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="6e0ea-137">Nome</span><span class="sxs-lookup"><span data-stu-id="6e0ea-137">Name</span></span>                                                                                                  | <span data-ttu-id="6e0ea-138">Significato</span><span class="sxs-lookup"><span data-stu-id="6e0ea-138">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6e0ea-139"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6e0ea-139"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="6e0ea-140">*pname* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="6e0ea-140">*pname* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="6e0ea-141"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6e0ea-141"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="6e0ea-142">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="6e0ea-142">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6e0ea-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="6e0ea-143">Remarks</span></span>

<span data-ttu-id="6e0ea-144">Per abilitare e disabilitare Fog con [**glEnable**](glenable.md) e [**glDisable**](gldisable.md), è possibile usare l'argomento per la \_ nebbia.</span><span class="sxs-lookup"><span data-stu-id="6e0ea-144">You enable and disable fog with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md), using the argument GL\_FOG.</span></span> <span data-ttu-id="6e0ea-145">Se abilitata, la nebbia interessa la geometria rasterizzata, le bitmap e i blocchi pixel, ma non le operazioni di cancellazione del buffer.</span><span class="sxs-lookup"><span data-stu-id="6e0ea-145">While enabled, fog affects rasterized geometry, bitmaps, and pixel blocks, but not buffer-clear operations.</span></span>

<span data-ttu-id="6e0ea-146">La funzione **glFogf** assegna il valore o i valori in *params* al parametro Fog specificato da *pname*.</span><span class="sxs-lookup"><span data-stu-id="6e0ea-146">The **glFogf** function assigns the value or values in *params* to the fog parameter specified by *pname*.</span></span>

<span data-ttu-id="6e0ea-147">Nebbia combina un colore di nebbia con ogni colore di post-texturing del frammento di pixel rasterizzato usando un fattore di fusione *f*.</span><span class="sxs-lookup"><span data-stu-id="6e0ea-147">Fog blends a fog color with each rasterized pixel fragment's posttexturing color using a blending factor *f*.</span></span> <span data-ttu-id="6e0ea-148">Il fattore *f* viene calcolato in uno dei tre modi seguenti, a seconda della modalità di nebbia.</span><span class="sxs-lookup"><span data-stu-id="6e0ea-148">Factor *f* is computed in one of three ways, depending on the fog mode.</span></span> <span data-ttu-id="6e0ea-149">Lasciare che *z* sia la distanza nelle coordinate oculari dall'origine al frammento a cui si sta eseguendo la nebbia.</span><span class="sxs-lookup"><span data-stu-id="6e0ea-149">Let *z* be the distance in eye coordinates from the origin to the fragment being fogged.</span></span> <span data-ttu-id="6e0ea-150">L'equazione per GL \_ Linear Fog è:</span><span class="sxs-lookup"><span data-stu-id="6e0ea-150">The equation for GL\_LINEAR fog is:</span></span>

![Equazione che mostra il valore di GL_LINEAR nebbia.](images/fog01.png)

<span data-ttu-id="6e0ea-152">L'equazione per GL \_ Exp Fog è:</span><span class="sxs-lookup"><span data-stu-id="6e0ea-152">The equation for GL\_EXP fog is:</span></span>

![Equazione che mostra il valore del fattore di fusione in modalità GL_EXP nebbia.](images/fog02.png)

<span data-ttu-id="6e0ea-154">L'equazione per GL \_ exp2 Fog è:</span><span class="sxs-lookup"><span data-stu-id="6e0ea-154">The equation for GL\_EXP2 fog is:</span></span>

![Equazione che mostra il valore del fattore di fusione in modalità GL_EXP2 nebbia.](images/fog03.png)

<span data-ttu-id="6e0ea-156">Indipendentemente dalla modalità di nebbia, *f* viene bloccato nell'intervallo \[ 0, 1 dopo il \] calcolo.</span><span class="sxs-lookup"><span data-stu-id="6e0ea-156">Regardless of the fog mode, *f* is clamped to the range \[0,1\] after it is computed.</span></span> <span data-ttu-id="6e0ea-157">Quindi, se OpenGL è in modalità colore RGBA, il colore *C*<sub>r</sub> del frammento viene sostituito da</span><span class="sxs-lookup"><span data-stu-id="6e0ea-157">Then, if OpenGL is in RGBA color mode, the fragment's color *C*<sub>r</sub> is replaced by</span></span>

![Equazione che mostra il colore del frammento offuscato come funzione di combinazione del fattore e del colore nebbia.](images/fog04.png)

<span data-ttu-id="6e0ea-159">In modalità di indice dei colori, l'indice di colore del frammento *i*<sub>r</sub> viene sostituito da</span><span class="sxs-lookup"><span data-stu-id="6e0ea-159">In color-index mode, the fragment's color index *i*<sub>r</sub> is replaced by</span></span>

![Equazione che mostra l'indice dei colori del frammento con offuscamento come funzione del fattore di fusione e del colore indicizzato.](images/fog05.png)

<span data-ttu-id="6e0ea-161">Le funzioni seguenti consentono di recuperare informazioni correlate alle funzioni **glFog** :</span><span class="sxs-lookup"><span data-stu-id="6e0ea-161">The following functions retrieve information related to the **glFog** functions:</span></span>

<span data-ttu-id="6e0ea-162">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento del \_ colore della nebbia GL \_</span><span class="sxs-lookup"><span data-stu-id="6e0ea-162">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_FOG\_COLOR</span></span>

<span data-ttu-id="6e0ea-163">**glGet** con argument GL \_ Fog \_ index</span><span class="sxs-lookup"><span data-stu-id="6e0ea-163">**glGet** with argument GL\_FOG\_INDEX</span></span>

<span data-ttu-id="6e0ea-164">**glGet** con densità di \_ nebbia argomento GL \_</span><span class="sxs-lookup"><span data-stu-id="6e0ea-164">**glGet** with argument GL\_FOG\_DENSITY</span></span>

<span data-ttu-id="6e0ea-165">**glGet** con argument GL \_ Fog \_ Start</span><span class="sxs-lookup"><span data-stu-id="6e0ea-165">**glGet** with argument GL\_FOG\_START</span></span>

<span data-ttu-id="6e0ea-166">**glGet** con argomento di \_ \_ fine nebbia</span><span class="sxs-lookup"><span data-stu-id="6e0ea-166">**glGet** with argument GL\_FOG\_END</span></span>

<span data-ttu-id="6e0ea-167">**glGet** con argomento della \_ modalità di nebbia GL \_</span><span class="sxs-lookup"><span data-stu-id="6e0ea-167">**glGet** with argument GL\_FOG\_MODE</span></span>

<span data-ttu-id="6e0ea-168">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Fog</span><span class="sxs-lookup"><span data-stu-id="6e0ea-168">[**glIsEnabled**](glisenabled.md) with argument GL\_FOG</span></span>

## <a name="requirements"></a><span data-ttu-id="6e0ea-169">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6e0ea-169">Requirements</span></span>



| <span data-ttu-id="6e0ea-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e0ea-170">Requirement</span></span> | <span data-ttu-id="6e0ea-171">Valore</span><span class="sxs-lookup"><span data-stu-id="6e0ea-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e0ea-172">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e0ea-172">Minimum supported client</span></span><br/> | <span data-ttu-id="6e0ea-173">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6e0ea-173">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6e0ea-174">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e0ea-174">Minimum supported server</span></span><br/> | <span data-ttu-id="6e0ea-175">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6e0ea-175">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6e0ea-176">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6e0ea-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e0ea-177"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e0ea-177"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6e0ea-178">Libreria</span><span class="sxs-lookup"><span data-stu-id="6e0ea-178">Library</span></span><br/>                  | <dl> <span data-ttu-id="6e0ea-179"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e0ea-179"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6e0ea-180">DLL</span><span class="sxs-lookup"><span data-stu-id="6e0ea-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e0ea-181"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e0ea-181"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e0ea-182">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6e0ea-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e0ea-183">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="6e0ea-183">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="6e0ea-184">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="6e0ea-184">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="6e0ea-185">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="6e0ea-185">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="6e0ea-186">**Remo**</span><span class="sxs-lookup"><span data-stu-id="6e0ea-186">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="6e0ea-187">**glGet**</span><span class="sxs-lookup"><span data-stu-id="6e0ea-187">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="6e0ea-188">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="6e0ea-188">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





