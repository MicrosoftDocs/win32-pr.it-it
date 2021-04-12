---
title: Struttura RAS_USER_0 (rassapi. h)
description: La \_ struttura RAS user \_ 0 viene utilizzata nelle funzioni RasAdminUserSetInfo e RasAdminUserGetInfo per specificare le informazioni relative a un utente.
ms.assetid: a2d4a935-f46d-4bc2-ada8-beaa3ac74834
keywords:
- RAS struttura RAS_USER_0
- RAS puntatore alla struttura PRAS_USER_0
topic_type:
- apiref
api_name:
- RAS_USER_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c79a6b946ed9d10cd2bfc989f8cde27fad2ffa92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517716"
---
# <a name="ras_user_0-structure"></a>\_Struttura utente RAS \_ 0

\[Questa versione della struttura **RAS \_ User \_ 0** non è supportata a partire da Windows Vista. Usare invece il [**nuovo \_ utente RAS \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) definito in mprapi. h.\]

La struttura **RAS \_ User \_ 0** viene utilizzata nelle funzioni [**RasAdminUserSetInfo**](rasadminusersetinfo.md) e [**RasAdminUserGetInfo**](rasadminusergetinfo.md) per specificare le informazioni relative a un utente.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _RAS_USER_0 {
  BYTE  bfPrivilege;
  WCHAR szPhoneNumber[RASSAPI_MAX_PHONENUMBER_SIZE + 1];
} RAS_USER_0, *PRAS_USER_0;
```



## <a name="members"></a>Members

<dl> <dt>

**bfPrivilege**
</dt> <dd>

Set di flag di bit che specificano i privilegi RAS dell'utente. Questo membro può essere una combinazione del \_ flag DialinPrivilege di RASPRIV e di uno dei flag di chiamata. Usare la \_ maschera RASPRIV CallbackType per identificare il tipo di privilegio di callback fornito all'utente. Vengono definiti i flag seguenti.



| Valore                                                                                                                                                                                                                                         | Significato                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="RASPRIV_NoCallback"></span><span id="raspriv_nocallback"></span><span id="RASPRIV_NOCALLBACK"></span><dl> <dt>**NoCallback RASPRIV \_**</dt> </dl>                             | L'utente non dispone di alcun privilegio di chiamata.<br/>                                               |
| <span id="RASPRIV_AdminSetCallback"></span><span id="raspriv_adminsetcallback"></span><span id="RASPRIV_ADMINSETCALLBACK"></span><dl> <dt>**\_ADMINSETCALLBACK RASPRIV**</dt> </dl>     | L'account utente è configurato in modo che l'amministratore imposti il numero di chiamate.<br/> |
| <span id="RASPRIV_CallerSetCallback"></span><span id="raspriv_callersetcallback"></span><span id="RASPRIV_CALLERSETCALLBACK"></span><dl> <dt>**\_CALLERSETCALLBACK RASPRIV**</dt> </dl> | Quando si effettua la connessione, l'utente remoto può specificare un numero di telefono di chiamata.<br/>              |
| <span id="RASPRIV_DialinPrivilege"></span><span id="raspriv_dialinprivilege"></span><span id="RASPRIV_DIALINPRIVILEGE"></span><dl> <dt>**\_DIALINPRIVILEGE RASPRIV**</dt> </dl>         | L'utente dispone delle autorizzazioni per connettersi a questo server.<br/>                                 |



 

Specificare uno dei flag di chiamata per la chiamata alla funzione [**RasAdminUserSetInfo**](rasadminusersetinfo.md) .

</dd> <dt>

**szPhoneNumber**
</dt> <dd>

Stringa Unicode con terminazione null che specifica il numero di telefono per l'utente.

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

[**RasAdminUserGetInfo**](rasadminusergetinfo.md)
</dt> <dt>

[**RasAdminUserSetInfo**](rasadminusersetinfo.md)
</dt> </dl>

 

 





