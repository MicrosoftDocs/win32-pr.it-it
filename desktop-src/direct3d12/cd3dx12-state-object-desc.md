---
title: CD3DX12_STATE_OBJECT_DESC classe (D3dx12.h)
description: Classe centrale degli helper di creazione di oggetti di stato D3DX12, che sono classi helper per la creazione di oggetti di stato da un set arbitrario di oggetti secondari.
keywords:
- CD3DX12_STATE_OBJECT_DESC classe
topic_type:
- apiref
api_name:
- CD3DX12_STATE_OBJECT_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/03/2021
ms.openlocfilehash: cc3d65a9779c379debd94e7872717e4449a71ac8
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813075"
---
# <a name="cd3dx12_state_object_desc-class"></a>CD3DX12_STATE_OBJECT_DESC classe

Classe centrale degli helper di creazione di oggetti di stato D3DX12, che sono classi helper per la creazione di oggetti di stato da un set arbitrario di oggetti secondari.

## <a name="syntax"></a>Sintassi

```cpp
class CD3DX12_STATE_OBJECT_DESC
{
    CD3DX12_STATE_OBJECT_DESC() noexcept;
    CD3DX12_STATE_OBJECT_DESC(D3D12_STATE_OBJECT_TYPE) noexcept;
    void SetStateObjectType(D3D12_STATE_OBJECT_TYPE) noexcept;
    operator const D3D12_STATE_OBJECT_DESC& ();
    operator const D3D12_STATE_OBJECT_DESC* ();
    template<typename T> T* CreateSubobject();
};
```

## <a name="members"></a>Members

`CD3DX12_STATE_OBJECT_DESC`

Costruttore predefinito. Crea una nuova istanza inizializzata per impostazione predefinita di un **CD3DX12_STATE_OBJECT_DESC**.

`CD3DX12_STATE_OBJECT_DESC(D3D12_STATE_OBJECT_TYPE)`

Costruttore che crea una nuova istanza di **un CD3DX12_STATE_OBJECT_DESC** inizializzato con un tipo subjobject corrispondente al valore [**del D3D12_STATE_OBJECT_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_object_type) passato.

`SetStateObjectType(D3D12_STATE_OBJECT_TYPE)`

Metodo che imposta il tipo di oggetto secondario sul valore [**del D3D12_STATE_OBJECT_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_object_type) passato.

`operator const D3D12_STATE_OBJECT_DESC&`

Operatore di conversione che restituisce un riferimento a una costante [**D3D12_STATE_OBJECT_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_desc) oggetto che descrive l'oggetto stato.

`operator const D3D12_STATE_OBJECT_DESC*`

Operatore di conversione che restituisce un puntatore a una [**costante D3D12_STATE_OBJECT_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_desc) oggetto che descrive l'oggetto stato.

`CreateSubobject`

Modello di funzione che crea un helper sububject la cui durata è di proprietà di questa classe.

Il parametro *di modello T* specifica il tipo di helper subjobject, ad esempio CD3DX12_HIT_GROUP_SUBOBJECT . [](cd3dx12-hit-group-subobject.md)

## <a name="remarks"></a>Commenti

Per usare gli helper di creazione di oggetti di stato D3DX12, iniziare creando un'istanza di un oggetto **CD3DX12_STATE_OBJECT_DESC** e chiamare la relativa funzione **CreateSubobject** per creare oggetti secondari. Ogni helper oggetto secondario dispone di metodi specifici di tale oggetto secondario per la configurazione del relativo contenuto.

```cpp
CD3DX12_STATE_OBJECT_DESC Collection1(D3D12_STATE_OBJECT_TYPE_COLLECTION);
auto Lib0 = Collection1.CreateSubobject<CD3DX12_DXIL_LIBRARY_SUBOBJECT>();
Lib0->SetDXILLibrary(&pMyAppDxilLibs[0]);
Lib0->DefineExport(L"rayGenShader0");
// In practice, these export listings might be data/engine-driven.
...
```

In alternativa, è possibile creare un'istanza degli helper subobject in modo esplicito, ad esempio tramite variabili locali, passando l'oggetto di stato desc (che deve puntare a esso) nel costruttore helper (o chiamare `mySubobjectHelper.AddToStateObject(Collection1)` ).

In questo scenario alternativo è necessario mantenere attivo il sottooggetto finché l'oggetto di stato a cui è associato è attivo, in caso contrario i relativi riferimenti al puntatore saranno obsoleti.

```cpp
CD3DX12_STATE_OBJECT_DESC RaytracingState2(D3D12_STATE_OBJECT_TYPE_RAYTRACING_PIPELINE);
CD3DX12_DXIL_LIBRARY_SUBOBJECT LibA(RaytracingState2);
LibA.SetDXILLibrary(&pMyAppDxilLibs[4]);
// Not manually specifying exports; meaning that all exports in the libraries are exported.
...
```

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Vedi anche

* [Strutture helper per Direct3D 12](helper-structures-for-d3d12.md)
