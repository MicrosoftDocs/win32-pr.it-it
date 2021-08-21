---
title: Funzione D3D12DecomposeSubresource (D3dx12.h)
description: Restituisce la sezione mip, la sezione di matrice e la sezione del piano che corrispondono all'indice di sottorisorsa specificato.
ms.assetid: 89FAD7C5-E732-4E74-AC2F-DEECD6ADDA7D
keywords:
- Funzione D3D12DecomposeSubresource
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
ms.openlocfilehash: 1c27089fb09c2408917be06b2f74e6d32f3e2f5aa9b96924de1ab92de190efb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045639"
---
# <a name="d3d12decomposesubresource-function"></a>Funzione D3D12DecomposeSubresource

Restituisce la sezione mip, la sezione di matrice e la sezione del piano che corrispondono all'indice di sottorisorsa specificato.

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

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indice della sottorisorsa.

</dd> <dt>

*MipLevels* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Numero massimo di livelli mipmap nella sottorisorsa.

</dd> <dt>

*ArraySize* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Numero di elementi nella matrice.

</dd> <dt>

*MipSlice* \[ out, ref\]
</dt> <dd>

Tipo: **T**

Restituisce la sezione mip corrispondente all'indice di sottorisorsa specificato.

</dd> <dt>

*ArraySlice* \[ out, ref\]
</dt> <dd>

Tipo: **U**

Restituisce la sezione di matrice corrispondente all'indice di sottorisorsa specificato.

</dd> <dt>

*PlaneSlice* \[ out, ref\]
</dt> <dd>

Tipo: **V**

Restituisce la sezione del piano che corrisponde all'indice di sottorisorsa specificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questa funzione determina quale sezione mip, sezione di matrice e sezione del piano corrispondono a un indice di sottorisorsa specificato. Si tratta di un'utilità utile, anche se è specifica di C++.

Questa funzione viene dichiarata come segue, con parametri templatizzati C++ per i tipi **T**, **U** e **V**:


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
| Intestazione<br/>  | <dl> <dt>D3dx12.h</dt> </dl>  |
| Libreria<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

[Funzioni helper per D3D12](helper-functions-for-d3d12.md)

[Sottorisorse](subresources.md)
