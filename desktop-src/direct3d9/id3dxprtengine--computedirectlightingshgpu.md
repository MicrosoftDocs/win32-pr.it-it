---
description: Usa la GPU per calcolare il contributo di illuminazione diretta agli oggetti 3D in cui la luminosità di origine è rappresentata da un'approssimazione di un'armonica sferica (SH). Il calcolo dell'illuminazione sulla GPU sarà in genere molto più veloce rispetto alla CPU.
ms.assetid: ccea5a5e-23f1-4fdf-bce8-9bfc35d45257
title: 'Metodo ID3DXPRTEngine:: ComputeDirectLightingSHGPU (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSHGPU
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e56dd807d28ba6952cd20c971b675b83687a3015
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323685"
---
# <a name="id3dxprtenginecomputedirectlightingshgpu-method"></a><span data-ttu-id="21f9b-104">Metodo ID3DXPRTEngine:: ComputeDirectLightingSHGPU</span><span class="sxs-lookup"><span data-stu-id="21f9b-104">ID3DXPRTEngine::ComputeDirectLightingSHGPU method</span></span>

<span data-ttu-id="21f9b-105">Usa la GPU per calcolare il contributo di illuminazione diretta agli oggetti 3D in cui la luminosità di origine è rappresentata da un'approssimazione di un'armonica sferica (SH).</span><span class="sxs-lookup"><span data-stu-id="21f9b-105">Uses the GPU to compute the direct lighting contribution to 3D objects where the source radiance is represented by a spherical harmonic (SH) approximation.</span></span> <span data-ttu-id="21f9b-106">Il calcolo dell'illuminazione sulla GPU sarà in genere molto più veloce rispetto alla CPU.</span><span class="sxs-lookup"><span data-stu-id="21f9b-106">Computing the lighting on the GPU will generally be much faster than on the CPU.</span></span>

## <a name="syntax"></a><span data-ttu-id="21f9b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="21f9b-107">Syntax</span></span>


```C++
HRESULT ComputeDirectLightingSHGPU(
  [in]      LPDIRECT3DDEVICE9 pDevice,
  [in]      UINT              Flags,
  [in]      UINT              Order,
  [in]      FLOAT             ZBias,
  [in]      FLOAT             ZAngleBias,
  [in, out] LPD3DXPRTBUFFER   pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="21f9b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="21f9b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21f9b-109">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21f9b-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21f9b-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="21f9b-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="21f9b-111">Puntatore all'oggetto dispositivo [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) usato per eseguire la simulazione sulla GPU.</span><span class="sxs-lookup"><span data-stu-id="21f9b-111">Pointer to the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) device object used to run the simulation on the GPU.</span></span> <span data-ttu-id="21f9b-112">Il dispositivo deve supportare i pixel shader [PS \_ 2 \_ 0](../direct3dhlsl/dx9-graphics-reference-asm-ps-2-0.md) .</span><span class="sxs-lookup"><span data-stu-id="21f9b-112">The device must support [ps\_2\_0](../direct3dhlsl/dx9-graphics-reference-asm-ps-2-0.md) pixel shaders.</span></span>

> [!Note]  
> <span data-ttu-id="21f9b-113">Le funzioni di callback non devono usare l'oggetto dispositivo [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) usato dal simulatore della GPU.</span><span class="sxs-lookup"><span data-stu-id="21f9b-113">Callback functions should not use the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) device object used by the GPU simulator.</span></span>

 

</dd> <dt>

<span data-ttu-id="21f9b-114">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21f9b-114">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21f9b-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="21f9b-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="21f9b-116">Parametro di simulazione GPU che definisce la risoluzione del buffer z dell'ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="21f9b-116">GPU simulation parameter that defines the resolution of the shadow z-buffer.</span></span> <span data-ttu-id="21f9b-117">Deve essere impostato su uno dei valori costanti di [**D3DXSHGPUSIMOPT**](./d3dxshgpusimopt.md).</span><span class="sxs-lookup"><span data-stu-id="21f9b-117">Should be set to one of the constant values from [**D3DXSHGPUSIMOPT**](./d3dxshgpusimopt.md).</span></span> <span data-ttu-id="21f9b-118">Per specificare una simulazione di precisione più elevata, il \_ valore Highquality di D3DXSHGPUSIMOPT può essere combinato con uno dei \_ valori SHADOWRESXXX di D3DXSHGPUSIMOPT.</span><span class="sxs-lookup"><span data-stu-id="21f9b-118">To specifiy higher precision simulation, the D3DXSHGPUSIMOPT\_HIGHQUALITY value may be combined with one of the D3DXSHGPUSIMOPT\_SHADOWRESxxx values.</span></span>

</dd> <dt>

<span data-ttu-id="21f9b-119">*Ordine* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="21f9b-119">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21f9b-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="21f9b-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="21f9b-121">Ordine della valutazione SH.</span><span class="sxs-lookup"><span data-stu-id="21f9b-121">Order of the SH evaluation.</span></span> <span data-ttu-id="21f9b-122">Deve essere compreso tra [D3DXSH \_ MINORDER](other-d3dx-constants.md) \_ e D3DXSH MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="21f9b-122">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="21f9b-123">La valutazione genera coefficienti Order ².</span><span class="sxs-lookup"><span data-stu-id="21f9b-123">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="21f9b-124">Il livello della valutazione è Order-1.</span><span class="sxs-lookup"><span data-stu-id="21f9b-124">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="21f9b-125">*ZBias* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21f9b-125">*ZBias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21f9b-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="21f9b-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="21f9b-127">Distorsione nella direzione normale.</span><span class="sxs-lookup"><span data-stu-id="21f9b-127">Bias in the normal direction.</span></span>

</dd> <dt>

<span data-ttu-id="21f9b-128">*ZAngleBias* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21f9b-128">*ZAngleBias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21f9b-129">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="21f9b-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="21f9b-130">Distorsione nella direzione normale, ridimensionata di uno meno il coseno dell'angolo con il raggio chiaro.</span><span class="sxs-lookup"><span data-stu-id="21f9b-130">Bias in the normal direction, scaled by one minus the cosine of the angle with the light ray.</span></span>

</dd> <dt>

<span data-ttu-id="21f9b-131">*pDataOut* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="21f9b-131">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="21f9b-132">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="21f9b-132">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="21f9b-133">Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="21f9b-133">Pointer to an [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span> <span data-ttu-id="21f9b-134">Questo buffer deve avere il numero appropriato di canali di colore allocati per la simulazione.</span><span class="sxs-lookup"><span data-stu-id="21f9b-134">This buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21f9b-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="21f9b-135">Return value</span></span>

<span data-ttu-id="21f9b-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="21f9b-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="21f9b-137">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="21f9b-137">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="21f9b-138">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="21f9b-138">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="21f9b-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="21f9b-139">Remarks</span></span>

<span data-ttu-id="21f9b-140">In questo metodo, l'albedo non viene moltiplicato per il segnale chiaro e solo la luce in ingresso è integrata nel simulatore.</span><span class="sxs-lookup"><span data-stu-id="21f9b-140">In this method, the albedo is not multiplied by the light signal, and only incoming light is integrated in the simulator.</span></span> <span data-ttu-id="21f9b-141">Se non si moltiplica l'albedo, è possibile modellare la variazione dell'albedo a una scala più sottile rispetto alla luminosità di origine, ottenendo così risultati più accurati dalla compressione.</span><span class="sxs-lookup"><span data-stu-id="21f9b-141">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="21f9b-142">Chiamare [**MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) per moltiplicare ogni vettore di traslazione di radiazione (PRT) pre-calcolato per l'albedo.</span><span class="sxs-lookup"><span data-stu-id="21f9b-142">Call [**MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) to multiply each precomputed radiance transfer (PRT) vector by the albedo.</span></span>

## <a name="requirements"></a><span data-ttu-id="21f9b-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21f9b-143">Requirements</span></span>



| <span data-ttu-id="21f9b-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="21f9b-144">Requirement</span></span> | <span data-ttu-id="21f9b-145">Valore</span><span class="sxs-lookup"><span data-stu-id="21f9b-145">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="21f9b-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="21f9b-146">Header</span></span><br/>  | <dl> <span data-ttu-id="21f9b-147"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="21f9b-147"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="21f9b-148">Libreria</span><span class="sxs-lookup"><span data-stu-id="21f9b-148">Library</span></span><br/> | <dl> <span data-ttu-id="21f9b-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="21f9b-149"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="21f9b-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21f9b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21f9b-151">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="21f9b-151">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
