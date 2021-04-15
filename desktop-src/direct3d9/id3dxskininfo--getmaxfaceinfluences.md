---
description: Ottiene le influenze massime della faccia in una mesh triangolare con il buffer di indice specificato.
ms.assetid: 72dc2440-87df-461e-80d0-9ad9b1e4d8ee
title: 'Metodo ID3DXSkinInfo:: GetMaxFaceInfluences (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetMaxFaceInfluences
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 11724c50d5224f0bcb2c9ced25523b869f3e347f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401922"
---
# <a name="id3dxskininfogetmaxfaceinfluences-method"></a><span data-ttu-id="6ee4a-103">Metodo ID3DXSkinInfo:: GetMaxFaceInfluences</span><span class="sxs-lookup"><span data-stu-id="6ee4a-103">ID3DXSkinInfo::GetMaxFaceInfluences method</span></span>

<span data-ttu-id="6ee4a-104">Ottiene le influenze massime della faccia in una mesh triangolare con il buffer di indice specificato.</span><span class="sxs-lookup"><span data-stu-id="6ee4a-104">Gets the maximum face influences in a triangle mesh with the specified index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ee4a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6ee4a-105">Syntax</span></span>


```C++
HRESULT GetMaxFaceInfluences(
  [in] LPDIRECT3DINDEXBUFFER9 pIB,
  [in] DWORD                  NumFaces,
  [in] DWORD                  *maxFaceInfluences
);
```



## <a name="parameters"></a><span data-ttu-id="6ee4a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6ee4a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ee4a-107">*pIB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6ee4a-107">*pIB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ee4a-108">Tipo: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)**</span><span class="sxs-lookup"><span data-stu-id="6ee4a-108">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)**</span></span>

<span data-ttu-id="6ee4a-109">Puntatore al buffer di indice contenente i dati dell'indice mesh.</span><span class="sxs-lookup"><span data-stu-id="6ee4a-109">Pointer to the index buffer that contains the mesh index data.</span></span>

</dd> <dt>

<span data-ttu-id="6ee4a-110">*NumFaces* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6ee4a-110">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ee4a-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6ee4a-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6ee4a-112">Numero di visi nella rete.</span><span class="sxs-lookup"><span data-stu-id="6ee4a-112">Number of faces in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="6ee4a-113">*maxFaceInfluences* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6ee4a-113">*maxFaceInfluences* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ee4a-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6ee4a-114">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6ee4a-115">Puntatore alle influenze massime della faccia.</span><span class="sxs-lookup"><span data-stu-id="6ee4a-115">Pointer to the maximum face influences.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ee4a-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6ee4a-116">Return value</span></span>

<span data-ttu-id="6ee4a-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6ee4a-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6ee4a-118">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6ee4a-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6ee4a-119">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="6ee4a-119">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ee4a-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ee4a-120">Requirements</span></span>



| <span data-ttu-id="6ee4a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ee4a-121">Requirement</span></span> | <span data-ttu-id="6ee4a-122">Valore</span><span class="sxs-lookup"><span data-stu-id="6ee4a-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ee4a-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6ee4a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="6ee4a-124"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ee4a-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6ee4a-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="6ee4a-125">Library</span></span><br/> | <dl> <span data-ttu-id="6ee4a-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ee4a-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6ee4a-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6ee4a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ee4a-128">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="6ee4a-128">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
