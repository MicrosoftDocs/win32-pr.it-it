---
description: Recupera un puntatore al GUID che identifica un oggetto file DirectX. Deprecato.
ms.assetid: 74c7a1d9-85e4-43eb-bcd8-1f3ddd713e9f
title: Metodo IDirectXFileObject::GetId (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject.GetId
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 5cb6788afe0b937822b8895790584f6928a7b5aecb564a31540337935763b2f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118800182"
---
# <a name="idirectxfileobjectgetid-method"></a>Metodo IDirectXFileObject::GetId

Recupera un puntatore al GUID che identifica un oggetto file DirectX. Deprecato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetId(
  [out, retval] 
            LPGUID pGuid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pGuid* \[ out, retval\]
</dt> <dd>

Tipo: **LPGUID**

Puntatore a un GUID per ricevere l'ID dell'oggetto. La funzione imposta il GUID su un GUID **NULL** se l'oggetto non ha un ID.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK. Se il metodo ha esito negativo, il valore restituito può essere DXFILEERR \_ BADVALUE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDirectXFileObject](idirectxfileobject.md)
</dt> </dl>

 

 




