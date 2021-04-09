---
title: funzione gluDeleteTess (Glu. h)
description: La funzione gluDeleteTess Elimina un oggetto a mosaico.
ms.assetid: 7e1540f7-5e7d-4a3b-8c94-5a6800b17411
keywords:
- funzione gluDeleteTess OpenGL
topic_type:
- apiref
api_name:
- gluDeleteTess
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee4625f0a9c2f51e9d7147c9564fcd4fb1fa7117
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740631"
---
# <a name="gludeletetess-function"></a><span data-ttu-id="0772b-104">gluDeleteTess (funzione)</span><span class="sxs-lookup"><span data-stu-id="0772b-104">gluDeleteTess function</span></span>

<span data-ttu-id="0772b-105">La funzione **gluDeleteTess** Elimina un oggetto a mosaico.</span><span class="sxs-lookup"><span data-stu-id="0772b-105">The **gluDeleteTess** function destroys a tessellation object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0772b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0772b-106">Syntax</span></span>


```C++
void WINAPI gluDeleteTess(
   GLUtesselator *tess
);
```



## <a name="parameters"></a><span data-ttu-id="0772b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="0772b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0772b-108">*Tess*</span><span class="sxs-lookup"><span data-stu-id="0772b-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="0772b-109">Oggetto a mosaico da eliminare (creato con [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="0772b-109">The tessellation object to destroy (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0772b-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0772b-110">Return value</span></span>

<span data-ttu-id="0772b-111">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="0772b-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0772b-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="0772b-112">Remarks</span></span>

<span data-ttu-id="0772b-113">La funzione **gluDeleteTess** Elimina l'oggetto mosaico indicato e libera la memoria usata.</span><span class="sxs-lookup"><span data-stu-id="0772b-113">The **gluDeleteTess** function destroys the indicated tessellation object and frees any memory that it used.</span></span>

## <a name="requirements"></a><span data-ttu-id="0772b-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0772b-114">Requirements</span></span>



| <span data-ttu-id="0772b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0772b-115">Requirement</span></span> | <span data-ttu-id="0772b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="0772b-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0772b-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0772b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0772b-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0772b-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="0772b-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0772b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0772b-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0772b-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0772b-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0772b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0772b-122"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="0772b-122"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="0772b-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="0772b-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="0772b-124"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0772b-124"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="0772b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0772b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0772b-126"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0772b-126"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0772b-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0772b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0772b-128">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="0772b-128">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="0772b-129">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="0772b-129">**gluTessBeginPolygon**</span></span>](glubeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="0772b-130">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="0772b-130">*gluTessCallback*</span></span>](glutess.md)
</dt> </dl>

 

 





