---
description: Ottiene i parametri di spostamento della geometria mesh.
ms.assetid: 155724ba-71be-4e9f-8c84-bb04f8eec578
title: 'Metodo ID3DXPatchMesh:: GetDisplaceParam (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetDisplaceParam
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3ce6891af8a15aa8f4af5c85312f124db6c05321
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323721"
---
# <a name="id3dxpatchmeshgetdisplaceparam-method"></a><span data-ttu-id="b883f-103">Metodo ID3DXPatchMesh:: GetDisplaceParam</span><span class="sxs-lookup"><span data-stu-id="b883f-103">ID3DXPatchMesh::GetDisplaceParam method</span></span>

<span data-ttu-id="b883f-104">Ottiene i parametri di spostamento della geometria mesh.</span><span class="sxs-lookup"><span data-stu-id="b883f-104">Gets mesh geometry displacement parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="b883f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b883f-105">Syntax</span></span>


```C++
HRESULT GetDisplaceParam(
  [in] LPDIRECT3DBASETEXTURE9 *Texture,
  [in] D3DTEXTUREFILTERTYPE   *MinFilter,
  [in] D3DTEXTUREFILTERTYPE   *MagFilter,
  [in] D3DTEXTUREFILTERTYPE   *MipFilter,
  [in] D3DTEXTUREADDRESS      *Wrap,
  [in] DWORD                  *dwLODBias
);
```



## <a name="parameters"></a><span data-ttu-id="b883f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b883f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b883f-107">*Trama* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b883f-107">*Texture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b883f-108">Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="b883f-108">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)\***</span></span>

<span data-ttu-id="b883f-109">Trama contenente i dati di spostamento.</span><span class="sxs-lookup"><span data-stu-id="b883f-109">Texture containing the displacement data.</span></span>

</dd> <dt>

<span data-ttu-id="b883f-110">*MinFilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b883f-110">*MinFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b883f-111">Tipo: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span><span class="sxs-lookup"><span data-stu-id="b883f-111">Type: **[**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span></span>

<span data-ttu-id="b883f-112">Livello minification.</span><span class="sxs-lookup"><span data-stu-id="b883f-112">Minification level.</span></span> <span data-ttu-id="b883f-113">Per ulteriori informazioni, vedere [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="b883f-113">For more information, see [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span>

</dd> <dt>

<span data-ttu-id="b883f-114">*MagFilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b883f-114">*MagFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b883f-115">Tipo: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span><span class="sxs-lookup"><span data-stu-id="b883f-115">Type: **[**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span></span>

<span data-ttu-id="b883f-116">Livello di ingrandimento.</span><span class="sxs-lookup"><span data-stu-id="b883f-116">Magnification level.</span></span> <span data-ttu-id="b883f-117">Per ulteriori informazioni, vedere [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="b883f-117">For more information, see [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span>

</dd> <dt>

<span data-ttu-id="b883f-118">*MipFilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b883f-118">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b883f-119">Tipo: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span><span class="sxs-lookup"><span data-stu-id="b883f-119">Type: **[**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span></span>

<span data-ttu-id="b883f-120">Livello di filtro MIP.</span><span class="sxs-lookup"><span data-stu-id="b883f-120">Mip filter level.</span></span> <span data-ttu-id="b883f-121">Per ulteriori informazioni, vedere [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="b883f-121">For more information, see [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span>

</dd> <dt>

<span data-ttu-id="b883f-122">A *capo automatico* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b883f-122">*Wrap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b883f-123">Tipo: **[ **D3DTEXTUREADDRESS**](./d3dtextureaddress.md)\***</span><span class="sxs-lookup"><span data-stu-id="b883f-123">Type: **[**D3DTEXTUREADDRESS**](./d3dtextureaddress.md)\***</span></span>

<span data-ttu-id="b883f-124">Modalità di wrapping degli indirizzi della trama.</span><span class="sxs-lookup"><span data-stu-id="b883f-124">Texture address wrap mode.</span></span> <span data-ttu-id="b883f-125">Per ulteriori informazioni, vedere [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span><span class="sxs-lookup"><span data-stu-id="b883f-125">For more information, see [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span></span>

</dd> <dt>

<span data-ttu-id="b883f-126">*dwLODBias* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b883f-126">*dwLODBias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b883f-127">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b883f-127">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b883f-128">Livello del valore di distorsione del dettaglio.</span><span class="sxs-lookup"><span data-stu-id="b883f-128">Level of detail bias value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b883f-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b883f-129">Return value</span></span>

<span data-ttu-id="b883f-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b883f-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b883f-131">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b883f-131">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b883f-132">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="b883f-132">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="b883f-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="b883f-133">Remarks</span></span>

<span data-ttu-id="b883f-134">Le mappe di spostamento possono essere solo trame 2D.</span><span class="sxs-lookup"><span data-stu-id="b883f-134">Displacement maps can only be 2D textures.</span></span> <span data-ttu-id="b883f-135">Mapping MIP viene ignorato per lo schema a mosaico non adattivo.</span><span class="sxs-lookup"><span data-stu-id="b883f-135">Mipmapping is ignored for nonadaptive tessellation.</span></span>

## <a name="requirements"></a><span data-ttu-id="b883f-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b883f-136">Requirements</span></span>



| <span data-ttu-id="b883f-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="b883f-137">Requirement</span></span> | <span data-ttu-id="b883f-138">Valore</span><span class="sxs-lookup"><span data-stu-id="b883f-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b883f-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b883f-139">Header</span></span><br/>  | <dl> <span data-ttu-id="b883f-140"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b883f-140"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b883f-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="b883f-141">Library</span></span><br/> | <dl> <span data-ttu-id="b883f-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b883f-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b883f-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b883f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b883f-144">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="b883f-144">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
