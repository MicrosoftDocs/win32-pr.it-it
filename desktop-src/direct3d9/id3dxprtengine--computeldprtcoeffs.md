---
description: Consente di calcolare i coefficienti LDPRT (precomputed Radiance Transfer) a livello locale rispetto ai vettori normali per campione per ridurre al minimo l'errore dei minimi quadrati rispetto ai dati ID3DXPRTBuffer di input.
ms.assetid: 302c20cd-d495-4a23-9692-7456355471eb
title: 'Metodo ID3DXPRTEngine:: ComputeLDPRTCoeffs (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeLDPRTCoeffs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 351ecb8022e06b1a5a24abad8fa8541798d13ba0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323684"
---
# <a name="id3dxprtenginecomputeldprtcoeffs-method"></a><span data-ttu-id="1ffa2-103">Metodo ID3DXPRTEngine:: ComputeLDPRTCoeffs</span><span class="sxs-lookup"><span data-stu-id="1ffa2-103">ID3DXPRTEngine::ComputeLDPRTCoeffs method</span></span>

<span data-ttu-id="1ffa2-104">Consente di calcolare i coefficienti LDPRT (precomputed Radiance Transfer) a livello locale rispetto ai vettori normali per campione per ridurre al minimo l'errore dei minimi quadrati rispetto ai dati [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di input.</span><span class="sxs-lookup"><span data-stu-id="1ffa2-104">Computes locally-deformable precomputed radiance transfer (LDPRT) coefficients relative to per-sample normal vectors to minimize the least-squares error with respect to input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) data.</span></span> <span data-ttu-id="1ffa2-105">Questi coefficienti possono essere usati con vettori normali o trasformati per modellare gli effetti globali sugli oggetti dinamici.</span><span class="sxs-lookup"><span data-stu-id="1ffa2-105">These coefficients can be used with skinned or transformed normal vectors to model global effects on dynamic objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ffa2-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1ffa2-106">Syntax</span></span>


```C++
HRESULT ComputeLDPRTCoeffs(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      UINT            Order,
  [in, out] D3DXVECTOR3     *pNormOut,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="1ffa2-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="1ffa2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ffa2-108">*pDataIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ffa2-108">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ffa2-109">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="1ffa2-109">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="1ffa2-110">Puntatore a un oggetto dati PRT (pre-Computed Radiance Transfer) di input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="1ffa2-110">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) spherical harmonic (SH) precomputed radiance transfer (PRT) data object.</span></span>

</dd> <dt>

<span data-ttu-id="1ffa2-111">*Ordine* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="1ffa2-111">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ffa2-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ffa2-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ffa2-113">Ordine della valutazione SH.</span><span class="sxs-lookup"><span data-stu-id="1ffa2-113">Order of the SH evaluation.</span></span> <span data-ttu-id="1ffa2-114">Deve essere compreso tra [D3DXSH \_ MINORDER](other-d3dx-constants.md) \_ e D3DXSH MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="1ffa2-114">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="1ffa2-115">La valutazione genera coefficienti Order ².</span><span class="sxs-lookup"><span data-stu-id="1ffa2-115">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="1ffa2-116">Il livello della valutazione è Order-1.</span><span class="sxs-lookup"><span data-stu-id="1ffa2-116">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="1ffa2-117">*pNormOut* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="1ffa2-117">*pNormOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ffa2-118">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="1ffa2-118">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1ffa2-119">Matrice di vettori facoltativa che deve essere riempita con vettori normali ottimali dello shader per i quali sono ottimizzati i coefficienti LDPRT.</span><span class="sxs-lookup"><span data-stu-id="1ffa2-119">Optional vector array to be filled with shader-optimal normal vectors for which LDPRT coefficients are optimized.</span></span> <span data-ttu-id="1ffa2-120">Questa matrice deve avere le stesse dimensioni del numero di campioni in pDataIn.</span><span class="sxs-lookup"><span data-stu-id="1ffa2-120">This array must be the same size as the number of samples in pDataIn.</span></span> <span data-ttu-id="1ffa2-121">Se **null**, vengono usati i vettori normali della superficie.</span><span class="sxs-lookup"><span data-stu-id="1ffa2-121">If **NULL**, surface normal vectors are used.</span></span>

</dd> <dt>

<span data-ttu-id="1ffa2-122">*pDataOut* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="1ffa2-122">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ffa2-123">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="1ffa2-123">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="1ffa2-124">Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di output che contiene i coefficienti armonici di zona dell'ordine per canale di colore per campione.</span><span class="sxs-lookup"><span data-stu-id="1ffa2-124">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that contains Order zonal harmonic coefficients per color channel per sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ffa2-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1ffa2-125">Return value</span></span>

<span data-ttu-id="1ffa2-126">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1ffa2-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1ffa2-127">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1ffa2-127">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1ffa2-128">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="1ffa2-128">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ffa2-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="1ffa2-129">Remarks</span></span>

<span data-ttu-id="1ffa2-130">Con questo metodo è possibile ottenere facoltativamente soluzioni per l'ombreggiatura di vettori normali.</span><span class="sxs-lookup"><span data-stu-id="1ffa2-130">Solutions for shading normal vectors can optionally be obtained with this method.</span></span> <span data-ttu-id="1ffa2-131">Questi vettori normali, insieme ai coefficienti LDPRT, possono rappresentare più accuratamente il segnale PRT.</span><span class="sxs-lookup"><span data-stu-id="1ffa2-131">These normal vectors, along with the LDPRT coefficients, can more accurately represent the PRT signal.</span></span> <span data-ttu-id="1ffa2-132">In questo caso, i coefficienti rappresentano le armoniche di zona orientate nella direzione normale.</span><span class="sxs-lookup"><span data-stu-id="1ffa2-132">In this case, the coefficients represent zonal harmonics oriented in the normal direction.</span></span>

<span data-ttu-id="1ffa2-133">Questo metodo non può essere usato con i risultati di [**ID3DXPRTEngine:: ComputeSurfSamplesBounce**](id3dxprtengine--computesurfsamplesbounce.md) o [**ID3DXPRTEngine:: ComputeSurfSamplesDirectSH**](id3dxprtengine--computesurfsamplesdirectsh.md).</span><span class="sxs-lookup"><span data-stu-id="1ffa2-133">This method cannot be used with results from [**ID3DXPRTEngine::ComputeSurfSamplesBounce**](id3dxprtengine--computesurfsamplesbounce.md) or [**ID3DXPRTEngine::ComputeSurfSamplesDirectSH**](id3dxprtengine--computesurfsamplesdirectsh.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1ffa2-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ffa2-134">Requirements</span></span>



| <span data-ttu-id="1ffa2-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ffa2-135">Requirement</span></span> | <span data-ttu-id="1ffa2-136">Valore</span><span class="sxs-lookup"><span data-stu-id="1ffa2-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ffa2-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1ffa2-137">Header</span></span><br/>  | <dl> <span data-ttu-id="1ffa2-138"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ffa2-138"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1ffa2-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="1ffa2-139">Library</span></span><br/> | <dl> <span data-ttu-id="1ffa2-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ffa2-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1ffa2-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ffa2-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ffa2-142">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="1ffa2-142">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
