---
title: funzione glIndexMask (GL. h)
description: La funzione glIndexMask controlla la scrittura di singoli bit nei buffer di indice dei colori.
ms.assetid: f4b5df36-390f-4254-95fb-98589750a11b
keywords:
- funzione glIndexMask OpenGL
topic_type:
- apiref
api_name:
- glIndexMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d426cb1f4bb2e794bef53853d0336db1d64b263
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301165"
---
# <a name="glindexmask-function"></a><span data-ttu-id="d9da2-104">glIndexMask (funzione)</span><span class="sxs-lookup"><span data-stu-id="d9da2-104">glIndexMask function</span></span>

<span data-ttu-id="d9da2-105">La funzione **glIndexMask** controlla la scrittura di singoli bit nei buffer di indice dei colori.</span><span class="sxs-lookup"><span data-stu-id="d9da2-105">The **glIndexMask** function controls the writing of individual bits in the color-index buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9da2-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d9da2-106">Syntax</span></span>


```C++
void WINAPI glIndexMask(
   GLuint mask
);
```



## <a name="parameters"></a><span data-ttu-id="d9da2-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="d9da2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9da2-108">*maschera*</span><span class="sxs-lookup"><span data-stu-id="d9da2-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="d9da2-109">Maschera di bit per abilitare e disabilitare la scrittura di singoli bit nei buffer di indice dei colori.</span><span class="sxs-lookup"><span data-stu-id="d9da2-109">A bit mask to enable and disable the writing of individual bits in the color-index buffers.</span></span> <span data-ttu-id="d9da2-110">Inizialmente, la maschera corrisponde a tutti gli altri.</span><span class="sxs-lookup"><span data-stu-id="d9da2-110">Initially, the mask is all ones.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9da2-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d9da2-111">Return value</span></span>

<span data-ttu-id="d9da2-112">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="d9da2-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d9da2-113">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="d9da2-113">Error codes</span></span>

<span data-ttu-id="d9da2-114">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="d9da2-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="d9da2-115">Nome</span><span class="sxs-lookup"><span data-stu-id="d9da2-115">Name</span></span>                                                                                                  | <span data-ttu-id="d9da2-116">Significato</span><span class="sxs-lookup"><span data-stu-id="d9da2-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d9da2-117"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d9da2-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d9da2-118">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="d9da2-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d9da2-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="d9da2-119">Remarks</span></span>

<span data-ttu-id="d9da2-120">La funzione **glIndexMask** controlla la scrittura di singoli bit nei buffer di indice dei colori.</span><span class="sxs-lookup"><span data-stu-id="d9da2-120">The **glIndexMask** function controls the writing of individual bits in the color-index buffers.</span></span> <span data-ttu-id="d9da2-121">I *n* bit meno significativi della *maschera*, dove *1* è il numero di bit in un buffer di indice dei colori, specificare una maschera.</span><span class="sxs-lookup"><span data-stu-id="d9da2-121">The least significant *n* bits of *mask*, where *1* is the number of bits in a color-index buffer, specify a mask.</span></span> <span data-ttu-id="d9da2-122">Ogni volta che viene visualizzato un oggetto nella maschera, il bit corrispondente nel buffer dell'indice dei colori (o buffer) viene reso scrivibile.</span><span class="sxs-lookup"><span data-stu-id="d9da2-122">Wherever a one appears in the mask, the corresponding bit in the color-index buffer (or buffers) is made writable.</span></span> <span data-ttu-id="d9da2-123">Quando viene visualizzato uno zero, il bit è protetto da scrittura.</span><span class="sxs-lookup"><span data-stu-id="d9da2-123">Where a zero appears, the bit is write-protected.</span></span>

<span data-ttu-id="d9da2-124">Questa maschera viene utilizzata solo in modalità di indice dei colori e influiscono solo sui buffer attualmente selezionati per la scrittura (vedere [**glDrawBuffer**](gldrawbuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="d9da2-124">This mask is used only in color-index mode, and it affects only the buffers currently selected for writing (see [**glDrawBuffer**](gldrawbuffer.md)).</span></span> <span data-ttu-id="d9da2-125">Inizialmente, tutti i bit sono abilitati per la scrittura.</span><span class="sxs-lookup"><span data-stu-id="d9da2-125">Initially, all bits are enabled for writing.</span></span>

<span data-ttu-id="d9da2-126">La funzione seguente recupera le informazioni correlate a **glIndexMask**:</span><span class="sxs-lookup"><span data-stu-id="d9da2-126">The following function retrieves information related to **glIndexMask**:</span></span>

<span data-ttu-id="d9da2-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ index \_ WRITEMASK</span><span class="sxs-lookup"><span data-stu-id="d9da2-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_INDEX\_WRITEMASK</span></span>

## <a name="requirements"></a><span data-ttu-id="d9da2-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9da2-128">Requirements</span></span>



| <span data-ttu-id="d9da2-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9da2-129">Requirement</span></span> | <span data-ttu-id="d9da2-130">Valore</span><span class="sxs-lookup"><span data-stu-id="d9da2-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9da2-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9da2-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d9da2-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d9da2-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d9da2-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9da2-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d9da2-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d9da2-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d9da2-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d9da2-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9da2-136"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9da2-136"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="d9da2-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="d9da2-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="d9da2-138"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9da2-138"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d9da2-139">DLL</span><span class="sxs-lookup"><span data-stu-id="d9da2-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9da2-140"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9da2-140"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9da2-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9da2-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9da2-142">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="d9da2-142">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="d9da2-143">**glDepthMask**</span><span class="sxs-lookup"><span data-stu-id="d9da2-143">**glDepthMask**</span></span>](gldepthmask.md)
</dt> <dt>

[<span data-ttu-id="d9da2-144">**glDrawBuffer**</span><span class="sxs-lookup"><span data-stu-id="d9da2-144">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="d9da2-145">**Remo**</span><span class="sxs-lookup"><span data-stu-id="d9da2-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="d9da2-146">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="d9da2-146">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="d9da2-147">**glStencilMask**</span><span class="sxs-lookup"><span data-stu-id="d9da2-147">**glStencilMask**</span></span>](glstencilmask.md)
</dt> </dl>

 

 





