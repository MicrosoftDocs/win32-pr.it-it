---
description: Recupera l'identificatore dello stilo.
ms.assetid: 27320a2f-1e4a-4d7d-a1f8-5244f4a03415
title: Metodo ITabletCursor::GetId
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetId
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: a7dc053b880c3ebaf4b94ae88a09c85f32f1dd5b8dc335756c8906c9a6f0fb4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938621"
---
# <a name="itabletcursorgetid-method"></a>Metodo ITabletCursor::GetId

Recupera l'identificatore dello stilo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetId(
  [out] CURSOR_ID *pCid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCid* \[ Cambio\]
</dt> <dd>

Identificatore dello stilo tablet.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                            | Descrizione                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Operazione completata.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

## <a name="remarks"></a>Commenti

CURSOR \_ ID è definito come DWORD.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia ITabletCursor**](itabletcursor.md)
</dt> </dl>

 

 




