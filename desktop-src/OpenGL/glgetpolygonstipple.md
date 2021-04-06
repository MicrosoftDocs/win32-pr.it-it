---
title: funzione glGetPolygonStipple (GL. h)
description: La funzione glGetPolygonStipple restituisce il pattern stipple del poligono.
ms.assetid: 95c1ebfa-8465-4bc1-b3f5-eed696a83816
keywords:
- funzione glGetPolygonStipple OpenGL
topic_type:
- apiref
api_name:
- glGetPolygonStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 643d0ea6b7583f26565ab7b9233f7df1dce9aead
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873461"
---
# <a name="glgetpolygonstipple-function"></a><span data-ttu-id="004fc-104">glGetPolygonStipple (funzione)</span><span class="sxs-lookup"><span data-stu-id="004fc-104">glGetPolygonStipple function</span></span>

<span data-ttu-id="004fc-105">La funzione **glGetPolygonStipple** restituisce il pattern stipple del poligono.</span><span class="sxs-lookup"><span data-stu-id="004fc-105">The **glGetPolygonStipple** function returns the polygon stipple pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="004fc-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="004fc-106">Syntax</span></span>


```C++
void WINAPI glGetPolygonStipple(
   GLubyte *mask
);
```



## <a name="parameters"></a><span data-ttu-id="004fc-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="004fc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="004fc-108">*maschera*</span><span class="sxs-lookup"><span data-stu-id="004fc-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="004fc-109">Restituisce il pattern stipple.</span><span class="sxs-lookup"><span data-stu-id="004fc-109">Returns the stipple pattern.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="004fc-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="004fc-110">Return value</span></span>

<span data-ttu-id="004fc-111">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="004fc-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="004fc-112">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="004fc-112">Error codes</span></span>

<span data-ttu-id="004fc-113">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="004fc-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="004fc-114">Nome</span><span class="sxs-lookup"><span data-stu-id="004fc-114">Name</span></span>                                                                                                  | <span data-ttu-id="004fc-115">Significato</span><span class="sxs-lookup"><span data-stu-id="004fc-115">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="004fc-116"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="004fc-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="004fc-117">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="004fc-117">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="004fc-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="004fc-118">Remarks</span></span>

<span data-ttu-id="004fc-119">La funzione **glGetPolygonStipple** restituisce un modello stipple poligono 32x32 tramite il parametro *mask* .</span><span class="sxs-lookup"><span data-stu-id="004fc-119">The **glGetPolygonStipple** function returns a 32x32 polygon stipple pattern through the *mask* parameter.</span></span> <span data-ttu-id="004fc-120">Il modello viene compresso in memoria come se fosse stato chiamato [**glReadPixels**](glreadpixels.md) con *altezza* e *larghezza* di 32, il *tipo* di \_ bitmap GL e il *formato* dell'indice dei \_ colori GL \_ e il modello stipple fosse archiviato in un buffer di indice colori 32x32 interno.</span><span class="sxs-lookup"><span data-stu-id="004fc-120">The pattern is packed into memory as if [**glReadPixels**](glreadpixels.md) with both *height* and *width* of 32, *type* of GL\_BITMAP, and *format* of GL\_COLOR\_INDEX were called, and the stipple pattern were stored in an internal 32x32 color-index buffer.</span></span> <span data-ttu-id="004fc-121">Diversamente da **glReadPixels**, tuttavia, le operazioni di trasferimento dei pixel (spostamento, offset e mappa pixel) non vengono applicate all'immagine stipple restituita.</span><span class="sxs-lookup"><span data-stu-id="004fc-121">Unlike **glReadPixels**, however, pixel-transfer operations (shift, offset, and pixel map) are not applied to the returned stipple image.</span></span>

<span data-ttu-id="004fc-122">Se viene generato un errore, non viene apportata alcuna modifica al contenuto della *maschera*.</span><span class="sxs-lookup"><span data-stu-id="004fc-122">If an error is generated, no change is made to the contents of *mask*.</span></span>

## <a name="requirements"></a><span data-ttu-id="004fc-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="004fc-123">Requirements</span></span>



| <span data-ttu-id="004fc-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="004fc-124">Requirement</span></span> | <span data-ttu-id="004fc-125">Valore</span><span class="sxs-lookup"><span data-stu-id="004fc-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="004fc-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="004fc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="004fc-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="004fc-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="004fc-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="004fc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="004fc-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="004fc-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="004fc-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="004fc-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="004fc-131"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="004fc-131"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="004fc-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="004fc-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="004fc-133"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="004fc-133"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="004fc-134">DLL</span><span class="sxs-lookup"><span data-stu-id="004fc-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="004fc-135"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="004fc-135"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="004fc-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="004fc-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="004fc-137">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="004fc-137">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="004fc-138">**Remo**</span><span class="sxs-lookup"><span data-stu-id="004fc-138">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="004fc-139">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="004fc-139">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="004fc-140">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="004fc-140">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="004fc-141">**glPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="004fc-141">**glPolygonStipple**</span></span>](glpolygonstipple.md)
</dt> <dt>

[<span data-ttu-id="004fc-142">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="004fc-142">**glReadPixels**</span></span>](glreadpixels.md)
</dt> </dl>

 

 





