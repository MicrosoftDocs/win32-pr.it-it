---
title: funzione glVertex4fv (GL. h)
description: Specifica un vertice. | funzione glVertex4fv (GL. h)
ms.assetid: c2a766fd-3ad8-463b-8f09-36d0673e6716
keywords:
- funzione glVertex4fv OpenGL
topic_type:
- apiref
api_name:
- glVertex4fv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e05551268b697ba4444c29d5f2b9bdfb0e832e4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321481"
---
# <a name="glvertex4fv-function"></a><span data-ttu-id="00fb6-105">glVertex4fv (funzione)</span><span class="sxs-lookup"><span data-stu-id="00fb6-105">glVertex4fv function</span></span>

<span data-ttu-id="00fb6-106">Specifica un vertice.</span><span class="sxs-lookup"><span data-stu-id="00fb6-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="00fb6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="00fb6-107">Syntax</span></span>


```C++
void WINAPI glVertex4fv(
   const GLfloat *v
);
```



## <a name="parameters"></a><span data-ttu-id="00fb6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="00fb6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00fb6-109">*v*</span><span class="sxs-lookup"><span data-stu-id="00fb6-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="00fb6-110">Puntatore a una matrice di quattro elementi.</span><span class="sxs-lookup"><span data-stu-id="00fb6-110">A pointer to an array of four elements.</span></span> <span data-ttu-id="00fb6-111">Gli elementi sono le coordinate x, y, z e w di un vertice.</span><span class="sxs-lookup"><span data-stu-id="00fb6-111">The elements are the x, y, z, and w coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00fb6-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="00fb6-112">Return value</span></span>

<span data-ttu-id="00fb6-113">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="00fb6-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="00fb6-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00fb6-114">Requirements</span></span>



| <span data-ttu-id="00fb6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="00fb6-115">Requirement</span></span> | <span data-ttu-id="00fb6-116">Valore</span><span class="sxs-lookup"><span data-stu-id="00fb6-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="00fb6-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00fb6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="00fb6-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="00fb6-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="00fb6-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00fb6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="00fb6-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="00fb6-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="00fb6-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="00fb6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="00fb6-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="00fb6-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="00fb6-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="00fb6-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="00fb6-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00fb6-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="00fb6-125">DLL</span><span class="sxs-lookup"><span data-stu-id="00fb6-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00fb6-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00fb6-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00fb6-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="00fb6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00fb6-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="00fb6-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="00fb6-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="00fb6-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="00fb6-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="00fb6-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="00fb6-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="00fb6-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="00fb6-132">**Remo**</span><span class="sxs-lookup"><span data-stu-id="00fb6-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="00fb6-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="00fb6-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="00fb6-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="00fb6-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="00fb6-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="00fb6-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="00fb6-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="00fb6-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="00fb6-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="00fb6-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="00fb6-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="00fb6-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





