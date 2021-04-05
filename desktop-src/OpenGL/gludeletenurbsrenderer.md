---
title: funzione gluDeleteNurbsRenderer (Glu. h)
description: La funzione gluDeleteNurbsRenderer Elimina un oggetto di logica B-spline (NURBS) non uniforme.
ms.assetid: 77063dcb-90b8-47e4-8b00-e1c46cf4f712
keywords:
- funzione gluDeleteNurbsRenderer OpenGL
topic_type:
- apiref
api_name:
- gluDeleteNurbsRenderer
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fb6ecf0bbb7076d4d6292676d3d358586d0986c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741418"
---
# <a name="gludeletenurbsrenderer-function"></a><span data-ttu-id="17345-104">gluDeleteNurbsRenderer (funzione)</span><span class="sxs-lookup"><span data-stu-id="17345-104">gluDeleteNurbsRenderer function</span></span>

<span data-ttu-id="17345-105">La funzione **gluDeleteNurbsRenderer** Elimina un oggetto di logica B-spline ([NURBS](using-nurbs-curves-and-surfaces.md)) non uniforme.</span><span class="sxs-lookup"><span data-stu-id="17345-105">The **gluDeleteNurbsRenderer** function destroys a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="17345-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="17345-106">Syntax</span></span>


```C++
void WINAPI gluDeleteNurbsRenderer(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a><span data-ttu-id="17345-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="17345-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17345-108">*juje*</span><span class="sxs-lookup"><span data-stu-id="17345-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="17345-109">Oggetto NURBS da eliminare definitivamente (creato con **gluNewNurbsRenderer**).</span><span class="sxs-lookup"><span data-stu-id="17345-109">The NURBS object to be destroyed (created with **gluNewNurbsRenderer**).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17345-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="17345-110">Return value</span></span>

<span data-ttu-id="17345-111">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="17345-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="17345-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="17345-112">Remarks</span></span>

<span data-ttu-id="17345-113">La funzione **gluDeleteNurbsRenderer** Elimina l'oggetto NURBS e libera la memoria usata.</span><span class="sxs-lookup"><span data-stu-id="17345-113">The **gluDeleteNurbsRenderer** function destroys the NURBS object and frees any memory that it used.</span></span> <span data-ttu-id="17345-114">Dopo aver chiamato **gluDeleteNurbsRenderer**, non è più possibile usare *juje* .</span><span class="sxs-lookup"><span data-stu-id="17345-114">After you have called **gluDeleteNurbsRenderer**, you cannot use *nobj* again.</span></span>

## <a name="requirements"></a><span data-ttu-id="17345-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17345-115">Requirements</span></span>



| <span data-ttu-id="17345-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="17345-116">Requirement</span></span> | <span data-ttu-id="17345-117">Valore</span><span class="sxs-lookup"><span data-stu-id="17345-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="17345-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17345-118">Minimum supported client</span></span><br/> | <span data-ttu-id="17345-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="17345-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="17345-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17345-120">Minimum supported server</span></span><br/> | <span data-ttu-id="17345-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="17345-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="17345-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="17345-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="17345-123"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="17345-123"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="17345-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="17345-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="17345-125"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17345-125"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="17345-126">DLL</span><span class="sxs-lookup"><span data-stu-id="17345-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17345-127"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17345-127"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17345-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="17345-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17345-129">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="17345-129">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> </dl>

 

 





