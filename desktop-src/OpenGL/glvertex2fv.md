---
title: funzione glVertex2fv (GL. h)
description: Specifica un vertice. | funzione glVertex2fv (GL. h)
ms.assetid: bae32d27-2a19-40d5-a3f7-0e7a41918034
keywords:
- funzione glVertex2fv OpenGL
topic_type:
- apiref
api_name:
- glVertex2fv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ecd7a57aff2166f3605d7007cd194f5cff04784
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321443"
---
# <a name="glvertex2fv-function"></a><span data-ttu-id="5e22a-105">glVertex2fv (funzione)</span><span class="sxs-lookup"><span data-stu-id="5e22a-105">glVertex2fv function</span></span>

<span data-ttu-id="5e22a-106">Specifica un vertice.</span><span class="sxs-lookup"><span data-stu-id="5e22a-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e22a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5e22a-107">Syntax</span></span>


```C++
void WINAPI glVertex2fv(
   const GLfloat *v
);
```



## <a name="parameters"></a><span data-ttu-id="5e22a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5e22a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e22a-109">*v*</span><span class="sxs-lookup"><span data-stu-id="5e22a-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="5e22a-110">Puntatore a una matrice di due elementi.</span><span class="sxs-lookup"><span data-stu-id="5e22a-110">A pointer to an array of two elements.</span></span> <span data-ttu-id="5e22a-111">Gli elementi sono le coordinate x e y di un vertice.</span><span class="sxs-lookup"><span data-stu-id="5e22a-111">The elements are the x and y coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e22a-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5e22a-112">Return value</span></span>

<span data-ttu-id="5e22a-113">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="5e22a-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e22a-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e22a-114">Requirements</span></span>



| <span data-ttu-id="5e22a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e22a-115">Requirement</span></span> | <span data-ttu-id="5e22a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="5e22a-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e22a-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e22a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5e22a-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5e22a-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5e22a-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e22a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5e22a-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5e22a-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5e22a-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5e22a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e22a-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e22a-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="5e22a-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="5e22a-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="5e22a-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e22a-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5e22a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5e22a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e22a-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e22a-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e22a-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e22a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e22a-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="5e22a-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="5e22a-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="5e22a-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="5e22a-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="5e22a-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="5e22a-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="5e22a-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="5e22a-132">**Remo**</span><span class="sxs-lookup"><span data-stu-id="5e22a-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="5e22a-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="5e22a-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="5e22a-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="5e22a-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="5e22a-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="5e22a-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="5e22a-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="5e22a-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="5e22a-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="5e22a-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="5e22a-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="5e22a-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





