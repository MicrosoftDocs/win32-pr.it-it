---
title: CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT classe (D3dx12.h)
description: Classe helper per la creazione di un oggetto secondario per esportare un oggetto secondario dello stato di associazione.
keywords:
- CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT classe
topic_type:
- apiref
api_name:
- CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/04/2021
ms.openlocfilehash: 23a0bfe1afff461e5d6b8ba69bedd6ade9069904
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812473"
---
# <a name="cd3dx12_subobject_to_exports_association_subobject-class"></a>CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT classe

Classe helper per la creazione di un oggetto secondario per esportare un oggetto secondario dello stato di associazione.

Per altre informazioni sugli helper per la creazione di oggetti di stato D3DX12, [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md).

## <a name="syntax"></a>Sintassi

```cpp
class CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT
{
    CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT() noexcept;
    CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC& ContainingStateObject);
    void SetSubobjectToAssociate(const D3D12_STATE_SUBOBJECT& SubobjectToAssociate) noexcept;
    void AddExport(LPCWSTR Export);
    template<size_t N> void AddExports(LPCWSTR(&Exports)[N]);
    void AddExports(const LPCWSTR* Exports, UINT N);
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept;
    operator const D3D12_SUBOBJECT_TO_EXPORTS_ASSOCIATION& () const noexcept;
};
```

## <a name="members"></a>Members

`CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT`

Costruttore predefinito. Crea una nuova istanza inizializzata per impostazione predefinita di un **CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT**.

`CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Costruttore che crea una nuova istanza di un **CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT** inizializzato con il contenuto di un [**oggetto CD3DX12_STATE_OBJECT_DESC.**](cd3dx12-state-object-desc.md)

`SetSubobjectToAssociate(const D3D12_STATE_SUBOBJECT&)`

Funzione per l'impostazione del sottooggetto da associare sotto [forma di D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) passato come parametro.

`AddExport(LPCWSTR)`

Aggiunge un'esportazione da associare.

`AddExports(LPCWSTR(&)[N]);`

Aggiunge una matrice di esportazioni da associare. Il parametro di modello *N* specifica il numero di elementi nella matrice.

`AddExports(const LPCWSTR*, UINT)`

Definisce una matrice di N *esportazioni* da associare.

`Type`

Recupera il tipo del sottooggetto, rappresentato dalla [D3D12_STATE_SUBOBJECT_TYPE_SUBOBJECT_TO_EXPORTS_ASSOCIATION](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) costante.

`operator const D3D12_STATE_SUBOBJECT&`

Operatore di conversione che restituisce un riferimento a una costante [D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) oggetto che descrive l'oggetto stato.

`operator const D3D12_SUBOBJECT_TO_EXPORTS_ASSOCIATION&`

Operatore di conversione che restituisce un riferimento a una costante [D3D12_SUBOBJECT_TO_EXPORTS_ASSOCIATION](/windows/win32/api/d3d12/ns-d3d12-d3d12_subobject_to_exports_association) oggetto che descrive l'oggetto stato.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Vedi anche

* [Strutture helper per Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
