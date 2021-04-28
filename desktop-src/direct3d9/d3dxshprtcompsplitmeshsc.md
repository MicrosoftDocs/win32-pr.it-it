---
description: 'Funzione D3DXSHPRTCompSplitMeshSC: usata con i risultati compressi della versione vertice del simulatore PRT (Precomputed Radiance Transfer).'
ms.assetid: 10d81920-2a1b-42fa-aabe-7d6b504f4d36
title: Funzione D3DXSHPRTCompSplitMeshSC (D3DX9Mesh.h)
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
ms.openlocfilehash: e51a86ec9b12992d49364d3a7c614751dacafac3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093899"
---
# <a name="d3dxshprtcompsplitmeshsc-function"></a><span data-ttu-id="f0bd7-103">Funzione D3DXSHPRTCompSplitMeshSC</span><span class="sxs-lookup"><span data-stu-id="f0bd7-103">D3DXSHPRTCompSplitMeshSC function</span></span>

<span data-ttu-id="f0bd7-104">Usato con i risultati compressi della versione dei vertici del simulatore di trasferimento di raggi pre-ricalcolo (PRT).</span><span class="sxs-lookup"><span data-stu-id="f0bd7-104">Used with compressed results of the vertex version of the precomputed radiance transfer (PRT) simulator.</span></span> <span data-ttu-id="f0bd7-105">Dopo [**aver chiamato D3DXSHPRTCompSuperCluster,**](d3dxshprtcompsupercluster.md) questa funzione può essere usata per dividere la mesh in un gruppo di visi/vertici per ogni super cluster.</span><span class="sxs-lookup"><span data-stu-id="f0bd7-105">After [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md) has been called, this function can be used to split the mesh into a group of faces/vertices per super cluster.</span></span> <span data-ttu-id="f0bd7-106">Ogni super cluster contiene tutti i visi che contengono tutti i vertici classificati in uno dei relativi cluster.</span><span class="sxs-lookup"><span data-stu-id="f0bd7-106">Each super cluster contains all of the faces that contain any vertex classified in one of its clusters.</span></span> <span data-ttu-id="f0bd7-107">Tutti i vertici connessi a questo set di visi sono inclusi anche nella matrice restituita ppVertStatus che indica se il vertice appartiene o meno al cluster super.</span><span class="sxs-lookup"><span data-stu-id="f0bd7-107">All of the vertices connected to this set of faces are also included with the returned array ppVertStatus indicating whether or not the vertex belongs to the super cluster.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0bd7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f0bd7-108">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="f0bd7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f0bd7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0bd7-110">*pClusterIDs* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f0bd7-110">*pClusterIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0bd7-111">Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0bd7-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f0bd7-112">*ID cluster NumVertices* (estratti da un buffer compresso).</span><span class="sxs-lookup"><span data-stu-id="f0bd7-112">*NumVertices* cluster IDs (extracted from a compressed buffer.)</span></span>

</dd> <dt>

<span data-ttu-id="f0bd7-113">*NumVertices* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f0bd7-113">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0bd7-114">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f0bd7-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f0bd7-115">Numero di vertici nella mesh originale.</span><span class="sxs-lookup"><span data-stu-id="f0bd7-115">Number of vertices in original mesh.</span></span>

</dd> <dt>

<span data-ttu-id="f0bd7-116">*NumCs* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f0bd7-116">*NumCs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0bd7-117">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f0bd7-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f0bd7-118">Numero di cluster (parametro di input per la compressione).</span><span class="sxs-lookup"><span data-stu-id="f0bd7-118">Number of clusters (input parameter to compression.)</span></span>

</dd> <dt>

<span data-ttu-id="f0bd7-119">*pSClusterIDs* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f0bd7-119">*pSClusterIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0bd7-120">Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0bd7-120">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f0bd7-121">Matrice di *numC di dimensioni* che conterranno ID cluster super.</span><span class="sxs-lookup"><span data-stu-id="f0bd7-121">Array of size *NumCs* that will contain super cluster IDs.</span></span>

</dd> <dt>

<span data-ttu-id="f0bd7-122">*NumSCS* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f0bd7-122">*NumSCs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0bd7-123">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f0bd7-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f0bd7-124">Numero di cluster super allocati in [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md).</span><span class="sxs-lookup"><span data-stu-id="f0bd7-124">Number of super clusters allocated in [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md).</span></span>

</dd> <dt>

<span data-ttu-id="f0bd7-125">*pInputIB* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f0bd7-125">*pInputIB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0bd7-126">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f0bd7-126">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f0bd7-127">Dati index buffer non elaborati per la mesh.</span><span class="sxs-lookup"><span data-stu-id="f0bd7-127">Raw index buffer for mesh.</span></span> <span data-ttu-id="f0bd7-128">Il formato dipende da *InputIBIs32Bit.*</span><span class="sxs-lookup"><span data-stu-id="f0bd7-128">The format depends on *InputIBIs32Bit*.</span></span>

</dd> <dt>

<span data-ttu-id="f0bd7-129">*InputIBIs32Bit* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f0bd7-129">*InputIBIs32Bit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0bd7-130">Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f0bd7-130">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f0bd7-131">Se **TRUE,** la index buffer è impostata su 32 bit. in caso contrario, 16 bit.</span><span class="sxs-lookup"><span data-stu-id="f0bd7-131">If **TRUE**, the index buffer is set to 32 bit; otherwise, 16 bit.</span></span>

</dd> <dt>

<span data-ttu-id="f0bd7-132">*NumFaces* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f0bd7-132">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0bd7-133">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f0bd7-133">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f0bd7-134">Numero di visi nella mesh originale *(pInputIB* è 3 volte la lunghezza).</span><span class="sxs-lookup"><span data-stu-id="f0bd7-134">Number of faces in the original mesh (*pInputIB* is 3 times this length.)</span></span>

</dd> <dt>

<span data-ttu-id="f0bd7-135">*ppIBData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f0bd7-135">*ppIBData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0bd7-136">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0bd7-136">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="f0bd7-137">Oggetto index buffer che conterrà i visi divisi risultanti.</span><span class="sxs-lookup"><span data-stu-id="f0bd7-137">Raw index buffer that will contain the resulting split faces.</span></span> <span data-ttu-id="f0bd7-138">Formato determinato da *InputIBIs32Bit*.</span><span class="sxs-lookup"><span data-stu-id="f0bd7-138">Format determined by *InputIBIs32Bit*.</span></span> <span data-ttu-id="f0bd7-139">Allocato dalla funzione.</span><span class="sxs-lookup"><span data-stu-id="f0bd7-139">Allocated by function.</span></span>

</dd> <dt>

<span data-ttu-id="f0bd7-140">*pIBDataLength* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f0bd7-140">*pIBDataLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0bd7-141">Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0bd7-141">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f0bd7-142">Lunghezza di *ppIBData*, assegnata nella funzione.</span><span class="sxs-lookup"><span data-stu-id="f0bd7-142">Length of *ppIBData*, assigned in function.</span></span>

</dd> <dt>

<span data-ttu-id="f0bd7-143">*OutputIBIs32Bit* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f0bd7-143">*OutputIBIs32Bit* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0bd7-144">Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f0bd7-144">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f0bd7-145">Se **TRUE,** alloca una matrice di interi senza segno; In caso contrario, alloca una matrice short senza segno.</span><span class="sxs-lookup"><span data-stu-id="f0bd7-145">If **TRUE**, allocates an unsigned integer array; otherwise, allocates an unsigned short array.</span></span>

</dd> <dt>

<span data-ttu-id="f0bd7-146">*ppFaceRemap* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f0bd7-146">*ppFaceRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0bd7-147">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0bd7-147">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="f0bd7-148">Mapping di ogni viso in *ppIBData* ai visi originali.</span><span class="sxs-lookup"><span data-stu-id="f0bd7-148">Mapping of each face in *ppIBData* to original faces.</span></span> <span data-ttu-id="f0bd7-149">La lunghezza \* *è pIBDataLength*/3.</span><span class="sxs-lookup"><span data-stu-id="f0bd7-149">Length is \**pIBDataLength*/3.</span></span>

</dd> <dt>

<span data-ttu-id="f0bd7-150">*ppVertData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f0bd7-150">*ppVertData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0bd7-151">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0bd7-151">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="f0bd7-152">Nuova struttura dei dati dei vertici.</span><span class="sxs-lookup"><span data-stu-id="f0bd7-152">New vertex data structure.</span></span> <span data-ttu-id="f0bd7-153">Dimensione di *pVertDataLength.*</span><span class="sxs-lookup"><span data-stu-id="f0bd7-153">Size of *pVertDataLength*.</span></span>

</dd> <dt>

<span data-ttu-id="f0bd7-154">*pVertDataLength* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f0bd7-154">*pVertDataLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0bd7-155">Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0bd7-155">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f0bd7-156">Numero di nuovi vertici nella mesh suddivisa.</span><span class="sxs-lookup"><span data-stu-id="f0bd7-156">Number of new vertices in split mesh.</span></span> <span data-ttu-id="f0bd7-157">Assegnato nella funzione .</span><span class="sxs-lookup"><span data-stu-id="f0bd7-157">Assigned in function.</span></span>

</dd> <dt>

<span data-ttu-id="f0bd7-158">*pSCClusterList* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f0bd7-158">*pSCClusterList* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0bd7-159">Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0bd7-159">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f0bd7-160">Matrice di *numCs* di lunghezza in cui *pSCData* indicizza (campi *pClusterIDs)* per ogni supercluster, contiene cluster ordinati per \* supercluster.</span><span class="sxs-lookup"><span data-stu-id="f0bd7-160">Array of length *NumCs* which *pSCData* indexes into (*pClusterIDs*\* fields) for each supercluster, contains clusters sorted by supercluster.</span></span>

</dd> <dt>

<span data-ttu-id="f0bd7-161">*pSCData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f0bd7-161">*pSCData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0bd7-162">Tipo: **[ **D3DXSHPRTSPLITMESHCLUSTERDATA**](d3dxshprtsplitmeshclusterdata.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0bd7-162">Type: **[**D3DXSHPRTSPLITMESHCLUSTERDATA**](d3dxshprtsplitmeshclusterdata.md)\***</span></span>

<span data-ttu-id="f0bd7-163">Struttura per cluster super.</span><span class="sxs-lookup"><span data-stu-id="f0bd7-163">Structure per super cluster.</span></span> <span data-ttu-id="f0bd7-164">Contiene indici in *ppIBData*, *pSCClusterList* e *ppVertData*.</span><span class="sxs-lookup"><span data-stu-id="f0bd7-164">Contains indices into *ppIBData*, *pSCClusterList*, and *ppVertData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0bd7-165">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f0bd7-165">Return value</span></span>

<span data-ttu-id="f0bd7-166">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f0bd7-166">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f0bd7-167">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f0bd7-167">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f0bd7-168">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="f0bd7-168">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0bd7-169">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0bd7-169">Requirements</span></span>



| <span data-ttu-id="f0bd7-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0bd7-170">Requirement</span></span> | <span data-ttu-id="f0bd7-171">Valore</span><span class="sxs-lookup"><span data-stu-id="f0bd7-171">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0bd7-172">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f0bd7-172">Header</span></span><br/>  | <dl> <span data-ttu-id="f0bd7-173"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="f0bd7-173"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f0bd7-174">Libreria</span><span class="sxs-lookup"><span data-stu-id="f0bd7-174">Library</span></span><br/> | <dl> <span data-ttu-id="f0bd7-175"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0bd7-175"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f0bd7-176">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f0bd7-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0bd7-177">Funzioni di trasferimento della radiance pre-ricalcolate</span><span class="sxs-lookup"><span data-stu-id="f0bd7-177">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
