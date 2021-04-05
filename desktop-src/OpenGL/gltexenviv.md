---
title: funzione glTexEnviv (GL. h)
description: La funzione glTexEnviv imposta un parametro di ambiente di trama.
ms.assetid: e98ce736-cc68-4687-8c1b-6b0fef7a677a
keywords:
- funzione glTexEnviv OpenGL
topic_type:
- apiref
api_name:
- glTexEnviv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5ec232f559e8d4af10369ebe98dd0aea71e36b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874617"
---
# <a name="gltexenviv-function"></a><span data-ttu-id="12d20-104">glTexEnviv (funzione)</span><span class="sxs-lookup"><span data-stu-id="12d20-104">glTexEnviv function</span></span>

<span data-ttu-id="12d20-105">La funzione **glTexEnviv** imposta un parametro di ambiente di trama.</span><span class="sxs-lookup"><span data-stu-id="12d20-105">The **glTexEnviv** function sets a texture environment parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="12d20-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="12d20-106">Syntax</span></span>


```C++
void WINAPI glTexEnviv(
         GLenum target,
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="12d20-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="12d20-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12d20-108">*target*</span><span class="sxs-lookup"><span data-stu-id="12d20-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="12d20-109">Ambiente di trama.</span><span class="sxs-lookup"><span data-stu-id="12d20-109">A texture environment.</span></span> <span data-ttu-id="12d20-110">Deve essere una \_ trama GL \_ env.</span><span class="sxs-lookup"><span data-stu-id="12d20-110">Must be GL\_TEXTURE\_ENV.</span></span>

</dd> <dt>

<span data-ttu-id="12d20-111">*pname*</span><span class="sxs-lookup"><span data-stu-id="12d20-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="12d20-112">Nome simbolico di un parametro di ambiente di trama a valore singolo.</span><span class="sxs-lookup"><span data-stu-id="12d20-112">The symbolic name of a single-valued texture environment parameter.</span></span> <span data-ttu-id="12d20-113">I valori accettati sono GL \_ texture \_ env \_ mode e GL \_ texture \_ env \_ Color.</span><span class="sxs-lookup"><span data-stu-id="12d20-113">Accepted values are GL\_TEXTURE\_ENV\_MODE and GL\_TEXTURE\_ENV\_COLOR.</span></span>

</dd> <dt>

<span data-ttu-id="12d20-114">*params*</span><span class="sxs-lookup"><span data-stu-id="12d20-114">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="12d20-115">Puntatore a una matrice di parametri, ovvero una singola costante simbolica o un colore RGBA.</span><span class="sxs-lookup"><span data-stu-id="12d20-115">A pointer to an array of parameters: either a single symbolic constant or an RGBA color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12d20-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="12d20-116">Return value</span></span>

<span data-ttu-id="12d20-117">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="12d20-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="12d20-118">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="12d20-118">Error codes</span></span>

<span data-ttu-id="12d20-119">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="12d20-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="12d20-120">Nome</span><span class="sxs-lookup"><span data-stu-id="12d20-120">Name</span></span>                                                                                                  | <span data-ttu-id="12d20-121">Significato</span><span class="sxs-lookup"><span data-stu-id="12d20-121">Meaning</span></span>                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="12d20-122"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="12d20-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="12d20-123">*target* o *pname* non è uno dei valori definiti accettati oppure quando *params* deve avere un valore costante definito (in base al valore di *pname*) e no.</span><span class="sxs-lookup"><span data-stu-id="12d20-123">*target* or *pname* was not one of the accepted defined values, or when *params* should have had a defined constant value (based on the value of *pname*) and did not.</span></span><br/> |
| <dl> <span data-ttu-id="12d20-124"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="12d20-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="12d20-125">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="12d20-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                             |



## <a name="remarks"></a><span data-ttu-id="12d20-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="12d20-126">Remarks</span></span>

<span data-ttu-id="12d20-127">Un ambiente di trama specifica come vengono interpretati i valori di trama quando si crea una trama di un frammento.</span><span class="sxs-lookup"><span data-stu-id="12d20-127">A texture environment specifies how texture values are interpreted when a fragment is textured.</span></span> <span data-ttu-id="12d20-128">Il parametro di *destinazione* deve essere un GL \_ texture \_ env.</span><span class="sxs-lookup"><span data-stu-id="12d20-128">The *target* parameter must be GL\_TEXTURE\_ENV.</span></span> <span data-ttu-id="12d20-129">Il parametro *pname* può essere la \_ modalità ENV della trama GL o il colore dell'ENV della \_ \_ trama GL \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="12d20-129">The *pname* parameter can be either GL\_TEXTURE\_ENV\_MODE or GL\_TEXTURE\_ENV\_COLOR.</span></span>

<span data-ttu-id="12d20-130">Se *pname* è \_ \_ \_ la modalità ENV della trama GL, *params* è (o punta a) il nome simbolico di una funzione texture.</span><span class="sxs-lookup"><span data-stu-id="12d20-130">If *pname* is GL\_TEXTURE\_ENV\_MODE, then *params* is (or points to) the symbolic name of a texture function.</span></span> <span data-ttu-id="12d20-131">Sono definite tre funzioni di trama, ovvero i \_ modulari GL, GL \_ decal e GL \_ Blend.</span><span class="sxs-lookup"><span data-stu-id="12d20-131">Three texture functions are defined: GL\_MODULATE, GL\_DECAL, and GL\_BLEND.</span></span>

<span data-ttu-id="12d20-132">Una funzione di trama agisce sul frammento per creare una trama usando il valore dell'immagine di trama che si applica al frammento (vedere [**glTexParameter**](gltexparameter-functions.md)) e produce un colore RGBA per tale frammento.</span><span class="sxs-lookup"><span data-stu-id="12d20-132">A texture function acts on the fragment to be textured using the texture image value that applies to the fragment (see [**glTexParameter**](gltexparameter-functions.md)) and produces an RGBA color for that fragment.</span></span> <span data-ttu-id="12d20-133">La tabella seguente illustra come viene prodotto il colore RGBA per ognuna delle tre funzioni di trama che è possibile scegliere.</span><span class="sxs-lookup"><span data-stu-id="12d20-133">The following table shows how the RGBA color is produced for each of the three texture functions that can be chosen.</span></span> <span data-ttu-id="12d20-134">*C* è una tripla di valori di colore (RGB) e *un* è il valore alfa associato.</span><span class="sxs-lookup"><span data-stu-id="12d20-134">*C* is a triple of color values (RGB) and *A* is the associated alpha value.</span></span> <span data-ttu-id="12d20-135">I valori RGBA estratti da un'immagine di trama sono compresi nell'intervallo compreso tra \[ 0 e 1 \] .</span><span class="sxs-lookup"><span data-stu-id="12d20-135">RGBA values extracted from a texture image are in the range \[0, 1\].</span></span> <span data-ttu-id="12d20-136">Il pedice *f* fa riferimento al frammento in ingresso, ovvero l'indice *t* nell'immagine di trama, il pedice *c* nel colore dell'ambiente di trama e l'indice *v* indica un valore prodotto dalla funzione texture.</span><span class="sxs-lookup"><span data-stu-id="12d20-136">The subscript *f* refers to the incoming fragment, the subscript *t* to the texture image, the subscript *c* to the texture environment color, and subscript *v* indicates a value produced by the texture function.</span></span>

<span data-ttu-id="12d20-137">Un'immagine di trama può avere fino a quattro componenti per ogni elemento di trama (vedere [**glTexImage1D**](glteximage1d.md) e [**glTexImage2D**](glteximage2d.md)).</span><span class="sxs-lookup"><span data-stu-id="12d20-137">A texture image can have up to four components per texture element (see [**glTexImage1D**](glteximage1d.md) and [**glTexImage2D**](glteximage2d.md)).</span></span> <span data-ttu-id="12d20-138">In un'immagine a un componente, lt indica il singolo componente.</span><span class="sxs-lookup"><span data-stu-id="12d20-138">In a one-component image, Lt indicates that single component.</span></span> <span data-ttu-id="12d20-139">Un'immagine A due componenti usa *L?*</span><span class="sxs-lookup"><span data-stu-id="12d20-139">A two-component image uses *L?*</span></span>  <span data-ttu-id="12d20-140">e *un?*</span><span class="sxs-lookup"><span data-stu-id="12d20-140">and *A?*</span></span> <span data-ttu-id="12d20-141">.</span><span class="sxs-lookup"><span data-stu-id="12d20-141">.</span></span> <span data-ttu-id="12d20-142">Un'immagine a tre componenti ha solo un valore di colore, *C?*</span><span class="sxs-lookup"><span data-stu-id="12d20-142">A three-component image has only a color value, *C?*</span></span> <span data-ttu-id="12d20-143">.</span><span class="sxs-lookup"><span data-stu-id="12d20-143">.</span></span> <span data-ttu-id="12d20-144">Un'immagine a quattro componenti presenta un valore di colore *C?*</span><span class="sxs-lookup"><span data-stu-id="12d20-144">A four-component image has both a color value *C?*</span></span>  <span data-ttu-id="12d20-145">e un valore alfa *A?*</span><span class="sxs-lookup"><span data-stu-id="12d20-145">and an alpha value *A?*</span></span> <span data-ttu-id="12d20-146">.</span><span class="sxs-lookup"><span data-stu-id="12d20-146">.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="12d20-147">Numero di componenti</span><span class="sxs-lookup"><span data-stu-id="12d20-147">Number of components</span></span></th>
<th><span data-ttu-id="12d20-148">GL_MODULATE</span><span class="sxs-lookup"><span data-stu-id="12d20-148">GL_MODULATE</span></span></th>
<th><span data-ttu-id="12d20-149">GL_DECAL</span><span class="sxs-lookup"><span data-stu-id="12d20-149">GL_DECAL</span></span></th>
<th><span data-ttu-id="12d20-150">GL_BLEND</span><span class="sxs-lookup"><span data-stu-id="12d20-150">GL_BLEND</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="12d20-151">1 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="12d20-151">1${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="12d20-152"><em>C<sub>v</sub> </em>   =  <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="12d20-152"><em>C<sub>v</sub></em>  = <em>L?</em></span></span> <span data-ttu-id="12d20-153"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="12d20-153"><em>C<sub>f</sub></em></span></span></td>
<td rowspan="2"><span data-ttu-id="12d20-154">$ {REMOVE} $ non definito</span><span class="sxs-lookup"><span data-stu-id="12d20-154">undefined${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="12d20-155"><em>C<sub>v</sub> </em>   =  <em>(1</em> - <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="12d20-155"><em>C<sub>v</sub></em>  = <em>(1</em> - <em>L?</em></span></span> <span data-ttu-id="12d20-156"><em>) C<sub>f</sub> </em> + <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="12d20-156"><em>)C<sub>f</sub></em> + <em>L?</em></span></span> <span data-ttu-id="12d20-157"><em>C<sub>c</sub></em></span><span class="sxs-lookup"><span data-stu-id="12d20-157"><em>C<sub>c</sub></em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12d20-158"><em><sub>V</sub> </em>   =  <em><sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="12d20-158"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="12d20-159"><em><sub>V</sub> </em>   =  <em><sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="12d20-159"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="12d20-160">2 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="12d20-160">2${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="12d20-161"><em>C<sub>v</sub> </em>   =  <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="12d20-161"><em>C<sub>v</sub></em>  = <em>L?</em></span></span> <span data-ttu-id="12d20-162"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="12d20-162"><em>C<sub>f</sub></em></span></span></td>
<td rowspan="2"><span data-ttu-id="12d20-163">$ {REMOVE} $ non definito</span><span class="sxs-lookup"><span data-stu-id="12d20-163">undefined${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="12d20-164"><em>C<sub>v</sub> </em>   =  <em>(1</em> - <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="12d20-164"><em>C<sub>v</sub></em>  = <em>(1</em> - <em>L?</em></span></span> <span data-ttu-id="12d20-165"><em>) C<sub>f</sub> </em> + <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="12d20-165"><em>)C<sub>f</sub></em> + <em>L?</em></span></span> <span data-ttu-id="12d20-166"><em>C<sub>c</sub></em></span><span class="sxs-lookup"><span data-stu-id="12d20-166"><em>C<sub>c</sub></em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12d20-167"><em><sub>V</sub> </em>   =  <em><sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="12d20-167"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="12d20-168"><em><sub>V</sub> </em>   =  <em><sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="12d20-168"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="12d20-169">3 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="12d20-169">3${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="12d20-170"><em>C<sub>v</sub> </em>   =  <em>C?</em></span><span class="sxs-lookup"><span data-stu-id="12d20-170"><em>C<sub>v</sub></em>  = <em>C?</em></span></span> <span data-ttu-id="12d20-171"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="12d20-171"><em>C<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="12d20-172"><em>C<sub>v</sub> </em>   =  <em>C?</em></span><span class="sxs-lookup"><span data-stu-id="12d20-172"><em>C<sub>v</sub></em>  = <em>C?</em></span></span></td>
<td rowspan="2"><span data-ttu-id="12d20-173">$ {REMOVE} $ non definito</span><span class="sxs-lookup"><span data-stu-id="12d20-173">undefined${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="12d20-174"><em><sub>V</sub> </em>   =  <em><sub>F</sub> </em> </span><span class="sxs-lookup"><span data-stu-id="12d20-174"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em> </span></span></td>
<td><span data-ttu-id="12d20-175"><em><sub>V</sub> </em>   =  <em><sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="12d20-175"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="12d20-176">4 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="12d20-176">4${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="12d20-177"><em>C<sub>v</sub> </em>   =  <em>C?</em></span><span class="sxs-lookup"><span data-stu-id="12d20-177"><em>C<sub>v</sub></em>  = <em>C?</em></span></span> <span data-ttu-id="12d20-178"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="12d20-178"><em>C<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="12d20-179"><em>C<sub>v</sub> </em> = (1- <em>A?</em></span><span class="sxs-lookup"><span data-stu-id="12d20-179"><em>C<sub>v</sub></em>  = (1 - <em>A?</em></span></span> <span data-ttu-id="12d20-180"><em>) C<sub>f</sub> </em> + <em>A?</em></span><span class="sxs-lookup"><span data-stu-id="12d20-180"><em>)C<sub>f</sub></em> + <em>A?</em></span></span> <span data-ttu-id="12d20-181"><em>C?</em></span><span class="sxs-lookup"><span data-stu-id="12d20-181"><em>C?</em></span></span></td>
<td rowspan="2"><span data-ttu-id="12d20-182">$ {REMOVE} $ non definito</span><span class="sxs-lookup"><span data-stu-id="12d20-182">undefined${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="12d20-183"><em><sub>V</sub> </em>   =  <em>A?</em></span><span class="sxs-lookup"><span data-stu-id="12d20-183"><em>A<sub>v</sub></em>  = <em>A?</em></span></span> <span data-ttu-id="12d20-184"><em><sub>F</sub></em> </span><span class="sxs-lookup"><span data-stu-id="12d20-184"><em>A<sub>f</sub></em> </span></span></td>
<td><span data-ttu-id="12d20-185"><em><sub>V</sub> </em>   =  <em><sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="12d20-185"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="12d20-186">Se pname è \_ \_ \_ il colore dell'ENV texture GL, *params* è un puntatore a una matrice che include un colore RGBA costituito da quattro valori.</span><span class="sxs-lookup"><span data-stu-id="12d20-186">If pname is GL\_TEXTURE\_ENV\_COLOR, *params* is a pointer to an array that holds an RGBA color consisting of four values.</span></span> <span data-ttu-id="12d20-187">I componenti dei colori integer vengono interpretati in modo lineare, in modo che il numero intero positivo sia mappato a 1,0 e l'intero più negativo sia mappato a-1,0.</span><span class="sxs-lookup"><span data-stu-id="12d20-187">Integer color components are interpreted linearly such that the most positive integer maps to 1.0, and the most negative integer maps to -1.0.</span></span> <span data-ttu-id="12d20-188">I valori vengono fissati nell'intervallo compreso tra \[ 0 e 1 \] quando vengono specificati.</span><span class="sxs-lookup"><span data-stu-id="12d20-188">The values are clamped to the range \[0, 1\] when they are specified.</span></span> <span data-ttu-id="12d20-189">*C <sub>c</sub>* accetta questi quattro valori.</span><span class="sxs-lookup"><span data-stu-id="12d20-189">*C<sub>c</sub>* takes these four values.</span></span>

<span data-ttu-id="12d20-190">Per \_ impostazione predefinita, la modalità ENV della trama GL viene \_ \_ impostata su GL \_ modulari e le \_ \_ \_ impostazioni predefinite del colore ENV</span><span class="sxs-lookup"><span data-stu-id="12d20-190">GL\_TEXTURE\_ENV\_MODE defaults to GL\_MODULATE and GL\_TEXTURE\_ENV\_COLOR defaults to (0, 0, 0, 0).</span></span>

<span data-ttu-id="12d20-191">La funzione seguente recupera le informazioni correlate a **glTexEnviv**:</span><span class="sxs-lookup"><span data-stu-id="12d20-191">The following function retrieves information related to **glTexEnviv**:</span></span>

[<span data-ttu-id="12d20-192">**glTexGetEnviv**</span><span class="sxs-lookup"><span data-stu-id="12d20-192">**glTexGetEnviv**</span></span>](glgettexenviv.md)

## <a name="requirements"></a><span data-ttu-id="12d20-193">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12d20-193">Requirements</span></span>



| <span data-ttu-id="12d20-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="12d20-194">Requirement</span></span> | <span data-ttu-id="12d20-195">Valore</span><span class="sxs-lookup"><span data-stu-id="12d20-195">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12d20-196">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12d20-196">Minimum supported client</span></span><br/> | <span data-ttu-id="12d20-197">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="12d20-197">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="12d20-198">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12d20-198">Minimum supported server</span></span><br/> | <span data-ttu-id="12d20-199">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="12d20-199">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="12d20-200">Intestazione</span><span class="sxs-lookup"><span data-stu-id="12d20-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="12d20-201"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="12d20-201"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="12d20-202">Libreria</span><span class="sxs-lookup"><span data-stu-id="12d20-202">Library</span></span><br/>                  | <dl> <span data-ttu-id="12d20-203"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="12d20-203"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="12d20-204">DLL</span><span class="sxs-lookup"><span data-stu-id="12d20-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12d20-205"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12d20-205"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12d20-206">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="12d20-206">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12d20-207">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="12d20-207">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="12d20-208">**Remo**</span><span class="sxs-lookup"><span data-stu-id="12d20-208">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="12d20-209">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="12d20-209">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="12d20-210">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="12d20-210">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="12d20-211">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="12d20-211">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





