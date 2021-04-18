---
description: Recupera un oggetto figlio in questo oggetto dati del file.
ms.assetid: d8f367dd-8858-48ae-9de5-17de1538aadf
title: 'Metodo ID3DXFileEnumObject:: GetChild (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetChild
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b5b8d535a9060e80318d4043af6362810023b9d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323065"
---
# <a name="id3dxfileenumobjectgetchild-method"></a>Metodo ID3DXFileEnumObject:: GetChild

Recupera un oggetto figlio in questo oggetto dati del file.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetChild(
  [in]  SIZE_T        id,
  [out] ID3DXFileData **ppObj
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ID* \[ in\]
</dt> <dd>

Tipo: **[ **size \_ T**](../winprog/windows-data-types.md)**

ID dell'oggetto figlio da recuperare.

</dd> <dt>

*ppObj* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DXFileData**](id3dxfiledata.md)\*\***

Indirizzo di un puntatore per la ricezione del puntatore a interfaccia dell'oggetto figlio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DXFERR \_ BADVALUE, D3DXFERR \_ NOMOREOBJECTS.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFileEnumObject](id3dxfileenumobject.md)
</dt> </dl>

 

 
