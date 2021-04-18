---
title: GUID di attributi di adapter DXCore
description: "I GUID dell'attributo adapter seguenti sono dichiarati in `dxcore_interface.h` e vengono utilizzati con i metodi [IDXCoreAdapterFactory:: CreateAdapterList](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md) e [IDXCoreAdapter:: IsAttributeSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md) ."
keywords:
- DXCore, attributo adapter, GUID
topic_type:
- apiref
api_name:
- DXCore adapter attribute GUIDs
api_location:
- dxcore_interface.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: a532552f144dfc21aa5d6a368aecd915d30b40c8
ms.sourcegitcommit: 8737f32d64e5f01c1d38aab92736e4088d6c446e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "106334305"
---
# <a name="dxcore-adapter-attribute-guids"></a>GUID di attributi di adapter DXCore

I GUID dell'attributo adapter seguenti sono dichiarati in `dxcore_interface.h` e vengono utilizzati con i metodi [IDXCoreAdapterFactory:: CreateAdapterList](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md) e [IDXCoreAdapter:: IsAttributeSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md) . Per qualsiasi adapter specificato, è possibile applicare uno o più attributi.

| GUID | Valore |
|-|-|
| `DXCORE_ADAPTER_ATTRIBUTE_D3D11_GRAPHICS`. Specifica un adapter che supporta l'uso con le API grafiche [Direct3D 11](/windows/win32/direct3d11) . Non sono state apportate garanzie sulle funzionalità specifiche, né una garanzia che il sistema operativo nella configurazione corrente supporti queste API. | 0x8c47866b, 0x7583, 0x450d, 0xF0, 0xF0, 0x6B, 0xAD, 0xA8, 0x95, 0XAF, 0x4b |
| `DXCORE_ADAPTER_ATTRIBUTE_D3D12_GRAPHICS`. Specifica un adapter che supporta l'uso con le API grafiche [Direct3D 12](/windows/win32/direct3d12) . Non sono state apportate garanzie sulle funzionalità specifiche, né una garanzia che il sistema operativo nella configurazione corrente supporti queste API. | 0x0c9ece4d, 0x2f6e, 0x4f01, 0x8c, 0x96, 0xE8, 0x9E, 0x33, 0x1B, 0x47, 0xB1 |
| `DXCORE_ADAPTER_ATTRIBUTE_D3D12_CORE_COMPUTE`. Specifica un adapter che supporta l'uso con le API di calcolo di [base di Direct3D 12](../direct3d12/core-feature-levels.md) . Non sono state apportate garanzie sulle funzionalità specifiche, né una garanzia che il sistema operativo nella configurazione corrente supporti queste API. | 0x248e2800, 0xa793, 0x4724, 0xab, 0xAA, 0x23, 0xA6, 0xDE, 0x1B, 0xE0, 0x90 |

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Intestazione | dxcore_interface. h |

## <a name="see-also"></a>Vedi anche

* [IDXCoreAdapterFactory::CreateAdapterList](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md)
* [IDXCoreAdapter::IsAttributeSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md)
* [Riferimento a DXCore](./dxcore-reference.md)
* [Uso di DXCore per enumerare gli adapter](./dxcore-enum-adapters.md)
* [Grafica Direct3D 12](../direct3d12/direct3d-12-graphics.md)
