---
title: funzione glClearColor (GL. h)
description: La funzione glClearColor specifica i valori Clear per i buffer dei colori.
ms.assetid: f938e3f4-9db3-4c24-97ae-531b6799224e
keywords:
- funzione glClearColor OpenGL
topic_type:
- apiref
api_name:
- glClearColor
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34005ce34900f5fee8a4c9b2f1b963b7fe4bb6d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741938"
---
# <a name="glclearcolor-function"></a><span data-ttu-id="ee287-104">glClearColor (funzione)</span><span class="sxs-lookup"><span data-stu-id="ee287-104">glClearColor function</span></span>

<span data-ttu-id="ee287-105">La funzione **glClearColor** specifica i valori Clear per i buffer dei colori.</span><span class="sxs-lookup"><span data-stu-id="ee287-105">The **glClearColor** function specifies clear values for the color buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee287-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ee287-106">Syntax</span></span>


```C++
void WINAPI glClearColor(
   GLclampf red,
   GLclampf green,
   GLclampf blue,
   GLclampf alpha
);
```



## <a name="parameters"></a><span data-ttu-id="ee287-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ee287-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee287-108">*Red*</span><span class="sxs-lookup"><span data-stu-id="ee287-108">*red*</span></span> 
</dt> <dd>

<span data-ttu-id="ee287-109">Valore rosso utilizzato da [**glClear**](glclear.md) per cancellare i buffer dei colori.</span><span class="sxs-lookup"><span data-stu-id="ee287-109">The red value that [**glClear**](glclear.md) uses to clear the color buffers.</span></span> <span data-ttu-id="ee287-110">Il valore predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="ee287-110">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="ee287-111">*verde*</span><span class="sxs-lookup"><span data-stu-id="ee287-111">*green*</span></span> 
</dt> <dd>

<span data-ttu-id="ee287-112">Valore verde utilizzato da [**glClear**](glclear.md) per cancellare i buffer dei colori.</span><span class="sxs-lookup"><span data-stu-id="ee287-112">The green value that [**glClear**](glclear.md) uses to clear the color buffers.</span></span> <span data-ttu-id="ee287-113">Il valore predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="ee287-113">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="ee287-114">*blu*</span><span class="sxs-lookup"><span data-stu-id="ee287-114">*blue*</span></span> 
</dt> <dd>

<span data-ttu-id="ee287-115">Valore blu usato da [**glClear**](glclear.md) per cancellare i buffer dei colori.</span><span class="sxs-lookup"><span data-stu-id="ee287-115">The blue value that [**glClear**](glclear.md) uses to clear the color buffers.</span></span> <span data-ttu-id="ee287-116">Il valore predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="ee287-116">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="ee287-117">*Alfa*</span><span class="sxs-lookup"><span data-stu-id="ee287-117">*alpha*</span></span> 
</dt> <dd>

<span data-ttu-id="ee287-118">Valore alfa usato da [**glClear**](glclear.md) per cancellare i buffer dei colori.</span><span class="sxs-lookup"><span data-stu-id="ee287-118">The alpha value that [**glClear**](glclear.md) uses to clear the color buffers.</span></span> <span data-ttu-id="ee287-119">Il valore predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="ee287-119">The default value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee287-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ee287-120">Return value</span></span>

<span data-ttu-id="ee287-121">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="ee287-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ee287-122">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="ee287-122">Error codes</span></span>

<span data-ttu-id="ee287-123">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="ee287-123">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="ee287-124">Nome</span><span class="sxs-lookup"><span data-stu-id="ee287-124">Name</span></span>                                                                                                  | <span data-ttu-id="ee287-125">Significato</span><span class="sxs-lookup"><span data-stu-id="ee287-125">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ee287-126"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ee287-126"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="ee287-127">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="ee287-127">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ee287-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee287-128">Remarks</span></span>

<span data-ttu-id="ee287-129">La funzione **glClearColor** specifica i valori rosso, verde, blu e alfa usati da [**glClear**](glclear.md) per cancellare i buffer dei colori.</span><span class="sxs-lookup"><span data-stu-id="ee287-129">The **glClearColor** function specifies the red, green, blue, and alpha values used by [**glClear**](glclear.md) to clear the color buffers.</span></span> <span data-ttu-id="ee287-130">I valori specificati da **glClearColor** vengono bloccati nell'intervallo compreso tra \[ 0 e 1 \] .</span><span class="sxs-lookup"><span data-stu-id="ee287-130">Values specified by **glClearColor** are clamped to the range \[0,1\].</span></span>

<span data-ttu-id="ee287-131">Le funzioni seguenti consentono di recuperare informazioni correlate alla funzione **glClearColor** :</span><span class="sxs-lookup"><span data-stu-id="ee287-131">The following functions retrieve information related to the **glClearColor** function:</span></span>

<span data-ttu-id="ee287-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con l'argomento contabilità GL \_ \_ Clear \_ value</span><span class="sxs-lookup"><span data-stu-id="ee287-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ACCUM\_CLEAR\_VALUE</span></span>

<span data-ttu-id="ee287-133">**glGet** con valore di \_ cancellazione del colore GL argomento \_ \_</span><span class="sxs-lookup"><span data-stu-id="ee287-133">**glGet** with argument GL\_COLOR\_CLEAR\_VALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="ee287-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee287-134">Requirements</span></span>



| <span data-ttu-id="ee287-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee287-135">Requirement</span></span> | <span data-ttu-id="ee287-136">Valore</span><span class="sxs-lookup"><span data-stu-id="ee287-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee287-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee287-137">Minimum supported client</span></span><br/> | <span data-ttu-id="ee287-138">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ee287-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ee287-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee287-139">Minimum supported server</span></span><br/> | <span data-ttu-id="ee287-140">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ee287-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ee287-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ee287-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee287-142"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee287-142"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ee287-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="ee287-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="ee287-144"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee287-144"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ee287-145">DLL</span><span class="sxs-lookup"><span data-stu-id="ee287-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee287-146"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee287-146"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee287-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ee287-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee287-148">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="ee287-148">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="ee287-149">**glClear**</span><span class="sxs-lookup"><span data-stu-id="ee287-149">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="ee287-150">**Remo**</span><span class="sxs-lookup"><span data-stu-id="ee287-150">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="ee287-151">**glGet**</span><span class="sxs-lookup"><span data-stu-id="ee287-151">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





