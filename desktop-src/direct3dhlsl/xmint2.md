---
title: Struttura XMINT2
description: Descrive un vettore integer 2D.
ms.assetid: 651f62f8-577d-4356-9bbc-0d4a9ca8fb01
keywords:
- Struttura XMINT2 HLSL
topic_type:
- apiref
api_name:
- XMINT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5dfe4aab8a23dbf1b7921742272b0d2b0ab2382
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549986"
---
# <a name="xmint2-structure"></a><span data-ttu-id="e07b4-104">Struttura XMINT2</span><span class="sxs-lookup"><span data-stu-id="e07b4-104">XMINT2 structure</span></span>

<span data-ttu-id="e07b4-105">Descrive un vettore integer 2D.</span><span class="sxs-lookup"><span data-stu-id="e07b4-105">Describes an 2D integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="e07b4-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e07b4-106">Syntax</span></span>


``` syntax
typedef struct _XMINT2 {
  INT x;
  INT y;
} XMINT2;
```



## <a name="members"></a><span data-ttu-id="e07b4-107">Members</span><span class="sxs-lookup"><span data-stu-id="e07b4-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e07b4-108">**x**</span><span class="sxs-lookup"><span data-stu-id="e07b4-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="e07b4-109">Componente x del vettore.</span><span class="sxs-lookup"><span data-stu-id="e07b4-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="e07b4-110">**y**</span><span class="sxs-lookup"><span data-stu-id="e07b4-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="e07b4-111">Componente y del vettore.</span><span class="sxs-lookup"><span data-stu-id="e07b4-111">y-component of the vector.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="e07b4-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="e07b4-112">Remarks</span></span>

<span data-ttu-id="e07b4-113">Questa struttura è definita ``D3DX\_DXGIFormatConvert.inl`` nell'intestazione di DirectX SDK (giugno 2010) per l'uso da C++.</span><span class="sxs-lookup"><span data-stu-id="e07b4-113">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="e07b4-114">La versione più recente di questa intestazione nel pacchetto NuGet [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) non la definisce più e si basa invece su [DirectX::XMINT2](/windows/win32/api/directxmath/ns-directxmath-xmint2) in DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="e07b4-114">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMINT2](/windows/win32/api/directxmath/ns-directxmath-xmint2) in DirectXMath instead.</span></span>



## <a name="requirements"></a><span data-ttu-id="e07b4-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e07b4-115">Requirements</span></span>



| <span data-ttu-id="e07b4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e07b4-116">Requirement</span></span> | <span data-ttu-id="e07b4-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e07b4-117">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e07b4-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e07b4-118">Header</span></span><br/> | <dl> <span data-ttu-id="e07b4-119"><dt>D3DX \_ DXGIFormatConvert.inl</dt></span><span class="sxs-lookup"><span data-stu-id="e07b4-119"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e07b4-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e07b4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e07b4-121">Strutture</span><span class="sxs-lookup"><span data-stu-id="e07b4-121">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="e07b4-122">Decompressione e creazione di un pacchetto DXGI \_ FORMAT per la In-Place di immagini</span><span class="sxs-lookup"><span data-stu-id="e07b4-122">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>