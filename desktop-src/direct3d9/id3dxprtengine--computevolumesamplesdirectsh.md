---
description: Calcola una proiezione di illuminazione distante in vettori di base armonica sferica (SH) che rappresentano la luminosità dell'evento imprevisto in posizioni specificate.
ms.assetid: 4d07b288-aec1-48eb-8d27-f3d7d8cfb69e
title: 'Metodo ID3DXPRTEngine:: ComputeVolumeSamplesDirectSH (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeVolumeSamplesDirectSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 757e227907eab73848f43b2b8e2f40f9b4b1071b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323451"
---
# <a name="id3dxprtenginecomputevolumesamplesdirectsh-method"></a><span data-ttu-id="17a72-103">Metodo ID3DXPRTEngine:: ComputeVolumeSamplesDirectSH</span><span class="sxs-lookup"><span data-stu-id="17a72-103">ID3DXPRTEngine::ComputeVolumeSamplesDirectSH method</span></span>

<span data-ttu-id="17a72-104">Calcola una proiezione di illuminazione distante in vettori di base armonica sferica (SH) che rappresentano la luminosità dell'evento imprevisto in posizioni specificate.</span><span class="sxs-lookup"><span data-stu-id="17a72-104">Computes a projection of distant lighting into spherical harmonic (SH) basis vectors that represent incident radiance at specified locations.</span></span>

## <a name="syntax"></a><span data-ttu-id="17a72-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="17a72-105">Syntax</span></span>


```C++
HRESULT ComputeVolumeSamplesDirectSH(
  [in]            UINT            OrderIn,
  [in]            UINT            OrderOut,
  [in]            UINT            NumVolSamples.xml,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="17a72-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="17a72-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17a72-107">*Ordinamento* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="17a72-107">*OrderIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17a72-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="17a72-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="17a72-109">Ordine della rappresentazione SH dell'illuminazione distante.</span><span class="sxs-lookup"><span data-stu-id="17a72-109">Order of the SH representation of distant lighting.</span></span> <span data-ttu-id="17a72-110">Deve essere compreso tra [D3DXSH \_ MINORDER](other-d3dx-constants.md) \_ e D3DXSH MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="17a72-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="17a72-111">Il grado della valutazione è orderin-1.</span><span class="sxs-lookup"><span data-stu-id="17a72-111">The degree of the evaluation is OrderIn - 1.</span></span>

</dd> <dt>

<span data-ttu-id="17a72-112">*Ordinamento* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="17a72-112">*OrderOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17a72-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="17a72-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="17a72-114">Ordine della rappresentazione SH dell'illuminazione locale.</span><span class="sxs-lookup"><span data-stu-id="17a72-114">Order of the SH representation of local lighting.</span></span> <span data-ttu-id="17a72-115">Deve essere compreso tra [D3DXSH \_ MINORDER](other-d3dx-constants.md) \_ e D3DXSH MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="17a72-115">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="17a72-116">Il grado della valutazione è Order out-1.</span><span class="sxs-lookup"><span data-stu-id="17a72-116">The degree of the evaluation is OrderOut - 1.</span></span>

</dd> <dt>

<span data-ttu-id="17a72-117">*NumVolSamples.xml* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="17a72-117">*NumVolSamples.xml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17a72-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="17a72-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="17a72-119">Numero di percorsi di esempio.</span><span class="sxs-lookup"><span data-stu-id="17a72-119">Number of sample locations.</span></span>

</dd> <dt>

<span data-ttu-id="17a72-120">*pSampleLocs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="17a72-120">*pSampleLocs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17a72-121">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="17a72-121">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="17a72-122">Posizione per ogni esempio.</span><span class="sxs-lookup"><span data-stu-id="17a72-122">Position for each sample.</span></span>

</dd> <dt>

<span data-ttu-id="17a72-123">*pDataOut* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="17a72-123">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="17a72-124">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="17a72-124">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="17a72-125">Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di output che proietta l'illuminazione distante in vettori di base sh.</span><span class="sxs-lookup"><span data-stu-id="17a72-125">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that projects the distant lighting into SH basis vectors.</span></span> <span data-ttu-id="17a72-126">Questo buffer deve avere il numero appropriato di canali di colore allocati per la simulazione.</span><span class="sxs-lookup"><span data-stu-id="17a72-126">This buffer must have the proper number of color channels allocated for the simulation.</span></span> <span data-ttu-id="17a72-127">Questo metodo genera un \* ordine in base al secondo per ogni canale in ogni posizione di esempio.</span><span class="sxs-lookup"><span data-stu-id="17a72-127">This method generates OrderIn² \* OrderOut"² scalars per channel at each sample location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17a72-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="17a72-128">Return value</span></span>

<span data-ttu-id="17a72-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="17a72-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="17a72-130">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="17a72-130">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="17a72-131">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="17a72-131">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="17a72-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="17a72-132">Remarks</span></span>

<span data-ttu-id="17a72-133">Questo metodo calcola il modo in cui la luce da un'origine distante arriva in ogni punto nello spazio specificato da pSampleLocs.</span><span class="sxs-lookup"><span data-stu-id="17a72-133">This method computes how light from a distant source arrives at each point in space specified by pSampleLocs.</span></span> <span data-ttu-id="17a72-134">I coefficienti SH rappresentano il mapping, a ogni punto di pSampleLocs, della luminosità del codice sorgente per l'evento imprevisto trasferito.</span><span class="sxs-lookup"><span data-stu-id="17a72-134">The SH coefficients represent the mapping, at each pSampleLocs point, of source radiance to transferred incident radiance.</span></span>

<span data-ttu-id="17a72-135">Per usare correttamente questo metodo, è necessario impostare il campionamento su una sfera con UseSphere = **true** e UseCosine = **false** in [**ID3DXPRTEngine:: SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md); in caso contrario, questo metodo restituirà un errore con D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="17a72-135">To use this method successfully, you must set sampling over a sphere with UseSphere = **TRUE** and UseCosine = **FALSE** in [**ID3DXPRTEngine::SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md); otherwise, this method will return an error with D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="17a72-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17a72-136">Requirements</span></span>



| <span data-ttu-id="17a72-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="17a72-137">Requirement</span></span> | <span data-ttu-id="17a72-138">Valore</span><span class="sxs-lookup"><span data-stu-id="17a72-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="17a72-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="17a72-139">Header</span></span><br/>  | <dl> <span data-ttu-id="17a72-140"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="17a72-140"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="17a72-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="17a72-141">Library</span></span><br/> | <dl> <span data-ttu-id="17a72-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17a72-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="17a72-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="17a72-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17a72-144">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="17a72-144">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="17a72-145">**ID3DXPRTEngine::ComputeVolumeSamples**</span><span class="sxs-lookup"><span data-stu-id="17a72-145">**ID3DXPRTEngine::ComputeVolumeSamples**</span></span>](id3dxprtengine--computevolumesamples.md)
</dt> </dl>

 

 
