---
description: Il codice di controllo FSCTL SRV REQUEST RESUME KEY viene usato per recuperare un riferimento al file opaco da usare con il codice di controllo \_ \_ \_ \_ \_ IOCTL COPYCHUNK.
ms.assetid: a6e0d253-5beb-4de8-8c40-d004f5794d47
title: FSCTL_SRV_REQUEST_RESUME_KEY codice di controllo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSCTL_SRV_REQUEST_RESUME_KEY
api_type:
- NA
api_location: ''
ms.openlocfilehash: a3654cd78b3e337e07c8267a98a09e0dcabbbb5cb193238e3ca3ebe31c59b12b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161815"
---
# <a name="fsctl_srv_request_resume_key-control-code"></a>Codice di controllo FSCTL \_ SRV \_ REQUEST RESUME \_ \_ KEY

Il **codice di controllo FSCTL \_ SRV REQUEST RESUME \_ \_ \_ KEY** viene usato per recuperare un riferimento al file opaco da usare con il codice di controllo [**\_ IOCTL COPYCHUNK.**](ioctl-copychunk.md)

Per eseguire questa operazione, chiamare la [**funzione DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  FSCTL_SRV_REQUEST_RESUME_KEY, // dwIoControlCode
  NULL,                         // lpInBuffer
  0,                            // nInBufferSize
  (LPVOID) lpOutBuffer,         // output buffer
  (DWORD) nOutBufferSize,       // size of output buffer
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* \[ Pollici\]
</dt> <dd>

Handle per il file per il quale deve essere richiesta la chiave del file di origine. Per ottenere questo handle, chiamare [**la funzione CreateFile.**](/windows/win32/api/fileapi/nf-fileapi-createfilea)

</dd> <dt>

*dwIoControlCode* \[ Pollici\]
</dt> <dd>

Codice di controllo per l'operazione. Usare **FSCTL \_ SRV \_ REQUEST RESUME \_ \_ KEY** per questa operazione.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Non utilizzato con questa operazione. impostato su **NULL.**

</dd> <dt>

*nInBufferSize* \[ Pollici\]
</dt> <dd>

Non utilizzato con questa operazione. impostato su zero.

</dd> <dt>

*lpOutBuffer* \[ Cambio\]
</dt> <dd>

Puntatore al buffer di output, una **struttura SRV \_ REQUEST RESUME \_ \_ KEY.** Per altre informazioni, vedere la sezione Osservazioni.

</dd> <dt>

*nOutBufferSize* \[ Pollici\]
</dt> <dd>

Dimensioni in byte del buffer di output.

</dd> <dt>

*lpBytesReturned* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve le dimensioni dei dati archiviati nel buffer di output, in byte.

Se il buffer di output è troppo piccolo, la chiamata ha esito negativo, la funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce **ERROR INSUFFICIENT \_ \_ BUFFER** e *lpBytesReturned* è zero.

Se il *parametro lpOverlapped* è **NULL,** *lpBytesReturned* non può essere **NULL.** Anche quando un'operazione non restituisce dati di output e il parametro *lpOutBuffer* è **NULL,** [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) usa *lpBytesReturned.* Dopo tale operazione, il valore di *lpBytesReturned* non ha significato.

Se *lpOverlapped* non è **NULL,** *lpBytesReturned* può essere **NULL.** Se *lpOverlapped* non è **NULL** e l'operazione restituisce dati, *lpBytesReturned* non ha significato fino al completamento dell'operazione sovrapposta. Per recuperare il numero di byte restituiti, chiamare [**la funzione GetOverlappedResult.**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) Se il *parametro hDevice* è associato a una porta di completamento I/O, è possibile recuperare il numero di byte restituiti chiamando la [**funzione GetQueuedCompletionStatus.**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

</dd> <dt>

*lpOverlapped* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura OVERLAPPED.**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped)

Se il *parametro hDevice* è stato aperto senza specificare **FILE FLAG \_ \_ OVERLAPPED,** *lpOverlapped* viene ignorato.

Se *hDevice è* stato aperto con il flag **FILE FLAG \_ \_ OVERLAPPED,** l'operazione viene eseguita come operazione sovrapposta (asincrona). In questo caso, *lpOverlapped* deve puntare a una struttura [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) valida che contiene un handle a un oggetto evento. In caso contrario, la funzione ha esito negativo in modi imprevedibili.

Per le operazioni [**sovrapposte, DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce immediatamente un risultato e l'oggetto evento viene segnalato quando l'operazione è stata completata. In caso contrario, la funzione non viene restituita fino al completamento dell'operazione o fino a quando non si verifica un errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione viene completata correttamente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce un valore diverso da zero.

Se l'operazione non riesce o è in sospeso, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce zero. Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Osservazioni

Al codice del controllo non è associato alcun file di intestazione. È necessario definire il codice del controllo e le strutture di dati come indicato di seguito.

``` syntax
#define FSCTL_SRV_REQUEST_RESUME_KEY CTL_CODE(FILE_DEVICE_NETWORK_FILE_SYSTEM, 30, METHOD_BUFFERED, FILE_ANY_ACCESS)

typedef struct _SRV_RESUME_KEY {
    UINT64 ResumeKey;
    UINT64 Timestamp;
    UINT64 Pid;
} SRV_RESUME_KEY, *PSRV_RESUME_KEY;

typedef struct _SRV_REQUEST_RESUME_KEY {
    SRV_RESUME_KEY Key;
    ULONG  ContextLength;
    BYTE   Context[1];
} SRV_REQUEST_RESUME_KEY, *PSRV_REQUEST_RESUME_KEY;
```

Questi membri possono essere descritti come segue.



| Membro                                                                                                                       | Descrizione                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ResumeKey"></span><span id="resumekey"></span><span id="RESUMEKEY"></span>**ResumeKey**<br/>                 | Valore opaco che identifica il file di origine nel server.<br/>                                                                                                   |
| <span id="Timestamp"></span><span id="timestamp"></span><span id="TIMESTAMP"></span>**Timestamp**<br/>                 | Valore opaco che identifica l'ora di apertura del file.<br/>                                                                                               |
| <span id="Pid"></span><span id="pid"></span><span id="PID"></span>**Pid**<br/>                                         | Valore opaco che identifica il processo che ha aperto il file.<br/>                                                                                                |
| <span id="Key"></span><span id="key"></span><span id="KEY"></span>**Chiave**<br/>                                         | Struttura **SRV \_ RESUME \_ KEY.** Per eseguire un'operazione di copia sul lato server, usare questa struttura con il codice di controllo [**\_ IOCTL COPYCHUNK.**](ioctl-copychunk.md)<br/> |
| <span id="ContextLength"></span><span id="contextlength"></span><span id="CONTEXTLENGTH"></span>**ContextLength**<br/> | Questo membro è riservato per l'uso nel sistema. non utilizzare .<br/>                                                                                                              |
| <span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>**Contesto**<br/>                         | Questo membro è riservato per l'uso nel sistema. non utilizzare .<br/>                                                                                                              |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Deviceiocontrol**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**IOCTL \_ COPYCHUNK**](ioctl-copychunk.md)
</dt> </dl>

 

 
