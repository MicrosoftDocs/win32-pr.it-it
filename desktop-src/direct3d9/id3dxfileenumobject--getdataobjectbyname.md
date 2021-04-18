---
description: Recupera l'oggetto dati con il nome specificato.
ms.assetid: ed53d871-24e8-4c51-8897-1055ef8a9af1
title: 'Metodo ID3DXFileEnumObject:: GetDataObjectByName (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetDataObjectByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 41850615726ac15e890162c6e28df9b638c582a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323062"
---
# <a name="id3dxfileenumobjectgetdataobjectbyname-method"></a>Metodo ID3DXFileEnumObject:: GetDataObjectByName

Recupera l'oggetto dati con il nome specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDataObjectByName(
  [in]  LPCSTR        szName,
  [out] ID3DXFileData **ppObj
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*szName* \[ in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntatore al nome richiesto.

</dd> <dt>

*ppObj* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DXFileData**](id3dxfiledata.md)\*\***

Indirizzo di un puntatore a un'interfaccia [**ID3DXFileData**](id3dxfiledata.md) , che rappresenta l'oggetto dati di file restituito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: DXFILEERR \_ BADVALUE, DXFILEERR \_ NotFound.

## <a name="remarks"></a>Commenti

Ottenere il nome szName dell'oggetto dati del file corrente con il metodo [**ID3DXFileData:: GetName**](id3dxfiledata--getname.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFileEnumObject](id3dxfileenumobject.md)
</dt> </dl>

 

 
