---
description: Moltiplica ogni vettore PRT (pre-Computed Radiance Transfer) per l'albedo per vertice.
ms.assetid: 2b3e4b19-7778-4240-ac79-3237fda2ed96
title: 'Metodo ID3DXPRTEngine:: MultiplyAlbedo (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.MultiplyAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a282605789644382f39fd8fff9ce8bb47d6dfc7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323439"
---
# <a name="id3dxprtenginemultiplyalbedo-method"></a><span data-ttu-id="323a6-103">Metodo ID3DXPRTEngine:: MultiplyAlbedo</span><span class="sxs-lookup"><span data-stu-id="323a6-103">ID3DXPRTEngine::MultiplyAlbedo method</span></span>

<span data-ttu-id="323a6-104">Moltiplica ogni vettore PRT (pre-Computed Radiance Transfer) per l'albedo per vertice.</span><span class="sxs-lookup"><span data-stu-id="323a6-104">Multiplies each precomputed radiance transfer (PRT) vector by the per-vertex albedo.</span></span>

## <a name="syntax"></a><span data-ttu-id="323a6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="323a6-105">Syntax</span></span>


```C++
HRESULT MultiplyAlbedo(
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="323a6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="323a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="323a6-107">*pDataOut* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="323a6-107">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="323a6-108">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="323a6-108">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="323a6-109">Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di output che conterrà vettori PRT moltiplicato per l'albedo per vertice.</span><span class="sxs-lookup"><span data-stu-id="323a6-109">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that will contain PRT vectors multiplied by the per-vertex albedo.</span></span> <span data-ttu-id="323a6-110">Se il buffer di output è un oggetto trama, è necessario prestare attenzione per archiviare l'albedo della trama con la stessa risoluzione del buffer di simulazione.</span><span class="sxs-lookup"><span data-stu-id="323a6-110">If this output buffer is a texture object, then care must be taken to store the albedo of the texture at the same resolution as the simulation buffer.</span></span> <span data-ttu-id="323a6-111">È possibile impostare la risoluzione corretta nell'albedo con [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md), applicando le aree di rilegatura delle trame, se necessario.</span><span class="sxs-lookup"><span data-stu-id="323a6-111">You can set the proper resolution on the albedo with [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md), applying texture gutter regions if appropriate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="323a6-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="323a6-112">Return value</span></span>

<span data-ttu-id="323a6-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="323a6-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="323a6-114">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="323a6-114">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="323a6-115">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="323a6-115">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="323a6-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="323a6-116">Remarks</span></span>

<span data-ttu-id="323a6-117">I metodi ID3DXPRTEngine:: Computexxx calcolano i buffer di output in cui il segnale chiaro non è stato moltiplicato per albedo.</span><span class="sxs-lookup"><span data-stu-id="323a6-117">The ID3DXPRTEngine::Computexxx methods compute output buffers in which the light signal has not been multiplied by albedo.</span></span> <span data-ttu-id="323a6-118">Se non si moltiplica l'albedo, è possibile modellare la variazione dell'albedo a una scala più sottile rispetto alla luminosità di origine, ottenendo così risultati più accurati dalla compressione.</span><span class="sxs-lookup"><span data-stu-id="323a6-118">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="323a6-119">Per includere albedo nel modello Light con rendering, chiamare questo metodo dopo uno dei metodi Computexxx.</span><span class="sxs-lookup"><span data-stu-id="323a6-119">To include albedo in the rendered-light model, call this method after one of the Computexxx methods.</span></span>

<span data-ttu-id="323a6-120">[**ID3DXPRTEngine:: SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md) deve essere chiamato prima di chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="323a6-120">[**ID3DXPRTEngine::SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md) should be called before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="323a6-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="323a6-121">Requirements</span></span>



| <span data-ttu-id="323a6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="323a6-122">Requirement</span></span> | <span data-ttu-id="323a6-123">Valore</span><span class="sxs-lookup"><span data-stu-id="323a6-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="323a6-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="323a6-124">Header</span></span><br/>  | <dl> <span data-ttu-id="323a6-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="323a6-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="323a6-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="323a6-126">Library</span></span><br/> | <dl> <span data-ttu-id="323a6-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="323a6-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="323a6-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="323a6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="323a6-129">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="323a6-129">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="323a6-130">**ID3DXPRTEngine::ComputeDirectLightingSH**</span><span class="sxs-lookup"><span data-stu-id="323a6-130">**ID3DXPRTEngine::ComputeDirectLightingSH**</span></span>](id3dxprtengine--computedirectlightingsh.md)
</dt> </dl>

 

 




