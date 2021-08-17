---
title: RAS_SERVER_0 struttura (Rassapi.h)
description: La struttura \_ RAS SERVER 0 viene usata dalla funzione RasAdminServerGetInfo per restituire informazioni sulle \_ porte configurate in un server RAS.
ms.assetid: 8818ad68-b528-45fe-9ff4-eea194259f25
keywords:
- RAS_SERVER_0 struttura RAS
- PRAS_SERVER_0 puntatore alla struttura RAS
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
ms.openlocfilehash: dbb7a135fd6f8d1d77b59d1085460d51ad5357e47ca1a050e3d1ba6fd89461c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789385"
---
# <a name="ras_server_0-structure"></a>Struttura \_ RAS SERVER \_ 0

\[La **struttura RAS SERVER \_ \_ 0** non è supportata a Windows Vista.\]

La **struttura RAS SERVER \_ \_ 0** viene usata dalla [**funzione RasAdminServerGetInfo**](rasadminservergetinfo.md) per restituire informazioni sulle porte configurate in un server RAS.

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

Specifica il numero totale di porte configurate nel server RAS disponibili per la connessione dei client remoti. Ad esempio, se il numero totale di porte configurate per la connessione a un server è quattro, ma una delle porte è attualmente in uso per la connessione in uscita, **TotalPorts** è tre.

</dd> <dt>

**PortsInUse**
</dt> <dd>

Specifica il numero di porte attualmente in uso dai client remoti.

</dd> <dt>

**RasVersion**
</dt> <dd>

Specifica la versione del server RAS. Usare queste informazioni per eseguire un'azione specifica della versione. Questo membro è uno dei valori seguenti.



| Valore                                                                                                                                                                  | Significato                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="RASDOWNLEVEL"></span><span id="rasdownlevel"></span><dl> <dt>**RASDOWNLEVEL**</dt> </dl>              | Indica un server RAS di LAN Manager versione 1.0.<br/>                      |
| <span id="RASADMIN_35"></span><span id="rasadmin_35"></span><dl> <dt>**RASADMIN \_ 35**</dt> </dl>                | Indica un server o Windows NT Server 3.51 e versioni precedenti.<br/> |
| <span id="RASADMIN_CURRENT"></span><span id="rasadmin_current"></span><dl> <dt>**RASADMIN \_ CURRENT**</dt> </dl> | Indica un Windows NT server o client RAS 4.0.<br/>                     |



 

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Rassapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica del servizio di accesso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Strutture di amministrazione del server RAS](ras-server-administration-structures.md)
</dt> <dt>

[**RasAdminServerGetInfo**](rasadminservergetinfo.md)
</dt> </dl>

 

 





