---
title: Funzione D3D12DecomposeSubresource (D3dx12. h)
description: Restituisce la sezione MIP, la sezione della matrice e la sezione del piano che corrispondono all'indice della sottorisorsa specificata.
ms.assetid: 89FAD7C5-E732-4E74-AC2F-DEECD6ADDA7D
keywords:
- D3D12DecomposeSubresource (funzione)
topic_type:
- apiref
api_name:
- D3D12DecomposeSubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec147833ee94969880865f679d40a198e0b22852
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322179"
---
# <a name="d3d12decomposesubresource-function"></a>D3D12DecomposeSubresource (funzione)

Restituisce la sezione MIP, la sezione della matrice e la sezione del piano che corrispondono all'indice della sottorisorsa specificata.

## <a name="syntax"></a>Sintassi


```C++
void inline D3D12DecomposeSubresource(
        UINT Subresource,
        UINT MipLevels,
        UINT ArraySize,
  _Out_ T    &MipSlice,
  _Out_ U    &ArraySlice,
  _Out_ V    &PlaneSlice
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Sottorisorsa* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indice della sottorisorsa.

</dd> <dt>

*MipLevels* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Numero massimo di livelli di mipmap nella sottorisorsa.

</dd> <dt>

*ArraySize* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Numero di elementi nella matrice.

</dd> <dt>

*MipSlice* \[ out, Ref\]
</dt> <dd>

Tipo: **T**

Restituisce la sezione MIP che corrisponde all'indice della sottorisorsa specificata.

</dd> <dt>

*ArraySlice* \[ out, Ref\]
</dt> <dd>

Tipo: **U**

Restituisce la sezione della matrice che corrisponde all'indice della sottorisorsa specificato.

</dd> <dt>

*PlaneSlice* \[ out, Ref\]
</dt> <dd>

Tipo: **V**

Restituisce la sezione del piano che corrisponde all'indice della sottorisorsa specificata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questa funzione determina quali sezioni MIP, sezione della matrice e sezione del piano corrispondono a un indice di sottorisorsa specificato. Si tratta di un'utilità utile, sebbene sia specifica di C++.

Questa funzione viene dichiarata come segue, con i parametri C++ creato un modello per i tipi **T**, **U** e **V**:


```c++
template <typename T, typename U, typename V>
inline void D3D12DecomposeSubresource( UINT Subresource, UINT MipLevels, UINT ArraySize, _Out_ T& MipSlice, _Out_ U& ArraySlice, _Out_ V& PlaneSlice )
{
    MipSlice = static_cast<T>(Subresource % MipLevels);
    ArraySlice = static_cast<U>((Subresource / MipLevels) % ArraySize);
    PlaneSlice = static_cast<V>(Subresource / (MipLevels * ArraySize));
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Libreria<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

[Funzioni helper per D3D12](helper-functions-for-d3d12.md)

[Sottorisorse](subresources.md)
