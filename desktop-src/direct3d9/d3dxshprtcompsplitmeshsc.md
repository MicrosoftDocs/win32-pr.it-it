---
description: Usato con i risultati compressi della versione Vertex del simulatore di trasferimento di luminosità pre-calcolata (PRT).
ms.assetid: 10d81920-2a1b-42fa-aabe-7d6b504f4d36
title: Funzione D3DXSHPRTCompSplitMeshSC (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTCompSplitMeshSC
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 18742d12b6e1ae106dcf832baccccb2416465880
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401948"
---
# <a name="d3dxshprtcompsplitmeshsc-function"></a><span data-ttu-id="78d1d-103">D3DXSHPRTCompSplitMeshSC (funzione)</span><span class="sxs-lookup"><span data-stu-id="78d1d-103">D3DXSHPRTCompSplitMeshSC function</span></span>

<span data-ttu-id="78d1d-104">Usato con i risultati compressi della versione Vertex del simulatore di trasferimento di luminosità pre-calcolata (PRT).</span><span class="sxs-lookup"><span data-stu-id="78d1d-104">Used with compressed results of the vertex version of the precomputed radiance transfer (PRT) simulator.</span></span> <span data-ttu-id="78d1d-105">Dopo la chiamata a [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md) , questa funzione può essere usata per suddividere la mesh in un gruppo di visi/vertici per cluster Super.</span><span class="sxs-lookup"><span data-stu-id="78d1d-105">After [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md) has been called, this function can be used to split the mesh into a group of faces/vertices per super cluster.</span></span> <span data-ttu-id="78d1d-106">Ogni cluster Super contiene tutti i visi che contengono tutti i vertici classificati in uno dei relativi cluster.</span><span class="sxs-lookup"><span data-stu-id="78d1d-106">Each super cluster contains all of the faces that contain any vertex classified in one of its clusters.</span></span> <span data-ttu-id="78d1d-107">Tutti i vertici connessi a questo set di visi sono inclusi anche con la matrice restituita ppVertStatus che indica se il vertice appartiene o meno al cluster Super.</span><span class="sxs-lookup"><span data-stu-id="78d1d-107">All of the vertices connected to this set of faces are also included with the returned array ppVertStatus indicating whether or not the vertex belongs to the super cluster.</span></span>

## <a name="syntax"></a><span data-ttu-id="78d1d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78d1d-108">Syntax</span></span>


```C++
HRESULT D3DXSHPRTCompSplitMeshSC(
  _In_    UINT                          *pClusterIDs,
  _In_    UINT                          NumVertices,
  _In_    UINT                          NumCs,
  _In_    UINT                          *pSClusterIDs,
  _In_    UINT                          NumSCs,
  _In_    LPVOID                        pInputIB,
  _In_    BOOL                          InputIBIs32Bit,
  _In_    UINT                          NumFaces,
  _Inout_ LPD3DXBUFFER                  *ppIBData,
  _Inout_ UINT                          *pIBDataLength,
  _Inout_ BOOL                          OutputIBIs32Bit,
  _Inout_ LPD3DXBUFFER                  *ppFaceRemap,
  _Inout_ LPD3DXBUFFER                  *ppVertData,
  _Inout_ UINT                          *pVertDataLength,
  _Inout_ UINT                          *pSCClusterList,
  _Inout_ D3DXSHPRTSPLITMESHCLUSTERDATA *pSCData
);
```



## <a name="parameters"></a><span data-ttu-id="78d1d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="78d1d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78d1d-110">*pClusterIDs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78d1d-110">*pClusterIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78d1d-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="78d1d-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="78d1d-112">ID cluster *numVertices* (estratti da un buffer compresso).</span><span class="sxs-lookup"><span data-stu-id="78d1d-112">*NumVertices* cluster IDs (extracted from a compressed buffer.)</span></span>

</dd> <dt>

<span data-ttu-id="78d1d-113">*NumVertices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78d1d-113">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78d1d-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78d1d-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="78d1d-115">Numero di vertici nel mesh originale.</span><span class="sxs-lookup"><span data-stu-id="78d1d-115">Number of vertices in original mesh.</span></span>

</dd> <dt>

<span data-ttu-id="78d1d-116">*NumCs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78d1d-116">*NumCs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78d1d-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78d1d-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="78d1d-118">Numero di cluster (parametro di input per la compressione).</span><span class="sxs-lookup"><span data-stu-id="78d1d-118">Number of clusters (input parameter to compression.)</span></span>

</dd> <dt>

<span data-ttu-id="78d1d-119">*pSClusterIDs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78d1d-119">*pSClusterIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78d1d-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="78d1d-120">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="78d1d-121">Matrice di dimensioni *NumCs* che conterrà gli ID del cluster superati.</span><span class="sxs-lookup"><span data-stu-id="78d1d-121">Array of size *NumCs* that will contain super cluster IDs.</span></span>

</dd> <dt>

<span data-ttu-id="78d1d-122">*NumSCs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78d1d-122">*NumSCs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78d1d-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78d1d-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="78d1d-124">Numero di cluster superati allocati in [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md).</span><span class="sxs-lookup"><span data-stu-id="78d1d-124">Number of super clusters allocated in [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md).</span></span>

</dd> <dt>

<span data-ttu-id="78d1d-125">*pInputIB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78d1d-125">*pInputIB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78d1d-126">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78d1d-126">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="78d1d-127">Buffer indice non elaborato per mesh.</span><span class="sxs-lookup"><span data-stu-id="78d1d-127">Raw index buffer for mesh.</span></span> <span data-ttu-id="78d1d-128">Il formato dipende da *InputIBIs32Bit*.</span><span class="sxs-lookup"><span data-stu-id="78d1d-128">The format depends on *InputIBIs32Bit*.</span></span>

</dd> <dt>

<span data-ttu-id="78d1d-129">*InputIBIs32Bit* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78d1d-129">*InputIBIs32Bit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78d1d-130">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78d1d-130">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="78d1d-131">Se **true**, il buffer dell'indice è impostato su 32 bit; in caso contrario, 16 bit.</span><span class="sxs-lookup"><span data-stu-id="78d1d-131">If **TRUE**, the index buffer is set to 32 bit; otherwise, 16 bit.</span></span>

</dd> <dt>

<span data-ttu-id="78d1d-132">*NumFaces* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78d1d-132">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78d1d-133">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78d1d-133">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="78d1d-134">Numero di visi nella mesh originale (*pInputIB* è 3 volte questa lunghezza).</span><span class="sxs-lookup"><span data-stu-id="78d1d-134">Number of faces in the original mesh (*pInputIB* is 3 times this length.)</span></span>

</dd> <dt>

<span data-ttu-id="78d1d-135">*ppIBData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="78d1d-135">*ppIBData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="78d1d-136">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="78d1d-136">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="78d1d-137">Buffer dell'indice non elaborato che conterrà i visi divisi risultanti.</span><span class="sxs-lookup"><span data-stu-id="78d1d-137">Raw index buffer that will contain the resulting split faces.</span></span> <span data-ttu-id="78d1d-138">Formato determinato da *InputIBIs32Bit*.</span><span class="sxs-lookup"><span data-stu-id="78d1d-138">Format determined by *InputIBIs32Bit*.</span></span> <span data-ttu-id="78d1d-139">Allocato per funzione.</span><span class="sxs-lookup"><span data-stu-id="78d1d-139">Allocated by function.</span></span>

</dd> <dt>

<span data-ttu-id="78d1d-140">*pIBDataLength* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="78d1d-140">*pIBDataLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="78d1d-141">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="78d1d-141">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="78d1d-142">Lunghezza di *ppIBData*, assegnata nella funzione.</span><span class="sxs-lookup"><span data-stu-id="78d1d-142">Length of *ppIBData*, assigned in function.</span></span>

</dd> <dt>

<span data-ttu-id="78d1d-143">*OutputIBIs32Bit* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="78d1d-143">*OutputIBIs32Bit* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="78d1d-144">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78d1d-144">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="78d1d-145">Se **true**, alloca una matrice di Unsigned Integer; in caso contrario, alloca una matrice short senza segno.</span><span class="sxs-lookup"><span data-stu-id="78d1d-145">If **TRUE**, allocates an unsigned integer array; otherwise, allocates an unsigned short array.</span></span>

</dd> <dt>

<span data-ttu-id="78d1d-146">*ppFaceRemap* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="78d1d-146">*ppFaceRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="78d1d-147">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="78d1d-147">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="78d1d-148">Mapping di ogni viso in *ppIBData* ai visi originali.</span><span class="sxs-lookup"><span data-stu-id="78d1d-148">Mapping of each face in *ppIBData* to original faces.</span></span> <span data-ttu-id="78d1d-149">La lunghezza è \* *pIBDataLength*/3.</span><span class="sxs-lookup"><span data-stu-id="78d1d-149">Length is \**pIBDataLength*/3.</span></span>

</dd> <dt>

<span data-ttu-id="78d1d-150">*ppVertData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="78d1d-150">*ppVertData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="78d1d-151">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="78d1d-151">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="78d1d-152">Nuova struttura di dati dei vertici.</span><span class="sxs-lookup"><span data-stu-id="78d1d-152">New vertex data structure.</span></span> <span data-ttu-id="78d1d-153">Dimensioni di *pVertDataLength*.</span><span class="sxs-lookup"><span data-stu-id="78d1d-153">Size of *pVertDataLength*.</span></span>

</dd> <dt>

<span data-ttu-id="78d1d-154">*pVertDataLength* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="78d1d-154">*pVertDataLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="78d1d-155">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="78d1d-155">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="78d1d-156">Numero di nuovi vertici in una mesh divisa.</span><span class="sxs-lookup"><span data-stu-id="78d1d-156">Number of new vertices in split mesh.</span></span> <span data-ttu-id="78d1d-157">Funzione assegnata.</span><span class="sxs-lookup"><span data-stu-id="78d1d-157">Assigned in function.</span></span>

</dd> <dt>

<span data-ttu-id="78d1d-158">*pSCClusterList* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="78d1d-158">*pSCClusterList* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="78d1d-159">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="78d1d-159">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="78d1d-160">Matrice di lunghezza *NumCs* che *pSCData* gli indici (campi *pClusterIDs* \* ) per ogni Supercluster, contiene i cluster ordinati in base al Supercluster.</span><span class="sxs-lookup"><span data-stu-id="78d1d-160">Array of length *NumCs* which *pSCData* indexes into (*pClusterIDs*\* fields) for each supercluster, contains clusters sorted by supercluster.</span></span>

</dd> <dt>

<span data-ttu-id="78d1d-161">*pSCData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="78d1d-161">*pSCData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="78d1d-162">Tipo: **[ **D3DXSHPRTSPLITMESHCLUSTERDATA**](d3dxshprtsplitmeshclusterdata.md)\***</span><span class="sxs-lookup"><span data-stu-id="78d1d-162">Type: **[**D3DXSHPRTSPLITMESHCLUSTERDATA**](d3dxshprtsplitmeshclusterdata.md)\***</span></span>

<span data-ttu-id="78d1d-163">Struttura per cluster Super.</span><span class="sxs-lookup"><span data-stu-id="78d1d-163">Structure per super cluster.</span></span> <span data-ttu-id="78d1d-164">Contiene indici in *ppIBData*, *pSCClusterList* e *ppVertData*.</span><span class="sxs-lookup"><span data-stu-id="78d1d-164">Contains indices into *ppIBData*, *pSCClusterList*, and *ppVertData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78d1d-165">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="78d1d-165">Return value</span></span>

<span data-ttu-id="78d1d-166">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="78d1d-166">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="78d1d-167">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="78d1d-167">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="78d1d-168">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="78d1d-168">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="78d1d-169">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78d1d-169">Requirements</span></span>



| <span data-ttu-id="78d1d-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="78d1d-170">Requirement</span></span> | <span data-ttu-id="78d1d-171">Valore</span><span class="sxs-lookup"><span data-stu-id="78d1d-171">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="78d1d-172">Intestazione</span><span class="sxs-lookup"><span data-stu-id="78d1d-172">Header</span></span><br/>  | <dl> <span data-ttu-id="78d1d-173"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="78d1d-173"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="78d1d-174">Libreria</span><span class="sxs-lookup"><span data-stu-id="78d1d-174">Library</span></span><br/> | <dl> <span data-ttu-id="78d1d-175"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="78d1d-175"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="78d1d-176">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78d1d-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78d1d-177">Funzioni di trasferimento Radiance pre-calcolate</span><span class="sxs-lookup"><span data-stu-id="78d1d-177">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
