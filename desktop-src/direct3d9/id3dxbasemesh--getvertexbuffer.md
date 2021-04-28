---
description: 'Metodo ID3DXBaseMesh::GetVertexBuffer: recupera il buffer dei vertici associato alla mesh.'
ms.assetid: 5caa6ce1-feab-4919-944e-f92fad3ad443
title: Metodo ID3DXBaseMesh::GetVertexBuffer (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9533188e3e2effe1759b58f70c9f033cc491844c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115369"
---
# <a name="id3dxbasemeshgetvertexbuffer-method"></a><span data-ttu-id="01d4b-103">Metodo ID3DXBaseMesh::GetVertexBuffer</span><span class="sxs-lookup"><span data-stu-id="01d4b-103">ID3DXBaseMesh::GetVertexBuffer method</span></span>

<span data-ttu-id="01d4b-104">Recupera il buffer dei vertici associato alla mesh.</span><span class="sxs-lookup"><span data-stu-id="01d4b-104">Retrieves the vertex buffer associated with the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="01d4b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="01d4b-105">Syntax</span></span>


```C++
HRESULT GetVertexBuffer(
  [out, retval] LPDIRECT3DVERTEXBUFFER9 *ppVB
);
```



## <a name="parameters"></a><span data-ttu-id="01d4b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="01d4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01d4b-107">*ppVB* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="01d4b-107">*ppVB* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="01d4b-108">Tipo: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="01d4b-108">Type: **[**LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***</span></span>

<span data-ttu-id="01d4b-109">Indirizzo di un puntatore a [**un'interfaccia IDirect3DVertexBuffer9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) che rappresenta l'oggetto vertex buffer associato alla mesh.</span><span class="sxs-lookup"><span data-stu-id="01d4b-109">Address of a pointer to an [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) interface, representing the vertex buffer object associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01d4b-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="01d4b-110">Return value</span></span>

<span data-ttu-id="01d4b-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="01d4b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="01d4b-112">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="01d4b-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="01d4b-113">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="01d4b-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="01d4b-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01d4b-114">Requirements</span></span>



| <span data-ttu-id="01d4b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="01d4b-115">Requirement</span></span> | <span data-ttu-id="01d4b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="01d4b-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="01d4b-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="01d4b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="01d4b-118"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="01d4b-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="01d4b-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="01d4b-119">Library</span></span><br/> | <dl> <span data-ttu-id="01d4b-120"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="01d4b-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="01d4b-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01d4b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01d4b-122">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="01d4b-122">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
