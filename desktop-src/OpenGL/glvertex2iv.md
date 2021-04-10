---
title: funzione glVertex2iv (GL. h)
description: Specifica un vertice. | funzione glVertex2iv (GL. h)
ms.assetid: 3b88bf7d-5743-4ac0-a79f-5f450b488bd2
keywords:
- funzione glVertex2iv OpenGL
topic_type:
- apiref
api_name:
- glVertex2iv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 594c50ff1e30184d5a7292c5b639f16a48f0820b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104058562"
---
# <a name="glvertex2iv-function"></a><span data-ttu-id="fa66c-105">glVertex2iv (funzione)</span><span class="sxs-lookup"><span data-stu-id="fa66c-105">glVertex2iv function</span></span>

<span data-ttu-id="fa66c-106">Specifica un vertice.</span><span class="sxs-lookup"><span data-stu-id="fa66c-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa66c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fa66c-107">Syntax</span></span>


```C++
void WINAPI glVertex2iv(
   const GLint *v
);
```



## <a name="parameters"></a><span data-ttu-id="fa66c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fa66c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa66c-109">*v*</span><span class="sxs-lookup"><span data-stu-id="fa66c-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="fa66c-110">Puntatore a una matrice di due elementi.</span><span class="sxs-lookup"><span data-stu-id="fa66c-110">A pointer to an array of two elements.</span></span> <span data-ttu-id="fa66c-111">Gli elementi sono le coordinate x e y di un vertice.</span><span class="sxs-lookup"><span data-stu-id="fa66c-111">The elements are the x and y coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa66c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fa66c-112">Return value</span></span>

<span data-ttu-id="fa66c-113">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="fa66c-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa66c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fa66c-114">Requirements</span></span>



| <span data-ttu-id="fa66c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa66c-115">Requirement</span></span> | <span data-ttu-id="fa66c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="fa66c-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa66c-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa66c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fa66c-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fa66c-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fa66c-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa66c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fa66c-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fa66c-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fa66c-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fa66c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa66c-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa66c-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="fa66c-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="fa66c-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="fa66c-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa66c-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="fa66c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="fa66c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa66c-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa66c-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa66c-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fa66c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa66c-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="fa66c-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="fa66c-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="fa66c-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="fa66c-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="fa66c-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="fa66c-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="fa66c-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="fa66c-132">**Remo**</span><span class="sxs-lookup"><span data-stu-id="fa66c-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="fa66c-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="fa66c-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="fa66c-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="fa66c-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="fa66c-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="fa66c-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="fa66c-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="fa66c-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="fa66c-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="fa66c-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="fa66c-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="fa66c-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





