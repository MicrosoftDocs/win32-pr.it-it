---
title: funzione glTexCoord4s (GL. h)
description: Imposta le coordinate di trama correnti. | funzione glTexCoord4s (GL. h)
ms.assetid: 948c63f5-a94d-4e55-9aa4-a320452fc29f
keywords:
- funzione glTexCoord4s OpenGL
topic_type:
- apiref
api_name:
- glTexCoord4s
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19a164b091c62b31523baa5be96d1578e1cbfa80
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103886205"
---
# <a name="gltexcoord4s-function"></a><span data-ttu-id="e6a3f-105">glTexCoord4s (funzione)</span><span class="sxs-lookup"><span data-stu-id="e6a3f-105">glTexCoord4s function</span></span>

<span data-ttu-id="e6a3f-106">Imposta le coordinate di trama correnti.</span><span class="sxs-lookup"><span data-stu-id="e6a3f-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6a3f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e6a3f-107">Syntax</span></span>


```C++
void WINAPI glTexCoord4s(
   GLshort s,
   GLshort t,
   GLshort r,
   GLshort q
);
```



## <a name="parameters"></a><span data-ttu-id="e6a3f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e6a3f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6a3f-109">*s*</span><span class="sxs-lookup"><span data-stu-id="e6a3f-109">*s*</span></span> 
</dt> <dd>

<span data-ttu-id="e6a3f-110">Coordinata di trama s.</span><span class="sxs-lookup"><span data-stu-id="e6a3f-110">The s texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="e6a3f-111">*t*</span><span class="sxs-lookup"><span data-stu-id="e6a3f-111">*t*</span></span> 
</dt> <dd>

<span data-ttu-id="e6a3f-112">Coordinata di trama t.</span><span class="sxs-lookup"><span data-stu-id="e6a3f-112">The t texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="e6a3f-113">*r*</span><span class="sxs-lookup"><span data-stu-id="e6a3f-113">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="e6a3f-114">Coordinata di trama r.</span><span class="sxs-lookup"><span data-stu-id="e6a3f-114">The r texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="e6a3f-115">*d*</span><span class="sxs-lookup"><span data-stu-id="e6a3f-115">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="e6a3f-116">Coordinata di trama q.</span><span class="sxs-lookup"><span data-stu-id="e6a3f-116">The q texture coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6a3f-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e6a3f-117">Return value</span></span>

<span data-ttu-id="e6a3f-118">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="e6a3f-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6a3f-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="e6a3f-119">Remarks</span></span>

<span data-ttu-id="e6a3f-120">La funzione [**glTexCoord**](gltexcoord-functions.md) imposta le coordinate di trama correnti che fanno parte dei dati associati ai vertici del poligono.</span><span class="sxs-lookup"><span data-stu-id="e6a3f-120">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="e6a3f-121">La funzione **glTexCoord** specifica le coordinate di trama in una, due, tre o quattro dimensioni.</span><span class="sxs-lookup"><span data-stu-id="e6a3f-121">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="e6a3f-122">La funzione glTexCoord1 imposta le coordinate di trama correnti su (s, 0, 0, 1); una chiamata a glTexCoord2 le imposta su (s, t, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="e6a3f-122">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="e6a3f-123">Analogamente, glTexCoord3 specifica le coordinate di trama come (s, t, r, 1) e glTexCoord4 definisce tutti e quattro i componenti in modo esplicito come (s, t, r, q).</span><span class="sxs-lookup"><span data-stu-id="e6a3f-123">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="e6a3f-124">È possibile aggiornare le coordinate di trama correnti in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="e6a3f-124">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="e6a3f-125">In particolare, è possibile chiamare glTexCoord tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="e6a3f-125">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="e6a3f-126">La funzione seguente recupera le informazioni correlate a **glTexCoord**:</span><span class="sxs-lookup"><span data-stu-id="e6a3f-126">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="e6a3f-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ \_ coordinate di trama correnti \_</span><span class="sxs-lookup"><span data-stu-id="e6a3f-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="e6a3f-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6a3f-128">Requirements</span></span>



| <span data-ttu-id="e6a3f-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6a3f-129">Requirement</span></span> | <span data-ttu-id="e6a3f-130">Valore</span><span class="sxs-lookup"><span data-stu-id="e6a3f-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6a3f-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6a3f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e6a3f-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e6a3f-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e6a3f-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6a3f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e6a3f-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e6a3f-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e6a3f-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6a3f-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6a3f-136"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6a3f-136"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e6a3f-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="e6a3f-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="e6a3f-138"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6a3f-138"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e6a3f-139">DLL</span><span class="sxs-lookup"><span data-stu-id="e6a3f-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6a3f-140"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6a3f-140"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6a3f-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6a3f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6a3f-142">glVertex</span><span class="sxs-lookup"><span data-stu-id="e6a3f-142">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





