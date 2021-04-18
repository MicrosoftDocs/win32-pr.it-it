---
title: 'Metodo ID3D12DeviceDownlevel:: QueryVideoMemoryInfo'
description: 'Copia il contenuto da una risorsa Direct3D 12 Texture2D in una finestra. | Metodo ID3D12DeviceDownlevel:: QueryVideoMemoryInfo'
keywords:
- Metodo QueryVideoMemoryInfo
- Metodo QueryVideoMemoryInfo, interfaccia ID3D12DeviceDownlevel
- Interfaccia ID3D12DeviceDownlevel, metodo QueryVideoMemoryInfo
topic_type:
- apiref
api_name:
- ID3D12DeviceDownlevel.QueryVideoMemoryInfo
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 32b93fcbbe44aaae0916e6d8f3f403eb960e26eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323123"
---
# <a name="id3d12devicedownlevelqueryvideomemoryinfo-method"></a><span data-ttu-id="ebd69-107">Metodo ID3D12DeviceDownlevel:: QueryVideoMemoryInfo</span><span class="sxs-lookup"><span data-stu-id="ebd69-107">ID3D12DeviceDownlevel::QueryVideoMemoryInfo method</span></span>

<span data-ttu-id="ebd69-108">Fornisce le statistiche sulla memoria in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ebd69-108">Provides memory statistics on Windows 7.</span></span> <span data-ttu-id="ebd69-109">Questo metodo è equivalente a [IDXGIAdapter3:: QueryVideoMemoryInfo](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo), che non è disponibile in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ebd69-109">This method is equivalent to [IDXGIAdapter3::QueryVideoMemoryInfo](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo), which is not available on Windows 7.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebd69-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ebd69-110">Syntax</span></span>

```cpp
HRESULT QueryVideoMemoryInfo( 
    UINT NodeIndex,
    DXGI_MEMORY_SEGMENT_GROUP MemorySegmentGroup,
    DXGI_QUERY_VIDEO_MEMORY_INFO *pVideoMemoryInfo
);
```

## <a name="parameters"></a><span data-ttu-id="ebd69-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="ebd69-111">Parameters</span></span>

`NodeIndex`

<span data-ttu-id="ebd69-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="ebd69-112">Type: **UINT**</span></span>

<span data-ttu-id="ebd69-113">Specifica la scheda fisica del dispositivo per la quale vengono eseguite query sulle informazioni sulla memoria del video.</span><span class="sxs-lookup"><span data-stu-id="ebd69-113">Specifies the device's physical adapter for which the video memory information is queried.</span></span> <span data-ttu-id="ebd69-114">Per l'operazione a singola GPU, impostare su zero.</span><span class="sxs-lookup"><span data-stu-id="ebd69-114">For single-GPU operation, set this to zero.</span></span> <span data-ttu-id="ebd69-115">Se sono presenti più nodi GPU, impostarlo sull'indice del nodo (scheda fisica del dispositivo) per cui vengono eseguite query sulle informazioni sulla memoria video.</span><span class="sxs-lookup"><span data-stu-id="ebd69-115">If there are multiple GPU nodes, set this to the index of the node (the device's physical adapter) for which the video memory information is queried.</span></span> <span data-ttu-id="ebd69-116">Vedere [sistemi](multi-engine.md)con più schede.</span><span class="sxs-lookup"><span data-stu-id="ebd69-116">See [Multi-adapter systems](multi-engine.md).</span></span>

`MemorySegmentGroup`

<span data-ttu-id="ebd69-117">Tipo: **[DXGI_MEMORY_SEGMENT_GROUP](/windows/win32/api/dxgi1_4/ne-dxgi1_4-dxgi_memory_segment_group)**</span><span class="sxs-lookup"><span data-stu-id="ebd69-117">Type: **[DXGI_MEMORY_SEGMENT_GROUP](/windows/win32/api/dxgi1_4/ne-dxgi1_4-dxgi_memory_segment_group)**</span></span>

<span data-ttu-id="ebd69-118">Specifica un **DXGI_MEMORY_SEGMENT_GROUP** che identifica il gruppo come locale o non locale.</span><span class="sxs-lookup"><span data-stu-id="ebd69-118">Specifies a **DXGI_MEMORY_SEGMENT_GROUP** that identifies the group as local or non-local.</span></span>

`pVideoMemoryInfo`

<span data-ttu-id="ebd69-119">Tipo: **[DXGI_QUERY_VIDEO_MEMORY_INFO](/windows/win32/api/dxgi1_4/ns-dxgi1_4-dxgi_query_video_memory_info)\***</span><span class="sxs-lookup"><span data-stu-id="ebd69-119">Type: **[DXGI_QUERY_VIDEO_MEMORY_INFO](/windows/win32/api/dxgi1_4/ns-dxgi1_4-dxgi_query_video_memory_info)\***</span></span>

<span data-ttu-id="ebd69-120">Compila una struttura di **DXGI_QUERY_VIDEO_MEMORY_INFO** con i valori correnti.</span><span class="sxs-lookup"><span data-stu-id="ebd69-120">Fills in a **DXGI_QUERY_VIDEO_MEMORY_INFO** structure with the current values.</span></span>

## <a name="return-value"></a><span data-ttu-id="ebd69-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ebd69-121">Return value</span></span>

<span data-ttu-id="ebd69-122">Restituisce **S_OK** in caso di esito positivo, altrimenti un HRESULT non riuscito.</span><span class="sxs-lookup"><span data-stu-id="ebd69-122">Returns **S_OK** on success, or else a failing HRESULT.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebd69-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ebd69-123">Requirements</span></span>

| <span data-ttu-id="ebd69-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebd69-124">Requirement</span></span> | <span data-ttu-id="ebd69-125">Valore</span><span class="sxs-lookup"><span data-stu-id="ebd69-125">Value</span></span> |
|--------|------------------|
| <span data-ttu-id="ebd69-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ebd69-126">Header</span></span> | <span data-ttu-id="ebd69-127">d3d12downlevel. h e dxgi1_4. h</span><span class="sxs-lookup"><span data-stu-id="ebd69-127">d3d12downlevel.h and dxgi1_4.h</span></span> |
| <span data-ttu-id="ebd69-128">DLL</span><span class="sxs-lookup"><span data-stu-id="ebd69-128">DLL</span></span>    | <span data-ttu-id="ebd69-129">D3D12.dll (solo Windows 7)</span><span class="sxs-lookup"><span data-stu-id="ebd69-129">D3D12.dll (Windows 7 only)</span></span> |

## <a name="see-also"></a><span data-ttu-id="ebd69-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ebd69-130">See also</span></span>
* [<span data-ttu-id="ebd69-131">ID3D12DeviceDownlevel</span><span class="sxs-lookup"><span data-stu-id="ebd69-131">ID3D12DeviceDownlevel</span></span>](id3d12devicedownlevel.md)
* [<span data-ttu-id="ebd69-132">Interfacce Direct3D 12 su Windows 7</span><span class="sxs-lookup"><span data-stu-id="ebd69-132">Direct3D 12 On Windows 7 interfaces</span></span>](direct3d-12on7-interfaces.md)
* [<span data-ttu-id="ebd69-133">Guida di riferimento a Direct3D 12 per Windows 7 (d3d12downlevel. h)</span><span class="sxs-lookup"><span data-stu-id="ebd69-133">Direct3D 12 on Windows 7 reference (d3d12downlevel.h)</span></span>](direct3d-12on7-reference.md)
* [<span data-ttu-id="ebd69-134">Direct3D 12 in Windows 7</span><span class="sxs-lookup"><span data-stu-id="ebd69-134">Direct3D 12 On Windows 7</span></span>](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
