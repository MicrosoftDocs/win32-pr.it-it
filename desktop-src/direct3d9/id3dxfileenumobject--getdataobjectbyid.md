---
description: Recupera l'oggetto dati con il GUID specificato.
ms.assetid: c3d598bd-0646-4f99-8517-4475ef7cd8c9
title: Metodo ID3DXFileEnumObject::GetDataObjectById (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetDataObjectById
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1a99da554a404a9bcc279830eaf50710a67a8c62bb61d1b67ac84c90b8fdc594
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118661"
---
# <a name="id3dxfileenumobjectgetdataobjectbyid-method"></a>Metodo ID3DXFileEnumObject::GetDataObjectById

Recupera l'oggetto dati con il GUID specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDataObjectById(
  [in]  REFGUID        rguid,
  [out] LPD3DXFILEDATA *ppDataObj
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

Tipo: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)\***

Indirizzo di un puntatore a [**un'interfaccia ID3DXFileData,**](id3dxfiledata.md) che rappresenta l'oggetto dati del file restituito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: DXFILEERR \_ BADVALUE, DXFILEERR \_ NOTFOUND.

## <a name="remarks"></a>Commenti

Ottenere il GUID rguid dell'oggetto dati del file corrente con il [**metodo ID3DXFileData::GetId.**](id3dxfiledata--getid.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFileEnumObject](id3dxfileenumobject.md)
</dt> </dl>

 

 
