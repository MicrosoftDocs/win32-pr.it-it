---
description: Calcola una proiezione dell'illuminazione diretta dal rimbalzo della luce precedente in vettori di base armonici sferici che rappresentano la radianza dell'evento imprevisto nelle posizioni specificate.
ms.assetid: ccde7c59-cb82-4d61-822a-e1e9ecea0a28
title: 'Metodo ID3DXPRTEngine:: ComputeVolumeSamples (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeVolumeSamples
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bd77fff723f0cf7e3dc2a52be6a40ff6f0d71fe1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323452"
---
# <a name="id3dxprtenginecomputevolumesamples-method"></a><span data-ttu-id="fe372-103">Metodo ID3DXPRTEngine:: ComputeVolumeSamples</span><span class="sxs-lookup"><span data-stu-id="fe372-103">ID3DXPRTEngine::ComputeVolumeSamples method</span></span>

<span data-ttu-id="fe372-104">Calcola una proiezione dell'illuminazione diretta dal rimbalzo della luce precedente in vettori di base armonici sferici che rappresentano la radianza dell'evento imprevisto nelle posizioni specificate.</span><span class="sxs-lookup"><span data-stu-id="fe372-104">Computes a projection of the direct lighting from the previous light bounce into spherical harmonic (SH) basis vectors that represent incident radiance at specified locations.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe372-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe372-105">Syntax</span></span>


```C++
HRESULT ComputeVolumeSamples(
  [in]            LPD3DXPRTBUFFER pSurfDataIn,
  [in]            UINT            Order,
  [in]            UINT            NumVolSamples.xml,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="fe372-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe372-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe372-107">*pSurfDataIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe372-107">*pSurfDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe372-108">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="fe372-108">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="fe372-109">Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di input che rappresenta l'oggetto 3D del rimbalzo della luce precedente.</span><span class="sxs-lookup"><span data-stu-id="fe372-109">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the 3D object from the previous light bounce.</span></span>

</dd> <dt>

<span data-ttu-id="fe372-110">*Ordine* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="fe372-110">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe372-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fe372-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fe372-112">Ordine della valutazione SH.</span><span class="sxs-lookup"><span data-stu-id="fe372-112">Order of the SH evaluation.</span></span> <span data-ttu-id="fe372-113">Deve essere compreso tra [D3DXSH \_ MINORDER](other-d3dx-constants.md) \_ e D3DXSH MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="fe372-113">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="fe372-114">La valutazione genera coefficienti Order ².</span><span class="sxs-lookup"><span data-stu-id="fe372-114">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="fe372-115">Il livello della valutazione è Order-1.</span><span class="sxs-lookup"><span data-stu-id="fe372-115">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="fe372-116">*NumVolSamples.xml* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe372-116">*NumVolSamples.xml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe372-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fe372-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fe372-118">Numero di percorsi di esempio.</span><span class="sxs-lookup"><span data-stu-id="fe372-118">Number of sample locations.</span></span>

</dd> <dt>

<span data-ttu-id="fe372-119">*pSampleLocs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe372-119">*pSampleLocs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe372-120">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="fe372-120">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="fe372-121">Posizione per ogni esempio.</span><span class="sxs-lookup"><span data-stu-id="fe372-121">Position for each sample.</span></span> <span data-ttu-id="fe372-122">Se pSampleLocs è **null**, ComputeVolumeSamples calcolerà le matrici di trasferimento a ogni vertice di rete.</span><span class="sxs-lookup"><span data-stu-id="fe372-122">If pSampleLocs is **NULL**, ComputeVolumeSamples will compute transfer matrices at every mesh vertex.</span></span> <span data-ttu-id="fe372-123">Tuttavia, se pSampleLocs non è **null**, è necessario campionare su una sfera (set UseSphere = **true** e UseCosine = **false** in [**ID3DXPRTEngine:: SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md)); in caso contrario, ComputeVolumeSamples restituirà D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="fe372-123">However, if pSampleLocs is not **NULL**, you must sample over a sphere (set UseSphere = **TRUE** and UseCosine = **FALSE** in [**ID3DXPRTEngine::SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md)); otherwise, ComputeVolumeSamples will return D3DERR\_INVALIDCALL.</span></span>

</dd> <dt>

<span data-ttu-id="fe372-124">*pDataOut* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="fe372-124">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe372-125">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="fe372-125">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="fe372-126">Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di output che proietta l'illuminazione diretta dal rimbalzo della luce precedente nei vettori di base sh.</span><span class="sxs-lookup"><span data-stu-id="fe372-126">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that projects the direct lighting from the previous light bounce into SH basis vectors.</span></span> <span data-ttu-id="fe372-127">Questo buffer deve avere il numero appropriato di canali di colore allocati per la simulazione.</span><span class="sxs-lookup"><span data-stu-id="fe372-127">This buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe372-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fe372-128">Return value</span></span>

<span data-ttu-id="fe372-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fe372-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fe372-130">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fe372-130">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fe372-131">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="fe372-131">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe372-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="fe372-132">Remarks</span></span>

<span data-ttu-id="fe372-133">Questo metodo calcola il modo in cui la luce della funzione di luminosità di origine viene riflessa dalla superficie che rappresenta la scena (pSurfDataIn) e arriva a ogni punto nello spazio specificato da pSampleLocs.</span><span class="sxs-lookup"><span data-stu-id="fe372-133">This method computes how the light from the source radiance function is reflected off the surface that represents the scene (pSurfDataIn) and arrives at each point in space specified by pSampleLocs.</span></span> <span data-ttu-id="fe372-134">I coefficienti SH rappresentano il mapping, a ogni punto di pSampleLocs, della luminosità del codice sorgente per l'evento imprevisto trasferito.</span><span class="sxs-lookup"><span data-stu-id="fe372-134">The SH coefficients represent the mapping, at each pSampleLocs point, of source radiance to transferred incident radiance.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe372-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe372-135">Requirements</span></span>



| <span data-ttu-id="fe372-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe372-136">Requirement</span></span> | <span data-ttu-id="fe372-137">Valore</span><span class="sxs-lookup"><span data-stu-id="fe372-137">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe372-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fe372-138">Header</span></span><br/>  | <dl> <span data-ttu-id="fe372-139"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe372-139"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="fe372-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="fe372-140">Library</span></span><br/> | <dl> <span data-ttu-id="fe372-141"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe372-141"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fe372-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe372-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe372-143">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="fe372-143">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="fe372-144">**ID3DXPRTEngine::ComputeVolumeSamplesDirectSH**</span><span class="sxs-lookup"><span data-stu-id="fe372-144">**ID3DXPRTEngine::ComputeVolumeSamplesDirectSH**</span></span>](id3dxprtengine--computevolumesamplesdirectsh.md)
</dt> </dl>

 

 
