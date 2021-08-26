---
title: Funzione RasAdminServerGetInfo (Rassapi.h)
description: La funzione RasAdminServerGetInfo ottiene la configurazione del server di un server RAS.
ms.assetid: a1c371fd-462c-443c-8016-592efb2f0b1a
keywords:
- Funzione RasAdminServerGetInfo RAS
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
ms.openlocfilehash: 1f6f83f7310700e774692d876bda979343da80aa45ea8012bf187e50f0af67bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028451"
---
# <a name="rasadminservergetinfo-function"></a>Funzione RasAdminServerGetInfo

\[Questa funzione viene fornita solo per compatibilità con le versioni precedenti Windows NT Server 4.0. Restituisce ERROR \_ CALL NOT IMPLEMENTED in Windows Server \_ \_ 2003. Le applicazioni devono usare [**la funzione MprAdminServerGetInfo.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminservergetinfo)\]

La **funzione RasAdminServerGetInfo** ottiene la configurazione del server di un server RAS.

## <a name="syntax"></a>Sintassi


```C++
DWORD RasAdminServerGetInfo(
  _In_  const WCHAR         *lpszServer,
  _Out_       PRAS_SERVER_0 pRasServer0
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpszServer* \[ Pollici\]
</dt> <dd>

Puntatore a **una stringa** Unicode con terminazione Null che specifica il nome del server RAS Windows NT/Windows 2000. Se questo parametro è **NULL,** la funzione restituisce informazioni sul computer locale. Specificare il nome con i caratteri \\ \\ " " iniziali, nel formato: \\ \\ *nomeserver*.

</dd> <dt>

*pRasServer0* \[ Cambio\]
</dt> <dd>

Puntatore alla [**struttura \_ RAS SERVER \_ 0**](ras-server-0-str.md) che riceve il numero di porte configurate nel server, il numero di porte attualmente in uso e il numero di versione del server.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è un codice di errore. I codici di errore possibili includono [**quelli restituiti da GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per [**la funzione CallNamedPipe.**](/windows/desktop/api/winbase/nf-winbase-callnamedpipea) Non sono disponibili informazioni estese sugli errori per questa funzione. non chiamare **GetLastError**.

## <a name="remarks"></a>Commenti

Per enumerare tutti i server RAS in un dominio, chiamare la [**funzione NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) e specificare SV \_ TYPE \_ DIALIN per il parametro *servertype.*

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

[**Enumerazione NetServerEnum**](/windows/win32/api/lmserver/nf-lmserver-netserverenum)
</dt> <dt>

[**SERVER \_ RAS \_ 0**](ras-server-0-str.md)
</dt> </dl>

 

