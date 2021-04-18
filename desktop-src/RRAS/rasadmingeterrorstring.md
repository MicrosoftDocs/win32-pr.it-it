---
title: Funzione RasAdminGetErrorString (rassapi. h)
description: La funzione RasAdminGetErrorString recupera una stringa di messaggio che corrisponde a un codice di errore RAS restituito da una delle funzioni di amministrazione del server RAS (RasAdmin).
ms.assetid: b51bc1f9-fed7-43b6-9a07-f19ea4c0cd01
keywords:
- RAS funzione RasAdminGetErrorString
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
ms.openlocfilehash: 7dc239c5f26061b5234631079ba21ce0d24ad570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327906"
---
# <a name="rasadmingeterrorstring-function"></a>RasAdminGetErrorString (funzione)

\[Questa funzione viene fornita solo per compatibilità con le versioni precedenti di Windows NT Server 4,0. Restituisce la \_ chiamata \_ di errore non \_ implementata in Windows Server 2003. Le applicazioni devono utilizzare la funzione [**MprAdminGetErrorString**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring) .\]

La funzione **RasAdminGetErrorString** recupera una stringa di messaggio che corrisponde a un codice di errore RAS restituito da una delle funzioni di amministrazione del server RAS (RASADMIN). Queste stringhe di messaggio vengono recuperate dal Rasmsg.dll installato come parte di RAS.

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

*ResourceId* \[ in\]
</dt> <dd>

Specifica un codice di errore restituito da una delle funzioni RasAdmin. Questo valore deve essere compreso nell'intervallo di codici di errore da RASBASE a RASBASEEND. Questi sono definiti in Raserror. h.

</dd> <dt>

*lpszString* \[ out\]
</dt> <dd>

Puntatore a un buffer che riceve il messaggio di errore corrispondente al codice di errore specificato.

</dd> <dt>

*InBufSize* \[ in\]
</dt> <dd>

Specifica la dimensione, in caratteri, del buffer *lpszString* . I messaggi di errore sono in genere di 80 caratteri o meno. una dimensione del buffer di 512 caratteri è sempre adeguata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un codice di errore. Questo valore può essere un ultimo valore di errore impostato dalle funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc)o [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa) . oppure può essere uno dei codici di errore seguenti.



| Valore                                                                                                      | Significato                                                                  |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**ERRORE \_ parametro non valido \_**</dt> </dl>   | I parametri *resourceId* o *lpszString* non sono validi.<br/>      |
| <dl> <dt>**ERRORE \_ buffer insufficiente \_**</dt> </dl> | La dimensione specificata dal parametro *InBufSize* è troppo piccola.<br/> |



 

Non sono disponibili informazioni estese sull'errore per questa funzione. non chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Commenti

Le funzioni RasAdmin possono restituire codici di errore non compresi nell'intervallo supportato dalla funzione **RasAdminGetErrorString** . Ad esempio, le funzioni RasAdmin possono restituire codici di errore definiti in Lmerr. h e Winerror. h. Prima di chiamare **RasAdminGetErrorString**, verificare che il codice di errore sia compreso nell'intervallo da rasbase a RASBASEEND, come definito in Raserror. h.

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

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc)
</dt> <dt>

[**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)
</dt> </dl>

 

