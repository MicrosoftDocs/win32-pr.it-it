---
description: 'Calcola la luminosità di origine risultante dalla dispersione della sottosuperficie, usando le proprietà del materiale impostate da ID3DXPRTEngine:: SetMeshMaterials. Questo metodo può essere utilizzato solo per i materiali definiti per ogni vertice in un oggetto mesh.'
ms.assetid: cdf0d9c1-70e3-44d5-b97a-0521e6739daf
title: 'Metodo ID3DXPRTEngine:: ComputeSS (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSS
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 89a69be6cc946ff6695d234b8bfb82532385526e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356064"
---
# <a name="id3dxprtenginecomputess-method"></a><span data-ttu-id="733ad-104">Metodo ID3DXPRTEngine:: ComputeSS</span><span class="sxs-lookup"><span data-stu-id="733ad-104">ID3DXPRTEngine::ComputeSS method</span></span>

<span data-ttu-id="733ad-105">Calcola la luminosità di origine risultante dalla dispersione della sottosuperficie, usando le proprietà del materiale impostate da [**ID3DXPRTEngine:: SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md).</span><span class="sxs-lookup"><span data-stu-id="733ad-105">Computes the source radiance resulting from subsurface scattering, using material properties set by [**ID3DXPRTEngine::SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md).</span></span> <span data-ttu-id="733ad-106">Questo metodo può essere utilizzato solo per i materiali definiti per ogni vertice in un oggetto mesh.</span><span class="sxs-lookup"><span data-stu-id="733ad-106">This method can be used only for materials defined per-vertex in a mesh object.</span></span>

## <a name="syntax"></a><span data-ttu-id="733ad-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="733ad-107">Syntax</span></span>


```C++
HRESULT ComputeSS(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a><span data-ttu-id="733ad-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="733ad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="733ad-109">*pDataIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="733ad-109">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="733ad-110">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="733ad-110">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="733ad-111">Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di input che rappresenta l'oggetto 3D del rimbalzo della luce precedente.</span><span class="sxs-lookup"><span data-stu-id="733ad-111">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the 3D object from the previous light bounce.</span></span> <span data-ttu-id="733ad-112">Questo buffer di input deve avere il numero appropriato di canali di colore allocati per la simulazione.</span><span class="sxs-lookup"><span data-stu-id="733ad-112">This input buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="733ad-113">*pDataOut* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="733ad-113">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="733ad-114">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="733ad-114">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="733ad-115">Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di output che modella un singolo rimbalzo della sottosuperficie.</span><span class="sxs-lookup"><span data-stu-id="733ad-115">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models a single bounce of the subsurface-scattered light.</span></span> <span data-ttu-id="733ad-116">Questo buffer di output deve avere il numero appropriato di canali di colore allocati per la simulazione.</span><span class="sxs-lookup"><span data-stu-id="733ad-116">This output buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="733ad-117">*pDataTotal* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="733ad-117">*pDataTotal* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="733ad-118">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="733ad-118">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="733ad-119">Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) facoltativo che corrisponde alla somma in corso di tutti gli output pDataOut precedenti.</span><span class="sxs-lookup"><span data-stu-id="733ad-119">Pointer to an optional [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that is the running sum of all previous pDataOut outputs.</span></span> <span data-ttu-id="733ad-120">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="733ad-120">May be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="733ad-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="733ad-121">Return value</span></span>

<span data-ttu-id="733ad-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="733ad-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="733ad-123">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="733ad-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="733ad-124">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="733ad-124">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="733ad-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="733ad-125">Remarks</span></span>

<span data-ttu-id="733ad-126">Per modellare la dispersione della sottosuperficie, chiamare questo metodo per ogni rimbalzo chiaro dopo la chiamata di un metodo ID3DXPRTEngine:: ComputeDirectLighting.</span><span class="sxs-lookup"><span data-stu-id="733ad-126">To model subsurface scattering, call this method for each light bounce after an ID3DXPRTEngine::ComputeDirectLighting method is called.</span></span>

<span data-ttu-id="733ad-127">Usare la sequenza chiamante seguente per modellare la dispersione della sottosuperficie.</span><span class="sxs-lookup"><span data-stu-id="733ad-127">Use the following calling sequence to model subsurface scattering.</span></span>


```
LPD3DXPRTBUFFER pDataA, pDataB, pDataC; // initialization
ID3DXPRTEngine* m_pPRTEngine;
    
hr = m_pPRTEngine->ComputeDirectLightingSH( SHOrder, pDataA );
    
// *pDataC should be set to zero. The ComputeSS call will add together the    
// direct lighting results from pDataA for non-subsurface scattering elements   
// and subsurface scattering results for the subsurface scattering elements.
    
hr = m_pPRTEngine->ComputeSS( pDataA, pDataB, pDataC );
if ( FAILED( hr ) ) goto Exit;
```



<span data-ttu-id="733ad-128">L'output di questo metodo non include l'albedo e solo la luce in ingresso è integrata nel simulatore.</span><span class="sxs-lookup"><span data-stu-id="733ad-128">The output of this method does not include albedo, and only incoming light is integrated in the simulator.</span></span> <span data-ttu-id="733ad-129">Se non si moltiplica l'albedo, è possibile modellare la variazione dell'albedo a una scala più sottile rispetto alla luminosità di origine, ottenendo così risultati più accurati dalla compressione.</span><span class="sxs-lookup"><span data-stu-id="733ad-129">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="733ad-130">Chiamare [**ID3DXPRTEngine:: MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) per moltiplicare ogni vettore di traslazione di radiazione (PRT) pre-calcolato per l'albedo.</span><span class="sxs-lookup"><span data-stu-id="733ad-130">Call [**ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) to multiply each precomputed radiance transfer (PRT) vector by the albedo.</span></span>

## <a name="requirements"></a><span data-ttu-id="733ad-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="733ad-131">Requirements</span></span>



| <span data-ttu-id="733ad-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="733ad-132">Requirement</span></span> | <span data-ttu-id="733ad-133">Valore</span><span class="sxs-lookup"><span data-stu-id="733ad-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="733ad-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="733ad-134">Header</span></span><br/>  | <dl> <span data-ttu-id="733ad-135"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="733ad-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="733ad-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="733ad-136">Library</span></span><br/> | <dl> <span data-ttu-id="733ad-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="733ad-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="733ad-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="733ad-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="733ad-139">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="733ad-139">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="733ad-140">**ID3DXPRTEngine::ComputeBounce**</span><span class="sxs-lookup"><span data-stu-id="733ad-140">**ID3DXPRTEngine::ComputeBounce**</span></span>](id3dxprtengine--computebounce.md)
</dt> </dl>

 

 




