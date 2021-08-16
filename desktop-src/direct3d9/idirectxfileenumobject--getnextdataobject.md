---
description: Recupera l'oggetto di primo livello successivo nel file DirectX. Deprecato.
ms.assetid: 91cd3205-5603-4a62-aab2-7ef4adb9e6d1
title: Metodo IDirectXFileEnumObject::GetNextDataObject (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetNextDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 42d95fcee1b431f5121389d7bb6595e5c53ca56298c75ed6010ee86733c310e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985131"
---
# <a name="idirectxfileenumobjectgetnextdataobject-method"></a>Metodo IDirectXFileEnumObject::GetNextDataObject

Recupera l'oggetto di primo livello successivo nel file DirectX. Deprecato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetNextDataObject(
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppDataObj* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***

Indirizzo di un puntatore a [**un'interfaccia IDirectXFileData,**](idirectxfiledata.md) che rappresenta l'oggetto dati del file restituito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: DXFILEERR \_ BADVALUE, DXFILEERR \_ NOMOREOBJECTS

## <a name="remarks"></a>Commenti

Gli oggetti di primo livello sono sempre oggetti dati. Gli oggetti riferimento ai dati e gli oggetti binari possono essere solo elementi figlio di oggetti dati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDirectXFileEnumObject](idirectxfileenumobject.md)
</dt> </dl>

 

 




