---
title: funzione glTexEnvfv (GL. h)
description: La funzione glTexEnvfv imposta un parametro di ambiente di trama.
ms.assetid: 7b8e65aa-1b5c-47ab-8d6c-df14c90075a8
keywords:
- funzione glTexEnvfv OpenGL
topic_type:
- apiref
api_name:
- glTexEnvfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52a2b74025deee08d2d895af0012e85e19ac269b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302756"
---
# <a name="gltexenvfv-function"></a><span data-ttu-id="ba6dc-104">glTexEnvfv (funzione)</span><span class="sxs-lookup"><span data-stu-id="ba6dc-104">glTexEnvfv function</span></span>

<span data-ttu-id="ba6dc-105">La funzione **glTexEnvfv** imposta un parametro di ambiente di trama.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-105">The **glTexEnvfv** function sets a texture environment parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba6dc-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ba6dc-106">Syntax</span></span>


```C++
void WINAPI glTexEnvfv(
         GLenum  target,
         GLenum  pname,
   const GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="ba6dc-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ba6dc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba6dc-108">*target*</span><span class="sxs-lookup"><span data-stu-id="ba6dc-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="ba6dc-109">Ambiente di trama.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-109">A texture environment.</span></span> <span data-ttu-id="ba6dc-110">Deve essere una \_ trama GL \_ env.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-110">Must be GL\_TEXTURE\_ENV.</span></span>

</dd> <dt>

<span data-ttu-id="ba6dc-111">*pname*</span><span class="sxs-lookup"><span data-stu-id="ba6dc-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="ba6dc-112">Nome simbolico di un parametro di ambiente di trama a valore singolo.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-112">The symbolic name of a single-valued texture environment parameter.</span></span> <span data-ttu-id="ba6dc-113">I valori accettati sono GL \_ texture \_ env \_ mode e GL \_ texture \_ env \_ Color.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-113">Accepted values are GL\_TEXTURE\_ENV\_MODE and GL\_TEXTURE\_ENV\_COLOR.</span></span>

</dd> <dt>

<span data-ttu-id="ba6dc-114">*params*</span><span class="sxs-lookup"><span data-stu-id="ba6dc-114">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="ba6dc-115">Puntatore a una matrice di parametri, ovvero una singola costante simbolica o un colore RGBA.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-115">A pointer to an array of parameters: either a single symbolic constant or an RGBA color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba6dc-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ba6dc-116">Return value</span></span>

<span data-ttu-id="ba6dc-117">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ba6dc-118">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="ba6dc-118">Error codes</span></span>

<span data-ttu-id="ba6dc-119">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="ba6dc-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="ba6dc-120">Nome</span><span class="sxs-lookup"><span data-stu-id="ba6dc-120">Name</span></span>                                                                                                  | <span data-ttu-id="ba6dc-121">Significato</span><span class="sxs-lookup"><span data-stu-id="ba6dc-121">Meaning</span></span>                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ba6dc-122"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ba6dc-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="ba6dc-123">*target* o *pname* non è uno dei valori definiti accettati oppure quando *params* deve avere un valore costante definito (in base al valore di *pname*) e no.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-123">*target* or *pname* was not one of the accepted defined values, or when *params* should have had a defined constant value (based on the value of *pname*) and did not.</span></span><br/> |
| <dl> <span data-ttu-id="ba6dc-124"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ba6dc-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="ba6dc-125">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="ba6dc-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                             |



## <a name="remarks"></a><span data-ttu-id="ba6dc-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="ba6dc-126">Remarks</span></span>

<span data-ttu-id="ba6dc-127">Un ambiente di trama specifica come vengono interpretati i valori di trama quando si crea una trama di un frammento.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-127">A texture environment specifies how texture values are interpreted when a fragment is textured.</span></span> <span data-ttu-id="ba6dc-128">Il parametro di *destinazione* deve essere un GL \_ texture \_ env.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-128">The *target* parameter must be GL\_TEXTURE\_ENV.</span></span> <span data-ttu-id="ba6dc-129">Il parametro *pname* può essere la \_ modalità ENV della trama GL o il colore dell'ENV della \_ \_ trama GL \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ba6dc-129">The *pname* parameter can be either GL\_TEXTURE\_ENV\_MODE or GL\_TEXTURE\_ENV\_COLOR.</span></span>

<span data-ttu-id="ba6dc-130">Se *pname* è \_ \_ \_ la modalità ENV della trama GL, *params* è (o punta a) il nome simbolico di una funzione texture.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-130">If *pname* is GL\_TEXTURE\_ENV\_MODE, then *params* is (or points to) the symbolic name of a texture function.</span></span> <span data-ttu-id="ba6dc-131">Sono definite tre funzioni di trama, ovvero i \_ modulari GL, GL \_ decal e GL \_ Blend.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-131">Three texture functions are defined: GL\_MODULATE, GL\_DECAL, and GL\_BLEND.</span></span>

<span data-ttu-id="ba6dc-132">Una funzione di trama agisce sul frammento per creare una trama usando il valore dell'immagine di trama che si applica al frammento (vedere [**glTexParameter**](gltexparameter-functions.md)) e produce un colore RGBA per tale frammento.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-132">A texture function acts on the fragment to be textured using the texture image value that applies to the fragment (see [**glTexParameter**](gltexparameter-functions.md)) and produces an RGBA color for that fragment.</span></span> <span data-ttu-id="ba6dc-133">La tabella seguente illustra come viene prodotto il colore RGBA per ognuna delle tre funzioni di trama che è possibile scegliere.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-133">The following table shows how the RGBA color is produced for each of the three texture functions that can be chosen.</span></span> <span data-ttu-id="ba6dc-134">*C* è una tripla di valori di colore (RGB) e *un* è il valore alfa associato.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-134">*C* is a triple of color values (RGB) and *A* is the associated alpha value.</span></span> <span data-ttu-id="ba6dc-135">I valori RGBA estratti da un'immagine di trama sono compresi nell'intervallo compreso tra \[ 0 e 1 \] .</span><span class="sxs-lookup"><span data-stu-id="ba6dc-135">RGBA values extracted from a texture image are in the range \[0, 1\].</span></span> <span data-ttu-id="ba6dc-136">Il pedice *f* fa riferimento al frammento in ingresso, ovvero l'indice *t* nell'immagine di trama, il pedice *c* nel colore dell'ambiente di trama e l'indice *v* indica un valore prodotto dalla funzione texture.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-136">The subscript *f* refers to the incoming fragment, the subscript *t* to the texture image, the subscript *c* to the texture environment color, and subscript *v* indicates a value produced by the texture function.</span></span>

<span data-ttu-id="ba6dc-137">Un'immagine di trama può avere fino a quattro componenti per ogni elemento di trama (vedere [**glTexImage1D**](glteximage1d.md) e [**glTexImage2D**](glteximage2d.md)).</span><span class="sxs-lookup"><span data-stu-id="ba6dc-137">A texture image can have up to four components per texture element (see [**glTexImage1D**](glteximage1d.md) and [**glTexImage2D**](glteximage2d.md)).</span></span> <span data-ttu-id="ba6dc-138">In un'immagine a un componente, lt indica il singolo componente.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-138">In a one-component image, Lt indicates that single component.</span></span> <span data-ttu-id="ba6dc-139">Un'immagine A due componenti usa *L?*</span><span class="sxs-lookup"><span data-stu-id="ba6dc-139">A two-component image uses *L?*</span></span>  <span data-ttu-id="ba6dc-140">e *un?*</span><span class="sxs-lookup"><span data-stu-id="ba6dc-140">and *A?*</span></span> <span data-ttu-id="ba6dc-141">.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-141">.</span></span> <span data-ttu-id="ba6dc-142">Un'immagine a tre componenti ha solo un valore di colore, *C?*</span><span class="sxs-lookup"><span data-stu-id="ba6dc-142">A three-component image has only a color value, *C?*</span></span> <span data-ttu-id="ba6dc-143">.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-143">.</span></span> <span data-ttu-id="ba6dc-144">Un'immagine a quattro componenti presenta un valore di colore *C?*</span><span class="sxs-lookup"><span data-stu-id="ba6dc-144">A four-component image has both a color value *C?*</span></span>  <span data-ttu-id="ba6dc-145">e un valore alfa *A?*</span><span class="sxs-lookup"><span data-stu-id="ba6dc-145">and an alpha value *A?*</span></span> <span data-ttu-id="ba6dc-146">.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-146">.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ba6dc-147">Numero di componenti</span><span class="sxs-lookup"><span data-stu-id="ba6dc-147">Number of components</span></span></th>
<th><span data-ttu-id="ba6dc-148">GL_MODULATE</span><span class="sxs-lookup"><span data-stu-id="ba6dc-148">GL_MODULATE</span></span></th>
<th><span data-ttu-id="ba6dc-149">GL_DECAL</span><span class="sxs-lookup"><span data-stu-id="ba6dc-149">GL_DECAL</span></span></th>
<th><span data-ttu-id="ba6dc-150">GL_BLEND</span><span class="sxs-lookup"><span data-stu-id="ba6dc-150">GL_BLEND</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="ba6dc-151">1 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="ba6dc-151">1${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="ba6dc-152"><em>C<sub>v</sub> </em>  =  <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="ba6dc-152"><em>C<sub>v</sub></em> = <em>L?</em></span></span> <span data-ttu-id="ba6dc-153"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="ba6dc-153"><em>C<sub>f</sub></em></span></span></td>
<td rowspan="2"><span data-ttu-id="ba6dc-154">$ {REMOVE} $ non definito</span><span class="sxs-lookup"><span data-stu-id="ba6dc-154">undefined${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="ba6dc-155"><em>C<sub>v</sub> </em>  =  <em>(1</em> - <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="ba6dc-155"><em>C<sub>v</sub></em> = <em>(1</em> - <em>L?</em></span></span> <span data-ttu-id="ba6dc-156"><em>) C<sub>f</sub> </em> + <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="ba6dc-156"><em>)C<sub>f</sub></em> + <em>L?</em></span></span> <span data-ttu-id="ba6dc-157"><em>C<sub>c</sub></em></span><span class="sxs-lookup"><span data-stu-id="ba6dc-157"><em>C<sub>c</sub></em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba6dc-158"><em><sub>V</sub> </em>  =  <em><sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="ba6dc-158"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="ba6dc-159"><em><sub>V</sub> </em>  =  <em><sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="ba6dc-159"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="ba6dc-160">2 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="ba6dc-160">2${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="ba6dc-161"><em>C<sub>v</sub> </em>  =  <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="ba6dc-161"><em>C<sub>v</sub></em> = <em>L?</em></span></span> <span data-ttu-id="ba6dc-162"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="ba6dc-162"><em>C<sub>f</sub></em></span></span></td>
<td rowspan="2"><span data-ttu-id="ba6dc-163">$ {REMOVE} $ non definito</span><span class="sxs-lookup"><span data-stu-id="ba6dc-163">undefined${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="ba6dc-164"><em>C<sub>v</sub> </em>  =  <em>(1</em> - <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="ba6dc-164"><em>C<sub>v</sub></em> = <em>(1</em> - <em>L?</em></span></span> <span data-ttu-id="ba6dc-165"><em>) C<sub>f</sub> </em> + <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="ba6dc-165"><em>)C<sub>f</sub></em> + <em>L?</em></span></span> <span data-ttu-id="ba6dc-166"><em>C<sub>c</sub></em></span><span class="sxs-lookup"><span data-stu-id="ba6dc-166"><em>C<sub>c</sub></em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba6dc-167"><em></em> <em><sub>V</sub></em>   =  <em>a<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="ba6dc-167"><em>A</em> <em><sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="ba6dc-168"><em><sub>V</sub> </em>  =  <em><sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="ba6dc-168"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="ba6dc-169">3 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="ba6dc-169">3${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="ba6dc-170"><em>C<sub>v</sub> </em>  =  <em>C?</em></span><span class="sxs-lookup"><span data-stu-id="ba6dc-170"><em>C<sub>v</sub></em> = <em>C?</em></span></span> <span data-ttu-id="ba6dc-171"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="ba6dc-171"><em>C<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="ba6dc-172"><em>C<sub>v</sub> </em>  =  <em>C?</em></span><span class="sxs-lookup"><span data-stu-id="ba6dc-172"><em>C<sub>v</sub></em> = <em>C?</em></span></span></td>
<td rowspan="2"><span data-ttu-id="ba6dc-173">$ {REMOVE} $ non definito</span><span class="sxs-lookup"><span data-stu-id="ba6dc-173">undefined${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba6dc-174"><em><sub>V</sub> </em>  =  <em><sub>F</sub> </em> </span><span class="sxs-lookup"><span data-stu-id="ba6dc-174"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em> </span></span></td>
<td><span data-ttu-id="ba6dc-175"><em><sub>V</sub> </em>  =  <em><sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="ba6dc-175"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="ba6dc-176">4 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="ba6dc-176">4${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="ba6dc-177"><em>C<sub>v</sub> </em>  =  <em>C?</em></span><span class="sxs-lookup"><span data-stu-id="ba6dc-177"><em>C<sub>v</sub></em> = <em>C?</em></span></span> <span data-ttu-id="ba6dc-178"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="ba6dc-178"><em>C<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="ba6dc-179"><em>C<sub>v</sub> </em> = (1- <em>A?</em></span><span class="sxs-lookup"><span data-stu-id="ba6dc-179"><em>C<sub>v</sub></em> = (1 - <em>A?</em></span></span> <span data-ttu-id="ba6dc-180"><em>) C<sub>f</sub> </em> + <em>A?</em></span><span class="sxs-lookup"><span data-stu-id="ba6dc-180"><em>)C<sub>f</sub></em> + <em>A?</em></span></span> <span data-ttu-id="ba6dc-181"><em>C?</em></span><span class="sxs-lookup"><span data-stu-id="ba6dc-181"><em>C?</em></span></span></td>
<td rowspan="2"><span data-ttu-id="ba6dc-182">$ {REMOVE} $ non definito</span><span class="sxs-lookup"><span data-stu-id="ba6dc-182">undefined${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba6dc-183"><em><sub>V</sub> </em>  =  <em>A?</em></span><span class="sxs-lookup"><span data-stu-id="ba6dc-183"><em>A<sub>v</sub></em> = <em>A?</em></span></span> <span data-ttu-id="ba6dc-184"><em><sub>F</sub></em> </span><span class="sxs-lookup"><span data-stu-id="ba6dc-184"><em>A<sub>f</sub></em> </span></span></td>
<td><span data-ttu-id="ba6dc-185"><em><sub>V</sub> </em>  =  <em><sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="ba6dc-185"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="ba6dc-186">Se pname è \_ \_ \_ il colore dell'ENV texture GL, *params* è un puntatore a una matrice che include un colore RGBA costituito da quattro valori.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-186">If pname is GL\_TEXTURE\_ENV\_COLOR, *params* is a pointer to an array that holds an RGBA color consisting of four values.</span></span> <span data-ttu-id="ba6dc-187">I componenti dei colori integer vengono interpretati in modo lineare, in modo che il numero intero positivo sia mappato a 1,0 e l'intero più negativo sia mappato a-1,0.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-187">Integer color components are interpreted linearly such that the most positive integer maps to 1.0, and the most negative integer maps to -1.0.</span></span> <span data-ttu-id="ba6dc-188">I valori vengono fissati nell'intervallo compreso tra \[ 0 e 1 \] quando vengono specificati.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-188">The values are clamped to the range \[0, 1\] when they are specified.</span></span> <span data-ttu-id="ba6dc-189">*C <sub>c</sub>* accetta questi quattro valori.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-189">*C<sub>c</sub>* takes these four values.</span></span>

<span data-ttu-id="ba6dc-190">Per \_ impostazione predefinita, la modalità ENV della trama GL viene \_ \_ impostata su GL \_ modulari e le \_ \_ \_ impostazioni predefinite del colore ENV</span><span class="sxs-lookup"><span data-stu-id="ba6dc-190">GL\_TEXTURE\_ENV\_MODE defaults to GL\_MODULATE and GL\_TEXTURE\_ENV\_COLOR defaults to (0, 0, 0, 0).</span></span>

<span data-ttu-id="ba6dc-191">La funzione seguente recupera le informazioni correlate a **glTexEnvfv**:</span><span class="sxs-lookup"><span data-stu-id="ba6dc-191">The following function retrieves information related to **glTexEnvfv**:</span></span>

[<span data-ttu-id="ba6dc-192">**glTexGetEnvfv**</span><span class="sxs-lookup"><span data-stu-id="ba6dc-192">**glTexGetEnvfv**</span></span>](glgettexenvfv.md)

## <a name="requirements"></a><span data-ttu-id="ba6dc-193">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba6dc-193">Requirements</span></span>



| <span data-ttu-id="ba6dc-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba6dc-194">Requirement</span></span> | <span data-ttu-id="ba6dc-195">Valore</span><span class="sxs-lookup"><span data-stu-id="ba6dc-195">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba6dc-196">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba6dc-196">Minimum supported client</span></span><br/> | <span data-ttu-id="ba6dc-197">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ba6dc-197">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ba6dc-198">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba6dc-198">Minimum supported server</span></span><br/> | <span data-ttu-id="ba6dc-199">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ba6dc-199">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ba6dc-200">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ba6dc-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba6dc-201"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba6dc-201"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ba6dc-202">Libreria</span><span class="sxs-lookup"><span data-stu-id="ba6dc-202">Library</span></span><br/>                  | <dl> <span data-ttu-id="ba6dc-203"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba6dc-203"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ba6dc-204">DLL</span><span class="sxs-lookup"><span data-stu-id="ba6dc-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba6dc-205"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba6dc-205"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba6dc-206">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba6dc-206">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba6dc-207">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="ba6dc-207">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="ba6dc-208">**Remo**</span><span class="sxs-lookup"><span data-stu-id="ba6dc-208">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="ba6dc-209">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="ba6dc-209">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="ba6dc-210">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="ba6dc-210">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="ba6dc-211">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="ba6dc-211">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





