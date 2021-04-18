---
title: funzione glGetTexEnviv (GL. h)
description: Le funzioni glGetTexEnvfv e glGetTexEnviv restituiscono parametri di ambiente di trama. | funzione glGetTexEnviv (GL. h)
ms.assetid: c1429cb9-4392-41ef-a978-a51db66445f2
keywords:
- funzione glGetTexEnviv OpenGL
topic_type:
- apiref
api_name:
- glGetTexEnviv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ff222b7de0bfcd5fa50e9fa5f260e329c60c69d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321409"
---
# <a name="glgettexenviv-function"></a><span data-ttu-id="7bbf2-105">glGetTexEnviv (funzione)</span><span class="sxs-lookup"><span data-stu-id="7bbf2-105">glGetTexEnviv function</span></span>

<span data-ttu-id="7bbf2-106">Le funzioni [**glGetTexEnvfv**](glgettexenvfv.md) e **glGetTexEnviv** restituiscono parametri di ambiente di trama.</span><span class="sxs-lookup"><span data-stu-id="7bbf2-106">The [**glGetTexEnvfv**](glgettexenvfv.md) and **glGetTexEnviv** functions return texture environment parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bbf2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7bbf2-107">Syntax</span></span>


```C++
void WINAPI glGetTexEnviv(
   GLenum target,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="7bbf2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7bbf2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bbf2-109">*target*</span><span class="sxs-lookup"><span data-stu-id="7bbf2-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="7bbf2-110">Ambiente di trama.</span><span class="sxs-lookup"><span data-stu-id="7bbf2-110">A texture environment.</span></span> <span data-ttu-id="7bbf2-111">Deve essere una \_ trama GL \_ env.</span><span class="sxs-lookup"><span data-stu-id="7bbf2-111">Must be GL\_TEXTURE\_ENV.</span></span>

</dd> <dt>

<span data-ttu-id="7bbf2-112">*pname*</span><span class="sxs-lookup"><span data-stu-id="7bbf2-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="7bbf2-113">Nome simbolico di un parametro dell'ambiente di trama.</span><span class="sxs-lookup"><span data-stu-id="7bbf2-113">The symbolic name of a texture environment parameter.</span></span> <span data-ttu-id="7bbf2-114">Vengono accettati i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="7bbf2-114">The following values are accepted.</span></span>



| <span data-ttu-id="7bbf2-115">Valore</span><span class="sxs-lookup"><span data-stu-id="7bbf2-115">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="7bbf2-116">Significato</span><span class="sxs-lookup"><span data-stu-id="7bbf2-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span><dl> <span data-ttu-id="7bbf2-117"><dt>**\_ \_ modalità ENV trama \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="7bbf2-117"><dt>**GL\_TEXTURE\_ENV\_MODE**</dt></span></span> </dl>    | <span data-ttu-id="7bbf2-118">Il parametro *params* restituisce la modalità dell'ambiente di trama a valore singolo, una costante simbolica.</span><span class="sxs-lookup"><span data-stu-id="7bbf2-118">The *params* parameter returns the single-valued texture environment mode, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                           |
| <span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span><dl> <span data-ttu-id="7bbf2-119"><dt>**\_ \_ colore ENV trama \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="7bbf2-119"><dt>**GL\_TEXTURE\_ENV\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="7bbf2-120">Il parametro *params* restituisce quattro valori integer o a virgola mobile che corrispondono al colore dell'ambiente di trama.</span><span class="sxs-lookup"><span data-stu-id="7bbf2-120">The *params* parameter returns four integer or floating-point values that are the texture environment color.</span></span> <span data-ttu-id="7bbf2-121">I valori integer, se richiesti, vengono mappati linearmente dalla rappresentazione a virgola mobile interna, in modo che 1,0 sia mappato al numero intero rappresentabile più positivo e-1,0 sia mappato al numero intero rappresentabile più negativo.</span><span class="sxs-lookup"><span data-stu-id="7bbf2-121">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer, and -1.0 maps to the most negative representable integer.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7bbf2-122">*params*</span><span class="sxs-lookup"><span data-stu-id="7bbf2-122">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="7bbf2-123">Restituisce i dati richiesti.</span><span class="sxs-lookup"><span data-stu-id="7bbf2-123">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7bbf2-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7bbf2-124">Return value</span></span>

<span data-ttu-id="7bbf2-125">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="7bbf2-125">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7bbf2-126">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="7bbf2-126">Error codes</span></span>

<span data-ttu-id="7bbf2-127">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="7bbf2-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="7bbf2-128">Nome</span><span class="sxs-lookup"><span data-stu-id="7bbf2-128">Name</span></span>                                                                                                  | <span data-ttu-id="7bbf2-129">Significato</span><span class="sxs-lookup"><span data-stu-id="7bbf2-129">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7bbf2-130"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7bbf2-130"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="7bbf2-131">*target* o *pname* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="7bbf2-131">*target* or *pname* was not an accepted value.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="7bbf2-132"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7bbf2-132"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="7bbf2-133">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="7bbf2-133">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7bbf2-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="7bbf2-134">Remarks</span></span>

<span data-ttu-id="7bbf2-135">La funzione **glGetTexEnv** restituisce i valori selezionati dei *params* di un ambiente di trama specificato con [**glTexEnv**](gltexenv-functions.md).</span><span class="sxs-lookup"><span data-stu-id="7bbf2-135">The **glGetTexEnv** function returns in *params* selected values of a texture environment that was specified with [**glTexEnv**](gltexenv-functions.md).</span></span> <span data-ttu-id="7bbf2-136">Il parametro *target* specifica un ambiente di trama.</span><span class="sxs-lookup"><span data-stu-id="7bbf2-136">The *target* parameter specifies a texture environment.</span></span> <span data-ttu-id="7bbf2-137">Attualmente, viene definito e supportato un solo ambiente di trama: GL \_ texture \_ env.</span><span class="sxs-lookup"><span data-stu-id="7bbf2-137">Currently, only one texture environment is defined and supported: GL\_TEXTURE\_ENV.</span></span>

<span data-ttu-id="7bbf2-138">Il parametro *pname* assegna un nome a un parametro di ambiente di trama specifico.</span><span class="sxs-lookup"><span data-stu-id="7bbf2-138">The *pname* parameter names a specific texture environment parameter.</span></span>

<span data-ttu-id="7bbf2-139">Se viene generato un errore, non viene apportata alcuna modifica al contenuto di *params*.</span><span class="sxs-lookup"><span data-stu-id="7bbf2-139">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bbf2-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7bbf2-140">Requirements</span></span>



| <span data-ttu-id="7bbf2-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bbf2-141">Requirement</span></span> | <span data-ttu-id="7bbf2-142">Valore</span><span class="sxs-lookup"><span data-stu-id="7bbf2-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7bbf2-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7bbf2-143">Minimum supported client</span></span><br/> | <span data-ttu-id="7bbf2-144">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7bbf2-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7bbf2-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7bbf2-145">Minimum supported server</span></span><br/> | <span data-ttu-id="7bbf2-146">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7bbf2-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7bbf2-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7bbf2-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="7bbf2-148"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="7bbf2-148"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="7bbf2-149">Libreria</span><span class="sxs-lookup"><span data-stu-id="7bbf2-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="7bbf2-150"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7bbf2-150"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7bbf2-151">DLL</span><span class="sxs-lookup"><span data-stu-id="7bbf2-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7bbf2-152"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7bbf2-152"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bbf2-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7bbf2-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bbf2-154">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="7bbf2-154">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="7bbf2-155">**Remo**</span><span class="sxs-lookup"><span data-stu-id="7bbf2-155">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="7bbf2-156">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="7bbf2-156">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> </dl>

 

 





