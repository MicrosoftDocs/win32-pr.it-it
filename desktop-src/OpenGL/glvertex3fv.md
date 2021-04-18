---
title: funzione glVertex3fv (GL. h)
description: Specifica un vertice. | funzione glVertex3fv (GL. h)
ms.assetid: d8790ffe-73b1-49d8-a7f5-2117177573ac
keywords:
- funzione glVertex3fv OpenGL
topic_type:
- apiref
api_name:
- glVertex3fv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f3bcbe73d071bc18e3a1a58ef2f505fa9bd6a3b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321493"
---
# <a name="glvertex3fv-function"></a><span data-ttu-id="a8bbf-105">glVertex3fv (funzione)</span><span class="sxs-lookup"><span data-stu-id="a8bbf-105">glVertex3fv function</span></span>

<span data-ttu-id="a8bbf-106">Specifica un vertice.</span><span class="sxs-lookup"><span data-stu-id="a8bbf-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8bbf-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a8bbf-107">Syntax</span></span>


```C++
void WINAPI glVertex3fv(
   const GLfloat *v
);
```



## <a name="parameters"></a><span data-ttu-id="a8bbf-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a8bbf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8bbf-109">*v*</span><span class="sxs-lookup"><span data-stu-id="a8bbf-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="a8bbf-110">Puntatore a una matrice di tre elementi.</span><span class="sxs-lookup"><span data-stu-id="a8bbf-110">A pointer to an array of three elements.</span></span> <span data-ttu-id="a8bbf-111">Gli elementi sono le coordinate x, y e z di un vertice.</span><span class="sxs-lookup"><span data-stu-id="a8bbf-111">The elements are the x, y, and z coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8bbf-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a8bbf-112">Return value</span></span>

<span data-ttu-id="a8bbf-113">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="a8bbf-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8bbf-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8bbf-114">Requirements</span></span>



| <span data-ttu-id="a8bbf-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8bbf-115">Requirement</span></span> | <span data-ttu-id="a8bbf-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a8bbf-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8bbf-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8bbf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a8bbf-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a8bbf-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a8bbf-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8bbf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a8bbf-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a8bbf-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a8bbf-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a8bbf-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8bbf-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8bbf-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a8bbf-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="a8bbf-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="a8bbf-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8bbf-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a8bbf-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a8bbf-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8bbf-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8bbf-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8bbf-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8bbf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8bbf-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a8bbf-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a8bbf-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="a8bbf-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="a8bbf-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="a8bbf-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="a8bbf-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="a8bbf-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="a8bbf-132">**Remo**</span><span class="sxs-lookup"><span data-stu-id="a8bbf-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a8bbf-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="a8bbf-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="a8bbf-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="a8bbf-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="a8bbf-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="a8bbf-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="a8bbf-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="a8bbf-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="a8bbf-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="a8bbf-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="a8bbf-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="a8bbf-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





