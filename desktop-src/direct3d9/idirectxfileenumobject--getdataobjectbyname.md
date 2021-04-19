---
description: Recupera l'oggetto dati con il nome specificato. Deprecato.
ms.assetid: d04d5a45-72d9-4256-8700-378e8139ed36
title: 'Metodo IDirectXFileEnumObject:: GetDataObjectByName (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetDataObjectByName
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 858097139702770d148765c4c9a57f6522d9633b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323435"
---
# <a name="idirectxfileenumobjectgetdataobjectbyname-method"></a>Metodo IDirectXFileEnumObject:: GetDataObjectByName

Recupera l'oggetto dati con il nome specificato. Deprecato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDataObjectByName(
  [in]  LPCSTR            szName,
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*szName* \[ in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntatore al nome richiesto.

</dd> <dt>

*ppDataObj* \[ out\]
</dt> <dd>

Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***

Indirizzo di un puntatore a un'interfaccia [**IDirectXFileData**](idirectxfiledata.md) , che rappresenta l'oggetto dati di file restituito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: DXFILEERR \_ BADVALUE, DXFILEERR \_ NotFound.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDirectXFileEnumObject](idirectxfileenumobject.md)
</dt> </dl>

 

 
