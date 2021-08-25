---
description: Si verifica quando il cursore si sposta sul digitalizzatore del tablet.
ms.assetid: cd2863af-59a9-4dd0-a679-84861a70ef53
title: Metodo ITabletEventSink::CursorMove
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
ms.openlocfilehash: 030fa5ba4adc725288d5135ccd24409d4fc02cddbc16da52aa375a275a73be5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119843491"
---
# <a name="itableteventsinkcursormove-method"></a>Metodo ITabletEventSink::CursorMove

Si verifica quando il cursore si sposta sul digitalizzatore del tablet.

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

*Tcid* 
</dt> <dd>

Identificatore univoco del digitalizzatore tablet.

</dd> <dt>

*Cid* 
</dt> <dd>

Identificatore univoco dello stilo del tablet.

</dd> <dt>

*hWnd* 
</dt> <dd>

Finestra sulla quale è stato spostato il cursore.

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
| <dl> <dt>**S \_ OK**</dt> </dl>   | Operazione completata.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia ITabletEventSink**](itableteventsink.md)
</dt> </dl>

 

 




