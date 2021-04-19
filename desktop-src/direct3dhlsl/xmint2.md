---
title: Struttura XMINT2
description: Descrive un vettore di interi 2D.
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
ms.openlocfilehash: 1e93e26933ad6b3829848e7e826d8d9685e9f141
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222859"
---
# <a name="xmint2-structure"></a><span data-ttu-id="94bd3-104">Struttura XMINT2</span><span class="sxs-lookup"><span data-stu-id="94bd3-104">XMINT2 structure</span></span>

<span data-ttu-id="94bd3-105">Descrive un vettore di interi 2D.</span><span class="sxs-lookup"><span data-stu-id="94bd3-105">Describes an 2D integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="94bd3-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="94bd3-106">Syntax</span></span>


``` syntax
typedef struct _XMINT2 {
  INT x;
  INT y;
} XMINT2;
```



## <a name="members"></a><span data-ttu-id="94bd3-107">Members</span><span class="sxs-lookup"><span data-stu-id="94bd3-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="94bd3-108">**x**</span><span class="sxs-lookup"><span data-stu-id="94bd3-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="94bd3-109">componente x del vettore.</span><span class="sxs-lookup"><span data-stu-id="94bd3-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="94bd3-110">**y**</span><span class="sxs-lookup"><span data-stu-id="94bd3-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="94bd3-111">componente y del vettore.</span><span class="sxs-lookup"><span data-stu-id="94bd3-111">y-component of the vector.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="94bd3-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="94bd3-112">Remarks</span></span>

<span data-ttu-id="94bd3-113">Questa struttura è definita nell' ``D3DX\_DXGIFormatConvert.inl`` intestazione in DirectX SDK (giugno 2010) per l'uso da C++.</span><span class="sxs-lookup"><span data-stu-id="94bd3-113">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="94bd3-114">La versione più recente di questa intestazione nel pacchetto NuGet [Microsoft. DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) non la definisce più e si basa invece su [DirectX:: XMINT2](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmint2) in DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="94bd3-114">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMINT2](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmint2) in DirectXMath instead.</span></span>



## <a name="requirements"></a><span data-ttu-id="94bd3-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="94bd3-115">Requirements</span></span>



| <span data-ttu-id="94bd3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="94bd3-116">Requirement</span></span> | <span data-ttu-id="94bd3-117">Valore</span><span class="sxs-lookup"><span data-stu-id="94bd3-117">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94bd3-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="94bd3-118">Header</span></span><br/> | <dl> <span data-ttu-id="94bd3-119"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="94bd3-119"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94bd3-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="94bd3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94bd3-121">Strutture</span><span class="sxs-lookup"><span data-stu-id="94bd3-121">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="94bd3-122">Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place</span><span class="sxs-lookup"><span data-stu-id="94bd3-122">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>
