---
title: funzione glPixelZoom (GL. h)
description: La funzione glPixelZoom specifica i fattori di zoom pixel.
ms.assetid: 57ead7d8-0502-46b4-9f66-dbb3cb75b0f9
keywords:
- funzione glPixelZoom OpenGL
topic_type:
- apiref
api_name:
- glPixelZoom
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 065e1735ca0228046cfb08e2fb441d3cdc02af74
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320426"
---
# <a name="glpixelzoom-function"></a><span data-ttu-id="ce3da-104">glPixelZoom (funzione)</span><span class="sxs-lookup"><span data-stu-id="ce3da-104">glPixelZoom function</span></span>

<span data-ttu-id="ce3da-105">La funzione **glPixelZoom** specifica i fattori di zoom pixel.</span><span class="sxs-lookup"><span data-stu-id="ce3da-105">The **glPixelZoom** function specifies the pixel zoom factors.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce3da-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ce3da-106">Syntax</span></span>


```C++
void WINAPI glPixelZoom(
   GLfloat xfactor,
   GLfloat yfactor
);
```



## <a name="parameters"></a><span data-ttu-id="ce3da-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ce3da-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce3da-108">*XFactor*</span><span class="sxs-lookup"><span data-stu-id="ce3da-108">*xfactor*</span></span> 
</dt> <dd>

<span data-ttu-id="ce3da-109">Fattore di zoom *x* per le operazioni di scrittura in pixel.</span><span class="sxs-lookup"><span data-stu-id="ce3da-109">The *x* zoom factor for pixel write operations.</span></span>

</dd> <dt>

<span data-ttu-id="ce3da-110">*yfactor*</span><span class="sxs-lookup"><span data-stu-id="ce3da-110">*yfactor*</span></span> 
</dt> <dd>

<span data-ttu-id="ce3da-111">Il fattore di zoom *y* per le operazioni di scrittura in pixel.</span><span class="sxs-lookup"><span data-stu-id="ce3da-111">The *y* zoom factor for pixel write operations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce3da-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ce3da-112">Return value</span></span>

<span data-ttu-id="ce3da-113">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="ce3da-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ce3da-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="ce3da-114">Error codes</span></span>

<span data-ttu-id="ce3da-115">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="ce3da-115">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="ce3da-116">Nome</span><span class="sxs-lookup"><span data-stu-id="ce3da-116">Name</span></span>                                                                                                  | <span data-ttu-id="ce3da-117">Significato</span><span class="sxs-lookup"><span data-stu-id="ce3da-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ce3da-118"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ce3da-118"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="ce3da-119">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="ce3da-119">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ce3da-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce3da-120">Remarks</span></span>

<span data-ttu-id="ce3da-121">La funzione **glPixelZoom** specifica i valori per i fattori di zoom *x* e *y* .</span><span class="sxs-lookup"><span data-stu-id="ce3da-121">The **glPixelZoom** function specifies values for the *x* and *y* zoom factors.</span></span> <span data-ttu-id="ce3da-122">Durante l'esecuzione di [**glDrawPixels**](gldrawpixels.md) o [**glCopyPixels**](glcopypixels.md), if (*x*<sub>r</sub> ,*y*<sub>r</sub> ) è la posizione raster corrente e un dato elemento si trova nella riga *n* e *m* del rettangolo pixel, quindi i pixel i cui centri si trovano nel rettangolo con angoli</span><span class="sxs-lookup"><span data-stu-id="ce3da-122">During the execution of [**glDrawPixels**](gldrawpixels.md) or [**glCopyPixels**](glcopypixels.md), if (*x*<sub>r</sub> ,*y*<sub>r</sub> ) is the current raster position, and a given element is in the *n* th row and *m* th column of the pixel rectangle, then pixels whose centers are in the rectangle with corners at</span></span>

![Equazione che mostra le posizioni in cui i pixel sono candidati per la sostituzione.](images/pix05.png)

<span data-ttu-id="ce3da-124">sono candidati per la sostituzione.</span><span class="sxs-lookup"><span data-stu-id="ce3da-124">are candidates for replacement.</span></span> <span data-ttu-id="ce3da-125">Vengono modificati anche tutti i pixel il cui centro si trova sul bordo inferiore o sinistro dell'area rettangolare.</span><span class="sxs-lookup"><span data-stu-id="ce3da-125">Any pixel whose center lies on the bottom or left edge of this rectangular region is also modified.</span></span>

<span data-ttu-id="ce3da-126">I fattori di zoom pixel non sono limitati ai valori positivi.</span><span class="sxs-lookup"><span data-stu-id="ce3da-126">Pixel zoom factors are not limited to positive values.</span></span> <span data-ttu-id="ce3da-127">I fattori di zoom negativi riflettono l'immagine risultante sulla posizione raster corrente.</span><span class="sxs-lookup"><span data-stu-id="ce3da-127">Negative zoom factors reflect the resulting image about the current raster position.</span></span>

<span data-ttu-id="ce3da-128">Le funzioni seguenti consentono di recuperare informazioni correlate a **glPixelZoom**:</span><span class="sxs-lookup"><span data-stu-id="ce3da-128">The following functions retrieve information related to **glPixelZoom**:</span></span>

<span data-ttu-id="ce3da-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Zoom \_ X</span><span class="sxs-lookup"><span data-stu-id="ce3da-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ZOOM\_X</span></span>

<span data-ttu-id="ce3da-130">**glGet** con argomento GL \_ Zoom \_ Y</span><span class="sxs-lookup"><span data-stu-id="ce3da-130">**glGet** with argument GL\_ZOOM\_Y</span></span>

## <a name="requirements"></a><span data-ttu-id="ce3da-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce3da-131">Requirements</span></span>



| <span data-ttu-id="ce3da-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce3da-132">Requirement</span></span> | <span data-ttu-id="ce3da-133">Valore</span><span class="sxs-lookup"><span data-stu-id="ce3da-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce3da-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce3da-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ce3da-135">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ce3da-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ce3da-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce3da-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ce3da-137">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ce3da-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ce3da-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ce3da-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce3da-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce3da-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ce3da-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="ce3da-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="ce3da-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce3da-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ce3da-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ce3da-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce3da-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce3da-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce3da-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce3da-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce3da-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="ce3da-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="ce3da-146">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="ce3da-146">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="ce3da-147">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="ce3da-147">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="ce3da-148">**Remo**</span><span class="sxs-lookup"><span data-stu-id="ce3da-148">**glEnd**</span></span>](glend.md)
</dt> </dl>

 

 





