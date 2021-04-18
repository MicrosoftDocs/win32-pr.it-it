---
description: Contiene dati di rampa rosso, verde e blu.
ms.assetid: c596f47a-6c09-4b97-ab2f-b1da3d851aa4
title: Struttura D3DGAMMARAMP (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DGAMMARAMP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 496885b8267d339c7617ec24b884fa193f8d9945
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322936"
---
# <a name="d3dgammaramp-structure"></a><span data-ttu-id="2bcaa-103">Struttura D3DGAMMARAMP</span><span class="sxs-lookup"><span data-stu-id="2bcaa-103">D3DGAMMARAMP structure</span></span>

<span data-ttu-id="2bcaa-104">Contiene dati di rampa rosso, verde e blu.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-104">Contains red, green, and blue ramp data.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bcaa-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2bcaa-105">Syntax</span></span>


```C++
typedef struct D3DGAMMARAMP {
  WORD red[256];
  WORD green[256];
  WORD blue[256];
} D3DGAMMARAMP, *LPD3DGAMMARAMP;
```



## <a name="members"></a><span data-ttu-id="2bcaa-106">Members</span><span class="sxs-lookup"><span data-stu-id="2bcaa-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2bcaa-107">**Red**</span><span class="sxs-lookup"><span data-stu-id="2bcaa-107">**red**</span></span>
</dt> <dd>

<span data-ttu-id="2bcaa-108">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2bcaa-108">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2bcaa-109">Matrice di elementi di 256 parole che descrivono la rampa di gamma rossa.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-109">Array of 256 WORD element that describes the red gamma ramp.</span></span>

</dd> <dt>

<span data-ttu-id="2bcaa-110">**verde**</span><span class="sxs-lookup"><span data-stu-id="2bcaa-110">**green**</span></span>
</dt> <dd>

<span data-ttu-id="2bcaa-111">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2bcaa-111">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2bcaa-112">Matrice di elementi di 256 parole che descrivono la rampa gamma verde.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-112">Array of 256 WORD element that describes the green gamma ramp.</span></span>

</dd> <dt>

<span data-ttu-id="2bcaa-113">**blu**</span><span class="sxs-lookup"><span data-stu-id="2bcaa-113">**blue**</span></span>
</dt> <dd>

<span data-ttu-id="2bcaa-114">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2bcaa-114">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2bcaa-115">Matrice di elementi di 256 parole che descrivono la rampa di gamma blu.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-115">Array of 256 WORD element that describes the blue gamma ramp.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2bcaa-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2bcaa-116">Requirements</span></span>



| <span data-ttu-id="2bcaa-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bcaa-117">Requirement</span></span> | <span data-ttu-id="2bcaa-118">Valore</span><span class="sxs-lookup"><span data-stu-id="2bcaa-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2bcaa-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2bcaa-119">Header</span></span><br/> | <dl> <span data-ttu-id="2bcaa-120"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bcaa-120"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bcaa-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2bcaa-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bcaa-122">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="2bcaa-122">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="2bcaa-123">**GetGammaRamp**</span><span class="sxs-lookup"><span data-stu-id="2bcaa-123">**GetGammaRamp**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp)
</dt> <dt>

[<span data-ttu-id="2bcaa-124">**SetGammaRamp**</span><span class="sxs-lookup"><span data-stu-id="2bcaa-124">**SetGammaRamp**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)
</dt> </dl>

 

 
