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
# <a name="id3d12devicedownlevelqueryvideomemoryinfo-method"></a>Metodo ID3D12DeviceDownlevel:: QueryVideoMemoryInfo

Fornisce le statistiche sulla memoria in Windows 7. Questo metodo è equivalente a [IDXGIAdapter3:: QueryVideoMemoryInfo](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo), che non è disponibile in Windows 7.

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

Tipo: **uint**

Specifica la scheda fisica del dispositivo per la quale vengono eseguite query sulle informazioni sulla memoria del video. Per l'operazione a singola GPU, impostare su zero. Se sono presenti più nodi GPU, impostarlo sull'indice del nodo (scheda fisica del dispositivo) per cui vengono eseguite query sulle informazioni sulla memoria video. Vedere [sistemi](multi-engine.md)con più schede.

`MemorySegmentGroup`

Tipo: **[DXGI_MEMORY_SEGMENT_GROUP](/windows/win32/api/dxgi1_4/ne-dxgi1_4-dxgi_memory_segment_group)**

Specifica un **DXGI_MEMORY_SEGMENT_GROUP** che identifica il gruppo come locale o non locale.

`pVideoMemoryInfo`

Tipo: **[DXGI_QUERY_VIDEO_MEMORY_INFO](/windows/win32/api/dxgi1_4/ns-dxgi1_4-dxgi_query_video_memory_info)\***

Compila una struttura di **DXGI_QUERY_VIDEO_MEMORY_INFO** con i valori correnti.

## <a name="return-value"></a>Valore restituito

Restituisce **S_OK** in caso di esito positivo, altrimenti un HRESULT non riuscito.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|--------|------------------|
| Intestazione | d3d12downlevel. h e dxgi1_4. h |
| DLL    | D3D12.dll (solo Windows 7) |

## <a name="see-also"></a>Vedi anche
* [ID3D12DeviceDownlevel](id3d12devicedownlevel.md)
* [Interfacce Direct3D 12 su Windows 7](direct3d-12on7-interfaces.md)
* [Guida di riferimento a Direct3D 12 per Windows 7 (d3d12downlevel. h)](direct3d-12on7-reference.md)
* [Direct3D 12 in Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
