---
description: Si verifica quando il cursore viene spostato sul digitalizzatore del tablet.
ms.assetid: cd2863af-59a9-4dd0-a679-84861a70ef53
title: 'Metodo ITabletEventSink:: CursorMove'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorMove
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: f6950e0b30c1b8fc8ccf3e60a8aaa05b9eeb3215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317922"
---
# <a name="itableteventsinkcursormove-method"></a>Metodo ITabletEventSink:: CursorMove

Si verifica quando il cursore viene spostato sul digitalizzatore del tablet.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CursorMove(
   TABLET_CONTEXT_ID tcid,
   CURSOR_ID         cid,
   HWND              hWnd,
   LONG              xPos,
   LONG              yPos
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TCID* 
</dt> <dd>

Dentifier univoco del digitalizzatore del tablet.

</dd> <dt>

*CID* 
</dt> <dd>

Identificatore univoco dello stilo del tablet.

</dd> <dt>

*hWnd* 
</dt> <dd>

Finestra su cui è stato spostato il cursore.

</dd> <dt>

*xPos* 
</dt> <dd>

Posizione X dello stilo.

</dd> <dt>

*yPos* 
</dt> <dd>

Posizione Y dello stilo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                            | Descrizione                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Esito positivo.<br/>                       |
| <dl> <dt>**E \_ non riescono**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia ITabletEventSink**](itableteventsink.md)
</dt> </dl>

 

 




