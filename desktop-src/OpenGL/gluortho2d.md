---
title: funzione gluOrtho2D (Glu. h)
description: La funzione gluOrtho2D definisce una matrice di proiezione ortogonale 2D.
ms.assetid: ba83fb5c-e5c7-4486-a815-a1aff0469757
keywords:
- funzione gluOrtho2D OpenGL
topic_type:
- apiref
api_name:
- gluOrtho2D
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a36b321f312a074a5dd78340968f1c9b2b844c6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400212"
---
# <a name="gluortho2d-function"></a><span data-ttu-id="94134-104">gluOrtho2D (funzione)</span><span class="sxs-lookup"><span data-stu-id="94134-104">gluOrtho2D function</span></span>

<span data-ttu-id="94134-105">La funzione **gluOrtho2D** definisce una matrice di proiezione ortogonale 2D.</span><span class="sxs-lookup"><span data-stu-id="94134-105">The **gluOrtho2D** function defines a 2-D orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="94134-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="94134-106">Syntax</span></span>


```C++
void WINAPI gluOrtho2D(
   GLdouble left,
   GLdouble right,
   GLdouble top,
   GLdouble bottom
);
```



## <a name="parameters"></a><span data-ttu-id="94134-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="94134-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94134-108">*sinistra*</span><span class="sxs-lookup"><span data-stu-id="94134-108">*left*</span></span> 
</dt> <dd>

<span data-ttu-id="94134-109">Coordinata per il piano di ritaglio verticale sinistro.</span><span class="sxs-lookup"><span data-stu-id="94134-109">The coordinate for the left vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="94134-110">*Ok*</span><span class="sxs-lookup"><span data-stu-id="94134-110">*right*</span></span> 
</dt> <dd>

<span data-ttu-id="94134-111">Coordinata per il piano di ritaglio verticale destro.</span><span class="sxs-lookup"><span data-stu-id="94134-111">The coordinate for the right vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="94134-112">*top*</span><span class="sxs-lookup"><span data-stu-id="94134-112">*top*</span></span> 
</dt> <dd>

<span data-ttu-id="94134-113">Coordinata per il piano di ritaglio orizzontale superiore.</span><span class="sxs-lookup"><span data-stu-id="94134-113">The coordinate for the top horizontal clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="94134-114">*parte inferiore*</span><span class="sxs-lookup"><span data-stu-id="94134-114">*bottom*</span></span> 
</dt> <dd>

<span data-ttu-id="94134-115">Coordinata per il piano di ritaglio orizzontale inferiore.</span><span class="sxs-lookup"><span data-stu-id="94134-115">The coordinate for the bottom horizontal clipping plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94134-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="94134-116">Return value</span></span>

<span data-ttu-id="94134-117">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="94134-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="94134-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="94134-118">Remarks</span></span>

<span data-ttu-id="94134-119">La funzione **gluOrtho2D** configura un'area di visualizzazione ortogonale bidimensionale.</span><span class="sxs-lookup"><span data-stu-id="94134-119">The **gluOrtho2D** function sets up a two-dimensional orthographic viewing region.</span></span> <span data-ttu-id="94134-120">Equivale a chiamare [**glOrtho**](glortho.md) con near = 1 e lontano = 1.</span><span class="sxs-lookup"><span data-stu-id="94134-120">This is equivalent to calling [**glOrtho**](glortho.md) with near =  1 and far = 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="94134-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="94134-121">Requirements</span></span>



| <span data-ttu-id="94134-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="94134-122">Requirement</span></span> | <span data-ttu-id="94134-123">Valore</span><span class="sxs-lookup"><span data-stu-id="94134-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="94134-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94134-124">Minimum supported client</span></span><br/> | <span data-ttu-id="94134-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="94134-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="94134-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94134-126">Minimum supported server</span></span><br/> | <span data-ttu-id="94134-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="94134-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="94134-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="94134-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="94134-129"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="94134-129"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="94134-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="94134-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="94134-131"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="94134-131"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="94134-132">DLL</span><span class="sxs-lookup"><span data-stu-id="94134-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94134-133"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94134-133"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94134-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="94134-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94134-135">**glOrtho**</span><span class="sxs-lookup"><span data-stu-id="94134-135">**glOrtho**</span></span>](glortho.md)
</dt> <dt>

[<span data-ttu-id="94134-136">**gluPerspective**</span><span class="sxs-lookup"><span data-stu-id="94134-136">**gluPerspective**</span></span>](gluperspective.md)
</dt> </dl>

 

 





