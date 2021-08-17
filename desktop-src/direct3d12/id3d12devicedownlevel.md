---
title: Interfaccia ID3D12DeviceDownlevel
description: Fornisce una Windows di statistiche di memoria specifica di 7.
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
ms.openlocfilehash: 8cd9b39e865377734fca3d0791b89219d611f57f456a85a8f9b12e345aba9e99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124079"
---
# <a name="id3d12devicedownlevel-interface"></a>Interfaccia ID3D12DeviceDownlevel

È possibile accedere a questa interfaccia tramite **QueryInterface** da un [dispositivo Direct3D 12](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) quando si usa [Direct3D 12 Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/). Fornisce una query Windows statistiche di memoria specifiche di 7.

### <a name="methods"></a>Metodi

**L'interfaccia ID3D12DeviceDownlevel** include questi metodi.

| Metodo | Descrizione |
|:-------|:------------|
| [**QueryVideoMemoryInfo**](id3d12devicedownlevel-queryvideomemoryinfo.md) | Fornisce statistiche sulla memoria per Windows 7. |

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|--------|------------------|
| Intestazione | d3d12downlevel.h |
| DLL    | D3D12.dll (solo Windows 7) |

## <a name="see-also"></a>Vedi anche
* [Interfacce Direct3D 12 Windows 7](direct3d-12on7-interfaces.md)
* [Informazioni di riferimento su Direct3D 12 Windows 7 (d3d12downlevel.h)](direct3d-12on7-reference.md)
* [Direct3D 12 in Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
