---
description: Applica il skining del software ai vertici di destinazione in base alle matrici correnti.
ms.assetid: 4858dfd4-dc0d-4852-9165-8ae1b40386d4
title: 'Metodo ID3DXSkinInfo:: UpdateSkinnedMesh (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.UpdateSkinnedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 645e6ae1e1cb84991b352c250b137cd3ae2491f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322053"
---
# <a name="id3dxskininfoupdateskinnedmesh-method"></a><span data-ttu-id="fbb8a-103">Metodo ID3DXSkinInfo:: UpdateSkinnedMesh</span><span class="sxs-lookup"><span data-stu-id="fbb8a-103">ID3DXSkinInfo::UpdateSkinnedMesh method</span></span>

<span data-ttu-id="fbb8a-104">Applica il skining del software ai vertici di destinazione in base alle matrici correnti.</span><span class="sxs-lookup"><span data-stu-id="fbb8a-104">Applies software skinning to the target vertices based on the current matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbb8a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fbb8a-105">Syntax</span></span>


```C++
HRESULT UpdateSkinnedMesh(
  [in] const D3DXMATRIX *pBoneTransforms,
  [in] const D3DXMATRIX *pBoneInvTransposeTransforms,
  [in]       LPCVOID    pVerticesSrc,
  [in]       PVOID      pVerticesDst
);
```



## <a name="parameters"></a><span data-ttu-id="fbb8a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fbb8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbb8a-107">*pBoneTransforms* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fbb8a-107">*pBoneTransforms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbb8a-108">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="fbb8a-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fbb8a-109">Matrice di trasformazione Bone.</span><span class="sxs-lookup"><span data-stu-id="fbb8a-109">Bone transform matrix.</span></span>

</dd> <dt>

<span data-ttu-id="fbb8a-110">*pBoneInvTransposeTransforms* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fbb8a-110">*pBoneInvTransposeTransforms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbb8a-111">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="fbb8a-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fbb8a-112">Trasponi inversa della matrice di trasformazione Bone.</span><span class="sxs-lookup"><span data-stu-id="fbb8a-112">Inverse transpose of the bone transform matrix.</span></span>

</dd> <dt>

<span data-ttu-id="fbb8a-113">*pVerticesSrc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fbb8a-113">*pVerticesSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbb8a-114">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fbb8a-114">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fbb8a-115">Puntatore al buffer che contiene i vertici di origine.</span><span class="sxs-lookup"><span data-stu-id="fbb8a-115">Pointer to the buffer containing the source vertices.</span></span>

</dd> <dt>

<span data-ttu-id="fbb8a-116">*pVerticesDst* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fbb8a-116">*pVerticesDst* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbb8a-117">Tipo: **[ **PVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fbb8a-117">Type: **[**PVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fbb8a-118">Puntatore al buffer che contiene i vertici di destinazione.</span><span class="sxs-lookup"><span data-stu-id="fbb8a-118">Pointer to the buffer containing the destination vertices.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbb8a-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fbb8a-119">Return value</span></span>

<span data-ttu-id="fbb8a-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fbb8a-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fbb8a-121">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fbb8a-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fbb8a-122">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="fbb8a-122">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbb8a-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="fbb8a-123">Remarks</span></span>

<span data-ttu-id="fbb8a-124">Quando viene usato per l'interfaccia dei vertici con due elementi position, questo metodo consente di associare il secondo elemento position con l'inverso dell'osso anziché l'osso stesso.</span><span class="sxs-lookup"><span data-stu-id="fbb8a-124">When used to skin vertices with two position elements, this method skins the second position element with the inverse of the bone instead of the bone itself.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbb8a-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fbb8a-125">Requirements</span></span>



| <span data-ttu-id="fbb8a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbb8a-126">Requirement</span></span> | <span data-ttu-id="fbb8a-127">Valore</span><span class="sxs-lookup"><span data-stu-id="fbb8a-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbb8a-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fbb8a-128">Header</span></span><br/>  | <dl> <span data-ttu-id="fbb8a-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbb8a-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="fbb8a-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="fbb8a-130">Library</span></span><br/> | <dl> <span data-ttu-id="fbb8a-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fbb8a-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fbb8a-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fbb8a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbb8a-133">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="fbb8a-133">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
