---
title: Funzione RasAdminPortClearStatistics (rassapi. h)
description: La funzione RasAdminPortClearStatistics Reimposta i contatori che rappresentano le varie statistiche restituite dalla funzione RasAdminPortGetInfo nella struttura delle \_ statistiche della porta RAS \_ . I contatori vengono reimpostati su zero e avviano l'accumulo.
ms.assetid: d2ce4652-1034-4ded-aa26-2678c719d5b9
keywords:
- RAS funzione RasAdminPortClearStatistics
topic_type:
- apiref
api_name:
- RasAdminPortClearStatistics
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57943fbefcba1625c7badff25827c62eaca8a8c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327902"
---
# <a name="rasadminportclearstatistics-function"></a>RasAdminPortClearStatistics (funzione)

\[Questa funzione viene fornita solo per compatibilità con le versioni precedenti di Windows NT Server 4,0. Restituisce la \_ chiamata \_ di errore non \_ implementata in Windows Server 2003. Le applicazioni devono utilizzare la funzione [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats) .\]

La funzione **RasAdminPortClearStatistics** Reimposta i contatori che rappresentano le varie statistiche restituite dalla funzione [**RasAdminPortGetInfo**](rasadminportgetinfo.md) nella struttura [**delle \_ \_ statistiche della porta RAS**](ras-port-statistics-str.md) . I contatori vengono reimpostati su zero e avviano l'accumulo.

## <a name="syntax"></a>Sintassi


```C++
DWORD RasAdminPortClearStatistics(
  _In_ const WCHAR *lpszServer,
  _In_ const WCHAR *lpszPort
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpszServer* \[ in\]
</dt> <dd>

Puntatore a una stringa Unicode con terminazione null che specifica il nome del server RAS. Specificare il nome con i \\ \\ caratteri "" iniziali nel formato: \\ \\ *ServerName*.

</dd> <dt>

*lpszPort* \[ in\]
</dt> <dd>

Puntatore a una stringa Unicode con terminazione null che specifica il nome della porta nel server.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.

Se la funzione ha esito negativo, il valore restituito può essere il codice di errore seguente.



| Valore                                                                                                 | Significato                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**ERRORE \_ dev \_ non \_ esiste**</dt> </dl> | La porta specificata non è valida.<br/> |



 

Non sono disponibili informazioni estese sull'errore per questa funzione. non chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Commenti

La funzione **RasAdminPortClearStatistics** Cancella le statistiche sul server, non localmente all'interno dell'applicazione che effettua la chiamata. Ciò significa che le statistiche vengono reimpostate anche per qualsiasi altra applicazione che sta monitorando la porta specificata.

Se la porta *lpszPort* fa parte di una connessione a più collegamenti, **RasAdminPortClearStatistics** Reimposta le statistiche per la porta specificata, la funzione Reimposta anche le statistiche cumulative per la connessione a più collegamenti. Tuttavia, la funzione non influisce sulle singole statistiche per le altre porte che fanno parte della connessione a più collegamenti.

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

[**\_statistiche porta \_ RAS**](ras-port-statistics-str.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

