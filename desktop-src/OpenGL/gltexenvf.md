---
title: funzione glTexEnvf (GL. h)
description: La funzione glTexEnvf imposta un parametro di ambiente di trama.
ms.assetid: 1b203240-a963-4dfe-96bc-735720e16122
keywords:
- funzione glTexEnvf OpenGL
topic_type:
- apiref
api_name:
- glTexEnvf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1566378b6dcd2f91a2e2cd445f0ec39c0f6f6a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741127"
---
# <a name="gltexenvf-function"></a><span data-ttu-id="4ead5-104">glTexEnvf (funzione)</span><span class="sxs-lookup"><span data-stu-id="4ead5-104">glTexEnvf function</span></span>

<span data-ttu-id="4ead5-105">La funzione **glTexEnvf** imposta un parametro di ambiente di trama.</span><span class="sxs-lookup"><span data-stu-id="4ead5-105">The **glTexEnvf** function sets a texture environment parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ead5-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4ead5-106">Syntax</span></span>


```C++
void WINAPI glTexEnvf(
   GLenum  target,
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a><span data-ttu-id="4ead5-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="4ead5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ead5-108">*target*</span><span class="sxs-lookup"><span data-stu-id="4ead5-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="4ead5-109">Ambiente di trama.</span><span class="sxs-lookup"><span data-stu-id="4ead5-109">A texture environment.</span></span> <span data-ttu-id="4ead5-110">Deve essere una \_ trama GL \_ env.</span><span class="sxs-lookup"><span data-stu-id="4ead5-110">Must be GL\_TEXTURE\_ENV.</span></span>

</dd> <dt>

<span data-ttu-id="4ead5-111">*pname*</span><span class="sxs-lookup"><span data-stu-id="4ead5-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="4ead5-112">Nome simbolico di un parametro di ambiente di trama a valore singolo.</span><span class="sxs-lookup"><span data-stu-id="4ead5-112">The symbolic name of a single-valued texture environment parameter.</span></span> <span data-ttu-id="4ead5-113">Deve essere la \_ modalità ENV della trama GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4ead5-113">Must be GL\_TEXTURE\_ENV\_MODE.</span></span>

</dd> <dt>

<span data-ttu-id="4ead5-114">*param*</span><span class="sxs-lookup"><span data-stu-id="4ead5-114">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="4ead5-115">Una singola costante simbolica, una regola GL \_ Modular, GL \_ decal, GL \_ Blend o GL \_ Replace.</span><span class="sxs-lookup"><span data-stu-id="4ead5-115">A single symbolic constant, one of GL\_MODULATE, GL\_DECAL, GL\_BLEND, or GL\_REPLACE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ead5-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4ead5-116">Return value</span></span>

<span data-ttu-id="4ead5-117">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="4ead5-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4ead5-118">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="4ead5-118">Error codes</span></span>

<span data-ttu-id="4ead5-119">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="4ead5-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="4ead5-120">Nome</span><span class="sxs-lookup"><span data-stu-id="4ead5-120">Name</span></span>                                                                                                  | <span data-ttu-id="4ead5-121">Significato</span><span class="sxs-lookup"><span data-stu-id="4ead5-121">Meaning</span></span>                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4ead5-122"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4ead5-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="4ead5-123">*target* o *pname* non è uno dei valori definiti accettati oppure quando *params* deve avere un valore costante definito (in base al valore di *pname*) e no.</span><span class="sxs-lookup"><span data-stu-id="4ead5-123">*target* or *pname* was not one of the accepted defined values, or when *params* should have had a defined constant value (based on the value of *pname*) and did not.</span></span><br/> |
| <dl> <span data-ttu-id="4ead5-124"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4ead5-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="4ead5-125">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="4ead5-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                             |



## <a name="remarks"></a><span data-ttu-id="4ead5-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="4ead5-126">Remarks</span></span>

<span data-ttu-id="4ead5-127">Un ambiente di trama specifica come vengono interpretati i valori di trama quando si crea una trama di un frammento.</span><span class="sxs-lookup"><span data-stu-id="4ead5-127">A texture environment specifies how texture values are interpreted when a fragment is textured.</span></span> <span data-ttu-id="4ead5-128">Il parametro di *destinazione* deve essere un GL \_ texture \_ env.</span><span class="sxs-lookup"><span data-stu-id="4ead5-128">The *target* parameter must be GL\_TEXTURE\_ENV.</span></span> <span data-ttu-id="4ead5-129">Il parametro *pname* è la \_ \_ modalità ENV texture env \_ .</span><span class="sxs-lookup"><span data-stu-id="4ead5-129">The *pname* parameter is GL\_TEXTURE\_ENV\_MODE.</span></span> <span data-ttu-id="4ead5-130">Sono definite tre funzioni di trama, ovvero i \_ modulari GL, GL \_ decal e GL \_ Blend.</span><span class="sxs-lookup"><span data-stu-id="4ead5-130">Three texture functions are defined: GL\_MODULATE, GL\_DECAL, and GL\_BLEND.</span></span>

<span data-ttu-id="4ead5-131">Una funzione di trama agisce sul frammento per creare una trama usando il valore dell'immagine di trama che si applica al frammento (vedere [**glTexParameter**](gltexparameter-functions.md)) e produce un colore RGBA per tale frammento.</span><span class="sxs-lookup"><span data-stu-id="4ead5-131">A texture function acts on the fragment to be textured using the texture image value that applies to the fragment (see [**glTexParameter**](gltexparameter-functions.md)) and produces an RGBA color for that fragment.</span></span> <span data-ttu-id="4ead5-132">La tabella seguente illustra come viene prodotto il colore RGBA per ognuna delle tre funzioni di trama che è possibile scegliere.</span><span class="sxs-lookup"><span data-stu-id="4ead5-132">The following table shows how the RGBA color is produced for each of the three texture functions that can be chosen.</span></span> <span data-ttu-id="4ead5-133">*C* è una tripla di valori di colore (RGB) e *un* è il valore alfa associato.</span><span class="sxs-lookup"><span data-stu-id="4ead5-133">*C* is a triple of color values (RGB) and *A* is the associated alpha value.</span></span> <span data-ttu-id="4ead5-134">I valori RGBA estratti da un'immagine di trama sono compresi nell'intervallo compreso tra \[ 0 e 1 \] .</span><span class="sxs-lookup"><span data-stu-id="4ead5-134">RGBA values extracted from a texture image are in the range \[0, 1\].</span></span> <span data-ttu-id="4ead5-135">Il pedice *f* fa riferimento al frammento in ingresso, ovvero l'indice *t* nell'immagine di trama, il pedice *c* nel colore dell'ambiente di trama e l'indice *v* indica un valore prodotto dalla funzione texture.</span><span class="sxs-lookup"><span data-stu-id="4ead5-135">The subscript *f* refers to the incoming fragment, the subscript *t* to the texture image, the subscript *c* to the texture environment color, and subscript *v* indicates a value produced by the texture function.</span></span>

<span data-ttu-id="4ead5-136">Un'immagine di trama può avere fino a quattro componenti per ogni elemento di trama (vedere [**glTexImage1D**](glteximage1d.md) e [**glTexImage2D**](glteximage2d.md)).</span><span class="sxs-lookup"><span data-stu-id="4ead5-136">A texture image can have up to four components per texture element (see [**glTexImage1D**](glteximage1d.md) and [**glTexImage2D**](glteximage2d.md)).</span></span> <span data-ttu-id="4ead5-137">In un'immagine a un componente, lt indica il singolo componente.</span><span class="sxs-lookup"><span data-stu-id="4ead5-137">In a one-component image, Lt indicates that single component.</span></span> <span data-ttu-id="4ead5-138">Un'immagine A due componenti usa *L?*</span><span class="sxs-lookup"><span data-stu-id="4ead5-138">A two-component image uses *L?*</span></span>  <span data-ttu-id="4ead5-139">e *un?*</span><span class="sxs-lookup"><span data-stu-id="4ead5-139">and *A?*</span></span> <span data-ttu-id="4ead5-140">.</span><span class="sxs-lookup"><span data-stu-id="4ead5-140">.</span></span> <span data-ttu-id="4ead5-141">Un'immagine a tre componenti ha solo un valore di colore, *C?*</span><span class="sxs-lookup"><span data-stu-id="4ead5-141">A three-component image has only a color value, *C?*</span></span> <span data-ttu-id="4ead5-142">.</span><span class="sxs-lookup"><span data-stu-id="4ead5-142">.</span></span> <span data-ttu-id="4ead5-143">Un'immagine a quattro componenti presenta un valore di colore *C?*</span><span class="sxs-lookup"><span data-stu-id="4ead5-143">A four-component image has both a color value *C?*</span></span>  <span data-ttu-id="4ead5-144">e un valore alfa *A?*</span><span class="sxs-lookup"><span data-stu-id="4ead5-144">and an alpha value *A?*</span></span> <span data-ttu-id="4ead5-145">.</span><span class="sxs-lookup"><span data-stu-id="4ead5-145">.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4ead5-146">Numero di componenti</span><span class="sxs-lookup"><span data-stu-id="4ead5-146">Number of components</span></span></th>
<th><span data-ttu-id="4ead5-147">GL_MODULATE</span><span class="sxs-lookup"><span data-stu-id="4ead5-147">GL_MODULATE</span></span></th>
<th><span data-ttu-id="4ead5-148">GL_DECAL</span><span class="sxs-lookup"><span data-stu-id="4ead5-148">GL_DECAL</span></span></th>
<th><span data-ttu-id="4ead5-149">GL_BLEND</span><span class="sxs-lookup"><span data-stu-id="4ead5-149">GL_BLEND</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="4ead5-150">1 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="4ead5-150">1${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="4ead5-151"><em>C<sub>v</sub> </em>  =  <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="4ead5-151"><em>C<sub>v</sub></em> = <em>L?</em></span></span> <span data-ttu-id="4ead5-152"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="4ead5-152"><em>C<sub>f</sub></em></span></span></td>
<td rowspan="2"><span data-ttu-id="4ead5-153">$ {REMOVE} $ non definito</span><span class="sxs-lookup"><span data-stu-id="4ead5-153">undefined${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="4ead5-154"><em>C</em> <em><sub>v</sub></em>  =  <em>(1</em> - <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="4ead5-154"><em>C</em> <em><sub>v</sub></em> = <em>(1</em> - <em>L?</em></span></span> <span data-ttu-id="4ead5-155"><em>) C<sub>f</sub> </em> + <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="4ead5-155"><em>)C<sub>f</sub></em> + <em>L?</em></span></span> <span data-ttu-id="4ead5-156"><em>C<sub>c</sub></em></span><span class="sxs-lookup"><span data-stu-id="4ead5-156"><em>C<sub>c</sub></em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ead5-157"><em><sub>V</sub> </em>  =  <em><sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="4ead5-157"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="4ead5-158"><em><sub>V</sub> </em>  =  <em><sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="4ead5-158"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="4ead5-159">2 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="4ead5-159">2${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="4ead5-160"><em>C<sub>v</sub> </em>  =  <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="4ead5-160"><em>C<sub>v</sub></em> = <em>L?</em></span></span> <span data-ttu-id="4ead5-161"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="4ead5-161"><em>C<sub>f</sub></em></span></span></td>
<td rowspan="2"><span data-ttu-id="4ead5-162">$ {REMOVE} $ non definito</span><span class="sxs-lookup"><span data-stu-id="4ead5-162">undefined${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="4ead5-163"><em>C<sub>v</sub> </em>  =  <em>(1</em> - <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="4ead5-163"><em>C<sub>v</sub></em> = <em>(1</em> - <em>L?</em></span></span> <span data-ttu-id="4ead5-164"><em>) C<sub>f</sub> </em> + <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="4ead5-164"><em>)C<sub>f</sub></em> + <em>L?</em></span></span> <span data-ttu-id="4ead5-165"><em>C<sub>c</sub></em></span><span class="sxs-lookup"><span data-stu-id="4ead5-165"><em>C<sub>c</sub></em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ead5-166"><em><sub>V</sub> </em>  =  <em><sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="4ead5-166"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="4ead5-167"><em><sub>V</sub> </em>  =  <em><sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="4ead5-167"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="4ead5-168">3 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="4ead5-168">3${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="4ead5-169"><em>C<sub>v</sub> </em>  =  <em>C?</em></span><span class="sxs-lookup"><span data-stu-id="4ead5-169"><em>C<sub>v</sub></em> = <em>C?</em></span></span> <span data-ttu-id="4ead5-170"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="4ead5-170"><em>C<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="4ead5-171"><em>C<sub>v</sub> </em>  =  <em>C?</em></span><span class="sxs-lookup"><span data-stu-id="4ead5-171"><em>C<sub>v</sub></em> = <em>C?</em></span></span></td>
<td rowspan="2"><span data-ttu-id="4ead5-172">$ {REMOVE} $ non definito</span><span class="sxs-lookup"><span data-stu-id="4ead5-172">undefined${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ead5-173"><em><sub>V</sub> </em>  =  <em><sub>F</sub> </em> </span><span class="sxs-lookup"><span data-stu-id="4ead5-173"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em> </span></span></td>
<td><span data-ttu-id="4ead5-174"><em><sub>V</sub> </em>  =  <em><sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="4ead5-174"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="4ead5-175">4 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="4ead5-175">4${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="4ead5-176"><em>C<sub>v</sub> </em>  =  <em>C?</em></span><span class="sxs-lookup"><span data-stu-id="4ead5-176"><em>C<sub>v</sub></em> = <em>C?</em></span></span> <span data-ttu-id="4ead5-177"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="4ead5-177"><em>C<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="4ead5-178"><em>C<sub>v</sub> </em> = (1- <em>A?</em></span><span class="sxs-lookup"><span data-stu-id="4ead5-178"><em>C<sub>v</sub></em> = (1 - <em>A?</em></span></span> <span data-ttu-id="4ead5-179"><em>) C<sub>f</sub> </em> + <em>A?</em></span><span class="sxs-lookup"><span data-stu-id="4ead5-179"><em>)C<sub>f</sub></em> + <em>A?</em></span></span> <span data-ttu-id="4ead5-180"><em>C?</em></span><span class="sxs-lookup"><span data-stu-id="4ead5-180"><em>C?</em></span></span></td>
<td rowspan="2"><span data-ttu-id="4ead5-181">$ {REMOVE} $ non definito</span><span class="sxs-lookup"><span data-stu-id="4ead5-181">undefined${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ead5-182"><em><sub>V</sub> </em>  =  <em>A?</em></span><span class="sxs-lookup"><span data-stu-id="4ead5-182"><em>A<sub>v</sub></em> = <em>A?</em></span></span> <span data-ttu-id="4ead5-183"><em><sub>F</sub></em> </span><span class="sxs-lookup"><span data-stu-id="4ead5-183"><em>A<sub>f</sub></em> </span></span></td>
<td><span data-ttu-id="4ead5-184"><em><sub>V</sub> </em>  =  <em><sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="4ead5-184"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="4ead5-185">\_ \_ Per impostazione predefinita, la modalità ENV della trama GL viene \_ \_ modulata.</span><span class="sxs-lookup"><span data-stu-id="4ead5-185">GL\_TEXTURE\_ENV\_MODE defaults to GL\_MODULATE.</span></span>

<span data-ttu-id="4ead5-186">La funzione seguente recupera le informazioni correlate a **glTexEnvf**:</span><span class="sxs-lookup"><span data-stu-id="4ead5-186">The following function retrieves information related to **glTexEnvf**:</span></span>

[<span data-ttu-id="4ead5-187">**glTexGetEnvfv**</span><span class="sxs-lookup"><span data-stu-id="4ead5-187">**glTexGetEnvfv**</span></span>](glgettexenvfv.md)

## <a name="requirements"></a><span data-ttu-id="4ead5-188">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ead5-188">Requirements</span></span>



| <span data-ttu-id="4ead5-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ead5-189">Requirement</span></span> | <span data-ttu-id="4ead5-190">Valore</span><span class="sxs-lookup"><span data-stu-id="4ead5-190">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ead5-191">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ead5-191">Minimum supported client</span></span><br/> | <span data-ttu-id="4ead5-192">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4ead5-192">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4ead5-193">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ead5-193">Minimum supported server</span></span><br/> | <span data-ttu-id="4ead5-194">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4ead5-194">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4ead5-195">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4ead5-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ead5-196"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ead5-196"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="4ead5-197">Libreria</span><span class="sxs-lookup"><span data-stu-id="4ead5-197">Library</span></span><br/>                  | <dl> <span data-ttu-id="4ead5-198"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4ead5-198"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4ead5-199">DLL</span><span class="sxs-lookup"><span data-stu-id="4ead5-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ead5-200"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ead5-200"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ead5-201">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4ead5-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ead5-202">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="4ead5-202">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="4ead5-203">**Remo**</span><span class="sxs-lookup"><span data-stu-id="4ead5-203">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="4ead5-204">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="4ead5-204">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="4ead5-205">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="4ead5-205">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="4ead5-206">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="4ead5-206">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





