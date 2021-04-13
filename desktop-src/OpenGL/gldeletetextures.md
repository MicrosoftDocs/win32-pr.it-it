---
title: funzione glDeleteTextures (GL. h)
description: La funzione glDeleteTextures Elimina le trame denominate.
ms.assetid: 300eb99a-9ee5-4495-9489-7e084db9c6c1
keywords:
- funzione glDeleteTextures OpenGL
topic_type:
- apiref
api_name:
- glDeleteTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37893874f143a210bde0099caa7b5ec266f8948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475676"
---
# <a name="gldeletetextures-function"></a><span data-ttu-id="859e3-104">glDeleteTextures (funzione)</span><span class="sxs-lookup"><span data-stu-id="859e3-104">glDeleteTextures function</span></span>

<span data-ttu-id="859e3-105">La funzione **glDeleteTextures** Elimina le trame denominate.</span><span class="sxs-lookup"><span data-stu-id="859e3-105">The **glDeleteTextures** function deletes named textures.</span></span>

## <a name="syntax"></a><span data-ttu-id="859e3-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="859e3-106">Syntax</span></span>


```C++
void WINAPI glDeleteTextures(
         GLsizei n,
   const GLuint  *textures
);
```



## <a name="parameters"></a><span data-ttu-id="859e3-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="859e3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="859e3-108">*n*</span><span class="sxs-lookup"><span data-stu-id="859e3-108">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="859e3-109">Numero di trame da eliminare.</span><span class="sxs-lookup"><span data-stu-id="859e3-109">The number of textures to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="859e3-110">*trame*</span><span class="sxs-lookup"><span data-stu-id="859e3-110">*textures*</span></span> 
</dt> <dd>

<span data-ttu-id="859e3-111">Matrice di trame da eliminare.</span><span class="sxs-lookup"><span data-stu-id="859e3-111">An array of textures to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="859e3-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="859e3-112">Return value</span></span>

<span data-ttu-id="859e3-113">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="859e3-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="859e3-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="859e3-114">Error codes</span></span>

<span data-ttu-id="859e3-115">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="859e3-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="859e3-116">Nome</span><span class="sxs-lookup"><span data-stu-id="859e3-116">Name</span></span>                                                                                                  | <span data-ttu-id="859e3-117">Significato</span><span class="sxs-lookup"><span data-stu-id="859e3-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="859e3-118"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="859e3-118"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="859e3-119">*n* è un valore negativo.</span><span class="sxs-lookup"><span data-stu-id="859e3-119">*n* was a negative value.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="859e3-120"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="859e3-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="859e3-121">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="859e3-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="859e3-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="859e3-122">Remarks</span></span>

<span data-ttu-id="859e3-123">La funzione **glDeleteTextures** Elimina *n* trame denominate dagli elementi delle *trame* della matrice.</span><span class="sxs-lookup"><span data-stu-id="859e3-123">The **glDeleteTextures** function deletes *n* textures named by the elements of the array *textures*.</span></span> <span data-ttu-id="859e3-124">Una volta eliminata, la trama non presenta alcun contenuto o dimensionalità e il nome è disponibile per il riutilizzo (ad esempio, da **glGenTextures**).</span><span class="sxs-lookup"><span data-stu-id="859e3-124">After a texture is deleted, it has no contents or dimensionality, and its name is free for reuse (for example, by **glGenTextures**).</span></span> <span data-ttu-id="859e3-125">La funzione **glDeleteTextures** ignora gli zeri e i nomi che non corrispondono alle trame esistenti.</span><span class="sxs-lookup"><span data-stu-id="859e3-125">The **glDeleteTextures** function ignores zeros and names that do not correspond to existing textures.</span></span>

<span data-ttu-id="859e3-126">Se una trama attualmente associata viene eliminata, l'associazione viene ripristinata su zero (trama predefinita).</span><span class="sxs-lookup"><span data-stu-id="859e3-126">If a texture that is currently bound is deleted, the binding reverts to zero (the default texture).</span></span>

<span data-ttu-id="859e3-127">Non è possibile includere chiamate a **glDeleteTextures** negli elenchi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="859e3-127">You cannot include calls to **glDeleteTextures** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="859e3-128">La funzione **glDeleteTextures** è disponibile solo in OpenGL versione 1,1 o successiva.</span><span class="sxs-lookup"><span data-stu-id="859e3-128">The **glDeleteTextures** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="859e3-129">La funzione seguente recupera le informazioni correlate a **glDeleteTextures**:</span><span class="sxs-lookup"><span data-stu-id="859e3-129">The following function retrieves information related to **glDeleteTextures**:</span></span>

-   [<span data-ttu-id="859e3-130">**glIsTexture**</span><span class="sxs-lookup"><span data-stu-id="859e3-130">**glIsTexture**</span></span>](glistexture.md)

## <a name="requirements"></a><span data-ttu-id="859e3-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="859e3-131">Requirements</span></span>



| <span data-ttu-id="859e3-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="859e3-132">Requirement</span></span> | <span data-ttu-id="859e3-133">Valore</span><span class="sxs-lookup"><span data-stu-id="859e3-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="859e3-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="859e3-134">Minimum supported client</span></span><br/> | <span data-ttu-id="859e3-135">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="859e3-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="859e3-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="859e3-136">Minimum supported server</span></span><br/> | <span data-ttu-id="859e3-137">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="859e3-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="859e3-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="859e3-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="859e3-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="859e3-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="859e3-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="859e3-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="859e3-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="859e3-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="859e3-142">DLL</span><span class="sxs-lookup"><span data-stu-id="859e3-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="859e3-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="859e3-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="859e3-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="859e3-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="859e3-145">**glAreTexturesResident**</span><span class="sxs-lookup"><span data-stu-id="859e3-145">**glAreTexturesResident**</span></span>](glaretexturesresident.md)
</dt> <dt>

[<span data-ttu-id="859e3-146">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="859e3-146">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="859e3-147">**glBindTexture**</span><span class="sxs-lookup"><span data-stu-id="859e3-147">**glBindTexture**</span></span>](glbindtexture.md)
</dt> <dt>

[<span data-ttu-id="859e3-148">**Remo**</span><span class="sxs-lookup"><span data-stu-id="859e3-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="859e3-149">**glGenTextures**</span><span class="sxs-lookup"><span data-stu-id="859e3-149">**glGenTextures**</span></span>](glgentextures.md)
</dt> <dt>

[<span data-ttu-id="859e3-150">**glGet**</span><span class="sxs-lookup"><span data-stu-id="859e3-150">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="859e3-151">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="859e3-151">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="859e3-152">**glIsTexture**</span><span class="sxs-lookup"><span data-stu-id="859e3-152">**glIsTexture**</span></span>](glistexture.md)
</dt> <dt>

[<span data-ttu-id="859e3-153">**glPrioritizeTextures**</span><span class="sxs-lookup"><span data-stu-id="859e3-153">**glPrioritizeTextures**</span></span>](glprioritizetextures.md)
</dt> <dt>

[<span data-ttu-id="859e3-154">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="859e3-154">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="859e3-155">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="859e3-155">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="859e3-156">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="859e3-156">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="859e3-157">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="859e3-157">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





