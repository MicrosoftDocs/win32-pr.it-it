---
title: funzione glVertex2sv (GL. h)
description: Specifica un vertice. | funzione glVertex2sv (GL. h)
ms.assetid: 4e13356a-a74b-4fb6-a001-1fffc28dd7a1
keywords:
- funzione glVertex2sv OpenGL
topic_type:
- apiref
api_name:
- glVertex2sv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e865ab8999e08f9c13ad46443ba039be1cda9e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321637"
---
# <a name="glvertex2sv-function"></a><span data-ttu-id="d49cf-105">glVertex2sv (funzione)</span><span class="sxs-lookup"><span data-stu-id="d49cf-105">glVertex2sv function</span></span>

<span data-ttu-id="d49cf-106">Specifica un vertice.</span><span class="sxs-lookup"><span data-stu-id="d49cf-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="d49cf-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d49cf-107">Syntax</span></span>


```C++
void WINAPI glVertex2sv(
   const GLshort *v
);
```



## <a name="parameters"></a><span data-ttu-id="d49cf-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d49cf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d49cf-109">*v*</span><span class="sxs-lookup"><span data-stu-id="d49cf-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="d49cf-110">Puntatore a una matrice di due elementi.</span><span class="sxs-lookup"><span data-stu-id="d49cf-110">A pointer to an array of two elements.</span></span> <span data-ttu-id="d49cf-111">Gli elementi sono le coordinate x e y di un vertice.</span><span class="sxs-lookup"><span data-stu-id="d49cf-111">The elements are the x and y coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d49cf-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d49cf-112">Return value</span></span>

<span data-ttu-id="d49cf-113">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="d49cf-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d49cf-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d49cf-114">Requirements</span></span>



| <span data-ttu-id="d49cf-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d49cf-115">Requirement</span></span> | <span data-ttu-id="d49cf-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d49cf-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d49cf-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d49cf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d49cf-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d49cf-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d49cf-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d49cf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d49cf-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d49cf-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d49cf-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d49cf-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d49cf-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="d49cf-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="d49cf-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="d49cf-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="d49cf-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d49cf-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d49cf-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d49cf-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d49cf-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d49cf-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d49cf-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d49cf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d49cf-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="d49cf-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="d49cf-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="d49cf-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="d49cf-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="d49cf-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="d49cf-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="d49cf-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="d49cf-132">**Remo**</span><span class="sxs-lookup"><span data-stu-id="d49cf-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="d49cf-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="d49cf-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="d49cf-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="d49cf-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="d49cf-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="d49cf-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="d49cf-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="d49cf-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="d49cf-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="d49cf-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="d49cf-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="d49cf-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





