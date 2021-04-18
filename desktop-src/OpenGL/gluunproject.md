---
title: funzione gluUnProject (Glu. h)
description: La funzione gluUnProject esegue il mapping delle coordinate della finestra alle coordinate dell'oggetto.
ms.assetid: 6a719fc2-ad40-4b22-9c99-5753f5dbb8a0
keywords:
- funzione gluUnProject OpenGL
topic_type:
- apiref
api_name:
- gluUnProject
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f45311171dd3d71c9e699953c049e0813f2df361
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302498"
---
# <a name="gluunproject-function"></a><span data-ttu-id="2fd93-104">gluUnProject (funzione)</span><span class="sxs-lookup"><span data-stu-id="2fd93-104">gluUnProject function</span></span>

<span data-ttu-id="2fd93-105">La funzione **gluUnProject** esegue il mapping delle coordinate della finestra alle coordinate dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2fd93-105">The **gluUnProject** function maps window coordinates to object coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fd93-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2fd93-106">Syntax</span></span>


```C++
int WINAPI gluUnProject(
         GLdouble winx,
         GLdouble winy,
         GLdouble winz,
   const GLdouble modelMatrix[16],
   const GLdouble projMatrix[16],
   const GLint    viewport[4],
         GLdouble *objx,
         GLdouble *objy,
         GLdouble *objz
);
```



## <a name="parameters"></a><span data-ttu-id="2fd93-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2fd93-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fd93-108">*Winx*</span><span class="sxs-lookup"><span data-stu-id="2fd93-108">*winx*</span></span> 
</dt> <dd>

<span data-ttu-id="2fd93-109">Coordinata x della finestra da mappare.</span><span class="sxs-lookup"><span data-stu-id="2fd93-109">The x window coordinate to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="2fd93-110">*vinoso*</span><span class="sxs-lookup"><span data-stu-id="2fd93-110">*winy*</span></span> 
</dt> <dd>

<span data-ttu-id="2fd93-111">Coordinata della finestra y da mappare.</span><span class="sxs-lookup"><span data-stu-id="2fd93-111">The y window coordinate to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="2fd93-112">*winz*</span><span class="sxs-lookup"><span data-stu-id="2fd93-112">*winz*</span></span> 
</dt> <dd>

<span data-ttu-id="2fd93-113">Coordinata della finestra z da mappare.</span><span class="sxs-lookup"><span data-stu-id="2fd93-113">The z window coordinate to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="2fd93-114">*modelMatrix*</span><span class="sxs-lookup"><span data-stu-id="2fd93-114">*modelMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="2fd93-115">Matrice Modelview (come da una chiamata [**glGetDoublev**](glgetdoublev.md) ).</span><span class="sxs-lookup"><span data-stu-id="2fd93-115">The modelview matrix (as from a [**glGetDoublev**](glgetdoublev.md) call).</span></span>

</dd> <dt>

<span data-ttu-id="2fd93-116">*projMatrix*</span><span class="sxs-lookup"><span data-stu-id="2fd93-116">*projMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="2fd93-117">Matrice di proiezione, come da una chiamata **glGetDoublev** .</span><span class="sxs-lookup"><span data-stu-id="2fd93-117">The projection matrix (as from a **glGetDoublev** call).</span></span>

</dd> <dt>

<span data-ttu-id="2fd93-118">*Viewport*</span><span class="sxs-lookup"><span data-stu-id="2fd93-118">*viewport*</span></span> 
</dt> <dd>

<span data-ttu-id="2fd93-119">Viewport, come da una chiamata [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) .</span><span class="sxs-lookup"><span data-stu-id="2fd93-119">The viewport (as from a [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) call).</span></span>

</dd> <dt>

<span data-ttu-id="2fd93-120">*objx*</span><span class="sxs-lookup"><span data-stu-id="2fd93-120">*objx*</span></span> 
</dt> <dd>

<span data-ttu-id="2fd93-121">Coordinata x dell'oggetto calcolato.</span><span class="sxs-lookup"><span data-stu-id="2fd93-121">The computed x object coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="2fd93-122">*objy*</span><span class="sxs-lookup"><span data-stu-id="2fd93-122">*objy*</span></span> 
</dt> <dd>

<span data-ttu-id="2fd93-123">Coordinata dell'oggetto y calcolato.</span><span class="sxs-lookup"><span data-stu-id="2fd93-123">The computed y object coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="2fd93-124">*objz*</span><span class="sxs-lookup"><span data-stu-id="2fd93-124">*objz*</span></span> 
</dt> <dd>

<span data-ttu-id="2fd93-125">Coordinata dell'oggetto z calcolato.</span><span class="sxs-lookup"><span data-stu-id="2fd93-125">The computed z object coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fd93-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2fd93-126">Return value</span></span>

<span data-ttu-id="2fd93-127">Se la funzione ha esito positivo, il valore restituito è GL \_ true.</span><span class="sxs-lookup"><span data-stu-id="2fd93-127">If the function succeeds, the return value is GL\_TRUE.</span></span>

<span data-ttu-id="2fd93-128">Se la funzione ha esito negativo, il valore restituito è GL \_ false.</span><span class="sxs-lookup"><span data-stu-id="2fd93-128">If the function fails, the return value is GL\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fd93-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="2fd93-129">Remarks</span></span>

<span data-ttu-id="2fd93-130">La funzione **gluUnProject** esegue il mapping tra le coordinate della finestra specificata e le coordinate dell'oggetto utilizzando *modelMatrix*, *projMatrix* e *viewport*.</span><span class="sxs-lookup"><span data-stu-id="2fd93-130">The **gluUnProject** function maps the specified window coordinates into object coordinates using *modelMatrix*, *projMatrix*, and *viewport*.</span></span> <span data-ttu-id="2fd93-131">Il risultato viene archiviato in *objX*, *objy* e *objz*.</span><span class="sxs-lookup"><span data-stu-id="2fd93-131">The result is stored in *objx*, *objy*, and *objz*.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fd93-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2fd93-132">Requirements</span></span>



| <span data-ttu-id="2fd93-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fd93-133">Requirement</span></span> | <span data-ttu-id="2fd93-134">Valore</span><span class="sxs-lookup"><span data-stu-id="2fd93-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2fd93-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2fd93-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2fd93-136">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2fd93-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="2fd93-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2fd93-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2fd93-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2fd93-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2fd93-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2fd93-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fd93-140"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fd93-140"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="2fd93-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="2fd93-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="2fd93-142"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2fd93-142"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2fd93-143">DLL</span><span class="sxs-lookup"><span data-stu-id="2fd93-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fd93-144"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fd93-144"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fd93-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2fd93-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fd93-146">**glGet**</span><span class="sxs-lookup"><span data-stu-id="2fd93-146">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="2fd93-147">**glGetDoublev**</span><span class="sxs-lookup"><span data-stu-id="2fd93-147">**glGetDoublev**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="2fd93-148">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="2fd93-148">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="2fd93-149">**gluProject**</span><span class="sxs-lookup"><span data-stu-id="2fd93-149">**gluProject**</span></span>](gluproject.md)
</dt> </dl>

 

 





