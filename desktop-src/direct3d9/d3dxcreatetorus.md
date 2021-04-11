---
description: Usa un sistema di coordinate a sinistra per creare una mesh contenente un toro.
ms.assetid: 68df7650-8a87-4762-8b57-5704c419b0d7
title: Funzione D3DXCreateTorus (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTorus
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 384950ca1f00d0115135cf9ae36a2883ec5470e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235024"
---
# <a name="d3dxcreatetorus-function"></a><span data-ttu-id="cb3f9-103">D3DXCreateTorus (funzione)</span><span class="sxs-lookup"><span data-stu-id="cb3f9-103">D3DXCreateTorus function</span></span>

<span data-ttu-id="cb3f9-104">Usa un sistema di coordinate a sinistra per creare una mesh contenente un toro.</span><span class="sxs-lookup"><span data-stu-id="cb3f9-104">Uses a left-handed coordinate system to create a mesh containing a torus.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb3f9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cb3f9-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTorus(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             InnerRadius,
  _In_  FLOAT             OuterRadius,
  _In_  UINT              Sides,
  _In_  UINT              Rings,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="cb3f9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cb3f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb3f9-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cb3f9-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb3f9-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="cb3f9-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="cb3f9-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo associato alla mesh Torus creata.</span><span class="sxs-lookup"><span data-stu-id="cb3f9-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created torus mesh.</span></span>

</dd> <dt>

<span data-ttu-id="cb3f9-110">*InnerRadius* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cb3f9-110">*InnerRadius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb3f9-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cb3f9-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cb3f9-112">Raggio interno di torus.</span><span class="sxs-lookup"><span data-stu-id="cb3f9-112">Inner-radius of the torus.</span></span> <span data-ttu-id="cb3f9-113">Il valore deve essere maggiore o uguale a 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="cb3f9-113">Value should be greater than or equal to 0.0f.</span></span>

</dd> <dt>

<span data-ttu-id="cb3f9-114">*OuterRadius* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cb3f9-114">*OuterRadius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb3f9-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cb3f9-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cb3f9-116">Raggio esterno dei Toru.</span><span class="sxs-lookup"><span data-stu-id="cb3f9-116">Outer-radius of the torus.</span></span> <span data-ttu-id="cb3f9-117">Il valore deve essere maggiore o uguale a 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="cb3f9-117">Value should be greater than or equal to 0.0f.</span></span>

</dd> <dt>

<span data-ttu-id="cb3f9-118">*Lati* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cb3f9-118">*Sides* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb3f9-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cb3f9-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cb3f9-120">Numero di lati in una sezione incrociata.</span><span class="sxs-lookup"><span data-stu-id="cb3f9-120">Number of sides in a cross-section.</span></span> <span data-ttu-id="cb3f9-121">Il valore deve essere maggiore o uguale a 3.</span><span class="sxs-lookup"><span data-stu-id="cb3f9-121">Value must be greater than or equal to 3.</span></span>

</dd> <dt>

<span data-ttu-id="cb3f9-122">*Anelli* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cb3f9-122">*Rings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb3f9-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cb3f9-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cb3f9-124">Numero di anelli che compongono il toro.</span><span class="sxs-lookup"><span data-stu-id="cb3f9-124">Number of rings making up the torus.</span></span> <span data-ttu-id="cb3f9-125">Il valore deve essere maggiore o uguale a 3.</span><span class="sxs-lookup"><span data-stu-id="cb3f9-125">Value must be greater than or equal to 3.</span></span>

</dd> <dt>

<span data-ttu-id="cb3f9-126">*ppMesh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cb3f9-126">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb3f9-127">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="cb3f9-127">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="cb3f9-128">Indirizzo di un puntatore alla forma di output, un'interfaccia [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="cb3f9-128">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="cb3f9-129">*ppAdjacency* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cb3f9-129">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb3f9-130">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="cb3f9-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="cb3f9-131">Indirizzo di un puntatore a un'interfaccia [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="cb3f9-131">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="cb3f9-132">Quando il metodo restituisce un risultato, questo parametro viene riempito con una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh.</span><span class="sxs-lookup"><span data-stu-id="cb3f9-132">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="cb3f9-133">È possibile specificare **null** .</span><span class="sxs-lookup"><span data-stu-id="cb3f9-133">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb3f9-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cb3f9-134">Return value</span></span>

<span data-ttu-id="cb3f9-135">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cb3f9-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cb3f9-136">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cb3f9-136">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cb3f9-137">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="cb3f9-137">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb3f9-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="cb3f9-138">Remarks</span></span>

<span data-ttu-id="cb3f9-139">I Torus creati sono centrati sull'origine e il relativo asse è allineato all'asse z.</span><span class="sxs-lookup"><span data-stu-id="cb3f9-139">The created torus is centered at the origin, and its axis is aligned with the z-axis.</span></span> <span data-ttu-id="cb3f9-140">Il raggio interno del Toro è il raggio della sezione incrociata (raggio secondario) e il raggio esterno del Toro è il raggio del foro centrale.</span><span class="sxs-lookup"><span data-stu-id="cb3f9-140">The inner radius of the torus is the radius of the cross-section (the minor radius), and the outer radius of the torus is the radius of the central hole.</span></span>

<span data-ttu-id="cb3f9-141">Questa funzione restituisce una mesh che può essere usata in un secondo momento per il disegno o la manipolazione da parte dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cb3f9-141">This function returns a mesh that can be used later for drawing or manipulation by the application.</span></span>

<span data-ttu-id="cb3f9-142">Questa funzione crea una mesh con l' \_ opzione di creazione gestita D3DXMESH e [D3DFVF \_ xyz \| D3DFVF \_ Normal](d3dfvf.md) Flexible Vertex Format (FVF).</span><span class="sxs-lookup"><span data-stu-id="cb3f9-142">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="cb3f9-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb3f9-143">Requirements</span></span>



| <span data-ttu-id="cb3f9-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb3f9-144">Requirement</span></span> | <span data-ttu-id="cb3f9-145">Valore</span><span class="sxs-lookup"><span data-stu-id="cb3f9-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb3f9-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cb3f9-146">Header</span></span><br/>  | <dl> <span data-ttu-id="cb3f9-147"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb3f9-147"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="cb3f9-148">Libreria</span><span class="sxs-lookup"><span data-stu-id="cb3f9-148">Library</span></span><br/> | <dl> <span data-ttu-id="cb3f9-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb3f9-149"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="cb3f9-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb3f9-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb3f9-151">Funzioni di disegno di forme</span><span class="sxs-lookup"><span data-stu-id="cb3f9-151">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
