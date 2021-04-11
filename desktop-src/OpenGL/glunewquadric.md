---
title: funzione gluNewQuadric (Glu. h)
description: La funzione gluNewQuadric crea un oggetto quadrica.
ms.assetid: 5a4289bf-b57a-4c74-b0e3-b7536671e4df
keywords:
- funzione gluNewQuadric OpenGL
topic_type:
- apiref
api_name:
- gluNewQuadric
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: affedc7dcebd2b7925449e22cc1b902e88d936f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964448"
---
# <a name="glunewquadric-function"></a><span data-ttu-id="4a040-104">gluNewQuadric (funzione)</span><span class="sxs-lookup"><span data-stu-id="4a040-104">gluNewQuadric function</span></span>

<span data-ttu-id="4a040-105">La funzione **gluNewQuadric** crea un oggetto quadrica.</span><span class="sxs-lookup"><span data-stu-id="4a040-105">The **gluNewQuadric** function creates a quadric object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a040-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a040-106">Syntax</span></span>


```C++
GLUquadric* WINAPI gluNewQuadric(void);
```



## <a name="parameters"></a><span data-ttu-id="4a040-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="4a040-107">Parameters</span></span>

<span data-ttu-id="4a040-108">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="4a040-108">This function has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a040-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="4a040-109">Remarks</span></span>

<span data-ttu-id="4a040-110">La funzione **gluNewQuadric** crea e restituisce un puntatore a un nuovo oggetto quadrica.</span><span class="sxs-lookup"><span data-stu-id="4a040-110">The **gluNewQuadric** function creates and returns a pointer to a new quadric object.</span></span> <span data-ttu-id="4a040-111">Fare riferimento a questo oggetto quando si chiamano le funzioni di rendering e controllo di quadrica.</span><span class="sxs-lookup"><span data-stu-id="4a040-111">Refer to this object when calling quadric rendering and control functions.</span></span> <span data-ttu-id="4a040-112">Un valore restituito pari a zero indica che la memoria disponibile non è sufficiente per allocare all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4a040-112">A return value of zero means there is not enough memory to allocate to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a040-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a040-113">Requirements</span></span>



| <span data-ttu-id="4a040-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a040-114">Requirement</span></span> | <span data-ttu-id="4a040-115">Valore</span><span class="sxs-lookup"><span data-stu-id="4a040-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4a040-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a040-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4a040-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4a040-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="4a040-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a040-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4a040-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4a040-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4a040-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4a040-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a040-121"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a040-121"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="4a040-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="4a040-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="4a040-123"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a040-123"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4a040-124">DLL</span><span class="sxs-lookup"><span data-stu-id="4a040-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a040-125"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a040-125"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a040-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4a040-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a040-127">**gluCylinder**</span><span class="sxs-lookup"><span data-stu-id="4a040-127">**gluCylinder**</span></span>](glucylinder.md)
</dt> <dt>

[<span data-ttu-id="4a040-128">**gluDeleteQuadric**</span><span class="sxs-lookup"><span data-stu-id="4a040-128">**gluDeleteQuadric**</span></span>](gludeletequadric.md)
</dt> <dt>

[<span data-ttu-id="4a040-129">**gluDisk**</span><span class="sxs-lookup"><span data-stu-id="4a040-129">**gluDisk**</span></span>](gludisk.md)
</dt> <dt>

[<span data-ttu-id="4a040-130">**gluPartialDisk**</span><span class="sxs-lookup"><span data-stu-id="4a040-130">**gluPartialDisk**</span></span>](glupartialdisk.md)
</dt> <dt>

[<span data-ttu-id="4a040-131">*gluQuadricCallback*</span><span class="sxs-lookup"><span data-stu-id="4a040-131">*gluQuadricCallback*</span></span>](gluquadric.md)
</dt> <dt>

[<span data-ttu-id="4a040-132">**gluQuadricDrawStyle**</span><span class="sxs-lookup"><span data-stu-id="4a040-132">**gluQuadricDrawStyle**</span></span>](gluquadricdrawstyle.md)
</dt> <dt>

[<span data-ttu-id="4a040-133">**gluQuadricNormals**</span><span class="sxs-lookup"><span data-stu-id="4a040-133">**gluQuadricNormals**</span></span>](gluquadricnormals.md)
</dt> <dt>

[<span data-ttu-id="4a040-134">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="4a040-134">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="4a040-135">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="4a040-135">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> <dt>

[<span data-ttu-id="4a040-136">**gluSphere**</span><span class="sxs-lookup"><span data-stu-id="4a040-136">**gluSphere**</span></span>](glusphere.md)
</dt> </dl>

 

 





