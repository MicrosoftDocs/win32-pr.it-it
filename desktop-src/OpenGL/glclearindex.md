---
title: funzione glClearIndex (GL. h)
description: La funzione glClearIndex specifica il valore Clear per i buffer di indice dei colori.
ms.assetid: 87983d93-c5a1-445f-8621-1c2952d93a0f
keywords:
- funzione glClearIndex OpenGL
topic_type:
- apiref
api_name:
- glClearIndex
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85b1ed90b017828e13d387e1e6db440c1d781cb5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477242"
---
# <a name="glclearindex-function"></a><span data-ttu-id="6f8dc-104">glClearIndex (funzione)</span><span class="sxs-lookup"><span data-stu-id="6f8dc-104">glClearIndex function</span></span>

<span data-ttu-id="6f8dc-105">La funzione **glClearIndex** specifica il valore Clear per i buffer di indice dei colori.</span><span class="sxs-lookup"><span data-stu-id="6f8dc-105">The **glClearIndex** function specifies the clear value for the color-index buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f8dc-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6f8dc-106">Syntax</span></span>


```C++
void WINAPI glClearIndex(
   GLfloat c
);
```



## <a name="parameters"></a><span data-ttu-id="6f8dc-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="6f8dc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f8dc-108">*c*</span><span class="sxs-lookup"><span data-stu-id="6f8dc-108">*c*</span></span> 
</dt> <dd>

<span data-ttu-id="6f8dc-109">Indice utilizzato quando i buffer dell'indice dei colori vengono cancellati.</span><span class="sxs-lookup"><span data-stu-id="6f8dc-109">The index used when the color-index buffers are cleared.</span></span> <span data-ttu-id="6f8dc-110">Il valore predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="6f8dc-110">The default value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f8dc-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6f8dc-111">Return value</span></span>

<span data-ttu-id="6f8dc-112">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="6f8dc-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6f8dc-113">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="6f8dc-113">Error codes</span></span>

<span data-ttu-id="6f8dc-114">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="6f8dc-114">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="6f8dc-115">Nome</span><span class="sxs-lookup"><span data-stu-id="6f8dc-115">Name</span></span>                                                                                                  | <span data-ttu-id="6f8dc-116">Significato</span><span class="sxs-lookup"><span data-stu-id="6f8dc-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6f8dc-117"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6f8dc-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="6f8dc-118">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="6f8dc-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6f8dc-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="6f8dc-119">Remarks</span></span>

<span data-ttu-id="6f8dc-120">La funzione **glClearIndex** specifica l'indice usato da [**glClear**](glclear.md) per cancellare i buffer dell'indice dei colori.</span><span class="sxs-lookup"><span data-stu-id="6f8dc-120">The **glClearIndex** function specifies the index used by [**glClear**](glclear.md) to clear the color-index buffers.</span></span> <span data-ttu-id="6f8dc-121">Il parametro *c* non è stato bloccato.</span><span class="sxs-lookup"><span data-stu-id="6f8dc-121">The *c* parameter is not clamped.</span></span> <span data-ttu-id="6f8dc-122">Il linguaggio *c* viene invece convertito in un valore a virgola fissa con una precisione non specificata a destra del punto binario.</span><span class="sxs-lookup"><span data-stu-id="6f8dc-122">Rather, *c* is converted to a fixed-point value with unspecified precision to the right of the binary point.</span></span> <span data-ttu-id="6f8dc-123">La parte intera di questo valore viene quindi mascherata con 2 <sup>m</sup>  -1, dove *m* è il numero di bit in un indice dei colori archiviato nel framebuffer.</span><span class="sxs-lookup"><span data-stu-id="6f8dc-123">The integer part of this value is then masked with 2 <sup>m</sup>  - 1, where *m* is the number of bits in a color index stored in the framebuffer.</span></span>

<span data-ttu-id="6f8dc-124">Le funzioni seguenti consentono di recuperare informazioni correlate a **glClearIndex**:</span><span class="sxs-lookup"><span data-stu-id="6f8dc-124">The following functions retrieve information related to **glClearIndex**:</span></span>

<span data-ttu-id="6f8dc-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con valore di \_ cancellazione dell'indice GL dell'argomento \_ \_</span><span class="sxs-lookup"><span data-stu-id="6f8dc-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_INDEX\_CLEAR\_VALUE</span></span>

<span data-ttu-id="6f8dc-126">**glGet** con bit di indice GL dell'argomento \_ \_</span><span class="sxs-lookup"><span data-stu-id="6f8dc-126">**glGet** with argument GL\_INDEX\_BITS</span></span>

## <a name="requirements"></a><span data-ttu-id="6f8dc-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f8dc-127">Requirements</span></span>



| <span data-ttu-id="6f8dc-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f8dc-128">Requirement</span></span> | <span data-ttu-id="6f8dc-129">Valore</span><span class="sxs-lookup"><span data-stu-id="6f8dc-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f8dc-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f8dc-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6f8dc-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6f8dc-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6f8dc-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f8dc-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6f8dc-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6f8dc-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6f8dc-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6f8dc-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f8dc-135"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f8dc-135"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6f8dc-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="6f8dc-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="6f8dc-137"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f8dc-137"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6f8dc-138">DLL</span><span class="sxs-lookup"><span data-stu-id="6f8dc-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f8dc-139"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f8dc-139"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f8dc-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6f8dc-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f8dc-141">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="6f8dc-141">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="6f8dc-142">**glClear**</span><span class="sxs-lookup"><span data-stu-id="6f8dc-142">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="6f8dc-143">**Remo**</span><span class="sxs-lookup"><span data-stu-id="6f8dc-143">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="6f8dc-144">**glGet**</span><span class="sxs-lookup"><span data-stu-id="6f8dc-144">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





