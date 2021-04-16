---
description: Esegue il mapping degli indici nell'intervallo compreso tra 0 e 255 e gli Stati di trasformazione corrispondenti.
ms.assetid: b0a1548c-de5d-4eff-baf9-4aecb5e13443
title: D3DTS_WORLDMATRIX macro (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTS_WORLDMATRIX
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: f80996a37e2fb48bf8ca7ea73f714b04e711b263
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530876"
---
# <a name="d3dts_worldmatrix-macro"></a><span data-ttu-id="ce285-103">D3DTS \_ WORLDMATRIX-macro</span><span class="sxs-lookup"><span data-stu-id="ce285-103">D3DTS\_WORLDMATRIX macro</span></span>

<span data-ttu-id="ce285-104">Esegue il mapping degli indici nell'intervallo compreso tra 0 e 255 e gli Stati di trasformazione corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="ce285-104">Maps indices in the range 0 through 255 to the corresponding transform states.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce285-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ce285-105">Syntax</span></span>


```C++
D3DTRANSFORMSTATETYPE D3DTS_WORLDMATRIX(
   int index
);
```



## <a name="parameters"></a><span data-ttu-id="ce285-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ce285-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce285-107">*index*</span><span class="sxs-lookup"><span data-stu-id="ce285-107">*index*</span></span> 
</dt> <dd>

<span data-ttu-id="ce285-108">Valore di indice compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="ce285-108">An index value in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce285-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ce285-109">Return value</span></span>

<span data-ttu-id="ce285-110">[**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) che esegue il mapping all' *Indice* specificato.</span><span class="sxs-lookup"><span data-stu-id="ce285-110">The [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) that maps to the given *index*.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce285-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce285-111">Remarks</span></span>

<span data-ttu-id="ce285-112">Gli Stati di trasformazione nell'intervallo compreso tra 256 e 511 sono riservati per archiviare fino a 256 matrici che possono essere indicizzate tramite indici a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="ce285-112">Transform states in the range 256 through 511 are reserved to store up to 256 matrices that can be indexed using 8-bit indices.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce285-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce285-113">Requirements</span></span>



| <span data-ttu-id="ce285-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce285-114">Requirement</span></span> | <span data-ttu-id="ce285-115">Valore</span><span class="sxs-lookup"><span data-stu-id="ce285-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce285-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ce285-116">Header</span></span><br/> | <dl> <span data-ttu-id="ce285-117"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce285-117"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce285-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce285-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce285-119">Macro</span><span class="sxs-lookup"><span data-stu-id="ce285-119">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="ce285-120">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="ce285-120">**SetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> </dl>

 

 
