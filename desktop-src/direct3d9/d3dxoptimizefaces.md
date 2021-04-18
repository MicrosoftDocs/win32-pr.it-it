---
description: Genera un nuovo mapping del volto ottimizzato per un elenco di triangolo.
ms.assetid: 428c2af8-43e7-4cf7-8b9b-04ba5cff82c8
title: Funzione D3DXOptimizeFaces (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXOptimizeFaces
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6c56dec04e01b542d2c760852a58826a8186c213
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322119"
---
# <a name="d3dxoptimizefaces-function"></a><span data-ttu-id="2611b-103">D3DXOptimizeFaces (funzione)</span><span class="sxs-lookup"><span data-stu-id="2611b-103">D3DXOptimizeFaces function</span></span>

<span data-ttu-id="2611b-104">Genera un nuovo mapping del volto ottimizzato per un elenco di triangolo.</span><span class="sxs-lookup"><span data-stu-id="2611b-104">Generates an optimized face remapping for a triangle list.</span></span>

## <a name="syntax"></a><span data-ttu-id="2611b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2611b-105">Syntax</span></span>


```C++
HRESULT D3DXOptimizeFaces(
  _In_    LPCVOID pIndices,
  _In_    UINT    NumFaces,
  _In_    UINT    NumVertices,
  _In_    BOOL    Indices32Bit,
  _Inout_ DWORD   *pFaceRemap
);
```



## <a name="parameters"></a><span data-ttu-id="2611b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2611b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2611b-107">*pIndices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2611b-107">*pIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2611b-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2611b-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2611b-109">Puntatore agli indici di elenco di triangolo da usare per l'ordinamento dei vertici.</span><span class="sxs-lookup"><span data-stu-id="2611b-109">Pointer to triangle list indices to use for ordering vertices.</span></span>

</dd> <dt>

<span data-ttu-id="2611b-110">*NumFaces* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2611b-110">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2611b-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2611b-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2611b-112">Numero di visi nell'elenco dei triangoli.</span><span class="sxs-lookup"><span data-stu-id="2611b-112">Number of faces in the triangle list.</span></span> <span data-ttu-id="2611b-113">Per le mesh a 16 bit, questo limite è di 2 ^ 16-1 (65535) o di un numero inferiore di visi.</span><span class="sxs-lookup"><span data-stu-id="2611b-113">For 16-bit meshes, this is limited to 2^16 - 1 (65535) or fewer faces.</span></span>

</dd> <dt>

<span data-ttu-id="2611b-114">*NumVertices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2611b-114">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2611b-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2611b-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2611b-116">Numero di vertici a cui fa riferimento l'elenco dei triangoli.</span><span class="sxs-lookup"><span data-stu-id="2611b-116">Number of vertices referenced by the triangle list.</span></span>

</dd> <dt>

<span data-ttu-id="2611b-117">*Indices32Bit* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2611b-117">*Indices32Bit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2611b-118">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2611b-118">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2611b-119">Flag che indica il tipo di indice: **true** se gli indici sono a 32 bit (più di 65535 indici); **false** se gli indici sono a 16 bit (65535 o un numero inferiore di indici).</span><span class="sxs-lookup"><span data-stu-id="2611b-119">Flag indicating index type: **TRUE** if indices are 32-bit (more than 65535 indices), **FALSE** if indices are 16-bit (65535 or fewer indices).</span></span>

</dd> <dt>

<span data-ttu-id="2611b-120">*pFaceRemap* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="2611b-120">*pFaceRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2611b-121">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2611b-121">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2611b-122">Puntatore al quadrante mesh originale diviso per generare la faccia corrente.</span><span class="sxs-lookup"><span data-stu-id="2611b-122">Pointer to the original mesh face that was split to generate the current face.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2611b-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2611b-123">Return value</span></span>

<span data-ttu-id="2611b-124">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2611b-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2611b-125">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2611b-125">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2611b-126">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="2611b-126">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="2611b-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="2611b-127">Remarks</span></span>

<span data-ttu-id="2611b-128">La procedura di ottimizzazione di questa funzione è equivalente dal punto di vista funzionale alla chiamata a [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) con il \_ flag D3DXMESHOPT DEVICEINDEPENDENT, ma questa funzione consente un uso più efficiente delle cache dei vertici.</span><span class="sxs-lookup"><span data-stu-id="2611b-128">This function's optimization procedure is functionally equivalent to calling [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) with the D3DXMESHOPT\_DEVICEINDEPENDENT flag, but this function makes more efficient use of vertex caches.</span></span>

## <a name="requirements"></a><span data-ttu-id="2611b-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2611b-129">Requirements</span></span>



| <span data-ttu-id="2611b-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2611b-130">Requirement</span></span> | <span data-ttu-id="2611b-131">Valore</span><span class="sxs-lookup"><span data-stu-id="2611b-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2611b-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2611b-132">Header</span></span><br/>  | <dl> <span data-ttu-id="2611b-133"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="2611b-133"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="2611b-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="2611b-134">Library</span></span><br/> | <dl> <span data-ttu-id="2611b-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2611b-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2611b-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2611b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2611b-137">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="2611b-137">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
