---
title: funzione glGenTextures (GL. h)
description: La funzione glGenTextures genera nomi di trama.
ms.assetid: f2491faf-2b33-4b06-9a9f-51ac295690fb
keywords:
- funzione glGenTextures OpenGL
topic_type:
- apiref
api_name:
- glGenTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 204a5d4fb736a88cf615577f4c740cde15d75829
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964832"
---
# <a name="glgentextures-function"></a><span data-ttu-id="a7b72-104">glGenTextures (funzione)</span><span class="sxs-lookup"><span data-stu-id="a7b72-104">glGenTextures function</span></span>

<span data-ttu-id="a7b72-105">La funzione **glGenTextures** genera nomi di trama.</span><span class="sxs-lookup"><span data-stu-id="a7b72-105">The **glGenTextures** function generates texture names.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7b72-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a7b72-106">Syntax</span></span>


```C++
void WINAPI glGenTextures(
   GLsizei n,
   GLuint  *textures
);
```



## <a name="parameters"></a><span data-ttu-id="a7b72-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="a7b72-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7b72-108">*n*</span><span class="sxs-lookup"><span data-stu-id="a7b72-108">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="a7b72-109">Numero di nomi di trama da generare.</span><span class="sxs-lookup"><span data-stu-id="a7b72-109">The number of texture names to be generated.</span></span>

</dd> <dt>

<span data-ttu-id="a7b72-110">*trame*</span><span class="sxs-lookup"><span data-stu-id="a7b72-110">*textures*</span></span> 
</dt> <dd>

<span data-ttu-id="a7b72-111">Puntatore al primo elemento di una matrice in cui sono archiviati i nomi delle trame generate.</span><span class="sxs-lookup"><span data-stu-id="a7b72-111">A pointer to the first element of an array in which the generated texture names are stored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7b72-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a7b72-112">Return value</span></span>

<span data-ttu-id="a7b72-113">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="a7b72-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a7b72-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="a7b72-114">Error codes</span></span>

<span data-ttu-id="a7b72-115">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="a7b72-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="a7b72-116">Nome</span><span class="sxs-lookup"><span data-stu-id="a7b72-116">Name</span></span>                                                                                                  | <span data-ttu-id="a7b72-117">Significato</span><span class="sxs-lookup"><span data-stu-id="a7b72-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a7b72-118"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a7b72-118"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="a7b72-119">*n* è un valore negativo.</span><span class="sxs-lookup"><span data-stu-id="a7b72-119">*n* was a negative value.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="a7b72-120"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a7b72-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="a7b72-121">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="a7b72-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a7b72-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="a7b72-122">Remarks</span></span>

<span data-ttu-id="a7b72-123">La funzione **glGenTextures** restituisce *n* nomi di trama nel parametro *Textures* .</span><span class="sxs-lookup"><span data-stu-id="a7b72-123">The **glGenTextures** function returns *n* texture names in the *textures* parameter.</span></span> <span data-ttu-id="a7b72-124">I nomi di trama non sono necessariamente un set contiguo di Integer, tuttavia nessuno dei nomi restituiti può essere in uso immediatamente prima di chiamare la funzione **glGenTextures** .</span><span class="sxs-lookup"><span data-stu-id="a7b72-124">The texture names are not necessarily a contiguous set of integers, however, none of the returned names can have been in use immediately prior to calling the **glGenTextures** function.</span></span> <span data-ttu-id="a7b72-125">Le trame generate presuppongono la dimensionalità della destinazione della trama a cui sono associate per la prima volta con la funzione [**glBindTexture**](glbindtexture.md) .</span><span class="sxs-lookup"><span data-stu-id="a7b72-125">The generated textures assume the dimensionality of the texture target to which they are first bound with the [**glBindTexture**](glbindtexture.md) function.</span></span> <span data-ttu-id="a7b72-126">I nomi di trama restituiti da **glGenTextures** non vengono restituiti dalle chiamate successive a **glGenTextures** a meno che non vengano eliminati per la prima volta chiamando [**glDeleteTextures**](gldeletetextures.md).</span><span class="sxs-lookup"><span data-stu-id="a7b72-126">Texture names returned by **glGenTextures** are not returned by subsequent calls to **glGenTextures** unless they are first deleted by calling [**glDeleteTextures**](gldeletetextures.md).</span></span>

<span data-ttu-id="a7b72-127">Non è possibile includere **glGenTextures** negli elenchi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="a7b72-127">You cannot include **glGenTextures** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="a7b72-128">La funzione **glGenTextures** è disponibile solo in OpenGL versione 1,1 o successiva.</span><span class="sxs-lookup"><span data-stu-id="a7b72-128">The **glGenTextures** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="a7b72-129">La funzione seguente recupera le informazioni correlate a **glGenTextures**:</span><span class="sxs-lookup"><span data-stu-id="a7b72-129">The following function retrieves information related to **glGenTextures**:</span></span>

-   [<span data-ttu-id="a7b72-130">**glIsTexture**</span><span class="sxs-lookup"><span data-stu-id="a7b72-130">**glIsTexture**</span></span>](glistexture.md)

## <a name="requirements"></a><span data-ttu-id="a7b72-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a7b72-131">Requirements</span></span>



| <span data-ttu-id="a7b72-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7b72-132">Requirement</span></span> | <span data-ttu-id="a7b72-133">Valore</span><span class="sxs-lookup"><span data-stu-id="a7b72-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7b72-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7b72-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a7b72-135">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a7b72-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a7b72-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7b72-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a7b72-137">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a7b72-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a7b72-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a7b72-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7b72-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7b72-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a7b72-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="a7b72-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="a7b72-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a7b72-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a7b72-142">DLL</span><span class="sxs-lookup"><span data-stu-id="a7b72-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7b72-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7b72-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7b72-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a7b72-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7b72-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a7b72-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a7b72-146">**glBindTexture**</span><span class="sxs-lookup"><span data-stu-id="a7b72-146">**glBindTexture**</span></span>](glbindtexture.md)
</dt> <dt>

[<span data-ttu-id="a7b72-147">**glDeleteTextures**</span><span class="sxs-lookup"><span data-stu-id="a7b72-147">**glDeleteTextures**</span></span>](gldeletetextures.md)
</dt> <dt>

[<span data-ttu-id="a7b72-148">**Remo**</span><span class="sxs-lookup"><span data-stu-id="a7b72-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a7b72-149">**glGet**</span><span class="sxs-lookup"><span data-stu-id="a7b72-149">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="a7b72-150">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="a7b72-150">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="a7b72-151">**glIsTexture**</span><span class="sxs-lookup"><span data-stu-id="a7b72-151">**glIsTexture**</span></span>](glistexture.md)
</dt> <dt>

[<span data-ttu-id="a7b72-152">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="a7b72-152">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="a7b72-153">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="a7b72-153">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="a7b72-154">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="a7b72-154">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





