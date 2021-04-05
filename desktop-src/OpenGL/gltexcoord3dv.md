---
title: funzione glTexCoord3dv (GL. h)
description: Imposta le coordinate di trama correnti. | funzione glTexCoord3dv (GL. h)
ms.assetid: 410f49d6-7950-4940-a377-d62ca2bd5db7
keywords:
- funzione glTexCoord3dv OpenGL
topic_type:
- apiref
api_name:
- glTexCoord3dv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4007e6a524075fc7c091cfc3c6e01044aeae3c22
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103886149"
---
# <a name="gltexcoord3dv-function"></a><span data-ttu-id="22ee1-105">glTexCoord3dv (funzione)</span><span class="sxs-lookup"><span data-stu-id="22ee1-105">glTexCoord3dv function</span></span>

<span data-ttu-id="22ee1-106">Imposta le coordinate di trama correnti.</span><span class="sxs-lookup"><span data-stu-id="22ee1-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="22ee1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="22ee1-107">Syntax</span></span>


```C++
void WINAPI glTexCoord3dv(
   const GLdouble *v
);
```



## <a name="parameters"></a><span data-ttu-id="22ee1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="22ee1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22ee1-109">*v*</span><span class="sxs-lookup"><span data-stu-id="22ee1-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="22ee1-110">Puntatore a una matrice di tre elementi, che a sua volta specifica le coordinate della trama s, t e r.</span><span class="sxs-lookup"><span data-stu-id="22ee1-110">A pointer to an array of three elements, which in turn specifies the s, t, and r texture coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22ee1-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="22ee1-111">Return value</span></span>

<span data-ttu-id="22ee1-112">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="22ee1-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="22ee1-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="22ee1-113">Remarks</span></span>

<span data-ttu-id="22ee1-114">La funzione [**glTexCoord**](gltexcoord-functions.md) imposta le coordinate di trama correnti che fanno parte dei dati associati ai vertici del poligono.</span><span class="sxs-lookup"><span data-stu-id="22ee1-114">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="22ee1-115">La funzione **glTexCoord** specifica le coordinate di trama in una, due, tre o quattro dimensioni.</span><span class="sxs-lookup"><span data-stu-id="22ee1-115">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="22ee1-116">La funzione glTexCoord1 imposta le coordinate di trama correnti su (s, 0, 0, 1); una chiamata a glTexCoord2 le imposta su (s, t, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="22ee1-116">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="22ee1-117">Analogamente, glTexCoord3 specifica le coordinate di trama come (s, t, r, 1) e glTexCoord4 definisce tutti e quattro i componenti in modo esplicito come (s, t, r, q).</span><span class="sxs-lookup"><span data-stu-id="22ee1-117">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="22ee1-118">È possibile aggiornare le coordinate di trama correnti in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="22ee1-118">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="22ee1-119">In particolare, è possibile chiamare glTexCoord tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="22ee1-119">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="22ee1-120">La funzione seguente recupera le informazioni correlate a **glTexCoord**:</span><span class="sxs-lookup"><span data-stu-id="22ee1-120">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="22ee1-121">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ \_ coordinate di trama correnti \_</span><span class="sxs-lookup"><span data-stu-id="22ee1-121">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="22ee1-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="22ee1-122">Requirements</span></span>



| <span data-ttu-id="22ee1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="22ee1-123">Requirement</span></span> | <span data-ttu-id="22ee1-124">Valore</span><span class="sxs-lookup"><span data-stu-id="22ee1-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22ee1-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22ee1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="22ee1-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="22ee1-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="22ee1-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22ee1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="22ee1-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="22ee1-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="22ee1-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="22ee1-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="22ee1-130"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="22ee1-130"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="22ee1-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="22ee1-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="22ee1-132"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22ee1-132"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="22ee1-133">DLL</span><span class="sxs-lookup"><span data-stu-id="22ee1-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22ee1-134"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22ee1-134"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22ee1-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="22ee1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22ee1-136">glVertex</span><span class="sxs-lookup"><span data-stu-id="22ee1-136">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





