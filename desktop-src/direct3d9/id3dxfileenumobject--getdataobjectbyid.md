---
description: Recupera l'oggetto dati con il GUID specificato.
ms.assetid: c3d598bd-0646-4f99-8517-4475ef7cd8c9
title: 'Metodo ID3DXFileEnumObject:: GetDataObjectById (D3DX9Xof. h)'
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
ms.openlocfilehash: 82a74ca4ff472d678ded92aa01f2c2406560955e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323064"
---
# <a name="id3dxfileenumobjectgetdataobjectbyid-method"></a>Metodo ID3DXFileEnumObject:: GetDataObjectById

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

*rguid* \[ in\]
</dt> <dd>

Tipo: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**

Riferimento al GUID richiesto.

</dd> <dt>

*ppDataObj* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)\***

Indirizzo di un puntatore a un'interfaccia [**ID3DXFileData**](id3dxfiledata.md) , che rappresenta l'oggetto dati di file restituito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: DXFILEERR \_ BADVALUE, DXFILEERR \_ NotFound.

## <a name="remarks"></a>Commenti

Ottenere il GUID rguid dell'oggetto dati del file corrente con il metodo [**ID3DXFileData:: GetId**](id3dxfiledata--getid.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFileEnumObject](id3dxfileenumobject.md)
</dt> </dl>

 

 
