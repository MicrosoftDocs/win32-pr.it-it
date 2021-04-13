---
description: Calcola la luminosità di origine risultante da un singolo rimbalzo della luce con riflesso. Questo metodo può essere usato per qualsiasi scena illuminata, incluso un modello PRT (precomputed Radiance Transfer) basato su SH (sferica).
ms.assetid: 91a6b503-acd2-459b-9d60-de68c879c61b
title: 'Metodo ID3DXPRTEngine:: ComputeBounce (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeBounce
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d40d4b2686087864cad17df0feb99dbc890033b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355704"
---
# <a name="id3dxprtenginecomputebounce-method"></a><span data-ttu-id="e071c-104">Metodo ID3DXPRTEngine:: ComputeBounce</span><span class="sxs-lookup"><span data-stu-id="e071c-104">ID3DXPRTEngine::ComputeBounce method</span></span>

<span data-ttu-id="e071c-105">Calcola la luminosità di origine risultante da un singolo rimbalzo della luce con riflesso.</span><span class="sxs-lookup"><span data-stu-id="e071c-105">Computes the source radiance resulting from a single bounce of interreflected light.</span></span> <span data-ttu-id="e071c-106">Questo metodo può essere usato per qualsiasi scena illuminata, incluso un modello PRT (precomputed Radiance Transfer) basato su SH (sferica).</span><span class="sxs-lookup"><span data-stu-id="e071c-106">This method can be used for any lit scene, including a spherical harmonic (SH)-based precomputed radiance transfer (PRT) model.</span></span>

## <a name="syntax"></a><span data-ttu-id="e071c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e071c-107">Syntax</span></span>


```C++
HRESULT ComputeBounce(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a><span data-ttu-id="e071c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e071c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e071c-109">*pDataIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e071c-109">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e071c-110">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="e071c-110">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="e071c-111">Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di input che rappresenta l'oggetto 3D del rimbalzo della luce precedente.</span><span class="sxs-lookup"><span data-stu-id="e071c-111">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the 3D object from the previous light bounce.</span></span> <span data-ttu-id="e071c-112">Questo buffer di input deve avere il numero appropriato di canali di colore allocati per la simulazione.</span><span class="sxs-lookup"><span data-stu-id="e071c-112">This input buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="e071c-113">*pDataOut* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="e071c-113">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e071c-114">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="e071c-114">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="e071c-115">Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di output che modella un singolo rimbalzo della luce con riflesso.</span><span class="sxs-lookup"><span data-stu-id="e071c-115">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models a single bounce of the interreflected light.</span></span> <span data-ttu-id="e071c-116">Questo buffer di output deve avere il numero appropriato di canali di colore allocati per la simulazione.</span><span class="sxs-lookup"><span data-stu-id="e071c-116">This output buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="e071c-117">*pDataTotal* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="e071c-117">*pDataTotal* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e071c-118">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="e071c-118">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="e071c-119">Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) facoltativo che corrisponde alla somma in corso di tutti gli output pDataOut precedenti.</span><span class="sxs-lookup"><span data-stu-id="e071c-119">Pointer to an optional [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that is the running sum of all previous pDataOut outputs.</span></span> <span data-ttu-id="e071c-120">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="e071c-120">May be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e071c-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e071c-121">Return value</span></span>

<span data-ttu-id="e071c-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e071c-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e071c-123">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e071c-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e071c-124">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="e071c-124">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="e071c-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="e071c-125">Remarks</span></span>

<span data-ttu-id="e071c-126">Usare la sequenza chiamante seguente per modellare più rimbalzi luce con illuminazione diretta.</span><span class="sxs-lookup"><span data-stu-id="e071c-126">Use the following calling sequence to model multiple light bounces with direct lighting.</span></span>


```
LPD3DXPRTBUFFER pDataA, pDataB, pDataC; // initialization
ID3DXPRTEngine* m_pPRTEngine;

ComputeDirectLightingSH( SHOrder, pDataA );
// The accumulation buffer, pDataC, needs to be 
// initialized to the direct lighting result.

pDataC->AddBuffer( pDataA );
hr = m_pPRTEngine->ComputeBounce( pDataA, pDataB, pDataC ); // first bounce
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, pDataC ); // second bounce
hr = m_pPRTEngine->ComputeBounce( pDataA, pDataB, pDataC ); // third bounce
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, pDataC ); // fourth bounce
```



<span data-ttu-id="e071c-127">Usare la sequenza chiamante seguente per modellare più rimbalzi luce con la dispersione della superficie.</span><span class="sxs-lookup"><span data-stu-id="e071c-127">Use the following calling sequence to model multiple light bounces with subsurface scattering.</span></span>


```
LPD3DXPRTBUFFER pDataA, pDataB, pDataC; // initialization
ID3DXPRTEngine* m_pPRTEngine;
ComputeDirectLightingSH( SHOrder, pDataA );

// *pDataC should be set to zero. The ComputeSS call will add together     
// the direct lighting results from pDataA for non-subsurface scattering 
// elements and subsurface scattering results for the subsurface scattering
// elements. Perform proper error handling for each call.
    
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, NULL   ); // first bounce
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, NULL   ); // second bounce
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
```



<span data-ttu-id="e071c-128">L'output di questo metodo non include l'albedo e solo la luce in ingresso è integrata nel simulatore.</span><span class="sxs-lookup"><span data-stu-id="e071c-128">The output of this method does not include albedo, and only incoming light is integrated in the simulator.</span></span> <span data-ttu-id="e071c-129">Se non si moltiplica l'albedo, è possibile modellare la variazione dell'albedo a una scala più sottile rispetto alla luminosità di origine, ottenendo così risultati più accurati dalla compressione.</span><span class="sxs-lookup"><span data-stu-id="e071c-129">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="e071c-130">Chiamare [**ID3DXPRTEngine:: MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) per moltiplicare ogni vettore PRT per l'albedo.</span><span class="sxs-lookup"><span data-stu-id="e071c-130">Call [**ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) to multiply each PRT vector by the albedo.</span></span>

## <a name="requirements"></a><span data-ttu-id="e071c-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e071c-131">Requirements</span></span>



| <span data-ttu-id="e071c-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="e071c-132">Requirement</span></span> | <span data-ttu-id="e071c-133">Valore</span><span class="sxs-lookup"><span data-stu-id="e071c-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e071c-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e071c-134">Header</span></span><br/>  | <dl> <span data-ttu-id="e071c-135"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e071c-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e071c-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="e071c-136">Library</span></span><br/> | <dl> <span data-ttu-id="e071c-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e071c-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e071c-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e071c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e071c-139">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="e071c-139">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="e071c-140">**ID3DXPRTEngine::ComputeSS**</span><span class="sxs-lookup"><span data-stu-id="e071c-140">**ID3DXPRTEngine::ComputeSS**</span></span>](id3dxprtengine--computess.md)
</dt> </dl>

 

 




