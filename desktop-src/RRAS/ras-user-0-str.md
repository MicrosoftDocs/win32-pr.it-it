---
title: RAS_USER_0 (Rassapi.h)
description: La struttura RAS USER 0 viene usata nelle funzioni \_ \_ RasAdminUserSetInfo e RasAdminUserGetInfo per specificare le informazioni su un utente.
ms.assetid: a2d4a935-f46d-4bc2-ada8-beaa3ac74834
keywords:
- RAS_USER_0 struttura RAS
- PRAS_USER_0 del puntatore della struttura RAS
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
ms.openlocfilehash: cbb4b04ddf3b81d330825b3333899e149d2f7b0d1f30c19106c6977e5291846f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789142"
---
# <a name="ras_user_0-structure"></a>Struttura \_ RAS USER \_ 0

\[Questa versione della **struttura RAS \_ USER \_ 0** non è supportata a Windows Vista. Usare invece la versione [**più recente di RAS USER \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) definita in mprapi.h.\]

La **struttura RAS USER \_ \_ 0** viene usata nelle funzioni [**RasAdminUserSetInfo**](rasadminusersetinfo.md) e [**RasAdminUserGetInfo**](rasadminusergetinfo.md) per specificare le informazioni su un utente.

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

Set di flag di bit che specificano i privilegi RAS dell'utente. Questo membro può essere una combinazione del \_ flag RasPRIV DialinPrivilege e di uno dei flag di richiamo. Usare la maschera RASPRIV \_ CallbackType per identificare il tipo di privilegio di callback fornito all'utente. Vengono definiti i flag seguenti.



| Valore                                                                                                                                                                                                                                         | Significato                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="RASPRIV_NoCallback"></span><span id="raspriv_nocallback"></span><span id="RASPRIV_NOCALLBACK"></span><dl> <dt>**RASPRIV \_ NoCallback**</dt> </dl>                             | L'utente non ha privilegi di call-back.<br/>                                               |
| <span id="RASPRIV_AdminSetCallback"></span><span id="raspriv_adminsetcallback"></span><span id="RASPRIV_ADMINSETCALLBACK"></span><dl> <dt>**RASPRIV \_ AdminSetCallback**</dt> </dl>     | L'account utente è configurato in modo che l'amministratore abbia impostato il numero di chiamata.<br/> |
| <span id="RASPRIV_CallerSetCallback"></span><span id="raspriv_callersetcallback"></span><span id="RASPRIV_CALLERSETCALLBACK"></span><dl> <dt>**RASPRIV \_ CallerSetCallback**</dt> </dl> | L'utente remoto può specificare un numero di telefono di chiamata durante la chiamata.<br/>              |
| <span id="RASPRIV_DialinPrivilege"></span><span id="raspriv_dialinprivilege"></span><span id="RASPRIV_DIALINPRIVILEGE"></span><dl> <dt>**RASPRIV \_ DialinPrivilege**</dt> </dl>         | L'utente dispone dell'autorizzazione per accedere a questo server.<br/>                                 |



 

Specificare uno dei flag di callback nella chiamata alla [**funzione RasAdminUserSetInfo.**](rasadminusersetinfo.md)

</dd> <dt>

**szPhoneNumber**
</dt> <dd>

Stringa Unicode con terminazione Null che specifica il numero di telefono di chiamata per l'utente.

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

[**RasAdminUserGetInfo**](rasadminusergetinfo.md)
</dt> <dt>

[**RasAdminUserSetInfo**](rasadminusersetinfo.md)
</dt> </dl>

 

 





