---
description: Usa un sistema di coordinate a sinistra per creare una mesh contenente una sfera.
ms.assetid: d3198805-9435-4849-892d-ec98dc2221d2
title: Funzione D3DXCreateSphere (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSphere
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e56ac6b8e8cc2195e2176e505cf430ea33b6b6ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235028"
---
# <a name="d3dxcreatesphere-function"></a><span data-ttu-id="09fb9-103">D3DXCreateSphere (funzione)</span><span class="sxs-lookup"><span data-stu-id="09fb9-103">D3DXCreateSphere function</span></span>

<span data-ttu-id="09fb9-104">Usa un sistema di coordinate a sinistra per creare una mesh contenente una sfera.</span><span class="sxs-lookup"><span data-stu-id="09fb9-104">Uses a left-handed coordinate system to create a mesh containing a sphere.</span></span>

## <a name="syntax"></a><span data-ttu-id="09fb9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="09fb9-105">Syntax</span></span>


```C++
HRESULT D3DXCreateSphere(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Radius,
  _In_  UINT              Slices,
  _In_  UINT              Stacks,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="09fb9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="09fb9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09fb9-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="09fb9-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09fb9-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="09fb9-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="09fb9-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo associato alla mesh della sfera creata.</span><span class="sxs-lookup"><span data-stu-id="09fb9-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created sphere mesh.</span></span>

</dd> <dt>

<span data-ttu-id="09fb9-110">*Raggio* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="09fb9-110">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09fb9-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="09fb9-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="09fb9-112">Raggio della sfera.</span><span class="sxs-lookup"><span data-stu-id="09fb9-112">Radius of the sphere.</span></span> <span data-ttu-id="09fb9-113">Questo valore deve essere maggiore o uguale a 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="09fb9-113">This value should be greater than or equal to 0.0f.</span></span>

</dd> <dt>

<span data-ttu-id="09fb9-114">*Sezioni* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="09fb9-114">*Slices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09fb9-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="09fb9-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="09fb9-116">Numero di sezioni sull'asse principale.</span><span class="sxs-lookup"><span data-stu-id="09fb9-116">Number of slices about the main axis.</span></span>

</dd> <dt>

<span data-ttu-id="09fb9-117">*Stack* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="09fb9-117">*Stacks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09fb9-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="09fb9-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="09fb9-119">Numero di stack lungo l'asse principale.</span><span class="sxs-lookup"><span data-stu-id="09fb9-119">Number of stacks along the main axis.</span></span>

</dd> <dt>

<span data-ttu-id="09fb9-120">*ppMesh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="09fb9-120">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09fb9-121">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="09fb9-121">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="09fb9-122">Indirizzo di un puntatore alla forma di output, un'interfaccia [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="09fb9-122">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="09fb9-123">*ppAdjacency* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="09fb9-123">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09fb9-124">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="09fb9-124">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="09fb9-125">Indirizzo di un puntatore a un'interfaccia [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="09fb9-125">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="09fb9-126">Quando il metodo restituisce un risultato, questo parametro viene riempito con una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh.</span><span class="sxs-lookup"><span data-stu-id="09fb9-126">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="09fb9-127">È possibile specificare **null** .</span><span class="sxs-lookup"><span data-stu-id="09fb9-127">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09fb9-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="09fb9-128">Return value</span></span>

<span data-ttu-id="09fb9-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="09fb9-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="09fb9-130">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="09fb9-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="09fb9-131">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="09fb9-131">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="09fb9-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="09fb9-132">Remarks</span></span>

<span data-ttu-id="09fb9-133">La sfera creata è centrata sull'origine e il relativo asse è allineato all'asse z.</span><span class="sxs-lookup"><span data-stu-id="09fb9-133">The created sphere is centered at the origin, and its axis is aligned with the z-axis.</span></span>

<span data-ttu-id="09fb9-134">Questa funzione crea una mesh con l' \_ opzione di creazione gestita D3DXMESH e [D3DFVF \_ xyz \| D3DFVF \_ Normal](d3dfvf.md) Flexible Vertex Format (FVF).</span><span class="sxs-lookup"><span data-stu-id="09fb9-134">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="09fb9-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09fb9-135">Requirements</span></span>



| <span data-ttu-id="09fb9-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="09fb9-136">Requirement</span></span> | <span data-ttu-id="09fb9-137">Valore</span><span class="sxs-lookup"><span data-stu-id="09fb9-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="09fb9-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="09fb9-138">Header</span></span><br/>  | <dl> <span data-ttu-id="09fb9-139"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="09fb9-139"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="09fb9-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="09fb9-140">Library</span></span><br/> | <dl> <span data-ttu-id="09fb9-141"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="09fb9-141"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="09fb9-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09fb9-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09fb9-143">Funzioni di disegno di forme</span><span class="sxs-lookup"><span data-stu-id="09fb9-143">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
