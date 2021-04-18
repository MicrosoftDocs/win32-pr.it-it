---
title: funzione gluNurbsCallback (Glu. h)
description: La funzione gluNurbsCallback definisce un callback per un oggetto logico B-spline (NURBS) non uniforme.
ms.assetid: 1e9afc00-57c6-459e-a9fc-463f45df2084
keywords:
- funzione gluNurbsCallback OpenGL
topic_type:
- apiref
api_name:
- gluNurbsCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a716724546ef0df4300bedb9aba44f7a23f530
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301258"
---
# <a name="glunurbscallback-function"></a><span data-ttu-id="fa973-104">gluNurbsCallback (funzione)</span><span class="sxs-lookup"><span data-stu-id="fa973-104">gluNurbsCallback function</span></span>

<span data-ttu-id="fa973-105">La funzione **gluNurbsCallback** definisce un callback per un oggetto logico B-spline ([NURBS](using-nurbs-curves-and-surfaces.md)) non uniforme.</span><span class="sxs-lookup"><span data-stu-id="fa973-105">The **gluNurbsCallback** function defines a callback for a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa973-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fa973-106">Syntax</span></span>


```C++
void WINAPI gluNurbsCallback(
   GLUnurbs *nobj,
   GLenum   which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a><span data-ttu-id="fa973-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="fa973-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa973-108">*juje*</span><span class="sxs-lookup"><span data-stu-id="fa973-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="fa973-109">Oggetto NURBS (creato con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="fa973-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="fa973-110">*che*</span><span class="sxs-lookup"><span data-stu-id="fa973-110">*which*</span></span> 
</dt> <dd>

<span data-ttu-id="fa973-111">Callback da definire.</span><span class="sxs-lookup"><span data-stu-id="fa973-111">The callback being defined.</span></span> <span data-ttu-id="fa973-112">L'unico valore valido è GLU \_ Error.</span><span class="sxs-lookup"><span data-stu-id="fa973-112">The only valid value is GLU\_ERROR.</span></span> <span data-ttu-id="fa973-113">Il significato di GLU \_ Error significa che la funzione Error viene chiamata quando viene rilevato un errore.</span><span class="sxs-lookup"><span data-stu-id="fa973-113">The meaning of GLU\_ERROR means that the error function is called when an error is encountered.</span></span> <span data-ttu-id="fa973-114">Il suo singolo argomento è di tipo **GLEnum** e indica l'errore specifico che si è verificato.</span><span class="sxs-lookup"><span data-stu-id="fa973-114">Its single argument is of type **GLenum**, and it indicates the specific error that occurred.</span></span> <span data-ttu-id="fa973-115">Sono presenti 37 errori univoci per NURBS, denominato GLU \_ NURBS \_ ERROR1 tramite Glu \_ NURBS \_ ERROR37.</span><span class="sxs-lookup"><span data-stu-id="fa973-115">There are 37 errors unique to NURBS, named GLU\_NURBS\_ERROR1 through GLU\_NURBS\_ERROR37.</span></span> <span data-ttu-id="fa973-116">Le stringhe di caratteri che descrivono questi errori possono essere recuperate con [**gluErrorString**](gluerrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="fa973-116">Character strings describing these errors can be retrieved with [**gluErrorString**](gluerrorstring.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa973-117">*FN*</span><span class="sxs-lookup"><span data-stu-id="fa973-117">*fn*</span></span> 
</dt> <dd>

<span data-ttu-id="fa973-118">Puntatore alla funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="fa973-118">A pointer to the callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa973-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fa973-119">Return value</span></span>

<span data-ttu-id="fa973-120">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="fa973-120">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa973-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="fa973-121">Remarks</span></span>

<span data-ttu-id="fa973-122">Utilizzare **gluNurbsCallback** per definire un callback che deve essere utilizzato da un oggetto NURBS.</span><span class="sxs-lookup"><span data-stu-id="fa973-122">Use **gluNurbsCallback** to define a callback to be used by a NURBS object.</span></span> <span data-ttu-id="fa973-123">Se il callback specificato è già definito, viene sostituito.</span><span class="sxs-lookup"><span data-stu-id="fa973-123">If the specified callback is already defined, it is replaced.</span></span> <span data-ttu-id="fa973-124">Se *FN* è **null**, qualsiasi callback esistente verrà cancellato.</span><span class="sxs-lookup"><span data-stu-id="fa973-124">If *fn* is **NULL**, then any existing callback is erased.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa973-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fa973-125">Requirements</span></span>



| <span data-ttu-id="fa973-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa973-126">Requirement</span></span> | <span data-ttu-id="fa973-127">Valore</span><span class="sxs-lookup"><span data-stu-id="fa973-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fa973-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa973-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fa973-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fa973-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="fa973-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa973-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fa973-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fa973-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="fa973-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fa973-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa973-133"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa973-133"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="fa973-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="fa973-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="fa973-135"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa973-135"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="fa973-136">DLL</span><span class="sxs-lookup"><span data-stu-id="fa973-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa973-137"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa973-137"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa973-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fa973-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa973-139">**gluErrorString**</span><span class="sxs-lookup"><span data-stu-id="fa973-139">**gluErrorString**</span></span>](gluerrorstring.md)
</dt> <dt>

[<span data-ttu-id="fa973-140">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="fa973-140">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> </dl>

 

 





