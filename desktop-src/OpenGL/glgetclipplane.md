---
title: funzione glGetClipPlane (GL. h)
description: La funzione glGetClipPlane restituisce i coefficienti del piano di ritaglio specificato.
ms.assetid: 8ff5ee0a-95c1-4321-8aa8-3d9d144d1ef6
keywords:
- funzione glGetClipPlane OpenGL
topic_type:
- apiref
api_name:
- glGetClipPlane
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b3e29d730c09bcc7c2b12082116e174cb39eb74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302762"
---
# <a name="glgetclipplane-function"></a><span data-ttu-id="263e0-104">glGetClipPlane (funzione)</span><span class="sxs-lookup"><span data-stu-id="263e0-104">glGetClipPlane function</span></span>

<span data-ttu-id="263e0-105">La funzione **glGetClipPlane** restituisce i coefficienti del piano di ritaglio specificato.</span><span class="sxs-lookup"><span data-stu-id="263e0-105">The **glGetClipPlane** function returns the coefficients of the specified clipping plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="263e0-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="263e0-106">Syntax</span></span>


```C++
void WINAPI glGetClipPlane(
   GLenum   plane,
   GLdouble *equation
);
```



## <a name="parameters"></a><span data-ttu-id="263e0-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="263e0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="263e0-108">*aereo*</span><span class="sxs-lookup"><span data-stu-id="263e0-108">*plane*</span></span> 
</dt> <dd>

<span data-ttu-id="263e0-109">Un piano di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="263e0-109">A clipping plane.</span></span> <span data-ttu-id="263e0-110">Il numero di piani di ritaglio dipende dall'implementazione, ma sono supportati almeno sei piani di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="263e0-110">The number of clipping planes depends on the implementation, but at least six clipping planes are supported.</span></span> <span data-ttu-id="263e0-111">Sono identificati da nomi simbolici del formato GL \_ clip \_ plane *i* dove 0 = *i* < i \_ \_ piani di ritaglio GL Max \_ .</span><span class="sxs-lookup"><span data-stu-id="263e0-111">They are identified by symbolic names of the form GL\_CLIP\_PLANE *i* where 0 = *i* < GL\_MAX\_CLIP\_PLANES.</span></span>

</dd> <dt>

<span data-ttu-id="263e0-112">*equazione*</span><span class="sxs-lookup"><span data-stu-id="263e0-112">*equation*</span></span> 
</dt> <dd>

<span data-ttu-id="263e0-113">Restituisce quattro valori a precisione doppia che corrispondono ai coefficienti *dell'equazione del piano delle coordinate* oculari.</span><span class="sxs-lookup"><span data-stu-id="263e0-113">Returns four double-precision values that are the coefficients of the plane equation of *plane* in eye coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="263e0-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="263e0-114">Return value</span></span>

<span data-ttu-id="263e0-115">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="263e0-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="263e0-116">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="263e0-116">Error codes</span></span>

<span data-ttu-id="263e0-117">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="263e0-117">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="263e0-118">Nome</span><span class="sxs-lookup"><span data-stu-id="263e0-118">Name</span></span>                                                                                                  | <span data-ttu-id="263e0-119">Significato</span><span class="sxs-lookup"><span data-stu-id="263e0-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="263e0-120"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="263e0-120"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="263e0-121">il *piano* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="263e0-121">*plane* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="263e0-122"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="263e0-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="263e0-123">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="263e0-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="263e0-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="263e0-124">Remarks</span></span>

<span data-ttu-id="263e0-125">La funzione **glGetClipPlane** restituisce in *equazione* i quattro coefficienti dell'equazione del piano per il *piano*.</span><span class="sxs-lookup"><span data-stu-id="263e0-125">The **glGetClipPlane** function returns in *equation* the four coefficients of the plane equation for *plane*.</span></span>

<span data-ttu-id="263e0-126">È sempre il caso GL \_ clip \_ plane *i* = GL \_ clip \_ PLANE0 + *i*.</span><span class="sxs-lookup"><span data-stu-id="263e0-126">It is always the case that GL\_CLIP\_PLANE *i* = GL\_CLIP\_PLANE0 + *i*.</span></span>

<span data-ttu-id="263e0-127">Se viene generato un errore, non viene apportata alcuna modifica al contenuto dell' *equazione*.</span><span class="sxs-lookup"><span data-stu-id="263e0-127">If an error is generated, no change is made to the contents of *equation*.</span></span>

## <a name="requirements"></a><span data-ttu-id="263e0-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="263e0-128">Requirements</span></span>



| <span data-ttu-id="263e0-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="263e0-129">Requirement</span></span> | <span data-ttu-id="263e0-130">Valore</span><span class="sxs-lookup"><span data-stu-id="263e0-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="263e0-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="263e0-131">Minimum supported client</span></span><br/> | <span data-ttu-id="263e0-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="263e0-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="263e0-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="263e0-133">Minimum supported server</span></span><br/> | <span data-ttu-id="263e0-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="263e0-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="263e0-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="263e0-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="263e0-136"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="263e0-136"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="263e0-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="263e0-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="263e0-138"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="263e0-138"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="263e0-139">DLL</span><span class="sxs-lookup"><span data-stu-id="263e0-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="263e0-140"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="263e0-140"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="263e0-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="263e0-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="263e0-142">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="263e0-142">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="263e0-143">**glClipPlane**</span><span class="sxs-lookup"><span data-stu-id="263e0-143">**glClipPlane**</span></span>](glclipplane.md)
</dt> <dt>

[<span data-ttu-id="263e0-144">**Remo**</span><span class="sxs-lookup"><span data-stu-id="263e0-144">**glEnd**</span></span>](glend.md)
</dt> </dl>

 

 





