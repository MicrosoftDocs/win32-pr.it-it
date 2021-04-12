---
title: funzione glTexParameteri (GL. h)
description: Imposta i parametri della trama. | funzione glTexParameteri (GL. h)
ms.assetid: 67705f63-7f86-47c1-81f7-deecc0cd2e16
keywords:
- funzione glTexParameteri OpenGL
topic_type:
- apiref
api_name:
- glTexParameteri
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 207ac902047c5a2b6a5266d08e71f8e47f7ccb97
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352721"
---
# <a name="gltexparameteri-function"></a><span data-ttu-id="08ae8-105">glTexParameteri (funzione)</span><span class="sxs-lookup"><span data-stu-id="08ae8-105">glTexParameteri function</span></span>

<span data-ttu-id="08ae8-106">Imposta i parametri della trama.</span><span class="sxs-lookup"><span data-stu-id="08ae8-106">Sets texture parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="08ae8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="08ae8-107">Syntax</span></span>


```C++
void WINAPI glTexParameteri(
   GLenum target,
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a><span data-ttu-id="08ae8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="08ae8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08ae8-109">*target*</span><span class="sxs-lookup"><span data-stu-id="08ae8-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="08ae8-110">Trama di destinazione, che deve essere di tipo GL \_ trama \_ 1D o GL \_ trama \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="08ae8-110">The target texture, which must be either GL\_TEXTURE\_1D or GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="08ae8-111">*pname*</span><span class="sxs-lookup"><span data-stu-id="08ae8-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="08ae8-112">Nome simbolico di un parametro di trama a valore singolo.</span><span class="sxs-lookup"><span data-stu-id="08ae8-112">The symbolic name of a single valued texture parameter.</span></span> <span data-ttu-id="08ae8-113">I simboli seguenti sono accettati in *pname*.</span><span class="sxs-lookup"><span data-stu-id="08ae8-113">The following symbols are accepted in *pname*.</span></span>



| <span data-ttu-id="08ae8-114">Valore</span><span class="sxs-lookup"><span data-stu-id="08ae8-114">Value</span></span>                                                                                                                                                                                   | <span data-ttu-id="08ae8-115">Significato</span><span class="sxs-lookup"><span data-stu-id="08ae8-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <span data-ttu-id="08ae8-116"><dt>**\_ \_ Filtro minimo trama \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="08ae8-116"><dt>**GL\_TEXTURE\_MIN\_FILTER**</dt></span></span> </dl> | <span data-ttu-id="08ae8-117">La funzione minimizzazione di trama viene utilizzata ogni volta che il pixel con trama viene mappato a un'area maggiore di un elemento texture.</span><span class="sxs-lookup"><span data-stu-id="08ae8-117">The texture minifying function is used whenever the pixel being textured maps to an area greater than one texture element.</span></span> <span data-ttu-id="08ae8-118">Sono disponibili sei funzioni minimizzazione definite.</span><span class="sxs-lookup"><span data-stu-id="08ae8-118">There are six defined minifying functions.</span></span> <span data-ttu-id="08ae8-119">Due di essi utilizzano i quattro elementi di trama più vicini o più vicini per calcolare il valore di trama.</span><span class="sxs-lookup"><span data-stu-id="08ae8-119">Two of them use the nearest one or nearest four texture elements to compute the texture value.</span></span> <span data-ttu-id="08ae8-120">Gli altri quattro usano mipmap.</span><span class="sxs-lookup"><span data-stu-id="08ae8-120">The other four use mipmaps.</span></span> <br/> <span data-ttu-id="08ae8-121">Un mipmap è un set ordinato di matrici che rappresentano la stessa immagine in risoluzioni progressivamente inferiori.</span><span class="sxs-lookup"><span data-stu-id="08ae8-121">A mipmap is an ordered set of arrays representing the same image at progressively lower resolutions.</span></span> <span data-ttu-id="08ae8-122">Se la trama ha dimensioni 2nx2<sup>m</sup> sono disponibili max (n, m) + 1 mipmap.</span><span class="sxs-lookup"><span data-stu-id="08ae8-122">If the texture has dimensions 2nx2<sup>m</sup> there are max(n, m) + 1 mipmaps.</span></span> <span data-ttu-id="08ae8-123">Il primo mipmap è la trama originale, con dimensioni 2nx2<sup>m</sup>.</span><span class="sxs-lookup"><span data-stu-id="08ae8-123">The first mipmap is the original texture, with dimensions 2nx2<sup>m</sup>.</span></span> <span data-ttu-id="08ae8-124">Ogni mipmap successiva ha dimensioni 2<sup>k</sup>1x2<sup>l</sup>1 dove 2<sup>k</sup>X2<sup>l</sup> sono le dimensioni del mipmap precedente, fino a k = 0 o l = 0.</span><span class="sxs-lookup"><span data-stu-id="08ae8-124">Each subsequent mipmap has dimensions 2<sup>k</sup>1x2<sup>l</sup>1 where 2<sup>k</sup>x2<sup>l</sup> are the dimensions of the previous mipmap, until either k = 0 or l = 0.</span></span> <span data-ttu-id="08ae8-125">A questo punto, mipmap successivi hanno la dimensione 1x2<sup>l</sup>1 o 2<sup>k</sup>1x1 fino alla mipmap finale, che ha la dimensione 1x1.</span><span class="sxs-lookup"><span data-stu-id="08ae8-125">At that point, subsequent mipmaps have dimension 1x2<sup>l</sup>1 or 2<sup>k</sup>1x1 until the final mipmap, which has dimension 1x1.</span></span> <span data-ttu-id="08ae8-126">Mipmap vengono definiti usando [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md) con l'argomento del livello di dettaglio che indica l'ordine del mipmap.</span><span class="sxs-lookup"><span data-stu-id="08ae8-126">Mipmaps are defined using [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md) with the level-of-detail argument indicating the order of the mipmaps.</span></span> <span data-ttu-id="08ae8-127">Il livello 0 è la trama originale; il livello max Bold (n, m) è il mipmap 1x1 finale.</span><span class="sxs-lookup"><span data-stu-id="08ae8-127">Level 0 is the original texture; level bold max(n, m) is the final 1x1 mipmap.</span></span><br/> |
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <span data-ttu-id="08ae8-128"><dt>**\_ \_ filtro mag trama di contabilità \_**</dt></span><span class="sxs-lookup"><span data-stu-id="08ae8-128"><dt>**GL\_TEXTURE\_MAG\_FILTER**</dt></span></span> </dl> | <span data-ttu-id="08ae8-129">La funzione di ingrandimento della trama viene utilizzata quando il pixel con trama viene mappato a un'area minore o uguale a un elemento texture.</span><span class="sxs-lookup"><span data-stu-id="08ae8-129">The texture magnification function is used when the pixel being textured maps to an area less than or equal to one texture element.</span></span> <span data-ttu-id="08ae8-130">Imposta la funzione di ingrandimento della trama su GL \_ più vicino o su GL \_ lineare.</span><span class="sxs-lookup"><span data-stu-id="08ae8-130">It sets the texture magnification function to either GL\_NEAREST or GL\_LINEAR.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <span data-ttu-id="08ae8-131"><dt>**\_wrapping di trama GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="08ae8-131"><dt>**GL\_TEXTURE\_WRAP\_S**</dt></span></span> </dl>             | <span data-ttu-id="08ae8-132">Imposta il parametro Wrap per le coordinate di trama su GL \_ clamp o GL \_ Repeat.</span><span class="sxs-lookup"><span data-stu-id="08ae8-132">Sets the wrap parameter for texture coordinate s to either GL\_CLAMP or GL\_REPEAT.</span></span> <span data-ttu-id="08ae8-133">\_Il morsetto GL causa il fissaggio delle coordinate a nell'intervallo \[ 0, 1 \] ed è utile per impedire l'inserimento di elementi quando si esegue il mapping di una singola immagine in un oggetto.</span><span class="sxs-lookup"><span data-stu-id="08ae8-133">GL\_CLAMP causes s coordinates to be clamped to the range \[0,1\] and is useful for preventing wrapping artifacts when mapping a single image onto an object.</span></span> <span data-ttu-id="08ae8-134">\_La ripetizione GL fa sì che la parte intera della coordinata s venga ignorata. OpenGL usa solo la parte frazionaria, creando così un modello ripetuto.</span><span class="sxs-lookup"><span data-stu-id="08ae8-134">GL\_REPEAT causes the integer part of the s coordinate to be ignored; OpenGL uses only the fractional part, thereby creating a repeating pattern.</span></span> <span data-ttu-id="08ae8-135">Gli elementi di trama del bordo sono accessibili solo se il wrapping è impostato sul \_ morsetto GL.</span><span class="sxs-lookup"><span data-stu-id="08ae8-135">Border texture elements are accessed only if wrapping is set to GL\_CLAMP.</span></span> <span data-ttu-id="08ae8-136">Inizialmente, GL \_ texture \_ Wrap \_ S è impostato su GL \_ Repeat.</span><span class="sxs-lookup"><span data-stu-id="08ae8-136">Initially, GL\_TEXTURE\_WRAP\_S is set to GL\_REPEAT.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <span data-ttu-id="08ae8-137"><dt>**\_wrapping trama \_ GL \_ T**</dt></span><span class="sxs-lookup"><span data-stu-id="08ae8-137"><dt>**GL\_TEXTURE\_WRAP\_T**</dt></span></span> </dl>             | <span data-ttu-id="08ae8-138">Imposta il parametro Wrap per la coordinata di trama t su un \_ morsetto GL o una \_ ripetizione GL.</span><span class="sxs-lookup"><span data-stu-id="08ae8-138">Sets the wrap parameter for texture coordinate t to either GL\_CLAMP or GL\_REPEAT.</span></span> <span data-ttu-id="08ae8-139">Vedere la discussione in GL \_ trama \_ Wrap \_ S.</span><span class="sxs-lookup"><span data-stu-id="08ae8-139">See the discussion under GL\_TEXTURE\_WRAP\_S.</span></span> <span data-ttu-id="08ae8-140">Inizialmente, GL \_ texture \_ Wrap \_ T è impostato su GL \_ Repeat</span><span class="sxs-lookup"><span data-stu-id="08ae8-140">Initially, GL\_TEXTURE\_WRAP\_T is set to GL\_REPEAT</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="08ae8-141">*param*</span><span class="sxs-lookup"><span data-stu-id="08ae8-141">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="08ae8-142">Valore di *pname*.</span><span class="sxs-lookup"><span data-stu-id="08ae8-142">The value of *pname*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08ae8-143">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="08ae8-143">Return value</span></span>

<span data-ttu-id="08ae8-144">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="08ae8-144">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="08ae8-145">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="08ae8-145">Error codes</span></span>

<span data-ttu-id="08ae8-146">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="08ae8-146">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="08ae8-147">Nome</span><span class="sxs-lookup"><span data-stu-id="08ae8-147">Name</span></span>                                                                                                  | <span data-ttu-id="08ae8-148">Significato</span><span class="sxs-lookup"><span data-stu-id="08ae8-148">Meaning</span></span>                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="08ae8-149"><dt>**GL \_ \_enumerazione non valida**</dt></span><span class="sxs-lookup"><span data-stu-id="08ae8-149"><dt>**GL\_INVALID\_ENUM** </dt></span></span> </dl>     | <span data-ttu-id="08ae8-150">*target* o *pname* non è uno dei valori definiti accettati oppure quando *param* deve avere un valore costante definito (in base al valore di *pname*) e no.</span><span class="sxs-lookup"><span data-stu-id="08ae8-150">*target* or *pname* was not one of the accepted defined values, or when *param* should have had a defined constant value (based on the value of *pname*) and did not.</span></span><br/> |
| <dl> <span data-ttu-id="08ae8-151"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="08ae8-151"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="08ae8-152">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="08ae8-152">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                            |



## <a name="remarks"></a><span data-ttu-id="08ae8-153">Commenti</span><span class="sxs-lookup"><span data-stu-id="08ae8-153">Remarks</span></span>

<span data-ttu-id="08ae8-154">Il mapping di trama è una tecnica che applica un'immagine alla superficie di un oggetto come se l'immagine fosse una decalcomania o una compattazione di cellophane.</span><span class="sxs-lookup"><span data-stu-id="08ae8-154">Texture mapping is a technique that applies an image onto an object's surface as if the image were a decal or cellophane shrink-wrap.</span></span> <span data-ttu-id="08ae8-155">L'immagine viene creata nello spazio di trama con un sistema di coordinate (*s*, *t*).</span><span class="sxs-lookup"><span data-stu-id="08ae8-155">The image is created in texture space, with an (*s*, *t*) coordinate system.</span></span> <span data-ttu-id="08ae8-156">Una trama è un'immagine a una o due dimensioni e un set di parametri che determinano la modalità di derivazione degli esempi dall'immagine.</span><span class="sxs-lookup"><span data-stu-id="08ae8-156">A texture is a one- or two-dimensional image and a set of parameters that determine how samples are derived from the image.</span></span>

<span data-ttu-id="08ae8-157">La funzione **glTexParameter** assegna il valore o i valori in params al parametro texture specificato come pname.</span><span class="sxs-lookup"><span data-stu-id="08ae8-157">The **glTexParameter** function assigns the value or values in params to the texture parameter specified as pname.</span></span> <span data-ttu-id="08ae8-158">Il parametro target definisce la trama di destinazione, ovvero GL \_ texture \_ 1D o GL \_ texture \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="08ae8-158">The target parameter defines the target texture, either GL\_TEXTURE\_1D or GL\_TEXTURE\_2D.</span></span>

<span data-ttu-id="08ae8-159">Poiché nel processo minification vengono campionati più elementi di trama, saranno evidenti meno artefatti di aliasing.</span><span class="sxs-lookup"><span data-stu-id="08ae8-159">As more texture elements are sampled in the minification process, fewer aliasing artifacts will be apparent.</span></span> <span data-ttu-id="08ae8-160">Sebbene le \_ funzioni GL più vicine e GL \_ Linear minification possano essere più veloci delle altre quattro, campionano solo uno o quattro elementi di trama per determinare il valore di trama del pixel di cui viene eseguito il rendering e possono produrre modelli moiré o transizioni incomplete.</span><span class="sxs-lookup"><span data-stu-id="08ae8-160">While the GL\_NEAREST and GL\_LINEAR minification functions can be faster than the other four, they sample only one or four texture elements to determine the texture value of the pixel being rendered and can produce moire patterns or ragged transitions.</span></span> <span data-ttu-id="08ae8-161">Il valore predefinito del \_ filtro di trama \_ min è GL \_ \_ più vicino \_ MIPMAP \_ lineare.</span><span class="sxs-lookup"><span data-stu-id="08ae8-161">The default value of GL\_TEXTURE\_MIN\_FILTER is GL\_NEAREST\_MIPMAP\_LINEAR.</span></span>

<span data-ttu-id="08ae8-162">Si supponga che la funzionalità di texturing sia abilitata (chiamando [**glEnable**](glenable.md) con argomento GL \_ texture \_ 1D o GL \_ texture \_ 2D) e \_ \_ \_ il filtro di trama GL min sia impostato su una delle funzioni che richiedono un mipmap.</span><span class="sxs-lookup"><span data-stu-id="08ae8-162">Suppose that texturing is enabled (by calling [**glEnable**](glenable.md) with argument GL\_TEXTURE\_1D or GL\_TEXTURE\_2D) and GL\_TEXTURE\_MIN\_FILTER is set to one of the functions that requires a mipmap.</span></span> <span data-ttu-id="08ae8-163">Se le dimensioni delle immagini di trama attualmente definite (con chiamate precedenti a [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md)) non seguono la sequenza corretta per mipmap o se sono presenti meno immagini di trama definite rispetto a quelle necessarie o se il set di immagini di trama presenta numeri diversi di componenti di trama, è come se il mapping della trama fosse disabilitato.</span><span class="sxs-lookup"><span data-stu-id="08ae8-163">If either the dimensions of the texture images currently defined (with previous calls to [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md)) do not follow the proper sequence for mipmaps, or there are fewer texture images defined than are needed, or the set of texture images have differing numbers of texture components, then it is as if texture mapping were disabled.</span></span> <span data-ttu-id="08ae8-164">Il filtro lineare accede ai quattro elementi di trama più vicini solo nelle trame 2D.</span><span class="sxs-lookup"><span data-stu-id="08ae8-164">Linear filtering accesses the four nearest texture elements only in 2-D textures.</span></span> <span data-ttu-id="08ae8-165">Nelle trame da 1 a, il filtro lineare accede ai due elementi di trama più vicini.</span><span class="sxs-lookup"><span data-stu-id="08ae8-165">In 1-D textures, linear filtering accesses the two nearest texture elements.</span></span> <span data-ttu-id="08ae8-166">La funzione seguente recupera le informazioni relative a **glTexParameterf**, **glTexParameteri**, **glTexParameterfv** e **glTexParameteriv**:</span><span class="sxs-lookup"><span data-stu-id="08ae8-166">The following function retrieves information related to **glTexParameterf**, **glTexParameteri**, **glTexParameterfv**, and **glTexParameteriv**:</span></span>

[<span data-ttu-id="08ae8-167">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="08ae8-167">**glGetTexParameter**</span></span>](glgettexparameter.md)

## <a name="requirements"></a><span data-ttu-id="08ae8-168">Requisiti</span><span class="sxs-lookup"><span data-stu-id="08ae8-168">Requirements</span></span>



| <span data-ttu-id="08ae8-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="08ae8-169">Requirement</span></span> | <span data-ttu-id="08ae8-170">Valore</span><span class="sxs-lookup"><span data-stu-id="08ae8-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08ae8-171">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08ae8-171">Minimum supported client</span></span><br/> | <span data-ttu-id="08ae8-172">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="08ae8-172">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="08ae8-173">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08ae8-173">Minimum supported server</span></span><br/> | <span data-ttu-id="08ae8-174">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="08ae8-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="08ae8-175">Intestazione</span><span class="sxs-lookup"><span data-stu-id="08ae8-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="08ae8-176"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="08ae8-176"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="08ae8-177">Libreria</span><span class="sxs-lookup"><span data-stu-id="08ae8-177">Library</span></span><br/>                  | <dl> <span data-ttu-id="08ae8-178"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="08ae8-178"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="08ae8-179">DLL</span><span class="sxs-lookup"><span data-stu-id="08ae8-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08ae8-180"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08ae8-180"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08ae8-181">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="08ae8-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08ae8-182">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="08ae8-182">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="08ae8-183">**glBindTexture**</span><span class="sxs-lookup"><span data-stu-id="08ae8-183">**glBindTexture**</span></span>](glbindtexture.md)
</dt> <dt>

[<span data-ttu-id="08ae8-184">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="08ae8-184">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="08ae8-185">**glCopyTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="08ae8-185">**glCopyTexImage1D**</span></span>](glcopyteximage1d.md)
</dt> <dt>

[<span data-ttu-id="08ae8-186">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="08ae8-186">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="08ae8-187">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="08ae8-187">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="08ae8-188">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="08ae8-188">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="08ae8-189">**Remo**</span><span class="sxs-lookup"><span data-stu-id="08ae8-189">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="08ae8-190">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="08ae8-190">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="08ae8-191">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="08ae8-191">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="08ae8-192">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="08ae8-192">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="08ae8-193">**glPrioritizeTextures**</span><span class="sxs-lookup"><span data-stu-id="08ae8-193">**glPrioritizeTextures**</span></span>](glprioritizetextures.md)
</dt> <dt>

[<span data-ttu-id="08ae8-194">glTexEnv</span><span class="sxs-lookup"><span data-stu-id="08ae8-194">glTexEnv</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="08ae8-195">glTexGen</span><span class="sxs-lookup"><span data-stu-id="08ae8-195">glTexGen</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="08ae8-196">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="08ae8-196">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="08ae8-197">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="08ae8-197">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="08ae8-198">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="08ae8-198">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="08ae8-199">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="08ae8-199">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> </dl>

 

 





