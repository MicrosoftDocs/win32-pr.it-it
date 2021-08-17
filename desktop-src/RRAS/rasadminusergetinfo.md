---
title: Funzione RasAdminUserGetInfo (Rassapi.h)
description: La funzione RasAdminUserGetInfo ottiene le autorizzazioni RAS e le informazioni sul numero di telefono di callback per un utente specificato.
ms.assetid: 178ff775-9cd2-43f0-9a9a-dbae337c5fe8
keywords:
- Funzione RasAdminUserGetInfo RAS
topic_type:
- apiref
api_name:
- RasAdminUserGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4cda41447af832bd4ae04a14c6f8038fee4b61a17ac98c919c0b085261b242d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788690"
---
# <a name="rasadminusergetinfo-function"></a>Funzione RasAdminUserGetInfo

\[Questa funzione viene fornita solo per compatibilità con le versioni precedenti Windows NT Server 4.0. Restituisce ERROR \_ CALL NOT IMPLEMENTED in Windows Server \_ \_ 2003. Le applicazioni devono usare [**la funzione MprAdminUserGetInfo.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo)\]

La **funzione RasAdminUserGetInfo** ottiene le autorizzazioni RAS e le informazioni sul numero di telefono di callback per un utente specificato.

## <a name="syntax"></a>Sintassi


```C++
DWORD RasAdminUserGetInfo(
  _In_ const WCHAR       *lpszUserAccountServer,
  _In_ const WCHAR       *lpszUser,
             PRAS_USER_0 pRasUser0
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpszUserAccountServer* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa Unicode con terminazione Null che specifica il nome del controller di dominio primario o di backup con il database dell'account utente. Usare la [**funzione RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) per ottenere il nome del server.

</dd> <dt>

*lpszUser* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa Unicode con terminazione Null che specifica il nome dell'utente per cui ottenere informazioni RAS.

</dd> <dt>

*pRasUser0* 
</dt> <dd>

Puntatore alla [**struttura \_ RAS USER \_ 0**](ras-user-0-str.md) che riceve i dati RAS per l'utente specificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito può essere il codice di errore seguente.



| Valore                                                                                            | Significato                                                  |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NERR \_ BufTooSmall**</dt> </dl> | Memoria insufficiente per eseguire questa funzione.<br/> |



 

Non sono disponibili informazioni estese sugli errori per questa funzione. non chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows 2000 Professional<br/>                                                   |
| Fine del supporto server<br/> | Windows 2000 Server<br/>                                                         |
| Intestazione<br/>                | <dl> <dt>Rassapi.h</dt> </dl>   |
| Libreria<br/>               | <dl> <dt>Rassapi.lib</dt> </dl> |
| DLL<br/>                   | <dl> <dt>Rassapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica del servizio di accesso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Funzioni di amministrazione del server RAS](ras-server-administration-functions.md)
</dt> <dt>

[**UTENTE \_ RAS \_ 0**](ras-user-0-str.md)
</dt> <dt>

[**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md)
</dt> <dt>

[**RasAdminUserSetInfo**](rasadminusersetinfo.md)
</dt> </dl>

 

