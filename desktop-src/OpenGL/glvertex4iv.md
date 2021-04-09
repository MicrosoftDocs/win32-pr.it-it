---
title: funzione glVertex4iv (GL. h)
description: Specifica un vertice. | funzione glVertex4iv (GL. h)
ms.assetid: 7b56777a-f904-4a9d-8d3d-84a38cbf0b45
keywords:
- funzione glVertex4iv OpenGL
topic_type:
- apiref
api_name:
- glVertex4iv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ff55c5534245843d5caa8797b2b529c7cfe00f9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103886260"
---
# <a name="glvertex4iv-function"></a><span data-ttu-id="a63a0-105">glVertex4iv (funzione)</span><span class="sxs-lookup"><span data-stu-id="a63a0-105">glVertex4iv function</span></span>

<span data-ttu-id="a63a0-106">Specifica un vertice.</span><span class="sxs-lookup"><span data-stu-id="a63a0-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="a63a0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a63a0-107">Syntax</span></span>


```C++
void WINAPI glVertex4iv(
   const GLint *v
);
```



## <a name="parameters"></a><span data-ttu-id="a63a0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a63a0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a63a0-109">*v*</span><span class="sxs-lookup"><span data-stu-id="a63a0-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="a63a0-110">Puntatore a una matrice di quattro elementi.</span><span class="sxs-lookup"><span data-stu-id="a63a0-110">A pointer to an array of four elements.</span></span> <span data-ttu-id="a63a0-111">Gli elementi sono le coordinate x, y, z e w di un vertice.</span><span class="sxs-lookup"><span data-stu-id="a63a0-111">The elements are the x, y, z, and w coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a63a0-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a63a0-112">Return value</span></span>

<span data-ttu-id="a63a0-113">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="a63a0-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a63a0-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a63a0-114">Requirements</span></span>



| <span data-ttu-id="a63a0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a63a0-115">Requirement</span></span> | <span data-ttu-id="a63a0-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a63a0-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a63a0-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a63a0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a63a0-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a63a0-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a63a0-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a63a0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a63a0-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a63a0-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a63a0-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a63a0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a63a0-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a63a0-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a63a0-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="a63a0-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="a63a0-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a63a0-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a63a0-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a63a0-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a63a0-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a63a0-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a63a0-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a63a0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a63a0-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a63a0-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a63a0-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="a63a0-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="a63a0-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="a63a0-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="a63a0-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="a63a0-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="a63a0-132">**Remo**</span><span class="sxs-lookup"><span data-stu-id="a63a0-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a63a0-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="a63a0-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="a63a0-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="a63a0-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="a63a0-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="a63a0-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="a63a0-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="a63a0-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="a63a0-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="a63a0-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="a63a0-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="a63a0-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





