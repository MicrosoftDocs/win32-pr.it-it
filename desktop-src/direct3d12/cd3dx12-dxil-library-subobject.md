---
title: CD3DX12_DXIL_LIBRARY_SUBOBJECT classe (D3dx12.h)
description: Classe helper per la creazione di un oggetto secondario di stato della libreria DXIL.
keywords:
- CD3DX12_DXIL_LIBRARY_SUBOBJECT classe
topic_type:
- apiref
api_name:
- CD3DX12_DXIL_LIBRARY_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/04/2021
ms.openlocfilehash: 33ec22dd722469ce131bc58d5aca83f0aed4edf0
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812548"
---
# <a name="cd3dx12_dxil_library_subobject-class"></a>CD3DX12_DXIL_LIBRARY_SUBOBJECT classe

Classe helper per la creazione di un oggetto secondario di stato della libreria DXIL.

Per altre informazioni sugli helper per la creazione di oggetti di stato D3DX12, [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md).

## <a name="syntax"></a>Sintassi

```cpp
class CD3DX12_DXIL_LIBRARY_SUBOBJECT
{
    CD3DX12_DXIL_LIBRARY_SUBOBJECT() noexcept;
    CD3DX12_DXIL_LIBRARY_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&);
    void SetDXILLibrary(const D3D12_SHADER_BYTECODE* pCode) noexcept;
    void DefineExport(
        LPCWSTR Name,
        LPCWSTR ExportToRename = nullptr,
        D3D12_EXPORT_FLAGS Flags = D3D12_EXPORT_FLAG_NONE);
    template<size_t N> void DefineExports(LPCWSTR(&Exports)[N]);
    void DefineExports(const LPCWSTR* Exports, UINT N);
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept;
    operator const D3D12_DXIL_LIBRARY_DESC& () const noexcept;
};
```

## <a name="members"></a>Members

`CD3DX12_DXIL_LIBRARY_SUBOBJECT`

Costruttore predefinito. Crea una nuova istanza inizializzata per impostazione predefinita di un **CD3DX12_DXIL_LIBRARY_SUBOBJECT**.

`CD3DX12_DXIL_LIBRARY_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Costruttore che crea una nuova istanza di un **CD3DX12_DXIL_LIBRARY_SUBOBJECT** inizializzato con il contenuto di un [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) oggetto .

`SetDXILLibrary(const D3D12_SHADER_BYTECODE*)`

Funzione per l'impostazione della libreria DXIL sotto forma di puntatore a un [D3D12_SHADER_BYTECODE](/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_bytecode) passato come parametro.

`DefineExport(LPCWSTR, LPCWSTR = nullptr, D3D12_EXPORT_FLAGS)`

Definisce un simbolo esportato dal sottooggetto. Accetta un [D3D12_EXPORT_FLAGS](/windows/win32/api/d3d12/ne-d3d12-d3d12_export_flags) come parametro facoltativo.

`DefineExports(LPCWSTR(&)[N]);`

Definisce una matrice di *N simboli* esportati dal sottooggetto. Il parametro di modello *N* specifica il numero di elementi nella matrice.

`DefineExports(const LPCWSTR*, UINT)`

Definisce una matrice di simboli esportati dal sottooggetto.

`Type`

Recupera il tipo del sottooggetto, rappresentato dalla [D3D12_STATE_SUBOBJECT_TYPE_DXIL_LIBRARY](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) costante.

`operator const D3D12_STATE_SUBOBJECT&`

Operatore di conversione che restituisce un riferimento a una costante [**D3D12_STATE_SUBOBJECT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) oggetto che descrive l'oggetto stato.

`operator const D3D12_DXIL_LIBRARY_DESC&`

Operatore di conversione che restituisce un riferimento a una costante [**D3D12_DXIL_LIBRARY_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_dxil_library_desc) oggetto che descrive l'oggetto stato.

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Vedi anche

* [Strutture helper per Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
