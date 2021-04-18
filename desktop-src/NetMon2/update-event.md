---
description: La \_ struttura dell'evento Update aggiorna gli eventi. Questa struttura viene passata di nuovo all'applicazione chiamante tramite la procedura di callback dello stato dell'evento da parte di NPP.
ms.assetid: 6896be5a-f986-44ff-a18b-010f7b9858aa
title: Struttura UPDATE_EVENT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UPDATE_EVENT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3da45020a68114182a71b25ff9bba380d3f89eee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310786"
---
# <a name="update_event-structure"></a>Aggiorna \_ struttura evento

La struttura dell' **\_ evento Update** aggiorna gli eventi. Questa struttura viene passata di nuovo all'applicazione chiamante tramite la procedura di callback dello stato dell'evento da parte di NPP.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _UPDATE_EVENT {
  USHORT       Event;
  DWORD        Action;
  DWORD        Status;
  DWORD        Value;
  __int64      TimeStamp;
  DWORD_PTR    lpUserContext;
  DWORD_PTR    lpReserved;
  UINT         FramesDropped;
  union {
    DWORD                        Reserved;
    LPFRAMETABLE                 lpFrameTable;
    DWORD_PTR                    lpPacketQueue;
    SECURITY_PERMISSION_RESPONSE SecurityResponse;
  };
  LPSTATISTICS lpFinalStats;
} UPDATE_EVENT, *PUPDATE_EVENT;
```



## <a name="members"></a>Members

<dl> <dt>

**Event**
</dt> <dd>

Evento effettivo registrato.

</dd> <dt>

**Azione**
</dt> <dd>

Azione eseguita.

</dd> <dt>

**Status**
</dt> <dd>

Indicazione sullo stato della rete.

</dd> <dt>

**Valore**
</dt> <dd>

Variabile contatore ausiliario.

</dd> <dt>

**TimeStamp**
</dt> <dd>

Eventi contrassegnati, in microsecondi.

</dd> <dt>

**lpUserContext**
</dt> <dd>

Contesto utente fornito dall'applicazione.

</dd> <dt>

**lpReserved**
</dt> <dd>

Driver o NAL use.

</dd> <dt>

**FramesDropped**
</dt> <dd>

Frame RTF rilasciati nel buffer specificato.

</dd> <dt>

**Reserved**
</dt> <dd>

Non viene restituito alcun dato con questa opzione switch.

</dd> <dt>

**lpFrameTable**
</dt> <dd>

Solo RTF.

</dd> <dt>

**lpPacketQueue**
</dt> <dd>

Per le trasmissioni.

</dd> <dt>

**SecurityResponse**
</dt> <dd>

Risposta di monitoraggio sicurezza remota.

</dd> <dt>

**lpFinalStats**
</dt> <dd>

Questa operazione viene compilata solo in caso di interruzioni non correlate alla sicurezza (ad esempio, trigger).

</dd> </dl>

## <a name="remarks"></a>Commenti

Gli utenti di C++ devono tenere presente che la dichiarazione per questo callback deve trovarsi nella parte pubblica del file di intestazione:

``` syntax
static WINAPI DWORD NetworkCallback( UPDATE_EVENT events);
```

L'implementazione deve trovarsi nella sezione protetta del file con estensione cpp:

``` syntax
DWORD WINAPI ClassName::NetworkCallback( UPDATE_EVENT events) {};
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




