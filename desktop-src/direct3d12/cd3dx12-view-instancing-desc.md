---
title: CD3DX12_VIEW_INSTANCING_DESC struttura (D3dx12.h)
description: Struttura helper per consentire una facile inizializzazione di una [**struttura D3DX12_VIEW_INSTANCING_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_view_instancing_desc) di supporto.
keywords:
- CD3DX12_VIEW_INSTANCING_DESC struttura
topic_type:
- apiref
api_name:
- CD3DX12_VIEW_INSTANCING_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2021
ms.openlocfilehash: 51c9f5caf5bedf9712001420993393a2dcfa6870
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813256"
---
# <a name="cd3dx12_view_instancing_desc-structure"></a>CD3DX12_VIEW_INSTANCING_DESC struttura

Struttura helper per consentire una facile inizializzazione di una [**struttura D3DX12_VIEW_INSTANCING_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) di supporto.

## <a name="syntax"></a>Sintassi

```cpp
struct CD3DX12_VIEW_INSTANCING_DESC : public D3D12_VIEW_INSTANCING_DESC
{
    CD3DX12_VIEW_INSTANCING_DESC();
    explicit CD3DX12_VIEW_INSTANCING_DESC(const D3D12_VIEW_INSTANCING_DESC& o) noexcept;
    explicit CD3DX12_VIEW_INSTANCING_DESC(CD3DX12_DEFAULT) noexcept;
    explicit CD3DX12_VIEW_INSTANCING_DESC(
        UINT InViewInstanceCount,
        const D3D12_VIEW_INSTANCE_LOCATION* InViewInstanceLocations,
        D3D12_VIEW_INSTANCING_FLAGS InFlags) noexcept;
};
```

## <a name="members"></a>Members

`CD3DX12_VIEW_INSTANCING_DESC`

Costruttore predefinito. Crea una nuova istanza non inizializzata di un CD3DX12_VIEW_INSTANCING_DESC **.**

`CD3DX12_VIEW_INSTANCING_DESC(const D3D12_VIEW_INSTANCING_DESC&)`

Costruttore che crea una nuova istanza di un **CD3DX12_VIEW_INSTANCING_DESC** inizializzato con il contenuto di una [**D3DX12_VIEW_INSTANCING_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) struttura .

`CD3DX12_VIEW_INSTANCING_DESC(CD3DX12_DEFAULT)`

Costruttore che crea una nuova istanza di un **CD3DX12_VIEW_INSTANCING_DESC** inizializzato con questi valori.

|Membro dei dati|Valore|
|-|-|
|ViewInstanceCount|0|
|pViewInstanceLocations|nullptr|
|Flags|D3D12_VIEW_INSTANCING_FLAG_NONE|

`CD3DX12_VIEW_INSTANCING_DESC(UINT, const D3D12_VIEW_INSTANCE_LOCATION*, D3D12_VIEW_INSTANCING_FLAGS)`

Costruttore che crea una nuova istanza di un **CD3DX12_VIEW_INSTANCING_DESC** inizializzato con i parametri passati.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Vedi anche

* [D3DX12_VIEW_INSTANCING_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc)
* [Strutture helper per Direct3D 12](helper-structures-for-d3d12.md)
