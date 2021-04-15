---
title: D2D1_SIZE_F (D2DBaseTypes. h)
description: Archivia una coppia ordinata di float, in genere la larghezza e l'altezza di un rettangolo.
ms.assetid: c2fd41fb-72b3-418b-ad87-65549b04657d
keywords:
- D2D1_SIZE_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a031e1e6a1e9ad7d6975f3dea63427655aa92f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475868"
---
# <a name="d2d1_size_f"></a><span data-ttu-id="30609-104">\_Dimensioni d2d1 \_ F</span><span class="sxs-lookup"><span data-stu-id="30609-104">D2D1\_SIZE\_F</span></span>

<span data-ttu-id="30609-105">Archivia una coppia ordinata di float, in genere la larghezza e l'altezza di un rettangolo.</span><span class="sxs-lookup"><span data-stu-id="30609-105">Stores an ordered pair of floats, typically the width and height of a rectangle.</span></span>


```C++
typedef D2D_SIZE_F D2D1_SIZE_F;
```



## <a name="remarks"></a><span data-ttu-id="30609-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="30609-106">Remarks</span></span>

<span data-ttu-id="30609-107">Analogamente ai punti, le dimensioni rappresentano un altro concetto di grafica importante.</span><span class="sxs-lookup"><span data-stu-id="30609-107">Like points, sizes are another important graphics concept.</span></span> <span data-ttu-id="30609-108">In Direct2D le dimensioni sono rappresentate dalle **strutture \_ d2d1 \_ F** o [**d2d1 \_ size \_ U**](d2d1-size-u.md) .</span><span class="sxs-lookup"><span data-stu-id="30609-108">In Direct2D, sizes are represented by the **D2D1\_SIZE\_F** or [**D2D1\_SIZE\_U**](d2d1-size-u.md) structures.</span></span> <span data-ttu-id="30609-109">Entrambi contengono una coppia ordinata di numeri, in genere la larghezza e l'altezza di un rettangolo.</span><span class="sxs-lookup"><span data-stu-id="30609-109">Both contain an ordered pair of numbers, typically the width and height of a rectangle.</span></span> <span data-ttu-id="30609-110">La struttura **d2d1 della \_ dimensione \_ F** contiene una coppia ordinata di valori **float** e la struttura **\_ \_ U d2d1 size** contiene una coppia ordinata di valori **UInt32** .</span><span class="sxs-lookup"><span data-stu-id="30609-110">The **D2D1\_SIZE\_F** structure contains an ordered pair of **FLOAT** values, and the **D2D1\_SIZE\_U** structure contains an ordered pair of **UINT32** values.</span></span>

<span data-ttu-id="30609-111">**D2d1 \_ SIZE \_ f** è un nuovo nome per un tipo già definito **D2D \_ size \_ f**.</span><span class="sxs-lookup"><span data-stu-id="30609-111">**D2D1\_SIZE\_F** is a new name for an already defined type **D2D\_SIZE\_F**.</span></span> <span data-ttu-id="30609-112">Per un elenco dei campi forniti da **d2d1 \_ size \_ f**, vedere **D2D \_ size \_ f**.</span><span class="sxs-lookup"><span data-stu-id="30609-112">For a list of the fields provided by **D2D1\_SIZE\_F**, see **D2D\_SIZE\_F**.</span></span>

## <a name="requirements"></a><span data-ttu-id="30609-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30609-113">Requirements</span></span>



| <span data-ttu-id="30609-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="30609-114">Requirement</span></span> | <span data-ttu-id="30609-115">Valore</span><span class="sxs-lookup"><span data-stu-id="30609-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30609-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30609-116">Minimum supported client</span></span><br/> | <span data-ttu-id="30609-117">Windows 7, Windows Vista con SP2 e aggiornamento della piattaforma per app desktop di Windows Vista \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="30609-117">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="30609-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30609-118">Minimum supported server</span></span><br/> | <span data-ttu-id="30609-119">Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma per app desktop di Windows Server 2008 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="30609-119">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="30609-120">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30609-120">Minimum supported phone</span></span><br/>  | <span data-ttu-id="30609-121">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="30609-121">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="30609-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="30609-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="30609-123"><dt>D2DBaseTypes. h (include D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="30609-123"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="30609-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30609-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30609-125">**\_Dimensioni D2D \_ F**</span><span class="sxs-lookup"><span data-stu-id="30609-125">**D2D\_SIZE\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_f)
</dt> <dt>

[<span data-ttu-id="30609-126">**D2D1 \_ dimensioni \_ U**</span><span class="sxs-lookup"><span data-stu-id="30609-126">**D2D1\_SIZE\_U**</span></span>](d2d1-size-u.md)
</dt> <dt>

[<span data-ttu-id="30609-127">**D2D1 \_ punto \_ 2F**</span><span class="sxs-lookup"><span data-stu-id="30609-127">**D2D1\_POINT\_2F**</span></span>](d2d1-point-2f.md)
</dt> </dl>

 

