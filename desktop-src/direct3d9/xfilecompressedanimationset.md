---
description: Identifica i dati di animazione del fotogramma chiave compressi.
ms.assetid: 2aab46db-e0ad-4bbb-b1c5-a254ec6cb984
title: Struttura XFILECOMPRESSEDANIMATIONSET (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- XFILECOMPRESSEDANIMATIONSET
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 240cac57c9c0d123203ee4599c14092df1327f94
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322294"
---
# <a name="xfilecompressedanimationset-structure"></a><span data-ttu-id="b2183-103">Struttura XFILECOMPRESSEDANIMATIONSET</span><span class="sxs-lookup"><span data-stu-id="b2183-103">XFILECOMPRESSEDANIMATIONSET structure</span></span>

<span data-ttu-id="b2183-104">Identifica i dati di animazione del fotogramma chiave compressi.</span><span class="sxs-lookup"><span data-stu-id="b2183-104">Identifies compressed key frame animation data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2183-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2183-105">Syntax</span></span>


```C++
typedef struct XFILECOMPRESSEDANIMATIONSET {
  DWORD CompressedBlockSize;
  FLOAT TicksPerSec;
  DWORD PlaybackType;
  DWORD BufferLength;
} XFILECOMPRESSEDANIMATIONSET, *LPXFILECOMPRESSEDANIMATIONSET;
```



## <a name="members"></a><span data-ttu-id="b2183-106">Members</span><span class="sxs-lookup"><span data-stu-id="b2183-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b2183-107">**CompressedBlockSize**</span><span class="sxs-lookup"><span data-stu-id="b2183-107">**CompressedBlockSize**</span></span>
</dt> <dd>

<span data-ttu-id="b2183-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b2183-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b2183-109">Dimensioni totali, in byte, dei dati compressi nel buffer dei dati di animazione del fotogramma chiave compresso.</span><span class="sxs-lookup"><span data-stu-id="b2183-109">Total size, in bytes, of the compressed data in the compressed key frame animation data buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b2183-110">**TicksPerSec**</span><span class="sxs-lookup"><span data-stu-id="b2183-110">**TicksPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="b2183-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b2183-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b2183-112">Numero di cicli del fotogramma chiave di animazione che si verificano al secondo.</span><span class="sxs-lookup"><span data-stu-id="b2183-112">Number of animation key frame ticks that occur per second.</span></span>

</dd> <dt>

<span data-ttu-id="b2183-113">**PlaybackType**</span><span class="sxs-lookup"><span data-stu-id="b2183-113">**PlaybackType**</span></span>
</dt> <dd>

<span data-ttu-id="b2183-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b2183-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b2183-115">Tipo del ciclo di riproduzione del set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="b2183-115">Type of the animation set playback loop.</span></span> <span data-ttu-id="b2183-116">Vedere [**D3DXPLAYBACK \_ Type**](./d3dxplayback-type.md).</span><span class="sxs-lookup"><span data-stu-id="b2183-116">See [**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2183-117">**BufferLength**</span><span class="sxs-lookup"><span data-stu-id="b2183-117">**BufferLength**</span></span>
</dt> <dd>

<span data-ttu-id="b2183-118">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b2183-118">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b2183-119">Dimensioni minime del buffer, in byte, necessarie per conservare i dati di animazione del fotogramma chiave compressi.</span><span class="sxs-lookup"><span data-stu-id="b2183-119">Minimum buffer size, in bytes, required to hold compressed key frame animation data.</span></span> <span data-ttu-id="b2183-120">Il valore è uguale a ((CompressedBlockSize + 3)/4).</span><span class="sxs-lookup"><span data-stu-id="b2183-120">Value is equal to ( ( CompressedBlockSize + 3 ) / 4 ).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b2183-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2183-121">Requirements</span></span>



| <span data-ttu-id="b2183-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2183-122">Requirement</span></span> | <span data-ttu-id="b2183-123">Valore</span><span class="sxs-lookup"><span data-stu-id="b2183-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2183-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b2183-124">Header</span></span><br/> | <dl> <span data-ttu-id="b2183-125"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2183-125"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2183-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2183-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2183-127">Strutture di file D3DX X</span><span class="sxs-lookup"><span data-stu-id="b2183-127">D3DX X File Structures</span></span>](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> <dt>

[<span data-ttu-id="b2183-128">**ID3DXCompressedAnimationSet**</span><span class="sxs-lookup"><span data-stu-id="b2183-128">**ID3DXCompressedAnimationSet**</span></span>](id3dxcompressedanimationset.md)
</dt> </dl>

 

 
