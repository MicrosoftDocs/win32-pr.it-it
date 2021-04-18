---
description: Calcolare gli IMT per triangolo da dati per vertice. Questa funzione consente di calcolare l'IMT in base a qualsiasi valore in una mesh (colore, normale e così via).
ms.assetid: a417a8ad-77b1-49ae-aea0-6a32a154499f
title: Funzione D3DXComputeIMTFromPerVertexSignal (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromPerVertexSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b12ea3f15f1a185125da46f575d37ad97dd5622
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322866"
---
# <a name="d3dxcomputeimtfrompervertexsignal-function"></a><span data-ttu-id="d895b-104">D3DXComputeIMTFromPerVertexSignal (funzione)</span><span class="sxs-lookup"><span data-stu-id="d895b-104">D3DXComputeIMTFromPerVertexSignal function</span></span>

<span data-ttu-id="d895b-105">Calcolare gli IMT per triangolo da dati per vertice.</span><span class="sxs-lookup"><span data-stu-id="d895b-105">Calculate per-triangle IMT's from from per-vertex data.</span></span> <span data-ttu-id="d895b-106">Questa funzione consente di calcolare l'IMT in base a qualsiasi valore in una mesh (colore, normale e così via).</span><span class="sxs-lookup"><span data-stu-id="d895b-106">This function allows you to calculate the IMT based off of any value in a mesh (color, normal, etc).</span></span>

## <a name="syntax"></a><span data-ttu-id="d895b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d895b-107">Syntax</span></span>


```C++
HRESULT D3DXComputeIMTFromPerVertexSignal(
  _In_        LPD3DXMESH      pMesh,
  _In_  const FLOAT           *pfVertexSignal,
  _In_        UINT            uSignalDimension,
  _In_        UINT            uSignalStride,
  _In_        DWORD           dwOptions,
              LPD3DXUVATLASCB pStatusCallback,
              LPVOID          pUserContext,
  _Out_       LPD3DXBUFFER    *ppIMTData
);
```



## <a name="parameters"></a><span data-ttu-id="d895b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d895b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d895b-109">*pMesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d895b-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d895b-110">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="d895b-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="d895b-111">Puntatore a una mesh di input (vedere [**ID3DXMesh**](id3dxmesh.md)) che contiene la geometria dell'oggetto per il calcolo di IMT.</span><span class="sxs-lookup"><span data-stu-id="d895b-111">A pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the IMT.</span></span>

</dd> <dt>

<span data-ttu-id="d895b-112">*pfVertexSignal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d895b-112">*pfVertexSignal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d895b-113">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="d895b-113">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d895b-114">Puntatore a una matrice di dati per vertice da cui verrà calcolato IMT.</span><span class="sxs-lookup"><span data-stu-id="d895b-114">A pointer to an array of per-vertex data from which IMT will be computed.</span></span> <span data-ttu-id="d895b-115">La dimensione della matrice è uSignalStride \* v, dove v è il numero di vertici nella rete.</span><span class="sxs-lookup"><span data-stu-id="d895b-115">The array size is uSignalStride \* v, where v is the number of vertices in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="d895b-116">*uSignalDimension* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d895b-116">*uSignalDimension* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d895b-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d895b-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d895b-118">Numero di float per vertice.</span><span class="sxs-lookup"><span data-stu-id="d895b-118">The number of floats per vertex.</span></span>

</dd> <dt>

<span data-ttu-id="d895b-119">*uSignalStride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d895b-119">*uSignalStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d895b-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d895b-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d895b-121">Numero di byte per vertice nella matrice.</span><span class="sxs-lookup"><span data-stu-id="d895b-121">The number of bytes per vertex in the array.</span></span> <span data-ttu-id="d895b-122">Deve essere un multiplo di sizeof (float)</span><span class="sxs-lookup"><span data-stu-id="d895b-122">This must be a multiple of sizeof(float)</span></span>

</dd> <dt>

<span data-ttu-id="d895b-123">*dwOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d895b-123">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d895b-124">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d895b-124">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d895b-125">Opzioni di incapsulamento della trama.</span><span class="sxs-lookup"><span data-stu-id="d895b-125">Texture wrap options.</span></span> <span data-ttu-id="d895b-126">Si tratta di una combinazione di uno o più [**flag D3DXIMT**](./d3dximt-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d895b-126">This is a combination of one or more [**D3DXIMT FLAGS**](./d3dximt-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="d895b-127">*pStatusCallback*</span><span class="sxs-lookup"><span data-stu-id="d895b-127">*pStatusCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="d895b-128">Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="d895b-128">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="d895b-129">Puntatore a una funzione di callback per monitorare lo stato di avanzamento del calcolo di IMT.</span><span class="sxs-lookup"><span data-stu-id="d895b-129">A pointer to a callback function to monitor IMT computation progress.</span></span>

</dd> <dt>

<span data-ttu-id="d895b-130">*pUserContext*</span><span class="sxs-lookup"><span data-stu-id="d895b-130">*pUserContext*</span></span> 
</dt> <dd>

<span data-ttu-id="d895b-131">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d895b-131">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d895b-132">Puntatore a una variabile definita dall'utente che viene passata alla funzione di callback dello stato.</span><span class="sxs-lookup"><span data-stu-id="d895b-132">A pointer to a user-defined variable which is passed to the status callback function.</span></span> <span data-ttu-id="d895b-133">Usato in genere da un'applicazione per passare un puntatore a una struttura di dati che fornisce informazioni sul contesto per la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="d895b-133">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="d895b-134">*ppIMTData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d895b-134">*ppIMTData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d895b-135">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="d895b-135">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="d895b-136">Puntatore al buffer (vedere [**ID3DXBuffer**](id3dxbuffer.md)) contenente la matrice IMT restituita.</span><span class="sxs-lookup"><span data-stu-id="d895b-136">A pointer to the buffer (see [**ID3DXBuffer**](id3dxbuffer.md)) containing the returned IMT array.</span></span> <span data-ttu-id="d895b-137">Questa matrice può essere fornita come input per le [funzioni UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md) di D3DX per definire la priorità dell'allocazione dello spazio di trama nella parametrizzazione della trama.</span><span class="sxs-lookup"><span data-stu-id="d895b-137">This array can be provided as input to the D3DX [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md) to prioritize texture-space allocation in the texture parameterization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d895b-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d895b-138">Return value</span></span>

<span data-ttu-id="d895b-139">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d895b-139">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d895b-140">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. in caso contrario, il valore è D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d895b-140">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d895b-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d895b-141">Requirements</span></span>



| <span data-ttu-id="d895b-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="d895b-142">Requirement</span></span> | <span data-ttu-id="d895b-143">Valore</span><span class="sxs-lookup"><span data-stu-id="d895b-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d895b-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d895b-144">Header</span></span><br/>  | <dl> <span data-ttu-id="d895b-145"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d895b-145"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d895b-146">Libreria</span><span class="sxs-lookup"><span data-stu-id="d895b-146">Library</span></span><br/> | <dl> <span data-ttu-id="d895b-147"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d895b-147"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d895b-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d895b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d895b-149">Funzioni UVAtlas</span><span class="sxs-lookup"><span data-stu-id="d895b-149">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[<span data-ttu-id="d895b-150">Uso di UVAtlas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d895b-150">Using UVAtlas (Direct3D 9)</span></span>](using-uvatlas.md)
</dt> </dl>

 

 
