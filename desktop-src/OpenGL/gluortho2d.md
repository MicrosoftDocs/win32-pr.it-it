---
title: Funzione gluOrtho2D (Glu.h)
description: La funzione gluOrtho2D definisce una matrice di proiezione ortogonale 2D.
ms.assetid: ba83fb5c-e5c7-4486-a815-a1aff0469757
keywords:
- Funzione gluOrtho2D OpenGL
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
ms.openlocfilehash: 1bf07fea583c5ae46680d888f6bf6c0a9c5aa9a0
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/19/2021
ms.locfileid: "110153554"
---
# <a name="gluortho2d-function"></a><span data-ttu-id="712ec-104">Funzione gluOrtho2D</span><span class="sxs-lookup"><span data-stu-id="712ec-104">gluOrtho2D function</span></span>

<span data-ttu-id="712ec-105">La **funzione gluOrtho2D** definisce una matrice di proiezione ortogonale 2D.</span><span class="sxs-lookup"><span data-stu-id="712ec-105">The **gluOrtho2D** function defines a 2-D orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="712ec-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="712ec-106">Syntax</span></span>


```C++
void WINAPI gluOrtho2D(
   GLdouble left,
   GLdouble right,
   GLdouble top,
   GLdouble bottom
);
```



## <a name="parameters"></a><span data-ttu-id="712ec-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="712ec-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="712ec-108">*Sinistra*</span><span class="sxs-lookup"><span data-stu-id="712ec-108">*left*</span></span> 
</dt> <dd>

<span data-ttu-id="712ec-109">Coordinata per il piano di ritaglio verticale sinistro.</span><span class="sxs-lookup"><span data-stu-id="712ec-109">The coordinate for the left vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="712ec-110">*va bene*</span><span class="sxs-lookup"><span data-stu-id="712ec-110">*right*</span></span> 
</dt> <dd>

<span data-ttu-id="712ec-111">Coordinata per il piano di ritaglio verticale destro.</span><span class="sxs-lookup"><span data-stu-id="712ec-111">The coordinate for the right vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="712ec-112">*top*</span><span class="sxs-lookup"><span data-stu-id="712ec-112">*top*</span></span> 
</dt> <dd>

<span data-ttu-id="712ec-113">Coordinata per il piano di ritaglio orizzontale superiore.</span><span class="sxs-lookup"><span data-stu-id="712ec-113">The coordinate for the top horizontal clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="712ec-114">*Fondoschiena*</span><span class="sxs-lookup"><span data-stu-id="712ec-114">*bottom*</span></span> 
</dt> <dd>

<span data-ttu-id="712ec-115">Coordinata per il piano di ritaglio orizzontale inferiore.</span><span class="sxs-lookup"><span data-stu-id="712ec-115">The coordinate for the bottom horizontal clipping plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="712ec-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="712ec-116">Return value</span></span>

<span data-ttu-id="712ec-117">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="712ec-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="712ec-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="712ec-118">Remarks</span></span>

<span data-ttu-id="712ec-119">La **funzione gluOrtho2D** configura un'area di visualizzazione ortografica bidimensionale.</span><span class="sxs-lookup"><span data-stu-id="712ec-119">The **gluOrtho2D** function sets up a two-dimensional orthographic viewing region.</span></span> <span data-ttu-id="712ec-120">Equivale a chiamare [**glOrtho con**](glortho.md) zNear = -1 e zFar = 1.</span><span class="sxs-lookup"><span data-stu-id="712ec-120">This is equivalent to calling [**glOrtho**](glortho.md) with zNear = -1 and zFar = 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="712ec-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="712ec-121">Requirements</span></span>



| <span data-ttu-id="712ec-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="712ec-122">Requirement</span></span> | <span data-ttu-id="712ec-123">valore</span><span class="sxs-lookup"><span data-stu-id="712ec-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="712ec-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="712ec-124">Minimum supported client</span></span><br/> | <span data-ttu-id="712ec-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="712ec-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="712ec-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="712ec-126">Minimum supported server</span></span><br/> | <span data-ttu-id="712ec-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="712ec-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="712ec-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="712ec-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="712ec-129"><dt>Glu.h</dt></span><span class="sxs-lookup"><span data-stu-id="712ec-129"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="712ec-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="712ec-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="712ec-131"><dt>Glu32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="712ec-131"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="712ec-132">DLL</span><span class="sxs-lookup"><span data-stu-id="712ec-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="712ec-133"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="712ec-133"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="712ec-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="712ec-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="712ec-135">**glOrtho**</span><span class="sxs-lookup"><span data-stu-id="712ec-135">**glOrtho**</span></span>](glortho.md)
</dt> <dt>

[<span data-ttu-id="712ec-136">**gluPerspective**</span><span class="sxs-lookup"><span data-stu-id="712ec-136">**gluPerspective**</span></span>](gluperspective.md)
</dt> </dl>

 

 





