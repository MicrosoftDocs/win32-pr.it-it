---
description: 'Funzione D3DXSHPRTCompSuperCluster: usata con i risultati compressi della versione vertice del simulatore PRT (Precomputed Radiance Transfer).'
ms.assetid: 0ec28b8c-5010-48a4-8e45-d7f9aa08185f
title: Funzione D3DXSHPRTCompSuperCluster (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTCompSuperCluster
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c22c8a3a14fd8af3e9104889b421068c7ff1457
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117859"
---
# <a name="d3dxshprtcompsupercluster-function"></a><span data-ttu-id="562a0-103">Funzione D3DXSHPRTCompSuperCluster</span><span class="sxs-lookup"><span data-stu-id="562a0-103">D3DXSHPRTCompSuperCluster function</span></span>

<span data-ttu-id="562a0-104">Usato con i risultati compressi della versione dei vertici del simulatore di trasferimento di raggi pre-ricalcolo (PRT).</span><span class="sxs-lookup"><span data-stu-id="562a0-104">Used with compressed results of the vertex version of the precomputed radiance transfer (PRT) simulator.</span></span> <span data-ttu-id="562a0-105">Genera "supercluster", ovvero gruppi di cluster che possono essere disegnati nella stessa chiamata di disegno.</span><span class="sxs-lookup"><span data-stu-id="562a0-105">Generates "superclusters," which are groups of clusters that can be drawn in the same draw call.</span></span> <span data-ttu-id="562a0-106">Per raggruppare i cluster viene usato un algoritmo greedy che riduce al minimo il ridisegno.</span><span class="sxs-lookup"><span data-stu-id="562a0-106">A greedy algorithm that minimizes overdraw is used to group the clusters.</span></span>

## <a name="syntax"></a><span data-ttu-id="562a0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="562a0-107">Syntax</span></span>


```C++
HRESULT D3DXSHPRTCompSuperCluster(
  _In_    UINT       *pClusterIDs,
  _In_    LPD3DXMESH pScene,
  _In_    UINT       MaxNumClusters,
  _In_    UINT       NumClusters,
  _Inout_ UINT       *pSClusterIDs,
  _Inout_ UINT       *pNumSCs
);
```



## <a name="parameters"></a><span data-ttu-id="562a0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="562a0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="562a0-109">*pClusterIDs* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="562a0-109">*pClusterIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="562a0-110">Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="562a0-110">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="562a0-111">Puntatore a un ID cluster NumVerts (estratto da un buffer compresso).</span><span class="sxs-lookup"><span data-stu-id="562a0-111">Pointer to a NumVerts cluster IDs (extracted from a compressed buffer.)</span></span>

</dd> <dt>

<span data-ttu-id="562a0-112">*pScene* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="562a0-112">*pScene* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="562a0-113">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="562a0-113">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="562a0-114">Puntatore a una mesh che rappresenta la scena composita passata al simulatore.</span><span class="sxs-lookup"><span data-stu-id="562a0-114">Pointer to a mesh that represents composite scene passed to the simulator.</span></span> <span data-ttu-id="562a0-115">Vedere [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="562a0-115">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="562a0-116">*MaxNumClusters* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="562a0-116">*MaxNumClusters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="562a0-117">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="562a0-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="562a0-118">Numero massimo di cluster allocati per cluster super.</span><span class="sxs-lookup"><span data-stu-id="562a0-118">Maximum number of clusters allocated per super cluster.</span></span>

</dd> <dt>

<span data-ttu-id="562a0-119">*NumCluster* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="562a0-119">*NumClusters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="562a0-120">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="562a0-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="562a0-121">Numero di cluster calcolati nel simulatore.</span><span class="sxs-lookup"><span data-stu-id="562a0-121">Number of clusters computed in the simulator.</span></span>

</dd> <dt>

<span data-ttu-id="562a0-122">*pSClusterIDs* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="562a0-122">*pSClusterIDs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="562a0-123">Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="562a0-123">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="562a0-124">Puntatore a una matrice di *lunghezza NumClusters*.</span><span class="sxs-lookup"><span data-stu-id="562a0-124">Pointer to an array of length *NumClusters*.</span></span> <span data-ttu-id="562a0-125">Contiene l'indice del super cluster a cui è stato assegnato il cluster corrispondente.</span><span class="sxs-lookup"><span data-stu-id="562a0-125">Contains the index of the super cluster to which the corresponding cluster was assigned.</span></span>

</dd> <dt>

<span data-ttu-id="562a0-126">*pNumSCs* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="562a0-126">*pNumSCs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="562a0-127">Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="562a0-127">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="562a0-128">Numero di super cluster allocati.</span><span class="sxs-lookup"><span data-stu-id="562a0-128">Number of super clusters allocated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="562a0-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="562a0-129">Return value</span></span>

<span data-ttu-id="562a0-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="562a0-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="562a0-131">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="562a0-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="562a0-132">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="562a0-132">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="562a0-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="562a0-133">Requirements</span></span>



| <span data-ttu-id="562a0-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="562a0-134">Requirement</span></span> | <span data-ttu-id="562a0-135">Valore</span><span class="sxs-lookup"><span data-stu-id="562a0-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="562a0-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="562a0-136">Header</span></span><br/>  | <dl> <span data-ttu-id="562a0-137"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="562a0-137"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="562a0-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="562a0-138">Library</span></span><br/> | <dl> <span data-ttu-id="562a0-139"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="562a0-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="562a0-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="562a0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="562a0-141">Funzioni di trasferimento di radiance pre-ricalcolate</span><span class="sxs-lookup"><span data-stu-id="562a0-141">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
