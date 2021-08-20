---
title: CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT classe (D3dx12.h)
description: Classe helper per la creazione di un sottooggetto dello stato di configurazione dello shader raytracing.
keywords:
- CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT classe
topic_type:
- apiref
api_name:
- CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/04/2021
ms.openlocfilehash: 69f30a3cae1eeab030c8929ccd606fb892f27dd5
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812912"
---
# <a name="cd3dx12_raytracing_shader_config_subobject-class"></a>CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT classe

Classe helper per la creazione di un sottooggetto dello stato di configurazione dello shader raytracing.

Per altre informazioni sugli helper per la creazione di oggetti di stato D3DX12, [vedere](cd3dx12-state-object-desc.md)CD3DX12_STATE_OBJECT_DESC .

## <a name="syntax"></a>Sintassi

```cpp
class CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT
{
    CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT() noexcept;
    CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC& ContainingStateObject);
    void Config(UINT MaxPayloadSizeInBytes, UINT MaxAttributeSizeInBytes) noexcept;
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept;
    operator const D3D12_RAYTRACING_SHADER_CONFIG& () const noexcept;
};
```

## <a name="members"></a>Members

`CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT`

Costruttore predefinito. Crea una nuova istanza inizializzata predefinita di un CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT **.**

`CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Costruttore che crea una nuova istanza di un **CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT** inizializzato con il contenuto di un [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) oggetto .

`Config(UINT, UINT)`

Funzione per la configurazione delle dimensioni massime del payload e delle dimensioni massime dell'attributo (entrambe in byte).

`Type`

Recupera il tipo del sottooggetto, rappresentato dalla [D3D12_STATE_SUBOBJECT_TYPE_RAYTRACING_SHADER_CONFIG](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) costante.

`operator const D3D12_STATE_SUBOBJECT&`

Operatore di conversione che restituisce un riferimento a una costante [D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) oggetto che descrive l'oggetto stato.

`operator const D3D12_RAYTRACING_SHADER_CONFIG&`

Operatore di conversione che restituisce un riferimento a una costante [D3D12_RAYTRACING_SHADER_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config) oggetto che descrive l'oggetto stato.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Vedi anche

* [Strutture helper per Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
