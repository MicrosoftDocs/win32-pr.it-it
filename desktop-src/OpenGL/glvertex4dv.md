---
title: funzione glVertex4dv (GL. h)
description: Specifica un vertice. | funzione glVertex4dv (GL. h)
ms.assetid: af0a3c69-0d71-4cbb-9494-561033d99ac1
keywords:
- funzione glVertex4dv OpenGL
topic_type:
- apiref
api_name:
- glVertex4dv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 532a71c576ca0b49dd645afe8b501f0e718a827b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321482"
---
# <a name="glvertex4dv-function"></a><span data-ttu-id="18ed4-105">glVertex4dv (funzione)</span><span class="sxs-lookup"><span data-stu-id="18ed4-105">glVertex4dv function</span></span>

<span data-ttu-id="18ed4-106">Specifica un vertice.</span><span class="sxs-lookup"><span data-stu-id="18ed4-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="18ed4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="18ed4-107">Syntax</span></span>


```C++
void WINAPI glVertex4dv(
   const GLdouble *v
);
```



## <a name="parameters"></a><span data-ttu-id="18ed4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="18ed4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18ed4-109">*v*</span><span class="sxs-lookup"><span data-stu-id="18ed4-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="18ed4-110">Puntatore a una matrice di quattro elementi.</span><span class="sxs-lookup"><span data-stu-id="18ed4-110">A pointer to an array of four elements.</span></span> <span data-ttu-id="18ed4-111">Gli elementi sono le coordinate x, y, z e w di un vertice.</span><span class="sxs-lookup"><span data-stu-id="18ed4-111">The elements are the x, y, z, and w coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18ed4-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="18ed4-112">Return value</span></span>

<span data-ttu-id="18ed4-113">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="18ed4-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="18ed4-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="18ed4-114">Requirements</span></span>



| <span data-ttu-id="18ed4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="18ed4-115">Requirement</span></span> | <span data-ttu-id="18ed4-116">Valore</span><span class="sxs-lookup"><span data-stu-id="18ed4-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18ed4-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18ed4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="18ed4-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="18ed4-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="18ed4-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18ed4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="18ed4-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="18ed4-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="18ed4-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="18ed4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="18ed4-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="18ed4-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="18ed4-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="18ed4-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="18ed4-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="18ed4-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="18ed4-125">DLL</span><span class="sxs-lookup"><span data-stu-id="18ed4-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18ed4-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18ed4-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18ed4-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="18ed4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18ed4-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="18ed4-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="18ed4-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="18ed4-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="18ed4-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="18ed4-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="18ed4-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="18ed4-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="18ed4-132">**Remo**</span><span class="sxs-lookup"><span data-stu-id="18ed4-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="18ed4-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="18ed4-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="18ed4-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="18ed4-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="18ed4-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="18ed4-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="18ed4-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="18ed4-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="18ed4-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="18ed4-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="18ed4-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="18ed4-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





