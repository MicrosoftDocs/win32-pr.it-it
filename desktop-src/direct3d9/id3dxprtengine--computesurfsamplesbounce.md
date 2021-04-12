---
description: Calcola gli esempi di trasferimento di radianza (PRT) pre-calcolati per un punto arbitrario (e il vettore normale).
ms.assetid: 862a9067-5c5e-4428-86f4-ebef653411b9
title: 'Metodo ID3DXPRTEngine:: ComputeSurfSamplesBounce (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSurfSamplesBounce
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 55cea3e87850273b6ea8d190422bd77afeb831f4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356054"
---
# <a name="id3dxprtenginecomputesurfsamplesbounce-method"></a><span data-ttu-id="86691-103">Metodo ID3DXPRTEngine:: ComputeSurfSamplesBounce</span><span class="sxs-lookup"><span data-stu-id="86691-103">ID3DXPRTEngine::ComputeSurfSamplesBounce method</span></span>

<span data-ttu-id="86691-104">Calcola gli esempi di trasferimento di radianza (PRT) pre-calcolati per un punto arbitrario (e il vettore normale).</span><span class="sxs-lookup"><span data-stu-id="86691-104">Computes precomputed radiance transfer (PRT) samples for an arbitrary point (and normal vector).</span></span>

## <a name="syntax"></a><span data-ttu-id="86691-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="86691-105">Syntax</span></span>


```C++
HRESULT ComputeSurfSamplesBounce(
  [in]            LPD3DXPRTBUFFER pSurfDataIn,
  [in]            UINT            NumSamples,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in]      const D3DXVECTOR3     *pSampleNorms,
  [in, out]       LPD3DXPRTBUFFER pDataOut,
  [in, out]       LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a><span data-ttu-id="86691-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="86691-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86691-107">*pSurfDataIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="86691-107">*pSurfDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86691-108">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="86691-108">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="86691-109">Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di input che rappresenta il Radiance di origine dell'oggetto 3D.</span><span class="sxs-lookup"><span data-stu-id="86691-109">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the source radiance of the 3D object.</span></span> <span data-ttu-id="86691-110">Questo buffer di input deve avere il numero appropriato di canali di colore allocati per la simulazione.</span><span class="sxs-lookup"><span data-stu-id="86691-110">This input buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="86691-111">*NumSamples valore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="86691-111">*NumSamples* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86691-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="86691-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="86691-113">Numero di percorsi di esempio.</span><span class="sxs-lookup"><span data-stu-id="86691-113">Number of sample locations.</span></span>

</dd> <dt>

<span data-ttu-id="86691-114">*pSampleLocs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="86691-114">*pSampleLocs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86691-115">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="86691-115">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="86691-116">Posizione per ogni esempio.</span><span class="sxs-lookup"><span data-stu-id="86691-116">Position for each sample.</span></span>

</dd> <dt>

<span data-ttu-id="86691-117">*pSampleNorms* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="86691-117">*pSampleNorms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86691-118">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="86691-118">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="86691-119">Vettore normale per ogni posizione di esempio.</span><span class="sxs-lookup"><span data-stu-id="86691-119">Normal vector for each sample location.</span></span>

</dd> <dt>

<span data-ttu-id="86691-120">*pDataOut* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="86691-120">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="86691-121">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="86691-121">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="86691-122">Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di output che modella il contributo di illuminazione diretta al punto, usando l'approssimazione dell'armonica sferica (SH).</span><span class="sxs-lookup"><span data-stu-id="86691-122">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models the direct lighting contribution to the point, using the spherical harmonic (SH) approximation.</span></span>

</dd> <dt>

<span data-ttu-id="86691-123">*pDataTotal* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="86691-123">*pDataTotal* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="86691-124">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="86691-124">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="86691-125">Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) facoltativo che corrisponde alla somma in corso di tutti gli output pDataOut precedenti.</span><span class="sxs-lookup"><span data-stu-id="86691-125">Pointer to an optional [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that is the running sum of all previous pDataOut outputs.</span></span> <span data-ttu-id="86691-126">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="86691-126">May be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86691-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="86691-127">Return value</span></span>

<span data-ttu-id="86691-128">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="86691-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="86691-129">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="86691-129">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="86691-130">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="86691-130">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="86691-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86691-131">Requirements</span></span>



| <span data-ttu-id="86691-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="86691-132">Requirement</span></span> | <span data-ttu-id="86691-133">Valore</span><span class="sxs-lookup"><span data-stu-id="86691-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="86691-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="86691-134">Header</span></span><br/>  | <dl> <span data-ttu-id="86691-135"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="86691-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="86691-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="86691-136">Library</span></span><br/> | <dl> <span data-ttu-id="86691-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86691-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="86691-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="86691-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86691-139">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="86691-139">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="86691-140">**ID3DXPRTEngine::ComputeSurfSamplesDirectSH**</span><span class="sxs-lookup"><span data-stu-id="86691-140">**ID3DXPRTEngine::ComputeSurfSamplesDirectSH**</span></span>](id3dxprtengine--computesurfsamplesdirectsh.md)
</dt> </dl>

 

 
