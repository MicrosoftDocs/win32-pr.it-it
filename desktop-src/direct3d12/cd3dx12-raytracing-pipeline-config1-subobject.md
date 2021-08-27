---
title: CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT classe (D3dx12.h)
description: Classe helper per la creazione di un oggetto secondario dello stato di configurazione della pipeline di raytracing, con flag.
keywords:
- CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT classe
topic_type:
- apiref
api_name:
- CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/05/2021
ms.openlocfilehash: fc2049f6a800891e165f57099ad7f9b0bbaba263
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812184"
---
# <a name="cd3dx12_raytracing_pipeline_config1_subobject-class"></a>CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT classe

Classe helper per la creazione di un oggetto secondario dello stato di configurazione della pipeline di raytracing, con flag.

Per altre informazioni sugli helper per la creazione di oggetti di stato D3DX12, [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md).

## <a name="syntax"></a>Sintassi

```cpp
class CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT
{
public:
    CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT() noexcept;
    CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC& ContainingStateObject);
    void Config(UINT MaxTraceRecursionDepth, D3D12_RAYTRACING_PIPELINE_FLAGS Flags) noexcept;
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept;
    operator const D3D12_RAYTRACING_PIPELINE_CONFIG1& () const noexcept;
};
```

## <a name="members"></a>Members

`CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT`

Costruttore predefinito. Crea una nuova istanza inizializzata per impostazione predefinita di un **CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT**.

`CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Costruttore che crea una nuova istanza di un **CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT** inizializzato con il contenuto di un [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) oggetto .

`Config(UINT, D3D12_RAYTRACING_PIPELINE_FLAGS)`

Funzione per la configurazione del limite di ricorsione di raggi per la pipeline di raytracing. Accetta anche un [D3D12_RAYTRACING_PIPELINE_FLAGS](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_flags) parametro .

`Type`

Recupera il tipo del sottooggetto, rappresentato dalla [D3D12_STATE_SUBOBJECT_TYPE_RAYTRACING_PIPELINE_CONFIG](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) costante.

`operator const D3D12_STATE_SUBOBJECT&`

Operatore di conversione che restituisce un riferimento a una costante [D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) oggetto che descrive l'oggetto stato.

`operator const D3D12_RAYTRACING_PIPELINE_CONFIG&`

Operatore di conversione che restituisce un riferimento a una costante [D3D12_RAYTRACING_PIPELINE_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config) oggetto che descrive l'oggetto stato.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Vedi anche

* [Strutture helper per Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
