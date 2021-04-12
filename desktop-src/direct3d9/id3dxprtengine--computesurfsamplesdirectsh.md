---
description: Calcola, in un punto arbitrario non su una mesh, un vettore di trasferimento che esegue il mapping della luminosità del codice sorgente, rappresentata da un'approssimazione ad armonica sferica (SH), per uscire dallo splendore.
ms.assetid: 44790465-440d-4426-b780-ed872fbf8efb
title: 'Metodo ID3DXPRTEngine:: ComputeSurfSamplesDirectSH (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSurfSamplesDirectSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 03adb1729a8a2e771ea681ccbdd180999d3adcbf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356044"
---
# <a name="id3dxprtenginecomputesurfsamplesdirectsh-method"></a><span data-ttu-id="8f5c1-103">Metodo ID3DXPRTEngine:: ComputeSurfSamplesDirectSH</span><span class="sxs-lookup"><span data-stu-id="8f5c1-103">ID3DXPRTEngine::ComputeSurfSamplesDirectSH method</span></span>

<span data-ttu-id="8f5c1-104">Calcola, in un punto arbitrario non su una mesh, un vettore di trasferimento che esegue il mapping della luminosità del codice sorgente, rappresentata da un'approssimazione ad armonica sferica (SH), per uscire dallo splendore.</span><span class="sxs-lookup"><span data-stu-id="8f5c1-104">Computes, at an arbitrary point not on a mesh, a transfer vector that maps source radiance (represented by a spherical harmonic (SH) approximation) to exit radiance.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f5c1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8f5c1-105">Syntax</span></span>


```C++
HRESULT ComputeSurfSamplesDirectSH(
  [in]            UINT            SHOrder,
  [in]            UINT            NumSamples,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in]      const D3DXVECTOR3     *pSampleNorms,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="8f5c1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8f5c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f5c1-107">*SHOrder* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8f5c1-107">*SHOrder* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f5c1-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8f5c1-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8f5c1-109">Ordine dell'approssimazione SH da usare.</span><span class="sxs-lookup"><span data-stu-id="8f5c1-109">Order of the SH approximation to use.</span></span>

</dd> <dt>

<span data-ttu-id="8f5c1-110">*NumSamples valore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8f5c1-110">*NumSamples* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f5c1-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8f5c1-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8f5c1-112">Numero di percorsi di esempio.</span><span class="sxs-lookup"><span data-stu-id="8f5c1-112">Number of sample locations.</span></span>

</dd> <dt>

<span data-ttu-id="8f5c1-113">*pSampleLocs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8f5c1-113">*pSampleLocs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f5c1-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="8f5c1-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="8f5c1-115">Posizione per ogni esempio.</span><span class="sxs-lookup"><span data-stu-id="8f5c1-115">Position for each sample.</span></span>

</dd> <dt>

<span data-ttu-id="8f5c1-116">*pSampleNorms* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8f5c1-116">*pSampleNorms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f5c1-117">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="8f5c1-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="8f5c1-118">Vettore normale per ogni posizione di esempio.</span><span class="sxs-lookup"><span data-stu-id="8f5c1-118">Normal vector for each sample location.</span></span>

</dd> <dt>

<span data-ttu-id="8f5c1-119">*pDataOut* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="8f5c1-119">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f5c1-120">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="8f5c1-120">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="8f5c1-121">Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di output che modella il contributo di illuminazione diretta al punto, usando l'approssimazione sh.</span><span class="sxs-lookup"><span data-stu-id="8f5c1-121">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models the direct lighting contribution to the point, using the SH approximation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f5c1-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8f5c1-122">Return value</span></span>

<span data-ttu-id="8f5c1-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8f5c1-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8f5c1-124">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8f5c1-124">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8f5c1-125">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="8f5c1-125">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f5c1-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="8f5c1-126">Remarks</span></span>

<span data-ttu-id="8f5c1-127">Non usare un buffer di trama quando si chiama questo metodo.</span><span class="sxs-lookup"><span data-stu-id="8f5c1-127">Do not use a texture buffer when calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f5c1-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8f5c1-128">Requirements</span></span>



| <span data-ttu-id="8f5c1-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f5c1-129">Requirement</span></span> | <span data-ttu-id="8f5c1-130">Valore</span><span class="sxs-lookup"><span data-stu-id="8f5c1-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f5c1-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8f5c1-131">Header</span></span><br/>  | <dl> <span data-ttu-id="8f5c1-132"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f5c1-132"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8f5c1-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="8f5c1-133">Library</span></span><br/> | <dl> <span data-ttu-id="8f5c1-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f5c1-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8f5c1-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8f5c1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f5c1-136">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="8f5c1-136">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="8f5c1-137">**ID3DXPRTEngine::ComputeDirectLightingSH**</span><span class="sxs-lookup"><span data-stu-id="8f5c1-137">**ID3DXPRTEngine::ComputeDirectLightingSH**</span></span>](id3dxprtengine--computedirectlightingsh.md)
</dt> <dt>

[<span data-ttu-id="8f5c1-138">**ID3DXPRTEngine::ComputeSurfSamplesBounce**</span><span class="sxs-lookup"><span data-stu-id="8f5c1-138">**ID3DXPRTEngine::ComputeSurfSamplesBounce**</span></span>](id3dxprtengine--computesurfsamplesbounce.md)
</dt> </dl>

 

 
