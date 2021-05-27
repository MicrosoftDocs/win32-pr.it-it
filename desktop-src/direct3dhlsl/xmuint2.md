---
title: Struttura XMUINT2
description: Descrive un vettore integer senza segno 2D.
ms.assetid: 8622eca1-fc8f-4129-a375-142b4f4018b0
keywords:
- Struttura XMUINT2 HLSL
topic_type:
- apiref
api_name:
- XMUINT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71168d08b8a91e09429a6f4e004c48c699635414
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549566"
---
# <a name="xmuint2-structure"></a><span data-ttu-id="6fb28-104">Struttura XMUINT2</span><span class="sxs-lookup"><span data-stu-id="6fb28-104">XMUINT2 structure</span></span>

<span data-ttu-id="6fb28-105">Descrive un vettore integer senza segno 2D.</span><span class="sxs-lookup"><span data-stu-id="6fb28-105">Describes an 2D unsigned integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fb28-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6fb28-106">Syntax</span></span>


``` syntax
typedef struct _XMUINT2 {
  UINT x;
  UINT y;
} XMUINT2;
```



## <a name="members"></a><span data-ttu-id="6fb28-107">Members</span><span class="sxs-lookup"><span data-stu-id="6fb28-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6fb28-108">**x**</span><span class="sxs-lookup"><span data-stu-id="6fb28-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="6fb28-109">Componente x del vettore.</span><span class="sxs-lookup"><span data-stu-id="6fb28-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="6fb28-110">**y**</span><span class="sxs-lookup"><span data-stu-id="6fb28-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="6fb28-111">Componente y del vettore.</span><span class="sxs-lookup"><span data-stu-id="6fb28-111">y-component of the vector.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="6fb28-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="6fb28-112">Remarks</span></span>

<span data-ttu-id="6fb28-113">Questa struttura è definita ``D3DX\_DXGIFormatConvert.inl`` nell'intestazione in DirectX SDK (giugno 2010) per l'uso da C++.</span><span class="sxs-lookup"><span data-stu-id="6fb28-113">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="6fb28-114">La versione più recente di questa intestazione nel pacchetto NuGet [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) non la definisce più e si basa invece su [DirectX::XMUINT2](/windows/win32/api/directxmath/ns-directxmath-xmuint2) in DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="6fb28-114">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMUINT2](/windows/win32/api/directxmath/ns-directxmath-xmuint2) in DirectXMath instead.</span></span>



## <a name="requirements"></a><span data-ttu-id="6fb28-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6fb28-115">Requirements</span></span>



| <span data-ttu-id="6fb28-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fb28-116">Requirement</span></span> | <span data-ttu-id="6fb28-117">Valore</span><span class="sxs-lookup"><span data-stu-id="6fb28-117">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fb28-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6fb28-118">Header</span></span><br/> | <dl> <span data-ttu-id="6fb28-119"><dt>D3DX \_ DXGIFormatConvert.inl</dt></span><span class="sxs-lookup"><span data-stu-id="6fb28-119"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fb28-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6fb28-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fb28-121">Strutture</span><span class="sxs-lookup"><span data-stu-id="6fb28-121">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="6fb28-122">Decompressione e impacchettamento del formato DXGI \_ per la In-Place di immagini</span><span class="sxs-lookup"><span data-stu-id="6fb28-122">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>