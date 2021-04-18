---
title: funzione glNormal3f (GL. h)
description: Imposta il vettore normale corrente. | funzione glNormal3f (GL. h)
ms.assetid: 8407996e-47fd-4c30-91f6-53d4341a1fca
keywords:
- funzione glNormal3f OpenGL
topic_type:
- apiref
api_name:
- glNormal3f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72e83b874b1588ad8bd91da9e5c9f831062de9cc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321640"
---
# <a name="glnormal3f-function"></a><span data-ttu-id="1245b-105">glNormal3f (funzione)</span><span class="sxs-lookup"><span data-stu-id="1245b-105">glNormal3f function</span></span>

<span data-ttu-id="1245b-106">Imposta il vettore normale corrente.</span><span class="sxs-lookup"><span data-stu-id="1245b-106">Sets the current normal vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="1245b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1245b-107">Syntax</span></span>


```C++
void WINAPI glNormal3f(
   GLfloat nx,
   GLfloat ny,
   GLfloat nz
);
```



## <a name="parameters"></a><span data-ttu-id="1245b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1245b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1245b-109">*NX*</span><span class="sxs-lookup"><span data-stu-id="1245b-109">*nx*</span></span> 
</dt> <dd>

<span data-ttu-id="1245b-110">Specifica la coordinata x del nuovo vettore normale corrente.</span><span class="sxs-lookup"><span data-stu-id="1245b-110">Specifies the x-coordinate for the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="1245b-111">*NY*</span><span class="sxs-lookup"><span data-stu-id="1245b-111">*ny*</span></span> 
</dt> <dd>

<span data-ttu-id="1245b-112">Specifica la coordinata y del nuovo vettore normale corrente.</span><span class="sxs-lookup"><span data-stu-id="1245b-112">Specifies the y-coordinate for the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="1245b-113">*NZ*</span><span class="sxs-lookup"><span data-stu-id="1245b-113">*nz*</span></span> 
</dt> <dd>

<span data-ttu-id="1245b-114">Specifica la coordinata z per il nuovo vettore normale corrente.</span><span class="sxs-lookup"><span data-stu-id="1245b-114">Specifies the z-coordinate for the new current normal vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1245b-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1245b-115">Return value</span></span>

<span data-ttu-id="1245b-116">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="1245b-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1245b-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="1245b-117">Remarks</span></span>

<span data-ttu-id="1245b-118">Il normale corrente viene impostato sulle coordinate specificate ogni volta che si chiama la funzione **glNormal3f** .</span><span class="sxs-lookup"><span data-stu-id="1245b-118">The current normal is set to the given coordinates whenever you call the **glNormal3f** function.</span></span>

<span data-ttu-id="1245b-119">Gli argomenti byte, short o Integer vengono convertiti in formato a virgola mobile con un mapping lineare che esegue il mapping del valore intero rappresentabile più positivo a 1,0 e il valore intero rappresentabile più negativo a-1,0.</span><span class="sxs-lookup"><span data-stu-id="1245b-119">Byte, short, or integer arguments are converted to floating-point format with a linear mapping that maps the most positive representable integer value to 1.0, and the most negative representable integer value to -1.0.</span></span>

<span data-ttu-id="1245b-120">I normali specificati tramite **glNormal3f** non devono avere la lunghezza dell'unità.</span><span class="sxs-lookup"><span data-stu-id="1245b-120">Normals specified by using **glNormal3f** need not have unit length.</span></span> <span data-ttu-id="1245b-121">Se la normalizzazione è abilitata, le normali specificate con **glNormal3f** vengono normalizzate dopo la trasformazione.</span><span class="sxs-lookup"><span data-stu-id="1245b-121">If normalization is enabled, then normals specified with **glNormal3f** are normalized after transformation.</span></span> <span data-ttu-id="1245b-122">È possibile controllare la normalizzazione usando [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) con l'argomento GL \_ Normalize.</span><span class="sxs-lookup"><span data-stu-id="1245b-122">You can control normalization by using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_NORMALIZE.</span></span> <span data-ttu-id="1245b-123">Per impostazione predefinita, la normalizzazione è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="1245b-123">By default, normalization is disabled.</span></span> <span data-ttu-id="1245b-124">È possibile aggiornare la normale corrente in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="1245b-124">You can update the current normal at any time.</span></span> <span data-ttu-id="1245b-125">In particolare, è possibile chiamare **glNormal3f** tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="1245b-125">In particular, you can call **glNormal3f** between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="1245b-126">Le funzioni seguenti consentono di recuperare informazioni correlate a **glNormal3f**:</span><span class="sxs-lookup"><span data-stu-id="1245b-126">The following functions retrieve information related to **glNormal3f**:</span></span>

<span data-ttu-id="1245b-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Current \_ Normal</span><span class="sxs-lookup"><span data-stu-id="1245b-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_NORMAL</span></span>

<span data-ttu-id="1245b-128">[**glIsEnable**](glisenabled.md) con argomento GL \_ Normalize</span><span class="sxs-lookup"><span data-stu-id="1245b-128">[**glIsEnable**](glisenabled.md) with argument GL\_NORMALIZE</span></span>

## <a name="requirements"></a><span data-ttu-id="1245b-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1245b-129">Requirements</span></span>



| <span data-ttu-id="1245b-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1245b-130">Requirement</span></span> | <span data-ttu-id="1245b-131">Valore</span><span class="sxs-lookup"><span data-stu-id="1245b-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1245b-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1245b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1245b-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1245b-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1245b-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1245b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1245b-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1245b-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1245b-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1245b-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="1245b-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="1245b-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1245b-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="1245b-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="1245b-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1245b-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1245b-140">DLL</span><span class="sxs-lookup"><span data-stu-id="1245b-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1245b-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1245b-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1245b-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1245b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1245b-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="1245b-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="1245b-144">**glColor**</span><span class="sxs-lookup"><span data-stu-id="1245b-144">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="1245b-145">**Remo**</span><span class="sxs-lookup"><span data-stu-id="1245b-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="1245b-146">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="1245b-146">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="1245b-147">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="1245b-147">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="1245b-148">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="1245b-148">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





