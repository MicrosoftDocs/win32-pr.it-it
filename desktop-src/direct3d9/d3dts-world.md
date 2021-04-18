---
description: Identifica la matrice di trasformazione da impostare come matrice di trasformazione globale.
ms.assetid: 2bf7ac8a-43d8-460e-a400-3b33e96441db
title: D3DTS_WORLD macro (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTS_WORLD
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: c3c8f0ac30230a747fba34d9962791b4b331d647
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322437"
---
# <a name="d3dts_world-macro"></a><span data-ttu-id="b024c-103">\_Macro D3DTS World</span><span class="sxs-lookup"><span data-stu-id="b024c-103">D3DTS\_WORLD macro</span></span>

<span data-ttu-id="b024c-104">Identifica la matrice di trasformazione da impostare come matrice di trasformazione globale.</span><span class="sxs-lookup"><span data-stu-id="b024c-104">Identifies the transformation matrix being set as the world transformation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="b024c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b024c-105">Syntax</span></span>


```C++
D3DTRANSFORMSTATETYPE D3DTS_WORLD(void);
```



## <a name="parameters"></a><span data-ttu-id="b024c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b024c-106">Parameters</span></span>

<span data-ttu-id="b024c-107">Questa macro non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="b024c-107">This macro has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b024c-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b024c-108">Return value</span></span>

<span data-ttu-id="b024c-109">[**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) equivalente a [**D3DTS \_ WORLDMATRIX (0)**](./d3dts-worldmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="b024c-109">A [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) equivalent to [**D3DTS\_WORLDMATRIX(0)**](./d3dts-worldmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b024c-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="b024c-110">Remarks</span></span>

<span data-ttu-id="b024c-111">Questa macro viene fornita per semplificare il porting delle applicazioni esistenti a Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="b024c-111">This macro is provided to facilitate porting existing applications to Direct3D 9.</span></span>

## <a name="requirements"></a><span data-ttu-id="b024c-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b024c-112">Requirements</span></span>



| <span data-ttu-id="b024c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b024c-113">Requirement</span></span> | <span data-ttu-id="b024c-114">Valore</span><span class="sxs-lookup"><span data-stu-id="b024c-114">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b024c-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b024c-115">Header</span></span><br/> | <dl> <span data-ttu-id="b024c-116"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="b024c-116"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b024c-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b024c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b024c-118">Macro</span><span class="sxs-lookup"><span data-stu-id="b024c-118">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="b024c-119">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="b024c-119">**SetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

[<span data-ttu-id="b024c-120">**\_WORLDMATRIX D3DTS**</span><span class="sxs-lookup"><span data-stu-id="b024c-120">**D3DTS\_WORLDMATRIX**</span></span>](d3dts-worldmatrix.md)
</dt> </dl>

 

 
