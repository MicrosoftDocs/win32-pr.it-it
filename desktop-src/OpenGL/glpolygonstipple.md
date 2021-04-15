---
title: funzione glPolygonStipple (GL. h)
description: La funzione glPolygonStipple imposta il pattern punteggiatura del poligono.
ms.assetid: e066f9cf-36da-4a3b-a34f-2f8a6f5a0ae6
keywords:
- funzione glPolygonStipple OpenGL
topic_type:
- apiref
api_name:
- glPolygonStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a2eb0b2e4319f7e3e37191fb197cd7ff86a2a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477236"
---
# <a name="glpolygonstipple-function"></a><span data-ttu-id="50572-104">glPolygonStipple (funzione)</span><span class="sxs-lookup"><span data-stu-id="50572-104">glPolygonStipple function</span></span>

<span data-ttu-id="50572-105">La funzione **glPolygonStipple** imposta il pattern punteggiatura del poligono.</span><span class="sxs-lookup"><span data-stu-id="50572-105">The **glPolygonStipple** function sets the polygon stippling pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="50572-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="50572-106">Syntax</span></span>


```C++
void WINAPI glPolygonStipple(
   const GLubyte *mask
);
```



## <a name="parameters"></a><span data-ttu-id="50572-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="50572-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50572-108">*maschera*</span><span class="sxs-lookup"><span data-stu-id="50572-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="50572-109">Un puntatore a un modello di stipple 32x32 che verrà decompresso dalla memoria nello stesso modo in cui [**glDrawPixels**](gldrawpixels.md) decomprime i pixel.</span><span class="sxs-lookup"><span data-stu-id="50572-109">A pointer to a 32x32 stipple pattern that will be unpacked from memory in the same way that [**glDrawPixels**](gldrawpixels.md) unpacks pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50572-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="50572-110">Return value</span></span>

<span data-ttu-id="50572-111">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="50572-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="50572-112">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="50572-112">Error codes</span></span>

<span data-ttu-id="50572-113">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="50572-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="50572-114">Nome</span><span class="sxs-lookup"><span data-stu-id="50572-114">Name</span></span>                                                                                                  | <span data-ttu-id="50572-115">Significato</span><span class="sxs-lookup"><span data-stu-id="50572-115">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="50572-116"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="50572-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="50572-117">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="50572-117">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="50572-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="50572-118">Remarks</span></span>

<span data-ttu-id="50572-119">La funzione **glPolygonStipple** imposta il pattern punteggiatura del poligono.</span><span class="sxs-lookup"><span data-stu-id="50572-119">The **glPolygonStipple** function sets the polygon stippling pattern.</span></span> <span data-ttu-id="50572-120">Poligono punteggiatura, ad esempio la linea punteggiatura (vedere [**glLineStipple**](gllinestipple.md)), maschera alcuni frammenti prodotti dalla rasterizzazione, creando un modello.</span><span class="sxs-lookup"><span data-stu-id="50572-120">Polygon stippling, like line stippling (see [**glLineStipple**](gllinestipple.md)), masks out certain fragments produced by rasterization, creating a pattern.</span></span> <span data-ttu-id="50572-121">Punteggiatura è indipendente dall'anti-aliasing del poligono.</span><span class="sxs-lookup"><span data-stu-id="50572-121">Stippling is independent of polygon antialiasing.</span></span>

<span data-ttu-id="50572-122">Il parametro *mask* è un puntatore a un modello stipple 32x32 che viene archiviato in memoria esattamente come i dati pixel forniti a **glDrawPixels** con *altezza* e *larghezza* uguali a 32, un *formato* pixel di indice dei \_ colori GL e il \_ *tipo* di dati della \_ bitmap GL.</span><span class="sxs-lookup"><span data-stu-id="50572-122">The *mask* parameter is a pointer to a 32x32 stipple pattern that is stored in memory just like the pixel data supplied to **glDrawPixels** with *height* and *width* both equal to 32, a pixel *format* of GL\_COLOR\_INDEX, and data *type* of GL\_BITMAP.</span></span> <span data-ttu-id="50572-123">Ovvero, il modello stipple è rappresentato come una matrice 32x32 di indici di colore a 1 bit compressi in byte senza segno.</span><span class="sxs-lookup"><span data-stu-id="50572-123">That is, the stipple pattern is represented as a 32x32 array of 1-bit color indexes packed in unsigned bytes.</span></span> <span data-ttu-id="50572-124">I parametri della funzione [**glPixelStore**](glpixelstore-functions.md) , ad esempio GL \_ unpack \_ swap \_ bytes e GL \_ depack \_ LSB \_ First, influiscono sul montaggio dei bit in un modello stipple.</span><span class="sxs-lookup"><span data-stu-id="50572-124">The [**glPixelStore**](glpixelstore-functions.md) function parameters, such as GL\_UNPACK\_SWAP\_BYTES and GL\_UNPACK\_LSB\_FIRST, affect the assembling of the bits into a stipple pattern.</span></span> <span data-ttu-id="50572-125">Tuttavia, le operazioni di trasferimento dei pixel, ovvero MAIUSC, offset e mappa pixel, non vengono applicate all'immagine di stipple.</span><span class="sxs-lookup"><span data-stu-id="50572-125">Pixel transfer operations (shift, offset, and pixel map) are not applied to the stipple image, however.</span></span>

<span data-ttu-id="50572-126">Polygon punteggiatura è abilitato e disabilitato con [**glEnable**](glenable.md) e **glDisable** usando l'argomento GL \_ Polygon \_ stipple.</span><span class="sxs-lookup"><span data-stu-id="50572-126">Polygon stippling is enabled and disabled with [**glEnable**](glenable.md) and **glDisable**, using argument GL\_POLYGON\_STIPPLE.</span></span> <span data-ttu-id="50572-127">Se abilitata, un frammento di poligono rasterizzato con le coordinate della finestra *x*<sub>w</sub> e *y*<sub>w</sub> viene inviato alla fase successiva di OpenGL se e solo se il bit (*x*<sub>w</sub> mod 32) nella riga (*y*<sub>w</sub> mod 32) del modello stipple è uno.</span><span class="sxs-lookup"><span data-stu-id="50572-127">If enabled, a rasterized polygon fragment with window coordinates *x*<sub>w</sub> and *y*<sub>w</sub> is sent to the next stage of OpenGL if and only if the (*x*<sub>w</sub> mod 32)th bit in the (*y*<sub>w</sub> mod 32)th row of the stipple pattern is one.</span></span> <span data-ttu-id="50572-128">Quando il poligono punteggiatura è disabilitato, è come se il modello stipple fosse tutti quelli.</span><span class="sxs-lookup"><span data-stu-id="50572-128">When polygon stippling is disabled, it is as if the stipple pattern were all ones.</span></span>

<span data-ttu-id="50572-129">Le funzioni seguenti consentono di recuperare informazioni correlate a **glPolygonStipple**:</span><span class="sxs-lookup"><span data-stu-id="50572-129">The following functions retrieve information related to **glPolygonStipple**:</span></span>

[<span data-ttu-id="50572-130">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="50572-130">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md)

<span data-ttu-id="50572-131">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Polygon \_ stipple</span><span class="sxs-lookup"><span data-stu-id="50572-131">[**glIsEnabled**](glisenabled.md) with argument GL\_POLYGON\_STIPPLE</span></span>

## <a name="requirements"></a><span data-ttu-id="50572-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50572-132">Requirements</span></span>



| <span data-ttu-id="50572-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="50572-133">Requirement</span></span> | <span data-ttu-id="50572-134">Valore</span><span class="sxs-lookup"><span data-stu-id="50572-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50572-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50572-135">Minimum supported client</span></span><br/> | <span data-ttu-id="50572-136">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="50572-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="50572-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50572-137">Minimum supported server</span></span><br/> | <span data-ttu-id="50572-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="50572-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="50572-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="50572-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="50572-140"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="50572-140"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="50572-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="50572-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="50572-142"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50572-142"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="50572-143">DLL</span><span class="sxs-lookup"><span data-stu-id="50572-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50572-144"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50572-144"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50572-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="50572-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50572-146">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="50572-146">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="50572-147">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="50572-147">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="50572-148">**Remo**</span><span class="sxs-lookup"><span data-stu-id="50572-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="50572-149">**glLineStipple**</span><span class="sxs-lookup"><span data-stu-id="50572-149">**glLineStipple**</span></span>](gllinestipple.md)
</dt> <dt>

[<span data-ttu-id="50572-150">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="50572-150">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="50572-151">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="50572-151">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> </dl>

 

 





