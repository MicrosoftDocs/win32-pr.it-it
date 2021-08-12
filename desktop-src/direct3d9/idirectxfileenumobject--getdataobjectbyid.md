---
description: Recupera l'oggetto dati con il GUID specificato. Deprecato.
ms.assetid: dd079b5c-18e1-4252-aabd-498c24910a08
title: Metodo IDirectXFileEnumObject::GetDataObjectById (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetDataObjectById
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 49bee0f513bcca71a98e72fb3f51e1bcc458083ce9b165b3e5163fb5f6b71708
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118292232"
---
# <a name="idirectxfileenumobjectgetdataobjectbyid-method"></a>Metodo IDirectXFileEnumObject::GetDataObjectById

Recupera l'oggetto dati con il GUID specificato. Deprecato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDataObjectById(
  [in]  REFGUID           rguid,
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*rguid* \[ Pollici\]
</dt> <dd>

Tipo: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**

Riferimento al GUID richiesto.

</dd> <dt>

*ppDataObj* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***

Indirizzo di un puntatore a [**un'interfaccia IDirectXFileData,**](idirectxfiledata.md) che rappresenta l'oggetto dati file restituito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: DXFILEERR \_ BADVALUE, DXFILEERR \_ NOTFOUND.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDirectXFileEnumObject](idirectxfileenumobject.md)
</dt> </dl>

 

 
