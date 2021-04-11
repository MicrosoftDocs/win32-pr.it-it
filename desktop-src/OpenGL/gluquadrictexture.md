---
title: funzione gluQuadricTexture (Glu. h)
description: La funzione gluQuadricTexture specifica se quadriche deve essere tramato.
ms.assetid: 11681497-f099-4856-a0ac-6a44abd3e1a1
keywords:
- funzione gluQuadricTexture OpenGL
topic_type:
- apiref
api_name:
- gluQuadricTexture
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cc395564b6c6f30f38a8c5129c489d0bfca6b80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120603"
---
# <a name="gluquadrictexture-function"></a><span data-ttu-id="82800-104">gluQuadricTexture (funzione)</span><span class="sxs-lookup"><span data-stu-id="82800-104">gluQuadricTexture function</span></span>

<span data-ttu-id="82800-105">La funzione **gluQuadricTexture** specifica se quadriche deve essere tramato.</span><span class="sxs-lookup"><span data-stu-id="82800-105">The **gluQuadricTexture** function specifies whether quadrics are to be textured.</span></span>

## <a name="syntax"></a><span data-ttu-id="82800-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="82800-106">Syntax</span></span>


```C++
void WINAPI gluQuadricTexture(
   GLUquadric *quadObject,
   GLboolean  textureCoords
);
```



## <a name="parameters"></a><span data-ttu-id="82800-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="82800-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82800-108">*quadObject*</span><span class="sxs-lookup"><span data-stu-id="82800-108">*quadObject*</span></span> 
</dt> <dd>

<span data-ttu-id="82800-109">Oggetto quadrica (creato con [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="82800-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="82800-110">*textureCoords*</span><span class="sxs-lookup"><span data-stu-id="82800-110">*textureCoords*</span></span> 
</dt> <dd>

<span data-ttu-id="82800-111">Flag che indica se devono essere generate le coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="82800-111">A flag indicating whether texture coordinates are to be generated.</span></span> <span data-ttu-id="82800-112">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="82800-112">The following values are valid.</span></span>



| <span data-ttu-id="82800-113">Valore</span><span class="sxs-lookup"><span data-stu-id="82800-113">Value</span></span>                                                                                                                                          | <span data-ttu-id="82800-114">Significato</span><span class="sxs-lookup"><span data-stu-id="82800-114">Meaning</span></span>                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="GL_TRUE"></span><span id="gl_true"></span><dl> <span data-ttu-id="82800-115"><dt>**GL \_ true**</dt></span><span class="sxs-lookup"><span data-stu-id="82800-115"><dt>**GL\_TRUE**</dt></span></span> </dl>    | <span data-ttu-id="82800-116">Genera coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="82800-116">Generate texture coordinates.</span></span><br/>                                   |
| <span id="GL_FALSE"></span><span id="gl_false"></span><dl> <span data-ttu-id="82800-117"><dt>**GL \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="82800-117"><dt>**GL\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="82800-118">Non generare coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="82800-118">Do not generate texture coordinates.</span></span> <span data-ttu-id="82800-119">Si tratta del valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="82800-119">This is the default value.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82800-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="82800-120">Return value</span></span>

<span data-ttu-id="82800-121">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="82800-121">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="82800-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="82800-122">Remarks</span></span>

<span data-ttu-id="82800-123">La funzione **gluQuadricTexture** specifica se devono essere generate le coordinate di trama per quadriche sottoposte a rendering con **quadObject**.</span><span class="sxs-lookup"><span data-stu-id="82800-123">The **gluQuadricTexture** function specifies whether texture coordinates are to be generated for quadrics rendered with **quadObject**.</span></span>

<span data-ttu-id="82800-124">Il modo in cui vengono generate le coordinate di trama dipende dal rendering del quadrica specifico.</span><span class="sxs-lookup"><span data-stu-id="82800-124">The manner in which texture coordinates are generated depends upon the specific quadric rendered.</span></span>

## <a name="requirements"></a><span data-ttu-id="82800-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82800-125">Requirements</span></span>



| <span data-ttu-id="82800-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="82800-126">Requirement</span></span> | <span data-ttu-id="82800-127">Valore</span><span class="sxs-lookup"><span data-stu-id="82800-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="82800-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82800-128">Minimum supported client</span></span><br/> | <span data-ttu-id="82800-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="82800-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="82800-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82800-130">Minimum supported server</span></span><br/> | <span data-ttu-id="82800-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="82800-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="82800-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="82800-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="82800-133"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="82800-133"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="82800-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="82800-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="82800-135"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82800-135"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="82800-136">DLL</span><span class="sxs-lookup"><span data-stu-id="82800-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82800-137"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82800-137"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82800-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="82800-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82800-139">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="82800-139">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="82800-140">**gluQuadricDrawStyle**</span><span class="sxs-lookup"><span data-stu-id="82800-140">**gluQuadricDrawStyle**</span></span>](gluquadricdrawstyle.md)
</dt> <dt>

[<span data-ttu-id="82800-141">**gluQuadricNormals**</span><span class="sxs-lookup"><span data-stu-id="82800-141">**gluQuadricNormals**</span></span>](gluquadricnormals.md)
</dt> </dl>

 

 





