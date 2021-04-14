---
description: Recupera l'identificatore dello stilo.
ms.assetid: 27320a2f-1e4a-4d7d-a1f8-5244f4a03415
title: 'Metodo ITabletCursor:: GetId'
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
ms.openlocfilehash: 5d4f71d2cd465bfd2d1ff4c245154a300c431df2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104401758"
---
# <a name="itabletcursorgetid-method"></a>Metodo ITabletCursor:: GetId

Recupera l'identificatore dello stilo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetId(
  [out] CURSOR_ID *pCid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCid* \[ out\]
</dt> <dd>

Identificatore dello stilo del tablet.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                            | Descrizione                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Esito positivo.<br/>                       |
| <dl> <dt>**E \_ non riescono**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

## <a name="remarks"></a>Commenti

\_L'ID del cursore viene definito come un valore DWORD.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia ITabletCursor**](itabletcursor.md)
</dt> </dl>

 

 




