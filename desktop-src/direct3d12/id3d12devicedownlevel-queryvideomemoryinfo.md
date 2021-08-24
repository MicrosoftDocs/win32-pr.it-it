---
title: Metodo ID3D12DeviceDownlevel::QueryVideoMemoryInfo
description: Copia il contenuto da una risorsa Texture2D Direct3D 12 in una finestra. | Metodo ID3D12DeviceDownlevel::QueryVideoMemoryInfo
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
ms.openlocfilehash: 526d25e8331fc949eb470c0813a083774afddc94312ed6751aaab9672e557d3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124109"
---
# <a name="id3d12devicedownlevelqueryvideomemoryinfo-method"></a>Metodo ID3D12DeviceDownlevel::QueryVideoMemoryInfo

Fornisce statistiche di memoria Windows 7. Questo metodo equivale a [IDXGIAdapter3::QueryVideoMemoryInfo,](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo)che non è disponibile in Windows 7.

## <a name="syntax"></a>Sintassi

```cpp
HRESULT QueryVideoMemoryInfo( 
    UINT NodeIndex,
    DXGI_MEMORY_SEGMENT_GROUP MemorySegmentGroup,
    DXGI_QUERY_VIDEO_MEMORY_INFO *pVideoMemoryInfo
);
```

## <a name="parameters"></a>Parametri

`NodeIndex`

Tipo: **UINT**

Specifica la scheda fisica del dispositivo per cui vengono query le informazioni sulla memoria video. Per un'operazione a GPU singola, impostare questa proprietà su zero. Se sono presenti più nodi GPU, impostare questo valore sull'indice del nodo (scheda fisica del dispositivo) per cui vengono query le informazioni sulla memoria video. Vedere [Sistemi con più schede.](multi-engine.md)

`MemorySegmentGroup`

Tipo: **[DXGI_MEMORY_SEGMENT_GROUP](/windows/win32/api/dxgi1_4/ne-dxgi1_4-dxgi_memory_segment_group)**

Specifica un **DXGI_MEMORY_SEGMENT_GROUP** che identifica il gruppo come locale o non locale.

`pVideoMemoryInfo`

Tipo: **[DXGI_QUERY_VIDEO_MEMORY_INFO](/windows/win32/api/dxgi1_4/ns-dxgi1_4-dxgi_query_video_memory_info)\***

Compila una struttura **DXGI_QUERY_VIDEO_MEMORY_INFO** con i valori correnti.

## <a name="return-value"></a>Valore restituito

Restituisce **S_OK** in caso di esito positivo oppure un HRESULT non riuscito.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|--------|------------------|
| Intestazione | d3d12downlevel.h e dxgi1_4.h |
| DLL    | D3D12.dll (solo Windows 7) |

## <a name="see-also"></a>Vedi anche
* [ID3D12DeviceDownlevel](id3d12devicedownlevel.md)
* [Direct3D 12 Windows 7 interfacce](direct3d-12on7-interfaces.md)
* [Riferimento direct3D 12 Windows 7 (d3d12downlevel.h)](direct3d-12on7-reference.md)
* [Direct3D 12 in Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
