---
title: funzione glAreTexturesResident (GL. h)
description: La funzione glAreTexturesResident determina se gli oggetti di trama specificati sono residenti nella memoria della trama.
ms.assetid: 55d068a8-d366-4fee-85d5-49373b8c5e02
keywords:
- funzione glAreTexturesResident OpenGL
topic_type:
- apiref
api_name:
- glAreTexturesResident
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e2e7e5965da9604c690384301de6f1879a98994
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301805"
---
# <a name="glaretexturesresident-function"></a><span data-ttu-id="843d4-104">glAreTexturesResident (funzione)</span><span class="sxs-lookup"><span data-stu-id="843d4-104">glAreTexturesResident function</span></span>

<span data-ttu-id="843d4-105">La funzione **glAreTexturesResident** determina se gli oggetti di trama specificati sono residenti nella memoria della trama.</span><span class="sxs-lookup"><span data-stu-id="843d4-105">The **glAreTexturesResident** function determines whether specified texture objects are resident in texture memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="843d4-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="843d4-106">Syntax</span></span>


```C++
GLboolean WINAPI glAreTexturesResident(
         GLsizei   n,
   const GLuint    *textures,
         GLboolean *residences
);
```



## <a name="parameters"></a><span data-ttu-id="843d4-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="843d4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="843d4-108">*n*</span><span class="sxs-lookup"><span data-stu-id="843d4-108">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="843d4-109">Numero di trame su cui eseguire la query.</span><span class="sxs-lookup"><span data-stu-id="843d4-109">The number of textures to be queried.</span></span>

</dd> <dt>

<span data-ttu-id="843d4-110">*trame*</span><span class="sxs-lookup"><span data-stu-id="843d4-110">*textures*</span></span> 
</dt> <dd>

<span data-ttu-id="843d4-111">Indirizzo di una matrice contenente i nomi delle trame su cui eseguire la query.</span><span class="sxs-lookup"><span data-stu-id="843d4-111">The address of an array containing the names of the textures to be queried.</span></span>

</dd> <dt>

<span data-ttu-id="843d4-112">*Residenze*</span><span class="sxs-lookup"><span data-stu-id="843d4-112">*residences*</span></span> 
</dt> <dd>

<span data-ttu-id="843d4-113">Indirizzo di una matrice in cui viene restituito lo stato della residenza della trama.</span><span class="sxs-lookup"><span data-stu-id="843d4-113">The address of an array in which the texture residence status is returned.</span></span> <span data-ttu-id="843d4-114">Lo stato di residenza di una trama denominata da un elemento di *trame* viene restituito nell'elemento corrispondente di *Residences*.</span><span class="sxs-lookup"><span data-stu-id="843d4-114">The residence status of a texture named by an element of *textures* is returned in the corresponding element of *residences*.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="843d4-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="843d4-115">Error codes</span></span>

<span data-ttu-id="843d4-116">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="843d4-116">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="843d4-117">Nome</span><span class="sxs-lookup"><span data-stu-id="843d4-117">Name</span></span>                                                                                                  | <span data-ttu-id="843d4-118">Significato</span><span class="sxs-lookup"><span data-stu-id="843d4-118">Meaning</span></span>                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="843d4-119"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="843d4-119"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="843d4-120">*n* è un valore negativo, un elemento nelle *trame* è zero oppure un elemento nelle *trame* non contiene un identificatore di trama.</span><span class="sxs-lookup"><span data-stu-id="843d4-120">*n* was a negative value, an element in *textures* was zero, or an element in *textures* did not contain a texture identifier.</span></span><br/> |
| <dl> <span data-ttu-id="843d4-121"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="843d4-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="843d4-122">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="843d4-122">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>     |



## <a name="remarks"></a><span data-ttu-id="843d4-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="843d4-123">Remarks</span></span>

<span data-ttu-id="843d4-124">Nei computer con una quantità limitata di memoria di trama, OpenGL stabilisce un working set di trame che sono residenti nella memoria della trama.</span><span class="sxs-lookup"><span data-stu-id="843d4-124">On machines with a limited amount of texture memory, OpenGL establishes a working set of textures that are resident in texture memory.</span></span> <span data-ttu-id="843d4-125">Queste trame possono essere associate a una destinazione di trama in modo molto più efficiente rispetto alle trame non residenti.</span><span class="sxs-lookup"><span data-stu-id="843d4-125">These textures can be bound to a texture target much more efficiently than textures that are not resident.</span></span>

<span data-ttu-id="843d4-126">La funzione **glAreTexturesResident** esegue una query sullo stato di residenza della trama delle trame *n* denominate dagli elementi delle *trame*.</span><span class="sxs-lookup"><span data-stu-id="843d4-126">The **glAreTexturesResident** function queries the texture residence status of the *n* textures named by the elements of *textures*.</span></span> <span data-ttu-id="843d4-127">Se tutte le trame denominate sono residenti, **glAreTexturesResident** restituisce GL \_ true e il contenuto delle *residenze* non viene disturbato.</span><span class="sxs-lookup"><span data-stu-id="843d4-127">If all the named textures are resident, **glAreTexturesResident** returns GL\_TRUE, and the contents of *residences* are undisturbed.</span></span> <span data-ttu-id="843d4-128">Se una delle trame denominate non è residente, **glAreTexturesResident** restituisce GL \_ false e viene restituito lo stato dettagliato negli *n* elementi di *Residences*.</span><span class="sxs-lookup"><span data-stu-id="843d4-128">If any of the named textures are not resident, **glAreTexturesResident** returns GL\_FALSE, and detailed status is returned in the *n* elements of *residences*.</span></span>

<span data-ttu-id="843d4-129">Se un elemento di *Residences* è GL \_ true, la trama denominata dall'elemento corrispondente delle *trame* sarà residente nella memoria della trama.</span><span class="sxs-lookup"><span data-stu-id="843d4-129">If an element of *residences* is GL\_TRUE, then the texture named by the corresponding element of *textures* is resident in texture memory.</span></span>

<span data-ttu-id="843d4-130">Per eseguire una query sullo stato di residenza di una singola trama con binding, chiamare [**glGetTexParameter**](glgettexparameter.md) con il parametro di *destinazione* impostato sulla trama di destinazione a cui è associata la destinazione e impostare il parametro *pname* su GL \_ texture \_ Resident.</span><span class="sxs-lookup"><span data-stu-id="843d4-130">To query the residence status of a single bound texture, call [**glGetTexParameter**](glgettexparameter.md) with the *target* parameter set to the target texture to which the target is bound and set the *pname* parameter to GL\_TEXTURE\_RESIDENT.</span></span> <span data-ttu-id="843d4-131">È necessario utilizzare questo metodo per eseguire una query sullo stato residente di una trama predefinita.</span><span class="sxs-lookup"><span data-stu-id="843d4-131">You must use this method to query the resident status of a default texture.</span></span>

<span data-ttu-id="843d4-132">Non è possibile includere **glAreTexturesResident** negli elenchi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="843d4-132">You cannot include **glAreTexturesResident** in display lists.</span></span>

<span data-ttu-id="843d4-133">La funzione **glAreTexturesResident** restituisce lo stato di residenza delle trame al momento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="843d4-133">The **glAreTexturesResident** function returns the residency status of the textures at the time of invocation.</span></span> <span data-ttu-id="843d4-134">Non garantisce che le trame rimangano residenti in qualsiasi altro momento.</span><span class="sxs-lookup"><span data-stu-id="843d4-134">It does not guarantee that the textures will remain resident at any other time.</span></span>

<span data-ttu-id="843d4-135">Se le trame risiedono nella memoria virtuale (non è presente alcuna memoria di trama), vengono considerate sempre residenti.</span><span class="sxs-lookup"><span data-stu-id="843d4-135">If textures reside in virtual memory (there is no texture memory), they are considered always resident.</span></span>

> [!Note]  
> <span data-ttu-id="843d4-136">La funzione **glAreTexturesResident** è disponibile solo in OpenGL versione 1,1 o successiva.</span><span class="sxs-lookup"><span data-stu-id="843d4-136">The **glAreTexturesResident** function is only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="843d4-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="843d4-137">Requirements</span></span>



| <span data-ttu-id="843d4-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="843d4-138">Requirement</span></span> | <span data-ttu-id="843d4-139">Valore</span><span class="sxs-lookup"><span data-stu-id="843d4-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="843d4-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="843d4-140">Minimum supported client</span></span><br/> | <span data-ttu-id="843d4-141">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="843d4-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="843d4-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="843d4-142">Minimum supported server</span></span><br/> | <span data-ttu-id="843d4-143">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="843d4-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="843d4-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="843d4-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="843d4-145"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="843d4-145"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="843d4-146">Libreria</span><span class="sxs-lookup"><span data-stu-id="843d4-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="843d4-147"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="843d4-147"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="843d4-148">DLL</span><span class="sxs-lookup"><span data-stu-id="843d4-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="843d4-149"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="843d4-149"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="843d4-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="843d4-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="843d4-151">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="843d4-151">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="843d4-152">**glBindTexture**</span><span class="sxs-lookup"><span data-stu-id="843d4-152">**glBindTexture**</span></span>](glbindtexture.md)
</dt> <dt>

[<span data-ttu-id="843d4-153">**Remo**</span><span class="sxs-lookup"><span data-stu-id="843d4-153">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="843d4-154">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="843d4-154">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="843d4-155">**glPrioritizeTextures**</span><span class="sxs-lookup"><span data-stu-id="843d4-155">**glPrioritizeTextures**</span></span>](glprioritizetextures.md)
</dt> <dt>

[<span data-ttu-id="843d4-156">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="843d4-156">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="843d4-157">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="843d4-157">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> </dl>

 

 





