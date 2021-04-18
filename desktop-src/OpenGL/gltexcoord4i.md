---
title: funzione glTexCoord4i (GL. h)
description: Imposta le coordinate di trama correnti. | funzione glTexCoord4i (GL. h)
ms.assetid: b2b49102-5129-49cc-9043-22ba46fbf08f
keywords:
- funzione glTexCoord4i OpenGL
topic_type:
- apiref
api_name:
- glTexCoord4i
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86ecdcddc7a62a2cce4adf595321c72dd877aa69
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321710"
---
# <a name="gltexcoord4i-function"></a><span data-ttu-id="c2a84-105">glTexCoord4i (funzione)</span><span class="sxs-lookup"><span data-stu-id="c2a84-105">glTexCoord4i function</span></span>

<span data-ttu-id="c2a84-106">Imposta le coordinate di trama correnti.</span><span class="sxs-lookup"><span data-stu-id="c2a84-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2a84-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c2a84-107">Syntax</span></span>


```C++
void WINAPI glTexCoord4i(
   GLint s,
   GLint t,
   GLint r,
   GLint q
);
```



## <a name="parameters"></a><span data-ttu-id="c2a84-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c2a84-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2a84-109">*s*</span><span class="sxs-lookup"><span data-stu-id="c2a84-109">*s*</span></span> 
</dt> <dd>

<span data-ttu-id="c2a84-110">Coordinata di trama s.</span><span class="sxs-lookup"><span data-stu-id="c2a84-110">The s texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="c2a84-111">*t*</span><span class="sxs-lookup"><span data-stu-id="c2a84-111">*t*</span></span> 
</dt> <dd>

<span data-ttu-id="c2a84-112">Coordinata di trama t.</span><span class="sxs-lookup"><span data-stu-id="c2a84-112">The t texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="c2a84-113">*r*</span><span class="sxs-lookup"><span data-stu-id="c2a84-113">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="c2a84-114">Coordinata di trama r.</span><span class="sxs-lookup"><span data-stu-id="c2a84-114">The r texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="c2a84-115">*d*</span><span class="sxs-lookup"><span data-stu-id="c2a84-115">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="c2a84-116">Coordinata di trama q.</span><span class="sxs-lookup"><span data-stu-id="c2a84-116">The q texture coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2a84-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c2a84-117">Return value</span></span>

<span data-ttu-id="c2a84-118">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="c2a84-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2a84-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="c2a84-119">Remarks</span></span>

<span data-ttu-id="c2a84-120">La funzione [**glTexCoord**](gltexcoord-functions.md) imposta le coordinate di trama correnti che fanno parte dei dati associati ai vertici del poligono.</span><span class="sxs-lookup"><span data-stu-id="c2a84-120">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="c2a84-121">La funzione **glTexCoord** specifica le coordinate di trama in una, due, tre o quattro dimensioni.</span><span class="sxs-lookup"><span data-stu-id="c2a84-121">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="c2a84-122">La funzione glTexCoord1 imposta le coordinate di trama correnti su (s, 0, 0, 1); una chiamata a glTexCoord2 le imposta su (s, t, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="c2a84-122">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="c2a84-123">Analogamente, glTexCoord3 specifica le coordinate di trama come (s, t, r, 1) e glTexCoord4 definisce tutti e quattro i componenti in modo esplicito come (s, t, r, q).</span><span class="sxs-lookup"><span data-stu-id="c2a84-123">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="c2a84-124">È possibile aggiornare le coordinate di trama correnti in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="c2a84-124">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="c2a84-125">In particolare, è possibile chiamare glTexCoord tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="c2a84-125">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="c2a84-126">La funzione seguente recupera le informazioni correlate a **glTexCoord**:</span><span class="sxs-lookup"><span data-stu-id="c2a84-126">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="c2a84-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ \_ coordinate di trama correnti \_</span><span class="sxs-lookup"><span data-stu-id="c2a84-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="c2a84-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2a84-128">Requirements</span></span>



| <span data-ttu-id="c2a84-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2a84-129">Requirement</span></span> | <span data-ttu-id="c2a84-130">Valore</span><span class="sxs-lookup"><span data-stu-id="c2a84-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2a84-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2a84-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c2a84-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c2a84-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c2a84-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2a84-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c2a84-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c2a84-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c2a84-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c2a84-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2a84-136"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2a84-136"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c2a84-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="c2a84-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="c2a84-138"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2a84-138"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c2a84-139">DLL</span><span class="sxs-lookup"><span data-stu-id="c2a84-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2a84-140"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2a84-140"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2a84-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c2a84-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2a84-142">glVertex</span><span class="sxs-lookup"><span data-stu-id="c2a84-142">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





