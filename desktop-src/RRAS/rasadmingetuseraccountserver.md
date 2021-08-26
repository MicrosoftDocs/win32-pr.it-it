---
title: Funzione RasAdminGetUserAccountServer (Rassapi.h)
description: La funzione RasAdminGetUserAccountServer recupera il nome del server con il database dell'account utente. Usare il nome del server restituito nelle funzioni RasAdminUserGetInfo e RasAdminUserSetInfo per ottenere o impostare informazioni su un utente specificato.
ms.assetid: db91aa48-32af-49ac-87ed-8c484926ca15
keywords:
- RasAdminGetUserAccountServer funzione RAS
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
ms.openlocfilehash: 4f2ac4052ad4638c3e0e2483adb68857f4c2b670322434107d93100b6a177855
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028541"
---
# <a name="rasadmingetuseraccountserver-function"></a>Funzione RasAdminGetUserAccountServer

\[Questa funzione viene fornita solo per la compatibilità con Windows NT Server 4.0. Restituisce ERROR \_ CALL NOT IMPLEMENTED in Windows Server \_ \_ 2003. Le applicazioni devono usare la [**funzione MprAdminGetPDCServer.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver)\]

La **funzione RasAdminGetUserAccountServer** recupera il nome del server con il database dell'account utente. Usare il nome del server restituito nelle [**funzioni RasAdminUserGetInfo**](rasadminusergetinfo.md) e [**RasAdminUserSetInfo**](rasadminusersetinfo.md) per ottenere o impostare informazioni su un utente specificato.

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

*lpszDomain* \[ Pollici\]
</dt> <dd>

Puntatore a **una stringa** Unicode con terminazione Null che specifica il nome del dominio a cui appartiene il server RAS. Questo parametro è **NULL per** le applicazioni di amministrazione RAS in esecuzione su workstation o server che non sono membri di un dominio. Se questo parametro è **NULL,** il *parametro lpszServer* deve essere diverso da **NULL.**

</dd> <dt>

*lpszServer* \[ Pollici\]
</dt> <dd>

Puntatore a **una stringa** Unicode con terminazione Null che specifica il nome del server RAS. Specificare il nome con caratteri \\ \\ " " iniziali, nel formato: \\ \\ *nomeserver*. Questo parametro può essere **NULL** se il *parametro lpszDomain* non è **NULL.**

</dd> <dt>

*lpszUserAccountServer* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer che riceve una **stringa Unicode** con terminazione Null che specifica il nome di un controller di dominio con il database dell'account utente. Il buffer deve essere sufficientemente grande da contenere il nome del server (UNCLEN +1). La funzione antefissi il nome del server restituito con caratteri \\ \\ " " iniziali, nel formato: \\ \\ *nomeserver*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito può essere il codice di errore seguente.



| Valore                                                                                                    | Significato                                                     |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**ERRORE \_ PARAMETRO NON \_ VALIDO**</dt> </dl> | Sia *lpszDomain che* *lpszServer* sono **NULL.**<br/> |



 

Non sono disponibili informazioni sugli errori estesi per questa funzione. non chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Commenti

La **funzione RasAdminGetUserAccountServer** ottiene il nome del server con il database degli account utente. Questa funzione richiede il nome del server RAS o il nome del dominio in cui risiede il server RAS.

Il *parametro lpszDomain* deve specificare un nome di dominio valido. Questo parametro è **NULL per** le applicazioni di amministrazione RAS in esecuzione su server che non sono membri di un dominio (ad esempio, il server si trova nel proprio gruppo di lavoro). In questo caso, il *parametro lpszServer* deve specificare il nome del server. Per ottenere il nome del server, chiamare la [**funzione GetComputerName.**](/windows/win32/api/winbase/nf-winbase-getcomputernamea) Assicurarsi di antefisare il nome del server con i \\ \\ caratteri " ".

Se il nome del server specificato da *lpszServer* è un server autonomo, ovvero il server o la workstation non è membro di un dominio, il nome del server stesso viene restituito nel buffer *lpszUserAccountServer.*

Usare quindi il nome del server dell'account utente in una chiamata alla funzione [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) per enumerare gli utenti nel database degli account utente.

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

[**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea)
</dt> <dt>

[**RasAdminUserGetInfo**](rasadminusergetinfo.md)
</dt> <dt>

[**RasAdminUserSetInfo**](rasadminusersetinfo.md)
</dt> </dl>

 

