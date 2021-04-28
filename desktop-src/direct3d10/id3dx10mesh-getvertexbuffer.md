---
description: 'Metodo ID3DX10Mesh::GetVertexBuffer: recupera il buffer dei vertici associato alla mesh.'
ms.assetid: c69a712b-8964-4a5b-a136-3f24060b7fd8
title: Metodo ID3DX10Mesh::GetVertexBuffer (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8a63b08cf978a65e1fa9999c79b8033436b41fa2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108079"
---
# <a name="id3dx10meshgetvertexbuffer-method"></a><span data-ttu-id="e9894-103">Metodo ID3DX10Mesh::GetVertexBuffer</span><span class="sxs-lookup"><span data-stu-id="e9894-103">ID3DX10Mesh::GetVertexBuffer method</span></span>

<span data-ttu-id="e9894-104">Recupera il buffer dei vertici associato alla mesh.</span><span class="sxs-lookup"><span data-stu-id="e9894-104">Retrieves the vertex buffer associated with the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9894-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9894-105">Syntax</span></span>


```C++
HRESULT GetVertexBuffer(
  [in]  UINT              iBuffer,
  [out] ID3DX10MeshBuffer **ppVertexBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="e9894-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e9894-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9894-107">*iBuffer* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="e9894-107">*iBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9894-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e9894-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e9894-109">Buffer dei vertici da ottenere.</span><span class="sxs-lookup"><span data-stu-id="e9894-109">The vertex buffer to get.</span></span> <span data-ttu-id="e9894-110">Si tratta di un valore di indice.</span><span class="sxs-lookup"><span data-stu-id="e9894-110">This is an index value.</span></span>

</dd> <dt>

<span data-ttu-id="e9894-111">*ppVertexBuffer* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="e9894-111">*ppVertexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9894-112">Tipo: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="e9894-112">Type: **[**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span></span>

<span data-ttu-id="e9894-113">Buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="e9894-113">The vertex buffer.</span></span> <span data-ttu-id="e9894-114">Vedere [ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)</span><span class="sxs-lookup"><span data-stu-id="e9894-114">See [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9894-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e9894-115">Return value</span></span>

<span data-ttu-id="e9894-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e9894-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e9894-117">Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 10.](d3d10-graphics-reference-returnvalues.md)</span><span class="sxs-lookup"><span data-stu-id="e9894-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e9894-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9894-118">Requirements</span></span>



| <span data-ttu-id="e9894-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9894-119">Requirement</span></span> | <span data-ttu-id="e9894-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e9894-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e9894-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e9894-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e9894-122"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="e9894-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="e9894-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="e9894-123">Library</span></span><br/> | <dl> <span data-ttu-id="e9894-124"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9894-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9894-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9894-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9894-126">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="e9894-126">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="e9894-127">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="e9894-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
