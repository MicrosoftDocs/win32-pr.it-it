---
description: Recupera il GUID del modello dell'oggetto. Deprecato.
ms.assetid: bb4a4a32-a9e7-4caa-869d-24cfb310d8d1
title: Metodo IDirectXFileData::GetType (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetType
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 564d682c606d8b6bc0001f5d430d2d93f36c25210746169af4802512c330da08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118292277"
---
# <a name="idirectxfiledatagettype-method"></a>Metodo IDirectXFileData::GetType

Recupera il GUID del modello dell'oggetto. Deprecato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetType(
  [out, retval] const GUID **ppguid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppguid* \[ out, retval\]
</dt> <dd>

Tipo: **[**CONST GUID**](guid.md) \* \***

Indirizzo di un puntatore per ricevere il GUID del modello dell'oggetto.

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

[IDirectXFileData](idirectxfiledata.md)
</dt> </dl>

 

 




