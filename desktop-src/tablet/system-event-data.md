---
description: Contiene informazioni su un evento di sistema tablet.
ms.assetid: 725f4b43-0bcb-4452-a87f-b24a85de0049
title: SYSTEM_EVENT_DATA struttura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SYSTEM_EVENT_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 58e153da2695990f74d1268aa3e861bb9011b108ebdd1ea2d5128ff6f8e40a20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708211"
---
# <a name="system_event_data-structure"></a>Struttura SYSTEM \_ EVENT \_ DATA

Contiene informazioni su un evento di sistema tablet.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagSYSTEM_EVENT_DATA {
  BYTE  bModifier;
  WCHAR wKey;
  LONG  xPos;
  LONG  yPos;
  BYTE  bCursorMode;
  DWORD dwButtonState;
} SYSTEM_EVENT_DATA;
```



## <a name="members"></a>Members

<dl> <dt>

**bModifier**
</dt> <dd>

Valori di bit per i modificatori. Per altre informazioni, vedere la sezione osservazioni.

</dd> <dt>

**wKey**
</dt> <dd>

Analizzare il codice per il carattere della tastiera.

</dd> <dt>

**xPos**
</dt> <dd>

Posizione X dell'evento.

</dd> <dt>

**yPos**
</dt> <dd>

Posizione Y dell'evento.

</dd> <dt>

**bCursorMode**
</dt> <dd>

Tipo di cursore che ha causato l'evento. Per altre informazioni, vedere la sezione osservazioni.

</dd> <dt>

**dwButtonState**
</dt> <dd>

Stato dei pulsanti al momento dell'evento di sistema.

</dd> </dl>

## <a name="remarks"></a>Commenti

Gli eventi di sistema seguenti sono definiti per l'uso nel **membro bModifier.**



| Valore               | Descrizione                  |
|---------------------|------------------------------|
| \_edizione Standard MODIFICATORE \_ CTRL  | Il tasto CTRL è stato premuto. |
| \_edizione Standard MODIFICATORE \_ ALT   | È stato premuto ALT.     |
| \_edizione Standard SPOSTAMENTO DEI \_ MODIFICATORI | È stato premuto MAIUSC.   |



 

Gli eventi di sistema seguenti sono definiti per l'uso nel **membro bCursorMode.**



| Valore              | Descrizione               |
|--------------------|---------------------------|
| \_edizione Standard CURSORE \_ NORMALE | Indica la punta della penna.    |
| \_edizione Standard CURSORE \_ ERASER | Indica la gomma della penna. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Metodo IStylusPlugin::SystemEvent**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-systemevent)
</dt> <dt>

[**Metodo ITabletEventSink::SystemEvent**](itableteventsink-systemevent.md)
</dt> </dl>

 

 




