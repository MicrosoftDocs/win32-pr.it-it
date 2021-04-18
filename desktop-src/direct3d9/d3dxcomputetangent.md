---
description: Calcola i vettori tangenti per le coordinate di trama specificate nella fase della trama. Fornito per supportare le applicazioni legacy. Usare D3DXComputeTangentFrameEx per ottenere risultati migliori.
ms.assetid: 39748459-3f9b-4b48-ae13-7143eb29c292
title: Funzione D3DXComputeTangent (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangent
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5cdb6a9dae3bdbad0f239fa61ba066d7b1bffb14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322613"
---
# <a name="d3dxcomputetangent-function"></a><span data-ttu-id="a1535-105">D3DXComputeTangent (funzione)</span><span class="sxs-lookup"><span data-stu-id="a1535-105">D3DXComputeTangent function</span></span>

<span data-ttu-id="a1535-106">Calcola i vettori tangenti per le coordinate di trama specificate nella fase della trama.</span><span class="sxs-lookup"><span data-stu-id="a1535-106">Computes the tangent vectors for the texture coordinates given in the texture stage.</span></span> <span data-ttu-id="a1535-107">Fornito per supportare le applicazioni legacy.</span><span class="sxs-lookup"><span data-stu-id="a1535-107">Provided to support legacy applications.</span></span> <span data-ttu-id="a1535-108">Usare [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) per ottenere risultati migliori.</span><span class="sxs-lookup"><span data-stu-id="a1535-108">Use [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) for better results.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1535-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a1535-109">Syntax</span></span>


```C++
HRESULT D3DXComputeTangent(
  _In_       LPD3DXMESH Mesh,
  _In_       DWORD      TexStageIndex,
  _In_       DWORD      TangentIndex,
  _In_       DWORD      BinormIndex,
  _In_       DWORD      Wrap,
  _In_ const DWORD      *pAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="a1535-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="a1535-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1535-111">*Mesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1535-111">*Mesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1535-112">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="a1535-112">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="a1535-113">Puntatore a un'interfaccia [**ID3DXMesh**](id3dxmesh.md) che rappresenta la mesh di input.</span><span class="sxs-lookup"><span data-stu-id="a1535-113">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface that represent the input mesh.</span></span>

</dd> <dt>

<span data-ttu-id="a1535-114">*TexStageIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1535-114">*TexStageIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1535-115">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1535-115">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a1535-116">Indice che rappresenta la fase della trama.</span><span class="sxs-lookup"><span data-stu-id="a1535-116">Index that represents the texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="a1535-117">*TangentIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1535-117">*TangentIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1535-118">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1535-118">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a1535-119">Indice che fornisce l'indice di utilizzo per i dati della tangente.</span><span class="sxs-lookup"><span data-stu-id="a1535-119">Index that provides the usage index for the tangent data.</span></span> <span data-ttu-id="a1535-120">La dichiarazione di vertice implica l'utilizzo. Questo indice modifica l'utilizzo con l'indice Usage.</span><span class="sxs-lookup"><span data-stu-id="a1535-120">The vertex declaration implies the usage; this index modifies the usage with the usage index.</span></span> <span data-ttu-id="a1535-121">Per ulteriori informazioni sulla dichiarazione di un vertice, vedere [dichiarazione di vertici (Direct3D 9)](vertex-declaration.md).</span><span class="sxs-lookup"><span data-stu-id="a1535-121">For more information about a vertex declaration, see [Vertex Declaration (Direct3D 9)](vertex-declaration.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1535-122">*BinormIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1535-122">*BinormIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1535-123">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1535-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a1535-124">Indice che fornisce l'indice di utilizzo per i dati binormali.</span><span class="sxs-lookup"><span data-stu-id="a1535-124">Index that provides the usage index for the binormal data.</span></span> <span data-ttu-id="a1535-125">La dichiarazione di vertice implica l'utilizzo. Questo indice modifica l'utilizzo con l'indice Usage.</span><span class="sxs-lookup"><span data-stu-id="a1535-125">The vertex declaration implies the usage; this index modifies the usage with the usage index.</span></span> <span data-ttu-id="a1535-126">Per ulteriori informazioni sulla dichiarazione di un vertice, vedere [dichiarazione di vertici (Direct3D 9)](vertex-declaration.md).</span><span class="sxs-lookup"><span data-stu-id="a1535-126">For more information about a vertex declaration, see [Vertex Declaration (Direct3D 9)](vertex-declaration.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1535-127">A *capo automatico* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1535-127">*Wrap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1535-128">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1535-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a1535-129">Impostare questo valore su 0 per nessun ritorno a capo o su 1 per il wrapping nelle direzioni u e V.</span><span class="sxs-lookup"><span data-stu-id="a1535-129">Set this value to 0 for no wrapping, or to 1 for wrapping in the U and V directions.</span></span>

</dd> <dt>

<span data-ttu-id="a1535-130">*pAdjacency* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1535-130">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1535-131">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="a1535-131">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a1535-132">Puntatore a una matrice di tre DWORD per ogni volto da riempire con indici facciali adiacenti.</span><span class="sxs-lookup"><span data-stu-id="a1535-132">Pointer to an array of three DWORDs per face to be filled with adjacent face indices.</span></span> <span data-ttu-id="a1535-133">Il numero di byte in questa matrice deve essere almeno ((3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)) \* sizeof (DWORD)).</span><span class="sxs-lookup"><span data-stu-id="a1535-133">The number of bytes in this array must be at least ((3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)) \* sizeof(DWORD)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1535-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a1535-134">Return value</span></span>

<span data-ttu-id="a1535-135">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a1535-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a1535-136">Se la funzione ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a1535-136">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a1535-137">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="a1535-137">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1535-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="a1535-138">Remarks</span></span>

<span data-ttu-id="a1535-139">Se la dichiarazione del vertice mesh specifica i campi tangente o binormale, **D3DXComputeTangent** aggiornerà tutti i dati tangente o binormali specificati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="a1535-139">If the mesh vertex declaration specifies tangent or binormal fields, **D3DXComputeTangent** will update any user-supplied tangent or binormal data.</span></span> <span data-ttu-id="a1535-140">In alternativa, impostare TangentIndex su [D3DX \_ default](other-d3dx-constants.md) in modo da non aggiornare i dati della tangente specificati dall'utente oppure impostare BinormIndex su D3DX \_ default per non aggiornare i dati binormali forniti dall'utente.</span><span class="sxs-lookup"><span data-stu-id="a1535-140">Alternatively, set TangentIndex to [D3DX\_DEFAULT](other-d3dx-constants.md) to not update the user-supplied tangent data, or set BinormIndex to D3DX\_DEFAULT to not update the user-supplied binormal data.</span></span> <span data-ttu-id="a1535-141">Impossibile impostare TexStageIndex su D3DX \_ default.</span><span class="sxs-lookup"><span data-stu-id="a1535-141">TexStageIndex cannot be set to D3DX\_DEFAULT.</span></span>

<span data-ttu-id="a1535-142">**D3DXComputeTangent** dipende dalla dichiarazione del vertice mesh contenente il campo Binormal (BinormIndex), il campo tangente (TangentIndex) o entrambi.</span><span class="sxs-lookup"><span data-stu-id="a1535-142">**D3DXComputeTangent** depends on the mesh vertex declaration containing either the binormal field (BinormIndex), the tangent field (TangentIndex), or both.</span></span> <span data-ttu-id="a1535-143">In caso contrario, la funzione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="a1535-143">If both are missing, this function will fail.</span></span>

<span data-ttu-id="a1535-144">Questa funzione chiama semplicemente [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) con i parametri di input seguenti:</span><span class="sxs-lookup"><span data-stu-id="a1535-144">This function simply calls [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) with the following input parameters:</span></span>


```
D3DXComputeTangentFrameEx( Mesh,
                           D3DDECLUSAGE_TEXCOORD,
                           TexStageIndex,
                           ( BinormIndex == D3DX_DEFAULT ) ?
                               D3DX_DEFAULT : D3DDECLUSAGE_BINORMAL,
                               // provides backward function compatibility
                           BinormIndex,
                           ( TangentIndex == D3DX_DEFAULT ) ?
                               D3DX_DEFAULT : D3DDECLUSAGE_TANGENT,
                           TangentIndex,
                           D3DX_DEFAULT, // do not store normals
                           0,
                           ( Wrap ? D3DXTANGENT_WRAP_UV : 0 )
                               | D3DXTANGENT_GENERATE_IN_PLACE
                               | D3DXTANGENT_ORTHOGONALIZE_FROM_U,
                           pAdjacency,
                           -1.01f,
                           -0.01f,
                           -1.01f,
                           NULL,
                           NULL);
```



## <a name="requirements"></a><span data-ttu-id="a1535-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1535-145">Requirements</span></span>



| <span data-ttu-id="a1535-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1535-146">Requirement</span></span> | <span data-ttu-id="a1535-147">Valore</span><span class="sxs-lookup"><span data-stu-id="a1535-147">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1535-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a1535-148">Header</span></span><br/>  | <dl> <span data-ttu-id="a1535-149"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1535-149"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a1535-150">Libreria</span><span class="sxs-lookup"><span data-stu-id="a1535-150">Library</span></span><br/> | <dl> <span data-ttu-id="a1535-151"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1535-151"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a1535-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1535-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1535-153">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="a1535-153">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
