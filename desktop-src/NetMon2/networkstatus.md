---
description: La struttura NETWORKSTATUS descrive lo stato corrente dell'oggetto NPP.
ms.assetid: e5e07480-cfc3-408f-9ca2-48a697e4b875
title: Struttura NETWORKSTATUS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NETWORKSTATUS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 067a57dabfb5222deb27de44c60c6eb121cd8c36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530228"
---
# <a name="networkstatus-structure"></a>Struttura NETWORKSTATUS

La struttura **NETWORKSTATUS** descrive lo stato corrente dell'oggetto NPP.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _NETWORKSTATUS {
  DWORD State;
  DWORD Flags;
} NETWORKSTATUS, *LPNETWORKSTATUS;
```



## <a name="members"></a>Members

<dl> <dt>

**State**
</dt> <dd>

Indica lo stato corrente dell'oggetto NPP.



| Valore                                                                                                                                                                                                          | Significato                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="NETWORKSTATUS_STATE_VOID"></span><span id="networkstatus_state_void"></span><dl> <dt>**\_stato NETWORKSTATUS \_ void**</dt> </dl>                | L'oggetto NPP non è connesso oppure è connesso e l'acquisizione non è stata avviata.<br/> |
| <span id="NETWORKSTATUS_STATE_CAPTURING"></span><span id="networkstatus_state_capturing"></span><dl> <dt>**\_acquisizione stato \_ NETWORKSTATUS**</dt> </dl> | L'oggetto NPP sta acquisendo i dati.<br/>                                                   |
| <span id="NETWORKSTATUS_STATE_PAUSED"></span><span id="networkstatus_state_paused"></span><dl> <dt>**\_stato NETWORKSTATUS \_ sospeso**</dt> </dl>          | L'oggetto NPP è stato sospeso durante l'acquisizione dei dati.<br/>                                     |



 

</dd> <dt>

**Flag**
</dt> <dd>

Flag che descrivono lo stato corrente dell'oggetto NPP.



| Valore                                                                                                                                                                                                                             | Significato                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="NETWORKSTATUS_FLAGS_TRIGGER_PENDING"></span><span id="networkstatus_flags_trigger_pending"></span><dl> <dt>**\_trigger flag \_ NETWORKSTATUS \_ in sospeso**</dt> </dl> | È presente un trigger in sospeso per l'oggetto NPP.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si usa questa struttura, è necessario allocare la memoria per la struttura prima di poterla usare e liberare la memoria quando la struttura non è più necessaria.

L'elenco vedere anche nella parte inferiore di questo argomento elenca tutti i metodi che utilizzano questa struttura.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDelaydC:: QueryStatus](idelaydc-querystatus.md)
</dt> <dt>

[IESP:: QueryStatus](iesp-querystatus.md)
</dt> <dt>

[IRTC:: QueryStatus](irtc-querystatus.md)
</dt> <dt>

[IStats:: QueryStatus](istats-querystatus.md)
</dt> </dl>

 

 




