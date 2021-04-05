---
title: funzione glColorMask (GL. h)
description: La funzione glColorMask Abilita e Disabilita la scrittura di componenti colore del buffer dei frame.
ms.assetid: 23d7f94e-f290-423c-a841-f86caf94009d
keywords:
- funzione glColorMask OpenGL
topic_type:
- apiref
api_name:
- glColorMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a9aa36eeceeae4aaa9373d73b50fda09663edb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873505"
---
# <a name="glcolormask-function"></a><span data-ttu-id="17085-104">glColorMask (funzione)</span><span class="sxs-lookup"><span data-stu-id="17085-104">glColorMask function</span></span>

<span data-ttu-id="17085-105">La funzione **glColorMask** Abilita e Disabilita la scrittura di componenti colore del buffer dei frame.</span><span class="sxs-lookup"><span data-stu-id="17085-105">The **glColorMask** function enables and disables writing of frame-buffer color components.</span></span>

## <a name="syntax"></a><span data-ttu-id="17085-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="17085-106">Syntax</span></span>


```C++
void WINAPI glColorMask(
   GLboolean red,
   GLboolean green,
   GLboolean blue,
   GLboolean alpha
);
```



## <a name="parameters"></a><span data-ttu-id="17085-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="17085-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17085-108">*Red*</span><span class="sxs-lookup"><span data-stu-id="17085-108">*red*</span></span> 
</dt> <dd>

<span data-ttu-id="17085-109">Consente di specificare se è possibile o meno scrivere il colore rosso nel framebuffer.</span><span class="sxs-lookup"><span data-stu-id="17085-109">Specify whether red can or cannot be written into the framebuffer.</span></span> <span data-ttu-id="17085-110">I valori predefiniti sono GL \_ true, a indicare che è possibile scrivere il componente color.</span><span class="sxs-lookup"><span data-stu-id="17085-110">The default values is GL\_TRUE, indicating that the color component can be written.</span></span>

</dd> <dt>

<span data-ttu-id="17085-111">*verde*</span><span class="sxs-lookup"><span data-stu-id="17085-111">*green*</span></span> 
</dt> <dd>

<span data-ttu-id="17085-112">Specificare se è possibile o meno scrivere il colore verde nel framebuffer.</span><span class="sxs-lookup"><span data-stu-id="17085-112">Specify whether green can or cannot be written into the framebuffer.</span></span> <span data-ttu-id="17085-113">Il valore predefinito è GL \_ true, a indicare che è possibile scrivere il componente color.</span><span class="sxs-lookup"><span data-stu-id="17085-113">The default value is GL\_TRUE, indicating that the color component can be written.</span></span>

</dd> <dt>

<span data-ttu-id="17085-114">*blu*</span><span class="sxs-lookup"><span data-stu-id="17085-114">*blue*</span></span> 
</dt> <dd>

<span data-ttu-id="17085-115">Consente di specificare se è possibile o meno scrivere il blu nel framebuffer.</span><span class="sxs-lookup"><span data-stu-id="17085-115">Specify whether blue can or cannot be written into the framebuffer.</span></span> <span data-ttu-id="17085-116">Il valore predefinito è GL \_ true, a indicare che è possibile scrivere il componente color.</span><span class="sxs-lookup"><span data-stu-id="17085-116">The default value is GL\_TRUE, indicating that the color component can be written.</span></span>

</dd> <dt>

<span data-ttu-id="17085-117">*Alfa*</span><span class="sxs-lookup"><span data-stu-id="17085-117">*alpha*</span></span> 
</dt> <dd>

<span data-ttu-id="17085-118">Consente di specificare se è possibile o meno scrivere Alpha nel framebuffer.</span><span class="sxs-lookup"><span data-stu-id="17085-118">Specify whether alpha can or cannot be written into the framebuffer.</span></span> <span data-ttu-id="17085-119">Il valore predefinito è GL \_ true, a indicare che è possibile scrivere il componente color.</span><span class="sxs-lookup"><span data-stu-id="17085-119">The default value is GL\_TRUE, indicating that the color component can be written.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17085-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="17085-120">Return value</span></span>

<span data-ttu-id="17085-121">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="17085-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="17085-122">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="17085-122">Error codes</span></span>

<span data-ttu-id="17085-123">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="17085-123">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="17085-124">Nome</span><span class="sxs-lookup"><span data-stu-id="17085-124">Name</span></span>                                                                                                  | <span data-ttu-id="17085-125">Significato</span><span class="sxs-lookup"><span data-stu-id="17085-125">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="17085-126"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="17085-126"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="17085-127">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="17085-127">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="17085-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="17085-128">Remarks</span></span>

<span data-ttu-id="17085-129">La funzione **glColorMask** specifica se i singoli componenti colore nel framebuffer possono o non possono essere scritti.</span><span class="sxs-lookup"><span data-stu-id="17085-129">The **glColorMask** function specifies whether the individual color components in the framebuffer can or cannot be written.</span></span> <span data-ttu-id="17085-130">Se il *colore rosso* è GL \_ false, ad esempio, non viene apportata alcuna modifica al componente rosso di qualsiasi pixel in uno dei buffer dei colori, indipendentemente dall'operazione di disegno tentata.</span><span class="sxs-lookup"><span data-stu-id="17085-130">If *red* is GL\_FALSE, for example, no change is made to the red component of any pixel in any of the color buffers, regardless of the drawing operation attempted.</span></span>

<span data-ttu-id="17085-131">Non è possibile controllare le modifiche apportate a singoli bit di componenti.</span><span class="sxs-lookup"><span data-stu-id="17085-131">Changes to individual bits of components cannot be controlled.</span></span> <span data-ttu-id="17085-132">Le modifiche sono invece abilitate o disabilitate per interi componenti colore.</span><span class="sxs-lookup"><span data-stu-id="17085-132">Rather, changes are either enabled or disabled for entire color components.</span></span>

<span data-ttu-id="17085-133">Le funzioni seguenti consentono di recuperare informazioni correlate a **glColorMask**:</span><span class="sxs-lookup"><span data-stu-id="17085-133">The following functions retrieve information related to **glColorMask**:</span></span>

<span data-ttu-id="17085-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Color \_ WRITEMASK</span><span class="sxs-lookup"><span data-stu-id="17085-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_COLOR\_WRITEMASK</span></span>

<span data-ttu-id="17085-135">**glGet** con argomento GL \_ RGBA \_ mode</span><span class="sxs-lookup"><span data-stu-id="17085-135">**glGet** with argument GL\_RGBA\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="17085-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17085-136">Requirements</span></span>



| <span data-ttu-id="17085-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="17085-137">Requirement</span></span> | <span data-ttu-id="17085-138">Valore</span><span class="sxs-lookup"><span data-stu-id="17085-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17085-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17085-139">Minimum supported client</span></span><br/> | <span data-ttu-id="17085-140">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="17085-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="17085-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17085-141">Minimum supported server</span></span><br/> | <span data-ttu-id="17085-142">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="17085-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="17085-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="17085-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="17085-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="17085-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="17085-145">Libreria</span><span class="sxs-lookup"><span data-stu-id="17085-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="17085-146"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17085-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="17085-147">DLL</span><span class="sxs-lookup"><span data-stu-id="17085-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17085-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17085-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17085-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="17085-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17085-150">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="17085-150">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="17085-151">**glColor**</span><span class="sxs-lookup"><span data-stu-id="17085-151">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="17085-152">**glDepthMask**</span><span class="sxs-lookup"><span data-stu-id="17085-152">**glDepthMask**</span></span>](gldepthmask.md)
</dt> <dt>

[<span data-ttu-id="17085-153">**Remo**</span><span class="sxs-lookup"><span data-stu-id="17085-153">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="17085-154">**glGet**</span><span class="sxs-lookup"><span data-stu-id="17085-154">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="17085-155">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="17085-155">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="17085-156">**glIndexMask**</span><span class="sxs-lookup"><span data-stu-id="17085-156">**glIndexMask**</span></span>](glindexmask.md)
</dt> <dt>

[<span data-ttu-id="17085-157">**glStencilMask**</span><span class="sxs-lookup"><span data-stu-id="17085-157">**glStencilMask**</span></span>](glstencilmask.md)
</dt> </dl>

 

 





