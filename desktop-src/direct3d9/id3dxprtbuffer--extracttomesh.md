---
description: Estrae i dati coefficienti da un buffer a canale singolo e li aggiunge a un oggetto ID3DXMesh.
ms.assetid: 4fada987-ddd7-4c02-a177-dd81f3790588
title: 'Metodo ID3DXPRTBuffer:: ExtractToMesh (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ExtractToMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e6dfe545a934f541938d6030cdc3814f451d93c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323704"
---
# <a name="id3dxprtbufferextracttomesh-method"></a><span data-ttu-id="cde71-103">Metodo ID3DXPRTBuffer:: ExtractToMesh</span><span class="sxs-lookup"><span data-stu-id="cde71-103">ID3DXPRTBuffer::ExtractToMesh method</span></span>

<span data-ttu-id="cde71-104">Estrae i dati coefficienti da un buffer a canale singolo e li aggiunge a un oggetto [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="cde71-104">Extracts coefficient data from a single-channel buffer and adds the data to an [**ID3DXMesh**](id3dxmesh.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cde71-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cde71-105">Syntax</span></span>


```C++
HRESULT ExtractToMesh(
  [in] UINT         NumCoefficients,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         UsageIndexStart,
  [in] LPD3DXMESH   pScene
);
```



## <a name="parameters"></a><span data-ttu-id="cde71-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cde71-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cde71-107">*NumCoefficients* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cde71-107">*NumCoefficients* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cde71-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cde71-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cde71-109">Numero di coefficienti da estrarre dal buffer.</span><span class="sxs-lookup"><span data-stu-id="cde71-109">Number of coefficients to extract from the buffer.</span></span> <span data-ttu-id="cde71-110">Quando si usa il trasferimento di radianza (SH) pre-calcolato a forma sferica (PRT), il numero di coefficienti deve essere Order ².</span><span class="sxs-lookup"><span data-stu-id="cde71-110">When using spherical harmonic (SH) precomputed radiance transfer (PRT), the number of coefficients should be Order ².</span></span> <span data-ttu-id="cde71-111">L'ordine deve essere compreso tra [D3DXSH \_ MINORDER](other-d3dx-constants.md) \_ e D3DXSH MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="cde71-111">Order must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="cde71-112">*Utilizzo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="cde71-112">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cde71-113">Tipo: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**</span><span class="sxs-lookup"><span data-stu-id="cde71-113">Type: **[**D3DDECLUSAGE**](./d3ddeclusage.md)**</span></span>

<span data-ttu-id="cde71-114">Descrizioni dell'utilizzo dei vertici della mesh.</span><span class="sxs-lookup"><span data-stu-id="cde71-114">Vertex usage descriptions of the mesh.</span></span> <span data-ttu-id="cde71-115">Vedere [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="cde71-115">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="cde71-116">*UsageIndexStart* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cde71-116">*UsageIndexStart* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cde71-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cde71-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cde71-118">Indice iniziale per i coefficienti da archiviare nella rete.</span><span class="sxs-lookup"><span data-stu-id="cde71-118">Starting index for coefficients to be stored in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="cde71-119">*pScene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cde71-119">*pScene* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cde71-120">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="cde71-120">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="cde71-121">Puntatore a un oggetto mesh [**ID3DXMesh**](id3dxmesh.md) che archivia i coefficienti.</span><span class="sxs-lookup"><span data-stu-id="cde71-121">Pointer to an [**ID3DXMesh**](id3dxmesh.md) mesh object that will store coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cde71-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cde71-122">Return value</span></span>

<span data-ttu-id="cde71-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cde71-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cde71-124">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cde71-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="cde71-125">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="cde71-125">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="cde71-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cde71-126">Requirements</span></span>



| <span data-ttu-id="cde71-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="cde71-127">Requirement</span></span> | <span data-ttu-id="cde71-128">Valore</span><span class="sxs-lookup"><span data-stu-id="cde71-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cde71-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cde71-129">Header</span></span><br/>  | <dl> <span data-ttu-id="cde71-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="cde71-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="cde71-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="cde71-131">Library</span></span><br/> | <dl> <span data-ttu-id="cde71-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cde71-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cde71-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cde71-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cde71-134">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="cde71-134">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 
