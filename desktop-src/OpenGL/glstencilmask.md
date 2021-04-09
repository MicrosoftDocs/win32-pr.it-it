---
title: funzione glStencilMask (GL. h)
description: La funzione glStencilMask controlla la scrittura di singoli bit nei piani dello stencil.
ms.assetid: c586f9db-bad5-4f06-a194-a8d979842d0c
keywords:
- funzione glStencilMask OpenGL
topic_type:
- apiref
api_name:
- glStencilMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e63790fa30e88abbde6e1ba47e624c6caf2dcfc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121583"
---
# <a name="glstencilmask-function"></a><span data-ttu-id="66356-104">glStencilMask (funzione)</span><span class="sxs-lookup"><span data-stu-id="66356-104">glStencilMask function</span></span>

<span data-ttu-id="66356-105">La funzione **glStencilMask** controlla la scrittura di singoli bit nei piani dello stencil.</span><span class="sxs-lookup"><span data-stu-id="66356-105">The **glStencilMask** function controls the writing of individual bits in the stencil planes.</span></span>

## <a name="syntax"></a><span data-ttu-id="66356-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="66356-106">Syntax</span></span>


```C++
void WINAPI glStencilMask(
   GLuint mask
);
```



## <a name="parameters"></a><span data-ttu-id="66356-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="66356-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66356-108">*maschera*</span><span class="sxs-lookup"><span data-stu-id="66356-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="66356-109">Maschera di bit per abilitare e disabilitare la scrittura di singoli bit nei piani dello stencil.</span><span class="sxs-lookup"><span data-stu-id="66356-109">A bit mask to enable and disable writing of individual bits in the stencil planes.</span></span> <span data-ttu-id="66356-110">Inizialmente, la maschera corrisponde a tutti gli altri.</span><span class="sxs-lookup"><span data-stu-id="66356-110">Initially, the mask is all ones.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66356-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="66356-111">Return value</span></span>

<span data-ttu-id="66356-112">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="66356-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="66356-113">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="66356-113">Error codes</span></span>

<span data-ttu-id="66356-114">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="66356-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="66356-115">Nome</span><span class="sxs-lookup"><span data-stu-id="66356-115">Name</span></span>                                                                                                  | <span data-ttu-id="66356-116">Significato</span><span class="sxs-lookup"><span data-stu-id="66356-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="66356-117"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="66356-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="66356-118">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="66356-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="66356-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="66356-119">Remarks</span></span>

<span data-ttu-id="66356-120">La funzione **glStencilMask** controlla la scrittura di singoli bit nei piani dello stencil.</span><span class="sxs-lookup"><span data-stu-id="66356-120">The **glStencilMask** function controls the writing of individual bits in the stencil planes.</span></span> <span data-ttu-id="66356-121">I *n* bit meno significativi della *maschera*, dove *n* è il numero di bit nel buffer dello stencil, specificare una maschera.</span><span class="sxs-lookup"><span data-stu-id="66356-121">The least significant *n* bits of *mask*, where *n* is the number of bits in the stencil buffer, specify a mask.</span></span> <span data-ttu-id="66356-122">Ogni volta che viene visualizzato un oggetto nella maschera, il bit corrispondente nel buffer dello stencil viene reso scrivibile.</span><span class="sxs-lookup"><span data-stu-id="66356-122">Wherever a one appears in the mask, the corresponding bit in the stencil buffer is made writable.</span></span> <span data-ttu-id="66356-123">Quando viene visualizzato uno zero, il bit è protetto da scrittura.</span><span class="sxs-lookup"><span data-stu-id="66356-123">Where a zero appears, the bit is write-protected.</span></span> <span data-ttu-id="66356-124">Inizialmente, tutti i bit sono abilitati per la scrittura.</span><span class="sxs-lookup"><span data-stu-id="66356-124">Initially, all bits are enabled for writing.</span></span>

<span data-ttu-id="66356-125">Le funzioni seguenti consentono di recuperare informazioni correlate a **glStencilMask**:</span><span class="sxs-lookup"><span data-stu-id="66356-125">The following functions retrieve information related to **glStencilMask**:</span></span>

<span data-ttu-id="66356-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con l'argomento GL \_ stencil \_ WRITEMASK</span><span class="sxs-lookup"><span data-stu-id="66356-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_STENCIL\_WRITEMASK</span></span>

<span data-ttu-id="66356-127">glGet con \_ bit stencil GL \_ argomento</span><span class="sxs-lookup"><span data-stu-id="66356-127">glGet with argument GL\_STENCIL\_BITS</span></span>

## <a name="requirements"></a><span data-ttu-id="66356-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66356-128">Requirements</span></span>



| <span data-ttu-id="66356-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="66356-129">Requirement</span></span> | <span data-ttu-id="66356-130">Valore</span><span class="sxs-lookup"><span data-stu-id="66356-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="66356-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66356-131">Minimum supported client</span></span><br/> | <span data-ttu-id="66356-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="66356-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="66356-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66356-133">Minimum supported server</span></span><br/> | <span data-ttu-id="66356-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="66356-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="66356-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="66356-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="66356-136"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="66356-136"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="66356-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="66356-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="66356-138"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="66356-138"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="66356-139">DLL</span><span class="sxs-lookup"><span data-stu-id="66356-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66356-140"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66356-140"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66356-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="66356-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66356-142">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="66356-142">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="66356-143">**glColorMask**</span><span class="sxs-lookup"><span data-stu-id="66356-143">**glColorMask**</span></span>](glcolormask.md)
</dt> <dt>

[<span data-ttu-id="66356-144">**glDepthMask**</span><span class="sxs-lookup"><span data-stu-id="66356-144">**glDepthMask**</span></span>](gldepthmask.md)
</dt> <dt>

[<span data-ttu-id="66356-145">**Remo**</span><span class="sxs-lookup"><span data-stu-id="66356-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="66356-146">**glIndexMask**</span><span class="sxs-lookup"><span data-stu-id="66356-146">**glIndexMask**</span></span>](glindexmask.md)
</dt> <dt>

[<span data-ttu-id="66356-147">**glStencilFunc**</span><span class="sxs-lookup"><span data-stu-id="66356-147">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> <dt>

[<span data-ttu-id="66356-148">**glStencilOp**</span><span class="sxs-lookup"><span data-stu-id="66356-148">**glStencilOp**</span></span>](glstencilop.md)
</dt> </dl>

 

 





