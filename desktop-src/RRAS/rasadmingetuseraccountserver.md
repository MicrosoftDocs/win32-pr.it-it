---
title: Funzione RasAdminGetUserAccountServer (rassapi. h)
description: La funzione RasAdminGetUserAccountServer Recupera il nome del server con il database degli account utente. Usare il nome del server restituito nelle funzioni RasAdminUserGetInfo e RasAdminUserSetInfo per ottenere o impostare le informazioni relative a un utente specificato.
ms.assetid: db91aa48-32af-49ac-87ed-8c484926ca15
keywords:
- RAS funzione RasAdminGetUserAccountServer
topic_type:
- apiref
api_name:
- RasAdminGetUserAccountServer
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c506287d94c5ec64445c74d8364a04db98100751
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327903"
---
# <a name="rasadmingetuseraccountserver-function"></a>RasAdminGetUserAccountServer (funzione)

\[Questa funzione viene fornita solo per compatibilità con le versioni precedenti di Windows NT Server 4,0. Restituisce la \_ chiamata \_ di errore non \_ implementata in Windows Server 2003. Le applicazioni devono utilizzare la funzione [**MprAdminGetPDCServer**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver) .\]

La funzione **RasAdminGetUserAccountServer** Recupera il nome del server con il database degli account utente. Usare il nome del server restituito nelle funzioni [**RasAdminUserGetInfo**](rasadminusergetinfo.md) e [**RasAdminUserSetInfo**](rasadminusersetinfo.md) per ottenere o impostare le informazioni relative a un utente specificato.

## <a name="syntax"></a>Sintassi


```C++
DWORD RasAdminGetUserAccountServer(
  _In_  const WCHAR  *lpszDomain,
  _In_  const WCHAR  *lpszServer,
  _Out_       LPWSTR lpszUserAccountServer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpszDomain* \[ in\]
</dt> <dd>

Puntatore a una stringa Unicode con terminazione **null** che specifica il nome del dominio a cui appartiene il server RAS. Questo parametro è **null** per le applicazioni di amministrazione RAS in esecuzione su workstation o server che non sono membri di un dominio. Se questo parametro è **null**, il parametro *lpszServer* deve essere diverso da **null**.

</dd> <dt>

*lpszServer* \[ in\]
</dt> <dd>

Puntatore a una stringa Unicode con terminazione **null** che specifica il nome del server RAS. Specificare il nome con i \\ \\ caratteri "" iniziali nel formato: \\ \\ *ServerName*. Questo parametro può essere **null** se il parametro *LpszDomain* non è **null**.

</dd> <dt>

*lpszUserAccountServer* \[ out\]
</dt> <dd>

Puntatore a un buffer che riceve una stringa Unicode con terminazione **null** che specifica il nome di un controller di dominio con il database degli account utente. Il buffer deve essere sufficientemente grande da contenere il nome del server (UNCLEn + 1). La funzione prefissa il nome del server restituito con i \\ \\ caratteri "" iniziali, nel formato: \\ \\ *ServerName*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.

Se la funzione ha esito negativo, il valore restituito può essere il codice di errore seguente.



| Valore                                                                                                    | Significato                                                     |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**ERRORE \_ parametro non valido \_**</dt> </dl> | Sia *lpszDomain* che *lpszServer* sono **null**.<br/> |



 

Non sono disponibili informazioni estese sull'errore per questa funzione. non chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Commenti

La funzione **RasAdminGetUserAccountServer** ottiene il nome del server con il database degli account utente. Questa funzione richiede il nome del server RAS o il nome del dominio in cui risiede il server RAS.

Il parametro *lpszDomain* deve specificare un nome di dominio valido. Questo parametro è **null** per le applicazioni di amministrazione RAS in esecuzione su server che non sono membri di un dominio (ad esempio, il server si trova nel proprio gruppo di lavoro). In questo caso, il parametro *lpszServer* deve specificare il nome del server. Per ottenere il nome del server, chiamare la funzione [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea) . Assicurarsi di anteporre al nome del server i caratteri " \\ \\ ".

Se il nome del server specificato da *lpszServer* è un server autonomo (ovvero, il server o la workstation non è un membro di un dominio), il nome del server stesso viene restituito nel buffer *lpszUserAccountServer* .

Utilizzare quindi il nome del server di account utente in una chiamata alla funzione [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) per enumerare gli utenti nel database degli account utente.

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

[**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea)
</dt> <dt>

[**RasAdminUserGetInfo**](rasadminusergetinfo.md)
</dt> <dt>

[**RasAdminUserSetInfo**](rasadminusersetinfo.md)
</dt> </dl>

 

