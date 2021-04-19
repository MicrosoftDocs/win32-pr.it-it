---
description: 'Calcola un vettore di trasferimento che esegue il mapping della luminosità di origine alla luminosità di uscita risultante dalla dispersione della sottosuperficie, usando il campionamento adattivo e le proprietà del materiale impostate da ID3DXPRTEngine:: SetMeshMaterials.'
ms.assetid: 34e42271-703b-4b67-8153-2eca3f8dde92
title: 'Metodo ID3DXPRTEngine:: ComputeSSAdaptive (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSSAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 198a597020a0bfcbc789cc741e42048bd89eb95f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323683"
---
# <a name="id3dxprtenginecomputessadaptive-method"></a><span data-ttu-id="4ca5a-103">Metodo ID3DXPRTEngine:: ComputeSSAdaptive</span><span class="sxs-lookup"><span data-stu-id="4ca5a-103">ID3DXPRTEngine::ComputeSSAdaptive method</span></span>

<span data-ttu-id="4ca5a-104">Calcola un vettore di trasferimento che esegue il mapping della luminosità di origine alla luminosità di uscita risultante dalla dispersione della sottosuperficie, usando il campionamento adattivo e le proprietà del materiale impostate da [**ID3DXPRTEngine:: SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md).</span><span class="sxs-lookup"><span data-stu-id="4ca5a-104">Computes a transfer vector that maps source radiance to exit radiance resulting from subsurface scattering, using adaptive sampling and material properties set by [**ID3DXPRTEngine::SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md).</span></span> <span data-ttu-id="4ca5a-105">Il metodo genera nuovi vertici e visi sulla mesh per approssimare in modo più accurato il segnale PRT (pre-Computed Radiance Transfer).</span><span class="sxs-lookup"><span data-stu-id="4ca5a-105">The method generates new vertices and faces on the mesh to more accurately approximate the precomputed radiance transfer (PRT) signal.</span></span> <span data-ttu-id="4ca5a-106">Questo metodo può essere utilizzato solo per i materiali definiti per ogni vertice in un oggetto mesh.</span><span class="sxs-lookup"><span data-stu-id="4ca5a-106">This method can be used only for materials defined per-vertex in a mesh object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ca5a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4ca5a-107">Syntax</span></span>


```C++
HRESULT ComputeSSAdaptive(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a><span data-ttu-id="4ca5a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4ca5a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ca5a-109">*pDataIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4ca5a-109">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ca5a-110">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="4ca5a-110">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="4ca5a-111">Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di input che rappresenta l'oggetto 3D del rimbalzo della luce precedente.</span><span class="sxs-lookup"><span data-stu-id="4ca5a-111">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the 3D object from the previous light bounce.</span></span> <span data-ttu-id="4ca5a-112">Questo buffer di input deve avere il numero appropriato di canali di colore allocati per la simulazione.</span><span class="sxs-lookup"><span data-stu-id="4ca5a-112">This input buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="4ca5a-113">*AdaptiveThresh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4ca5a-113">*AdaptiveThresh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ca5a-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4ca5a-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4ca5a-115">Soglia sul vettore PRT da usare per la suddivisione dei vertici e delle facce mesh.</span><span class="sxs-lookup"><span data-stu-id="4ca5a-115">Threshold on the PRT vector to use for subdividing mesh vertices and faces.</span></span> <span data-ttu-id="4ca5a-116">Se è minore di 1e-6F, viene specificato un valore predefinito di 1e-6F.</span><span class="sxs-lookup"><span data-stu-id="4ca5a-116">If less than 1e-6f, a default value of 1e-6f is specified.</span></span>

</dd> <dt>

<span data-ttu-id="4ca5a-117">*MinEdgeLength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4ca5a-117">*MinEdgeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ca5a-118">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4ca5a-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4ca5a-119">Lunghezza minima del bordo della superficie che verrà generata nel campionamento adattivo.</span><span class="sxs-lookup"><span data-stu-id="4ca5a-119">Minimum face edge length that will be generated in adaptive sampling.</span></span> <span data-ttu-id="4ca5a-120">Se il metodo determina che il valore è troppo piccolo, viene specificato un valore dipendente dal modello.</span><span class="sxs-lookup"><span data-stu-id="4ca5a-120">If the method determines that the value is too small, a model-dependent value is specified.</span></span>

</dd> <dt>

<span data-ttu-id="4ca5a-121">*MaxSubdiv* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4ca5a-121">*MaxSubdiv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ca5a-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4ca5a-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4ca5a-123">Livello massimo di suddivisione di una faccia che verrà utilizzata nel campionamento adattivo.</span><span class="sxs-lookup"><span data-stu-id="4ca5a-123">Maximum level of subdivision of a face that will be used in adaptive sampling.</span></span> <span data-ttu-id="4ca5a-124">Se è zero, viene specificato un valore predefinito pari a 4.</span><span class="sxs-lookup"><span data-stu-id="4ca5a-124">If zero, a default value of 4 is specified.</span></span>

</dd> <dt>

<span data-ttu-id="4ca5a-125">*pDataOut* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="4ca5a-125">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ca5a-126">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="4ca5a-126">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="4ca5a-127">Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di output che modella un singolo rimbalzo della sottosuperficie.</span><span class="sxs-lookup"><span data-stu-id="4ca5a-127">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models a single bounce of the subsurface-scattered light.</span></span> <span data-ttu-id="4ca5a-128">Questo buffer di output deve avere il numero appropriato di canali di colore allocati per la simulazione.</span><span class="sxs-lookup"><span data-stu-id="4ca5a-128">This output buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="4ca5a-129">*pDataTotal* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="4ca5a-129">*pDataTotal* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ca5a-130">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="4ca5a-130">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="4ca5a-131">Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) facoltativo che corrisponde alla somma in corso di tutti gli output pDataOut precedenti.</span><span class="sxs-lookup"><span data-stu-id="4ca5a-131">Pointer to an optional [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that is the running sum of all previous pDataOut outputs.</span></span> <span data-ttu-id="4ca5a-132">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="4ca5a-132">May be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ca5a-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4ca5a-133">Return value</span></span>

<span data-ttu-id="4ca5a-134">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4ca5a-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4ca5a-135">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4ca5a-135">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4ca5a-136">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="4ca5a-136">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ca5a-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="4ca5a-137">Remarks</span></span>

<span data-ttu-id="4ca5a-138">Per modellare la dispersione della sottosuperficie, chiamare questo metodo per ogni rimbalzo chiaro dopo la chiamata di un metodo [**ID3DXPRTEngine:: ComputeDirectLightingSHAdaptive**](id3dxprtengine--computedirectlightingshadaptive.md) .</span><span class="sxs-lookup"><span data-stu-id="4ca5a-138">To model subsurface scattering, call this method for each light bounce after an [**ID3DXPRTEngine::ComputeDirectLightingSHAdaptive**](id3dxprtengine--computedirectlightingshadaptive.md) method is called.</span></span>

<span data-ttu-id="4ca5a-139">L'output di questo metodo non include l'albedo e solo la luce in ingresso è integrata nel simulatore.</span><span class="sxs-lookup"><span data-stu-id="4ca5a-139">The output of this method does not include albedo, and only incoming light is integrated in the simulator.</span></span> <span data-ttu-id="4ca5a-140">Se non si moltiplica l'albedo, è possibile modellare la variazione dell'albedo a una scala più sottile rispetto alla luminosità di origine, ottenendo così risultati più accurati dalla compressione.</span><span class="sxs-lookup"><span data-stu-id="4ca5a-140">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="4ca5a-141">Chiamare [**ID3DXPRTEngine:: MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) per moltiplicare ogni vettore PRT per l'albedo.</span><span class="sxs-lookup"><span data-stu-id="4ca5a-141">Call [**ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) to multiply each PRT vector by the albedo.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ca5a-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ca5a-142">Requirements</span></span>



| <span data-ttu-id="4ca5a-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ca5a-143">Requirement</span></span> | <span data-ttu-id="4ca5a-144">Valore</span><span class="sxs-lookup"><span data-stu-id="4ca5a-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ca5a-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4ca5a-145">Header</span></span><br/>  | <dl> <span data-ttu-id="4ca5a-146"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ca5a-146"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="4ca5a-147">Libreria</span><span class="sxs-lookup"><span data-stu-id="4ca5a-147">Library</span></span><br/> | <dl> <span data-ttu-id="4ca5a-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4ca5a-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4ca5a-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4ca5a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ca5a-150">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="4ca5a-150">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="4ca5a-151">**ID3DXPRTEngine::ComputeBounce**</span><span class="sxs-lookup"><span data-stu-id="4ca5a-151">**ID3DXPRTEngine::ComputeBounce**</span></span>](id3dxprtengine--computebounce.md)
</dt> <dt>

[<span data-ttu-id="4ca5a-152">**ID3DXPRTEngine::ComputeSS**</span><span class="sxs-lookup"><span data-stu-id="4ca5a-152">**ID3DXPRTEngine::ComputeSS**</span></span>](id3dxprtengine--computess.md)
</dt> </dl>

 

 
