---
description: Accedere al buffer adiacenza della mesh.
ms.assetid: 42b13f14-4edf-4b56-9198-60a548855542
title: 'Metodo ID3DX10Mesh:: GetAdjacencyBuffer (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetAdjacencyBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 80dd5c6e6d9b12cb1c648c42a4758d215d3810c7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323153"
---
# <a name="id3dx10meshgetadjacencybuffer-method"></a><span data-ttu-id="c018a-103">Metodo ID3DX10Mesh:: GetAdjacencyBuffer</span><span class="sxs-lookup"><span data-stu-id="c018a-103">ID3DX10Mesh::GetAdjacencyBuffer method</span></span>

<span data-ttu-id="c018a-104">Accedere al buffer adiacenza della mesh.</span><span class="sxs-lookup"><span data-stu-id="c018a-104">Access the mesh's adjacency buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c018a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c018a-105">Syntax</span></span>


```C++
HRESULT GetAdjacencyBuffer(
  [out] ID3DX10MeshBuffer **ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="c018a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c018a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c018a-107">*ppAdjacency* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c018a-107">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c018a-108">Tipo: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="c018a-108">Type: **[**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span></span>

<span data-ttu-id="c018a-109">Buffer adiacenza.</span><span class="sxs-lookup"><span data-stu-id="c018a-109">The adjacency buffer.</span></span> <span data-ttu-id="c018a-110">Vedere [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="c018a-110">See [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c018a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c018a-111">Return value</span></span>

<span data-ttu-id="c018a-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c018a-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c018a-113">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="c018a-113">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c018a-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c018a-114">Requirements</span></span>



| <span data-ttu-id="c018a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c018a-115">Requirement</span></span> | <span data-ttu-id="c018a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="c018a-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c018a-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c018a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c018a-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="c018a-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="c018a-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="c018a-119">Library</span></span><br/> | <dl> <span data-ttu-id="c018a-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c018a-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c018a-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c018a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c018a-122">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="c018a-122">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="c018a-123">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="c018a-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




