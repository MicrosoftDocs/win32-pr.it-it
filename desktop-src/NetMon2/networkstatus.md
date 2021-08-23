---
description: La struttura NETWORKSTATUS descrive lo stato corrente di NPP.
ms.assetid: e5e07480-cfc3-408f-9ca2-48a697e4b875
title: Struttura NETWORKSTATUS (Netmon.h)
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
ms.openlocfilehash: 3031cd8bd8f1af4e5ea5f03aec93b9a2f28b3ec098a8110563bb89869c97ae3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799521"
---
# <a name="networkstatus-structure"></a>Struttura NETWORKSTATUS

La **struttura NETWORKSTATUS** descrive lo stato corrente di NPP.

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

Indica lo stato corrente di NPP.



| Valore                                                                                                                                                                                                          | Significato                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="NETWORKSTATUS_STATE_VOID"></span><span id="networkstatus_state_void"></span><dl> <dt>**NETWORKSTATUS \_ STATE \_ VOID**</dt> </dl>                | NPP non è connesso oppure è connesso e l'acquisizione non viene avviata.<br/> |
| <span id="NETWORKSTATUS_STATE_CAPTURING"></span><span id="networkstatus_state_capturing"></span><dl> <dt>**ACQUISIZIONE DELLO STATO \_ NETWORKSTATUS \_**</dt> </dl> | NPP sta acquisendo i dati.<br/>                                                   |
| <span id="NETWORKSTATUS_STATE_PAUSED"></span><span id="networkstatus_state_paused"></span><dl> <dt>**STATO DI \_ STATO DI RETE \_ SOSPESO**</dt> </dl>          | Il servizio NPP è stato sospeso durante l'acquisizione dei dati.<br/>                                     |



 

</dd> <dt>

**Flag**
</dt> <dd>

Flag che descrivono lo stato corrente di NPP.



| Valore                                                                                                                                                                                                                             | Significato                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="NETWORKSTATUS_FLAGS_TRIGGER_PENDING"></span><span id="networkstatus_flags_trigger_pending"></span><dl> <dt>**TRIGGER FLAG NETWORKSTATUS \_ \_ IN \_ SOSPESO**</dt> </dl> | È presente un trigger in sospeso per NPP.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si usa questa struttura, è necessario allocare la memoria per la struttura prima di poterla usare e liberare la memoria quando la struttura non è più necessaria.

L'elenco Vedere anche nella parte inferiore di questo argomento elenca tutti i metodi che usano questa struttura.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDelaydC::QueryStatus](idelaydc-querystatus.md)
</dt> <dt>

[IESP::QueryStatus](iesp-querystatus.md)
</dt> <dt>

[IRTC::QueryStatus](irtc-querystatus.md)
</dt> <dt>

[IStats::QueryStatus](istats-querystatus.md)
</dt> </dl>

 

 




