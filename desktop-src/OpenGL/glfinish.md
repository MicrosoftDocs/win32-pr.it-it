---
title: funzione glFinish (GL. h)
description: La funzione glFinish si blocca fino al completamento di tutte le esecuzioni di OpenGL.
ms.assetid: 1dcb4767-02ea-41d8-bf1f-d61d20873d4f
keywords:
- funzione glFinish OpenGL
topic_type:
- apiref
api_name:
- glFinish
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4731ffc91dbb8d31137a792b59d3ebc36bb4d5d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519157"
---
# <a name="glfinish-function"></a><span data-ttu-id="f0dfe-104">glFinish (funzione)</span><span class="sxs-lookup"><span data-stu-id="f0dfe-104">glFinish function</span></span>

<span data-ttu-id="f0dfe-105">La funzione **glFinish** si blocca fino al completamento di tutte le esecuzioni di OpenGL.</span><span class="sxs-lookup"><span data-stu-id="f0dfe-105">The **glFinish** function blocks until all OpenGL execution is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0dfe-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f0dfe-106">Syntax</span></span>


```C++
void WINAPI glFinish(void);
```



## <a name="parameters"></a><span data-ttu-id="f0dfe-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f0dfe-107">Parameters</span></span>

<span data-ttu-id="f0dfe-108">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="f0dfe-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f0dfe-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f0dfe-109">Return value</span></span>

<span data-ttu-id="f0dfe-110">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="f0dfe-110">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f0dfe-111">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="f0dfe-111">Error codes</span></span>

<span data-ttu-id="f0dfe-112">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="f0dfe-112">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="f0dfe-113">Nome</span><span class="sxs-lookup"><span data-stu-id="f0dfe-113">Name</span></span>                                                                                                  | <span data-ttu-id="f0dfe-114">Significato</span><span class="sxs-lookup"><span data-stu-id="f0dfe-114">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f0dfe-115"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f0dfe-115"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="f0dfe-116">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="f0dfe-116">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f0dfe-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="f0dfe-117">Remarks</span></span>

<span data-ttu-id="f0dfe-118">La funzione **glFinish** non restituisce alcun risultato finché non vengono completati gli effetti di tutte le funzioni di OpenGL precedentemente chiamate.</span><span class="sxs-lookup"><span data-stu-id="f0dfe-118">The **glFinish** function does not return until the effects of all previously called OpenGL functions are complete.</span></span> <span data-ttu-id="f0dfe-119">Tali effetti includono tutte le modifiche allo stato OpenGL, tutte le modifiche allo stato di connessione e tutte le modifiche apportate al contenuto del framebuffer.</span><span class="sxs-lookup"><span data-stu-id="f0dfe-119">Such effects include all changes to the OpenGL state, all changes to the connection state, and all changes to the framebuffer contents.</span></span>

<span data-ttu-id="f0dfe-120">La funzione **glFinish** richiede un round trip al server.</span><span class="sxs-lookup"><span data-stu-id="f0dfe-120">The **glFinish** function requires a round trip to the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0dfe-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0dfe-121">Requirements</span></span>



| <span data-ttu-id="f0dfe-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0dfe-122">Requirement</span></span> | <span data-ttu-id="f0dfe-123">Valore</span><span class="sxs-lookup"><span data-stu-id="f0dfe-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0dfe-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0dfe-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f0dfe-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f0dfe-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f0dfe-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0dfe-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f0dfe-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f0dfe-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f0dfe-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f0dfe-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0dfe-129"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0dfe-129"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f0dfe-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="f0dfe-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="f0dfe-131"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0dfe-131"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f0dfe-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f0dfe-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0dfe-133"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0dfe-133"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0dfe-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f0dfe-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0dfe-135">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f0dfe-135">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f0dfe-136">**Remo**</span><span class="sxs-lookup"><span data-stu-id="f0dfe-136">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f0dfe-137">**glFlush**</span><span class="sxs-lookup"><span data-stu-id="f0dfe-137">**glFlush**</span></span>](glflush.md)
</dt> </dl>

 

 





