---
title: Interfaccia ID3D12DeviceDownlevel
description: Fornisce una query delle statistiche di memoria specifica di Windows 7.
keywords:
- Interfaccia ID3D12DeviceDownlevel
topic_type:
- apiref
api_name:
- ID3D12DeviceDownlevel
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 401cbd0045211ef51e3ef6b06042262964ae2ec5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322162"
---
# <a name="id3d12devicedownlevel-interface"></a>Interfaccia ID3D12DeviceDownlevel

È possibile accedere a questa interfaccia tramite **QueryInterface** da un [dispositivo Direct3D 12](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) quando si usa [Direct3D 12 in Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/). Fornisce una query delle statistiche di memoria specifiche di Windows 7.

### <a name="methods"></a>Metodi

L'interfaccia **ID3D12DeviceDownlevel** dispone di questi metodi.

| Metodo | Descrizione |
|:-------|:------------|
| [**QueryVideoMemoryInfo**](id3d12devicedownlevel-queryvideomemoryinfo.md) | Fornisce le statistiche sulla memoria in Windows 7. |

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|--------|------------------|
| Intestazione | d3d12downlevel. h |
| DLL    | D3D12.dll (solo Windows 7) |

## <a name="see-also"></a>Vedi anche
* [Interfacce Direct3D 12 su Windows 7](direct3d-12on7-interfaces.md)
* [Guida di riferimento a Direct3D 12 per Windows 7 (d3d12downlevel. h)](direct3d-12on7-reference.md)
* [Direct3D 12 in Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
