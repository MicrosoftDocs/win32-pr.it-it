---
title: Funzione RasAdminGetErrorString (Rassapi.h)
description: La funzione RasAdminGetErrorString recupera una stringa di messaggio corrispondente a un codice di errore RAS restituito da una delle funzioni di amministrazione del server RAS (RasAdmin).
ms.assetid: b51bc1f9-fed7-43b6-9a07-f19ea4c0cd01
keywords:
- RasAdminGetErrorString (funzione RAS)
topic_type:
- apiref
api_name:
- RasAdminGetErrorString
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a45c768daef7c889351744c5e046c83f4de7e220f59752c1db271067efb68366
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028603"
---
# <a name="rasadmingeterrorstring-function"></a>Funzione RasAdminGetErrorString

\[Questa funzione viene fornita solo per la compatibilità con Windows NT Server 4.0. Restituisce ERROR \_ CALL NOT IMPLEMENTED in Windows Server \_ \_ 2003. Le applicazioni devono usare [**la funzione MprAdminGetErrorString.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring)\]

La **funzione RasAdminGetErrorString** recupera una stringa di messaggio corrispondente a un codice di errore RAS restituito da una delle funzioni di amministrazione del server RAS (RasAdmin). Queste stringhe di messaggio vengono recuperate dal Rasmsg.dll installato come parte di RAS.

## <a name="syntax"></a>Sintassi


```C++
DWORD RasAdminGetErrorString(
  _In_  UINT  ResourceId,
  _Out_ WCHAR *lpszString,
  _In_  DWORD InBufSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ResourceId* \[ Pollici\]
</dt> <dd>

Specifica un codice di errore restituito da una delle funzioni RasAdmin. Questo valore deve essere compreso nell'intervallo di codici di errore da RASBASE a RASBASEEND. Questi sono definiti in Raserror.h.

</dd> <dt>

*lpszString* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer che riceve il messaggio di errore corrispondente al codice di errore specificato.

</dd> <dt>

*InBufSize* \[ Pollici\]
</dt> <dd>

Specifica le dimensioni, in caratteri, del buffer *lpszString.* I messaggi di errore sono in genere di massimo 80 caratteri. una dimensione del buffer di 512 caratteri è sempre adeguata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è un codice di errore. Questo valore può essere un ultimo valore di errore impostato dalle [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc) [**o LoadString.**](/windows/win32/api/winuser/nf-winuser-loadstringa) oppure può essere uno dei codici di errore seguenti.



| Valore                                                                                                      | Significato                                                                  |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**ERRORE \_ PARAMETRO NON \_ VALIDO**</dt> </dl>   | I *parametri ResourceId* *o lpszString* non sono validi.<br/>      |
| <dl> <dt>**ERRORE \_ BUFFER \_ INSUFFICIENTE**</dt> </dl> | Le dimensioni specificate dal *parametro InBufSize* sono troppo piccole.<br/> |



 

Non sono disponibili informazioni sugli errori estesi per questa funzione. non chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Commenti

Le funzioni RasAdmin possono restituire codici di errore non nell'intervallo supportato dalla **funzione RasAdminGetErrorString.** Ad esempio, le funzioni RasAdmin possono restituire codici di errore definiti in Lmerr.h e Winerror.h. Prima di **chiamare RasAdminGetErrorString,** verificare che il codice di errore sia compreso nell'intervallo da RASBASE a RASBASEEND, come definito in Raserror.h.

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

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**Globalalloc**](/windows/win32/api/winbase/nf-winbase-globalalloc)
</dt> <dt>

[**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)
</dt> </dl>

 

