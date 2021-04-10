---
description: Calcola il contributo di illuminazione diretta per gli oggetti 3D in cui la luminosità di origine è rappresentata da un'approssimazione armonica sferica (SH), usando il campionamento adattivo.
ms.assetid: 792d8460-d608-4384-ac1c-556435074580
title: 'Metodo ID3DXPRTEngine:: ComputeDirectLightingSHAdaptive (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSHAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8abbcfd955fa909166b53f6e050b9aff5837508d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762376"
---
# <a name="id3dxprtenginecomputedirectlightingshadaptive-method"></a><span data-ttu-id="e8543-103">Metodo ID3DXPRTEngine:: ComputeDirectLightingSHAdaptive</span><span class="sxs-lookup"><span data-stu-id="e8543-103">ID3DXPRTEngine::ComputeDirectLightingSHAdaptive method</span></span>

<span data-ttu-id="e8543-104">Calcola il contributo di illuminazione diretta per gli oggetti 3D in cui la luminosità di origine è rappresentata da un'approssimazione armonica sferica (SH), usando il campionamento adattivo.</span><span class="sxs-lookup"><span data-stu-id="e8543-104">Computes the direct lighting contribution to 3D objects where the source radiance is represented by a spherical harmonic (SH) approximation, using adaptive sampling.</span></span> <span data-ttu-id="e8543-105">Questo metodo genera nuovi vertici e visi sulla mesh per approssimare in modo più accurato il segnale PRT (pre-Computed Radiance Transfer).</span><span class="sxs-lookup"><span data-stu-id="e8543-105">This method generates new vertices and faces on the mesh to more accurately approximate the precomputed radiance transfer (PRT) signal.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8543-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8543-106">Syntax</span></span>


```C++
HRESULT ComputeDirectLightingSHAdaptive(
  [in]      UINT            Order,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="e8543-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="e8543-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8543-108">*Ordine* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="e8543-108">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8543-109">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e8543-109">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e8543-110">Ordine della valutazione SH.</span><span class="sxs-lookup"><span data-stu-id="e8543-110">Order of the SH evaluation.</span></span> <span data-ttu-id="e8543-111">Deve essere compreso tra [D3DXSH \_ MINORDER](other-d3dx-constants.md) \_ e D3DXSH MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="e8543-111">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="e8543-112">La valutazione genera coefficienti Order ².</span><span class="sxs-lookup"><span data-stu-id="e8543-112">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="e8543-113">Il livello della valutazione è Order-1.</span><span class="sxs-lookup"><span data-stu-id="e8543-113">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="e8543-114">*AdaptiveThresh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8543-114">*AdaptiveThresh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8543-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e8543-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e8543-116">Soglia sul vettore PRT da usare per la suddivisione dei vertici e delle facce mesh.</span><span class="sxs-lookup"><span data-stu-id="e8543-116">Threshold on the PRT vector to use for subdividing mesh vertices and faces.</span></span> <span data-ttu-id="e8543-117">Se è minore di 1e-6F, viene specificato un valore predefinito di 1e-6F.</span><span class="sxs-lookup"><span data-stu-id="e8543-117">If less than 1e-6f, a default value of 1e-6f is specified.</span></span>

</dd> <dt>

<span data-ttu-id="e8543-118">*MinEdgeLength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8543-118">*MinEdgeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8543-119">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e8543-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e8543-120">Lunghezza minima del bordo della superficie che verrà generata nel campionamento adattivo.</span><span class="sxs-lookup"><span data-stu-id="e8543-120">Minimum face edge length that will be generated in adaptive sampling.</span></span> <span data-ttu-id="e8543-121">Se il metodo determina che il valore è troppo piccolo, viene specificato un valore dipendente dal modello.</span><span class="sxs-lookup"><span data-stu-id="e8543-121">If the method determines that the value is too small, a model-dependent value is specified.</span></span> <span data-ttu-id="e8543-122">Se è zero, viene specificato un valore predefinito pari a 4.</span><span class="sxs-lookup"><span data-stu-id="e8543-122">If zero, a default value of 4 is specified.</span></span>

</dd> <dt>

<span data-ttu-id="e8543-123">*MaxSubdiv* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8543-123">*MaxSubdiv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8543-124">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e8543-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e8543-125">Livello massimo di suddivisione di una faccia che verrà utilizzata nel campionamento adattivo.</span><span class="sxs-lookup"><span data-stu-id="e8543-125">Maximum level of subdivision of a face that will be used in adaptive sampling.</span></span>

</dd> <dt>

<span data-ttu-id="e8543-126">*pDataOut* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="e8543-126">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8543-127">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="e8543-127">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="e8543-128">Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di output.</span><span class="sxs-lookup"><span data-stu-id="e8543-128">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span> <span data-ttu-id="e8543-129">Questo buffer deve avere il numero appropriato di canali di colore allocati per la simulazione.</span><span class="sxs-lookup"><span data-stu-id="e8543-129">This buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8543-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e8543-130">Return value</span></span>

<span data-ttu-id="e8543-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e8543-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e8543-132">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e8543-132">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e8543-133">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="e8543-133">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8543-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8543-134">Requirements</span></span>



| <span data-ttu-id="e8543-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8543-135">Requirement</span></span> | <span data-ttu-id="e8543-136">Valore</span><span class="sxs-lookup"><span data-stu-id="e8543-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8543-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e8543-137">Header</span></span><br/>  | <dl> <span data-ttu-id="e8543-138"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8543-138"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e8543-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="e8543-139">Library</span></span><br/> | <dl> <span data-ttu-id="e8543-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e8543-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e8543-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8543-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8543-142">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="e8543-142">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="e8543-143">**ID3DXPRTEngine::RobustMeshRefine**</span><span class="sxs-lookup"><span data-stu-id="e8543-143">**ID3DXPRTEngine::RobustMeshRefine**</span></span>](id3dxprtengine--robustmeshrefine.md)
</dt> </dl>

 

 
