---
title: funzione glDepthMask (GL. h)
description: La funzione glDepthMask Abilita o Disabilita la scrittura nel buffer di profondità.
ms.assetid: 067b18e2-f21a-4dde-8fa6-dd975746e189
keywords:
- funzione glDepthMask OpenGL
topic_type:
- apiref
api_name:
- glDepthMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5873d517770f1ce61f9a2eaad3ea7cce7b4fd7ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400703"
---
# <a name="gldepthmask-function"></a><span data-ttu-id="00b0c-104">glDepthMask (funzione)</span><span class="sxs-lookup"><span data-stu-id="00b0c-104">glDepthMask function</span></span>

<span data-ttu-id="00b0c-105">La funzione **glDepthMask** Abilita o Disabilita la scrittura nel buffer di profondità.</span><span class="sxs-lookup"><span data-stu-id="00b0c-105">The **glDepthMask** function enables or disables writing into the depth buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="00b0c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="00b0c-106">Syntax</span></span>


```C++
void WINAPI glDepthMask(
   GLboolean flag
);
```



## <a name="parameters"></a><span data-ttu-id="00b0c-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="00b0c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00b0c-108">*flag*</span><span class="sxs-lookup"><span data-stu-id="00b0c-108">*flag*</span></span> 
</dt> <dd>

<span data-ttu-id="00b0c-109">Specifica se il buffer di profondità è abilitato per la scrittura.</span><span class="sxs-lookup"><span data-stu-id="00b0c-109">Specifies whether the depth buffer is enabled for writing.</span></span> <span data-ttu-id="00b0c-110">Se il *flag* è zero, la scrittura nel buffer di profondità è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="00b0c-110">If *flag* is zero, depth-buffer writing is disabled.</span></span> <span data-ttu-id="00b0c-111">In caso contrario, è abilitato.</span><span class="sxs-lookup"><span data-stu-id="00b0c-111">Otherwise, it is enabled.</span></span> <span data-ttu-id="00b0c-112">Inizialmente, la scrittura nel buffer di profondità è abilitata.</span><span class="sxs-lookup"><span data-stu-id="00b0c-112">Initially, depth-buffer writing is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00b0c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="00b0c-113">Return value</span></span>

<span data-ttu-id="00b0c-114">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="00b0c-114">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="00b0c-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="00b0c-115">Error codes</span></span>

<span data-ttu-id="00b0c-116">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="00b0c-116">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="00b0c-117">Nome</span><span class="sxs-lookup"><span data-stu-id="00b0c-117">Name</span></span>                                                                                                  | <span data-ttu-id="00b0c-118">Significato</span><span class="sxs-lookup"><span data-stu-id="00b0c-118">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="00b0c-119"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="00b0c-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="00b0c-120">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="00b0c-120">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="00b0c-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="00b0c-121">Remarks</span></span>

<span data-ttu-id="00b0c-122">La funzione seguente recupera le informazioni correlate a **glDepthMask**:</span><span class="sxs-lookup"><span data-stu-id="00b0c-122">The following function retrieves information related to **glDepthMask**:</span></span>

<span data-ttu-id="00b0c-123">**glGet** con argomento di \_ profondità GL \_ WRITEMASK</span><span class="sxs-lookup"><span data-stu-id="00b0c-123">**glGet** with argument GL\_DEPTH\_WRITEMASK</span></span>

## <a name="requirements"></a><span data-ttu-id="00b0c-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00b0c-124">Requirements</span></span>



| <span data-ttu-id="00b0c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="00b0c-125">Requirement</span></span> | <span data-ttu-id="00b0c-126">Valore</span><span class="sxs-lookup"><span data-stu-id="00b0c-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="00b0c-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00b0c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="00b0c-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="00b0c-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="00b0c-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00b0c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="00b0c-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="00b0c-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="00b0c-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="00b0c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="00b0c-132"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="00b0c-132"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="00b0c-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="00b0c-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="00b0c-134"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00b0c-134"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="00b0c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="00b0c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00b0c-136"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00b0c-136"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00b0c-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="00b0c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00b0c-138">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="00b0c-138">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="00b0c-139">**glColorMask**</span><span class="sxs-lookup"><span data-stu-id="00b0c-139">**glColorMask**</span></span>](glcolormask.md)
</dt> <dt>

[<span data-ttu-id="00b0c-140">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="00b0c-140">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="00b0c-141">**glDepthRange**</span><span class="sxs-lookup"><span data-stu-id="00b0c-141">**glDepthRange**</span></span>](gldepthrange.md)
</dt> <dt>

[<span data-ttu-id="00b0c-142">**Remo**</span><span class="sxs-lookup"><span data-stu-id="00b0c-142">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="00b0c-143">**glGet**</span><span class="sxs-lookup"><span data-stu-id="00b0c-143">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="00b0c-144">**glIndexMask**</span><span class="sxs-lookup"><span data-stu-id="00b0c-144">**glIndexMask**</span></span>](glindexmask.md)
</dt> <dt>

[<span data-ttu-id="00b0c-145">**glStencilMask**</span><span class="sxs-lookup"><span data-stu-id="00b0c-145">**glStencilMask**</span></span>](glstencilmask.md)
</dt> </dl>

 

 





