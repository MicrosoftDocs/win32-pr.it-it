---
description: Calcola il contributo di illuminazione diretta agli oggetti 3D in cui la luminosità di origine è rappresentata da un'approssimazione di un'armonica sferica (SH).
ms.assetid: 52d614cc-578a-4f2b-ba91-70d0c4371042
title: 'Metodo ID3DXPRTEngine:: ComputeDirectLightingSH (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 01b6c3cff082c40c4df5d9bee1d997599a41965b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323686"
---
# <a name="id3dxprtenginecomputedirectlightingsh-method"></a><span data-ttu-id="824e2-103">Metodo ID3DXPRTEngine:: ComputeDirectLightingSH</span><span class="sxs-lookup"><span data-stu-id="824e2-103">ID3DXPRTEngine::ComputeDirectLightingSH method</span></span>

<span data-ttu-id="824e2-104">Calcola il contributo di illuminazione diretta agli oggetti 3D in cui la luminosità di origine è rappresentata da un'approssimazione di un'armonica sferica (SH).</span><span class="sxs-lookup"><span data-stu-id="824e2-104">Computes the direct lighting contribution to 3D objects where the source radiance is represented by a spherical harmonic (SH) approximation.</span></span>

## <a name="syntax"></a><span data-ttu-id="824e2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="824e2-105">Syntax</span></span>


```C++
HRESULT ComputeDirectLightingSH(
  [in]      UINT            Order,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="824e2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="824e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="824e2-107">*Ordine* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="824e2-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="824e2-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="824e2-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="824e2-109">Ordine della valutazione SH.</span><span class="sxs-lookup"><span data-stu-id="824e2-109">Order of the SH evaluation.</span></span> <span data-ttu-id="824e2-110">Deve essere compreso tra [D3DXSH \_ MINORDER](other-d3dx-constants.md) \_ e D3DXSH MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="824e2-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="824e2-111">La valutazione genera coefficienti Order ².</span><span class="sxs-lookup"><span data-stu-id="824e2-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="824e2-112">Il livello della valutazione è Order-1.</span><span class="sxs-lookup"><span data-stu-id="824e2-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="824e2-113">*pDataOut* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="824e2-113">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="824e2-114">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="824e2-114">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="824e2-115">Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di output che modella il contributo di illuminazione diretta con l'approssimazione sh.</span><span class="sxs-lookup"><span data-stu-id="824e2-115">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models the direct lighting contribution with the SH approximation.</span></span> <span data-ttu-id="824e2-116">Questo buffer deve avere il numero appropriato di canali di colore allocati per la simulazione.</span><span class="sxs-lookup"><span data-stu-id="824e2-116">This buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="824e2-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="824e2-117">Return value</span></span>

<span data-ttu-id="824e2-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="824e2-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="824e2-119">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="824e2-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="824e2-120">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="824e2-120">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="824e2-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="824e2-121">Remarks</span></span>

<span data-ttu-id="824e2-122">L'output non include l'albedo e solo la luce in ingresso è integrata nel simulatore.</span><span class="sxs-lookup"><span data-stu-id="824e2-122">The output does not include albedo, and only incoming light is integrated in the simulator.</span></span> <span data-ttu-id="824e2-123">Se non si moltiplica l'albedo, è possibile modellare la variazione dell'albedo a una scala più sottile rispetto alla luminosità di origine, ottenendo così risultati più accurati dalla compressione.</span><span class="sxs-lookup"><span data-stu-id="824e2-123">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="824e2-124">Chiamare [**ID3DXPRTEngine:: MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) per moltiplicare ogni vettore di traslazione di radiazione (PRT) pre-calcolato per l'albedo.</span><span class="sxs-lookup"><span data-stu-id="824e2-124">Call [**ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) to multiply each precomputed radiance transfer (PRT) vector by the albedo.</span></span>

## <a name="requirements"></a><span data-ttu-id="824e2-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="824e2-125">Requirements</span></span>



| <span data-ttu-id="824e2-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="824e2-126">Requirement</span></span> | <span data-ttu-id="824e2-127">Valore</span><span class="sxs-lookup"><span data-stu-id="824e2-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="824e2-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="824e2-128">Header</span></span><br/>  | <dl> <span data-ttu-id="824e2-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="824e2-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="824e2-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="824e2-130">Library</span></span><br/> | <dl> <span data-ttu-id="824e2-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="824e2-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="824e2-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="824e2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="824e2-133">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="824e2-133">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
