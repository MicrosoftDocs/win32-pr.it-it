---
description: Restituisce il numero di elementi nella dichiarazione del vertice.
ms.assetid: 3ce24e59-0ec3-4d53-8bc8-8a5a7cdf53b2
title: Funzione D3DXGetDeclLength (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetDeclLength
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5576b4b86d5238d4942e09d605f695c66136799a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322671"
---
# <a name="d3dxgetdecllength-function"></a><span data-ttu-id="4d21e-103">D3DXGetDeclLength (funzione)</span><span class="sxs-lookup"><span data-stu-id="4d21e-103">D3DXGetDeclLength function</span></span>

<span data-ttu-id="4d21e-104">Restituisce il numero di elementi nella dichiarazione del vertice.</span><span class="sxs-lookup"><span data-stu-id="4d21e-104">Returns the number of elements in the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d21e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4d21e-105">Syntax</span></span>


```C++
UINT D3DXGetDeclLength(
  _In_ const D3DVERTEXELEMENT9 *pDecl
);
```



## <a name="parameters"></a><span data-ttu-id="4d21e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4d21e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d21e-107">*pDecl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d21e-107">*pDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d21e-108">Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="4d21e-108">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="4d21e-109">Puntatore alla dichiarazione del vertice.</span><span class="sxs-lookup"><span data-stu-id="4d21e-109">A pointer to the vertex declaration.</span></span> <span data-ttu-id="4d21e-110">Vedere [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="4d21e-110">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d21e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4d21e-111">Return value</span></span>

<span data-ttu-id="4d21e-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4d21e-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4d21e-113">Numero di elementi nella dichiarazione del vertice.</span><span class="sxs-lookup"><span data-stu-id="4d21e-113">The number of elements in the vertex declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d21e-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d21e-114">Requirements</span></span>



| <span data-ttu-id="4d21e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d21e-115">Requirement</span></span> | <span data-ttu-id="4d21e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="4d21e-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d21e-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4d21e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="4d21e-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d21e-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="4d21e-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="4d21e-119">Library</span></span><br/> | <dl> <span data-ttu-id="4d21e-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4d21e-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4d21e-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4d21e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d21e-122">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="4d21e-122">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
