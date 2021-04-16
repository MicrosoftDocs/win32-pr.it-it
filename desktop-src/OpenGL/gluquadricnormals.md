---
title: funzione gluQuadricNormals (Glu. h)
description: La funzione gluQuadricNormals specifica il tipo di normali da usare per quadriche.
ms.assetid: 945759ec-ed4a-480f-8243-49fc785867c1
keywords:
- funzione gluQuadricNormals OpenGL
topic_type:
- apiref
api_name:
- gluQuadricNormals
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f11f9d8cd1884d7a5d1bc4cd03797517ba484126
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478017"
---
# <a name="gluquadricnormals-function"></a><span data-ttu-id="22ec5-104">gluQuadricNormals (funzione)</span><span class="sxs-lookup"><span data-stu-id="22ec5-104">gluQuadricNormals function</span></span>

<span data-ttu-id="22ec5-105">La funzione **gluQuadricNormals** specifica il tipo di normali da usare per quadriche.</span><span class="sxs-lookup"><span data-stu-id="22ec5-105">The **gluQuadricNormals** function specifies what kind of normals are to be used for quadrics.</span></span>

## <a name="syntax"></a><span data-ttu-id="22ec5-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="22ec5-106">Syntax</span></span>


```C++
void WINAPI gluQuadricNormals(
   GLUquadric *quadObject,
   GLenum     normals
);
```



## <a name="parameters"></a><span data-ttu-id="22ec5-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="22ec5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22ec5-108">*quadObject*</span><span class="sxs-lookup"><span data-stu-id="22ec5-108">*quadObject*</span></span> 
</dt> <dd>

<span data-ttu-id="22ec5-109">Oggetto quadrica (creato con [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="22ec5-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="22ec5-110">*normali*</span><span class="sxs-lookup"><span data-stu-id="22ec5-110">*normals*</span></span> 
</dt> <dd>

<span data-ttu-id="22ec5-111">Tipo desiderato di normali.</span><span class="sxs-lookup"><span data-stu-id="22ec5-111">The desired type of normals.</span></span> <span data-ttu-id="22ec5-112">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="22ec5-112">The following values are valid.</span></span>



| <span data-ttu-id="22ec5-113">Valore</span><span class="sxs-lookup"><span data-stu-id="22ec5-113">Value</span></span>                                                                                                                                                | <span data-ttu-id="22ec5-114">Significato</span><span class="sxs-lookup"><span data-stu-id="22ec5-114">Meaning</span></span>                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="GLU_NONE"></span><span id="glu_none"></span><dl> <span data-ttu-id="22ec5-115"><dt>**GLU \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="22ec5-115"><dt>**GLU\_NONE**</dt></span></span> </dl>       | <span data-ttu-id="22ec5-116">Non viene generato alcun normale.</span><span class="sxs-lookup"><span data-stu-id="22ec5-116">No normals are generated.</span></span><br/>                                                         |
| <span id="GLU_FLAT"></span><span id="glu_flat"></span><dl> <span data-ttu-id="22ec5-117"><dt>**GLU \_ Flat**</dt></span><span class="sxs-lookup"><span data-stu-id="22ec5-117"><dt>**GLU\_FLAT**</dt></span></span> </dl>       | <span data-ttu-id="22ec5-118">Viene generato un normale per ogni facet di un quadrica.</span><span class="sxs-lookup"><span data-stu-id="22ec5-118">One normal is generated for every facet of a quadric.</span></span><br/>                             |
| <span id="GLU_SMOOTH"></span><span id="glu_smooth"></span><dl> <span data-ttu-id="22ec5-119"><dt>**GLU \_ smussato**</dt></span><span class="sxs-lookup"><span data-stu-id="22ec5-119"><dt>**GLU\_SMOOTH**</dt></span></span> </dl> | <span data-ttu-id="22ec5-120">Viene generato un normale per ogni vertice di un quadrica.</span><span class="sxs-lookup"><span data-stu-id="22ec5-120">One normal is generated for every vertex of a quadric.</span></span> <span data-ttu-id="22ec5-121">Si tratta del valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="22ec5-121">This is the default value.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22ec5-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="22ec5-122">Return value</span></span>

<span data-ttu-id="22ec5-123">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="22ec5-123">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="22ec5-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="22ec5-124">Remarks</span></span>

<span data-ttu-id="22ec5-125">La funzione **gluQuadricNormals** specifica il tipo di normali da usare per il rendering quadriche con **quadObject**.</span><span class="sxs-lookup"><span data-stu-id="22ec5-125">The **gluQuadricNormals** function specifies what kind of normals are to be used for quadrics rendered with **quadObject**.</span></span>

## <a name="requirements"></a><span data-ttu-id="22ec5-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="22ec5-126">Requirements</span></span>



| <span data-ttu-id="22ec5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="22ec5-127">Requirement</span></span> | <span data-ttu-id="22ec5-128">Valore</span><span class="sxs-lookup"><span data-stu-id="22ec5-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="22ec5-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22ec5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="22ec5-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="22ec5-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="22ec5-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22ec5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="22ec5-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="22ec5-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="22ec5-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="22ec5-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="22ec5-134"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="22ec5-134"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="22ec5-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="22ec5-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="22ec5-136"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22ec5-136"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="22ec5-137">DLL</span><span class="sxs-lookup"><span data-stu-id="22ec5-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22ec5-138"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22ec5-138"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22ec5-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="22ec5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22ec5-140">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="22ec5-140">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="22ec5-141">**gluQuadricDrawStyle**</span><span class="sxs-lookup"><span data-stu-id="22ec5-141">**gluQuadricDrawStyle**</span></span>](gluquadricdrawstyle.md)
</dt> <dt>

[<span data-ttu-id="22ec5-142">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="22ec5-142">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="22ec5-143">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="22ec5-143">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> </dl>

 

 





