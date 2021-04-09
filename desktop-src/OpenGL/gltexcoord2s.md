---
title: funzione glTexCoord2s (GL. h)
description: Imposta le coordinate di trama correnti. | funzione glTexCoord2s (GL. h)
ms.assetid: d1bd7286-e32e-43ef-919a-4debf62a50ef
keywords:
- funzione glTexCoord2s OpenGL
topic_type:
- apiref
api_name:
- glTexCoord2s
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 256ecceb66e6a70f60f8de8bca914dc380ee9f00
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103886210"
---
# <a name="gltexcoord2s-function"></a><span data-ttu-id="11c31-105">glTexCoord2s (funzione)</span><span class="sxs-lookup"><span data-stu-id="11c31-105">glTexCoord2s function</span></span>

<span data-ttu-id="11c31-106">Imposta le coordinate di trama correnti.</span><span class="sxs-lookup"><span data-stu-id="11c31-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="11c31-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="11c31-107">Syntax</span></span>


```C++
void WINAPI glTexCoord2s(
   GLshort s,
   GLshort t
);
```



## <a name="parameters"></a><span data-ttu-id="11c31-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="11c31-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11c31-109">*s*</span><span class="sxs-lookup"><span data-stu-id="11c31-109">*s*</span></span> 
</dt> <dd>

<span data-ttu-id="11c31-110">Coordinata di trama s.</span><span class="sxs-lookup"><span data-stu-id="11c31-110">The s texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="11c31-111">*t*</span><span class="sxs-lookup"><span data-stu-id="11c31-111">*t*</span></span> 
</dt> <dd>

<span data-ttu-id="11c31-112">Coordinata di trama t.</span><span class="sxs-lookup"><span data-stu-id="11c31-112">The t texture coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11c31-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="11c31-113">Return value</span></span>

<span data-ttu-id="11c31-114">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="11c31-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="11c31-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="11c31-115">Remarks</span></span>

<span data-ttu-id="11c31-116">La funzione [**glTexCoord**](gltexcoord-functions.md) imposta le coordinate di trama correnti che fanno parte dei dati associati ai vertici del poligono.</span><span class="sxs-lookup"><span data-stu-id="11c31-116">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="11c31-117">La funzione **glTexCoord** specifica le coordinate di trama in una, due, tre o quattro dimensioni.</span><span class="sxs-lookup"><span data-stu-id="11c31-117">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="11c31-118">La funzione glTexCoord1 imposta le coordinate di trama correnti su (s, 0, 0, 1); una chiamata a glTexCoord2 le imposta su (s, t, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="11c31-118">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="11c31-119">Analogamente, glTexCoord3 specifica le coordinate di trama come (s, t, r, 1) e glTexCoord4 definisce tutti e quattro i componenti in modo esplicito come (s, t, r, q).</span><span class="sxs-lookup"><span data-stu-id="11c31-119">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="11c31-120">È possibile aggiornare le coordinate di trama correnti in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="11c31-120">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="11c31-121">In particolare, è possibile chiamare glTexCoord tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="11c31-121">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="11c31-122">La funzione seguente recupera le informazioni correlate a **glTexCoord**:</span><span class="sxs-lookup"><span data-stu-id="11c31-122">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="11c31-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ \_ coordinate di trama correnti \_</span><span class="sxs-lookup"><span data-stu-id="11c31-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="11c31-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="11c31-124">Requirements</span></span>



| <span data-ttu-id="11c31-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="11c31-125">Requirement</span></span> | <span data-ttu-id="11c31-126">Valore</span><span class="sxs-lookup"><span data-stu-id="11c31-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="11c31-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11c31-127">Minimum supported client</span></span><br/> | <span data-ttu-id="11c31-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="11c31-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="11c31-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11c31-129">Minimum supported server</span></span><br/> | <span data-ttu-id="11c31-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="11c31-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="11c31-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="11c31-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="11c31-132"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="11c31-132"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="11c31-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="11c31-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="11c31-134"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11c31-134"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="11c31-135">DLL</span><span class="sxs-lookup"><span data-stu-id="11c31-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11c31-136"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11c31-136"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11c31-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="11c31-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11c31-138">glVertex</span><span class="sxs-lookup"><span data-stu-id="11c31-138">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





