---
description: Impostazione di compressione armonica sferica (SH).
ms.assetid: 214d6efb-419d-4eea-8360-322885c26bc3
title: Enumerazione D3DXSHCOMPRESSQUALITYTYPE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHCOMPRESSQUALITYTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: d61c70317505442ca4911a13dac8566f9bd7c6fb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234999"
---
# <a name="d3dxshcompressqualitytype-enumeration"></a><span data-ttu-id="504a6-103">Enumerazione D3DXSHCOMPRESSQUALITYTYPE</span><span class="sxs-lookup"><span data-stu-id="504a6-103">D3DXSHCOMPRESSQUALITYTYPE enumeration</span></span>

<span data-ttu-id="504a6-104">Impostazione di compressione armonica sferica (SH).</span><span class="sxs-lookup"><span data-stu-id="504a6-104">Spherical harmonic (SH) compression setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="504a6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="504a6-105">Syntax</span></span>


```C++
typedef enum D3DXSHCOMPRESSQUALITYTYPE { 
  D3DXSHCQUAL_FASTLOWQUALITY   = 1,
  D3DXSHCQUAL_SLOWHIGHQUALITY  = 2,
  D3DXSHCQUAL_FORCE_DWORD      = 0x7fffffff
} D3DXSHCOMPRESSQUALITYTYPE, *LPD3DXSHCOMPRESSQUALITYTYPE;
```



## <a name="constants"></a><span data-ttu-id="504a6-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="504a6-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="504a6-107"><span id="D3DXSHCQUAL_FASTLOWQUALITY"></span><span id="d3dxshcqual_fastlowquality"></span>**\_FASTLOWQUALITY D3DXSHCQUAL**</span><span class="sxs-lookup"><span data-stu-id="504a6-107"><span id="D3DXSHCQUAL_FASTLOWQUALITY"></span><span id="d3dxshcqual_fastlowquality"></span>**D3DXSHCQUAL\_FASTLOWQUALITY**</span></span>
</dt> <dd>

<span data-ttu-id="504a6-108">La compressione dei dati è di bassa qualità, ma è veloce da comprimere.</span><span class="sxs-lookup"><span data-stu-id="504a6-108">The data compression is low quality, but is fast to compress.</span></span>

</dd> <dt>

<span data-ttu-id="504a6-109"><span id="D3DXSHCQUAL_SLOWHIGHQUALITY"></span><span id="d3dxshcqual_slowhighquality"></span>**\_SLOWHIGHQUALITY D3DXSHCQUAL**</span><span class="sxs-lookup"><span data-stu-id="504a6-109"><span id="D3DXSHCQUAL_SLOWHIGHQUALITY"></span><span id="d3dxshcqual_slowhighquality"></span>**D3DXSHCQUAL\_SLOWHIGHQUALITY**</span></span>
</dt> <dd>

<span data-ttu-id="504a6-110">La compressione dei dati è di qualità elevata, ma è lenta da comprimere.</span><span class="sxs-lookup"><span data-stu-id="504a6-110">The data compression is high quality, but is slow to compress.</span></span>

</dd> <dt>

<span data-ttu-id="504a6-111"><span id="D3DXSHCQUAL_FORCE_DWORD"></span><span id="d3dxshcqual_force_dword"></span>**D3DXSHCQUAL \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="504a6-111"><span id="D3DXSHCQUAL_FORCE_DWORD"></span><span id="d3dxshcqual_force_dword"></span>**D3DXSHCQUAL\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="504a6-112">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="504a6-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="504a6-113">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="504a6-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="504a6-114">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="504a6-114">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="504a6-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="504a6-115">Requirements</span></span>



| <span data-ttu-id="504a6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="504a6-116">Requirement</span></span> | <span data-ttu-id="504a6-117">Valore</span><span class="sxs-lookup"><span data-stu-id="504a6-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="504a6-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="504a6-118">Header</span></span><br/> | <dl> <span data-ttu-id="504a6-119"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="504a6-119"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="504a6-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="504a6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="504a6-121">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="504a6-121">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




