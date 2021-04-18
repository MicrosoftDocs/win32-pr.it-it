---
description: Opzioni di wrapping della trama per le API di calcolo IMT.
ms.assetid: ec364418-67c6-42c7-9c5d-b97aa7e17c24
title: Enumerazione flag D3DXIMT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIMT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 97731d4720e67fce899bf96f457e55f6adbc05a7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322651"
---
# <a name="d3dximt-flags-enumeration"></a><span data-ttu-id="50544-103">Enumerazione flag D3DXIMT</span><span class="sxs-lookup"><span data-stu-id="50544-103">D3DXIMT FLAGS enumeration</span></span>

<span data-ttu-id="50544-104">Opzioni di wrapping della trama per le API di calcolo IMT.</span><span class="sxs-lookup"><span data-stu-id="50544-104">Texture wrapping options for IMT computation APIs.</span></span>

## <a name="syntax"></a><span data-ttu-id="50544-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="50544-105">Syntax</span></span>


```C++
typedef enum D3DXIMT_FLAGS { 
  D3DXIMT_WRAP_U   = 1,
  D3DXIMT_WRAP_V   = 2,
  D3DXIMT_WRAP_UV  = 3
} D3DXIMT FLAGS, *LPD3DXIMT FLAGS;
```



## <a name="constants"></a><span data-ttu-id="50544-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="50544-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="50544-107"><span id="D3DXIMT_WRAP_U"></span><span id="d3dximt_wrap_u"></span>**D3DXIMT a \_ capo automatico \_ U**</span><span class="sxs-lookup"><span data-stu-id="50544-107"><span id="D3DXIMT_WRAP_U"></span><span id="d3dximt_wrap_u"></span>**D3DXIMT\_WRAP\_U**</span></span>
</dt> <dd>

<span data-ttu-id="50544-108">Il wrapping della trama nella direzione U.</span><span class="sxs-lookup"><span data-stu-id="50544-108">The texture wraps in the U direction.</span></span>

</dd> <dt>

<span data-ttu-id="50544-109"><span id="D3DXIMT_WRAP_V"></span><span id="d3dximt_wrap_v"></span>**D3DXIMT \_ Wrap \_ V**</span><span class="sxs-lookup"><span data-stu-id="50544-109"><span id="D3DXIMT_WRAP_V"></span><span id="d3dximt_wrap_v"></span>**D3DXIMT\_WRAP\_V**</span></span>
</dt> <dd>

<span data-ttu-id="50544-110">Il wrapping della trama nella direzione V.</span><span class="sxs-lookup"><span data-stu-id="50544-110">The texture wraps in the V direction.</span></span>

</dd> <dt>

<span data-ttu-id="50544-111"><span id="D3DXIMT_WRAP_UV"></span><span id="d3dximt_wrap_uv"></span>**D3DXIMT a \_ capo \_ UV**</span><span class="sxs-lookup"><span data-stu-id="50544-111"><span id="D3DXIMT_WRAP_UV"></span><span id="d3dximt_wrap_uv"></span>**D3DXIMT\_WRAP\_UV**</span></span>
</dt> <dd>

<span data-ttu-id="50544-112">Il wrapping della trama nella direzione dell'utente e della V.</span><span class="sxs-lookup"><span data-stu-id="50544-112">The texture wraps in both the U and V direction.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="50544-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50544-113">Requirements</span></span>



| <span data-ttu-id="50544-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="50544-114">Requirement</span></span> | <span data-ttu-id="50544-115">Valore</span><span class="sxs-lookup"><span data-stu-id="50544-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="50544-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="50544-116">Header</span></span><br/> | <dl> <span data-ttu-id="50544-117"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="50544-117"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50544-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="50544-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50544-119">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="50544-119">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="50544-120">**D3DXComputeIMTFromSignal**</span><span class="sxs-lookup"><span data-stu-id="50544-120">**D3DXComputeIMTFromSignal**</span></span>](d3dxcomputeimtfromsignal.md)
</dt> <dt>

[<span data-ttu-id="50544-121">**D3DXComputeIMTFromTexture**</span><span class="sxs-lookup"><span data-stu-id="50544-121">**D3DXComputeIMTFromTexture**</span></span>](d3dxcomputeimtfromtexture.md)
</dt> <dt>

[<span data-ttu-id="50544-122">**D3DXComputeIMTFromPerTexelSignal**</span><span class="sxs-lookup"><span data-stu-id="50544-122">**D3DXComputeIMTFromPerTexelSignal**</span></span>](d3dxcomputeimtfrompertexelsignal.md)
</dt> <dt>

[<span data-ttu-id="50544-123">**D3DXComputeIMTFromPerVertexSignal**</span><span class="sxs-lookup"><span data-stu-id="50544-123">**D3DXComputeIMTFromPerVertexSignal**</span></span>](d3dxcomputeimtfrompervertexsignal.md)
</dt> </dl>

 

 




