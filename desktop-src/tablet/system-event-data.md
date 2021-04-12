---
description: Contiene informazioni su un evento di sistema tablet.
ms.assetid: 725f4b43-0bcb-4452-a87f-b24a85de0049
title: Struttura SYSTEM_EVENT_DATA
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
ms.openlocfilehash: 5d77c78a78a6cecae0368e8d9192a0dc0efc10e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234077"
---
# <a name="system_event_data-structure"></a>\_ \_ Struttura dei dati degli eventi di sistema

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

Valori di bit per i modificatori. Per ulteriori informazioni, vedere la sezione Osservazioni.

</dd> <dt>

**Tasto wsul**
</dt> <dd>

Analizza il codice per il carattere della tastiera.

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

Tipo di cursore che ha causato l'evento. Per ulteriori informazioni, vedere la sezione Osservazioni.

</dd> <dt>

**dwButtonState**
</dt> <dd>

Stato dei pulsanti al momento dell'evento di sistema.

</dd> </dl>

## <a name="remarks"></a>Commenti

Gli eventi di sistema seguenti vengono definiti per l'utilizzo nel membro **bModifier** .



| Valore               | Descrizione                  |
|---------------------|------------------------------|
| \_modificatore se \_ CTRL  | È stato premuto il tasto CTRL. |
| \_ALT modificatore se \_   | È stato premuto il tasto ALT.     |
| \_MAIUSC se modificatore \_ | Il tasto MAIUSC è stato premuto.   |



 

Gli eventi di sistema seguenti vengono definiti per l'utilizzo nel membro **bCursorMode** .



| Valore              | Descrizione               |
|--------------------|---------------------------|
| \_cursore normale \_ se | Indica il suggerimento della penna.    |
| \_cursore gomma se \_ | Indica la gomma della penna. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Metodo IStylusPlugin:: SystemEvent**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-systemevent)
</dt> <dt>

[**Metodo ITabletEventSink:: SystemEvent**](itableteventsink-systemevent.md)
</dt> </dl>

 

 




