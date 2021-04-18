---
title: Funzione RasAdminServerGetInfo (rassapi. h)
description: La funzione RasAdminServerGetInfo ottiene la configurazione del server di un server RAS.
ms.assetid: a1c371fd-462c-443c-8016-592efb2f0b1a
keywords:
- RAS funzione RasAdminServerGetInfo
topic_type:
- apiref
api_name:
- RasAdminServerGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 115a2421db5efbafb72d73952684ff7758c6995b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330764"
---
# <a name="rasadminservergetinfo-function"></a>RasAdminServerGetInfo (funzione)

\[Questa funzione viene fornita solo per compatibilità con le versioni precedenti di Windows NT Server 4,0. Restituisce la \_ chiamata \_ di errore non \_ implementata in Windows Server 2003. Le applicazioni devono utilizzare la funzione [**MprAdminServerGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminservergetinfo) .\]

La funzione **RasAdminServerGetInfo** ottiene la configurazione del server di un server RAS.

## <a name="syntax"></a>Sintassi


```C++
DWORD RasAdminServerGetInfo(
  _In_  const WCHAR         *lpszServer,
  _Out_       PRAS_SERVER_0 pRasServer0
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpszServer* \[ in\]
</dt> <dd>

Puntatore a una stringa Unicode con terminazione **null** che specifica il nome del server RAS Windows NT/Windows 2000. Se questo parametro è **null**, la funzione restituisce informazioni sul computer locale. Specificare il nome con i \\ \\ caratteri "" iniziali nel formato: \\ \\ *ServerName*.

</dd> <dt>

*pRasServer0* \[ out\]
</dt> <dd>

Puntatore alla struttura [**del \_ server RAS \_ 0**](ras-server-0-str.md) che riceve il numero di porte configurate nel server, il numero di porte attualmente in uso e il numero di versione del server.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un codice di errore. I codici di errore possibili includono quelli restituiti da [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per la funzione [**CallNamedPipe**](/windows/desktop/api/winbase/nf-winbase-callnamedpipea) . Non sono disponibili informazioni estese sull'errore per questa funzione. non chiamare **GetLastError**.

## <a name="remarks"></a>Commenti

Per enumerare tutti i server RAS in un dominio, chiamare la funzione [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) e specificare SV \_ digitare \_ dialin per il parametro *ServerType* .

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

[**NetServerEnum**](/windows/win32/api/lmserver/nf-lmserver-netserverenum)
</dt> <dt>

[**\_Server RAS \_ 0**](ras-server-0-str.md)
</dt> </dl>

 

