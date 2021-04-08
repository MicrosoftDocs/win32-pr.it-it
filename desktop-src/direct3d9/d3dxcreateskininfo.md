---
description: Crea un oggetto mesh dell'interfaccia vuota utilizzando un dichiaratore.
ms.assetid: c98da2e5-a9eb-4070-8846-b346b5c57fb3
title: Funzione D3DXCreateSkinInfo (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfo
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 83ee214eb997414e113256060dbe59d3cd47d1a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886283"
---
# <a name="d3dxcreateskininfo-function"></a><span data-ttu-id="d5ff2-103">D3DXCreateSkinInfo (funzione)</span><span class="sxs-lookup"><span data-stu-id="d5ff2-103">D3DXCreateSkinInfo function</span></span>

<span data-ttu-id="d5ff2-104">Crea un oggetto mesh dell'interfaccia vuota utilizzando un dichiaratore.</span><span class="sxs-lookup"><span data-stu-id="d5ff2-104">Creates an empty skin mesh object using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5ff2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d5ff2-105">Syntax</span></span>


```C++
HRESULT D3DXCreateSkinInfo(
  _In_        DWORD             NumVertices,
  _In_  const D3DVERTEXELEMENT9 *pDeclaration,
  _In_        DWORD             NumBones,
  _Out_       LPD3DXSKININFO    *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="d5ff2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d5ff2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5ff2-107">*NumVertices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5ff2-107">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5ff2-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d5ff2-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d5ff2-109">Numero di vertici per la mesh dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="d5ff2-109">Number of vertices for the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="d5ff2-110">*pDeclaration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5ff2-110">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5ff2-111">Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="d5ff2-111">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="d5ff2-112">Matrice di elementi [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , che descrive il formato del vertice per la mesh restituita.</span><span class="sxs-lookup"><span data-stu-id="d5ff2-112">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the vertex format for the returned mesh.</span></span>

</dd> <dt>

<span data-ttu-id="d5ff2-113">*NumBones* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5ff2-113">*NumBones* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5ff2-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d5ff2-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d5ff2-115">Numero di ossa per la mesh dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="d5ff2-115">Number of bones for the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="d5ff2-116">*ppSkinInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d5ff2-116">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5ff2-117">Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="d5ff2-117">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***</span></span>

<span data-ttu-id="d5ff2-118">Indirizzo di un puntatore a un'interfaccia [**ID3DXSkinInfo**](id3dxskininfo.md) , che rappresenta l'oggetto mesh interfaccia creato.</span><span class="sxs-lookup"><span data-stu-id="d5ff2-118">Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) interface, representing the created skin mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5ff2-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d5ff2-119">Return value</span></span>

<span data-ttu-id="d5ff2-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d5ff2-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d5ff2-121">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d5ff2-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d5ff2-122">Se la funzione ha esito negativo, il valore restituito può essere: E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="d5ff2-122">If the function fails, the return value can be: E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5ff2-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="d5ff2-123">Remarks</span></span>

<span data-ttu-id="d5ff2-124">Usare [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md) per popolare l'oggetto mesh interfaccia vuota restituito da questo metodo.</span><span class="sxs-lookup"><span data-stu-id="d5ff2-124">Use [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md) to populate the empty skin mesh object returned by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5ff2-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5ff2-125">Requirements</span></span>



| <span data-ttu-id="d5ff2-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5ff2-126">Requirement</span></span> | <span data-ttu-id="d5ff2-127">Valore</span><span class="sxs-lookup"><span data-stu-id="d5ff2-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5ff2-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d5ff2-128">Header</span></span><br/>  | <dl> <span data-ttu-id="d5ff2-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5ff2-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d5ff2-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="d5ff2-130">Library</span></span><br/> | <dl> <span data-ttu-id="d5ff2-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5ff2-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d5ff2-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5ff2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5ff2-133">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="d5ff2-133">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="d5ff2-134">**SetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="d5ff2-134">**SetBoneInfluence**</span></span>](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 
