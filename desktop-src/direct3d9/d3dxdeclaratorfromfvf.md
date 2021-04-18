---
description: Restituisce un dichiaratore da un codice FVF (Flexible Vertex Format).
ms.assetid: 0272239c-0873-4a5c-b046-541f4ba603f4
title: Funzione D3DXDeclaratorFromFVF (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDeclaratorFromFVF
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: de5360c7f9bd28d4c97184f985f06e48ca0002d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322714"
---
# <a name="d3dxdeclaratorfromfvf-function"></a><span data-ttu-id="6b8a7-103">D3DXDeclaratorFromFVF (funzione)</span><span class="sxs-lookup"><span data-stu-id="6b8a7-103">D3DXDeclaratorFromFVF function</span></span>

<span data-ttu-id="6b8a7-104">Restituisce un dichiaratore da un codice FVF (Flexible Vertex Format).</span><span class="sxs-lookup"><span data-stu-id="6b8a7-104">Returns a declarator from a flexible vertex format (FVF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b8a7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6b8a7-105">Syntax</span></span>


```C++
HRESULT D3DXDeclaratorFromFVF(
  _In_    DWORD             FVF,
  _Inout_ D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a><span data-ttu-id="6b8a7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6b8a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b8a7-107">*FVF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b8a7-107">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b8a7-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b8a7-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6b8a7-109">Combinazione di [D3DFVF](d3dfvf.md) che descrive il FVF da cui generare la matrice di dichiaratori restituita.</span><span class="sxs-lookup"><span data-stu-id="6b8a7-109">Combination of [D3DFVF](d3dfvf.md) that describes the FVF from which to generate the returned declarator array.</span></span>

</dd> <dt>

<span data-ttu-id="6b8a7-110">*Dichiarazione* \[ di in uscita\]</span><span class="sxs-lookup"><span data-stu-id="6b8a7-110">*Declaration* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b8a7-111">Tipo: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="6b8a7-111">Type: **[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="6b8a7-112">Matrice di elementi [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) che descrive il formato del vertice dei vertici della mesh.</span><span class="sxs-lookup"><span data-stu-id="6b8a7-112">An array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="6b8a7-113">Il limite superiore della matrice di dichiaratori è [**Max \_ FVF \_ decl \_ size**](./max-fvf-decl-size.md).</span><span class="sxs-lookup"><span data-stu-id="6b8a7-113">The upper limit of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b8a7-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6b8a7-114">Return value</span></span>

<span data-ttu-id="6b8a7-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6b8a7-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6b8a7-116">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6b8a7-116">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6b8a7-117">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DXERR \_ INVALIDMESH.</span><span class="sxs-lookup"><span data-stu-id="6b8a7-117">If the function fails, the return value can be one of the following: D3DXERR\_INVALIDMESH.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b8a7-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b8a7-118">Requirements</span></span>



| <span data-ttu-id="6b8a7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b8a7-119">Requirement</span></span> | <span data-ttu-id="6b8a7-120">Valore</span><span class="sxs-lookup"><span data-stu-id="6b8a7-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b8a7-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6b8a7-121">Header</span></span><br/>  | <dl> <span data-ttu-id="6b8a7-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b8a7-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6b8a7-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="6b8a7-123">Library</span></span><br/> | <dl> <span data-ttu-id="6b8a7-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b8a7-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6b8a7-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b8a7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b8a7-126">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="6b8a7-126">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="6b8a7-127">**D3DXFVFFromDeclarator**</span><span class="sxs-lookup"><span data-stu-id="6b8a7-127">**D3DXFVFFromDeclarator**</span></span>](d3dxfvffromdeclarator.md)
</dt> </dl>

 

 
