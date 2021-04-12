---
description: Ottiene il buffer Rep del punto della rete.
ms.assetid: 4be7bee5-15ea-496f-83c2-a3a9bafd97c6
title: 'Metodo ID3DX10Mesh:: GetPointRepBuffer (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetPointRepBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 131094792f35b21fd230b66bda6a43fb104b65ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132350"
---
# <a name="id3dx10meshgetpointrepbuffer-method"></a><span data-ttu-id="aa965-103">Metodo ID3DX10Mesh:: GetPointRepBuffer</span><span class="sxs-lookup"><span data-stu-id="aa965-103">ID3DX10Mesh::GetPointRepBuffer method</span></span>

<span data-ttu-id="aa965-104">Ottiene il buffer Rep del punto della rete.</span><span class="sxs-lookup"><span data-stu-id="aa965-104">Get the mesh's point rep buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa965-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aa965-105">Syntax</span></span>


```C++
HRESULT GetPointRepBuffer(
  [out] ID3DX10MeshBuffer **ppPointReps
);
```



## <a name="parameters"></a><span data-ttu-id="aa965-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="aa965-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa965-107">*ppPointReps* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="aa965-107">*ppPointReps* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa965-108">Tipo: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="aa965-108">Type: **[**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span></span>

<span data-ttu-id="aa965-109">Puntatore a un buffer Mesh contenente i dati della Rep punti della rete.</span><span class="sxs-lookup"><span data-stu-id="aa965-109">Pointer to a mesh buffer containing the mesh's point rep data.</span></span> <span data-ttu-id="aa965-110">Vedere [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="aa965-110">See [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa965-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aa965-111">Return value</span></span>

<span data-ttu-id="aa965-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="aa965-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="aa965-113">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="aa965-113">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa965-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa965-114">Requirements</span></span>



| <span data-ttu-id="aa965-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa965-115">Requirement</span></span> | <span data-ttu-id="aa965-116">Valore</span><span class="sxs-lookup"><span data-stu-id="aa965-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aa965-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aa965-117">Header</span></span><br/>  | <dl> <span data-ttu-id="aa965-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa965-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="aa965-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="aa965-119">Library</span></span><br/> | <dl> <span data-ttu-id="aa965-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aa965-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa965-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa965-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa965-122">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="aa965-122">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="aa965-123">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="aa965-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




