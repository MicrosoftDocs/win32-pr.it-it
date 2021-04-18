---
title: funzione gluNewTess (Glu. h)
description: La funzione gluNewTess crea un oggetto a mosaico.
ms.assetid: dfc9fce8-ecab-493b-85ee-6d7487814186
keywords:
- funzione gluNewTess OpenGL
topic_type:
- apiref
api_name:
- gluNewTess
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0573ead0cf9b81568c4bf2101e317bef7faf148
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301458"
---
# <a name="glunewtess-function"></a><span data-ttu-id="b699f-104">gluNewTess (funzione)</span><span class="sxs-lookup"><span data-stu-id="b699f-104">gluNewTess function</span></span>

<span data-ttu-id="b699f-105">La funzione **gluNewTess** crea un oggetto a mosaico.</span><span class="sxs-lookup"><span data-stu-id="b699f-105">The **gluNewTess** function creates a tessellation object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b699f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b699f-106">Syntax</span></span>


```C++
GLUtesselator* WINAPI gluNewTess(void);
```



## <a name="parameters"></a><span data-ttu-id="b699f-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="b699f-107">Parameters</span></span>

<span data-ttu-id="b699f-108">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="b699f-108">This function has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="b699f-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="b699f-109">Remarks</span></span>

<span data-ttu-id="b699f-110">La funzione **gluNewTess** crea e restituisce un puntatore a un nuovo oggetto a mosaico.</span><span class="sxs-lookup"><span data-stu-id="b699f-110">The **gluNewTess** function creates and returns a pointer to a new tessellation object.</span></span> <span data-ttu-id="b699f-111">Fare riferimento a questo oggetto quando si chiamano le funzioni a mosaico.</span><span class="sxs-lookup"><span data-stu-id="b699f-111">Refer to this object when calling tessellation functions.</span></span> <span data-ttu-id="b699f-112">Un valore restituito pari a zero indica che la memoria disponibile non è sufficiente per allocare all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b699f-112">A return value of zero means there is not enough memory to allocate to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="b699f-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b699f-113">Requirements</span></span>



| <span data-ttu-id="b699f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b699f-114">Requirement</span></span> | <span data-ttu-id="b699f-115">Valore</span><span class="sxs-lookup"><span data-stu-id="b699f-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b699f-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b699f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b699f-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b699f-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b699f-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b699f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b699f-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b699f-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b699f-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b699f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b699f-121"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="b699f-121"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="b699f-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="b699f-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="b699f-123"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b699f-123"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b699f-124">DLL</span><span class="sxs-lookup"><span data-stu-id="b699f-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b699f-125"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b699f-125"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b699f-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b699f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b699f-127">**gluDeleteTess**</span><span class="sxs-lookup"><span data-stu-id="b699f-127">**gluDeleteTess**</span></span>](gludeletetess.md)
</dt> <dt>

[<span data-ttu-id="b699f-128">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="b699f-128">**gluTessBeginPolygon**</span></span>](glubeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="b699f-129">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="b699f-129">*gluTessCallback*</span></span>](glutess.md)
</dt> </dl>

 

 





