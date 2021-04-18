---
description: Crea una mesh di interfaccia personalizzata da un'altra mesh.
ms.assetid: 4c69377e-61ef-42b8-8864-c116164d4b22
title: Funzione D3DXCreateSkinInfoFromBlendedMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfoFromBlendedMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d81de43dde2b4f0df5913831ddfcefbab1a41855
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530925"
---
# <a name="d3dxcreateskininfofromblendedmesh-function"></a><span data-ttu-id="8ced1-103">D3DXCreateSkinInfoFromBlendedMesh (funzione)</span><span class="sxs-lookup"><span data-stu-id="8ced1-103">D3DXCreateSkinInfoFromBlendedMesh function</span></span>

<span data-ttu-id="8ced1-104">Crea una mesh di interfaccia personalizzata da un'altra mesh.</span><span class="sxs-lookup"><span data-stu-id="8ced1-104">Creates a skin mesh from another mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ced1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8ced1-105">Syntax</span></span>


```C++
HRESULT D3DXCreateSkinInfoFromBlendedMesh(
  _In_        LPD3DXBASEMESH      pMesh,
  _In_        DWORD               NumBones,
  _In_  const D3DXBONECOMBINATION *pBoneCombinationTable,
  _Out_       LPD3DXSKININFO      *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="8ced1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8ced1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ced1-107">*pMesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ced1-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ced1-108">Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="8ced1-108">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="8ced1-109">Puntatore a un oggetto [**ID3DXBaseMesh**](id3dxbasemesh.md) , mesh da cui creare la mesh dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="8ced1-109">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) object, the mesh from which to create the skin mesh.</span></span>

</dd> <dt>

<span data-ttu-id="8ced1-110">*NumBones* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ced1-110">*NumBones* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ced1-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ced1-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8ced1-112">Lunghezza della matrice associata a BoneId.</span><span class="sxs-lookup"><span data-stu-id="8ced1-112">The length of the array attached to the BoneId.</span></span> <span data-ttu-id="8ced1-113">Vedere [**D3DXBONECOMBINATION**](d3dxbonecombination.md).</span><span class="sxs-lookup"><span data-stu-id="8ced1-113">See [**D3DXBONECOMBINATION**](d3dxbonecombination.md).</span></span>

</dd> <dt>

<span data-ttu-id="8ced1-114">*pBoneCombinationTable* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ced1-114">*pBoneCombinationTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ced1-115">Tipo: **const [**D3DXBONECOMBINATION**](d3dxbonecombination.md) \***</span><span class="sxs-lookup"><span data-stu-id="8ced1-115">Type: **const [**D3DXBONECOMBINATION**](d3dxbonecombination.md)\***</span></span>

<span data-ttu-id="8ced1-116">Puntatore a una matrice di combinazioni di osso.</span><span class="sxs-lookup"><span data-stu-id="8ced1-116">Pointer to an array of bone combinations.</span></span> <span data-ttu-id="8ced1-117">Vedere [**D3DXBONECOMBINATION**](d3dxbonecombination.md).</span><span class="sxs-lookup"><span data-stu-id="8ced1-117">See [**D3DXBONECOMBINATION**](d3dxbonecombination.md).</span></span>

</dd> <dt>

<span data-ttu-id="8ced1-118">*ppSkinInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8ced1-118">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ced1-119">Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ced1-119">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***</span></span>

<span data-ttu-id="8ced1-120">Indirizzo di un puntatore a un'interfaccia [**ID3DXSkinInfo**](id3dxskininfo.md) che rappresenta l'oggetto mesh interfaccia creato.</span><span class="sxs-lookup"><span data-stu-id="8ced1-120">Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) interface representing the created skin mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ced1-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8ced1-121">Return value</span></span>

<span data-ttu-id="8ced1-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8ced1-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8ced1-123">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8ced1-123">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8ced1-124">Se la funzione ha esito negativo, il valore restituito può essere il seguente: E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="8ced1-124">If the function fails, the return value can be the following: E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ced1-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ced1-125">Requirements</span></span>



| <span data-ttu-id="8ced1-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ced1-126">Requirement</span></span> | <span data-ttu-id="8ced1-127">Valore</span><span class="sxs-lookup"><span data-stu-id="8ced1-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ced1-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8ced1-128">Header</span></span><br/>  | <dl> <span data-ttu-id="8ced1-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ced1-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8ced1-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="8ced1-130">Library</span></span><br/> | <dl> <span data-ttu-id="8ced1-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ced1-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8ced1-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8ced1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ced1-133">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="8ced1-133">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
