---
title: funzione glNormal3i (GL. h)
description: Imposta il vettore normale corrente. | funzione glNormal3i (GL. h)
ms.assetid: ea14e5c6-a725-4d24-9a48-c138ee8b6cd1
keywords:
- funzione glNormal3i OpenGL
topic_type:
- apiref
api_name:
- glNormal3i
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be4c368fcd93ef832bcdb9cf82abe82c5e02413d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353741"
---
# <a name="glnormal3i-function"></a><span data-ttu-id="6696d-105">glNormal3i (funzione)</span><span class="sxs-lookup"><span data-stu-id="6696d-105">glNormal3i function</span></span>

<span data-ttu-id="6696d-106">Imposta il vettore normale corrente.</span><span class="sxs-lookup"><span data-stu-id="6696d-106">Sets the current normal vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="6696d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6696d-107">Syntax</span></span>


```C++
void WINAPI glNormal3i(
   GLint nx,
   GLint ny,
   GLint nz
);
```



## <a name="parameters"></a><span data-ttu-id="6696d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6696d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6696d-109">*NX*</span><span class="sxs-lookup"><span data-stu-id="6696d-109">*nx*</span></span> 
</dt> <dd>

<span data-ttu-id="6696d-110">Specifica la coordinata x del nuovo vettore normale corrente.</span><span class="sxs-lookup"><span data-stu-id="6696d-110">Specifies the x-coordinate for the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="6696d-111">*NY*</span><span class="sxs-lookup"><span data-stu-id="6696d-111">*ny*</span></span> 
</dt> <dd>

<span data-ttu-id="6696d-112">Specifica la coordinata y del nuovo vettore normale corrente.</span><span class="sxs-lookup"><span data-stu-id="6696d-112">Specifies the y-coordinate for the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="6696d-113">*NZ*</span><span class="sxs-lookup"><span data-stu-id="6696d-113">*nz*</span></span> 
</dt> <dd>

<span data-ttu-id="6696d-114">Specifica la coordinata z per il nuovo vettore normale corrente.</span><span class="sxs-lookup"><span data-stu-id="6696d-114">Specifies the z-coordinate for the new current normal vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6696d-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6696d-115">Return value</span></span>

<span data-ttu-id="6696d-116">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="6696d-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6696d-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="6696d-117">Remarks</span></span>

<span data-ttu-id="6696d-118">Il normale corrente viene impostato sulle coordinate specificate ogni volta che si chiama la funzione **glNormal3i**.</span><span class="sxs-lookup"><span data-stu-id="6696d-118">The current normal is set to the given coordinates whenever you call the **glNormal3i** function.</span></span>

<span data-ttu-id="6696d-119">Gli argomenti byte, short o Integer vengono convertiti in formato a virgola mobile con un mapping lineare che esegue il mapping del valore intero rappresentabile più positivo a 1,0 e il valore intero rappresentabile più negativo a-1,0.</span><span class="sxs-lookup"><span data-stu-id="6696d-119">Byte, short, or integer arguments are converted to floating-point format with a linear mapping that maps the most positive representable integer value to 1.0, and the most negative representable integer value to -1.0.</span></span>

<span data-ttu-id="6696d-120">I normali specificati tramite **glNormal3i** non devono avere la lunghezza dell'unità.</span><span class="sxs-lookup"><span data-stu-id="6696d-120">Normals specified by using **glNormal3i** need not have unit length.</span></span> <span data-ttu-id="6696d-121">Se la normalizzazione è abilitata, le normali specificate con **glNormal3i** vengono normalizzate dopo la trasformazione.</span><span class="sxs-lookup"><span data-stu-id="6696d-121">If normalization is enabled, then normals specified with **glNormal3i** are normalized after transformation.</span></span> <span data-ttu-id="6696d-122">È possibile controllare la normalizzazione usando [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) con l'argomento GL \_ Normalize.</span><span class="sxs-lookup"><span data-stu-id="6696d-122">You can control normalization by using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_NORMALIZE.</span></span> <span data-ttu-id="6696d-123">Per impostazione predefinita, la normalizzazione è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="6696d-123">By default, normalization is disabled.</span></span> <span data-ttu-id="6696d-124">È possibile aggiornare la normale corrente in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="6696d-124">You can update the current normal at any time.</span></span> <span data-ttu-id="6696d-125">In particolare, è possibile chiamare **glNormal3i** tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="6696d-125">In particular, you can call **glNormal3i** between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="6696d-126">Le funzioni seguenti consentono di recuperare informazioni correlate a **glNormal3i**:</span><span class="sxs-lookup"><span data-stu-id="6696d-126">The following functions retrieve information related to **glNormal3i**:</span></span>

<span data-ttu-id="6696d-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Current \_ Normal</span><span class="sxs-lookup"><span data-stu-id="6696d-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_NORMAL</span></span>

<span data-ttu-id="6696d-128">[**glIsEnable**](glisenabled.md) con argomento GL \_ Normalize</span><span class="sxs-lookup"><span data-stu-id="6696d-128">[**glIsEnable**](glisenabled.md) with argument GL\_NORMALIZE</span></span>

## <a name="requirements"></a><span data-ttu-id="6696d-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6696d-129">Requirements</span></span>



| <span data-ttu-id="6696d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="6696d-130">Requirement</span></span> | <span data-ttu-id="6696d-131">Valore</span><span class="sxs-lookup"><span data-stu-id="6696d-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6696d-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6696d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6696d-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6696d-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6696d-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6696d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6696d-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6696d-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6696d-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6696d-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="6696d-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6696d-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6696d-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="6696d-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="6696d-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6696d-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6696d-140">DLL</span><span class="sxs-lookup"><span data-stu-id="6696d-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6696d-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6696d-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6696d-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6696d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6696d-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="6696d-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="6696d-144">**glColor**</span><span class="sxs-lookup"><span data-stu-id="6696d-144">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="6696d-145">**Remo**</span><span class="sxs-lookup"><span data-stu-id="6696d-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="6696d-146">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="6696d-146">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="6696d-147">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="6696d-147">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="6696d-148">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="6696d-148">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





