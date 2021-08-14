---
title: GUID di attributi di adapter DXCore
description: I GUID degli attributi dell'adapter seguenti vengono dichiarati in e usati con i `dxcore_interface.h` [metodi IDXCoreAdapterFactory::CreateAdapterList](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md) e [IDXCoreAdapter::IsAttributeSupported.](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md)
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
ms.openlocfilehash: 44b6be239286e13cecbf6eb501b333cba5541f6de1dfd8e217166d9620bdfbd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279661"
---
# <a name="dxcore-adapter-attribute-guids"></a>GUID di attributi di adapter DXCore

I GUID degli attributi dell'adapter seguenti vengono dichiarati in e usati con i `dxcore_interface.h` [metodi IDXCoreAdapterFactory::CreateAdapterList](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md) e [IDXCoreAdapter::IsAttributeSupported.](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md) Per qualsiasi adattatore specificato, è possibile applicare uno o più attributi.

| GUID | Valore |
|-|-|
| `DXCORE_ADAPTER_ATTRIBUTE_D3D11_GRAPHICS`. Specifica un adattatore che supporta l'uso con le API [grafiche Direct3D 11.](/windows/win32/direct3d11) Non vengono garantite funzionalità specifiche, né è garantito che il sistema operativo nella configurazione corrente supporti queste API. | 0x8c47866b, 0x7583, 0x450d, 0xf0, 0xf0, 0x6b, 0xad, 0xa8, 0x95, 0xaf, 0x4b |
| `DXCORE_ADAPTER_ATTRIBUTE_D3D12_GRAPHICS`. Specifica un adattatore che supporta l'uso con le API [grafiche Direct3D 12.](/windows/win32/direct3d12) Non vengono garantite funzionalità specifiche, né è garantito che il sistema operativo nella configurazione corrente supporti queste API. | 0x0c9ece4d, 0x2f6e, 0x4f01, 0x8c, 0x96, 0xe8, 0x9e, 0x33, 0x1b, 0x47, 0xb1 |
| `DXCORE_ADAPTER_ATTRIBUTE_D3D12_CORE_COMPUTE`. Specifica un adattatore che supporta l'uso con le API di [calcolo Direct3D 12 Core.](../direct3d12/core-feature-levels.md) Non vengono garantite funzionalità specifiche, né è garantito che il sistema operativo nella configurazione corrente supporti queste API. | 0x248e2800, 0xa793, 0x4724, 0xab, 0xaa, 0x23, 0xa6, 0xde, 0x1b, 0xe0, 0x90 |

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Intestazione | dxcore_interface.h |

## <a name="see-also"></a>Vedi anche

* [IDXCoreAdapterFactory::CreateAdapterList](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md)
* [IDXCoreAdapter::IsAttributeSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md)
* [Informazioni di riferimento su DXCore](./dxcore-reference.md)
* [Uso di DXCore per enumerare gli adapter](./dxcore-enum-adapters.md)
* [Grafica Direct3D 12](../direct3d12/direct3d-12-graphics.md)
