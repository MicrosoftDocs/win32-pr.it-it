---
title: funzione glNormal3b (GL. h)
description: Imposta il vettore normale corrente. | funzione glNormal3b (GL. h)
ms.assetid: b6976143-bc9a-4766-9f7e-5380c3a24173
keywords:
- funzione glNormal3b OpenGL
topic_type:
- apiref
api_name:
- glNormal3b
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a09a92b718881670ed5625fd5aa94a23193cdd6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103886082"
---
# <a name="glnormal3b-function"></a><span data-ttu-id="f71b5-105">glNormal3b (funzione)</span><span class="sxs-lookup"><span data-stu-id="f71b5-105">glNormal3b function</span></span>

<span data-ttu-id="f71b5-106">Imposta il vettore normale corrente.</span><span class="sxs-lookup"><span data-stu-id="f71b5-106">Sets the current normal vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="f71b5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f71b5-107">Syntax</span></span>


```C++
void WINAPI glNormal3b(
   GLbyte nx,
   GLbyte ny,
   GLbyte nz
);
```



## <a name="parameters"></a><span data-ttu-id="f71b5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f71b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f71b5-109">*NX*</span><span class="sxs-lookup"><span data-stu-id="f71b5-109">*nx*</span></span> 
</dt> <dd>

<span data-ttu-id="f71b5-110">Specifica la coordinata x del nuovo vettore normale corrente.</span><span class="sxs-lookup"><span data-stu-id="f71b5-110">Specifies the x-coordinate for the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="f71b5-111">*NY*</span><span class="sxs-lookup"><span data-stu-id="f71b5-111">*ny*</span></span> 
</dt> <dd>

<span data-ttu-id="f71b5-112">Specifica la coordinata y del nuovo vettore normale corrente.</span><span class="sxs-lookup"><span data-stu-id="f71b5-112">Specifies the y-coordinate for the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="f71b5-113">*NZ*</span><span class="sxs-lookup"><span data-stu-id="f71b5-113">*nz*</span></span> 
</dt> <dd>

<span data-ttu-id="f71b5-114">Specifica la coordinata z per il nuovo vettore normale corrente.</span><span class="sxs-lookup"><span data-stu-id="f71b5-114">Specifies the z-coordinate for the new current normal vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f71b5-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f71b5-115">Return value</span></span>

<span data-ttu-id="f71b5-116">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="f71b5-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f71b5-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="f71b5-117">Remarks</span></span>

<span data-ttu-id="f71b5-118">Il normale corrente viene impostato sulle coordinate specificate ogni volta che si chiama la funzione **glNormal3b** .</span><span class="sxs-lookup"><span data-stu-id="f71b5-118">The current normal is set to the given coordinates whenever you call the **glNormal3b** function.</span></span>

<span data-ttu-id="f71b5-119">Gli argomenti byte, short o Integer vengono convertiti in formato a virgola mobile utilizzando un mapping lineare che esegue il mapping del valore intero rappresentabile più positivo a 1,0 e il valore intero rappresentabile più negativo a-1,0.</span><span class="sxs-lookup"><span data-stu-id="f71b5-119">Byte, short, or integer arguments are converted to floating-point format by using a linear mapping that maps the most positive representable integer value to 1.0, and the most negative representable integer value to -1.0.</span></span>

<span data-ttu-id="f71b5-120">I normali specificati con **glNormal3b** non devono avere una lunghezza di unità.</span><span class="sxs-lookup"><span data-stu-id="f71b5-120">Normals specified with **glNormal3b** need not have unit length.</span></span> <span data-ttu-id="f71b5-121">Se la normalizzazione è abilitata, le normali specificate con **glNormal3b** vengono normalizzate dopo la trasformazione.</span><span class="sxs-lookup"><span data-stu-id="f71b5-121">If normalization is enabled, then normals specified with **glNormal3b** are normalized after transformation.</span></span> <span data-ttu-id="f71b5-122">È possibile controllare la normalizzazione usando [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) con l'argomento GL \_ Normalize.</span><span class="sxs-lookup"><span data-stu-id="f71b5-122">You can control normalization by using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_NORMALIZE.</span></span> <span data-ttu-id="f71b5-123">Per impostazione predefinita, la normalizzazione è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="f71b5-123">By default, normalization is disabled.</span></span> <span data-ttu-id="f71b5-124">È possibile aggiornare la normale corrente in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="f71b5-124">You can update the current normal at any time.</span></span> <span data-ttu-id="f71b5-125">In particolare, è possibile chiamare **glNormal3b** tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="f71b5-125">In particular, you can call **glNormal3b** between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="f71b5-126">Le funzioni seguenti consentono di recuperare informazioni correlate a **glNormal3b**:</span><span class="sxs-lookup"><span data-stu-id="f71b5-126">The following functions retrieve information related to **glNormal3b**:</span></span>

<span data-ttu-id="f71b5-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Current \_ Normal</span><span class="sxs-lookup"><span data-stu-id="f71b5-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_NORMAL</span></span>

<span data-ttu-id="f71b5-128">[**glIsEnable**](glisenabled.md) con argomento GL \_ Normalize</span><span class="sxs-lookup"><span data-stu-id="f71b5-128">[**glIsEnable**](glisenabled.md) with argument GL\_NORMALIZE</span></span>

## <a name="requirements"></a><span data-ttu-id="f71b5-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f71b5-129">Requirements</span></span>



| <span data-ttu-id="f71b5-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f71b5-130">Requirement</span></span> | <span data-ttu-id="f71b5-131">Valore</span><span class="sxs-lookup"><span data-stu-id="f71b5-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f71b5-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f71b5-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f71b5-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f71b5-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f71b5-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f71b5-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f71b5-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f71b5-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f71b5-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f71b5-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="f71b5-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f71b5-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f71b5-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="f71b5-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="f71b5-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f71b5-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f71b5-140">DLL</span><span class="sxs-lookup"><span data-stu-id="f71b5-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f71b5-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f71b5-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f71b5-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f71b5-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f71b5-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f71b5-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f71b5-144">**glColor**</span><span class="sxs-lookup"><span data-stu-id="f71b5-144">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="f71b5-145">**Remo**</span><span class="sxs-lookup"><span data-stu-id="f71b5-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f71b5-146">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="f71b5-146">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="f71b5-147">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="f71b5-147">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="f71b5-148">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="f71b5-148">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





