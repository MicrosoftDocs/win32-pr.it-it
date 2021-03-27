---
title: Enumerazione D3DX11_NORMALMAP_FLAG (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Opzioni di mappa normali. È possibile combinare un numero qualsiasi di questi flag usando un'operazione OR bit per bit.
ms.assetid: cc9c8a54-be1e-4594-8274-9955562a6fa8
keywords:
- Enumerazione D3DX11_NORMALMAP_FLAG Direct3D 11
- Puntatore di enumerazione LPD3DX11_NORMALMAP_FLAG Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_NORMALMAP_FLAG
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37f5d9669370e6df03d783ae1cb82a5eeb5a9142
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235204"
---
# <a name="d3dx11_normalmap_flag-enumeration"></a><span data-ttu-id="64c1b-107">\_ \_ Enumerazione flag normalmap D3DX11</span><span class="sxs-lookup"><span data-stu-id="64c1b-107">D3DX11\_NORMALMAP\_FLAG enumeration</span></span>

> [!Note]  
> <span data-ttu-id="64c1b-108">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="64c1b-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="64c1b-109">Opzioni di mappa normali.</span><span class="sxs-lookup"><span data-stu-id="64c1b-109">Normal map options.</span></span> <span data-ttu-id="64c1b-110">È possibile combinare un numero qualsiasi di questi flag usando un'operazione OR bit per bit.</span><span class="sxs-lookup"><span data-stu-id="64c1b-110">You can combine any number of these flags by using a bitwise OR operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="64c1b-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="64c1b-111">Syntax</span></span>


```C++
typedef enum D3DX11_NORMALMAP_FLAG { 
  D3DX11_NORMALMAP_MIRROR_U           = (1 << 16),
  D3DX11_NORMALMAP_MIRROR_V           = (2 << 16),
  D3DX11_NORMALMAP_MIRROR             = (3 << 16),
  D3DX11_NORMALMAP_INVERTSIGN         = (8 << 16),
  D3DX11_NORMALMAP_COMPUTE_OCCLUSION  = (16 << 16)
} D3DX11_NORMALMAP_FLAG, *LPD3DX11_NORMALMAP_FLAG;
```



## <a name="constants"></a><span data-ttu-id="64c1b-112">Costanti</span><span class="sxs-lookup"><span data-stu-id="64c1b-112">Constants</span></span>

<dl> <dt>

<span data-ttu-id="64c1b-113"><span id="D3DX11_NORMALMAP_MIRROR_U"></span><span id="d3dx11_normalmap_mirror_u"></span>**D3DX11 \_ normalmap \_ mirror \_ U**</span><span class="sxs-lookup"><span data-stu-id="64c1b-113"><span id="D3DX11_NORMALMAP_MIRROR_U"></span><span id="d3dx11_normalmap_mirror_u"></span>**D3DX11\_NORMALMAP\_MIRROR\_U**</span></span>
</dt> <dd>

<span data-ttu-id="64c1b-114">Indica che i pixel al di fuori del bordo della trama sull'asse U devono essere rispecchiati, non a capo.</span><span class="sxs-lookup"><span data-stu-id="64c1b-114">Indicates that pixels off the edge of the texture on the U-axis should be mirrored, not wraped.</span></span>

</dd> <dt>

<span data-ttu-id="64c1b-115"><span id="D3DX11_NORMALMAP_MIRROR_V"></span><span id="d3dx11_normalmap_mirror_v"></span>**D3DX11 \_ normalmap \_ mirror \_ V**</span><span class="sxs-lookup"><span data-stu-id="64c1b-115"><span id="D3DX11_NORMALMAP_MIRROR_V"></span><span id="d3dx11_normalmap_mirror_v"></span>**D3DX11\_NORMALMAP\_MIRROR\_V**</span></span>
</dt> <dd>

<span data-ttu-id="64c1b-116">Indica che è necessario eseguire il mirroring dei pixel al di fuori del bordo della trama sull'asse V, senza eseguire il wrapping.</span><span class="sxs-lookup"><span data-stu-id="64c1b-116">Indicates that pixels off the edge of the texture on the V-axis should be mirrored, not wraped.</span></span>

</dd> <dt>

<span data-ttu-id="64c1b-117"><span id="D3DX11_NORMALMAP_MIRROR"></span><span id="d3dx11_normalmap_mirror"></span>**\_Mirror normalmap \_ D3DX11**</span><span class="sxs-lookup"><span data-stu-id="64c1b-117"><span id="D3DX11_NORMALMAP_MIRROR"></span><span id="d3dx11_normalmap_mirror"></span>**D3DX11\_NORMALMAP\_MIRROR**</span></span>
</dt> <dd>

<span data-ttu-id="64c1b-118">Uguale a D3DX11 \_ normalmap \_ mirror \_ U \| D3DX11 \_ normalmap \_ mirror \_ V.</span><span class="sxs-lookup"><span data-stu-id="64c1b-118">Same as D3DX11\_NORMALMAP\_MIRROR\_U \| D3DX11\_NORMALMAP\_MIRROR\_V.</span></span>

</dd> <dt>

<span data-ttu-id="64c1b-119"><span id="D3DX11_NORMALMAP_INVERTSIGN"></span><span id="d3dx11_normalmap_invertsign"></span>**D3DX11 \_ normalmap \_ INVERTSIGN**</span><span class="sxs-lookup"><span data-stu-id="64c1b-119"><span id="D3DX11_NORMALMAP_INVERTSIGN"></span><span id="d3dx11_normalmap_invertsign"></span>**D3DX11\_NORMALMAP\_INVERTSIGN**</span></span>
</dt> <dd>

<span data-ttu-id="64c1b-120">Inverte la direzione di ogni normale.</span><span class="sxs-lookup"><span data-stu-id="64c1b-120">Inverts the direction of each normal.</span></span>

</dd> <dt>

<span data-ttu-id="64c1b-121"><span id="D3DX11_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx11_normalmap_compute_occlusion"></span>**\_ \_ Occlusione di calcolo normalmap D3DX11 \_**</span><span class="sxs-lookup"><span data-stu-id="64c1b-121"><span id="D3DX11_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx11_normalmap_compute_occlusion"></span>**D3DX11\_NORMALMAP\_COMPUTE\_OCCLUSION**</span></span>
</dt> <dd>

<span data-ttu-id="64c1b-122">Calcola il termine di occlusione per pixel e lo codifica in alfa.</span><span class="sxs-lookup"><span data-stu-id="64c1b-122">Computes the per pixel occlusion term and encodes it into the alpha.</span></span> <span data-ttu-id="64c1b-123">Un valore alfa pari a 1 indica che il pixel non è nascosto in alcun modo, mentre un valore alfa pari a 0 indica che il pixel è completamente nascosto.</span><span class="sxs-lookup"><span data-stu-id="64c1b-123">An Alpha of 1 means that the pixel is not obscured in any way, and an alpha of 0 would mean that the pixel is completely obscured.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="64c1b-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="64c1b-124">Remarks</span></span>

<span data-ttu-id="64c1b-125">Questi flag vengono usati da [**D3DX11ComputeNormalMap**](d3dx11computenormalmap.md).</span><span class="sxs-lookup"><span data-stu-id="64c1b-125">These flags are used by [**D3DX11ComputeNormalMap**](d3dx11computenormalmap.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="64c1b-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="64c1b-126">Requirements</span></span>



| <span data-ttu-id="64c1b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="64c1b-127">Requirement</span></span> | <span data-ttu-id="64c1b-128">Valore</span><span class="sxs-lookup"><span data-stu-id="64c1b-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="64c1b-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="64c1b-129">Header</span></span><br/> | <dl> <span data-ttu-id="64c1b-130"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="64c1b-130"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64c1b-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="64c1b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64c1b-132">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="64c1b-132">D3DX Enumerations</span></span>](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





