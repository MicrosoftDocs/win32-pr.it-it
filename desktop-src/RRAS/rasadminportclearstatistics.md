---
title: Funzione RasAdminPortClearStatistics (Rassapi.h)
description: La funzione RasAdminPortClearStatistics reimposta i contatori che rappresentano le varie statistiche segnalate dalla funzione RasAdminPortGetInfo nella struttura RAS \_ PORT \_ STATISTICS. I contatori vengono reimpostati su zero e iniziano ad accumularsi.
ms.assetid: d2ce4652-1034-4ded-aa26-2678c719d5b9
keywords:
- Funzione RasAdminPortClearStatistics RAS
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
ms.openlocfilehash: 3da7d17516e7dd7708821a7c60c2d93db913f25c38471524367ae96494e41f38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788988"
---
# <a name="rasadminportclearstatistics-function"></a>Funzione RasAdminPortClearStatistics

\[Questa funzione viene fornita solo per compatibilità con le versioni precedenti Windows NT Server 4.0. Restituisce ERROR \_ CALL NOT IMPLEMENTED in Windows Server \_ \_ 2003. Le applicazioni devono usare [**la funzione MprAdminPortClearStats.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)\]

La **funzione RasAdminPortClearStatistics** reimposta i contatori che rappresentano le varie statistiche segnalate dalla funzione [**RasAdminPortGetInfo**](rasadminportgetinfo.md) nella [**struttura RAS PORT \_ \_ STATISTICS.**](ras-port-statistics-str.md) I contatori vengono reimpostati su zero e iniziano ad accumularsi.

## <a name="syntax"></a>Sintassi


```C++
DWORD RasAdminPortClearStatistics(
  _In_ const WCHAR *lpszServer,
  _In_ const WCHAR *lpszPort
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpszServer* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa Unicode con terminazione Null che specifica il nome del server RAS. Specificare il nome con i caratteri \\ \\ " " iniziali, nel formato: \\ \\ *nomeserver*.

</dd> <dt>

*lpszPort* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa Unicode con terminazione Null che specifica il nome della porta nel server.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito può essere il codice di errore seguente.



| Valore                                                                                                 | Significato                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**ERRORE \_ SVILUPPO \_ \_ INESISTENTE**</dt> </dl> | La porta specificata non è valida.<br/> |



 

Non sono disponibili informazioni estese sugli errori per questa funzione. non chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Commenti

La **funzione RasAdminPortClearStatistics** cancella le statistiche nel server, non localmente all'interno dell'applicazione che effettua la chiamata. Ciò significa che le statistiche vengono reimpostate anche per qualsiasi altra applicazione che monitora la porta specificata.

Se la porta *lpszPort* fa parte di una connessione multilink, **RasAdminPortClearStatistics** reimposta le statistiche per la porta specificata, la funzione reimposta anche le statistiche cumulative per la connessione multilink. Tuttavia, la funzione non influisce sulle singole statistiche per altre porte che fanno parte della connessione multilink.

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

[**STATISTICHE \_ PORTA \_ RAS**](ras-port-statistics-str.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

