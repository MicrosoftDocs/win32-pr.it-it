---
description: Calcola la luminosità di origine risultante da un singolo rimbalzo della luce con riflesso, usando il campionamento adattivo.
ms.assetid: 61f8cecd-d95a-4f02-929e-02f2bce5bde9
title: 'Metodo ID3DXPRTEngine:: ComputeBounceAdaptive (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeBounceAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 787dee9719e0450dd39ebb19f4c06ee76013cb07
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323454"
---
# <a name="id3dxprtenginecomputebounceadaptive-method"></a><span data-ttu-id="8cd73-103">Metodo ID3DXPRTEngine:: ComputeBounceAdaptive</span><span class="sxs-lookup"><span data-stu-id="8cd73-103">ID3DXPRTEngine::ComputeBounceAdaptive method</span></span>

<span data-ttu-id="8cd73-104">Calcola la luminosità di origine risultante da un singolo rimbalzo della luce con riflesso, usando il campionamento adattivo.</span><span class="sxs-lookup"><span data-stu-id="8cd73-104">Computes the source radiance resulting from a single bounce of interreflected light, using adaptive sampling.</span></span> <span data-ttu-id="8cd73-105">Questo metodo genera nuovi vertici e visi sulla mesh per approssimare in modo più accurato il segnale PRT (pre-Computed Radiance Transfer).</span><span class="sxs-lookup"><span data-stu-id="8cd73-105">This method generates new vertices and faces on the mesh to more accurately approximate the precomputed radiance transfer (PRT) signal.</span></span> <span data-ttu-id="8cd73-106">Questo metodo può essere usato per qualsiasi scena illuminata, incluso un modello di PRT a sferica (SH).</span><span class="sxs-lookup"><span data-stu-id="8cd73-106">This method can be used for any lit scene, including a spherical harmonic (SH)-based PRT model.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cd73-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8cd73-107">Syntax</span></span>


```C++
HRESULT ComputeBounceAdaptive(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a><span data-ttu-id="8cd73-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8cd73-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cd73-109">*pDataIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8cd73-109">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cd73-110">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="8cd73-110">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="8cd73-111">Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di input che rappresenta l'oggetto 3D del rimbalzo della luce precedente.</span><span class="sxs-lookup"><span data-stu-id="8cd73-111">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the 3D object from the previous light bounce.</span></span> <span data-ttu-id="8cd73-112">Questo buffer di input deve avere il numero appropriato di canali di colore allocati per la simulazione.</span><span class="sxs-lookup"><span data-stu-id="8cd73-112">This input buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="8cd73-113">*AdaptiveThresh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8cd73-113">*AdaptiveThresh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cd73-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8cd73-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8cd73-115">Soglia sul vettore PRT da usare per la suddivisione dei vertici e delle facce mesh.</span><span class="sxs-lookup"><span data-stu-id="8cd73-115">Threshold on the PRT vector to use for subdividing mesh vertices and faces.</span></span> <span data-ttu-id="8cd73-116">Se è minore di 1e-6F, viene specificato un valore predefinito di 1e-6F.</span><span class="sxs-lookup"><span data-stu-id="8cd73-116">If less than 1e-6f, a default value of 1e-6f is specified.</span></span>

</dd> <dt>

<span data-ttu-id="8cd73-117">*MinEdgeLength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8cd73-117">*MinEdgeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cd73-118">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8cd73-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8cd73-119">Lunghezza minima del bordo della superficie che verrà generata nel campionamento adattivo.</span><span class="sxs-lookup"><span data-stu-id="8cd73-119">Minimum face edge length that will be generated in adaptive sampling.</span></span> <span data-ttu-id="8cd73-120">Se il metodo determina che il valore è troppo piccolo, viene specificato un valore dipendente dal modello.</span><span class="sxs-lookup"><span data-stu-id="8cd73-120">If the method determines that the value is too small, a model-dependent value is specified.</span></span> <span data-ttu-id="8cd73-121">Se è zero, viene specificato un valore predefinito pari a 4.</span><span class="sxs-lookup"><span data-stu-id="8cd73-121">If zero, a default value of 4 is specified.</span></span>

</dd> <dt>

<span data-ttu-id="8cd73-122">*MaxSubdiv* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8cd73-122">*MaxSubdiv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cd73-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8cd73-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8cd73-124">Livello massimo di suddivisione di una faccia che verrà utilizzata nel campionamento adattivo.</span><span class="sxs-lookup"><span data-stu-id="8cd73-124">Maximum level of subdivision of a face that will be used in adaptive sampling.</span></span>

</dd> <dt>

<span data-ttu-id="8cd73-125">*pDataOut* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="8cd73-125">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cd73-126">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="8cd73-126">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="8cd73-127">Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di output.</span><span class="sxs-lookup"><span data-stu-id="8cd73-127">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span> <span data-ttu-id="8cd73-128">Questo buffer di output deve avere il numero appropriato di canali di colore allocati per la simulazione.</span><span class="sxs-lookup"><span data-stu-id="8cd73-128">This output buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="8cd73-129">*pDataTotal* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="8cd73-129">*pDataTotal* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cd73-130">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="8cd73-130">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="8cd73-131">Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) facoltativo che mantiene una somma in esecuzione di pDataOut con ogni calcolo di rimbalzo chiaro.</span><span class="sxs-lookup"><span data-stu-id="8cd73-131">Pointer to an optional [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that keeps a running sum of pDataOut with each light bounce computation.</span></span> <span data-ttu-id="8cd73-132">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="8cd73-132">May be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cd73-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8cd73-133">Return value</span></span>

<span data-ttu-id="8cd73-134">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8cd73-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8cd73-135">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8cd73-135">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8cd73-136">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="8cd73-136">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cd73-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8cd73-137">Requirements</span></span>



| <span data-ttu-id="8cd73-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cd73-138">Requirement</span></span> | <span data-ttu-id="8cd73-139">Valore</span><span class="sxs-lookup"><span data-stu-id="8cd73-139">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8cd73-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8cd73-140">Header</span></span><br/>  | <dl> <span data-ttu-id="8cd73-141"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cd73-141"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8cd73-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="8cd73-142">Library</span></span><br/> | <dl> <span data-ttu-id="8cd73-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8cd73-143"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8cd73-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8cd73-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cd73-145">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="8cd73-145">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="8cd73-146">**ID3DXPRTEngine::RobustMeshRefine**</span><span class="sxs-lookup"><span data-stu-id="8cd73-146">**ID3DXPRTEngine::RobustMeshRefine**</span></span>](id3dxprtengine--robustmeshrefine.md)
</dt> </dl>

 

 
