---
title: funzione glVertex2dv (GL. h)
description: Specifica un vertice. | funzione glVertex2dv (GL. h)
ms.assetid: b685d0aa-2874-4ad9-a20c-86823e9ad00b
keywords:
- funzione glVertex2dv OpenGL
topic_type:
- apiref
api_name:
- glVertex2dv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4839fa650302a67c98a0aef3d227dfafa8ddb688
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969111"
---
# <a name="glvertex2dv-function"></a><span data-ttu-id="b84fd-105">glVertex2dv (funzione)</span><span class="sxs-lookup"><span data-stu-id="b84fd-105">glVertex2dv function</span></span>

<span data-ttu-id="b84fd-106">Specifica un vertice.</span><span class="sxs-lookup"><span data-stu-id="b84fd-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="b84fd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b84fd-107">Syntax</span></span>


```C++
void WINAPI glVertex2dv(
   const GLdouble *v
);
```



## <a name="parameters"></a><span data-ttu-id="b84fd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b84fd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b84fd-109">*v*</span><span class="sxs-lookup"><span data-stu-id="b84fd-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="b84fd-110">Puntatore a una matrice di due elementi.</span><span class="sxs-lookup"><span data-stu-id="b84fd-110">A pointer to an array of two elements.</span></span> <span data-ttu-id="b84fd-111">Gli elementi sono le coordinate x e y di un vertice.</span><span class="sxs-lookup"><span data-stu-id="b84fd-111">The elements are the x and y coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b84fd-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b84fd-112">Return value</span></span>

<span data-ttu-id="b84fd-113">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="b84fd-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b84fd-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b84fd-114">Requirements</span></span>



| <span data-ttu-id="b84fd-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b84fd-115">Requirement</span></span> | <span data-ttu-id="b84fd-116">Valore</span><span class="sxs-lookup"><span data-stu-id="b84fd-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b84fd-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b84fd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b84fd-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b84fd-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b84fd-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b84fd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b84fd-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b84fd-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b84fd-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b84fd-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b84fd-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b84fd-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b84fd-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="b84fd-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="b84fd-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b84fd-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b84fd-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b84fd-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b84fd-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b84fd-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b84fd-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b84fd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b84fd-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b84fd-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b84fd-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="b84fd-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="b84fd-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="b84fd-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="b84fd-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="b84fd-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="b84fd-132">**Remo**</span><span class="sxs-lookup"><span data-stu-id="b84fd-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b84fd-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="b84fd-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="b84fd-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="b84fd-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="b84fd-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="b84fd-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="b84fd-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="b84fd-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="b84fd-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="b84fd-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="b84fd-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="b84fd-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





