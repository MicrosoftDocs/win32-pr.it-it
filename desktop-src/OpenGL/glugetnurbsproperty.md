---
title: funzione gluGetNurbsProperty (Glu. h)
description: La funzione gluGetNurbsProperty ottiene una proprietà di logica B-spline (NURBS) non uniforme.
ms.assetid: 7dbc75a0-d04e-4794-b3dd-a602addf9dfa
keywords:
- funzione gluGetNurbsProperty OpenGL
topic_type:
- apiref
api_name:
- gluGetNurbsProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 583da688e3495ebc2eb9d6f71972658c6426469c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119531"
---
# <a name="glugetnurbsproperty-function"></a><span data-ttu-id="7cade-104">gluGetNurbsProperty (funzione)</span><span class="sxs-lookup"><span data-stu-id="7cade-104">gluGetNurbsProperty function</span></span>

<span data-ttu-id="7cade-105">La funzione **gluGetNurbsProperty** ottiene una proprietà di logica B-spline ([NURBS](using-nurbs-curves-and-surfaces.md)) non uniforme.</span><span class="sxs-lookup"><span data-stu-id="7cade-105">The **gluGetNurbsProperty** function gets a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cade-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7cade-106">Syntax</span></span>


```C++
void WINAPI gluGetNurbsProperty(
   GLUnurbs *nobj,
   GLenum   property,
   GLfloat  *value
);
```



## <a name="parameters"></a><span data-ttu-id="7cade-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="7cade-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cade-108">*juje*</span><span class="sxs-lookup"><span data-stu-id="7cade-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="7cade-109">Oggetto NURBS (creato con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="7cade-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="7cade-110">*property*</span><span class="sxs-lookup"><span data-stu-id="7cade-110">*property*</span></span> 
</dt> <dd>

<span data-ttu-id="7cade-111">Proprietà di cui è necessario recuperare il valore.</span><span class="sxs-lookup"><span data-stu-id="7cade-111">The property whose value is to be retrieved.</span></span> <span data-ttu-id="7cade-112">Sono validi i valori seguenti: \_ tolleranza di campionamento Glu \_ , modalità di \_ visualizzazione Glu \_ , \_ abbattimento Glu, GLU \_ auto \_ Load \_ Matrix, Glu \_ parametrica \_ tolerance, Glu \_ Sampling \_ Method, Glu \_ U \_ Step e Glu \_ V \_ Step.</span><span class="sxs-lookup"><span data-stu-id="7cade-112">The following values are valid: GLU\_SAMPLING\_TOLERANCE, GLU\_DISPLAY\_MODE, GLU\_CULLING, GLU\_AUTO\_LOAD\_MATRIX, GLU\_PARAMETRIC\_TOLERANCE, GLU\_SAMPLING\_METHOD, GLU\_U\_STEP, and GLU\_V\_STEP.</span></span>

</dd> <dt>

<span data-ttu-id="7cade-113">*value*</span><span class="sxs-lookup"><span data-stu-id="7cade-113">*value*</span></span> 
</dt> <dd>

<span data-ttu-id="7cade-114">Puntatore alla posizione in cui viene scritto il valore della proprietà denominata.</span><span class="sxs-lookup"><span data-stu-id="7cade-114">A pointer to the location into which the value of the named property is written.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cade-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7cade-115">Return value</span></span>

<span data-ttu-id="7cade-116">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="7cade-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cade-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="7cade-117">Remarks</span></span>

<span data-ttu-id="7cade-118">Utilizzare **gluGetNurbsProperty** per recuperare le proprietà archiviate in un oggetto NURBS.</span><span class="sxs-lookup"><span data-stu-id="7cade-118">Use **gluGetNurbsProperty** to retrieve properties stored in a NURBS object.</span></span> <span data-ttu-id="7cade-119">Queste proprietà influiscono sulla modalità di rendering delle curve e delle superfici NURBS.</span><span class="sxs-lookup"><span data-stu-id="7cade-119">These properties affect the way NURBS curves and surfaces are rendered.</span></span> <span data-ttu-id="7cade-120">Per informazioni sulle proprietà NURBS, vedere [**gluNurbsProperty**](glunurbsproperty.md).</span><span class="sxs-lookup"><span data-stu-id="7cade-120">For information about NURBS properties, see [**gluNurbsProperty**](glunurbsproperty.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7cade-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7cade-121">Requirements</span></span>



| <span data-ttu-id="7cade-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cade-122">Requirement</span></span> | <span data-ttu-id="7cade-123">Valore</span><span class="sxs-lookup"><span data-stu-id="7cade-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7cade-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7cade-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7cade-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7cade-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7cade-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7cade-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7cade-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7cade-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7cade-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7cade-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cade-129"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cade-129"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="7cade-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="7cade-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="7cade-131"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7cade-131"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7cade-132">DLL</span><span class="sxs-lookup"><span data-stu-id="7cade-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7cade-133"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cade-133"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cade-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7cade-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cade-135">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="7cade-135">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="7cade-136">**gluNurbsProperty**</span><span class="sxs-lookup"><span data-stu-id="7cade-136">**gluNurbsProperty**</span></span>](glunurbsproperty.md)
</dt> </dl>

 

 





