---
description: Estrae i coefficienti di proiezione del componente principale per campione (PCA) da un buffer di dati compresso ID3DXPRTCompBuffer e aggiunge i dati a un oggetto ID3DXMesh.
ms.assetid: 0680d626-f07a-43d3-acb9-e8db82b5e933
title: 'Metodo ID3DXPRTCompBuffer:: ExtractToMesh (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractToMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 607b583b89358d2d28030a4187b1608174d849c0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322321"
---
# <a name="id3dxprtcompbufferextracttomesh-method"></a><span data-ttu-id="89415-103">Metodo ID3DXPRTCompBuffer:: ExtractToMesh</span><span class="sxs-lookup"><span data-stu-id="89415-103">ID3DXPRTCompBuffer::ExtractToMesh method</span></span>

<span data-ttu-id="89415-104">Estrae i coefficienti di proiezione del componente principale per campione (PCA) da un buffer di dati compresso [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) e aggiunge i dati a un oggetto [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="89415-104">Extracts the per-sample principal component analysis (PCA) projection coefficients from an [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) compressed data buffer and adds the data to an [**ID3DXMesh**](id3dxmesh.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="89415-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89415-105">Syntax</span></span>


```C++
HRESULT ExtractToMesh(
  [in] UINT         NumPCA,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         UsageIndexStart,
  [in] LPD3DXMESH   pScene
);
```



## <a name="parameters"></a><span data-ttu-id="89415-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="89415-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89415-107">*NumPCA* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89415-107">*NumPCA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89415-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="89415-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="89415-109">Numero di coefficienti PCA da estrarre dal buffer.</span><span class="sxs-lookup"><span data-stu-id="89415-109">Number of PCA coefficients to extract from the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="89415-110">*Utilizzo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="89415-110">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89415-111">Tipo: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**</span><span class="sxs-lookup"><span data-stu-id="89415-111">Type: **[**D3DDECLUSAGE**](./d3ddeclusage.md)**</span></span>

<span data-ttu-id="89415-112">Descrizioni dell'utilizzo dei vertici della mesh.</span><span class="sxs-lookup"><span data-stu-id="89415-112">Vertex usage descriptions of the mesh.</span></span> <span data-ttu-id="89415-113">Vedere [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="89415-113">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="89415-114">*UsageIndexStart* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89415-114">*UsageIndexStart* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89415-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="89415-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="89415-116">Indice iniziale per i coefficienti PCA da archiviare nella rete mesh.</span><span class="sxs-lookup"><span data-stu-id="89415-116">Starting index for PCA coefficients to be stored in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="89415-117">*pScene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89415-117">*pScene* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89415-118">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="89415-118">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="89415-119">Puntatore a un oggetto mesh [**ID3DXMesh**](id3dxmesh.md) in cui vengono archiviati i coefficienti PCA.</span><span class="sxs-lookup"><span data-stu-id="89415-119">Pointer to an [**ID3DXMesh**](id3dxmesh.md) mesh object that will store PCA coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89415-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="89415-120">Return value</span></span>

<span data-ttu-id="89415-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="89415-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="89415-122">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="89415-122">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="89415-123">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="89415-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="89415-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89415-124">Requirements</span></span>



| <span data-ttu-id="89415-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="89415-125">Requirement</span></span> | <span data-ttu-id="89415-126">Valore</span><span class="sxs-lookup"><span data-stu-id="89415-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="89415-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="89415-127">Header</span></span><br/>  | <dl> <span data-ttu-id="89415-128"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="89415-128"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="89415-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="89415-129">Library</span></span><br/> | <dl> <span data-ttu-id="89415-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="89415-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="89415-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89415-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89415-132">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="89415-132">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
