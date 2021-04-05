---
description: Usa un sistema di coordinate a sinistra per creare una mesh contenente un poligono a n lati.
ms.assetid: f3313f55-3e60-4440-8bea-d2886b636c9a
title: Funzione D3DXCreatePolygon (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePolygon
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 94a7e48f512d25ca53d1f3ff80889a013e2ecdcb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058610"
---
# <a name="d3dxcreatepolygon-function"></a><span data-ttu-id="cd528-103">D3DXCreatePolygon (funzione)</span><span class="sxs-lookup"><span data-stu-id="cd528-103">D3DXCreatePolygon function</span></span>

<span data-ttu-id="cd528-104">Usa un sistema di coordinate a sinistra per creare una mesh contenente un poligono a n lati.</span><span class="sxs-lookup"><span data-stu-id="cd528-104">Uses a left-handed coordinate system to create a mesh containing an n-sided polygon.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd528-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cd528-105">Syntax</span></span>


```C++
HRESULT D3DXCreatePolygon(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Length,
  _In_  UINT              Sides,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="cd528-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cd528-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd528-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd528-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd528-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="cd528-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="cd528-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo associato alla mesh poligonale creata.</span><span class="sxs-lookup"><span data-stu-id="cd528-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created polygon mesh.</span></span>

</dd> <dt>

<span data-ttu-id="cd528-110">*Lunghezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd528-110">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd528-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cd528-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cd528-112">Lunghezza di ogni lato.</span><span class="sxs-lookup"><span data-stu-id="cd528-112">Length of each side.</span></span>

</dd> <dt>

<span data-ttu-id="cd528-113">*Lati* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd528-113">*Sides* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd528-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cd528-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cd528-115">Numero di lati del poligono.</span><span class="sxs-lookup"><span data-stu-id="cd528-115">Number of sides for the polygon.</span></span> <span data-ttu-id="cd528-116">Il valore deve essere maggiore o uguale a 3.</span><span class="sxs-lookup"><span data-stu-id="cd528-116">Value must be greater than or equal to 3.</span></span>

</dd> <dt>

<span data-ttu-id="cd528-117">*ppMesh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cd528-117">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd528-118">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="cd528-118">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="cd528-119">Indirizzo di un puntatore alla forma di output, un'interfaccia [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="cd528-119">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="cd528-120">*ppAdjacency* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cd528-120">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd528-121">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="cd528-121">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="cd528-122">Indirizzo di un puntatore a un'interfaccia [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="cd528-122">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="cd528-123">Quando il metodo restituisce un risultato, questo parametro viene riempito con una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh.</span><span class="sxs-lookup"><span data-stu-id="cd528-123">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="cd528-124">È possibile specificare **null** .</span><span class="sxs-lookup"><span data-stu-id="cd528-124">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd528-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cd528-125">Return value</span></span>

<span data-ttu-id="cd528-126">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cd528-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cd528-127">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cd528-127">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cd528-128">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="cd528-128">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd528-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="cd528-129">Remarks</span></span>

<span data-ttu-id="cd528-130">Il poligono creato è centrato all'origine.</span><span class="sxs-lookup"><span data-stu-id="cd528-130">The created polygon is centered at the origin.</span></span>

<span data-ttu-id="cd528-131">Questa funzione crea una mesh con l' \_ opzione di creazione gestita D3DXMESH e [D3DFVF \_ xyz \| D3DFVF \_ Normal](d3dfvf.md) Flexible Vertex Format (FVF).</span><span class="sxs-lookup"><span data-stu-id="cd528-131">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd528-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd528-132">Requirements</span></span>



| <span data-ttu-id="cd528-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd528-133">Requirement</span></span> | <span data-ttu-id="cd528-134">Valore</span><span class="sxs-lookup"><span data-stu-id="cd528-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd528-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cd528-135">Header</span></span><br/>  | <dl> <span data-ttu-id="cd528-136"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd528-136"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="cd528-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="cd528-137">Library</span></span><br/> | <dl> <span data-ttu-id="cd528-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd528-138"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="cd528-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd528-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd528-140">Funzioni di disegno di forme</span><span class="sxs-lookup"><span data-stu-id="cd528-140">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
