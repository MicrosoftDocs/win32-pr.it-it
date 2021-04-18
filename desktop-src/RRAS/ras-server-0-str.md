---
title: Struttura RAS_SERVER_0 (rassapi. h)
description: La \_ struttura del server RAS \_ 0 viene utilizzata dalla funzione RasAdminServerGetInfo per restituire informazioni sulle porte configurate in un server RAS.
ms.assetid: 8818ad68-b528-45fe-9ff4-eea194259f25
keywords:
- RAS struttura RAS_SERVER_0
- RAS puntatore alla struttura PRAS_SERVER_0
topic_type:
- apiref
api_name:
- RAS_SERVER_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16f910fdfe53221daf8227d9f3e594133548fee9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302186"
---
# <a name="ras_server_0-structure"></a>\_Struttura server RAS \_ 0

\[La struttura del **\_ server RAS \_ 0** non è supportata a partire da Windows Vista.\]

La struttura del **\_ server RAS \_ 0** viene utilizzata dalla funzione [**RasAdminServerGetInfo**](rasadminservergetinfo.md) per restituire informazioni sulle porte configurate in un server RAS.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _RAS_SERVER_0 {
  WORD  TotalPorts;
  WORD  PortsInUse;
  DWORD RasVersion;
} RAS_SERVER_0, *PRAS_SERVER_0;
```



## <a name="members"></a>Members

<dl> <dt>

**TotalPorts**
</dt> <dd>

Specifica il numero totale di porte configurate nel server RAS disponibili per la connessione dei client remoti. Se, ad esempio, il numero totale di porte configurate per la connessione a un server è quattro, ma una delle porte è attualmente in uso per la connessione, **TotalPorts** è tre.

</dd> <dt>

**PortsInUse**
</dt> <dd>

Specifica il numero di porte attualmente utilizzate dai client remoti.

</dd> <dt>

**RasVersion**
</dt> <dd>

Specifica la versione del server RAS. Usare queste informazioni per eseguire un'azione specifica della versione. Questo membro è uno dei valori seguenti.



| Valore                                                                                                                                                                  | Significato                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="RASDOWNLEVEL"></span><span id="rasdownlevel"></span><dl> <dt>**RASDOWNLEVEL**</dt> </dl>              | Indica un server RAS della versione 1,0 di LAN Manager.<br/>                      |
| <span id="RASADMIN_35"></span><span id="rasadmin_35"></span><dl> <dt>**RASADMIN \_ 35**</dt> </dl>                | Indica un server o un client RAS Windows NT Server 3,51 e versioni precedenti.<br/> |
| <span id="RASADMIN_CURRENT"></span><span id="rasadmin_current"></span><dl> <dt>**RASADMIN \_ corrente**</dt> </dl> | Indica un server o un client RAS Windows NT 4,0.<br/>                     |



 

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Rassapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica del servizio di accesso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Strutture di amministrazione del server RAS](ras-server-administration-structures.md)
</dt> <dt>

[**RasAdminServerGetInfo**](rasadminservergetinfo.md)
</dt> </dl>

 

 





