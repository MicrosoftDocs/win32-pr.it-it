---
title: funzione glMatrixMode (GL. h)
description: La funzione glMatrixMode specifica quale matrice è la matrice corrente.
ms.assetid: f1006ea3-322a-42a9-b33c-6c7181985ef9
keywords:
- funzione glMatrixMode OpenGL
topic_type:
- apiref
api_name:
- glMatrixMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9877d62fc6e721cc6757206c7c2d07d24f3e879b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120438"
---
# <a name="glmatrixmode-function"></a><span data-ttu-id="7acd0-104">glMatrixMode (funzione)</span><span class="sxs-lookup"><span data-stu-id="7acd0-104">glMatrixMode function</span></span>

<span data-ttu-id="7acd0-105">La funzione **glMatrixMode** specifica quale matrice è la matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="7acd0-105">The **glMatrixMode** function specifies which matrix is the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="7acd0-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7acd0-106">Syntax</span></span>


```C++
void WINAPI glMatrixMode(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="7acd0-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="7acd0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7acd0-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="7acd0-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="7acd0-109">Stack matrice che rappresenta la destinazione per le successive operazioni di matrice.</span><span class="sxs-lookup"><span data-stu-id="7acd0-109">The matrix stack that is the target for subsequent matrix operations.</span></span> <span data-ttu-id="7acd0-110">Il parametro *mode* può assumere uno dei tre valori.</span><span class="sxs-lookup"><span data-stu-id="7acd0-110">The *mode* parameter can assume one of three values.</span></span>



| <span data-ttu-id="7acd0-111">Valore</span><span class="sxs-lookup"><span data-stu-id="7acd0-111">Value</span></span>                                                                                                                                                         | <span data-ttu-id="7acd0-112">Significato</span><span class="sxs-lookup"><span data-stu-id="7acd0-112">Meaning</span></span>                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="GL_MODELVIEW"></span><span id="gl_modelview"></span><dl> <span data-ttu-id="7acd0-113"><dt>**\_MODELVIEW GL**</dt></span><span class="sxs-lookup"><span data-stu-id="7acd0-113"><dt>**GL\_MODELVIEW**</dt></span></span> </dl>    | <span data-ttu-id="7acd0-114">Applica le successive operazioni della matrice allo stack della matrice Modelview.</span><span class="sxs-lookup"><span data-stu-id="7acd0-114">Applies subsequent matrix operations to the modelview matrix stack.</span></span><br/>  |
| <span id="GL_PROJECTION"></span><span id="gl_projection"></span><dl> <span data-ttu-id="7acd0-115"><dt>**\_proiezione GL**</dt></span><span class="sxs-lookup"><span data-stu-id="7acd0-115"><dt>**GL\_PROJECTION**</dt></span></span> </dl> | <span data-ttu-id="7acd0-116">Applica le successive operazioni della matrice allo stack della matrice di proiezione.</span><span class="sxs-lookup"><span data-stu-id="7acd0-116">Applies subsequent matrix operations to the projection matrix stack.</span></span><br/> |
| <span id="GL_TEXTURE"></span><span id="gl_texture"></span><dl> <span data-ttu-id="7acd0-117"><dt>**\_trama GL**</dt></span><span class="sxs-lookup"><span data-stu-id="7acd0-117"><dt>**GL\_TEXTURE**</dt></span></span> </dl>          | <span data-ttu-id="7acd0-118">Applica le successive operazioni della matrice allo stack della matrice di trame.</span><span class="sxs-lookup"><span data-stu-id="7acd0-118">Applies subsequent matrix operations to the texture matrix stack.</span></span><br/>    |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7acd0-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7acd0-119">Return value</span></span>

<span data-ttu-id="7acd0-120">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="7acd0-120">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7acd0-121">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="7acd0-121">Error codes</span></span>

<span data-ttu-id="7acd0-122">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="7acd0-122">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="7acd0-123">Nome</span><span class="sxs-lookup"><span data-stu-id="7acd0-123">Name</span></span>                                                                                                  | <span data-ttu-id="7acd0-124">Significato</span><span class="sxs-lookup"><span data-stu-id="7acd0-124">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7acd0-125"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7acd0-125"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="7acd0-126">la *modalità* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="7acd0-126">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="7acd0-127"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7acd0-127"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="7acd0-128">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="7acd0-128">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7acd0-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="7acd0-129">Remarks</span></span>

<span data-ttu-id="7acd0-130">La funzione **glMatrixMode** imposta la modalità della matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="7acd0-130">The **glMatrixMode** function sets the current matrix mode.</span></span>

<span data-ttu-id="7acd0-131">La funzione seguente recupera le informazioni correlate a **glMatrixMode**:</span><span class="sxs-lookup"><span data-stu-id="7acd0-131">The following function retrieves information related to **glMatrixMode**:</span></span>

<span data-ttu-id="7acd0-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento della \_ modalità matrice GL \_</span><span class="sxs-lookup"><span data-stu-id="7acd0-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="7acd0-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7acd0-133">Requirements</span></span>



| <span data-ttu-id="7acd0-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="7acd0-134">Requirement</span></span> | <span data-ttu-id="7acd0-135">Valore</span><span class="sxs-lookup"><span data-stu-id="7acd0-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7acd0-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7acd0-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7acd0-137">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7acd0-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7acd0-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7acd0-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7acd0-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7acd0-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7acd0-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7acd0-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="7acd0-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="7acd0-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="7acd0-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="7acd0-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="7acd0-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7acd0-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7acd0-144">DLL</span><span class="sxs-lookup"><span data-stu-id="7acd0-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7acd0-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7acd0-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7acd0-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7acd0-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7acd0-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="7acd0-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="7acd0-148">**Remo**</span><span class="sxs-lookup"><span data-stu-id="7acd0-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="7acd0-149">**glLoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="7acd0-149">**glLoadMatrix**</span></span>](glloadmatrix.md)
</dt> <dt>

[<span data-ttu-id="7acd0-150">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="7acd0-150">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





