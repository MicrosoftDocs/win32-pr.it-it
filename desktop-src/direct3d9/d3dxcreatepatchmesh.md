---
description: Crea una mesh da una mesh di patch di controllo.
ms.assetid: 50e4f7aa-a6b8-4a2b-9813-a9448f408d06
title: Funzione D3DXCreatePatchMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 375052e240973f56af32825f74caccf6f9411d75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355859"
---
# <a name="d3dxcreatepatchmesh-function"></a><span data-ttu-id="1bc4c-103">D3DXCreatePatchMesh (funzione)</span><span class="sxs-lookup"><span data-stu-id="1bc4c-103">D3DXCreatePatchMesh function</span></span>

<span data-ttu-id="1bc4c-104">Crea una mesh da una mesh di patch di controllo.</span><span class="sxs-lookup"><span data-stu-id="1bc4c-104">Creates a mesh from a control-patch mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bc4c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1bc4c-105">Syntax</span></span>


```C++
HRESULT D3DXCreatePatchMesh(
  _In_  const D3DXPATCHINFO     *pInfo,
  _In_        DWORD             dwNumPatches,
  _In_        DWORD             dwNumVertices,
  _In_        DWORD             dwOptions,
  _In_  const D3DVERTEXELEMENT9 *pDecl,
  _In_        LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_       LPD3DXPATCHMESH   *pPatchMesh
);
```



## <a name="parameters"></a><span data-ttu-id="1bc4c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1bc4c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bc4c-107">*pInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1bc4c-107">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bc4c-108">Tipo: **const [**D3DXPATCHINFO**](d3dxpatchinfo.md) \***</span><span class="sxs-lookup"><span data-stu-id="1bc4c-108">Type: **const [**D3DXPATCHINFO**](d3dxpatchinfo.md)\***</span></span>

<span data-ttu-id="1bc4c-109">Struttura delle informazioni sulla patch.</span><span class="sxs-lookup"><span data-stu-id="1bc4c-109">Patch information structure.</span></span> <span data-ttu-id="1bc4c-110">Per ulteriori informazioni, vedere [**D3DXPATCHINFO**](d3dxpatchinfo.md).</span><span class="sxs-lookup"><span data-stu-id="1bc4c-110">For more information, see [**D3DXPATCHINFO**](d3dxpatchinfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="1bc4c-111">*dwNumPatches* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1bc4c-111">*dwNumPatches* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bc4c-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1bc4c-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1bc4c-113">Numero di patch.</span><span class="sxs-lookup"><span data-stu-id="1bc4c-113">Number of patches.</span></span>

</dd> <dt>

<span data-ttu-id="1bc4c-114">*dwNumVertices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1bc4c-114">*dwNumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bc4c-115">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1bc4c-115">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1bc4c-116">Numero di vertici di controllo nella patch.</span><span class="sxs-lookup"><span data-stu-id="1bc4c-116">Number of control vertices in the patch.</span></span>

</dd> <dt>

<span data-ttu-id="1bc4c-117">*dwOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1bc4c-117">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bc4c-118">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1bc4c-118">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1bc4c-119">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="1bc4c-119">Unused.</span></span> <span data-ttu-id="1bc4c-120">Riservato per un uso successivo.</span><span class="sxs-lookup"><span data-stu-id="1bc4c-120">Reserved for later use.</span></span>

</dd> <dt>

<span data-ttu-id="1bc4c-121">*pDecl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1bc4c-121">*pDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bc4c-122">Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="1bc4c-122">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="1bc4c-123">Matrice di elementi [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , che descrive il formato del vertice per la mesh restituita.</span><span class="sxs-lookup"><span data-stu-id="1bc4c-123">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the vertex format for the returned mesh.</span></span>

</dd> <dt>

<span data-ttu-id="1bc4c-124">*pD3DDevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1bc4c-124">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bc4c-125">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="1bc4c-125">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="1bc4c-126">Puntatore al dispositivo che crea la mesh della patch.</span><span class="sxs-lookup"><span data-stu-id="1bc4c-126">Pointer the device that creates the patch mesh.</span></span> <span data-ttu-id="1bc4c-127">Vedere [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="1bc4c-127">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="1bc4c-128">*pPatchMesh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1bc4c-128">*pPatchMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1bc4c-129">Tipo: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="1bc4c-129">Type: **[**LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span></span>

<span data-ttu-id="1bc4c-130">Puntatore all'oggetto [**ID3DXPatchMesh**](id3dxpatchmesh.md) creato.</span><span class="sxs-lookup"><span data-stu-id="1bc4c-130">Pointer to the [**ID3DXPatchMesh**](id3dxpatchmesh.md) object that is created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bc4c-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1bc4c-131">Return value</span></span>

<span data-ttu-id="1bc4c-132">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1bc4c-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1bc4c-133">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1bc4c-133">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1bc4c-134">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="1bc4c-134">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="1bc4c-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="1bc4c-135">Remarks</span></span>

<span data-ttu-id="1bc4c-136">Questo metodo accetta una mesh patch di input e la converte in una rete tassellati.</span><span class="sxs-lookup"><span data-stu-id="1bc4c-136">This method takes an input patch mesh and converts it to a tessellated mesh.</span></span> <span data-ttu-id="1bc4c-137">Le mesh di patch utilizzano buffer di indice a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="1bc4c-137">Patch meshes use 16-bit index buffers.</span></span> <span data-ttu-id="1bc4c-138">Pertanto, gli indici per [**LockIndexBuffer**](id3dxpatchmesh--lockindexbuffer.md) sono a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="1bc4c-138">Therefore, indices to [**LockIndexBuffer**](id3dxpatchmesh--lockindexbuffer.md) are 16 bits.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bc4c-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1bc4c-139">Requirements</span></span>



| <span data-ttu-id="1bc4c-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bc4c-140">Requirement</span></span> | <span data-ttu-id="1bc4c-141">Valore</span><span class="sxs-lookup"><span data-stu-id="1bc4c-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1bc4c-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1bc4c-142">Header</span></span><br/>  | <dl> <span data-ttu-id="1bc4c-143"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bc4c-143"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1bc4c-144">Libreria</span><span class="sxs-lookup"><span data-stu-id="1bc4c-144">Library</span></span><br/> | <dl> <span data-ttu-id="1bc4c-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1bc4c-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1bc4c-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1bc4c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bc4c-147">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="1bc4c-147">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="1bc4c-148">**D3DXPATCHINFO**</span><span class="sxs-lookup"><span data-stu-id="1bc4c-148">**D3DXPATCHINFO**</span></span>](d3dxpatchinfo.md)
</dt> </dl>

 

 
