---
title: funzione glClearStencil (GL. h)
description: La funzione glClearStencil specifica il valore Clear per il buffer dello stencil.
ms.assetid: bbde8fa8-78f3-45bd-bac3-5d03839acc52
keywords:
- funzione glClearStencil OpenGL
topic_type:
- apiref
api_name:
- glClearStencil
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78d831540b4c7833368bbac075835faaec359695
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964356"
---
# <a name="glclearstencil-function"></a><span data-ttu-id="28476-104">glClearStencil (funzione)</span><span class="sxs-lookup"><span data-stu-id="28476-104">glClearStencil function</span></span>

<span data-ttu-id="28476-105">La funzione **glClearStencil** specifica il valore Clear per il buffer dello stencil.</span><span class="sxs-lookup"><span data-stu-id="28476-105">The **glClearStencil** function specifies the clear value for the stencil buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="28476-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="28476-106">Syntax</span></span>


```C++
void WINAPI glClearStencil(
   GLint s
);
```



## <a name="parameters"></a><span data-ttu-id="28476-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="28476-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28476-108">*s*</span><span class="sxs-lookup"><span data-stu-id="28476-108">*s*</span></span> 
</dt> <dd>

<span data-ttu-id="28476-109">Indice utilizzato quando il buffer dello stencil viene cancellato.</span><span class="sxs-lookup"><span data-stu-id="28476-109">The index used when the stencil buffer is cleared.</span></span> <span data-ttu-id="28476-110">Il valore predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="28476-110">The default value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28476-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="28476-111">Return value</span></span>

<span data-ttu-id="28476-112">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="28476-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="28476-113">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="28476-113">Error codes</span></span>

<span data-ttu-id="28476-114">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="28476-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="28476-115">Nome</span><span class="sxs-lookup"><span data-stu-id="28476-115">Name</span></span>                                                                                                  | <span data-ttu-id="28476-116">Significato</span><span class="sxs-lookup"><span data-stu-id="28476-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="28476-117"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="28476-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="28476-118">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="28476-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="28476-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="28476-119">Remarks</span></span>

<span data-ttu-id="28476-120">La funzione **glClearStencil** specifica l'indice utilizzato da [**glClear**](glclear.md) per cancellare il buffer dello stencil.</span><span class="sxs-lookup"><span data-stu-id="28476-120">The **glClearStencil** function specifies the index used by [**glClear**](glclear.md) to clear the stencil buffer.</span></span> <span data-ttu-id="28476-121">Il parametro *s* è mascherato da 2 <sup>m</sup>  -1, dove *m* è il numero di bit nel buffer dello stencil.</span><span class="sxs-lookup"><span data-stu-id="28476-121">The *s* parameter is masked with 2 <sup>m</sup>  - 1, where *m* is the number of bits in the stencil buffer.</span></span>

<span data-ttu-id="28476-122">Le funzioni seguenti consentono di recuperare informazioni correlate alla funzione **glClearStencil** :</span><span class="sxs-lookup"><span data-stu-id="28476-122">The following functions retrieve information related to the **glClearStencil** function:</span></span>

<span data-ttu-id="28476-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con il \_ \_ valore Clear dello stencil GL degli argomenti \_</span><span class="sxs-lookup"><span data-stu-id="28476-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_STENCIL\_CLEAR\_VALUE</span></span>

<span data-ttu-id="28476-124">**glGet** con \_ bit stencil GL \_ argomento</span><span class="sxs-lookup"><span data-stu-id="28476-124">**glGet** with argument GL\_STENCIL\_BITS</span></span>

## <a name="requirements"></a><span data-ttu-id="28476-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="28476-125">Requirements</span></span>



| <span data-ttu-id="28476-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="28476-126">Requirement</span></span> | <span data-ttu-id="28476-127">Valore</span><span class="sxs-lookup"><span data-stu-id="28476-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28476-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28476-128">Minimum supported client</span></span><br/> | <span data-ttu-id="28476-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="28476-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="28476-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28476-130">Minimum supported server</span></span><br/> | <span data-ttu-id="28476-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="28476-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="28476-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="28476-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="28476-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="28476-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="28476-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="28476-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="28476-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="28476-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="28476-136">DLL</span><span class="sxs-lookup"><span data-stu-id="28476-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28476-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28476-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28476-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="28476-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28476-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="28476-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="28476-140">**glClear**</span><span class="sxs-lookup"><span data-stu-id="28476-140">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="28476-141">**Remo**</span><span class="sxs-lookup"><span data-stu-id="28476-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="28476-142">**glGet**</span><span class="sxs-lookup"><span data-stu-id="28476-142">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





