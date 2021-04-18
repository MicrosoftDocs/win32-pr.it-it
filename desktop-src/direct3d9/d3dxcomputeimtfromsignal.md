---
description: Calcola gli IMT per triangolo da un segnale personalizzato specificato dall'applicazione che varia in base alla superficie della mesh, in genere con una frequenza maggiore rispetto ai dati dei vertici. Il segnale viene valutato tramite una funzione di callback specificata dall'utente.
ms.assetid: f1d96021-0b7d-43e6-b51b-71a90d2f5ad8
title: Funzione D3DXComputeIMTFromSignal (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 979304a350c226a9406e62896bb84492d8046e74
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323033"
---
# <a name="d3dxcomputeimtfromsignal-function"></a><span data-ttu-id="d56ea-104">D3DXComputeIMTFromSignal (funzione)</span><span class="sxs-lookup"><span data-stu-id="d56ea-104">D3DXComputeIMTFromSignal function</span></span>

<span data-ttu-id="d56ea-105">Calcola gli IMT per triangolo da un segnale personalizzato specificato dall'applicazione che varia in base alla superficie della mesh, in genere con una frequenza maggiore rispetto ai dati dei vertici.</span><span class="sxs-lookup"><span data-stu-id="d56ea-105">Calculates per-triangle IMT's from a custom application-specified signal that varies over the surface of the mesh (generally at a higher frequency than vertex data).</span></span> <span data-ttu-id="d56ea-106">Il segnale viene valutato tramite una funzione di callback specificata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="d56ea-106">The signal is evaluated via a user-specified callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="d56ea-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d56ea-107">Syntax</span></span>


```C++
HRESULT D3DXComputeIMTFromSignal(
  _In_  LPD3DXMESH              pMesh,
  _In_  DWORD                   dwTextureIndex,
  _In_  UINT                    uSignalDimension,
  _In_  FLOAT                   fMaxUVDistance,
  _In_  DWORD                   dwOptions,
  _In_  LPD3DXIMTSIGNALCALLBACK pSignalCallback,
  _In_  VOID                    *pUserData,
        LPD3DXUVATLASCB         pStatusCallback,
        LPVOID                  pUserContext,
  _Out_ LPD3DXBUFFER            *ppIMTData
);
```



## <a name="parameters"></a><span data-ttu-id="d56ea-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d56ea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d56ea-109">*pMesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d56ea-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d56ea-110">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="d56ea-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="d56ea-111">Puntatore a una mesh di input (vedere [**ID3DXMesh**](id3dxmesh.md)) che contiene la geometria dell'oggetto per il calcolo di IMT.</span><span class="sxs-lookup"><span data-stu-id="d56ea-111">A pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the IMT.</span></span>

</dd> <dt>

<span data-ttu-id="d56ea-112">*dwTextureIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d56ea-112">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d56ea-113">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d56ea-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d56ea-114">Indice di coordinate di trama in base zero che identifica il set di coordinate di trama da usare.</span><span class="sxs-lookup"><span data-stu-id="d56ea-114">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="d56ea-115">*uSignalDimension* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d56ea-115">*uSignalDimension* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d56ea-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d56ea-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d56ea-117">Numero di componenti in ogni punto dati del segnale.</span><span class="sxs-lookup"><span data-stu-id="d56ea-117">The number of components in each data point in the signal.</span></span>

</dd> <dt>

<span data-ttu-id="d56ea-118">*fMaxUVDistance* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d56ea-118">*fMaxUVDistance* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d56ea-119">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d56ea-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d56ea-120">Distanza massima tra i vertici; l'algoritmo continua la suddivisione fino a quando la distanza tra tutti i vertici è minore o uguale a fMaxUVDistance.</span><span class="sxs-lookup"><span data-stu-id="d56ea-120">The maximum distance between vertices; the algorithm continues subdividing until the distance between all vertices is less than or equal to fMaxUVDistance.</span></span>

</dd> <dt>

<span data-ttu-id="d56ea-121">*dwOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d56ea-121">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d56ea-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d56ea-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d56ea-123">Opzioni di incapsulamento della trama.</span><span class="sxs-lookup"><span data-stu-id="d56ea-123">Texture wrap options.</span></span> <span data-ttu-id="d56ea-124">Si tratta di una combinazione di uno o più [**flag D3DXIMT**](./d3dximt-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d56ea-124">This is a combination of one or more [**D3DXIMT FLAGS**](./d3dximt-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="d56ea-125">*pSignalCallback* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d56ea-125">*pSignalCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d56ea-126">Tipo: **[LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md)**</span><span class="sxs-lookup"><span data-stu-id="d56ea-126">Type: **[LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md)**</span></span>

<span data-ttu-id="d56ea-127">Puntatore a una funzione dell'analizzatore fornita dall'utente, che verrà usata per calcolare il valore del segnale a coordinate U, V arbitrarie.</span><span class="sxs-lookup"><span data-stu-id="d56ea-127">A pointer to a user-provided evaluator function, which will be used to compute the signal value at arbitrary U,V coordinates.</span></span> <span data-ttu-id="d56ea-128">La funzione segue il prototipo di [LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md).</span><span class="sxs-lookup"><span data-stu-id="d56ea-128">The function follows the prototype of [LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md).</span></span>

</dd> <dt>

<span data-ttu-id="d56ea-129">*pUserData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d56ea-129">*pUserData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d56ea-130">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="d56ea-130">Type: **VOID\***</span></span>

<span data-ttu-id="d56ea-131">Puntatore a un valore definito dall'utente che viene passato alla funzione di callback del segnale.</span><span class="sxs-lookup"><span data-stu-id="d56ea-131">A pointer to a user-defined value which is passed to the signal callback function.</span></span> <span data-ttu-id="d56ea-132">Usato in genere da un'applicazione per passare un puntatore a una struttura di dati che fornisce informazioni sul contesto per la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="d56ea-132">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="d56ea-133">*pStatusCallback*</span><span class="sxs-lookup"><span data-stu-id="d56ea-133">*pStatusCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="d56ea-134">Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="d56ea-134">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="d56ea-135">Puntatore a una funzione di callback per monitorare lo stato di avanzamento del calcolo di IMT.</span><span class="sxs-lookup"><span data-stu-id="d56ea-135">A pointer to a callback function to monitor IMT computation progress.</span></span>

</dd> <dt>

<span data-ttu-id="d56ea-136">*pUserContext*</span><span class="sxs-lookup"><span data-stu-id="d56ea-136">*pUserContext*</span></span> 
</dt> <dd>

<span data-ttu-id="d56ea-137">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d56ea-137">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d56ea-138">Puntatore a una variabile definita dall'utente che viene passata alla funzione di callback dello stato.</span><span class="sxs-lookup"><span data-stu-id="d56ea-138">A pointer to a user-defined variable which is passed to the status callback function.</span></span> <span data-ttu-id="d56ea-139">Usato in genere da un'applicazione per passare un puntatore a una struttura di dati che fornisce informazioni sul contesto per la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="d56ea-139">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="d56ea-140">*ppIMTData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d56ea-140">*ppIMTData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d56ea-141">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="d56ea-141">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="d56ea-142">Puntatore al buffer (vedere [**ID3DXBuffer**](id3dxbuffer.md)) contenente la matrice IMT restituita.</span><span class="sxs-lookup"><span data-stu-id="d56ea-142">A pointer to the buffer (see [**ID3DXBuffer**](id3dxbuffer.md)) containing the returned IMT array.</span></span> <span data-ttu-id="d56ea-143">Questa matrice può essere fornita come input per le [funzioni UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md) di D3DX per definire la priorità dell'allocazione dello spazio di trama nella parametrizzazione della trama.</span><span class="sxs-lookup"><span data-stu-id="d56ea-143">This array can be provided as input to the D3DX [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md) to prioritize texture-space allocation in the texture parameterization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d56ea-144">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d56ea-144">Return value</span></span>

<span data-ttu-id="d56ea-145">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d56ea-145">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d56ea-146">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. in caso contrario, il valore è D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d56ea-146">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d56ea-147">Commenti</span><span class="sxs-lookup"><span data-stu-id="d56ea-147">Remarks</span></span>

<span data-ttu-id="d56ea-148">Questa funzione richiede che la mesh di input contenga un mapping di trama da segnale a mesh, ad esempio coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="d56ea-148">This function requires that the input mesh contain a signal-to-mesh texture mapping (ie. texture coordinates).</span></span> <span data-ttu-id="d56ea-149">Consente all'utente di definire un segnale arbitrariamente sulla superficie della mesh.</span><span class="sxs-lookup"><span data-stu-id="d56ea-149">It allows the user to define a signal arbitrarily over the surface of the mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="d56ea-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d56ea-150">Requirements</span></span>



| <span data-ttu-id="d56ea-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="d56ea-151">Requirement</span></span> | <span data-ttu-id="d56ea-152">Valore</span><span class="sxs-lookup"><span data-stu-id="d56ea-152">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d56ea-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d56ea-153">Header</span></span><br/>  | <dl> <span data-ttu-id="d56ea-154"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d56ea-154"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d56ea-155">Libreria</span><span class="sxs-lookup"><span data-stu-id="d56ea-155">Library</span></span><br/> | <dl> <span data-ttu-id="d56ea-156"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d56ea-156"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d56ea-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d56ea-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d56ea-158">Funzioni UVAtlas</span><span class="sxs-lookup"><span data-stu-id="d56ea-158">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[<span data-ttu-id="d56ea-159">Uso di UVAtlas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d56ea-159">Using UVAtlas (Direct3D 9)</span></span>](using-uvatlas.md)
</dt> </dl>

 

 
