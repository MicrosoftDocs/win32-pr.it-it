---
description: Vettori di calcolo tangente, binormali e normali per una rete mesh.
ms.assetid: 54edb9a5-440d-4191-a58f-296e5b804e0c
title: Funzione D3DXComputeTangentFrame (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangentFrame
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4b95d8f046499716a2c7972593093dfb409b11f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323426"
---
# <a name="d3dxcomputetangentframe-function"></a><span data-ttu-id="b765a-103">D3DXComputeTangentFrame (funzione)</span><span class="sxs-lookup"><span data-stu-id="b765a-103">D3DXComputeTangentFrame function</span></span>

<span data-ttu-id="b765a-104">Vettori di calcolo tangente, binormali e normali per una rete mesh.</span><span class="sxs-lookup"><span data-stu-id="b765a-104">Compute tangent, binormal, and normal vectors for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="b765a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b765a-105">Syntax</span></span>


```C++
HRESULT D3DXComputeTangentFrame(
  _In_ ID3DXMesh *pMesh,
  _In_ DWORD     dwOptions
);
```



## <a name="parameters"></a><span data-ttu-id="b765a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b765a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b765a-107">*pMesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b765a-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b765a-108">Tipo: **[ **ID3DXMesh**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="b765a-108">Type: **[**ID3DXMesh**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="b765a-109">Puntatore a un oggetto mesh [**ID3DXMesh**](id3dxmesh.md) di input.</span><span class="sxs-lookup"><span data-stu-id="b765a-109">Pointer to an input [**ID3DXMesh**](id3dxmesh.md) mesh object.</span></span>

</dd> <dt>

<span data-ttu-id="b765a-110">*dwOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b765a-110">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b765a-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b765a-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b765a-112">Combinazione di uno o più flag [**D3DXTANGENT**](./d3dxtangent.md) .</span><span class="sxs-lookup"><span data-stu-id="b765a-112">Combination of one or more [**D3DXTANGENT**](./d3dxtangent.md) flags.</span></span>

<span data-ttu-id="b765a-113">Utilizzare **null** per specificare le opzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="b765a-113">Use **NULL** to specify the following options:</span></span>

-   <span data-ttu-id="b765a-114">Ponderare la lunghezza del vettore normale in base all'angolo, in radianti, in base ai due bordi che lasciano il vertice.</span><span class="sxs-lookup"><span data-stu-id="b765a-114">Weight the normal vector length by the angle, in radians, subtended by the two edges leaving the vertex.</span></span>
-   <span data-ttu-id="b765a-115">Calcola le coordinate cartesiane ortogonali dalle coordinate di trama UV.</span><span class="sxs-lookup"><span data-stu-id="b765a-115">Compute orthogonal Cartesian coordinates from the UV texture coordinates.</span></span>
-   <span data-ttu-id="b765a-116">Non è possibile eseguire il wrapper delle trame nelle direzioni U o V</span><span class="sxs-lookup"><span data-stu-id="b765a-116">Textures are not wrapped in either U or V directions</span></span>
-   <span data-ttu-id="b765a-117">Le derivazioni parziali rispetto alle coordinate di trama vengono normalizzate.</span><span class="sxs-lookup"><span data-stu-id="b765a-117">Partial derivatives with respect to texture coordinates are normalized.</span></span>
-   <span data-ttu-id="b765a-118">I vertici vengono ordinati in senso antiorario intorno a ogni triangolo.</span><span class="sxs-lookup"><span data-stu-id="b765a-118">Vertices are ordered in a counterclockwise direction around each triangle.</span></span>
-   <span data-ttu-id="b765a-119">Usare vettori normali per vertice già presenti nella mesh di input.</span><span class="sxs-lookup"><span data-stu-id="b765a-119">Use per-vertex normal vectors already present in the input mesh.</span></span>
-   <span data-ttu-id="b765a-120">I risultati verranno archiviati nella mesh di input originale.</span><span class="sxs-lookup"><span data-stu-id="b765a-120">The results will be stored in the original input mesh.</span></span> <span data-ttu-id="b765a-121">La funzione avrà esito negativo se è necessario creare nuovi vertici.</span><span class="sxs-lookup"><span data-stu-id="b765a-121">The function will fail if new vertices need to be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b765a-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b765a-122">Return value</span></span>

<span data-ttu-id="b765a-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b765a-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b765a-124">Se la funzione ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b765a-124">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b765a-125">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="b765a-125">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="b765a-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="b765a-126">Remarks</span></span>

<span data-ttu-id="b765a-127">Questa funzione chiama semplicemente [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) con i parametri di input seguenti:</span><span class="sxs-lookup"><span data-stu-id="b765a-127">This function simply calls [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) with the following input parameters:</span></span>


```
D3DXComputeTangentFrameEx(pMesh, D3DDECLUSAGE_TEXCOORD, 0,   
      D3DDECLUSAGE_BINORMAL, 0, D3DDECLUSAGE_TANGENT, 0, 
      D3DDECLUSAGE_NORMAL, 0, 
      dwOptions | D3DXTANGENT_GENERATE_IN_PLACE,
      NULL, 0.01f, 0.25f, 0.01f, NULL, NULL);
```



<span data-ttu-id="b765a-128">Le singolarità vengono gestite come richiesto raggruppando i bordi e suddividendo i vertici.</span><span class="sxs-lookup"><span data-stu-id="b765a-128">Singularities are handled as required by grouping edges and splitting vertices.</span></span> <span data-ttu-id="b765a-129">Se è necessario suddividere i vertici, la funzione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="b765a-129">If any vertices need to be split, the function will fail.</span></span> <span data-ttu-id="b765a-130">Il vettore normale calcolato a ogni vertice è sempre normalizzato per avere una lunghezza di unità.</span><span class="sxs-lookup"><span data-stu-id="b765a-130">The computed normal vector at each vertex is always normalized to have unit length.</span></span>

<span data-ttu-id="b765a-131">La soluzione più affidabile per calcolare le coordinate cartesiane ortogonali consiste nel non impostare i flag D3DXTANGENT \_ ORTHOGONALIZE \_ \_ e D3DXTANGENT \_ ORTHOGONALIZE \_ da \_ V, in modo che le coordinate ortogonali vengano calcolate da entrambe le coordinate di trama UV.</span><span class="sxs-lookup"><span data-stu-id="b765a-131">The most robust solution for computing orthogonal Cartesian coordinates is to not set flags D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U and D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V, so that orthogonal coordinates are computed from both UV texture coordinates.</span></span> <span data-ttu-id="b765a-132">Tuttavia, in questo caso, se U o V è zero, la funzione calcolerà le coordinate ortogonali usando D3DXTANGENT \_ ORTHOGONALIZE \_ \_ rispettivamente da V o D3DXTANGENT \_ ORTHOGONALIZE \_ from \_ U.</span><span class="sxs-lookup"><span data-stu-id="b765a-132">However, in this case, if either U or V is zero, then the function will compute orthogonal coordinates using D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V or D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="b765a-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b765a-133">Requirements</span></span>



| <span data-ttu-id="b765a-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="b765a-134">Requirement</span></span> | <span data-ttu-id="b765a-135">Valore</span><span class="sxs-lookup"><span data-stu-id="b765a-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b765a-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b765a-136">Header</span></span><br/>  | <dl> <span data-ttu-id="b765a-137"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b765a-137"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b765a-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="b765a-138">Library</span></span><br/> | <dl> <span data-ttu-id="b765a-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b765a-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b765a-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b765a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b765a-141">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="b765a-141">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="b765a-142">**D3DXComputeTangentFrameEx**</span><span class="sxs-lookup"><span data-stu-id="b765a-142">**D3DXComputeTangentFrameEx**</span></span>](d3dxcomputetangentframeex.md)
</dt> <dt>

[<span data-ttu-id="b765a-143">**D3DXTANGENT**</span><span class="sxs-lookup"><span data-stu-id="b765a-143">**D3DXTANGENT**</span></span>](./d3dxtangent.md)
</dt> </dl>

 

 
