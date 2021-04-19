---
description: Recupera un puntatore al GUID che identifica un oggetto file DirectX. Deprecato.
ms.assetid: 74c7a1d9-85e4-43eb-bcd8-1f3ddd713e9f
title: 'Metodo IDirectXFileObject:: GetId (DXFile. h)'
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
ms.openlocfilehash: 336dbde487ecd1b3af7b32d3743f037c235952f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322536"
---
# <a name="idirectxfileobjectgetid-method"></a>Metodo IDirectXFileObject:: GetId

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

Puntatore a un GUID per ricevere l'ID dell'oggetto. La funzione imposterà il GUID su un GUID **null** se l'oggetto non dispone di un ID.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK. Se il metodo ha esito negativo, il valore restituito può essere DXFILEERR \_ BADVALUE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDirectXFileObject](idirectxfileobject.md)
</dt> </dl>

 

 




