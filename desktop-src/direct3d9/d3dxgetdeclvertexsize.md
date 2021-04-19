---
description: Restituisce la dimensione di un vertice dalla dichiarazione del vertice.
ms.assetid: a2524f96-103e-43ab-bdcb-b99e7402fd89
title: Funzione D3DXGetDeclVertexSize (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetDeclVertexSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c962064faa61dc7045b0111c5efbf1d1bea9fd40
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322669"
---
# <a name="d3dxgetdeclvertexsize-function"></a><span data-ttu-id="c0ff8-103">D3DXGetDeclVertexSize (funzione)</span><span class="sxs-lookup"><span data-stu-id="c0ff8-103">D3DXGetDeclVertexSize function</span></span>

<span data-ttu-id="c0ff8-104">Restituisce la dimensione di un vertice dalla dichiarazione del vertice.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-104">Returns the size of a vertex from the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0ff8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c0ff8-105">Syntax</span></span>


```C++
UINT D3DXGetDeclVertexSize(
  _In_ const D3DVERTEXELEMENT9 *pDecl,
  _In_       DWORD             Stream
);
```



## <a name="parameters"></a><span data-ttu-id="c0ff8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c0ff8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0ff8-107">*pDecl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c0ff8-107">*pDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0ff8-108">Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="c0ff8-108">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="c0ff8-109">Puntatore alla dichiarazione del vertice.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-109">A pointer to the vertex declaration.</span></span> <span data-ttu-id="c0ff8-110">Vedere [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="c0ff8-110">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0ff8-111">*Flusso* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="c0ff8-111">*Stream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0ff8-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c0ff8-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c0ff8-113">Indice del flusso in base zero.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-113">The zero-based stream index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0ff8-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c0ff8-114">Return value</span></span>

<span data-ttu-id="c0ff8-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c0ff8-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c0ff8-116">Dimensioni della dichiarazione dei vertici, in byte.</span><span class="sxs-lookup"><span data-stu-id="c0ff8-116">The vertex declaration size, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0ff8-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0ff8-117">Requirements</span></span>



| <span data-ttu-id="c0ff8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0ff8-118">Requirement</span></span> | <span data-ttu-id="c0ff8-119">Valore</span><span class="sxs-lookup"><span data-stu-id="c0ff8-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0ff8-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c0ff8-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c0ff8-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0ff8-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c0ff8-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="c0ff8-122">Library</span></span><br/> | <dl> <span data-ttu-id="c0ff8-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0ff8-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c0ff8-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c0ff8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0ff8-125">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="c0ff8-125">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
