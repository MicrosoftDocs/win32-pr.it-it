---
description: Copia i valori di albedo per vertice da una mesh.
ms.assetid: 3a6f1cc2-a870-4463-98df-599d9fbd9d78
title: 'Metodo ID3DXPRTEngine:: ExtractPerVertexAlbedo (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ExtractPerVertexAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ed23b75b3113421b6242f49416e4b54bfce336f4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969488"
---
# <a name="id3dxprtengineextractpervertexalbedo-method"></a><span data-ttu-id="3c9cb-103">Metodo ID3DXPRTEngine:: ExtractPerVertexAlbedo</span><span class="sxs-lookup"><span data-stu-id="3c9cb-103">ID3DXPRTEngine::ExtractPerVertexAlbedo method</span></span>

<span data-ttu-id="3c9cb-104">Copia i valori di albedo per vertice da una mesh.</span><span class="sxs-lookup"><span data-stu-id="3c9cb-104">Copies per-vertex albedo values from a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c9cb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c9cb-105">Syntax</span></span>


```C++
HRESULT ExtractPerVertexAlbedo(
  [in] LPD3DXMESH   pMesh,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         NumChanIn
);
```



## <a name="parameters"></a><span data-ttu-id="3c9cb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c9cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c9cb-107">*pMesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c9cb-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c9cb-108">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="3c9cb-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="3c9cb-109">Puntatore all'oggetto mesh [**ID3DXMesh**](id3dxmesh.md) usato in [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) per creare l'oggetto [**ID3DXPRTEngine**](id3dxprtengine.md) .</span><span class="sxs-lookup"><span data-stu-id="3c9cb-109">Pointer to the [**ID3DXMesh**](id3dxmesh.md) mesh object used in [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) to create the [**ID3DXPRTEngine**](id3dxprtengine.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="3c9cb-110">*Utilizzo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="3c9cb-110">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c9cb-111">Tipo: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**</span><span class="sxs-lookup"><span data-stu-id="3c9cb-111">Type: **[**D3DDECLUSAGE**](./d3ddeclusage.md)**</span></span>

<span data-ttu-id="3c9cb-112">Descrizioni dell'utilizzo dei vertici da copiare dalla mesh.</span><span class="sxs-lookup"><span data-stu-id="3c9cb-112">Vertex usage descriptions to copy from the mesh.</span></span> <span data-ttu-id="3c9cb-113">Vedere [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="3c9cb-113">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="3c9cb-114">*NumChanIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c9cb-114">*NumChanIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c9cb-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3c9cb-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3c9cb-116">Numero di canali dei colori da copiare dalla mesh.</span><span class="sxs-lookup"><span data-stu-id="3c9cb-116">Number of color channels to copy from the mesh.</span></span> <span data-ttu-id="3c9cb-117">Impostare su 1 per specificare i materiali grigi (R = G = B) o 3 per abilitare gli effetti di emorragia del colore.</span><span class="sxs-lookup"><span data-stu-id="3c9cb-117">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c9cb-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3c9cb-118">Return value</span></span>

<span data-ttu-id="3c9cb-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3c9cb-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3c9cb-120">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3c9cb-120">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="3c9cb-121">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="3c9cb-121">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c9cb-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c9cb-122">Requirements</span></span>



| <span data-ttu-id="3c9cb-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c9cb-123">Requirement</span></span> | <span data-ttu-id="3c9cb-124">Valore</span><span class="sxs-lookup"><span data-stu-id="3c9cb-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c9cb-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3c9cb-125">Header</span></span><br/>  | <dl> <span data-ttu-id="3c9cb-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c9cb-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3c9cb-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="3c9cb-127">Library</span></span><br/> | <dl> <span data-ttu-id="3c9cb-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c9cb-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3c9cb-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c9cb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c9cb-130">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="3c9cb-130">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
