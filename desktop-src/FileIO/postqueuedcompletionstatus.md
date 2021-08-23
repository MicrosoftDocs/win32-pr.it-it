---
description: Invia un pacchetto di completamento I/O a una porta di completamento I/O.
ms.assetid: 69a9b1e5-2d40-42de-a14a-f7b6f29bf571
title: Funzione PostQueuedCompletionStatus (IoAPI.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PostQueuedCompletionStatus
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: e56bad8b9de85f22836f9446b67340d22e71fe83552da6796e7864d3baddae4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683361"
---
# <a name="postqueuedcompletionstatus-function"></a>Funzione PostQueuedCompletionStatus

Invia un pacchetto di completamento I/O a una porta di completamento I/O.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI PostQueuedCompletionStatus(
  _In_     HANDLE       CompletionPort,
  _In_     DWORD        dwNumberOfBytesTransferred,
  _In_     ULONG_PTR    dwCompletionKey,
  _In_opt_ LPOVERLAPPED lpOverlapped
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*CompletionPort* \[ Pollici\]
</dt> <dd>

Handle di una porta di completamento I/O in cui deve essere inviato il pacchetto di completamento di I/O.

</dd> <dt>

*dwNumberOfBytesTransferred* \[ Pollici\]
</dt> <dd>

Valore da restituire tramite il parametro *lpNumberOfBytesTransferred* della [**funzione GetQueuedCompletionStatus.**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

</dd> <dt>

*dwCompletionKey* \[ Pollici\]
</dt> <dd>

Valore da restituire tramite il *parametro lpCompletionKey* della [**funzione GetQueuedCompletionStatus.**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

</dd> <dt>

*lpOverlapped* \[ in, facoltativo\]
</dt> <dd>

Valore da restituire tramite il *parametro lpOverlapped* della [**funzione GetQueuedCompletionStatus.**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero. Per ottenere informazioni estese sugli errori, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

## <a name="remarks"></a>Commenti

Il pacchetto di completamento I/O soddisferà una chiamata in sospeso alla [**funzione GetQueuedCompletionStatus.**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) Questa funzione restituisce con i tre valori passati come secondo, terzo e quarto parametro della chiamata a **PostQueuedCompletionStatus**. Il sistema non usa né convalida questi valori. In particolare, il *parametro lpOverlapped* non deve puntare a una [**struttura OVERLAPPED.**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)

In Windows 8 e Windows Server 2012 questa funzione è supportata dalle tecnologie seguenti.



| Tecnologia                                           | Supportato      |
|------------------------------------------------------|----------------|
| Server Message Block (SMB) 3.0<br/>   | Sì<br/> |
| Failover trasparente SMB 3.0 (TFO)<br/>        | Sì<br/> |
| SMB 3.0 con condivisioni file con scalabilità orizzontale<br/>   | Sì<br/> |
| Volume condiviso cluster File System (CsvFS)<br/> | Sì<br/> |
| File system resiliente (ReFS)<br/>              | Sì<br/> |



 

CsvFs esegue operazioni di I/O reindirizzate per i file compressi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App \[ UWP per le app desktop \| XP\]<br/>                                                                                                                                                                                                                                                       |
| Server minimo supportato<br/> | Windows App UWP per app desktop server 2003 \[ \|\]<br/>                                                                                                                                                                                                                                              |
| Intestazione<br/>                   | <dl> <dt>IoAPI.h (includere Windows.h);</dt> <dt>WinBase.h in Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                                                  |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CreateIoCompletionPort**](createiocompletionport.md)
</dt> <dt>

[Funzioni di gestione file](file-management-functions.md)
</dt> <dt>

[**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[**Sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)
</dt> </dl>

 

