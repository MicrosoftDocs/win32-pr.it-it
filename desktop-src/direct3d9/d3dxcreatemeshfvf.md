---
description: Crea un oggetto mesh usando un codice FVF (Flexible Vertex Format).
ms.assetid: 4681f181-8a16-42d4-bbfa-bdee5ed69fd3
title: Funzione D3DXCreateMeshFVF (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateMeshFVF
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e9d5589b0f02bfcb85f9c0f0dc4dc5de69e2fb23
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323548"
---
# <a name="d3dxcreatemeshfvf-function"></a><span data-ttu-id="def8f-103">D3DXCreateMeshFVF (funzione)</span><span class="sxs-lookup"><span data-stu-id="def8f-103">D3DXCreateMeshFVF function</span></span>

<span data-ttu-id="def8f-104">Crea un oggetto mesh usando un codice FVF (Flexible Vertex Format).</span><span class="sxs-lookup"><span data-stu-id="def8f-104">Creates a mesh object using a flexible vertex format (FVF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="def8f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="def8f-105">Syntax</span></span>


```C++
HRESULT D3DXCreateMeshFVF(
  _In_  DWORD             NumFaces,
  _In_  DWORD             NumVertices,
  _In_  DWORD             Options,
  _In_  DWORD             FVF,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="def8f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="def8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="def8f-107">*NumFaces* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="def8f-107">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="def8f-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="def8f-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="def8f-109">Numero di visi per la mesh.</span><span class="sxs-lookup"><span data-stu-id="def8f-109">Number of faces for the mesh.</span></span> <span data-ttu-id="def8f-110">L'intervallo valido per questo numero è maggiore di 0 e uno minore del valore DWORD massimo, in genere 2 ³ ²-1, perché l'ultimo indice è riservato.</span><span class="sxs-lookup"><span data-stu-id="def8f-110">The valid range for this number is greater than 0, and one less than the max DWORD value, typically 2³² - 1, because the last index is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="def8f-111">*NumVertices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="def8f-111">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="def8f-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="def8f-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="def8f-113">Numero di vertici per la mesh.</span><span class="sxs-lookup"><span data-stu-id="def8f-113">Number of vertices for the mesh.</span></span> <span data-ttu-id="def8f-114">Questo parametro deve essere maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="def8f-114">This parameter must be greater than 0.</span></span>

</dd> <dt>

<span data-ttu-id="def8f-115">*Opzioni* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="def8f-115">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="def8f-116">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="def8f-116">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="def8f-117">Combinazione di uno o più flag dell'enumerazione [**D3DXMESH**](./d3dxmesh.md) , che specifica le opzioni di creazione per la mesh.</span><span class="sxs-lookup"><span data-stu-id="def8f-117">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="def8f-118">*FVF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="def8f-118">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="def8f-119">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="def8f-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="def8f-120">Combinazione di [D3DFVF](d3dfvf.md) che descrive il formato del vertice per la mesh restituita.</span><span class="sxs-lookup"><span data-stu-id="def8f-120">Combination of [D3DFVF](d3dfvf.md) that describes the vertex format for the returned mesh.</span></span> <span data-ttu-id="def8f-121">Questa funzione non supporta D3DFVF \_ XYZRHW.</span><span class="sxs-lookup"><span data-stu-id="def8f-121">This function does not support D3DFVF\_XYZRHW.</span></span>

</dd> <dt>

<span data-ttu-id="def8f-122">*pD3DDevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="def8f-122">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="def8f-123">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="def8f-123">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="def8f-124">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , l'oggetto dispositivo da associare alla mesh.</span><span class="sxs-lookup"><span data-stu-id="def8f-124">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object to be associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="def8f-125">*ppMesh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="def8f-125">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="def8f-126">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="def8f-126">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="def8f-127">Indirizzo di un puntatore a un'interfaccia [**ID3DXMesh**](id3dxmesh.md) , che rappresenta l'oggetto mesh creato.</span><span class="sxs-lookup"><span data-stu-id="def8f-127">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the created mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="def8f-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="def8f-128">Return value</span></span>

<span data-ttu-id="def8f-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="def8f-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="def8f-130">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="def8f-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="def8f-131">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="def8f-131">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="def8f-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="def8f-132">Requirements</span></span>



| <span data-ttu-id="def8f-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="def8f-133">Requirement</span></span> | <span data-ttu-id="def8f-134">Valore</span><span class="sxs-lookup"><span data-stu-id="def8f-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="def8f-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="def8f-135">Header</span></span><br/>  | <dl> <span data-ttu-id="def8f-136"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="def8f-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="def8f-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="def8f-137">Library</span></span><br/> | <dl> <span data-ttu-id="def8f-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="def8f-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="def8f-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="def8f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="def8f-140">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="def8f-140">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="def8f-141">**D3DXFVFFromDeclarator**</span><span class="sxs-lookup"><span data-stu-id="def8f-141">**D3DXFVFFromDeclarator**</span></span>](d3dxfvffromdeclarator.md)
</dt> </dl>

 

 
