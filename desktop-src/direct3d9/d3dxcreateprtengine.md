---
description: Consente di creare un oggetto ID3DXPRTEngine in grado di generare in modo efficiente simulazioni del trasferimento Radiance (pre-Computed Radiance Transfer) di una scena 3D.
ms.assetid: fdfe02b5-03fb-4bee-a53b-012ae3572644
title: Funzione D3DXCreatePRTEngine (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTEngine
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b76b58953de81041922659c3315bba9cdf7788b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530930"
---
# <a name="d3dxcreateprtengine-function"></a><span data-ttu-id="b5318-103">D3DXCreatePRTEngine (funzione)</span><span class="sxs-lookup"><span data-stu-id="b5318-103">D3DXCreatePRTEngine function</span></span>

<span data-ttu-id="b5318-104">Consente di creare un oggetto [**ID3DXPRTEngine**](id3dxprtengine.md) in grado di generare in modo efficiente simulazioni del trasferimento Radiance (pre-Computed Radiance Transfer) di una scena 3D.</span><span class="sxs-lookup"><span data-stu-id="b5318-104">Creates an [**ID3DXPRTEngine**](id3dxprtengine.md) object that can efficiently generate precomputed radiance transfer (PRT) simulations of a 3D scene.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5318-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5318-105">Syntax</span></span>


```C++
HRESULT D3DXCreatePRTEngine(
  _In_    LPD3DXMESH      pMesh,
  _In_    DWORD           *pAdjacency,
  _In_    BOOL            ExtractUVs,
  _In_    LPD3DXMESH      pBlockerMesh,
  _Inout_ LPD3DXPRTENGINE ppEngine
);
```



## <a name="parameters"></a><span data-ttu-id="b5318-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5318-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5318-107">*pMesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5318-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5318-108">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="b5318-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="b5318-109">Puntatore a un oggetto mesh [**ID3DXMesh**](id3dxmesh.md) di input che modella la scena 3D.</span><span class="sxs-lookup"><span data-stu-id="b5318-109">Pointer to an input [**ID3DXMesh**](id3dxmesh.md) mesh object that models the 3D scene.</span></span> <span data-ttu-id="b5318-110">Questa mesh deve contenere una tabella di attributi in cui i vertici si trovano in un attributo univoco.</span><span class="sxs-lookup"><span data-stu-id="b5318-110">This mesh must have an attribute table in which vertices are in a unique attribute.</span></span>

</dd> <dt>

<span data-ttu-id="b5318-111">*pAdjacency* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5318-111">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5318-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b5318-112">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b5318-113">Puntatore facoltativo a una matrice di tre DWORD per volto da riempire con indici facciali adiacenti.</span><span class="sxs-lookup"><span data-stu-id="b5318-113">Optional pointer to an array of three DWORDs per face to be filled with adjacent face indices.</span></span> <span data-ttu-id="b5318-114">Il numero di byte in questa matrice deve essere almeno ((3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)) \* sizeof (DWORD)).</span><span class="sxs-lookup"><span data-stu-id="b5318-114">The number of bytes in this array must be at least ((3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)) \* sizeof(DWORD)).</span></span> <span data-ttu-id="b5318-115">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="b5318-115">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b5318-116">*ExtractUVs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5318-116">*ExtractUVs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5318-117">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b5318-117">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b5318-118">Se **true**, verranno usate le trame per archiviare i vettori ALBEDOS o PRT.</span><span class="sxs-lookup"><span data-stu-id="b5318-118">If **TRUE**, textures will be used to store albedos or PRT vectors.</span></span>

</dd> <dt>

<span data-ttu-id="b5318-119">*pBlockerMesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5318-119">*pBlockerMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5318-120">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="b5318-120">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="b5318-121">Puntatore a un oggetto mesh [**ID3DXMesh**](id3dxmesh.md) facoltativo che blocca la scena 3D.</span><span class="sxs-lookup"><span data-stu-id="b5318-121">Pointer to an optional [**ID3DXMesh**](id3dxmesh.md) mesh object that blocks the 3D scene.</span></span> <span data-ttu-id="b5318-122">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="b5318-122">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b5318-123">*ppEngine* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="b5318-123">*ppEngine* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5318-124">Tipo: **[ **LPD3DXPRTENGINE**](id3dxprtengine.md)**</span><span class="sxs-lookup"><span data-stu-id="b5318-124">Type: **[**LPD3DXPRTENGINE**](id3dxprtengine.md)**</span></span>

<span data-ttu-id="b5318-125">Puntatore a un oggetto [**ID3DXPRTEngine**](id3dxprtengine.md) di output.</span><span class="sxs-lookup"><span data-stu-id="b5318-125">Pointer to an output [**ID3DXPRTEngine**](id3dxprtengine.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5318-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5318-126">Return value</span></span>

<span data-ttu-id="b5318-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b5318-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b5318-128">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b5318-128">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b5318-129">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="b5318-129">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5318-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="b5318-130">Remarks</span></span>

<span data-ttu-id="b5318-131">Usare [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) per combinare più mesh in un'unica interfaccia mesh.</span><span class="sxs-lookup"><span data-stu-id="b5318-131">Use [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) to combine multiple meshes into a single mesh interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5318-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5318-132">Requirements</span></span>



| <span data-ttu-id="b5318-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5318-133">Requirement</span></span> | <span data-ttu-id="b5318-134">Valore</span><span class="sxs-lookup"><span data-stu-id="b5318-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5318-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b5318-135">Header</span></span><br/>  | <dl> <span data-ttu-id="b5318-136"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5318-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b5318-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="b5318-137">Library</span></span><br/> | <dl> <span data-ttu-id="b5318-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5318-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b5318-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5318-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5318-140">Funzioni di trasferimento Radiance pre-calcolate</span><span class="sxs-lookup"><span data-stu-id="b5318-140">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
