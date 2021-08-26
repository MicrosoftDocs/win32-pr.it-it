---
title: Funzione RasAdminPortDisconnect (Rassapi.h)
description: La funzione RasAdminPortDisconnect disconnette una porta attualmente in uso.
ms.assetid: 7ed3bc46-2d56-44c8-afd5-fcbdad0f7f3a
keywords:
- RasAdminPortDisconnect ( funzione RAS)
topic_type:
- apiref
api_name:
- RasAdminPortDisconnect
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 369a0f3abf4cee54f92c9bfd846557623de5e23fffd4724a701ca7c04aa818af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028521"
---
# <a name="rasadminportdisconnect-function"></a>Funzione RasAdminPortDisconnect

\[Questa funzione viene fornita solo per la compatibilità con Windows NT Server 4.0. Restituisce ERROR \_ CALL NOT IMPLEMENTED in Windows Server \_ \_ 2003. Le applicazioni devono usare la [**funzione MprAdminPortDisconnect.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect)\]

La **funzione RasAdminPortDisconnect** disconnette una porta attualmente in uso.

## <a name="syntax"></a>Sintassi


```C++
DWORD RasAdminPortDisconnect(
  _In_ const WCHAR *lpszServer,
  _In_ const WCHAR *lpszPort
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpszServer* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa Unicode con terminazione Null che specifica il nome del server RAS Windows NT/Windows 2000. Specificare il nome con caratteri \\ \\ " " iniziali, nel formato: \\ \\ *nomeserver*.

</dd> <dt>

*lpszPort* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa Unicode con terminazione Null che specifica il nome della porta nel server.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito può essere uno dei codici di errore seguenti.



| Valore                                                                                               | Significato                                      |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**ERRORE \_ PORTA \_ NON VALIDA**</dt> </dl> | La porta specificata non è valida.<br/>    |
| <dl> <dt>**NERR \_ UserNotFound**</dt> </dl>   | La porta non è attualmente in uso.<br/> |



 

Non sono disponibili informazioni sugli errori estesi per questa funzione. non chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

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
</dt> </dl>

 

