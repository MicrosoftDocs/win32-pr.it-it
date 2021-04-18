---
description: Usa un sistema di coordinate a sinistra per creare una mesh contenente una casella allineata asse.
ms.assetid: 396ef0f7-65d5-46f9-9b97-e6471f2fb5fe
title: Funzione D3DXCreateBox (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateBox
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 187c389dd2d90b4457237540026a63edc4ab4f4c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322391"
---
# <a name="d3dxcreatebox-function"></a><span data-ttu-id="65608-103">D3DXCreateBox (funzione)</span><span class="sxs-lookup"><span data-stu-id="65608-103">D3DXCreateBox function</span></span>

<span data-ttu-id="65608-104">Usa un sistema di coordinate a sinistra per creare una mesh contenente una casella allineata asse.</span><span class="sxs-lookup"><span data-stu-id="65608-104">Uses a left-handed coordinate system to create a mesh containing an axis-aligned box.</span></span>

## <a name="syntax"></a><span data-ttu-id="65608-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="65608-105">Syntax</span></span>


```C++
HRESULT D3DXCreateBox(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Width,
  _In_  FLOAT             Height,
  _In_  FLOAT             Depth,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="65608-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="65608-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65608-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65608-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65608-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="65608-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="65608-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo associato alla Mesh Box creata.</span><span class="sxs-lookup"><span data-stu-id="65608-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created box mesh.</span></span>

</dd> <dt>

<span data-ttu-id="65608-110">*Larghezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65608-110">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65608-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65608-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="65608-112">Larghezza della casella lungo l'asse x.</span><span class="sxs-lookup"><span data-stu-id="65608-112">Width of the box, along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="65608-113">*Altezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65608-113">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65608-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65608-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="65608-115">Altezza della casella lungo l'asse y.</span><span class="sxs-lookup"><span data-stu-id="65608-115">Height of the box, along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="65608-116">*Profondità* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65608-116">*Depth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65608-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65608-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="65608-118">Profondità della casella lungo l'asse z.</span><span class="sxs-lookup"><span data-stu-id="65608-118">Depth of the box, along the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="65608-119">*ppMesh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="65608-119">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65608-120">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="65608-120">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="65608-121">Indirizzo di un puntatore alla forma di output, un'interfaccia [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="65608-121">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="65608-122">*ppAdjacency* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="65608-122">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65608-123">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="65608-123">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="65608-124">Indirizzo di un puntatore a un'interfaccia [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="65608-124">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="65608-125">Quando il metodo restituisce un risultato, questo parametro viene riempito con una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh.</span><span class="sxs-lookup"><span data-stu-id="65608-125">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="65608-126">È possibile specificare **null** .</span><span class="sxs-lookup"><span data-stu-id="65608-126">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65608-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="65608-127">Return value</span></span>

<span data-ttu-id="65608-128">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="65608-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="65608-129">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="65608-129">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="65608-130">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="65608-130">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="65608-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="65608-131">Remarks</span></span>

<span data-ttu-id="65608-132">La casella creata è centrata all'origine.</span><span class="sxs-lookup"><span data-stu-id="65608-132">The created box is centered at the origin.</span></span>

<span data-ttu-id="65608-133">Questa funzione crea una mesh con l' \_ opzione di creazione gestita D3DXMESH e [D3DFVF \_ xyz \| D3DFVF \_ Normal](d3dfvf.md) Flexible Vertex Format (FVF).</span><span class="sxs-lookup"><span data-stu-id="65608-133">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="65608-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="65608-134">Requirements</span></span>



| <span data-ttu-id="65608-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="65608-135">Requirement</span></span> | <span data-ttu-id="65608-136">Valore</span><span class="sxs-lookup"><span data-stu-id="65608-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65608-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="65608-137">Header</span></span><br/>  | <dl> <span data-ttu-id="65608-138"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="65608-138"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="65608-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="65608-139">Library</span></span><br/> | <dl> <span data-ttu-id="65608-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65608-140"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="65608-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="65608-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65608-142">Funzioni di disegno di forme</span><span class="sxs-lookup"><span data-stu-id="65608-142">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
