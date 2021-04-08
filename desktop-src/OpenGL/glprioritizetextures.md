---
title: funzione glPrioritizeTextures (GL. h)
description: La funzione glPrioritizeTextures imposta la priorità di residenza delle trame.
ms.assetid: 09018c86-c667-4e43-a95a-51a8077aed33
keywords:
- funzione glPrioritizeTextures OpenGL
topic_type:
- apiref
api_name:
- glPrioritizeTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d38ab4b1bd6b5f9682b4d8753e7e84f1f2b58a09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740647"
---
# <a name="glprioritizetextures-function"></a><span data-ttu-id="ccd1a-104">glPrioritizeTextures (funzione)</span><span class="sxs-lookup"><span data-stu-id="ccd1a-104">glPrioritizeTextures function</span></span>

<span data-ttu-id="ccd1a-105">La funzione **glPrioritizeTextures** imposta la priorità di residenza delle trame.</span><span class="sxs-lookup"><span data-stu-id="ccd1a-105">The **glPrioritizeTextures** function sets the residence priority of textures.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccd1a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ccd1a-106">Syntax</span></span>


```C++
void WINAPI glPrioritizeTextures(
         GLsizei  n,
   const GLuint   *textures,
   const GLclampf *priorities
);
```



## <a name="parameters"></a><span data-ttu-id="ccd1a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ccd1a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccd1a-108">*n*</span><span class="sxs-lookup"><span data-stu-id="ccd1a-108">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="ccd1a-109">Numero di trame da assegnare in ordine di priorità.</span><span class="sxs-lookup"><span data-stu-id="ccd1a-109">The number of textures to be prioritized.</span></span>

</dd> <dt>

<span data-ttu-id="ccd1a-110">*trame*</span><span class="sxs-lookup"><span data-stu-id="ccd1a-110">*textures*</span></span> 
</dt> <dd>

<span data-ttu-id="ccd1a-111">Puntatore al primo elemento di una matrice contenente i nomi delle trame da assegnare in ordine di priorità.</span><span class="sxs-lookup"><span data-stu-id="ccd1a-111">A pointer to the first element of an array containing the names of the textures to be prioritized.</span></span>

</dd> <dt>

<span data-ttu-id="ccd1a-112">*priorità*</span><span class="sxs-lookup"><span data-stu-id="ccd1a-112">*priorities*</span></span> 
</dt> <dd>

<span data-ttu-id="ccd1a-113">Puntatore al primo elemento di una matrice contenente le priorità della trama.</span><span class="sxs-lookup"><span data-stu-id="ccd1a-113">A pointer to the first element of an array containing the texture priorities.</span></span> <span data-ttu-id="ccd1a-114">Una priorità specificata in un elemento *del parametro* prioritys viene applicata alla trama denominata dall'elemento corrispondente del parametro *Textures* .</span><span class="sxs-lookup"><span data-stu-id="ccd1a-114">A priority given in an element of the *priorities* parameter applies to the texture named by the corresponding element of the *textures* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccd1a-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ccd1a-115">Return value</span></span>

<span data-ttu-id="ccd1a-116">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="ccd1a-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ccd1a-117">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="ccd1a-117">Error codes</span></span>

<span data-ttu-id="ccd1a-118">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="ccd1a-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="ccd1a-119">Nome</span><span class="sxs-lookup"><span data-stu-id="ccd1a-119">Name</span></span>                                                                                                  | <span data-ttu-id="ccd1a-120">Significato</span><span class="sxs-lookup"><span data-stu-id="ccd1a-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ccd1a-121"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ccd1a-121"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="ccd1a-122">*n* è un valore negativo.</span><span class="sxs-lookup"><span data-stu-id="ccd1a-122">*n* was a negative value.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="ccd1a-123"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ccd1a-123"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="ccd1a-124">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="ccd1a-124">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ccd1a-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="ccd1a-125">Remarks</span></span>

<span data-ttu-id="ccd1a-126">La funzione **glPrioritizeTextures** assegna le priorità di trama *n* specificate nel parametro *priorità* alle *n* trame denominate nel parametro *Textures* .</span><span class="sxs-lookup"><span data-stu-id="ccd1a-126">The **glPrioritizeTextures** function assigns the *n* texture priorities specified in the *priorities* parameter to the *n* textures named in the *textures* parameter.</span></span> <span data-ttu-id="ccd1a-127">Nei computer con una quantità limitata di memoria di trama, OpenGL stabilisce un "working set" di trame che sono residenti nella memoria della trama.</span><span class="sxs-lookup"><span data-stu-id="ccd1a-127">On computers with a limited amount of texture memory, OpenGL establishes a "working set" of textures that are resident in texture memory.</span></span> <span data-ttu-id="ccd1a-128">Queste trame possono essere associate a una destinazione di trama in modo molto più efficiente rispetto alle trame non residenti.</span><span class="sxs-lookup"><span data-stu-id="ccd1a-128">These textures can be bound to a texture target much more efficiently than textures that are not resident.</span></span>

<span data-ttu-id="ccd1a-129">Specificando una priorità per ogni trama, la funzione **glPrioritizeTextures** consente di determinare quali trame devono essere residenti.</span><span class="sxs-lookup"><span data-stu-id="ccd1a-129">By specifying a priority for each texture, the **glPrioritizeTextures** function enables you to determine which textures should be resident.</span></span>

<span data-ttu-id="ccd1a-130">Gli elementi priorità trama nelle *priorità* vengono fissati nell'intervallo \[ 0,0, 1,0 \] prima di essere assegnati.</span><span class="sxs-lookup"><span data-stu-id="ccd1a-130">The texture priorities elements in *priorities* are clamped to the range \[0.0, 1.0\] before being assigned.</span></span> <span data-ttu-id="ccd1a-131">Zero indica la priorità più bassa; in questo modo, le trame con priorità zero sono meno idonee per la residenza.</span><span class="sxs-lookup"><span data-stu-id="ccd1a-131">Zero indicates the lowest priority; thus textures with priority zero are least likely to be resident.</span></span> <span data-ttu-id="ccd1a-132">Il valore 1,0 indica la priorità più alta. in questo modo, è probabile che le trame con priorità 1,0 siano residenti.</span><span class="sxs-lookup"><span data-stu-id="ccd1a-132">The value 1.0 indicates the highest priority; thus textures with priority 1.0 are most likely to be resident.</span></span> <span data-ttu-id="ccd1a-133">Tuttavia, non è garantito che le trame siano residenti fino a quando non sono associate.</span><span class="sxs-lookup"><span data-stu-id="ccd1a-133">However, textures are not guaranteed to be resident until they are bound.</span></span>

<span data-ttu-id="ccd1a-134">La funzione **glPrioritizeTextures** ignora i tentativi di assegnazione delle priorità alla trama 0 o a qualsiasi nome di trama che non corrisponde a una trama esistente.</span><span class="sxs-lookup"><span data-stu-id="ccd1a-134">The **glPrioritizeTextures** function ignores attempts to prioritize texture 0, or any texture name that does not correspond to an existing texture.</span></span> <span data-ttu-id="ccd1a-135">Nessuna delle funzioni denominate dal parametro *Textures* deve essere associata a una destinazione di trama.</span><span class="sxs-lookup"><span data-stu-id="ccd1a-135">None of the functions named by the *textures* parameter need to be bound to a texture target.</span></span>

<span data-ttu-id="ccd1a-136">Se una trama è attualmente associata, è anche possibile usare la funzione [**glTexParameter**](gltexparameter-functions.md) per impostarne la priorità.</span><span class="sxs-lookup"><span data-stu-id="ccd1a-136">If a texture is currently bound, you can also use the [**glTexParameter**](gltexparameter-functions.md) function to set its priority.</span></span> <span data-ttu-id="ccd1a-137">Questo è l'unico modo per impostare la priorità di una trama predefinita.</span><span class="sxs-lookup"><span data-stu-id="ccd1a-137">This is the only way to set the priority of a default texture.</span></span>

<span data-ttu-id="ccd1a-138">È possibile includere **glPrioritizeTextures** negli elenchi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="ccd1a-138">You can include **glPrioritizeTextures** in display lists.</span></span>

<span data-ttu-id="ccd1a-139">La funzione seguente recupera la priorità di una trama attualmente associata a **glPrioritizeTextures**:</span><span class="sxs-lookup"><span data-stu-id="ccd1a-139">The following function retrieves the priority of a currently-bound texture related to **glPrioritizeTextures**:</span></span>

-   <span data-ttu-id="ccd1a-140">[**glGetTexParameter**](glgettexparameter.md) con nome parametro \_ priorità trama \_ GL</span><span class="sxs-lookup"><span data-stu-id="ccd1a-140">[**glGetTexParameter**](glgettexparameter.md) with parameter name GL\_TEXTURE\_PRIORITY</span></span>

> [!Note]  
> <span data-ttu-id="ccd1a-141">La funzione **glPrioritizeTextures** è disponibile solo in OpenGL versione 1,1 o successiva.</span><span class="sxs-lookup"><span data-stu-id="ccd1a-141">The **glPrioritizeTextures** function is only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ccd1a-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ccd1a-142">Requirements</span></span>



| <span data-ttu-id="ccd1a-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccd1a-143">Requirement</span></span> | <span data-ttu-id="ccd1a-144">Valore</span><span class="sxs-lookup"><span data-stu-id="ccd1a-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ccd1a-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ccd1a-145">Minimum supported client</span></span><br/> | <span data-ttu-id="ccd1a-146">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ccd1a-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ccd1a-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ccd1a-147">Minimum supported server</span></span><br/> | <span data-ttu-id="ccd1a-148">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ccd1a-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ccd1a-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ccd1a-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccd1a-150"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccd1a-150"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ccd1a-151">Libreria</span><span class="sxs-lookup"><span data-stu-id="ccd1a-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="ccd1a-152"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ccd1a-152"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ccd1a-153">DLL</span><span class="sxs-lookup"><span data-stu-id="ccd1a-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccd1a-154"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccd1a-154"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccd1a-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ccd1a-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccd1a-156">**glAreTexturesResident**</span><span class="sxs-lookup"><span data-stu-id="ccd1a-156">**glAreTexturesResident**</span></span>](glaretexturesresident.md)
</dt> <dt>

[<span data-ttu-id="ccd1a-157">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="ccd1a-157">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="ccd1a-158">**Remo**</span><span class="sxs-lookup"><span data-stu-id="ccd1a-158">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="ccd1a-159">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="ccd1a-159">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="ccd1a-160">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="ccd1a-160">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="ccd1a-161">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="ccd1a-161">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="ccd1a-162">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="ccd1a-162">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





