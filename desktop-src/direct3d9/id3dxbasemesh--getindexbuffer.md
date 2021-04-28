---
description: 'Metodo ID3DXBaseMesh::GetIndexBuffer: recupera i dati in un index buffer.'
ms.assetid: 8e14a047-a8a6-4763-88c7-3b439044eeb4
title: Metodo ID3DXBaseMesh::GetIndexBuffer (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 40e57193a2bf9a47ed0c57e6d13644441fbc42ce
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115429"
---
# <a name="id3dxbasemeshgetindexbuffer-method"></a><span data-ttu-id="4473a-103">Metodo ID3DXBaseMesh::GetIndexBuffer</span><span class="sxs-lookup"><span data-stu-id="4473a-103">ID3DXBaseMesh::GetIndexBuffer method</span></span>

<span data-ttu-id="4473a-104">Recupera i dati in un index buffer.</span><span class="sxs-lookup"><span data-stu-id="4473a-104">Retrieves the data in an index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="4473a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4473a-105">Syntax</span></span>


```C++
HRESULT GetIndexBuffer(
  [out, retval] LPDIRECT3DINDEXBUFFER9 *ppIB
);
```



## <a name="parameters"></a><span data-ttu-id="4473a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4473a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4473a-107">*ppIB* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="4473a-107">*ppIB* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4473a-108">Tipo: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="4473a-108">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span></span>

<span data-ttu-id="4473a-109">Indirizzo di un puntatore a [**un'interfaccia IDirect3DIndexBuffer9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) che rappresenta l index buffer o object associato alla mesh.</span><span class="sxs-lookup"><span data-stu-id="4473a-109">Address of a pointer to an [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) interface, representing the index buffer object associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4473a-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4473a-110">Return value</span></span>

<span data-ttu-id="4473a-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4473a-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4473a-112">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4473a-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4473a-113">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="4473a-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="4473a-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4473a-114">Requirements</span></span>



| <span data-ttu-id="4473a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4473a-115">Requirement</span></span> | <span data-ttu-id="4473a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="4473a-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4473a-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4473a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="4473a-118"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="4473a-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="4473a-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="4473a-119">Library</span></span><br/> | <dl> <span data-ttu-id="4473a-120"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="4473a-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4473a-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4473a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4473a-122">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="4473a-122">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
