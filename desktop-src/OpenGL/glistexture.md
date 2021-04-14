---
title: funzione glIsTexture (GL. h)
description: La funzione glIsTexture determina se un nome corrisponde a una trama.
ms.assetid: 89d06642-ff28-4a67-ac7f-ca58150f301e
keywords:
- funzione glIsTexture OpenGL
topic_type:
- apiref
api_name:
- glIsTexture
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8897cc0eb004da701f28b410f2ca28b6194c9d26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478712"
---
# <a name="glistexture-function"></a><span data-ttu-id="8fc51-104">glIsTexture (funzione)</span><span class="sxs-lookup"><span data-stu-id="8fc51-104">glIsTexture function</span></span>

<span data-ttu-id="8fc51-105">La funzione **glIsTexture** determina se un nome corrisponde a una trama.</span><span class="sxs-lookup"><span data-stu-id="8fc51-105">The **glIsTexture** function determines if a name corresponds to a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fc51-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8fc51-106">Syntax</span></span>


```C++
GLboolean WINAPI glIsTexture(
   GLuint texture
);
```



## <a name="parameters"></a><span data-ttu-id="8fc51-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="8fc51-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fc51-108">*trama*</span><span class="sxs-lookup"><span data-stu-id="8fc51-108">*texture*</span></span> 
</dt> <dd>

<span data-ttu-id="8fc51-109">Valore che rappresenta il nome di una trama.</span><span class="sxs-lookup"><span data-stu-id="8fc51-109">A value that is the name of a texture.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="8fc51-110">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="8fc51-110">Error codes</span></span>

<span data-ttu-id="8fc51-111">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="8fc51-111">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="8fc51-112">Nome</span><span class="sxs-lookup"><span data-stu-id="8fc51-112">Name</span></span>                                                                                                  | <span data-ttu-id="8fc51-113">Significato</span><span class="sxs-lookup"><span data-stu-id="8fc51-113">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8fc51-114"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8fc51-114"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="8fc51-115">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="8fc51-115">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8fc51-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="8fc51-116">Remarks</span></span>

<span data-ttu-id="8fc51-117">Se il parametro *texture* è attualmente il nome di una trama, la funzione **glIsTexture** restituisce GL \_ true.</span><span class="sxs-lookup"><span data-stu-id="8fc51-117">If the *texture* parameter is currently the name of a texture, the **glIsTexture** function returns GL\_TRUE.</span></span> <span data-ttu-id="8fc51-118">La funzione **glIsTexture** restituisce GL \_ false se *texture* è zero.</span><span class="sxs-lookup"><span data-stu-id="8fc51-118">The **glIsTexture** function returns GL\_FALSE if *texture* is zero.</span></span> <span data-ttu-id="8fc51-119">Restituisce anche GL \_ false se è un valore diverso da zero che non è attualmente il nome di una trama o se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="8fc51-119">It also returns GL\_FALSE if it is a non-zero value that is not currently the name of a texture, or if an error occurs.</span></span>

<span data-ttu-id="8fc51-120">Non è possibile includere chiamate a **glIsTexture** negli elenchi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8fc51-120">You cannot include calls to **glIsTexture** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="8fc51-121">La funzione **glIsTexture** è disponibile solo in OpenGL versione 1,1 o successiva.</span><span class="sxs-lookup"><span data-stu-id="8fc51-121">The **glIsTexture** function is only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8fc51-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8fc51-122">Requirements</span></span>



| <span data-ttu-id="8fc51-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fc51-123">Requirement</span></span> | <span data-ttu-id="8fc51-124">Valore</span><span class="sxs-lookup"><span data-stu-id="8fc51-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8fc51-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8fc51-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8fc51-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8fc51-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8fc51-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8fc51-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8fc51-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8fc51-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8fc51-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8fc51-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fc51-130"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fc51-130"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="8fc51-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="8fc51-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="8fc51-132"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8fc51-132"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8fc51-133">DLL</span><span class="sxs-lookup"><span data-stu-id="8fc51-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fc51-134"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fc51-134"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fc51-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8fc51-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fc51-136">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="8fc51-136">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="8fc51-137">**glBindTexture**</span><span class="sxs-lookup"><span data-stu-id="8fc51-137">**glBindTexture**</span></span>](glbindtexture.md)
</dt> <dt>

[<span data-ttu-id="8fc51-138">**Remo**</span><span class="sxs-lookup"><span data-stu-id="8fc51-138">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="8fc51-139">**glGenTextures**</span><span class="sxs-lookup"><span data-stu-id="8fc51-139">**glGenTextures**</span></span>](glgentextures.md)
</dt> <dt>

[<span data-ttu-id="8fc51-140">**glGet**</span><span class="sxs-lookup"><span data-stu-id="8fc51-140">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="8fc51-141">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="8fc51-141">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="8fc51-142">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="8fc51-142">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="8fc51-143">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="8fc51-143">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="8fc51-144">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="8fc51-144">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





