---
description: Salda insieme i vertici replicati con attributi uguali. Questo metodo usa i valori Epsilon specificati per i confronti di uguaglianza.
ms.assetid: bddf6e0c-55a1-40d2-8681-e7f0f9002bfa
title: Funzione D3DXWeldVertices (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXWeldVertices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 76e0a6f259bc8ba547a02b2e95cccf718d54e904
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762083"
---
# <a name="d3dxweldvertices-function"></a><span data-ttu-id="07728-104">D3DXWeldVertices (funzione)</span><span class="sxs-lookup"><span data-stu-id="07728-104">D3DXWeldVertices function</span></span>

<span data-ttu-id="07728-105">Salda insieme i vertici replicati con attributi uguali.</span><span class="sxs-lookup"><span data-stu-id="07728-105">Welds together replicated vertices that have equal attributes.</span></span> <span data-ttu-id="07728-106">Questo metodo usa i valori Epsilon specificati per i confronti di uguaglianza.</span><span class="sxs-lookup"><span data-stu-id="07728-106">This method uses specified epsilon values for equality comparisons.</span></span>

## <a name="syntax"></a><span data-ttu-id="07728-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07728-107">Syntax</span></span>


```C++
HRESULT D3DXWeldVertices(
  _In_          LPD3DXMESH       pMesh,
  _In_          DWORD            Flags,
  _In_    const D3DXWeldEpsilons *pEpsilons,
  _In_    const DWORD            *pAdjacencyIn,
  _Inout_       DWORD            *pAdjacencyOut,
  _Out_         DWORD            *pFaceRemap,
  _Out_         LPD3DXBUFFER     *ppVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="07728-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="07728-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07728-109">*pMesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="07728-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07728-110">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="07728-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="07728-111">Puntatore a un oggetto [**ID3DXMesh**](id3dxmesh.md) , mesh da cui si saldano i vertici.</span><span class="sxs-lookup"><span data-stu-id="07728-111">Pointer to an [**ID3DXMesh**](id3dxmesh.md) object, the mesh from which to weld vertices.</span></span>

</dd> <dt>

<span data-ttu-id="07728-112">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="07728-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07728-113">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07728-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="07728-114">Combinazione di uno o più flag di [**D3DXWELDEPSILONSFLAGS**](./d3dxweldepsilonsflags.md).</span><span class="sxs-lookup"><span data-stu-id="07728-114">Combination of one or more flags from [**D3DXWELDEPSILONSFLAGS**](./d3dxweldepsilonsflags.md).</span></span>

</dd> <dt>

<span data-ttu-id="07728-115">*pEpsilons* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="07728-115">*pEpsilons* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07728-116">Tipo: **const [**D3DXWeldEpsilons**](d3dxweldepsilons.md) \***</span><span class="sxs-lookup"><span data-stu-id="07728-116">Type: **const [**D3DXWeldEpsilons**](d3dxweldepsilons.md)\***</span></span>

<span data-ttu-id="07728-117">Puntatore a una struttura [**D3DXWeldEpsilons**](d3dxweldepsilons.md) , che specifica i valori Epsilon da usare per questo metodo.</span><span class="sxs-lookup"><span data-stu-id="07728-117">Pointer to a [**D3DXWeldEpsilons**](d3dxweldepsilons.md) structure, specifying the epsilon values to be used for this method.</span></span> <span data-ttu-id="07728-118">Utilizzare **null** per inizializzare tutti i membri della struttura sul valore predefinito 1.0 e-6F.</span><span class="sxs-lookup"><span data-stu-id="07728-118">Use **NULL** to initialize all structure members to a default value of 1.0e-6f.</span></span>

</dd> <dt>

<span data-ttu-id="07728-119">*pAdjacencyIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="07728-119">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07728-120">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="07728-120">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="07728-121">Puntatore a una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh di origine.</span><span class="sxs-lookup"><span data-stu-id="07728-121">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the source mesh.</span></span> <span data-ttu-id="07728-122">Se il bordo non ha visi adiacenti, il valore è 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="07728-122">If the edge has no adjacent faces, the value is 0xffffffff.</span></span> <span data-ttu-id="07728-123">Se questo parametro è impostato su **null**, viene chiamato [**ID3DXBaseMesh:: GenerateAdjacency**](id3dxbasemesh--generateadjacency.md) per creare informazioni adiacenza logiche.</span><span class="sxs-lookup"><span data-stu-id="07728-123">If this parameter is set to **NULL**, [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md) will be called to create logical adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="07728-124">*pAdjacencyOut* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="07728-124">*pAdjacencyOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="07728-125">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="07728-125">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="07728-126">Puntatore a una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh ottimizzata.</span><span class="sxs-lookup"><span data-stu-id="07728-126">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the optimized mesh.</span></span> <span data-ttu-id="07728-127">Se il bordo non ha visi adiacenti, il valore è 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="07728-127">If the edge has no adjacent faces, the value is 0xffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="07728-128">*pFaceRemap* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="07728-128">*pFaceRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07728-129">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="07728-129">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="07728-130">Matrice di DWORD, una per ogni volto, che identifica la faccia mesh originale che corrisponde a ogni face nella rete elettrosaldata.</span><span class="sxs-lookup"><span data-stu-id="07728-130">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the welded mesh.</span></span>

</dd> <dt>

<span data-ttu-id="07728-131">*ppVertexRemap* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="07728-131">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07728-132">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="07728-132">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="07728-133">Indirizzo di un puntatore a un'interfaccia [**ID3DXBuffer**](id3dxbuffer.md) , che contiene un valore DWORD per ogni vertice che specifica la modalità di mapping dei nuovi vertici ai vertici precedenti.</span><span class="sxs-lookup"><span data-stu-id="07728-133">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="07728-134">Questo mapping è utile se è necessario modificare i dati esterni in base al nuovo mapping dei vertici.</span><span class="sxs-lookup"><span data-stu-id="07728-134">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07728-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="07728-135">Return value</span></span>

<span data-ttu-id="07728-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="07728-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="07728-137">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="07728-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="07728-138">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="07728-138">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="07728-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="07728-139">Remarks</span></span>

<span data-ttu-id="07728-140">Questa funzione utilizza le informazioni adiacenza fornite per determinare i punti replicati.</span><span class="sxs-lookup"><span data-stu-id="07728-140">This function uses supplied adjacency information to determine the points that are replicated.</span></span> <span data-ttu-id="07728-141">I vertici vengono uniti in base a un confronto Epsilon.</span><span class="sxs-lookup"><span data-stu-id="07728-141">Vertices are merged based on an epsilon comparison.</span></span> <span data-ttu-id="07728-142">I vertici con posizione uguale devono essere già stati calcolati e rappresentati da dati rappresentativi del punto.</span><span class="sxs-lookup"><span data-stu-id="07728-142">Vertices with equal position must already have been calculated and represented by point-representative data.</span></span>

<span data-ttu-id="07728-143">Questa funzione combina i vertici a saldatura logica con componenti simili, ad esempio normali o coordinate di trama all'interno di pEpsilons.</span><span class="sxs-lookup"><span data-stu-id="07728-143">This function combines logically-welded vertices that have similar components, such as normals or texture coordinates within pEpsilons.</span></span>

<span data-ttu-id="07728-144">Il codice di esempio seguente chiama questa funzione con la saldatura abilitata.</span><span class="sxs-lookup"><span data-stu-id="07728-144">The following example code calls this function with welding enabled.</span></span> <span data-ttu-id="07728-145">I vertici vengono confrontati usando i valori Epsilon per la posizione del vettore e del vertice normali.</span><span class="sxs-lookup"><span data-stu-id="07728-145">Vertices are compared using epsilon values for normal vector and vertex position.</span></span> <span data-ttu-id="07728-146">Un puntatore viene restituito a una matrice di rimapping visi (*pFaceRemap*).</span><span class="sxs-lookup"><span data-stu-id="07728-146">A pointer is returned to a face remapping array (*pFaceRemap*).</span></span>


```
TCHAR            strMediaPath[512];       // X-file path 
LPD3DXBUFFER     pAdjacencyBuffer = NULL; // adjacency data buffer
LPD3DXBUFFER     pD3DXMtrlBuffer  = NULL; // material buffer
LPD3DXMESH       pMesh            = NULL; // mesh object
DWORD            m_dwNumMaterials;        // number of materials
D3DXWELDEPSILONS Epsilons;                // structure with epsilon values
DWORD            *pFaceRemap[65536];      // face remapping array
DWORD            i;                       // internal variable
    
    // Load the mesh from the specified file
    hr = D3DXLoadMeshFromX ( strMediaPath,
                         D3DXMESH_MANAGED,
                         m_pd3dDevice,
                         &pAdjacencyBuffer,
                         &pD3DXMtrlBuffer,
                         NULL,
                         &m_dwNumMaterials,
                         &pMesh ) )
                             
    if( FAILED( hr ) ) 
      goto End;              // Go to error handling
    
    // Set epsilon values
    Epsilons.Normal = 0.001;
    Epsilons.Position = 0.1;
    
    // Weld the vertices
    for( i=0; i < 65536; i++ )
    { 
        pFaceRemap[i] = 0; 
    }
    
    hr = D3DXWeldVertices ( pMesh,
                            D3DXWELDEPSILONS_WELDPARTIALMATCHES,
                            &Epsilons,
                            (DWORD*)pAdjacencyBuffer->GetBufferPointer(),
                            (DWORD*)pAdjacencyBuffer->GetBufferPointer(),
                            (DWORD*)pFaceRemap,
                            NULL )
                            
    if( FAILED( hr ) ) 
      goto End;              // Go to error handling
```



## <a name="requirements"></a><span data-ttu-id="07728-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07728-147">Requirements</span></span>



| <span data-ttu-id="07728-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="07728-148">Requirement</span></span> | <span data-ttu-id="07728-149">Valore</span><span class="sxs-lookup"><span data-stu-id="07728-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07728-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="07728-150">Header</span></span><br/>  | <dl> <span data-ttu-id="07728-151"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="07728-151"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="07728-152">Libreria</span><span class="sxs-lookup"><span data-stu-id="07728-152">Library</span></span><br/> | <dl> <span data-ttu-id="07728-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07728-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="07728-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07728-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07728-155">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="07728-155">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
