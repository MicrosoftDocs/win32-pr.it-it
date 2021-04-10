---
title: funzione gluNewNurbsRenderer (Glu. h)
description: La funzione gluNewNurbsRenderer crea un oggetto di logica B-spline (NURBS) non uniforme.
ms.assetid: f47badb0-6b75-4bfd-9771-516668d9e255
keywords:
- funzione gluNewNurbsRenderer OpenGL
topic_type:
- apiref
api_name:
- gluNewNurbsRenderer
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b6e35df5abd9fb9e7757dd79066fbbe7efe8680
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964449"
---
# <a name="glunewnurbsrenderer-function"></a><span data-ttu-id="f2e41-104">gluNewNurbsRenderer (funzione)</span><span class="sxs-lookup"><span data-stu-id="f2e41-104">gluNewNurbsRenderer function</span></span>

<span data-ttu-id="f2e41-105">La funzione **gluNewNurbsRenderer** crea un oggetto di logica B-spline ([NURBS](using-nurbs-curves-and-surfaces.md)) non uniforme.</span><span class="sxs-lookup"><span data-stu-id="f2e41-105">The **gluNewNurbsRenderer** function creates a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2e41-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f2e41-106">Syntax</span></span>


```C++
GLUnurbs* WINAPI gluNewNurbsRenderer(void);
```



## <a name="parameters"></a><span data-ttu-id="f2e41-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f2e41-107">Parameters</span></span>

<span data-ttu-id="f2e41-108">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="f2e41-108">This function has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2e41-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="f2e41-109">Remarks</span></span>

<span data-ttu-id="f2e41-110">La funzione **gluNewNurbsRenderer** crea e restituisce un puntatore a un nuovo oggetto NURBS.</span><span class="sxs-lookup"><span data-stu-id="f2e41-110">The **gluNewNurbsRenderer** function creates and returns a pointer to a new NURBS object.</span></span> <span data-ttu-id="f2e41-111">Fare riferimento a questo oggetto quando si chiamano le funzioni di rendering e controllo NURBS.</span><span class="sxs-lookup"><span data-stu-id="f2e41-111">Refer to this object when calling NURBS rendering and control functions.</span></span> <span data-ttu-id="f2e41-112">Un valore restituito pari a zero indica che la memoria disponibile non è sufficiente per allocare all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f2e41-112">A return value of zero means there is not enough memory to allocate to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2e41-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f2e41-113">Requirements</span></span>



| <span data-ttu-id="f2e41-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2e41-114">Requirement</span></span> | <span data-ttu-id="f2e41-115">Valore</span><span class="sxs-lookup"><span data-stu-id="f2e41-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f2e41-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2e41-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f2e41-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f2e41-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f2e41-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2e41-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f2e41-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f2e41-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f2e41-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f2e41-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2e41-121"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2e41-121"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="f2e41-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="f2e41-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="f2e41-123"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2e41-123"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f2e41-124">DLL</span><span class="sxs-lookup"><span data-stu-id="f2e41-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2e41-125"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2e41-125"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2e41-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f2e41-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2e41-127">**gluBeginCurve**</span><span class="sxs-lookup"><span data-stu-id="f2e41-127">**gluBeginCurve**</span></span>](glubegincurve.md)
</dt> <dt>

[<span data-ttu-id="f2e41-128">**gluBeginSurface**</span><span class="sxs-lookup"><span data-stu-id="f2e41-128">**gluBeginSurface**</span></span>](glubeginsurface.md)
</dt> <dt>

[<span data-ttu-id="f2e41-129">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="f2e41-129">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="f2e41-130">**gluDeleteNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="f2e41-130">**gluDeleteNurbsRenderer**</span></span>](gludeletenurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="f2e41-131">*gluNurbsCallback*</span><span class="sxs-lookup"><span data-stu-id="f2e41-131">*gluNurbsCallback*</span></span>](glunurbs.md)
</dt> <dt>

[<span data-ttu-id="f2e41-132">**gluNurbsProperty**</span><span class="sxs-lookup"><span data-stu-id="f2e41-132">**gluNurbsProperty**</span></span>](glunurbsproperty.md)
</dt> </dl>

 

 





