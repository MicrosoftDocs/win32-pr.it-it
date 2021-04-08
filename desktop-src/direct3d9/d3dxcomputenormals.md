---
description: Calcola le normali unità per ogni vertice in una rete mesh. Fornito per supportare le applicazioni legacy. Usare D3DXComputeTangentFrameEx per ottenere risultati migliori.
ms.assetid: 7c879149-2c4c-4824-9604-e88696cc6ddc
title: Funzione D3DXComputeNormals (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeNormals
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3f95e5e353c318429f5340d1a831f9ca3050ba3c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969406"
---
# <a name="d3dxcomputenormals-function"></a><span data-ttu-id="087e2-105">D3DXComputeNormals (funzione)</span><span class="sxs-lookup"><span data-stu-id="087e2-105">D3DXComputeNormals function</span></span>

<span data-ttu-id="087e2-106">Calcola le normali unità per ogni vertice in una rete mesh.</span><span class="sxs-lookup"><span data-stu-id="087e2-106">Computes unit normals for each vertex in a mesh.</span></span> <span data-ttu-id="087e2-107">Fornito per supportare le applicazioni legacy.</span><span class="sxs-lookup"><span data-stu-id="087e2-107">Provided to support legacy applications.</span></span> <span data-ttu-id="087e2-108">Usare [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) per ottenere risultati migliori.</span><span class="sxs-lookup"><span data-stu-id="087e2-108">Use [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) for better results.</span></span>

## <a name="syntax"></a><span data-ttu-id="087e2-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="087e2-109">Syntax</span></span>


```C++
HRESULT D3DXComputeNormals(
  _Inout_       LPD3DXBASEMESH pMesh,
  _In_    const DWORD          *pAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="087e2-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="087e2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="087e2-111">*pMesh* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="087e2-111">*pMesh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="087e2-112">Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="087e2-112">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="087e2-113">Puntatore a un'interfaccia [**ID3DXBaseMesh**](id3dxbasemesh.md) , che rappresenta l'oggetto mesh normalizzato.</span><span class="sxs-lookup"><span data-stu-id="087e2-113">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) interface, representing the normalized mesh object.</span></span>

</dd> <dt>

<span data-ttu-id="087e2-114">*pAdjacency* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="087e2-114">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="087e2-115">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="087e2-115">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="087e2-116">Puntatore a una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella rete progressiva creata.</span><span class="sxs-lookup"><span data-stu-id="087e2-116">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the created progressive mesh.</span></span> <span data-ttu-id="087e2-117">Questo parametro è facoltativo e deve essere impostato su **null** se non è usato.</span><span class="sxs-lookup"><span data-stu-id="087e2-117">This parameter is optional and should be set to **NULL** if it is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="087e2-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="087e2-118">Return value</span></span>

<span data-ttu-id="087e2-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="087e2-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="087e2-120">Se la funzione ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="087e2-120">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="087e2-121">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="087e2-121">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="087e2-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="087e2-122">Remarks</span></span>

<span data-ttu-id="087e2-123">Per la mesh di input deve essere specificato il flag [D3DFVF \_ Normal](d3dfvf.md) nel formato di vertice flessibile (FVF).</span><span class="sxs-lookup"><span data-stu-id="087e2-123">The input mesh must have the [D3DFVF\_NORMAL](d3dfvf.md) flag specified in its flexible vertex format (FVF).</span></span>

<span data-ttu-id="087e2-124">Un normale per un vertice viene generato calcolando la media dei normali di tutti i visi che condividono tale vertice.</span><span class="sxs-lookup"><span data-stu-id="087e2-124">A normal for a vertex is generated by averaging the normals of all faces that share that vertex.</span></span>

<span data-ttu-id="087e2-125">Se viene specificato adiacenza, i vertici replicati vengono ignorati e "smussati".</span><span class="sxs-lookup"><span data-stu-id="087e2-125">If adjacency is provided, replicated vertices are ignored and "smoothed" over.</span></span> <span data-ttu-id="087e2-126">Se adiacenza non viene specificato, i vertici replicati avranno le normali medie in solo dai visi che vi fanno riferimento in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="087e2-126">If adjacency is not provided, replicated vertices will have normals averaged in from only the faces explicitly referencing them.</span></span>

<span data-ttu-id="087e2-127">Questa funzione chiama semplicemente [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) con i parametri di input seguenti:</span><span class="sxs-lookup"><span data-stu-id="087e2-127">This function simply calls [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) with the following input parameters:</span></span>


```
D3DXComputeTangentFrameEx( pMesh,
                           D3DX_DEFAULT,
                           0,
                           D3DX_DEFAULT,
                           0,
                           D3DX_DEFAULT,
                           0,
                           D3DDECLUSAGE_NORMAL,
                           0,
                           D3DXTANGENT_GENERATE_IN_PLACE | D3DXTANGENT_CALCULATE_NORMALS,
                           pAdjacency,
                           -1.01f,
                           -0.01f,
                           -1.01f,
                           NULL,
                           NULL);
```



## <a name="requirements"></a><span data-ttu-id="087e2-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="087e2-128">Requirements</span></span>



| <span data-ttu-id="087e2-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="087e2-129">Requirement</span></span> | <span data-ttu-id="087e2-130">Valore</span><span class="sxs-lookup"><span data-stu-id="087e2-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="087e2-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="087e2-131">Header</span></span><br/>  | <dl> <span data-ttu-id="087e2-132"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="087e2-132"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="087e2-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="087e2-133">Library</span></span><br/> | <dl> <span data-ttu-id="087e2-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="087e2-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="087e2-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="087e2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="087e2-136">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="087e2-136">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
