---
title: funzione glClearDepth (GL. h)
description: La funzione glClearDepth specifica il valore Clear per il buffer di profondità.
ms.assetid: 8e26ae78-edc1-4201-a0db-d5bc8ae6dc82
keywords:
- funzione glClearDepth OpenGL
topic_type:
- apiref
api_name:
- glClearDepth
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cf968c7ae172bf4ce354c84b2071d62304327ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340782"
---
# <a name="glcleardepth-function"></a><span data-ttu-id="28a16-104">glClearDepth (funzione)</span><span class="sxs-lookup"><span data-stu-id="28a16-104">glClearDepth function</span></span>

<span data-ttu-id="28a16-105">La funzione **glClearDepth** specifica il valore Clear per il buffer di profondità.</span><span class="sxs-lookup"><span data-stu-id="28a16-105">The **glClearDepth** function specifies the clear value for the depth buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="28a16-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="28a16-106">Syntax</span></span>


```C++
void WINAPI glClearDepth(
   GLclampd depth
);
```



## <a name="parameters"></a><span data-ttu-id="28a16-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="28a16-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28a16-108">*profondità*</span><span class="sxs-lookup"><span data-stu-id="28a16-108">*depth*</span></span> 
</dt> <dd>

<span data-ttu-id="28a16-109">Valore di profondità utilizzato quando il buffer di profondità viene cancellato.</span><span class="sxs-lookup"><span data-stu-id="28a16-109">The depth value used when the depth buffer is cleared.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28a16-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="28a16-110">Return value</span></span>

<span data-ttu-id="28a16-111">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="28a16-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="28a16-112">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="28a16-112">Error codes</span></span>

<span data-ttu-id="28a16-113">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="28a16-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="28a16-114">Nome</span><span class="sxs-lookup"><span data-stu-id="28a16-114">Name</span></span>                                                                                                  | <span data-ttu-id="28a16-115">Significato</span><span class="sxs-lookup"><span data-stu-id="28a16-115">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="28a16-116"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="28a16-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="28a16-117">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="28a16-117">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="28a16-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="28a16-118">Remarks</span></span>

<span data-ttu-id="28a16-119">La funzione **glClearDepth** specifica il valore Depth usato da [**glClear**](glclear.md) per cancellare il buffer di profondità.</span><span class="sxs-lookup"><span data-stu-id="28a16-119">The **glClearDepth** function specifies the depth value used by [**glClear**](glclear.md) to clear the depth buffer.</span></span> <span data-ttu-id="28a16-120">I valori specificati da **glClearDepth** vengono bloccati nell'intervallo compreso tra \[ 0 e 1 \] .</span><span class="sxs-lookup"><span data-stu-id="28a16-120">Values specified by **glClearDepth** are clamped to the range \[0,1\].</span></span>

<span data-ttu-id="28a16-121">La funzione seguente recupera le informazioni correlate alla funzione **glClearDepth** :</span><span class="sxs-lookup"><span data-stu-id="28a16-121">The following function retrieves information related to the **glClearDepth** function:</span></span>

<span data-ttu-id="28a16-122">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con \_ \_ valore Clear Depth Depth \_</span><span class="sxs-lookup"><span data-stu-id="28a16-122">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_DEPTH\_CLEAR\_VALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="28a16-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="28a16-123">Requirements</span></span>



| <span data-ttu-id="28a16-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="28a16-124">Requirement</span></span> | <span data-ttu-id="28a16-125">Valore</span><span class="sxs-lookup"><span data-stu-id="28a16-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28a16-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28a16-126">Minimum supported client</span></span><br/> | <span data-ttu-id="28a16-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="28a16-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="28a16-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28a16-128">Minimum supported server</span></span><br/> | <span data-ttu-id="28a16-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="28a16-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="28a16-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="28a16-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="28a16-131"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="28a16-131"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="28a16-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="28a16-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="28a16-133"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="28a16-133"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="28a16-134">DLL</span><span class="sxs-lookup"><span data-stu-id="28a16-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28a16-135"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28a16-135"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28a16-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="28a16-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28a16-137">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="28a16-137">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="28a16-138">**glClear**</span><span class="sxs-lookup"><span data-stu-id="28a16-138">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="28a16-139">**Remo**</span><span class="sxs-lookup"><span data-stu-id="28a16-139">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="28a16-140">**glGet**</span><span class="sxs-lookup"><span data-stu-id="28a16-140">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





