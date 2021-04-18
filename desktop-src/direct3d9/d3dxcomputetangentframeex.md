---
description: Esegue calcoli del fotogramma tangente su una mesh. Vengono generati i vettori tangenti, binormali e facoltativamente normali. Le singolarità vengono gestite come richiesto raggruppando i bordi e suddividendo i vertici.
ms.assetid: 15cc46bc-6db6-4e1d-a95e-cd60d2666600
title: Funzione D3DXComputeTangentFrameEx (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangentFrameEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 58c7e8a1f1f7247d6a3ecc92d5771d68c9c3e5a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322318"
---
# <a name="d3dxcomputetangentframeex-function"></a><span data-ttu-id="084de-105">D3DXComputeTangentFrameEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="084de-105">D3DXComputeTangentFrameEx function</span></span>

<span data-ttu-id="084de-106">Esegue calcoli del fotogramma tangente su una mesh.</span><span class="sxs-lookup"><span data-stu-id="084de-106">Performs tangent frame computations on a mesh.</span></span> <span data-ttu-id="084de-107">Vengono generati i vettori tangenti, binormali e facoltativamente normali.</span><span class="sxs-lookup"><span data-stu-id="084de-107">Tangent, binormal, and optionally normal vectors are generated.</span></span> <span data-ttu-id="084de-108">Le singolarità vengono gestite come richiesto raggruppando i bordi e suddividendo i vertici.</span><span class="sxs-lookup"><span data-stu-id="084de-108">Singularities are handled as required by grouping edges and splitting vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="084de-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="084de-109">Syntax</span></span>


```C++
HRESULT D3DXComputeTangentFrameEx(
  _In_        ID3DXMesh   *pMesh,
  _In_        DWORD       dwTextureInSemantic,
  _In_        DWORD       dwTextureInIndex,
  _In_        DWORD       dwUPartialOutSemantic,
  _In_        DWORD       dwUPartialOutIndex,
  _In_        DWORD       dwVPartialOutSemantic,
  _In_        DWORD       dwVPartialOutIndex,
  _In_        DWORD       dwNormalOutSemantic,
  _In_        DWORD       dwNormalOutIndex,
  _In_        DWORD       dwOptions,
  _In_  const DWORD       *pdwAdjacency,
  _In_        FLOAT       fPartialEdgeThreshold,
  _In_        FLOAT       fSingularPointThreshold,
  _In_        FLOAT       fNormalEdgeThreshold,
  _Out_       ID3DXMesh   **ppMeshOut,
  _Out_       ID3DXBuffer **ppVertexMapping
);
```



## <a name="parameters"></a><span data-ttu-id="084de-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="084de-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="084de-111">*pMesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="084de-111">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="084de-112">Tipo: **[ **ID3DXMesh**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="084de-112">Type: **[**ID3DXMesh**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="084de-113">Puntatore a un oggetto mesh [**ID3DXMesh**](id3dxmesh.md) di input.</span><span class="sxs-lookup"><span data-stu-id="084de-113">Pointer to an input [**ID3DXMesh**](id3dxmesh.md) mesh object.</span></span>

</dd> <dt>

<span data-ttu-id="084de-114">*dwTextureInSemantic* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="084de-114">*dwTextureInSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="084de-115">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="084de-115">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="084de-116">Specifica la semantica di input delle coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="084de-116">Specifies the texture coordinate input semantic.</span></span> <span data-ttu-id="084de-117">Se D3DX \_ è impostato su default, la funzione presuppone che non esistano coordinate di trama e la funzione avrà esito negativo a meno che non venga specificato il normale calcolo vettoriale.</span><span class="sxs-lookup"><span data-stu-id="084de-117">If D3DX\_DEFAULT, the function assumes that there are no texture coordinates, and the function will fail unless normal vector calculation is specified.</span></span>

</dd> <dt>

<span data-ttu-id="084de-118">*dwTextureInIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="084de-118">*dwTextureInIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="084de-119">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="084de-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="084de-120">Se una mesh ha più coordinate di trama, specifica la coordinata di trama da usare per i calcoli del fotogramma tangente.</span><span class="sxs-lookup"><span data-stu-id="084de-120">If a mesh has multiple texture coordinates, specifies the texture coordinate to use for the tangent frame computations.</span></span> <span data-ttu-id="084de-121">Se è zero, la mesh dispone solo di una singola coordinata di trama.</span><span class="sxs-lookup"><span data-stu-id="084de-121">If zero, the mesh has only a single texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="084de-122">*dwUPartialOutSemantic* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="084de-122">*dwUPartialOutSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="084de-123">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="084de-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="084de-124">Specifica la semantica di output per il tipo, in genere D3DDECLUSAGE \_ tangente, che descrive la posizione in cui verrà archiviata la derivata parziale rispetto alla coordinata di trama U.</span><span class="sxs-lookup"><span data-stu-id="084de-124">Specifies the output semantic for the type, typically D3DDECLUSAGE\_TANGENT, that describes where the partial derivative with respect to the U texture coordinate will be stored.</span></span> <span data-ttu-id="084de-125">Se D3DX \_ è impostato su default, questo derivato parziale non verrà archiviato.</span><span class="sxs-lookup"><span data-stu-id="084de-125">If D3DX\_DEFAULT, then this partial derivative will not be stored.</span></span>

</dd> <dt>

<span data-ttu-id="084de-126">*dwUPartialOutIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="084de-126">*dwUPartialOutIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="084de-127">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="084de-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="084de-128">Specifica l'indice semantico in cui archiviare la derivata parziale rispetto alla coordinata di trama U.</span><span class="sxs-lookup"><span data-stu-id="084de-128">Specifies the semantic index at which to store the partial derivative with respect to the U texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="084de-129">*dwVPartialOutSemantic* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="084de-129">*dwVPartialOutSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="084de-130">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="084de-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="084de-131">Specifica il tipo [**D3DDECLUSAGE**](./d3ddeclusage.md) , in genere D3DDECLUSAGE \_ Binormal, che descrive la posizione in cui verrà archiviata la derivata parziale rispetto alla coordinata di trama V.</span><span class="sxs-lookup"><span data-stu-id="084de-131">Specifies the [**D3DDECLUSAGE**](./d3ddeclusage.md) type, typically D3DDECLUSAGE\_BINORMAL, that describes where the partial derivative with respect to the V texture coordinate will be stored.</span></span> <span data-ttu-id="084de-132">Se D3DX \_ è impostato su default, questo derivato parziale non verrà archiviato.</span><span class="sxs-lookup"><span data-stu-id="084de-132">If D3DX\_DEFAULT, then this partial derivative will not be stored.</span></span>

</dd> <dt>

<span data-ttu-id="084de-133">*dwVPartialOutIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="084de-133">*dwVPartialOutIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="084de-134">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="084de-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="084de-135">Specifica l'indice semantico in cui archiviare la derivata parziale rispetto alla coordinata di trama V.</span><span class="sxs-lookup"><span data-stu-id="084de-135">Specifies the semantic index at which to store the partial derivative with respect to the V texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="084de-136">*dwNormalOutSemantic* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="084de-136">*dwNormalOutSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="084de-137">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="084de-137">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="084de-138">Specifica la semantica normale di output, in genere D3DDECLUSAGE \_ normale, che descrive la posizione in cui verrà archiviato il vettore normale in ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="084de-138">Specifies the output normal semantic, typically D3DDECLUSAGE\_NORMAL, that describes where the normal vector at each vertex will be stored.</span></span> <span data-ttu-id="084de-139">Se D3DX \_ è impostato su default, questo vettore normale non verrà archiviato.</span><span class="sxs-lookup"><span data-stu-id="084de-139">If D3DX\_DEFAULT, then this normal vector will not be stored.</span></span>

</dd> <dt>

<span data-ttu-id="084de-140">*dwNormalOutIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="084de-140">*dwNormalOutIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="084de-141">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="084de-141">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="084de-142">Specifica l'indice semantico in cui archiviare il vettore normale a ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="084de-142">Specifies the semantic index at which to store the normal vector at each vertex.</span></span>

</dd> <dt>

<span data-ttu-id="084de-143">*dwOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="084de-143">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="084de-144">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="084de-144">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="084de-145">Combinazione di uno o più flag [**D3DXTANGENT**](./d3dxtangent.md) che specificano le opzioni di calcolo del frame tangente.</span><span class="sxs-lookup"><span data-stu-id="084de-145">Combination of one or more [**D3DXTANGENT**](./d3dxtangent.md) flags that specify tangent frame computation options.</span></span> <span data-ttu-id="084de-146">Se **null**, verranno specificate le opzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="084de-146">If **NULL**, the following options will be specified:</span></span>



| <span data-ttu-id="084de-147">Descrizione</span><span class="sxs-lookup"><span data-stu-id="084de-147">Description</span></span>                                                                                              | <span data-ttu-id="084de-148">[**D3DXTANGENT**](./d3dxtangent.md) Valore del flag</span><span class="sxs-lookup"><span data-stu-id="084de-148">[**D3DXTANGENT**](./d3dxtangent.md) Flag Value</span></span>                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="084de-149">Ponderare la lunghezza del vettore normale in base all'angolo, in radianti, in base ai due bordi che lasciano il vertice.</span><span class="sxs-lookup"><span data-stu-id="084de-149">Weight the normal vector length by the angle, in radians, subtended by the two edges leaving the vertex.</span></span> | <span data-ttu-id="084de-150">&. (D3DXTANGENT \_ PESO \_ per \_ area \| D3DXTANGENT \_ peso \_ uguale)</span><span class="sxs-lookup"><span data-stu-id="084de-150">& !( D3DXTANGENT\_WEIGHT\_BY\_AREA \| D3DXTANGENT\_WEIGHT\_EQUAL )</span></span>                |
| <span data-ttu-id="084de-151">Calcola le coordinate cartesiane ortogonali dalle coordinate di trama (u, v).</span><span class="sxs-lookup"><span data-stu-id="084de-151">Compute orthogonal Cartesian coordinates from texture coordinates (u, v).</span></span> <span data-ttu-id="084de-152">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="084de-152">See Remarks.</span></span>                   | <span data-ttu-id="084de-153">&. (D3DXTANGENT \_ ORTHOGONALIZE \_ da \_ U \| D3DXTANGENT \_ ORTHOGONALIZE \_ from \_ V)</span><span class="sxs-lookup"><span data-stu-id="084de-153">& !( D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U \| D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V )</span></span> |
| <span data-ttu-id="084de-154">Non è possibile eseguire il wrapper delle trame nelle direzioni u o v</span><span class="sxs-lookup"><span data-stu-id="084de-154">Textures are not wrapped in either u or v directions</span></span>                                                     | <span data-ttu-id="084de-155">&. (D3DXTANGENT \_ a capo \_ UV)</span><span class="sxs-lookup"><span data-stu-id="084de-155">& !( D3DXTANGENT\_WRAP\_UV )</span></span>                                                      |
| <span data-ttu-id="084de-156">Le derivazioni parziali rispetto alle coordinate di trama vengono normalizzate.</span><span class="sxs-lookup"><span data-stu-id="084de-156">Partial derivatives with respect to texture coordinates are normalized.</span></span>                                  | <span data-ttu-id="084de-157">&. (D3DXTANGENT \_ non \_ normalizzare i \_ parziali)</span><span class="sxs-lookup"><span data-stu-id="084de-157">& !( D3DXTANGENT\_DONT\_NORMALIZE\_PARTIALS )</span></span>                                     |
| <span data-ttu-id="084de-158">I vertici vengono ordinati in senso antiorario intorno a ogni triangolo.</span><span class="sxs-lookup"><span data-stu-id="084de-158">Vertices are ordered in a counterclockwise direction around each triangle.</span></span>                               | <span data-ttu-id="084de-159">&. (D3DXTANGENT \_ \_CW vento)</span><span class="sxs-lookup"><span data-stu-id="084de-159">& !( D3DXTANGENT\_WIND\_CW )</span></span>                                                      |
| <span data-ttu-id="084de-160">Usare vettori normali per vertice già presenti nella mesh di input.</span><span class="sxs-lookup"><span data-stu-id="084de-160">Use per-vertex normal vectors already present in the input mesh.</span></span>                                         | <span data-ttu-id="084de-161">&. (D3DXTANGENT \_ Calcola \_ normali)</span><span class="sxs-lookup"><span data-stu-id="084de-161">& !( D3DXTANGENT\_CALCULATE\_NORMALS )</span></span>                                            |



 

<span data-ttu-id="084de-162">Se D3DXTANGENT \_ generate \_ sul \_ posto non è impostato, la mesh di input viene clonata.</span><span class="sxs-lookup"><span data-stu-id="084de-162">If D3DXTANGENT\_GENERATE\_IN\_PLACE is not set, the input mesh is cloned.</span></span> <span data-ttu-id="084de-163">La mesh originale deve quindi disporre di spazio sufficiente per archiviare il vettore normale calcolato e i dati parziali derivati.</span><span class="sxs-lookup"><span data-stu-id="084de-163">The original mesh must therefore have sufficient space to store the computed normal vector and partial derivative data.</span></span>

</dd> <dt>

<span data-ttu-id="084de-164">*pdwAdjacency* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="084de-164">*pdwAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="084de-165">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="084de-165">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="084de-166">Puntatore a una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh.</span><span class="sxs-lookup"><span data-stu-id="084de-166">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="084de-167">Il numero di byte in questa matrice deve essere almeno 3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD).</span><span class="sxs-lookup"><span data-stu-id="084de-167">The number of bytes in this array must be at least 3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).</span></span>

</dd> <dt>

<span data-ttu-id="084de-168">*fPartialEdgeThreshold* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="084de-168">*fPartialEdgeThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="084de-169">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="084de-169">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="084de-170">Specifica il coseno massimo dell'angolo in corrispondenza del quale due derivati parziali sono considerati incompatibili tra loro.</span><span class="sxs-lookup"><span data-stu-id="084de-170">Specifies the maximum cosine of the angle at which two partial derivatives are deemed to be incompatible with each other.</span></span> <span data-ttu-id="084de-171">Se il prodotto punto della direzione dei due derivati parziali nei triangoli adiacenti è minore o uguale a questa soglia, i vertici condivisi tra questi triangoli verranno divisi.</span><span class="sxs-lookup"><span data-stu-id="084de-171">If the dot product of the direction of the two partial derivatives in adjacent triangles is less than or equal to this threshold, then the vertices shared between these triangles will be split.</span></span>

</dd> <dt>

<span data-ttu-id="084de-172">*fSingularPointThreshold* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="084de-172">*fSingularPointThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="084de-173">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="084de-173">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="084de-174">Specifica la grandezza massima di una derivata parziale in corrispondenza della quale un vertice verrà considerato singolare.</span><span class="sxs-lookup"><span data-stu-id="084de-174">Specifies the maximum magnitude of a partial derivative at which a vertex will be deemed singular.</span></span> <span data-ttu-id="084de-175">Poiché più triangoli sono un evento imprevisto in un punto in cui sono presenti frame tangente adiacenti, ma si annulla completamente l'uno dall'altro (ad esempio, nella parte superiore di una sfera), la grandezza della derivata parziale diminuirà.</span><span class="sxs-lookup"><span data-stu-id="084de-175">As multiple triangles are incident on a point that have nearby tangent frames, but altogether cancel each other out (such as at the top of a sphere), the magnitude of the partial derivative will decrease.</span></span> <span data-ttu-id="084de-176">Se la grandezza è minore o uguale a questa soglia, il vertice verrà diviso per ogni triangolo che lo contiene.</span><span class="sxs-lookup"><span data-stu-id="084de-176">If the magnitude is less than or equal to this threshold, then the vertex will be split for every triangle that contains it.</span></span>

</dd> <dt>

<span data-ttu-id="084de-177">*fNormalEdgeThreshold* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="084de-177">*fNormalEdgeThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="084de-178">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="084de-178">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="084de-179">Analogamente a fPartialEdgeThreshold, specifica il coseno massimo dell'angolo tra due normali che rappresenta una soglia oltre la quale i vertici condivisi tra triangoli verranno divisi.</span><span class="sxs-lookup"><span data-stu-id="084de-179">Similar to fPartialEdgeThreshold, specifies the maximum cosine of the angle between two normals that is a threshold beyond which vertices shared between triangles will be split.</span></span> <span data-ttu-id="084de-180">Se il prodotto dot delle due normali è inferiore alla soglia, i vertici condivisi verranno suddivisi, formando un bordo rigido tra triangoli adiacenti.</span><span class="sxs-lookup"><span data-stu-id="084de-180">If the dot product of the two normals is less than the threshold, the shared vertices will be split, forming a hard edge between neighboring triangles.</span></span> <span data-ttu-id="084de-181">Se il prodotto punto è superiore alla soglia, i triangoli adiacenti avranno le normali interpolate.</span><span class="sxs-lookup"><span data-stu-id="084de-181">If the dot product is more than the threshold, neighboring triangles will have their normals interpolated.</span></span>

</dd> <dt>

<span data-ttu-id="084de-182">*ppMeshOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="084de-182">*ppMeshOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="084de-183">Tipo: **[ **ID3DXMesh**](id3dxmesh.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="084de-183">Type: **[**ID3DXMesh**](id3dxmesh.md)\*\***</span></span>

<span data-ttu-id="084de-184">Indirizzo di un puntatore a un oggetto mesh [**ID3DXMesh**](id3dxmesh.md) di output che riceve i dati di vettore di tangente, binormali e normali calcolati.</span><span class="sxs-lookup"><span data-stu-id="084de-184">Address of a pointer to an output [**ID3DXMesh**](id3dxmesh.md) mesh object that receives the computed tangent, binormal, and normal vector data.</span></span>

</dd> <dt>

<span data-ttu-id="084de-185">*ppVertexMapping* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="084de-185">*ppVertexMapping* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="084de-186">Tipo: **[ **ID3DXBuffer**](id3dxbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="084de-186">Type: **[**ID3DXBuffer**](id3dxbuffer.md)\*\***</span></span>

<span data-ttu-id="084de-187">Indirizzo di un puntatore a un oggetto buffer [**ID3DXBuffer**](id3dxbuffer.md) di output che riceve un mapping dei nuovi vertici calcolati da questo metodo ai vertici originali.</span><span class="sxs-lookup"><span data-stu-id="084de-187">Address of a pointer to an output [**ID3DXBuffer**](id3dxbuffer.md) buffer object that receives a mapping of new vertices computed by this method to the original vertices.</span></span> <span data-ttu-id="084de-188">Il buffer è una matrice di DWORD, con le dimensioni della matrice definite come numero di vertici in ppMeshOut.</span><span class="sxs-lookup"><span data-stu-id="084de-188">The buffer is an array of DWORDs, with the array size defined as the number of vertices in ppMeshOut.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="084de-189">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="084de-189">Return value</span></span>

<span data-ttu-id="084de-190">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="084de-190">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="084de-191">Se la funzione ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="084de-191">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="084de-192">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="084de-192">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="084de-193">Commenti</span><span class="sxs-lookup"><span data-stu-id="084de-193">Remarks</span></span>

<span data-ttu-id="084de-194">Una versione semplificata di questa funzione è disponibile come [**D3DXComputeTangentFrame**](d3dxcomputetangentframe.md).</span><span class="sxs-lookup"><span data-stu-id="084de-194">A simplified version of this function is available as [**D3DXComputeTangentFrame**](d3dxcomputetangentframe.md).</span></span>

<span data-ttu-id="084de-195">Il vettore normale calcolato a ogni vertice è sempre normalizzato per avere una lunghezza di unità.</span><span class="sxs-lookup"><span data-stu-id="084de-195">The computed normal vector at each vertex is always normalized to have unit length.</span></span>

<span data-ttu-id="084de-196">La soluzione più affidabile per calcolare le coordinate cartesiane ortogonali consiste nel non impostare i flag D3DXTANGENT \_ ORTHOGONALIZE \_ \_ e D3DXTANGENT \_ ORTHOGONALIZE \_ da \_ V, in modo che le coordinate ortogonali vengano calcolate da entrambe le coordinate di trama e V.</span><span class="sxs-lookup"><span data-stu-id="084de-196">The most robust solution for computing orthogonal Cartesian coordinates is to not set flags D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U and D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V, so that orthogonal coordinates are computed from both texture coordinates u and v.</span></span> <span data-ttu-id="084de-197">Tuttavia, in questo caso, se u o v è zero, la funzione calcolerà le coordinate ortogonali usando D3DXTANGENT \_ ORTHOGONALIZE \_ \_ rispettivamente da v o D3DXTANGENT \_ ORTHOGONALIZE \_ da \_ u.</span><span class="sxs-lookup"><span data-stu-id="084de-197">However, in this case, if either u or v is zero, then the function will compute orthogonal coordinates using D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V or D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="084de-198">Requisiti</span><span class="sxs-lookup"><span data-stu-id="084de-198">Requirements</span></span>



| <span data-ttu-id="084de-199">Requisito</span><span class="sxs-lookup"><span data-stu-id="084de-199">Requirement</span></span> | <span data-ttu-id="084de-200">Valore</span><span class="sxs-lookup"><span data-stu-id="084de-200">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="084de-201">Intestazione</span><span class="sxs-lookup"><span data-stu-id="084de-201">Header</span></span><br/>  | <dl> <span data-ttu-id="084de-202"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="084de-202"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="084de-203">Libreria</span><span class="sxs-lookup"><span data-stu-id="084de-203">Library</span></span><br/> | <dl> <span data-ttu-id="084de-204"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="084de-204"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="084de-205">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="084de-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="084de-206">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="084de-206">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="084de-207">**D3DXComputeTangentFrame**</span><span class="sxs-lookup"><span data-stu-id="084de-207">**D3DXComputeTangentFrame**</span></span>](d3dxcomputetangentframe.md)
</dt> </dl>

 

 
