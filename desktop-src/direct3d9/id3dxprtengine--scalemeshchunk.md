---
description: Ridimensiona tutti gli esempi associati a una data mesh specificata. Il metodo è utile per il calcolo della dispersione della sottosuperficie.
ms.assetid: abb9ca6a-5fc2-4986-8a38-29998fe5e537
title: 'Metodo ID3DXPRTEngine:: ScaleMeshChunk (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ScaleMeshChunk
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f688a5175e7b50c33dd93d06a4f988a14c062c86
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323436"
---
# <a name="id3dxprtenginescalemeshchunk-method"></a><span data-ttu-id="ad140-104">Metodo ID3DXPRTEngine:: ScaleMeshChunk</span><span class="sxs-lookup"><span data-stu-id="ad140-104">ID3DXPRTEngine::ScaleMeshChunk method</span></span>

<span data-ttu-id="ad140-105">Ridimensiona tutti gli esempi associati a una data mesh specificata.</span><span class="sxs-lookup"><span data-stu-id="ad140-105">Scales all the samples associated with a given submesh.</span></span> <span data-ttu-id="ad140-106">Il metodo è utile per il calcolo della dispersione della sottosuperficie.</span><span class="sxs-lookup"><span data-stu-id="ad140-106">The method is useful for computing subsurface scattering.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad140-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ad140-107">Syntax</span></span>


```C++
HRESULT ScaleMeshChunk(
  [in]      UINT            uMeshChunk,
  [in]      FLOAT           fScale,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="ad140-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ad140-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad140-109">*uMeshChunk* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad140-109">*uMeshChunk* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad140-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ad140-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ad140-111">Posizione nella rete in cui iniziare il ridimensionamento degli esempi.</span><span class="sxs-lookup"><span data-stu-id="ad140-111">Location in the mesh at which to start scaling samples.</span></span>

</dd> <dt>

<span data-ttu-id="ad140-112">*fScale* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad140-112">*fScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad140-113">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ad140-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ad140-114">Valore in base al quale moltiplicare ogni vettore nel sottomesh.</span><span class="sxs-lookup"><span data-stu-id="ad140-114">Value by which to multiply each vector in the submesh.</span></span>

</dd> <dt>

<span data-ttu-id="ad140-115">*pDataOut* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="ad140-115">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad140-116">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="ad140-116">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="ad140-117">Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) per ricevere esempi riscalati nel sottomesh.</span><span class="sxs-lookup"><span data-stu-id="ad140-117">Pointer to a [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object to receive rescaled samples in the submesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad140-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ad140-118">Return value</span></span>

<span data-ttu-id="ad140-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ad140-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ad140-120">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ad140-120">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ad140-121">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="ad140-121">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad140-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad140-122">Requirements</span></span>



| <span data-ttu-id="ad140-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad140-123">Requirement</span></span> | <span data-ttu-id="ad140-124">Valore</span><span class="sxs-lookup"><span data-stu-id="ad140-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad140-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ad140-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ad140-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad140-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ad140-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="ad140-127">Library</span></span><br/> | <dl> <span data-ttu-id="ad140-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad140-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ad140-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad140-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad140-130">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="ad140-130">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
