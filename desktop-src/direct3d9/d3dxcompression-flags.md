---
description: Definisce la modalità di compressione utilizzata per l'archiviazione dei dati del set di animazioni compresso.
ms.assetid: 41592b71-52ba-4727-a885-fb10fc23c5f8
title: Enumerazione D3DXCOMPRESSION_FLAGS (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCOMPRESSION_FLAGS
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 6f912c44659d418d543194ba82a9d82f31e7ef08
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322871"
---
# <a name="d3dxcompression_flags-enumeration"></a><span data-ttu-id="c7c42-103">\_Enumerazione flag D3DXCOMPRESSION</span><span class="sxs-lookup"><span data-stu-id="c7c42-103">D3DXCOMPRESSION\_FLAGS enumeration</span></span>

<span data-ttu-id="c7c42-104">Definisce la modalità di compressione utilizzata per l'archiviazione dei dati del set di animazioni compresso.</span><span class="sxs-lookup"><span data-stu-id="c7c42-104">Defines the compression mode used for storing compressed animation set data.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7c42-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c7c42-105">Syntax</span></span>


```C++
typedef enum D3DXCOMPRESSION_FLAGS { 
  D3DXCOMPRESS_DEFAULT      = 0,
  D3DXCOMPRESS_STRONG       = 1,
  D3DXCOMPRESS_FORCE_DWORD  = 0x7fffffff
} D3DXCOMPRESSION_FLAGS, *LPD3DXCOMPRESSION_FLAGS;
```



## <a name="constants"></a><span data-ttu-id="c7c42-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="c7c42-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c7c42-107"><span id="D3DXCOMPRESS_DEFAULT"></span><span id="d3dxcompress_default"></span>**\_Impostazione predefinita D3DXCOMPRESS**</span><span class="sxs-lookup"><span data-stu-id="c7c42-107"><span id="D3DXCOMPRESS_DEFAULT"></span><span id="d3dxcompress_default"></span>**D3DXCOMPRESS\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="c7c42-108">Implementa la compressione rapida.</span><span class="sxs-lookup"><span data-stu-id="c7c42-108">Implements fast compression.</span></span>

</dd> <dt>

<span data-ttu-id="c7c42-109"><span id="D3DXCOMPRESS_STRONG"></span><span id="d3dxcompress_strong"></span>**D3DXCOMPRESS \_ forte**</span><span class="sxs-lookup"><span data-stu-id="c7c42-109"><span id="D3DXCOMPRESS_STRONG"></span><span id="d3dxcompress_strong"></span>**D3DXCOMPRESS\_STRONG**</span></span>
</dt> <dd>

<span data-ttu-id="c7c42-110">Implementa la compressione lenta.</span><span class="sxs-lookup"><span data-stu-id="c7c42-110">Implements slow compression.</span></span> <span data-ttu-id="c7c42-111">Viene in genere creato un set di animazioni compresso di qualità superiore rispetto a quando \_ si usa l'impostazione predefinita D3DXCOMPRESS.</span><span class="sxs-lookup"><span data-stu-id="c7c42-111">Typically results in a better quality compressed animation set than if D3DXCOMPRESS\_DEFAULT is used.</span></span>

</dd> <dt>

<span data-ttu-id="c7c42-112"><span id="D3DXCOMPRESS_FORCE_DWORD"></span><span id="d3dxcompress_force_dword"></span>**D3DXCOMPRESS \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="c7c42-112"><span id="D3DXCOMPRESS_FORCE_DWORD"></span><span id="d3dxcompress_force_dword"></span>**D3DXCOMPRESS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="c7c42-113">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="c7c42-113">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="c7c42-114">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="c7c42-114">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="c7c42-115">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="c7c42-115">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c7c42-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c7c42-116">Requirements</span></span>



| <span data-ttu-id="c7c42-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7c42-117">Requirement</span></span> | <span data-ttu-id="c7c42-118">Valore</span><span class="sxs-lookup"><span data-stu-id="c7c42-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7c42-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c7c42-119">Header</span></span><br/> | <dl> <span data-ttu-id="c7c42-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7c42-120"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7c42-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c7c42-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7c42-122">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="c7c42-122">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




