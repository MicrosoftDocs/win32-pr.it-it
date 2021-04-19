---
title: funzione glTexCoord4iv (GL. h)
description: Imposta le coordinate di trama correnti. | funzione glTexCoord4iv (GL. h)
ms.assetid: 4ce3070c-70c1-4a2b-a6e7-084a4baa3dc5
keywords:
- funzione glTexCoord4iv OpenGL
topic_type:
- apiref
api_name:
- glTexCoord4iv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c2ec50556e871a66db79bb3d7d956e103f586a9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321790"
---
# <a name="gltexcoord4iv-function"></a><span data-ttu-id="39c60-105">glTexCoord4iv (funzione)</span><span class="sxs-lookup"><span data-stu-id="39c60-105">glTexCoord4iv function</span></span>

<span data-ttu-id="39c60-106">Imposta le coordinate di trama correnti.</span><span class="sxs-lookup"><span data-stu-id="39c60-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="39c60-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="39c60-107">Syntax</span></span>


```C++
void WINAPI glTexCoord4iv(
   const GLint *v
);
```



## <a name="parameters"></a><span data-ttu-id="39c60-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="39c60-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39c60-109">*v*</span><span class="sxs-lookup"><span data-stu-id="39c60-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="39c60-110">Puntatore a una matrice di quattro elementi, che a sua volta specifica le coordinate di trama s, t, r e q.</span><span class="sxs-lookup"><span data-stu-id="39c60-110">A pointer to an array of four elements, which in turn specifies the s, t, r, and q texture coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39c60-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="39c60-111">Return value</span></span>

<span data-ttu-id="39c60-112">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="39c60-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="39c60-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="39c60-113">Remarks</span></span>

<span data-ttu-id="39c60-114">La funzione [**glTexCoord**](gltexcoord-functions.md) imposta le coordinate di trama correnti che fanno parte dei dati associati ai vertici del poligono.</span><span class="sxs-lookup"><span data-stu-id="39c60-114">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="39c60-115">La funzione **glTexCoord** specifica le coordinate di trama in una, due, tre o quattro dimensioni.</span><span class="sxs-lookup"><span data-stu-id="39c60-115">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="39c60-116">La funzione glTexCoord1 imposta le coordinate di trama correnti su (s, 0, 0, 1); una chiamata a glTexCoord2 le imposta su (s, t, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="39c60-116">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="39c60-117">Analogamente, glTexCoord3 specifica le coordinate di trama come (s, t, r, 1) e glTexCoord4 definisce tutti e quattro i componenti in modo esplicito come (s, t, r, q).</span><span class="sxs-lookup"><span data-stu-id="39c60-117">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="39c60-118">È possibile aggiornare le coordinate di trama correnti in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="39c60-118">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="39c60-119">In particolare, è possibile chiamare glTexCoord tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="39c60-119">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="39c60-120">La funzione seguente recupera le informazioni correlate a **glTexCoord**:</span><span class="sxs-lookup"><span data-stu-id="39c60-120">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="39c60-121">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ \_ coordinate di trama correnti \_</span><span class="sxs-lookup"><span data-stu-id="39c60-121">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="39c60-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39c60-122">Requirements</span></span>



| <span data-ttu-id="39c60-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="39c60-123">Requirement</span></span> | <span data-ttu-id="39c60-124">Valore</span><span class="sxs-lookup"><span data-stu-id="39c60-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39c60-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39c60-125">Minimum supported client</span></span><br/> | <span data-ttu-id="39c60-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="39c60-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="39c60-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39c60-127">Minimum supported server</span></span><br/> | <span data-ttu-id="39c60-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="39c60-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="39c60-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="39c60-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="39c60-130"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="39c60-130"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="39c60-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="39c60-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="39c60-132"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="39c60-132"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="39c60-133">DLL</span><span class="sxs-lookup"><span data-stu-id="39c60-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39c60-134"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39c60-134"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39c60-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39c60-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39c60-136">glVertex</span><span class="sxs-lookup"><span data-stu-id="39c60-136">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





