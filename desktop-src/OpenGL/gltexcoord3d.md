---
title: funzione glTexCoord3d (GL. h)
description: Imposta le coordinate di trama correnti. | funzione glTexCoord3d (GL. h)
ms.assetid: 41b8aa69-c069-493f-a1e3-51cf6a01209e
keywords:
- funzione glTexCoord3d OpenGL
topic_type:
- apiref
api_name:
- glTexCoord3d
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abb7603ed0f823e3b8d841328378d9e207638716
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530744"
---
# <a name="gltexcoord3d-function"></a><span data-ttu-id="3c79a-105">glTexCoord3d (funzione)</span><span class="sxs-lookup"><span data-stu-id="3c79a-105">glTexCoord3d function</span></span>

<span data-ttu-id="3c79a-106">Imposta le coordinate di trama correnti.</span><span class="sxs-lookup"><span data-stu-id="3c79a-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c79a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c79a-107">Syntax</span></span>


```C++
void WINAPI glTexCoord3d(
   GLdouble s,
   GLdouble t,
   GLdouble r
);
```



## <a name="parameters"></a><span data-ttu-id="3c79a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c79a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c79a-109">*s*</span><span class="sxs-lookup"><span data-stu-id="3c79a-109">*s*</span></span> 
</dt> <dd>

<span data-ttu-id="3c79a-110">Coordinata di trama s.</span><span class="sxs-lookup"><span data-stu-id="3c79a-110">The s texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="3c79a-111">*t*</span><span class="sxs-lookup"><span data-stu-id="3c79a-111">*t*</span></span> 
</dt> <dd>

<span data-ttu-id="3c79a-112">Coordinata di trama t.</span><span class="sxs-lookup"><span data-stu-id="3c79a-112">The t texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="3c79a-113">*r*</span><span class="sxs-lookup"><span data-stu-id="3c79a-113">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="3c79a-114">Coordinata di trama r.</span><span class="sxs-lookup"><span data-stu-id="3c79a-114">The r texture coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c79a-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3c79a-115">Return value</span></span>

<span data-ttu-id="3c79a-116">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="3c79a-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c79a-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="3c79a-117">Remarks</span></span>

<span data-ttu-id="3c79a-118">La funzione [**glTexCoord**](gltexcoord-functions.md) imposta le coordinate di trama correnti che fanno parte dei dati associati ai vertici del poligono.</span><span class="sxs-lookup"><span data-stu-id="3c79a-118">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="3c79a-119">La funzione **glTexCoord** specifica le coordinate di trama in una, due, tre o quattro dimensioni.</span><span class="sxs-lookup"><span data-stu-id="3c79a-119">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="3c79a-120">La funzione glTexCoord1 imposta le coordinate di trama correnti su (s, 0, 0, 1); una chiamata a glTexCoord2 le imposta su (s, t, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="3c79a-120">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="3c79a-121">Analogamente, glTexCoord3 specifica le coordinate di trama come (s, t, r, 1) e glTexCoord4 definisce tutti e quattro i componenti in modo esplicito come (s, t, r, q).</span><span class="sxs-lookup"><span data-stu-id="3c79a-121">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="3c79a-122">È possibile aggiornare le coordinate di trama correnti in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="3c79a-122">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="3c79a-123">In particolare, è possibile chiamare glTexCoord tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="3c79a-123">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="3c79a-124">La funzione seguente recupera le informazioni correlate a **glTexCoord**:</span><span class="sxs-lookup"><span data-stu-id="3c79a-124">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="3c79a-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ \_ coordinate di trama correnti \_</span><span class="sxs-lookup"><span data-stu-id="3c79a-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="3c79a-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c79a-126">Requirements</span></span>



| <span data-ttu-id="3c79a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c79a-127">Requirement</span></span> | <span data-ttu-id="3c79a-128">Valore</span><span class="sxs-lookup"><span data-stu-id="3c79a-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c79a-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c79a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3c79a-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3c79a-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3c79a-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c79a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3c79a-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3c79a-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3c79a-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3c79a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c79a-134"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c79a-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3c79a-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="3c79a-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="3c79a-136"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c79a-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3c79a-137">DLL</span><span class="sxs-lookup"><span data-stu-id="3c79a-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c79a-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c79a-138"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c79a-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c79a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c79a-140">glVertex</span><span class="sxs-lookup"><span data-stu-id="3c79a-140">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





