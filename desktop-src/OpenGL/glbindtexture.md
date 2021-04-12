---
title: funzione glBindTexture (GL. h)
description: La funzione glBindTexture consente la creazione di una trama denominata associata a una destinazione di trama.
ms.assetid: 800f2360-b40e-4911-9a45-6f310aeeefeb
keywords:
- funzione glBindTexture OpenGL
topic_type:
- apiref
api_name:
- glBindTexture
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e76009a486e3903ad8230891af8b7593ab8aaa47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400709"
---
# <a name="glbindtexture-function"></a><span data-ttu-id="81281-104">glBindTexture (funzione)</span><span class="sxs-lookup"><span data-stu-id="81281-104">glBindTexture function</span></span>

<span data-ttu-id="81281-105">La funzione **glBindTexture** consente la creazione di una trama denominata associata a una destinazione di trama.</span><span class="sxs-lookup"><span data-stu-id="81281-105">The **glBindTexture** function enables the creation of a named texture that is bound to a texture target.</span></span>

## <a name="syntax"></a><span data-ttu-id="81281-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="81281-106">Syntax</span></span>


```C++
void WINAPI glBindTexture(
   GLenum target,
   GLuint texture
);
```



## <a name="parameters"></a><span data-ttu-id="81281-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="81281-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81281-108">*target*</span><span class="sxs-lookup"><span data-stu-id="81281-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="81281-109">Destinazione a cui è associata la trama.</span><span class="sxs-lookup"><span data-stu-id="81281-109">The target to which the texture is bound.</span></span> <span data-ttu-id="81281-110">È necessario che il valore di GL \_ trama \_ 1D o GL \_ trama \_ 2D sia.</span><span class="sxs-lookup"><span data-stu-id="81281-110">Must have the value GL\_TEXTURE\_1D or GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="81281-111">*trama*</span><span class="sxs-lookup"><span data-stu-id="81281-111">*texture*</span></span> 
</dt> <dd>

<span data-ttu-id="81281-112">Nome di una trama; il nome della trama non può essere attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="81281-112">The name of a texture; the texture name cannot currently be in use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81281-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="81281-113">Return value</span></span>

<span data-ttu-id="81281-114">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="81281-114">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="81281-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="81281-115">Error codes</span></span>

<span data-ttu-id="81281-116">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="81281-116">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="81281-117">Nome</span><span class="sxs-lookup"><span data-stu-id="81281-117">Name</span></span>                                                                                                  | <span data-ttu-id="81281-118">Significato</span><span class="sxs-lookup"><span data-stu-id="81281-118">Meaning</span></span>                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="81281-119"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="81281-119"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="81281-120">La *destinazione* del parametro non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="81281-120">The parameter *target* was not an accepted value.</span></span><br/>                                                                                                                                                       |
| <dl> <span data-ttu-id="81281-121"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="81281-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="81281-122">La *trama* del parametro non ha la stessa dimensionalità della *destinazione* oppure è stata chiamata la funzione tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="81281-122">The parameter *texture* did not have the same dimensionality as *target*, or the function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="81281-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="81281-123">Remarks</span></span>

<span data-ttu-id="81281-124">La funzione **glBindTexture** consente di creare una trama denominata.</span><span class="sxs-lookup"><span data-stu-id="81281-124">The **glBindTexture** function enables you to create a named texture.</span></span> <span data-ttu-id="81281-125">La chiamata di **glBindTexture** con la *destinazione* impostata su GL \_ texture \_ 1D o GL \_ trama \_ 2D e la *trama* impostata sul nome della nuova trama creata associa il nome della trama alla destinazione di trama appropriata.</span><span class="sxs-lookup"><span data-stu-id="81281-125">Calling **glBindTexture** with *target* set to GL\_TEXTURE\_1D or GL\_TEXTURE\_2D, and *texture* set to the name of the new texture you have created binds the texture name to the appropriate texture target.</span></span> <span data-ttu-id="81281-126">Quando una trama è associata a una destinazione, l'associazione precedente per tale destinazione non è più attiva.</span><span class="sxs-lookup"><span data-stu-id="81281-126">When a texture is bound to a target, the previous binding for that target is no longer in effect.</span></span>

<span data-ttu-id="81281-127">I nomi di trama sono interi senza segno il cui valore è zero riservato per rappresentare la trama predefinita per ogni destinazione di trama.</span><span class="sxs-lookup"><span data-stu-id="81281-127">Texture names are unsigned integers with the value zero reserved to represent the default texture for each texture target.</span></span> <span data-ttu-id="81281-128">I nomi di trama e il contenuto della trama corrispondente sono locali nello spazio di visualizzazione condiviso del contesto di rendering OpenGL corrente. due contesti di rendering condividono nomi di trama solo se condividono anche elenchi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="81281-128">Texture names and the corresponding texture contents are local to the shared display-list space of the current OpenGL rendering context; two rendering contexts share texture names only if they also share display lists.</span></span> <span data-ttu-id="81281-129">È possibile generare un set di nuovi nomi di trama usando [**glGenTextures**](glgentextures.md).</span><span class="sxs-lookup"><span data-stu-id="81281-129">You can generate a set of new texture names using [**glGenTextures**](glgentextures.md).</span></span>

<span data-ttu-id="81281-130">Quando una trama viene associata per la prima volta, presuppone la dimensionalità della relativa destinazione di trama; una trama associata alla \_ trama GL \_ 1D diventa unidimensionale e una trama associata alla trama GL \_ \_ 2D diventa bidimensionale.</span><span class="sxs-lookup"><span data-stu-id="81281-130">When a texture is first bound, it assumes the dimensionality of its texture target; a texture bound to GL\_TEXTURE\_1D becomes one-dimensional and a texture bound to GL\_TEXTURE\_2D becomes two-dimensional.</span></span> <span data-ttu-id="81281-131">Le operazioni eseguite su una destinazione di trama influiscono anche su una trama associata alla destinazione.</span><span class="sxs-lookup"><span data-stu-id="81281-131">Operations you perform on a texture target also affect a texture bound to the target.</span></span> <span data-ttu-id="81281-132">Quando si esegue una query su una destinazione di trama, il valore restituito è lo stato della trama a esso associata.</span><span class="sxs-lookup"><span data-stu-id="81281-132">When you query a texture target, the return value is the state of the texture bound to it.</span></span> <span data-ttu-id="81281-133">Le destinazioni di trama diventano alias per le trame attualmente vincolate.</span><span class="sxs-lookup"><span data-stu-id="81281-133">Texture targets become aliases for textures currently bound to them.</span></span>

<span data-ttu-id="81281-134">Quando si associa una trama a **glBindTexture**, l'associazione rimane attiva fino a quando una trama diversa viene associata alla stessa destinazione o si elimina la trama associata con la funzione [**glDeleteTextures**](gldeletetextures.md) .</span><span class="sxs-lookup"><span data-stu-id="81281-134">When you bind a texture with **glBindTexture**, the binding remains active until a different texture is bound to the same target or you delete the bound texture with the [**glDeleteTextures**](gldeletetextures.md) function.</span></span> <span data-ttu-id="81281-135">Dopo aver creato una trama denominata, è possibile associarla a una destinazione di trama con la stessa dimensionalità della frequenza necessaria.</span><span class="sxs-lookup"><span data-stu-id="81281-135">Once you create a named texture you can bind it to a texture target that has the same dimensionality as often as needed.</span></span>

<span data-ttu-id="81281-136">In genere è molto più veloce usare **glBindTexture** per associare una trama denominata esistente a una delle destinazioni di trama anziché ricaricare l'immagine di trama usando [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="81281-136">It is usually much faster to use **glBindTexture** to bind an existing named texture to one of the texture targets than it is to reload the texture image using [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span> <span data-ttu-id="81281-137">Per un maggiore controllo sulle prestazioni di texturing, usare [**glPrioritizeTextures**](glprioritizetextures.md).</span><span class="sxs-lookup"><span data-stu-id="81281-137">For additional control of texturing performance, use [**glPrioritizeTextures**](glprioritizetextures.md).</span></span>

<span data-ttu-id="81281-138">È possibile includere chiamate a **glBindTexture** negli elenchi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="81281-138">You can include calls to **glBindTexture** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="81281-139">La funzione **glBindTexture** è disponibile solo in OpenGL versione 1,1 o successiva.</span><span class="sxs-lookup"><span data-stu-id="81281-139">The **glBindTexture** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="81281-140">Le funzioni seguenti consentono di recuperare informazioni correlate a **glBindTexture**:</span><span class="sxs-lookup"><span data-stu-id="81281-140">The following functions retrieve information related to **glBindTexture**:</span></span>

-   <span data-ttu-id="81281-141">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ texture \_ 1D \_ binding</span><span class="sxs-lookup"><span data-stu-id="81281-141">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_TEXTURE\_1D\_BINDING</span></span>

<span data-ttu-id="81281-142">**glGet** con argomento GL \_ trama \_ 2D \_ binding</span><span class="sxs-lookup"><span data-stu-id="81281-142">**glGet** with argument GL\_TEXTURE\_2D\_BINDING</span></span>

## <a name="requirements"></a><span data-ttu-id="81281-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81281-143">Requirements</span></span>



| <span data-ttu-id="81281-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="81281-144">Requirement</span></span> | <span data-ttu-id="81281-145">Valore</span><span class="sxs-lookup"><span data-stu-id="81281-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81281-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81281-146">Minimum supported client</span></span><br/> | <span data-ttu-id="81281-147">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="81281-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="81281-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81281-148">Minimum supported server</span></span><br/> | <span data-ttu-id="81281-149">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="81281-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="81281-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="81281-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="81281-151"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="81281-151"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="81281-152">Libreria</span><span class="sxs-lookup"><span data-stu-id="81281-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="81281-153"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81281-153"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="81281-154">DLL</span><span class="sxs-lookup"><span data-stu-id="81281-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81281-155"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81281-155"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81281-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="81281-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81281-157">**glAreTexturesResident**</span><span class="sxs-lookup"><span data-stu-id="81281-157">**glAreTexturesResident**</span></span>](glaretexturesresident.md)
</dt> <dt>

[<span data-ttu-id="81281-158">**glDeleteTextures**</span><span class="sxs-lookup"><span data-stu-id="81281-158">**glDeleteTextures**</span></span>](gldeletetextures.md)
</dt> <dt>

[<span data-ttu-id="81281-159">**glGenTextures**</span><span class="sxs-lookup"><span data-stu-id="81281-159">**glGenTextures**</span></span>](glgentextures.md)
</dt> <dt>

[<span data-ttu-id="81281-160">**glGet**</span><span class="sxs-lookup"><span data-stu-id="81281-160">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="81281-161">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="81281-161">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="81281-162">**glIsTexture**</span><span class="sxs-lookup"><span data-stu-id="81281-162">**glIsTexture**</span></span>](glistexture.md)
</dt> <dt>

[<span data-ttu-id="81281-163">**glPrioritizeTextures**</span><span class="sxs-lookup"><span data-stu-id="81281-163">**glPrioritizeTextures**</span></span>](glprioritizetextures.md)
</dt> <dt>

[<span data-ttu-id="81281-164">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="81281-164">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="81281-165">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="81281-165">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="81281-166">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="81281-166">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





