---
title: funzione glNormal3sv (GL. h)
description: Imposta il vettore normale corrente. | funzione glNormal3sv (GL. h)
ms.assetid: 59cdebc9-594a-429f-ba5d-7c63a533cc11
keywords:
- funzione glNormal3sv OpenGL
topic_type:
- apiref
api_name:
- glNormal3sv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf639364ead2e4188e56677bb68930592c4e5d5c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969243"
---
# <a name="glnormal3sv-function"></a><span data-ttu-id="c0db8-105">glNormal3sv (funzione)</span><span class="sxs-lookup"><span data-stu-id="c0db8-105">glNormal3sv function</span></span>

<span data-ttu-id="c0db8-106">Imposta il vettore normale corrente.</span><span class="sxs-lookup"><span data-stu-id="c0db8-106">Sets the current normal vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0db8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c0db8-107">Syntax</span></span>


```C++
void WINAPI glNormal3sv(
   const GLshort *v
);
```



## <a name="parameters"></a><span data-ttu-id="c0db8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c0db8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0db8-109">*v*</span><span class="sxs-lookup"><span data-stu-id="c0db8-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="c0db8-110">Puntatore a una matrice di tre elementi, ovvero le coordinate x, y e z della nuova normale corrente.</span><span class="sxs-lookup"><span data-stu-id="c0db8-110">A pointer to an array of three elements: the x, y, and z coordinates of the new current normal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0db8-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c0db8-111">Return value</span></span>

<span data-ttu-id="c0db8-112">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="c0db8-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0db8-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="c0db8-113">Remarks</span></span>

<span data-ttu-id="c0db8-114">Il normale corrente viene impostato sulle coordinate specificate ogni volta che si chiama la funzione **glNormal3sv** .</span><span class="sxs-lookup"><span data-stu-id="c0db8-114">The current normal is set to the given coordinates whenever you call the **glNormal3sv** function.</span></span>

<span data-ttu-id="c0db8-115">Gli argomenti byte, short o Integer vengono convertiti in formato a virgola mobile con un mapping lineare che esegue il mapping del valore intero rappresentabile più positivo a 1,0 e il valore intero rappresentabile più negativo a-1,0.</span><span class="sxs-lookup"><span data-stu-id="c0db8-115">Byte, short, or integer arguments are converted to floating-point format with a linear mapping that maps the most positive representable integer value to 1.0, and the most negative representable integer value to -1.0.</span></span>

<span data-ttu-id="c0db8-116">I normali specificati tramite **glNormal3sv** non devono avere la lunghezza dell'unità.</span><span class="sxs-lookup"><span data-stu-id="c0db8-116">Normals specified by using **glNormal3sv** need not have unit length.</span></span> <span data-ttu-id="c0db8-117">Se la normalizzazione è abilitata, le normali specificate con **glNormal3sv** vengono normalizzate dopo la trasformazione.</span><span class="sxs-lookup"><span data-stu-id="c0db8-117">If normalization is enabled, then normals specified with **glNormal3sv** are normalized after transformation.</span></span> <span data-ttu-id="c0db8-118">È possibile controllare la normalizzazione usando [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) con l'argomento GL \_ Normalize.</span><span class="sxs-lookup"><span data-stu-id="c0db8-118">You can control normalization by using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_NORMALIZE.</span></span> <span data-ttu-id="c0db8-119">Per impostazione predefinita, la normalizzazione è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="c0db8-119">By default, normalization is disabled.</span></span> <span data-ttu-id="c0db8-120">È possibile aggiornare la normale corrente in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="c0db8-120">You can update the current normal at any time.</span></span> <span data-ttu-id="c0db8-121">In particolare, è possibile chiamare **glNormal3sv** tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="c0db8-121">In particular, you can call **glNormal3sv** between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="c0db8-122">Le funzioni seguenti consentono di recuperare informazioni correlate a **glNormal3sv**:</span><span class="sxs-lookup"><span data-stu-id="c0db8-122">The following functions retrieve information related to **glNormal3sv**:</span></span>

<span data-ttu-id="c0db8-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Current \_ Normal</span><span class="sxs-lookup"><span data-stu-id="c0db8-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_NORMAL</span></span>

<span data-ttu-id="c0db8-124">[**glIsEnable**](glisenabled.md) con argomento GL \_ Normalize</span><span class="sxs-lookup"><span data-stu-id="c0db8-124">[**glIsEnable**](glisenabled.md) with argument GL\_NORMALIZE</span></span>

## <a name="requirements"></a><span data-ttu-id="c0db8-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0db8-125">Requirements</span></span>



| <span data-ttu-id="c0db8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0db8-126">Requirement</span></span> | <span data-ttu-id="c0db8-127">Valore</span><span class="sxs-lookup"><span data-stu-id="c0db8-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0db8-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0db8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c0db8-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c0db8-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c0db8-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0db8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c0db8-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c0db8-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c0db8-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c0db8-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0db8-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0db8-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c0db8-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="c0db8-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="c0db8-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0db8-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c0db8-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c0db8-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0db8-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0db8-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0db8-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c0db8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0db8-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="c0db8-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="c0db8-140">**glColor**</span><span class="sxs-lookup"><span data-stu-id="c0db8-140">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="c0db8-141">**Remo**</span><span class="sxs-lookup"><span data-stu-id="c0db8-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="c0db8-142">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="c0db8-142">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="c0db8-143">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="c0db8-143">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="c0db8-144">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="c0db8-144">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





