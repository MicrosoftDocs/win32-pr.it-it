---
title: funzione gluGetTessProperty (Glu. h)
description: La funzione gluGetTessProperty ottiene una proprietà dell'oggetto mosaico.
ms.assetid: 6aa565d8-2257-4259-a959-b7d806a7ed96
keywords:
- funzione gluGetTessProperty OpenGL
topic_type:
- apiref
api_name:
- gluGetTessProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 482f32b227dbcf0c2a62405e344aa719bb4b9e17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400524"
---
# <a name="glugettessproperty-function"></a><span data-ttu-id="9fcaa-104">gluGetTessProperty (funzione)</span><span class="sxs-lookup"><span data-stu-id="9fcaa-104">gluGetTessProperty function</span></span>

<span data-ttu-id="9fcaa-105">La funzione **gluGetTessProperty** ottiene una proprietà dell'oggetto mosaico.</span><span class="sxs-lookup"><span data-stu-id="9fcaa-105">The **gluGetTessProperty** function gets a tessellation object property.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fcaa-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9fcaa-106">Syntax</span></span>


```C++
void WINAPI gluGetTessProperty(
   GLUtesselator *tess,
   GLenum        which,
   GLdouble      *value
);
```



## <a name="parameters"></a><span data-ttu-id="9fcaa-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="9fcaa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fcaa-108">*Tess*</span><span class="sxs-lookup"><span data-stu-id="9fcaa-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="9fcaa-109">Oggetto a mosaico creato con [**gluNewTess**](glunewtess.md).</span><span class="sxs-lookup"><span data-stu-id="9fcaa-109">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="9fcaa-110">*che*</span><span class="sxs-lookup"><span data-stu-id="9fcaa-110">*which*</span></span> 
</dt> <dd>

<span data-ttu-id="9fcaa-111">Proprietà di cui è necessario recuperare il valore.</span><span class="sxs-lookup"><span data-stu-id="9fcaa-111">The property whose value is to be retrieved.</span></span> <span data-ttu-id="9fcaa-112">Sono validi i valori seguenti: \_ regola di Winding di Glu Tess \_ \_ , Glu \_ Tess \_ \_ solo limite e Glu \_ Tess \_ tolerance.</span><span class="sxs-lookup"><span data-stu-id="9fcaa-112">The following values are valid: GLU\_TESS\_WINDING\_RULE, GLU\_TESS\_BOUNDARY\_ONLY, and GLU\_TESS\_TOLERANCE.</span></span>

</dd> <dt>

<span data-ttu-id="9fcaa-113">*value*</span><span class="sxs-lookup"><span data-stu-id="9fcaa-113">*value*</span></span> 
</dt> <dd>

<span data-ttu-id="9fcaa-114">Puntatore alla posizione in cui viene scritto il valore della proprietà denominata.</span><span class="sxs-lookup"><span data-stu-id="9fcaa-114">A pointer to the location where the value of the named property is written.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fcaa-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9fcaa-115">Return value</span></span>

<span data-ttu-id="9fcaa-116">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="9fcaa-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fcaa-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="9fcaa-117">Remarks</span></span>

<span data-ttu-id="9fcaa-118">Utilizzare **gluGetTessProperty** per recuperare le proprietà archiviate in un oggetto a mosaico.</span><span class="sxs-lookup"><span data-stu-id="9fcaa-118">Use **gluGetTessProperty** to retrieve properties stored in a tessellation object.</span></span> <span data-ttu-id="9fcaa-119">Queste proprietà influiscono sulla modalità di interpretazione e rendering degli oggetti a mosaico.</span><span class="sxs-lookup"><span data-stu-id="9fcaa-119">These properties affect the way tessellation objects are interpreted and rendered.</span></span> <span data-ttu-id="9fcaa-120">Per informazioni sulle proprietà e sulle operazioni eseguite, vedere [**gluTessProperty**](glutessproperty.md).</span><span class="sxs-lookup"><span data-stu-id="9fcaa-120">For information about what the properties are and what they do, see [**gluTessProperty**](glutessproperty.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9fcaa-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9fcaa-121">Requirements</span></span>



| <span data-ttu-id="9fcaa-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fcaa-122">Requirement</span></span> | <span data-ttu-id="9fcaa-123">Valore</span><span class="sxs-lookup"><span data-stu-id="9fcaa-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9fcaa-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fcaa-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9fcaa-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9fcaa-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9fcaa-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fcaa-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9fcaa-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9fcaa-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9fcaa-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9fcaa-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fcaa-129"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fcaa-129"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="9fcaa-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="9fcaa-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="9fcaa-131"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9fcaa-131"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9fcaa-132">DLL</span><span class="sxs-lookup"><span data-stu-id="9fcaa-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fcaa-133"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fcaa-133"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fcaa-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9fcaa-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fcaa-135">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="9fcaa-135">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="9fcaa-136">**gluTessProperty**</span><span class="sxs-lookup"><span data-stu-id="9fcaa-136">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> </dl>

 

 





