---
title: funzione glVertex3dv (GL. h)
description: Specifica un vertice. | funzione glVertex3dv (GL. h)
ms.assetid: 8424735c-2424-4594-aa46-8ce635aabe34
keywords:
- funzione glVertex3dv OpenGL
topic_type:
- apiref
api_name:
- glVertex3dv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1557afc60ee79d02e356a87dd6296d72c1d0f00f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104132243"
---
# <a name="glvertex3dv-function"></a><span data-ttu-id="acc18-105">glVertex3dv (funzione)</span><span class="sxs-lookup"><span data-stu-id="acc18-105">glVertex3dv function</span></span>

<span data-ttu-id="acc18-106">Specifica un vertice.</span><span class="sxs-lookup"><span data-stu-id="acc18-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="acc18-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="acc18-107">Syntax</span></span>


```C++
void WINAPI glVertex3dv(
   const GLdouble *v
);
```



## <a name="parameters"></a><span data-ttu-id="acc18-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="acc18-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acc18-109">*v*</span><span class="sxs-lookup"><span data-stu-id="acc18-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="acc18-110">Puntatore a una matrice di tre elementi.</span><span class="sxs-lookup"><span data-stu-id="acc18-110">A pointer to an array of three elements.</span></span> <span data-ttu-id="acc18-111">Gli elementi sono le coordinate x, y e z di un vertice.</span><span class="sxs-lookup"><span data-stu-id="acc18-111">The elements are the x, y, and z coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acc18-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="acc18-112">Return value</span></span>

<span data-ttu-id="acc18-113">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="acc18-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="acc18-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="acc18-114">Requirements</span></span>



| <span data-ttu-id="acc18-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="acc18-115">Requirement</span></span> | <span data-ttu-id="acc18-116">Valore</span><span class="sxs-lookup"><span data-stu-id="acc18-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="acc18-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="acc18-117">Minimum supported client</span></span><br/> | <span data-ttu-id="acc18-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="acc18-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="acc18-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="acc18-119">Minimum supported server</span></span><br/> | <span data-ttu-id="acc18-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="acc18-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="acc18-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="acc18-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="acc18-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="acc18-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="acc18-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="acc18-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="acc18-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="acc18-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="acc18-125">DLL</span><span class="sxs-lookup"><span data-stu-id="acc18-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="acc18-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="acc18-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acc18-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="acc18-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acc18-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="acc18-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="acc18-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="acc18-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="acc18-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="acc18-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="acc18-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="acc18-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="acc18-132">**Remo**</span><span class="sxs-lookup"><span data-stu-id="acc18-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="acc18-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="acc18-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="acc18-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="acc18-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="acc18-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="acc18-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="acc18-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="acc18-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="acc18-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="acc18-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="acc18-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="acc18-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





