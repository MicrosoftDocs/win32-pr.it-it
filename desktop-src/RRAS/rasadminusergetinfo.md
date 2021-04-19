---
title: Funzione RasAdminUserGetInfo (rassapi. h)
description: La funzione RasAdminUserGetInfo ottiene le informazioni relative al numero di telefono di callback e alle autorizzazioni RAS per un utente specificato.
ms.assetid: 178ff775-9cd2-43f0-9a9a-dbae337c5fe8
keywords:
- RAS funzione RasAdminUserGetInfo
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
ms.openlocfilehash: 89fe08a918a958ffb5a656ce2c76cecec31cbb61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327900"
---
# <a name="rasadminusergetinfo-function"></a>RasAdminUserGetInfo (funzione)

\[Questa funzione viene fornita solo per compatibilità con le versioni precedenti di Windows NT Server 4,0. Restituisce la \_ chiamata \_ di errore non \_ implementata in Windows Server 2003. Le applicazioni devono utilizzare la funzione [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) .\]

La funzione **RasAdminUserGetInfo** ottiene le informazioni relative al numero di telefono di callback e alle autorizzazioni RAS per un utente specificato.

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

*lpszUserAccountServer* \[ in\]
</dt> <dd>

Puntatore a una stringa Unicode con terminazione null che specifica il nome del controller di dominio primario o di backup con il database degli account utente. Utilizzare la funzione [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) per ottenere il nome del server.

</dd> <dt>

*lpszUser* \[ in\]
</dt> <dd>

Puntatore a una stringa Unicode con terminazione null che specifica il nome dell'utente per il quale ottenere le informazioni RAS.

</dd> <dt>

*pRasUser0* 
</dt> <dd>

Puntatore alla struttura [**dell' \_ utente RAS \_ 0**](ras-user-0-str.md) che riceve i dati RAS per l'utente specificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.

Se la funzione ha esito negativo, il valore restituito può essere il codice di errore seguente.



| Valore                                                                                            | Significato                                                  |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**\_BUFTOOSMALL Nerr**</dt> </dl> | Memoria insufficiente per eseguire questa funzione.<br/> |



 

Non sono disponibili informazioni estese sull'errore per questa funzione. non chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows 2000 Professional<br/>                                                   |
| Fine del supporto server<br/> | Windows 2000 Server<br/>                                                         |
| Intestazione<br/>                | <dl> <dt>Rassapi. h</dt> </dl>   |
| Libreria<br/>               | <dl> <dt>Rassapi. lib</dt> </dl> |
| DLL<br/>                   | <dl> <dt>Rassapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica del servizio di accesso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Funzioni di amministrazione del server RAS](ras-server-administration-functions.md)
</dt> <dt>

[**\_Utente RAS \_ 0**](ras-user-0-str.md)
</dt> <dt>

[**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md)
</dt> <dt>

[**RasAdminUserSetInfo**](rasadminusersetinfo.md)
</dt> </dl>

 

