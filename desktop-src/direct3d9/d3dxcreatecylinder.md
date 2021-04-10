---
description: Usa un sistema di coordinate a sinistra per creare una mesh contenente un cilindro.
ms.assetid: 54b8a59e-d13f-44cb-84c0-f63c7b1ffb1b
title: Funzione D3DXCreateCylinder (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCylinder
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ec97755d45b21a85e1a73bbcd2214ee4c1e2358f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762089"
---
# <a name="d3dxcreatecylinder-function"></a><span data-ttu-id="b5531-103">D3DXCreateCylinder (funzione)</span><span class="sxs-lookup"><span data-stu-id="b5531-103">D3DXCreateCylinder function</span></span>

<span data-ttu-id="b5531-104">Usa un sistema di coordinate a sinistra per creare una mesh contenente un cilindro.</span><span class="sxs-lookup"><span data-stu-id="b5531-104">Uses a left-handed coordinate system to create a mesh containing a cylinder.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5531-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5531-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCylinder(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Radius1,
  _In_  FLOAT             Radius2,
  _In_  FLOAT             Length,
  _In_  UINT              Slices,
  _In_  UINT              Stacks,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="b5531-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5531-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5531-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5531-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5531-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="b5531-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="b5531-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo associato alla mesh a cilindri creata.</span><span class="sxs-lookup"><span data-stu-id="b5531-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created cylinder mesh.</span></span>

</dd> <dt>

<span data-ttu-id="b5531-110">*Radius1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5531-110">*Radius1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5531-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b5531-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b5531-112">Raggio all'estremità Z negativa.</span><span class="sxs-lookup"><span data-stu-id="b5531-112">Radius at the negative Z end.</span></span> <span data-ttu-id="b5531-113">Il valore deve essere maggiore o uguale a 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="b5531-113">Value should be greater than or equal to 0.0f.</span></span>

</dd> <dt>

<span data-ttu-id="b5531-114">*Radius2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5531-114">*Radius2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5531-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b5531-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b5531-116">Raggio al termine Z positivo.</span><span class="sxs-lookup"><span data-stu-id="b5531-116">Radius at the positive Z end.</span></span> <span data-ttu-id="b5531-117">Il valore deve essere maggiore o uguale a 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="b5531-117">Value should be greater than or equal to 0.0f.</span></span>

</dd> <dt>

<span data-ttu-id="b5531-118">*Lunghezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5531-118">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5531-119">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b5531-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b5531-120">Lunghezza del cilindro lungo l'asse z.</span><span class="sxs-lookup"><span data-stu-id="b5531-120">Length of the cylinder along the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="b5531-121">*Sezioni* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5531-121">*Slices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5531-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b5531-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b5531-123">Numero di sezioni sull'asse principale.</span><span class="sxs-lookup"><span data-stu-id="b5531-123">Number of slices about the main axis.</span></span>

</dd> <dt>

<span data-ttu-id="b5531-124">*Stack* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5531-124">*Stacks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5531-125">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b5531-125">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b5531-126">Numero di stack lungo l'asse principale.</span><span class="sxs-lookup"><span data-stu-id="b5531-126">Number of stacks along the main axis.</span></span>

</dd> <dt>

<span data-ttu-id="b5531-127">*ppMesh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b5531-127">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5531-128">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="b5531-128">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="b5531-129">Indirizzo di un puntatore alla forma di output, un'interfaccia [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="b5531-129">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="b5531-130">*ppAdjacency* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b5531-130">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5531-131">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="b5531-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="b5531-132">Indirizzo di un puntatore a un'interfaccia [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="b5531-132">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="b5531-133">Quando il metodo restituisce un risultato, questo parametro viene riempito con una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh.</span><span class="sxs-lookup"><span data-stu-id="b5531-133">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="b5531-134">È possibile specificare **null** .</span><span class="sxs-lookup"><span data-stu-id="b5531-134">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5531-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5531-135">Return value</span></span>

<span data-ttu-id="b5531-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b5531-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b5531-137">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b5531-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b5531-138">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="b5531-138">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5531-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="b5531-139">Remarks</span></span>

<span data-ttu-id="b5531-140">Il cilindro creato è centrato sull'origine e il relativo asse è allineato all'asse z.</span><span class="sxs-lookup"><span data-stu-id="b5531-140">The created cylinder is centered at the origin, and its axis is aligned with the z-axis.</span></span>

<span data-ttu-id="b5531-141">Questa funzione crea una mesh con l' \_ opzione di creazione gestita D3DXMESH e [D3DFVF \_ xyz \| D3DFVF \_ Normal](d3dfvf.md) Flexible Vertex Format (FVF).</span><span class="sxs-lookup"><span data-stu-id="b5531-141">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5531-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5531-142">Requirements</span></span>



| <span data-ttu-id="b5531-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5531-143">Requirement</span></span> | <span data-ttu-id="b5531-144">Valore</span><span class="sxs-lookup"><span data-stu-id="b5531-144">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5531-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b5531-145">Header</span></span><br/>  | <dl> <span data-ttu-id="b5531-146"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5531-146"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="b5531-147">Libreria</span><span class="sxs-lookup"><span data-stu-id="b5531-147">Library</span></span><br/> | <dl> <span data-ttu-id="b5531-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5531-148"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="b5531-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5531-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5531-150">Funzioni di disegno di forme</span><span class="sxs-lookup"><span data-stu-id="b5531-150">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
