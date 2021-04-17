---
title: funzione gluProject (Glu. h)
description: La funzione gluProject esegue il mapping delle coordinate dell'oggetto alle coordinate della finestra.
ms.assetid: cfd8bc5b-b684-4207-8bdb-bf086858da13
keywords:
- funzione gluProject OpenGL
topic_type:
- apiref
api_name:
- gluProject
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84972d95d381a630bf6caf7f0099ce740a4f2741
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478023"
---
# <a name="gluproject-function"></a><span data-ttu-id="cb1cc-104">gluProject (funzione)</span><span class="sxs-lookup"><span data-stu-id="cb1cc-104">gluProject function</span></span>

<span data-ttu-id="cb1cc-105">La funzione **gluProject** esegue il mapping delle coordinate dell'oggetto alle coordinate della finestra.</span><span class="sxs-lookup"><span data-stu-id="cb1cc-105">The **gluProject** function maps object coordinates to window coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb1cc-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cb1cc-106">Syntax</span></span>


```C++
int WINAPI gluProject(
         GLdouble objx,
         GLdouble objy,
         GLdouble objz,
   const GLdouble modelMatrix[16],
   const GLdouble projMatrix[16],
   const GLint    viewport[4],
         GLdouble *winx,
         GLdouble *winy,
         GLdouble *winz
);
```



## <a name="parameters"></a><span data-ttu-id="cb1cc-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="cb1cc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb1cc-108">*objx*</span><span class="sxs-lookup"><span data-stu-id="cb1cc-108">*objx*</span></span> 
</dt> <dd>

<span data-ttu-id="cb1cc-109">Coordinata x dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cb1cc-109">The x object coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="cb1cc-110">*objy*</span><span class="sxs-lookup"><span data-stu-id="cb1cc-110">*objy*</span></span> 
</dt> <dd>

<span data-ttu-id="cb1cc-111">Coordinata y dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cb1cc-111">The y object coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="cb1cc-112">*objz*</span><span class="sxs-lookup"><span data-stu-id="cb1cc-112">*objz*</span></span> 
</dt> <dd>

<span data-ttu-id="cb1cc-113">Coordinata z dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cb1cc-113">The z object coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="cb1cc-114">*modelMatrix*</span><span class="sxs-lookup"><span data-stu-id="cb1cc-114">*modelMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="cb1cc-115">Matrice Modelview corrente (come da una chiamata [**glGetDoublev**](glgetdoublev.md) ).</span><span class="sxs-lookup"><span data-stu-id="cb1cc-115">The current modelview matrix (as from a [**glGetDoublev**](glgetdoublev.md) call).</span></span>

</dd> <dt>

<span data-ttu-id="cb1cc-116">*projMatrix*</span><span class="sxs-lookup"><span data-stu-id="cb1cc-116">*projMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="cb1cc-117">Matrice di proiezione corrente (come da una chiamata **glGetDoublev** ).</span><span class="sxs-lookup"><span data-stu-id="cb1cc-117">The current projection matrix (as from a **glGetDoublev** call).</span></span>

</dd> <dt>

<span data-ttu-id="cb1cc-118">*Viewport*</span><span class="sxs-lookup"><span data-stu-id="cb1cc-118">*viewport*</span></span> 
</dt> <dd>

<span data-ttu-id="cb1cc-119">Viewport corrente (come da una chiamata [**glGetIntegerv**](glgetintegerv.md) ).</span><span class="sxs-lookup"><span data-stu-id="cb1cc-119">The current viewport (as from a [**glGetIntegerv**](glgetintegerv.md) call).</span></span>

</dd> <dt>

<span data-ttu-id="cb1cc-120">*Winx*</span><span class="sxs-lookup"><span data-stu-id="cb1cc-120">*winx*</span></span> 
</dt> <dd>

<span data-ttu-id="cb1cc-121">Coordinata x della finestra calcolata.</span><span class="sxs-lookup"><span data-stu-id="cb1cc-121">The computed x window coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="cb1cc-122">*vinoso*</span><span class="sxs-lookup"><span data-stu-id="cb1cc-122">*winy*</span></span> 
</dt> <dd>

<span data-ttu-id="cb1cc-123">Coordinata della finestra y calcolata.</span><span class="sxs-lookup"><span data-stu-id="cb1cc-123">The computed y window coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="cb1cc-124">*winz*</span><span class="sxs-lookup"><span data-stu-id="cb1cc-124">*winz*</span></span> 
</dt> <dd>

<span data-ttu-id="cb1cc-125">Coordinata della finestra z calcolata.</span><span class="sxs-lookup"><span data-stu-id="cb1cc-125">The computed z window coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb1cc-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cb1cc-126">Return value</span></span>

<span data-ttu-id="cb1cc-127">Se la funzione ha esito positivo, il valore restituito è GL \_ true.</span><span class="sxs-lookup"><span data-stu-id="cb1cc-127">If the function succeeds, the return value is GL\_TRUE.</span></span>

<span data-ttu-id="cb1cc-128">Se la funzione ha esito negativo, il valore restituito è GL \_ false.</span><span class="sxs-lookup"><span data-stu-id="cb1cc-128">If the function fails, the return value is GL\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb1cc-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="cb1cc-129">Remarks</span></span>

<span data-ttu-id="cb1cc-130">La funzione **gluProject** trasforma le coordinate dell'oggetto specificato in coordinate della finestra usando *modelMatrix*, *projMatrix* e *viewport*.</span><span class="sxs-lookup"><span data-stu-id="cb1cc-130">The **gluProject** function transforms the specified object coordinates into window coordinates using *modelMatrix*, *projMatrix*, and *viewport*.</span></span> <span data-ttu-id="cb1cc-131">Il risultato viene archiviato in *Winx*, *vinoso* e *Winz*.</span><span class="sxs-lookup"><span data-stu-id="cb1cc-131">The result is stored in *winx*, *winy*, and *winz*.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb1cc-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb1cc-132">Requirements</span></span>



| <span data-ttu-id="cb1cc-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb1cc-133">Requirement</span></span> | <span data-ttu-id="cb1cc-134">Valore</span><span class="sxs-lookup"><span data-stu-id="cb1cc-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cb1cc-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb1cc-135">Minimum supported client</span></span><br/> | <span data-ttu-id="cb1cc-136">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cb1cc-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="cb1cc-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb1cc-137">Minimum supported server</span></span><br/> | <span data-ttu-id="cb1cc-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cb1cc-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cb1cc-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cb1cc-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb1cc-140"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb1cc-140"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="cb1cc-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="cb1cc-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="cb1cc-142"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb1cc-142"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="cb1cc-143">DLL</span><span class="sxs-lookup"><span data-stu-id="cb1cc-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb1cc-144"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb1cc-144"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb1cc-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb1cc-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb1cc-146">**glGetDoublev**</span><span class="sxs-lookup"><span data-stu-id="cb1cc-146">**glGetDoublev**</span></span>](glgetdoublev.md)
</dt> <dt>

[<span data-ttu-id="cb1cc-147">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="cb1cc-147">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="cb1cc-148">**gluUnProject**</span><span class="sxs-lookup"><span data-stu-id="cb1cc-148">**gluUnProject**</span></span>](gluunproject.md)
</dt> </dl>

 

 





