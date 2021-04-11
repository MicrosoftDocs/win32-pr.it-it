---
title: funzione glTexCoord4sv (GL. h)
description: Imposta le coordinate di trama correnti. | funzione glTexCoord4sv (GL. h)
ms.assetid: 8192d896-c099-410b-9df6-21f9b66d910b
keywords:
- funzione glTexCoord4dv OpenGL
topic_type:
- apiref
api_name:
- glTexCoord4dv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d3ef51cb7a02c5220cce8c6014eb4ecdd0a9fea
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234862"
---
# <a name="gltexcoord4sv-function"></a><span data-ttu-id="9721c-105">glTexCoord4sv (funzione)</span><span class="sxs-lookup"><span data-stu-id="9721c-105">glTexCoord4sv function</span></span>

<span data-ttu-id="9721c-106">Imposta le coordinate di trama correnti.</span><span class="sxs-lookup"><span data-stu-id="9721c-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="9721c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9721c-107">Syntax</span></span>


```C++
void WINAPI glTexCoord4dv(
   const GLshort *v
);
```



## <a name="parameters"></a><span data-ttu-id="9721c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9721c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9721c-109">*v*</span><span class="sxs-lookup"><span data-stu-id="9721c-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="9721c-110">Puntatore a una matrice di quattro elementi, che a sua volta specifica le coordinate di trama s, t, r e q.</span><span class="sxs-lookup"><span data-stu-id="9721c-110">A pointer to an array of four elements, which in turn specifies the s, t, r, and q texture coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9721c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9721c-111">Return value</span></span>

<span data-ttu-id="9721c-112">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="9721c-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9721c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="9721c-113">Remarks</span></span>

<span data-ttu-id="9721c-114">La funzione [**glTexCoord**](gltexcoord-functions.md) imposta le coordinate di trama correnti che fanno parte dei dati associati ai vertici del poligono.</span><span class="sxs-lookup"><span data-stu-id="9721c-114">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="9721c-115">La funzione **glTexCoord** specifica le coordinate di trama in una, due, tre o quattro dimensioni.</span><span class="sxs-lookup"><span data-stu-id="9721c-115">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="9721c-116">La funzione glTexCoord1 imposta le coordinate di trama correnti su (s, 0, 0, 1); una chiamata a glTexCoord2 le imposta su (s, t, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="9721c-116">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="9721c-117">Analogamente, glTexCoord3 specifica le coordinate di trama come (s, t, r, 1) e glTexCoord4 definisce tutti e quattro i componenti in modo esplicito come (s, t, r, q).</span><span class="sxs-lookup"><span data-stu-id="9721c-117">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="9721c-118">È possibile aggiornare le coordinate di trama correnti in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="9721c-118">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="9721c-119">In particolare, è possibile chiamare glTexCoord tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="9721c-119">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="9721c-120">La funzione seguente recupera le informazioni correlate a **glTexCoord**:</span><span class="sxs-lookup"><span data-stu-id="9721c-120">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="9721c-121">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ \_ coordinate di trama correnti \_</span><span class="sxs-lookup"><span data-stu-id="9721c-121">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="9721c-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9721c-122">Requirements</span></span>



| <span data-ttu-id="9721c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9721c-123">Requirement</span></span> | <span data-ttu-id="9721c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="9721c-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9721c-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9721c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9721c-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9721c-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9721c-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9721c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9721c-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9721c-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9721c-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9721c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9721c-130"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9721c-130"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9721c-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="9721c-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="9721c-132"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9721c-132"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9721c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9721c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9721c-134"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9721c-134"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9721c-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9721c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9721c-136">glVertex</span><span class="sxs-lookup"><span data-stu-id="9721c-136">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





