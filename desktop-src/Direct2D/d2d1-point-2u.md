---
title: D2D1_POINT_2U (D2DBaseTypes. h)
description: Rappresenta una coordinata x e una coppia di coordinate y nello spazio bidimensionale. | D2D1_POINT_2U (D2DBaseTypes. h)
ms.assetid: 652c0dd7-c24d-4941-ae23-2be21b53af69
keywords:
- D2D1_POINT_2U
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050cf6372a1b84ed72647c8c5a5d76e352f4960f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234744"
---
# <a name="d2d1_point_2u"></a><span data-ttu-id="dfce2-105">Punto di D2D1 \_ \_ 2U</span><span class="sxs-lookup"><span data-stu-id="dfce2-105">D2D1\_POINT\_2U</span></span>

<span data-ttu-id="dfce2-106">Rappresenta una coordinata x e una coppia di coordinate y nello spazio bidimensionale.</span><span class="sxs-lookup"><span data-stu-id="dfce2-106">Represents an x-coordinate and y-coordinate pair in two-dimensional space.</span></span>


```C++
typedef D2D_POINT_2U D2D1_POINT_2U;
```



## <a name="remarks"></a><span data-ttu-id="dfce2-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="dfce2-107">Remarks</span></span>

<span data-ttu-id="dfce2-108">I punti in Direct2D sono rappresentati dalle strutture [**d2d1 \_ Point \_ 2F**](d2d1-point-2f.md) o **d2d1 \_ Point \_ 2U** .</span><span class="sxs-lookup"><span data-stu-id="dfce2-108">Points in Direct2D are represented by the [**D2D1\_POINT\_2F**](d2d1-point-2f.md) or **D2D1\_POINT\_2U** structures.</span></span> <span data-ttu-id="dfce2-109">Entrambi contengono una coordinata x e una coppia di coordinate y nello spazio bidimensionale.</span><span class="sxs-lookup"><span data-stu-id="dfce2-109">Both contain an x-coordinate and y-coordinate pair in two-dimensional space.</span></span> <span data-ttu-id="dfce2-110">La **struttura d2d1 \_ Point \_ 2F** archivia le coordinate come valori **float** e la struttura **d2d1 \_ Point \_ 2U** le archivia come valori **UInt32** .</span><span class="sxs-lookup"><span data-stu-id="dfce2-110">The **D2D1\_POINT\_2F** structure stores the coordinates as **FLOAT** values, and the **D2D1\_POINT\_2U** structure stores them as **UINT32** values.</span></span>

<span data-ttu-id="dfce2-111">**D2d1 \_ Il punto \_ 2U** è un nuovo nome per il tipo già definito [**D2D \_ punto \_ 2U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2u).</span><span class="sxs-lookup"><span data-stu-id="dfce2-111">**D2D1\_POINT\_2U** is a new name for the already defined type [**D2D\_POINT\_2U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2u).</span></span>

## <a name="requirements"></a><span data-ttu-id="dfce2-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dfce2-112">Requirements</span></span>



| <span data-ttu-id="dfce2-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfce2-113">Requirement</span></span> | <span data-ttu-id="dfce2-114">Valore</span><span class="sxs-lookup"><span data-stu-id="dfce2-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfce2-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dfce2-115">Minimum supported client</span></span><br/> | <span data-ttu-id="dfce2-116">Windows 7, Windows Vista con SP2 e aggiornamento della piattaforma per app desktop di Windows Vista \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="dfce2-116">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="dfce2-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dfce2-117">Minimum supported server</span></span><br/> | <span data-ttu-id="dfce2-118">Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma per app desktop di Windows Server 2008 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="dfce2-118">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="dfce2-119">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dfce2-119">Minimum supported phone</span></span><br/>  | <span data-ttu-id="dfce2-120">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="dfce2-120">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="dfce2-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dfce2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfce2-122"><dt>D2DBaseTypes. h (include D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dfce2-122"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="dfce2-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dfce2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfce2-124">**Punto di D2D \_ \_ 2U**</span><span class="sxs-lookup"><span data-stu-id="dfce2-124">**D2D\_POINT\_2U**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2u)
</dt> <dt>

[<span data-ttu-id="dfce2-125">**D2D \_ punto \_ 2F**</span><span class="sxs-lookup"><span data-stu-id="dfce2-125">**D2D\_POINT\_2F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2f)
</dt> </dl>

 

 





