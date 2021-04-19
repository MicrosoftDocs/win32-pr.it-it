---
description: Crea un oggetto mesh dell'interfaccia vuota utilizzando un codice FVF (Flexible Vertex Format).
ms.assetid: 72e27850-0102-4121-a397-16f2e0220b93
title: Funzione D3DXCreateSkinInfoFVF (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfoFVF
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 907ab874b8cd8b766e6f9413212ba8771df9b25c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322728"
---
# <a name="d3dxcreateskininfofvf-function"></a><span data-ttu-id="8302b-103">D3DXCreateSkinInfoFVF (funzione)</span><span class="sxs-lookup"><span data-stu-id="8302b-103">D3DXCreateSkinInfoFVF function</span></span>

<span data-ttu-id="8302b-104">Crea un oggetto mesh dell'interfaccia vuota utilizzando un codice FVF (Flexible Vertex Format).</span><span class="sxs-lookup"><span data-stu-id="8302b-104">Creates an empty skin mesh object using a flexible vertex format (FVF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="8302b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8302b-105">Syntax</span></span>


```C++
HRESULT D3DXCreateSkinInfoFVF(
  _In_  DWORD          NumVertices,
  _In_  DWORD          FVF,
  _In_  DWORD          NumBones,
  _Out_ LPD3DXSKININFO *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="8302b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8302b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8302b-107">*NumVertices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8302b-107">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8302b-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8302b-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8302b-109">Numero di vertici per la mesh dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="8302b-109">Number of vertices for the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="8302b-110">*FVF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8302b-110">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8302b-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8302b-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8302b-112">Combinazione di [D3DFVF](d3dfvf.md) che descrive il formato del vertice per la mesh dell'interfaccia restituita.</span><span class="sxs-lookup"><span data-stu-id="8302b-112">Combination of [D3DFVF](d3dfvf.md) that describes the vertex format for the returned skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="8302b-113">*NumBones* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8302b-113">*NumBones* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8302b-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8302b-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8302b-115">Numero di ossa per la mesh dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="8302b-115">Number of bones for the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="8302b-116">*ppSkinInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8302b-116">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8302b-117">Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="8302b-117">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***</span></span>

<span data-ttu-id="8302b-118">Indirizzo di un puntatore a un'interfaccia [**ID3DXSkinInfo**](id3dxskininfo.md) , che rappresenta l'oggetto informazioni di interfaccia creato.</span><span class="sxs-lookup"><span data-stu-id="8302b-118">Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) interface, representing the created skin information object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8302b-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8302b-119">Return value</span></span>

<span data-ttu-id="8302b-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8302b-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8302b-121">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8302b-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8302b-122">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="8302b-122">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="8302b-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="8302b-123">Remarks</span></span>

<span data-ttu-id="8302b-124">Usare [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md) per popolare l'oggetto mesh interfaccia vuota restituito da questo metodo.</span><span class="sxs-lookup"><span data-stu-id="8302b-124">Use [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md) to populate the empty skin mesh object returned by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8302b-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8302b-125">Requirements</span></span>



| <span data-ttu-id="8302b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8302b-126">Requirement</span></span> | <span data-ttu-id="8302b-127">Valore</span><span class="sxs-lookup"><span data-stu-id="8302b-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8302b-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8302b-128">Header</span></span><br/>  | <dl> <span data-ttu-id="8302b-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8302b-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8302b-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="8302b-130">Library</span></span><br/> | <dl> <span data-ttu-id="8302b-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8302b-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8302b-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8302b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8302b-133">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="8302b-133">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="8302b-134">**SetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="8302b-134">**SetBoneInfluence**</span></span>](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 
