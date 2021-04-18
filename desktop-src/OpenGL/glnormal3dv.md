---
title: funzione glNormal3dv (GL. h)
description: Imposta il vettore normale corrente. | funzione glNormal3dv (GL. h)
ms.assetid: 9d4f8d3c-f4c4-4165-a5f9-edc89319008b
keywords:
- funzione glNormal3dv OpenGL
topic_type:
- apiref
api_name:
- glNormal3dv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84f2c2cefd5b0373808347e8a9ef17eb2ca2f863
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321641"
---
# <a name="glnormal3dv-function"></a><span data-ttu-id="cca8b-105">glNormal3dv (funzione)</span><span class="sxs-lookup"><span data-stu-id="cca8b-105">glNormal3dv function</span></span>

<span data-ttu-id="cca8b-106">Imposta il vettore normale corrente.</span><span class="sxs-lookup"><span data-stu-id="cca8b-106">Sets the current normal vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="cca8b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cca8b-107">Syntax</span></span>


```C++
void WINAPI glNormal3dv(
   const GLdouble *v
);
```



## <a name="parameters"></a><span data-ttu-id="cca8b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="cca8b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cca8b-109">*v*</span><span class="sxs-lookup"><span data-stu-id="cca8b-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="cca8b-110">Puntatore a una matrice di tre elementi, ovvero le coordinate x, y e z della nuova normale corrente.</span><span class="sxs-lookup"><span data-stu-id="cca8b-110">A pointer to an array of three elements: the x, y, and z coordinates of the new current normal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cca8b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cca8b-111">Return value</span></span>

<span data-ttu-id="cca8b-112">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="cca8b-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cca8b-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="cca8b-113">Remarks</span></span>

<span data-ttu-id="cca8b-114">Il normale corrente viene impostato sulle coordinate specificate ogni volta che si chiama la funzione **glNormal3dv**.</span><span class="sxs-lookup"><span data-stu-id="cca8b-114">The current normal is set to the given coordinates whenever you call the **glNormal3dv** function.</span></span>

<span data-ttu-id="cca8b-115">Gli argomenti byte, short o Integer vengono convertiti in formato a virgola mobile con un mapping lineare che esegue il mapping del valore intero rappresentabile più positivo a 1,0 e il valore intero rappresentabile più negativo a-1,0.</span><span class="sxs-lookup"><span data-stu-id="cca8b-115">Byte, short, or integer arguments are converted to floating-point format with a linear mapping that maps the most positive representable integer value to 1.0, and the most negative representable integer value to -1.0.</span></span>

<span data-ttu-id="cca8b-116">I normali specificati tramite **glNormal3dv** non devono avere la lunghezza dell'unità.</span><span class="sxs-lookup"><span data-stu-id="cca8b-116">Normals specified by using **glNormal3dv** need not have unit length.</span></span> <span data-ttu-id="cca8b-117">Se la normalizzazione è abilitata, le normali specificate con **glNormal3dv** vengono normalizzate dopo la trasformazione.</span><span class="sxs-lookup"><span data-stu-id="cca8b-117">If normalization is enabled, then normals specified with **glNormal3dv** are normalized after transformation.</span></span> <span data-ttu-id="cca8b-118">È possibile controllare la normalizzazione usando [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) con l'argomento GL \_ Normalize.</span><span class="sxs-lookup"><span data-stu-id="cca8b-118">You can control normalization by using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_NORMALIZE.</span></span> <span data-ttu-id="cca8b-119">Per impostazione predefinita, la normalizzazione è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="cca8b-119">By default, normalization is disabled.</span></span> <span data-ttu-id="cca8b-120">È possibile aggiornare la normale corrente in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="cca8b-120">You can update the current normal at any time.</span></span> <span data-ttu-id="cca8b-121">In particolare, è possibile chiamare **glNormal3dv** tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="cca8b-121">In particular, you can call **glNormal3dv** between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="cca8b-122">Le funzioni seguenti consentono di recuperare informazioni correlate a **glNormal3dv**:</span><span class="sxs-lookup"><span data-stu-id="cca8b-122">The following functions retrieve information related to **glNormal3dv**:</span></span>

<span data-ttu-id="cca8b-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Current \_ Normal</span><span class="sxs-lookup"><span data-stu-id="cca8b-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_NORMAL</span></span>

<span data-ttu-id="cca8b-124">[**glIsEnable**](glisenabled.md) con argomento GL \_ Normalize</span><span class="sxs-lookup"><span data-stu-id="cca8b-124">[**glIsEnable**](glisenabled.md) with argument GL\_NORMALIZE</span></span>

## <a name="requirements"></a><span data-ttu-id="cca8b-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cca8b-125">Requirements</span></span>



| <span data-ttu-id="cca8b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="cca8b-126">Requirement</span></span> | <span data-ttu-id="cca8b-127">Valore</span><span class="sxs-lookup"><span data-stu-id="cca8b-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cca8b-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cca8b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cca8b-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cca8b-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="cca8b-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cca8b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cca8b-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cca8b-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cca8b-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cca8b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="cca8b-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="cca8b-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="cca8b-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="cca8b-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="cca8b-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cca8b-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="cca8b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="cca8b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cca8b-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cca8b-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cca8b-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cca8b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cca8b-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="cca8b-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="cca8b-140">**glColor**</span><span class="sxs-lookup"><span data-stu-id="cca8b-140">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="cca8b-141">**Remo**</span><span class="sxs-lookup"><span data-stu-id="cca8b-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="cca8b-142">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="cca8b-142">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="cca8b-143">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="cca8b-143">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="cca8b-144">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="cca8b-144">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





