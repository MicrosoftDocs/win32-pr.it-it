---
title: Struttura XMUINT4
description: Descrive un vettore intero senza segno 4D.
ms.assetid: 289293e5-882e-479c-886e-82c802f824b5
keywords:
- Struttura XMUINT4 HLSL
topic_type:
- apiref
api_name:
- XMUINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e424b4e5fd1c97f5aec01571d887b54dbb143b7
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549896"
---
# <a name="xmuint4-structure"></a><span data-ttu-id="71c9e-104">Struttura XMUINT4</span><span class="sxs-lookup"><span data-stu-id="71c9e-104">XMUINT4 structure</span></span>

<span data-ttu-id="71c9e-105">Descrive un vettore integer senza segno 4D.</span><span class="sxs-lookup"><span data-stu-id="71c9e-105">Describes an 4D unsigned integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="71c9e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="71c9e-106">Syntax</span></span>


``` syntax
typedef struct _XMUINT4 {
  UINT x;
  UINT {
    UINT {
      UINT w;
    }z;
  }y;
} XMUINT4;
```



## <a name="members"></a><span data-ttu-id="71c9e-107">Members</span><span class="sxs-lookup"><span data-stu-id="71c9e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="71c9e-108">**x**</span><span class="sxs-lookup"><span data-stu-id="71c9e-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="71c9e-109">Componente x del vettore.</span><span class="sxs-lookup"><span data-stu-id="71c9e-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="71c9e-110">**y**</span><span class="sxs-lookup"><span data-stu-id="71c9e-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="71c9e-111">Componente y del vettore.</span><span class="sxs-lookup"><span data-stu-id="71c9e-111">y-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="71c9e-112">**z**</span><span class="sxs-lookup"><span data-stu-id="71c9e-112">**z**</span></span>
</dt> <dd>

<span data-ttu-id="71c9e-113">Componente z del vettore.</span><span class="sxs-lookup"><span data-stu-id="71c9e-113">z-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="71c9e-114">**w**</span><span class="sxs-lookup"><span data-stu-id="71c9e-114">**w**</span></span>
</dt> <dd>

<span data-ttu-id="71c9e-115">w-component del vettore.</span><span class="sxs-lookup"><span data-stu-id="71c9e-115">w-component of the vector.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>




## <a name="remarks"></a><span data-ttu-id="71c9e-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="71c9e-116">Remarks</span></span>

<span data-ttu-id="71c9e-117">Questa struttura è definita ``D3DX\_DXGIFormatConvert.inl`` nell'intestazione di DirectX SDK (giugno 2010) per l'uso da C++.</span><span class="sxs-lookup"><span data-stu-id="71c9e-117">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="71c9e-118">La versione più recente di questa intestazione nel pacchetto NuGet [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) non la definisce più e si basa invece su [DirectX::XMUINT4](/windows/win32/api/directxmath/ns-directxmath-xmuint4) in DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="71c9e-118">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMUINT4](/windows/win32/api/directxmath/ns-directxmath-xmuint4) in DirectXMath instead.</span></span>




## <a name="requirements"></a><span data-ttu-id="71c9e-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71c9e-119">Requirements</span></span>



| <span data-ttu-id="71c9e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="71c9e-120">Requirement</span></span> | <span data-ttu-id="71c9e-121">Valore</span><span class="sxs-lookup"><span data-stu-id="71c9e-121">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71c9e-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="71c9e-122">Header</span></span><br/> | <dl> <span data-ttu-id="71c9e-123"><dt>D3DX \_ DXGIFormatConvert.inl</dt></span><span class="sxs-lookup"><span data-stu-id="71c9e-123"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71c9e-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71c9e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71c9e-125">Strutture</span><span class="sxs-lookup"><span data-stu-id="71c9e-125">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="71c9e-126">Decompressione e impacchettamento del formato DXGI \_ per la In-Place di immagini</span><span class="sxs-lookup"><span data-stu-id="71c9e-126">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>