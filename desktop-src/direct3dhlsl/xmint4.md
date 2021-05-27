---
title: Struttura XMINT4
description: Descrive un vettore integer 4D.
ms.assetid: 1f21727d-fcb4-4514-b30e-d8ef0e36c256
keywords:
- Struttura XMINT4 HLSL
topic_type:
- apiref
api_name:
- XMINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead9e7da8d48025c456ae6e57b0ffe64cdb00f46
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549956"
---
# <a name="xmint4-structure"></a><span data-ttu-id="29c03-104">Struttura XMINT4</span><span class="sxs-lookup"><span data-stu-id="29c03-104">XMINT4 structure</span></span>

<span data-ttu-id="29c03-105">Descrive un vettore integer 4D.</span><span class="sxs-lookup"><span data-stu-id="29c03-105">Describes an 4D integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="29c03-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="29c03-106">Syntax</span></span>


``` syntax
typedef struct _XMINT4 {
  INT x;
  INT {
    INT {
      INT w;
    }z;
  }y;
} XMINT4;
```



## <a name="members"></a><span data-ttu-id="29c03-107">Members</span><span class="sxs-lookup"><span data-stu-id="29c03-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="29c03-108">**x**</span><span class="sxs-lookup"><span data-stu-id="29c03-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="29c03-109">Componente x del vettore.</span><span class="sxs-lookup"><span data-stu-id="29c03-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="29c03-110">**y**</span><span class="sxs-lookup"><span data-stu-id="29c03-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="29c03-111">Componente y del vettore.</span><span class="sxs-lookup"><span data-stu-id="29c03-111">y-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="29c03-112">**z**</span><span class="sxs-lookup"><span data-stu-id="29c03-112">**z**</span></span>
</dt> <dd>

<span data-ttu-id="29c03-113">Componente z del vettore.</span><span class="sxs-lookup"><span data-stu-id="29c03-113">z-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="29c03-114">**w**</span><span class="sxs-lookup"><span data-stu-id="29c03-114">**w**</span></span>
</dt> <dd>

<span data-ttu-id="29c03-115">w-component del vettore.</span><span class="sxs-lookup"><span data-stu-id="29c03-115">w-component of the vector.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="29c03-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29c03-116">Requirements</span></span>



| <span data-ttu-id="29c03-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="29c03-117">Requirement</span></span> | <span data-ttu-id="29c03-118">Valore</span><span class="sxs-lookup"><span data-stu-id="29c03-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29c03-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="29c03-119">Header</span></span><br/> | <dl> <span data-ttu-id="29c03-120"><dt>D3DX \_ DXGIFormatConvert.inl</dt></span><span class="sxs-lookup"><span data-stu-id="29c03-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="remarks"></a><span data-ttu-id="29c03-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="29c03-121">Remarks</span></span>

<span data-ttu-id="29c03-122">Questa struttura è definita ``D3DX\_DXGIFormatConvert.inl`` nell'intestazione in DirectX SDK (giugno 2010) per l'uso da C++.</span><span class="sxs-lookup"><span data-stu-id="29c03-122">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="29c03-123">La versione più recente di questa intestazione nel pacchetto NuGet [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) non la definisce più e si basa invece su [DirectX::XMINT4](/windows/win32/api/directxmath/ns-directxmath-xmint4) in DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="29c03-123">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMINT4](/windows/win32/api/directxmath/ns-directxmath-xmint4) in DirectXMath instead.</span></span>



## <a name="see-also"></a><span data-ttu-id="29c03-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29c03-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29c03-125">Strutture</span><span class="sxs-lookup"><span data-stu-id="29c03-125">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="29c03-126">Decompressione e impacchettamento del formato DXGI \_ per la In-Place di immagini</span><span class="sxs-lookup"><span data-stu-id="29c03-126">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>