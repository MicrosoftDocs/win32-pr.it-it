---
description: Descrive lo stato raster.
ms.assetid: f7b5b714-8fc8-47b8-adec-1089b8d07081
title: Struttura D3DRASTER_STATUS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRASTER_STATUS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e77ab0e6ee164eadae862ed03df5652c21ba7040
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322916"
---
# <a name="d3draster_status-structure"></a><span data-ttu-id="51c57-103">\_Struttura di stato D3DRASTER</span><span class="sxs-lookup"><span data-stu-id="51c57-103">D3DRASTER\_STATUS structure</span></span>

<span data-ttu-id="51c57-104">Descrive lo stato raster.</span><span class="sxs-lookup"><span data-stu-id="51c57-104">Describes the raster status.</span></span>

## <a name="syntax"></a><span data-ttu-id="51c57-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="51c57-105">Syntax</span></span>


```C++
typedef struct D3DRASTER_STATUS {
  BOOL InVBlank;
  UINT ScanLine;
} D3DRASTER_STATUS, *LPD3DRASTER_STATUS;
```



## <a name="members"></a><span data-ttu-id="51c57-106">Members</span><span class="sxs-lookup"><span data-stu-id="51c57-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="51c57-107">**InVBlank**</span><span class="sxs-lookup"><span data-stu-id="51c57-107">**InVBlank**</span></span>
</dt> <dd>

<span data-ttu-id="51c57-108">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="51c57-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="51c57-109">**True** se il raster è nel periodo vuoto verticale.</span><span class="sxs-lookup"><span data-stu-id="51c57-109">**TRUE** if the raster is in the vertical blank period.</span></span> <span data-ttu-id="51c57-110">**False** se il raster non è nel periodo di blanking verticale.</span><span class="sxs-lookup"><span data-stu-id="51c57-110">**FALSE** if the raster is not in the vertical blank period.</span></span>

</dd> <dt>

<span data-ttu-id="51c57-111">**ScanLine**</span><span class="sxs-lookup"><span data-stu-id="51c57-111">**ScanLine**</span></span>
</dt> <dd>

<span data-ttu-id="51c57-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="51c57-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="51c57-113">Se InVBlank è **false**, questo valore è un Integer approssimativamente corrispondente alla riga di analisi corrente disegnata dal raster.</span><span class="sxs-lookup"><span data-stu-id="51c57-113">If InVBlank is **FALSE**, then this value is an integer roughly corresponding to the current scan line painted by the raster.</span></span> <span data-ttu-id="51c57-114">Le righe di analisi sono numerate nello stesso modo delle coordinate di superficie Direct3D: 0 è la parte superiore della superficie primaria, estendendo al valore (altezza della superficie-1) nella parte inferiore dello schermo.</span><span class="sxs-lookup"><span data-stu-id="51c57-114">Scan lines are numbered in the same way as Direct3D surface coordinates: 0 is the top of the primary surface, extending to the value (height of the surface - 1) at the bottom of the display.</span></span>

<span data-ttu-id="51c57-115">Se InVBlank è **true**, questo valore è impostato su zero e può essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="51c57-115">If InVBlank is **TRUE**, then this value is set to zero and can be ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="51c57-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="51c57-116">Requirements</span></span>



| <span data-ttu-id="51c57-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="51c57-117">Requirement</span></span> | <span data-ttu-id="51c57-118">Valore</span><span class="sxs-lookup"><span data-stu-id="51c57-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="51c57-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="51c57-119">Header</span></span><br/> | <dl> <span data-ttu-id="51c57-120"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="51c57-120"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51c57-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="51c57-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51c57-122">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="51c57-122">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="51c57-123">**GetRasterStatus**</span><span class="sxs-lookup"><span data-stu-id="51c57-123">**GetRasterStatus**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrasterstatus)
</dt> </dl>

 

 
