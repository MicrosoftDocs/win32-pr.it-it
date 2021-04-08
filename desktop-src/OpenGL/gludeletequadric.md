---
title: funzione gluDeleteQuadric (Glu. h)
description: La funzione gluDeleteQuadric Elimina un oggetto quadrica.
ms.assetid: 09efd887-0fe8-4a56-bc6f-2177a4930035
keywords:
- funzione gluDeleteQuadric OpenGL
topic_type:
- apiref
api_name:
- gluDeleteQuadric
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b5ee85e943cd958e394efb191932393d228d948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742231"
---
# <a name="gludeletequadric-function"></a><span data-ttu-id="9690d-104">gluDeleteQuadric (funzione)</span><span class="sxs-lookup"><span data-stu-id="9690d-104">gluDeleteQuadric function</span></span>

<span data-ttu-id="9690d-105">La funzione **gluDeleteQuadric** Elimina un oggetto quadrica.</span><span class="sxs-lookup"><span data-stu-id="9690d-105">The **gluDeleteQuadric** function destroys a quadric object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9690d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9690d-106">Syntax</span></span>


```C++
void WINAPI gluDeleteQuadric(
   GLUquadricObj *state
);
```



## <a name="parameters"></a><span data-ttu-id="9690d-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="9690d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9690d-108">*state*</span><span class="sxs-lookup"><span data-stu-id="9690d-108">*state*</span></span> 
</dt> <dd>

<span data-ttu-id="9690d-109">Oggetto quadrica da eliminare definitivamente (creato con [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="9690d-109">The quadric object to be destroyed (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9690d-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9690d-110">Return value</span></span>

<span data-ttu-id="9690d-111">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="9690d-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9690d-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="9690d-112">Remarks</span></span>

<span data-ttu-id="9690d-113">La funzione **gluDeleteQuadric** Elimina l'oggetto quadrica e libera la memoria usata.</span><span class="sxs-lookup"><span data-stu-id="9690d-113">The **gluDeleteQuadric** function destroys the quadric object and frees any memory that it used.</span></span> <span data-ttu-id="9690d-114">Dopo aver chiamato **gluDeleteQuadric**, non è possibile usare di nuovo *lo stato* .</span><span class="sxs-lookup"><span data-stu-id="9690d-114">After you have called **gluDeleteQuadric**, you cannot use *state* again.</span></span>

## <a name="requirements"></a><span data-ttu-id="9690d-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9690d-115">Requirements</span></span>



| <span data-ttu-id="9690d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9690d-116">Requirement</span></span> | <span data-ttu-id="9690d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="9690d-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9690d-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9690d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9690d-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9690d-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9690d-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9690d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9690d-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9690d-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9690d-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9690d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9690d-123"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="9690d-123"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="9690d-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="9690d-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="9690d-125"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9690d-125"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9690d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="9690d-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9690d-127"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9690d-127"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9690d-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9690d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9690d-129">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="9690d-129">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> </dl>

 

 





