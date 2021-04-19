---
title: D2D1_POINT_2F (D2DBaseTypes. h)
description: Rappresenta una coordinata x e una coppia di coordinate y nello spazio bidimensionale. | D2D1_POINT_2F (D2DBaseTypes. h)
ms.assetid: b317ae75-d738-4e1a-bcd1-adf3e95b197e
keywords:
- D2D1_POINT_2F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f93bf4a0d1a1b3f988f1c6d168388e9910080dcb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321548"
---
# <a name="d2d1_point_2f"></a><span data-ttu-id="510d4-105">D2D1 \_ punto \_ 2F</span><span class="sxs-lookup"><span data-stu-id="510d4-105">D2D1\_POINT\_2F</span></span>

<span data-ttu-id="510d4-106">Rappresenta una coordinata x e una coppia di coordinate y nello spazio bidimensionale.</span><span class="sxs-lookup"><span data-stu-id="510d4-106">Represents an x-coordinate and y-coordinate pair in two-dimensional space.</span></span>


```C++
typedef D2D_POINT_2F D2D1_POINT_2F;
```



## <a name="remarks"></a><span data-ttu-id="510d4-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="510d4-107">Remarks</span></span>

<span data-ttu-id="510d4-108">I punti in Direct2D sono rappresentati dalle strutture **d2d1 \_ Point \_ 2F** o [**d2d1 \_ Point \_ 2U**](d2d1-point-2u.md) .</span><span class="sxs-lookup"><span data-stu-id="510d4-108">Points in Direct2D are represented by the **D2D1\_POINT\_2F** or [**D2D1\_POINT\_2U**](d2d1-point-2u.md) structures.</span></span> <span data-ttu-id="510d4-109">Entrambi contengono una coordinata x e una coppia di coordinate y nello spazio bidimensionale.</span><span class="sxs-lookup"><span data-stu-id="510d4-109">Both contain an x-coordinate and y-coordinate pair in two-dimensional space.</span></span> <span data-ttu-id="510d4-110">La **struttura d2d1 \_ Point \_ 2F** archivia le coordinate come valori **float** e la struttura **d2d1 \_ Point \_ 2U** le archivia come valori **UInt32** .</span><span class="sxs-lookup"><span data-stu-id="510d4-110">The **D2D1\_POINT\_2F** structure stores the coordinates as **FLOAT** values, and the **D2D1\_POINT\_2U** structure stores them as **UINT32** values.</span></span>

<span data-ttu-id="510d4-111">**D2d1 \_ Il punto \_ 2F** è un nuovo nome per il tipo già definito [**D2D \_ Point \_ 2F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2f).</span><span class="sxs-lookup"><span data-stu-id="510d4-111">**D2D1\_POINT\_2F** is a new name for the already defined type [**D2D\_POINT\_2F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2f).</span></span>

## <a name="requirements"></a><span data-ttu-id="510d4-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="510d4-112">Requirements</span></span>



| <span data-ttu-id="510d4-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="510d4-113">Requirement</span></span> | <span data-ttu-id="510d4-114">Valore</span><span class="sxs-lookup"><span data-stu-id="510d4-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="510d4-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="510d4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="510d4-116">Windows 7, Windows Vista con SP2 e aggiornamento della piattaforma per app desktop di Windows Vista \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="510d4-116">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="510d4-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="510d4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="510d4-118">Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma per app desktop di Windows Server 2008 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="510d4-118">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="510d4-119">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="510d4-119">Minimum supported phone</span></span><br/>  | <span data-ttu-id="510d4-120">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="510d4-120">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="510d4-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="510d4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="510d4-122"><dt>D2DBaseTypes. h (include D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="510d4-122"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="510d4-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="510d4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="510d4-124">**Punto di D2D1 \_ \_ 2U**</span><span class="sxs-lookup"><span data-stu-id="510d4-124">**D2D1\_POINT\_2U**</span></span>](/windows/desktop/Direct2D/d2d1-point-2u)
</dt> <dt>

[<span data-ttu-id="510d4-125">**D2D \_ punto \_ 2F**</span><span class="sxs-lookup"><span data-stu-id="510d4-125">**D2D\_POINT\_2F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2f)
</dt> </dl>

 

