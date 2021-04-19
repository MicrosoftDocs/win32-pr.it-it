---
description: Recupera i valori albedo dei vertici mesh.
ms.assetid: 12b8d6d1-c806-4dcd-80ac-f3963215dcf4
title: 'Metodo ID3DXPRTEngine:: GetVertexAlbedo (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.GetVertexAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7926f6393221552107667c9209ef2b4c51945ab8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323440"
---
# <a name="id3dxprtenginegetvertexalbedo-method"></a><span data-ttu-id="6aa7c-103">Metodo ID3DXPRTEngine:: GetVertexAlbedo</span><span class="sxs-lookup"><span data-stu-id="6aa7c-103">ID3DXPRTEngine::GetVertexAlbedo method</span></span>

<span data-ttu-id="6aa7c-104">Recupera i valori albedo dei vertici mesh.</span><span class="sxs-lookup"><span data-stu-id="6aa7c-104">Retrieves albedo values of the mesh vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="6aa7c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6aa7c-105">Syntax</span></span>


```C++
HRESULT GetVertexAlbedo(
  [in, out] D3DXCOLOR *pVertColors,
  [in]      UINT      NumVerts
);
```



## <a name="parameters"></a><span data-ttu-id="6aa7c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6aa7c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6aa7c-107">*pVertColors* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="6aa7c-107">*pVertColors* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6aa7c-108">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="6aa7c-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="6aa7c-109">Puntatore a una matrice di destinazione di valori albedo dei vertici della mesh.</span><span class="sxs-lookup"><span data-stu-id="6aa7c-109">Pointer to a destination array of albedo values of the mesh vertices.</span></span> <span data-ttu-id="6aa7c-110">Vedere [**D3DXCOLOR**](d3dxcolor.md).</span><span class="sxs-lookup"><span data-stu-id="6aa7c-110">See [**D3DXCOLOR**](d3dxcolor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6aa7c-111">*NumVerts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6aa7c-111">*NumVerts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6aa7c-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6aa7c-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6aa7c-113">Numero di vertici nella rete.</span><span class="sxs-lookup"><span data-stu-id="6aa7c-113">Number of vertices in the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6aa7c-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6aa7c-114">Return value</span></span>

<span data-ttu-id="6aa7c-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6aa7c-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6aa7c-116">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6aa7c-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="6aa7c-117">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="6aa7c-117">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="6aa7c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6aa7c-118">Requirements</span></span>



| <span data-ttu-id="6aa7c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6aa7c-119">Requirement</span></span> | <span data-ttu-id="6aa7c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="6aa7c-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6aa7c-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6aa7c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="6aa7c-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="6aa7c-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6aa7c-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="6aa7c-123">Library</span></span><br/> | <dl> <span data-ttu-id="6aa7c-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6aa7c-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6aa7c-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6aa7c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6aa7c-126">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="6aa7c-126">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
