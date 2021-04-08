---
description: Il \_ \_ \_ codice di controllo della chiave Resume della richiesta FSCTL SRV \_ viene usato per recuperare un riferimento a un file opaco da usare con il \_ codice di controllo IOCTL copychunk esegue.
ms.assetid: a6e0d253-5beb-4de8-8c40-d004f5794d47
title: Codice di controllo FSCTL_SRV_REQUEST_RESUME_KEY
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
ms.openlocfilehash: 8f11b70f7b4bfd05cbd5f7c29323f1dca00083a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877305"
---
# <a name="fsctl_srv_request_resume_key-control-code"></a>FSCTL \_ il \_ codice di controllo della chiave di ripresa della richiesta SRV \_ \_

Il codice di controllo della **\_ \_ \_ \_ chiave Resume della richiesta FSCTL SRV** viene usato per recuperare un riferimento a un file opaco da usare con il codice di controllo [**IOCTL \_ copychunk esegue**](ioctl-copychunk.md) .

Per eseguire questa operazione, chiamare la funzione [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.


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

*hDevice* \[ in\]
</dt> <dd>

Handle per il file per il quale deve essere richiesta la chiave del file di origine. Per ottenere questo handle, chiamare la funzione [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* \[ in\]
</dt> <dd>

Codice di controllo per l'operazione. Usare **la \_ \_ chiave di \_ ripresa \_ della richiesta SRV FSCTL** per questa operazione.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Non utilizzato con questa operazione. impostare su **null**.

</dd> <dt>

*nInBufferSize* \[ in\]
</dt> <dd>

Non utilizzato con questa operazione. impostare su zero.

</dd> <dt>

*lpOutBuffer* \[ out\]
</dt> <dd>

Un puntatore al buffer di output, una struttura di **\_ chiavi di \_ ripresa \_ della richiesta SRV** . Per altre informazioni, vedere la sezione Osservazioni.

</dd> <dt>

*nOutBufferSize* \[ in\]
</dt> <dd>

Dimensioni in byte del buffer di output.

</dd> <dt>

*lpBytesReturned* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve le dimensioni in byte dei dati archiviati nel buffer di output.

Se il buffer di output è troppo piccolo, la chiamata ha esito negativo, la funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l' **errore \_ \_ buffer insufficiente** e *lpBytesReturned* è zero.

Se il parametro *lpOverlapped* è **null**, *lpBytesReturned* non può essere **null**. Anche quando un'operazione non restituisce dati di output e il parametro *lpOutBuffer* è **null**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) USA *lpBytesReturned*. Dopo tale operazione, il valore di *lpBytesReturned* non è significativo.

Se *lpOverlapped* non è **null**, *lpBytesReturned* può essere **null**. Se *lpOverlapped* non è **null** e l'operazione restituisce dati, *lpBytesReturned* non ha significato fino al completamento dell'operazione di sovrapposizione. Per recuperare il numero di byte restituiti, chiamare la funzione [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) . Se il parametro *hDevice* è associato a una porta di completamento di i/O, è possibile recuperare il numero di byte restituiti chiamando la funzione [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

</dd> <dt>

*lpOverlapped* \[ in\]
</dt> <dd>

Puntatore a una struttura [**sovrapposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .

Se il parametro *hDevice* è stato aperto senza specificare il **flag di file \_ \_ sovrapposto**, *lpOverlapped* viene ignorato.

Se *hDevice* è stato aperto con il flag **file \_ \_ sovrapposto** , l'operazione viene eseguita come operazione sovrapposta (asincrona). In questo caso, *lpOverlapped* deve puntare a una struttura [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) valida che contiene un handle per un oggetto evento. In caso contrario, la funzione avrà esito negativo in modi imprevedibili.

Per le operazioni sovrapposte, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce immediatamente un risultato e l'oggetto evento viene segnalato al completamento dell'operazione. In caso contrario, la funzione non viene restituita fino a quando l'operazione non viene completata o fino a quando non si verifica un errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione viene completata correttamente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce un valore diverso da zero.

Se l'operazione ha esito negativo o è in sospeso, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce zero. Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Osservazioni

A questo codice di controllo non è associato alcun file di intestazione. È necessario definire il codice di controllo e le strutture di dati come indicato di seguito.

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
| <span id="Timestamp"></span><span id="timestamp"></span><span id="TIMESTAMP"></span>**Timestamp**<br/>                 | Valore opaco che identifica l'ora in cui è stato aperto il file.<br/>                                                                                               |
| <span id="Pid"></span><span id="pid"></span><span id="PID"></span>**PID**<br/>                                         | Valore opaco che identifica il processo che ha aperto il file.<br/>                                                                                                |
| <span id="Key"></span><span id="key"></span><span id="KEY"></span>**Chiave**<br/>                                         | Struttura **di \_ \_ chiavi di ripresa SRV** . Per eseguire un'operazione di copia sul lato server, usare questa struttura con il codice di controllo [**IOCTL \_ copychunk esegue**](ioctl-copychunk.md) .<br/> |
| <span id="ContextLength"></span><span id="contextlength"></span><span id="CONTEXTLENGTH"></span>**ContextLength**<br/> | Questo membro è riservato per l'utilizzo del sistema; Non usare.<br/>                                                                                                              |
| <span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>**Contesto**<br/>                         | Questo membro è riservato per l'utilizzo del sistema; Non usare.<br/>                                                                                                              |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**\_COPYCHUNK esegue IOCTL**](ioctl-copychunk.md)
</dt> </dl>

 

 
