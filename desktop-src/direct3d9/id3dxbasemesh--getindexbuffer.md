---
description: Recupera i dati in un buffer di indice.
ms.assetid: 8e14a047-a8a6-4763-88c7-3b439044eeb4
title: 'Metodo ID3DXBaseMesh:: GetIndexBuffer (D3DX9Mesh. h)'
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
ms.openlocfilehash: 5b7cf57cd8f31e54cf48ae7f0cab69a40783debe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355159"
---
# <a name="id3dxbasemeshgetindexbuffer-method"></a><span data-ttu-id="716b2-103">Metodo ID3DXBaseMesh:: GetIndexBuffer</span><span class="sxs-lookup"><span data-stu-id="716b2-103">ID3DXBaseMesh::GetIndexBuffer method</span></span>

<span data-ttu-id="716b2-104">Recupera i dati in un buffer di indice.</span><span class="sxs-lookup"><span data-stu-id="716b2-104">Retrieves the data in an index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="716b2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="716b2-105">Syntax</span></span>


```C++
HRESULT GetIndexBuffer(
  [out, retval] LPDIRECT3DINDEXBUFFER9 *ppIB
);
```



## <a name="parameters"></a><span data-ttu-id="716b2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="716b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="716b2-107">*ppIB* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="716b2-107">*ppIB* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="716b2-108">Tipo: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="716b2-108">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span></span>

<span data-ttu-id="716b2-109">Indirizzo di un puntatore a un'interfaccia [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) , che rappresenta l'oggetto buffer di indice associato alla mesh.</span><span class="sxs-lookup"><span data-stu-id="716b2-109">Address of a pointer to an [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) interface, representing the index buffer object associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="716b2-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="716b2-110">Return value</span></span>

<span data-ttu-id="716b2-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="716b2-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="716b2-112">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="716b2-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="716b2-113">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="716b2-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="716b2-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="716b2-114">Requirements</span></span>



| <span data-ttu-id="716b2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="716b2-115">Requirement</span></span> | <span data-ttu-id="716b2-116">Valore</span><span class="sxs-lookup"><span data-stu-id="716b2-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="716b2-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="716b2-117">Header</span></span><br/>  | <dl> <span data-ttu-id="716b2-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="716b2-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="716b2-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="716b2-119">Library</span></span><br/> | <dl> <span data-ttu-id="716b2-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="716b2-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="716b2-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="716b2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="716b2-122">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="716b2-122">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
