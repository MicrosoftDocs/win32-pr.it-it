---
title: funzione glClearAccum (GL. h)
description: La funzione glClearAccum specifica i valori Clear per il buffer di accumulo.
ms.assetid: 77d8f340-be47-43f4-96fc-31025a4c8b4e
keywords:
- funzione glClearAccum OpenGL
topic_type:
- apiref
api_name:
- glClearAccum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3098e87a47509b8c05035171a8f31e57d8618424
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120070"
---
# <a name="glclearaccum-function"></a><span data-ttu-id="0b830-104">glClearAccum (funzione)</span><span class="sxs-lookup"><span data-stu-id="0b830-104">glClearAccum function</span></span>

<span data-ttu-id="0b830-105">La funzione **glClearAccum** specifica i valori Clear per il buffer di accumulo.</span><span class="sxs-lookup"><span data-stu-id="0b830-105">The **glClearAccum** function specifies the clear values for the accumulation buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b830-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b830-106">Syntax</span></span>


```C++
void WINAPI glClearAccum(
   GLfloat red,
   GLfloat green,
   GLfloat blue,
   GLfloat alpha
);
```



## <a name="parameters"></a><span data-ttu-id="0b830-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="0b830-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b830-108">*Red*</span><span class="sxs-lookup"><span data-stu-id="0b830-108">*red*</span></span> 
</dt> <dd>

<span data-ttu-id="0b830-109">Valore rosso utilizzato quando il buffer di accumulo viene cancellato.</span><span class="sxs-lookup"><span data-stu-id="0b830-109">The red value used when the accumulation buffer is cleared.</span></span> <span data-ttu-id="0b830-110">Il valore predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="0b830-110">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="0b830-111">*verde*</span><span class="sxs-lookup"><span data-stu-id="0b830-111">*green*</span></span> 
</dt> <dd>

<span data-ttu-id="0b830-112">Valore verde utilizzato quando il buffer di accumulo viene cancellato.</span><span class="sxs-lookup"><span data-stu-id="0b830-112">The green value used when the accumulation buffer is cleared.</span></span> <span data-ttu-id="0b830-113">Il valore predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="0b830-113">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="0b830-114">*blu*</span><span class="sxs-lookup"><span data-stu-id="0b830-114">*blue*</span></span> 
</dt> <dd>

<span data-ttu-id="0b830-115">Valore blu utilizzato quando il buffer di accumulo viene cancellato.</span><span class="sxs-lookup"><span data-stu-id="0b830-115">The blue value used when the accumulation buffer is cleared.</span></span> <span data-ttu-id="0b830-116">Il valore predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="0b830-116">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="0b830-117">*Alfa*</span><span class="sxs-lookup"><span data-stu-id="0b830-117">*alpha*</span></span> 
</dt> <dd>

<span data-ttu-id="0b830-118">Valore alfa utilizzato quando il buffer di accumulo viene cancellato.</span><span class="sxs-lookup"><span data-stu-id="0b830-118">The alpha value used when the accumulation buffer is cleared.</span></span> <span data-ttu-id="0b830-119">Il valore predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="0b830-119">The default value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b830-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0b830-120">Return value</span></span>

<span data-ttu-id="0b830-121">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="0b830-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0b830-122">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="0b830-122">Error codes</span></span>

<span data-ttu-id="0b830-123">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="0b830-123">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="0b830-124">Nome</span><span class="sxs-lookup"><span data-stu-id="0b830-124">Name</span></span>                                                                                                  | <span data-ttu-id="0b830-125">Significato</span><span class="sxs-lookup"><span data-stu-id="0b830-125">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0b830-126"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0b830-126"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="0b830-127">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="0b830-127">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0b830-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="0b830-128">Remarks</span></span>

<span data-ttu-id="0b830-129">La funzione **glClearAccum** specifica i valori rosso, verde, blu e alfa usati da [**glClear**](glclear.md) per cancellare il buffer di accumulo.</span><span class="sxs-lookup"><span data-stu-id="0b830-129">The **glClearAccum** function specifies the red, green, blue, and alpha values used by [**glClear**](glclear.md) to clear the accumulation buffer.</span></span>

<span data-ttu-id="0b830-130">I valori specificati da **glClearAccum** vengono bloccati nell'intervallo \[ 1, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="0b830-130">Values specified by **glClearAccum** are clamped to the range \[1,1\].</span></span>

<span data-ttu-id="0b830-131">La funzione seguente recupera le informazioni correlate a **glClearAccum**:</span><span class="sxs-lookup"><span data-stu-id="0b830-131">The following function retrieves information related to **glClearAccum**:</span></span>

<span data-ttu-id="0b830-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con l'argomento contabilità GL \_ \_ Clear \_ value</span><span class="sxs-lookup"><span data-stu-id="0b830-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ACCUM\_CLEAR\_VALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="0b830-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b830-133">Requirements</span></span>



| <span data-ttu-id="0b830-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b830-134">Requirement</span></span> | <span data-ttu-id="0b830-135">Valore</span><span class="sxs-lookup"><span data-stu-id="0b830-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b830-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b830-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0b830-137">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0b830-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0b830-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b830-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0b830-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0b830-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0b830-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0b830-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b830-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b830-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="0b830-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="0b830-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="0b830-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b830-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="0b830-144">DLL</span><span class="sxs-lookup"><span data-stu-id="0b830-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b830-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b830-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b830-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b830-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b830-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="0b830-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="0b830-148">**glClear**</span><span class="sxs-lookup"><span data-stu-id="0b830-148">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="0b830-149">**Remo**</span><span class="sxs-lookup"><span data-stu-id="0b830-149">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="0b830-150">**glGet**</span><span class="sxs-lookup"><span data-stu-id="0b830-150">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





