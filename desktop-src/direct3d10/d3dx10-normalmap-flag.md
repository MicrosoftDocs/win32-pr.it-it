---
description: Questi flag vengono utilizzati per controllare il modo in cui D3DX10ComputeNormalMap genera mappe normali. Qualsiasi numero di flag può essere o combinato in qualsiasi combinazione.
ms.assetid: 307936c1-3137-41fe-8bea-7a82e6db0867
title: Enumerazione D3DX10_NORMALMAP_FLAG (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_NORMALMAP_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: c4b6962561007fbc3e64b471c045e98b2f8328b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322954"
---
# <a name="d3dx10_normalmap_flag-enumeration"></a><span data-ttu-id="b79be-104">\_ \_ Enumerazione flag normalmap d3dx10</span><span class="sxs-lookup"><span data-stu-id="b79be-104">D3DX10\_NORMALMAP\_FLAG enumeration</span></span>

<span data-ttu-id="b79be-105">Questi flag vengono utilizzati per controllare il modo in cui [**D3DX10ComputeNormalMap**](d3dx10computenormalmap.md) genera mappe normali.</span><span class="sxs-lookup"><span data-stu-id="b79be-105">These flags are used to control how [**D3DX10ComputeNormalMap**](d3dx10computenormalmap.md) generates normal maps.</span></span> <span data-ttu-id="b79be-106">Qualsiasi numero di flag può essere o combinato in qualsiasi combinazione.</span><span class="sxs-lookup"><span data-stu-id="b79be-106">Any number of these flags may be OR'd together in any combination.</span></span>

## <a name="syntax"></a><span data-ttu-id="b79be-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b79be-107">Syntax</span></span>


```C++
typedef enum D3DX10_NORMALMAP_FLAG { 
  D3DX10_NORMALMAP_MIRROR_U           = (1 << 16),
  D3DX10_NORMALMAP_MIRROR_V           = (2 << 16),
  D3DX10_NORMALMAP_MIRROR             = (3 << 16),
  D3DX10_NORMALMAP_INVERTSIGN         = (8 << 16),
  D3DX10_NORMALMAP_COMPUTE_OCCLUSION  = (16 << 16)
} D3DX10_NORMALMAP_FLAG, *LPD3DX10_NORMALMAP_FLAG;
```



## <a name="constants"></a><span data-ttu-id="b79be-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="b79be-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b79be-109"><span id="D3DX10_NORMALMAP_MIRROR_U"></span><span id="d3dx10_normalmap_mirror_u"></span>**D3DX10 \_ normalmap \_ mirror \_ U**</span><span class="sxs-lookup"><span data-stu-id="b79be-109"><span id="D3DX10_NORMALMAP_MIRROR_U"></span><span id="d3dx10_normalmap_mirror_u"></span>**D3DX10\_NORMALMAP\_MIRROR\_U**</span></span>
</dt> <dd>

<span data-ttu-id="b79be-110">Indica che i pixel al di fuori del bordo della trama sull'asse U devono essere rispecchiati, non a capo.</span><span class="sxs-lookup"><span data-stu-id="b79be-110">Indicates that pixels off the edge of the texture on the U-axis should be mirrored, not wraped.</span></span>

</dd> <dt>

<span data-ttu-id="b79be-111"><span id="D3DX10_NORMALMAP_MIRROR_V"></span><span id="d3dx10_normalmap_mirror_v"></span>**D3DX10 \_ normalmap \_ mirror \_ V**</span><span class="sxs-lookup"><span data-stu-id="b79be-111"><span id="D3DX10_NORMALMAP_MIRROR_V"></span><span id="d3dx10_normalmap_mirror_v"></span>**D3DX10\_NORMALMAP\_MIRROR\_V**</span></span>
</dt> <dd>

<span data-ttu-id="b79be-112">Indica che è necessario eseguire il mirroring dei pixel al di fuori del bordo della trama sull'asse V, senza eseguire il wrapping.</span><span class="sxs-lookup"><span data-stu-id="b79be-112">Indicates that pixels off the edge of the texture on the V-axis should be mirrored, not wraped.</span></span>

</dd> <dt>

<span data-ttu-id="b79be-113"><span id="D3DX10_NORMALMAP_MIRROR"></span><span id="d3dx10_normalmap_mirror"></span>**\_Mirror normalmap \_ d3dx10**</span><span class="sxs-lookup"><span data-stu-id="b79be-113"><span id="D3DX10_NORMALMAP_MIRROR"></span><span id="d3dx10_normalmap_mirror"></span>**D3DX10\_NORMALMAP\_MIRROR**</span></span>
</dt> <dd>

<span data-ttu-id="b79be-114">Uguale a D3DX10 \_ normalmap \_ mirror \_ U \| d3dx10 \_ normalmap \_ mirror \_ V.</span><span class="sxs-lookup"><span data-stu-id="b79be-114">Same as D3DX10\_NORMALMAP\_MIRROR\_U \| D3DX10\_NORMALMAP\_MIRROR\_V.</span></span>

</dd> <dt>

<span data-ttu-id="b79be-115"><span id="D3DX10_NORMALMAP_INVERTSIGN"></span><span id="d3dx10_normalmap_invertsign"></span>**D3DX10 \_ normalmap \_ INVERTSIGN**</span><span class="sxs-lookup"><span data-stu-id="b79be-115"><span id="D3DX10_NORMALMAP_INVERTSIGN"></span><span id="d3dx10_normalmap_invertsign"></span>**D3DX10\_NORMALMAP\_INVERTSIGN**</span></span>
</dt> <dd>

<span data-ttu-id="b79be-116">Inverte la direzione di ogni normale.</span><span class="sxs-lookup"><span data-stu-id="b79be-116">Inverts the direction of each normal.</span></span>

</dd> <dt>

<span data-ttu-id="b79be-117"><span id="D3DX10_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx10_normalmap_compute_occlusion"></span>**\_ \_ Occlusione di calcolo normalmap d3dx10 \_**</span><span class="sxs-lookup"><span data-stu-id="b79be-117"><span id="D3DX10_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx10_normalmap_compute_occlusion"></span>**D3DX10\_NORMALMAP\_COMPUTE\_OCCLUSION**</span></span>
</dt> <dd>

<span data-ttu-id="b79be-118">Calcola il termine di occlusione per pixel e lo codifica in alfa.</span><span class="sxs-lookup"><span data-stu-id="b79be-118">Computes the per pixel occlusion term and encodes it into the alpha.</span></span> <span data-ttu-id="b79be-119">Un valore alfa pari a 1 indica che il pixel non è nascosto in alcun modo, mentre un valore alfa pari a 0 indica che il pixel è completamente nascosto.</span><span class="sxs-lookup"><span data-stu-id="b79be-119">An Alpha of 1 means that the pixel is not obscured in any way, and an alpha of 0 would mean that the pixel is completely obscured.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b79be-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b79be-120">Requirements</span></span>



| <span data-ttu-id="b79be-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b79be-121">Requirement</span></span> | <span data-ttu-id="b79be-122">Valore</span><span class="sxs-lookup"><span data-stu-id="b79be-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b79be-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b79be-123">Header</span></span><br/> | <dl> <span data-ttu-id="b79be-124"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="b79be-124"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b79be-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b79be-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b79be-126">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="b79be-126">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




