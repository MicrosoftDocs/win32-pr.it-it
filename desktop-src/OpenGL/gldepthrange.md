---
title: funzione glDepthRange (GL. h)
description: La funzione glDepthRange specifica il mapping dei valori z dalle coordinate del dispositivo normalizzate alle coordinate della finestra.
ms.assetid: 44aed5e5-4bd2-4e7f-ad05-1cf4be5254a5
keywords:
- funzione glDepthRange OpenGL
topic_type:
- apiref
api_name:
- glDepthRange
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0bd6a22ae91877c9b20fa5387edd9438942a07d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400422"
---
# <a name="gldepthrange-function"></a><span data-ttu-id="cfec2-104">glDepthRange (funzione)</span><span class="sxs-lookup"><span data-stu-id="cfec2-104">glDepthRange function</span></span>

<span data-ttu-id="cfec2-105">La funzione **glDepthRange** specifica il mapping dei valori *z* dalle coordinate del dispositivo normalizzate alle coordinate della finestra.</span><span class="sxs-lookup"><span data-stu-id="cfec2-105">The **glDepthRange** function specifies the mapping of *z* values from normalized device coordinates to window coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfec2-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cfec2-106">Syntax</span></span>


```C++
void WINAPI glDepthRange(
   GLclampd zNear,
   GLclampd zFar
);
```



## <a name="parameters"></a><span data-ttu-id="cfec2-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="cfec2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfec2-108">*zNear*</span><span class="sxs-lookup"><span data-stu-id="cfec2-108">*zNear*</span></span> 
</dt> <dd>

<span data-ttu-id="cfec2-109">Mapping del piano di ritaglio vicino alle coordinate della finestra.</span><span class="sxs-lookup"><span data-stu-id="cfec2-109">The mapping of the near clipping plane to window coordinates.</span></span> <span data-ttu-id="cfec2-110">Il valore predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="cfec2-110">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="cfec2-111">*zFar*</span><span class="sxs-lookup"><span data-stu-id="cfec2-111">*zFar*</span></span> 
</dt> <dd>

<span data-ttu-id="cfec2-112">Mapping del piano di ritaglio estremo alle coordinate della finestra.</span><span class="sxs-lookup"><span data-stu-id="cfec2-112">The mapping of the far clipping plane to window coordinates.</span></span> <span data-ttu-id="cfec2-113">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="cfec2-113">The default value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfec2-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cfec2-114">Return value</span></span>

<span data-ttu-id="cfec2-115">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="cfec2-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cfec2-116">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="cfec2-116">Error codes</span></span>

<span data-ttu-id="cfec2-117">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="cfec2-117">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="cfec2-118">Nome</span><span class="sxs-lookup"><span data-stu-id="cfec2-118">Name</span></span>                                                                                                  | <span data-ttu-id="cfec2-119">Significato</span><span class="sxs-lookup"><span data-stu-id="cfec2-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cfec2-120"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cfec2-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="cfec2-121">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="cfec2-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="cfec2-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="cfec2-122">Remarks</span></span>

<span data-ttu-id="cfec2-123">Dopo il ritaglio e la divisione per *w*, le coordinate *z* variano da 0,0 a 1,0, corrispondenti ai piani di ritaglio vicini e lontani.</span><span class="sxs-lookup"><span data-stu-id="cfec2-123">After clipping and division by *w*, *z* -coordinates range from 0.0 to 1.0, corresponding to the near and far clipping planes.</span></span> <span data-ttu-id="cfec2-124">La funzione **glDepthRange** specifica un mapping lineare delle coordinate *z* normalizzate in questo intervallo alla finestra *z*-coordinates.</span><span class="sxs-lookup"><span data-stu-id="cfec2-124">The **glDepthRange** function specifies a linear mapping of the normalized *z*-coordinates in this range to window *z*-coordinates.</span></span> <span data-ttu-id="cfec2-125">Indipendentemente dall'implementazione effettiva del buffer di profondità, i valori di profondità delle coordinate della finestra vengono considerati come se fossero compresi tra 0,0 e 1,0 (ad esempio, i componenti dei colori).</span><span class="sxs-lookup"><span data-stu-id="cfec2-125">Regardless of the actual depth buffer implementation, window coordinate depth values are treated as though they range from 0.0 through 1.0 (like color components).</span></span> <span data-ttu-id="cfec2-126">Pertanto, i valori accettati da **glDepthRange** vengono entrambi fissati a questo intervallo prima che vengano accettati.</span><span class="sxs-lookup"><span data-stu-id="cfec2-126">Thus, the values accepted by **glDepthRange** are both clamped to this range before they are accepted.</span></span>

<span data-ttu-id="cfec2-127">Il mapping predefinito di (0, 1) esegue il mapping del piano vicino a 0 e del piano lontano a 1.</span><span class="sxs-lookup"><span data-stu-id="cfec2-127">The default mapping of (0,1) maps the near plane to 0 and the far plane to 1.</span></span> <span data-ttu-id="cfec2-128">Con questo mapping, l'intervallo di buffer di profondità viene utilizzato completamente.</span><span class="sxs-lookup"><span data-stu-id="cfec2-128">With this mapping, the depth buffer range is fully utilized.</span></span>

<span data-ttu-id="cfec2-129">Non è necessario che *zNear* sia minore di *zFar*.</span><span class="sxs-lookup"><span data-stu-id="cfec2-129">It is not necessary that *zNear* be less than *zFar*.</span></span> <span data-ttu-id="cfec2-130">I mapping inversi, ad esempio (1, 0), sono accettabili.</span><span class="sxs-lookup"><span data-stu-id="cfec2-130">Reverse mappings such as (1,0) are acceptable.</span></span>

<span data-ttu-id="cfec2-131">La funzione seguente recupera le informazioni correlate a **glDepthRange**:</span><span class="sxs-lookup"><span data-stu-id="cfec2-131">The following function retrieves information related to **glDepthRange**:</span></span>

<span data-ttu-id="cfec2-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con intervallo di \_ profondità GL argomento \_</span><span class="sxs-lookup"><span data-stu-id="cfec2-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_DEPTH\_RANGE</span></span>

## <a name="requirements"></a><span data-ttu-id="cfec2-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cfec2-133">Requirements</span></span>



| <span data-ttu-id="cfec2-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfec2-134">Requirement</span></span> | <span data-ttu-id="cfec2-135">Valore</span><span class="sxs-lookup"><span data-stu-id="cfec2-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cfec2-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cfec2-136">Minimum supported client</span></span><br/> | <span data-ttu-id="cfec2-137">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cfec2-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="cfec2-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cfec2-138">Minimum supported server</span></span><br/> | <span data-ttu-id="cfec2-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cfec2-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cfec2-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cfec2-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfec2-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfec2-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="cfec2-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="cfec2-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="cfec2-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cfec2-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="cfec2-144">DLL</span><span class="sxs-lookup"><span data-stu-id="cfec2-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfec2-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfec2-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfec2-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cfec2-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfec2-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="cfec2-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="cfec2-148">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="cfec2-148">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="cfec2-149">**Remo**</span><span class="sxs-lookup"><span data-stu-id="cfec2-149">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="cfec2-150">**glGet**</span><span class="sxs-lookup"><span data-stu-id="cfec2-150">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="cfec2-151">**glViewport**</span><span class="sxs-lookup"><span data-stu-id="cfec2-151">**glViewport**</span></span>](glviewport.md)
</dt> </dl>

 

 





