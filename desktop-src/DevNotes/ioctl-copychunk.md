---
description: Il codice di controllo IOCTL COPYCHUNK avvia una copia sul lato server di un intervallo di \_ dati, detto anche blocco.
ms.assetid: 36f68840-bd5c-4cfc-a8ad-0cfbbdc5a2a9
title: IOCTL_COPYCHUNK di controllo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COPY_CHUNK
api_type:
- NA
api_location: ''
ms.openlocfilehash: 415e94d8ed19d3248beb31d8a5e6327e1adc11078483d4f60fcd42699e4dab89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001731"
---
# <a name="ioctl_copychunk-control-code"></a>Codice di controllo \_ IOCTL COPYCHUNK

Il **codice di controllo IOCTL \_ COPYCHUNK** avvia una copia sul lato server di un intervallo di dati, detto anche blocco.

Per eseguire questa operazione, chiamare la [**funzione DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_COPYCHUNK,              // dwIoControlCode
  (LPVOID) lpInBuffer,          // input buffer
  (DWORD) nInBufferSize,        // size of input buffer
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

Handle per il file che rappresenta la destinazione dell'operazione di copia sul lato server. Per ottenere questo handle, chiamare la [**funzione CreateFile.**](/windows/win32/api/fileapi/nf-fileapi-createfilea)

</dd> <dt>

*dwIoControlCode* \[ Pollici\]
</dt> <dd>

Codice di controllo per l'operazione. Usare **IOCTL \_ COPYCHUNK** per questa operazione.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Puntatore al buffer di input, struttura **\_ COPYCHUNK \_ SRV.** Per altre informazioni, vedere la sezione Osservazioni.

</dd> <dt>

*nInBufferSize* \[ Pollici\]
</dt> <dd>

Dimensioni del buffer di input, in byte.

</dd> <dt>

*lpOutBuffer* \[ Cambio\]
</dt> <dd>

Puntatore al buffer di output, una **struttura \_ SRV COPYCHUNK \_ RESPONSE.** Per altre informazioni, vedere la sezione Osservazioni.

</dd> <dt>

*nOutBufferSize* \[ Pollici\]
</dt> <dd>

Dimensioni in byte del buffer di output.

</dd> <dt>

*lpBytesReturned* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve le dimensioni dei dati archiviati nel buffer di output, in byte.

Se il buffer di output è troppo piccolo, la chiamata ha esito negativo, la [**funzione GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce **ERROR INSUFFICIENT \_ \_ BUFFER** e *lpBytesReturned* è zero.

Se il *parametro lpOverlapped* **è NULL,** *lpBytesReturned* non può essere **NULL.** Anche quando un'operazione non restituisce dati di output e *il parametro lpOutBuffer* è **NULL,** [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) usa *lpBytesReturned*. Dopo tale operazione, il valore di *lpBytesReturned* non ha alcun significato.

Se *lpOverlapped* non è **NULL,** *lpBytesReturned* può essere **NULL.** Se *lpOverlapped* non è **NULL** e l'operazione restituisce dati, *lpBytesReturned* non ha significato fino al completamento dell'operazione sovrapposta. Per recuperare il numero di byte restituiti, chiamare la [**funzione GetOverlappedResult.**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) Se il *parametro hDevice* è associato a una porta di completamento I/O, è possibile recuperare il numero di byte restituiti chiamando la [**funzione GetQueuedCompletionStatus.**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

</dd> <dt>

*lpOverlapped* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura OVERLAPPED.**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped)

Se il *parametro hDevice* è stato aperto senza specificare **FILE FLAG \_ \_ OVERLAPPED,** *lpOverlapped* viene ignorato.

Se *hDevice è* stato aperto con il flag **FILE FLAG \_ \_ OVERLAPPED,** l'operazione viene eseguita come operazione sovrapposta (asincrona). In questo caso, *lpOverlapped* deve puntare a una struttura [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) valida che contiene un handle per un oggetto evento. In caso contrario, la funzione ha esito negativo in modo imprevedibile.

Per le operazioni sovrapposte, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce immediatamente e l'oggetto evento viene segnalato al termine dell'operazione. In caso contrario, la funzione non restituisce fino al completamento dell'operazione o fino a quando non si verifica un errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione viene completata correttamente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce un valore diverso da zero.

Se l'operazione ha esito negativo o è in sospeso, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce zero. Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Osservazioni

A questo codice di controllo non è associato alcun file di intestazione. È necessario definire il codice del controllo e le strutture di dati come indicato di seguito.

``` syntax
#define IOCTL_COPYCHUNK CTL_CODE(FILE_DEVICE_NETWORK_FILE_SYSTEM, 262, METHOD_BUFFERED,  FILE_READ_ACCESS)

typedef struct _SRV_COPYCHUNK {
    LARGE_INTEGER SourceOffset;
    LARGE_INTEGER DestinationOffset;
    ULONG  Length;
} SRV_COPYCHUNK, *PSRV_COPYCHUNK;

typedef struct _SRV_COPYCHUNK_COPY {
    SRV_RESUME_KEY SourceFile;
    ULONG          ChunkCount;
    ULONG          Reserved;
    SRV_COPYCHUNK  Chunk[1];    // Array
} SRV_COPYCHUNK_COPY, *PSRV_COPYCHUNK_COPY;

typedef struct _SRV_COPYCHUNK_RESPONSE {
    ULONG          ChunksWritten;
    ULONG          ChunkBytesWritten;
    ULONG          TotalBytesWritten;
} SRV_COPYCHUNK_RESPONSE, *PSRV_COPYCHUNK_RESPONSE;
```

Questi membri possono essere descritti come segue.



| Membro                                                                                                                                       | Descrizione                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SourceOffset"></span><span id="sourceoffset"></span><span id="SOURCEOFFSET"></span>**SourceOffset**<br/>                     | Offset, in byte, dall'inizio del file di origine al blocco da copiare.<br/>                                                                                                                                                                                                                                                                     |
| <span id="DestinationOffset"></span><span id="destinationoffset"></span><span id="DESTINATIONOFFSET"></span>**DestinationOffset**<br/> | Offset, in byte, dall'inizio del file di destinazione al percorso in cui deve essere copiato il blocco.<br/>                                                                                                                                                                                                                                               |
| <span id="Length"></span><span id="length"></span><span id="LENGTH"></span>**Lunghezza**<br/>                                             | Numero di byte di dati nel blocco da copiare. Deve essere maggiore di zero e minore o uguale a 1 MB. **Lunghezza** \* **ChunkCount** deve essere minore o uguale a 16 MB.<br/>                                                                                                                                                                         |
| <span id="SourceFile"></span><span id="sourcefile"></span><span id="SOURCEFILE"></span>**SourceFile**<br/>                             | Chiave che rappresenta il file di origine con i dati da copiare. Questa chiave viene ottenuta tramite [**FSCTL \_ SRV \_ REQUEST RESUME \_ \_ KEY**](fsctl-srv-request-resume-key.md).<br/>                                                                                                                                                                                   |
| <span id="ChunkCount"></span><span id="chunkcount"></span><span id="CHUNKCOUNT"></span>**ChunkCount**<br/>                             | Numero di blocchi da copiare. Deve essere maggiore di zero e minore o uguale a 256.<br/>                                                                                                                                                                                                                                                                |
| <span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Riservati**<br/>                                     | Questo membro è riservato per l'uso del sistema. non utilizzare .<br/>                                                                                                                                                                                                                                                                                                        |
| <span id="Chunk"></span><span id="chunk"></span><span id="CHUNK"></span>**Pezzo**<br/>                                                 | Matrice di **strutture ChunkCount** **SRV \_ COPYCHUNK,** una per ogni blocco da copiare. La lunghezza, in byte, di questa matrice deve essere **ChunkCount** \* sizeof(**SRV \_ COPYCHUNK**).<br/>                                                                                                                                                                       |
| <span id="ChunksWritten"></span><span id="chunkswritten"></span><span id="CHUNKSWRITTEN"></span>**ChunksWritten**<br/>                 | Se l'operazione non è riuscita con **ERROR \_ INVALID \_ PARAMETER**, questo valore indica il numero massimo di blocchi che il server accetterà in una singola richiesta, ovvero 256. In caso contrario, questo valore indica il numero di blocchi scritti correttamente.<br/>                                                                                               |
| <span id="ChunkBytesWritten"></span><span id="chunkbyteswritten"></span><span id="CHUNKBYTESWRITTEN"></span>**ChunkBytesWritten**<br/> | Se l'operazione non è riuscita con **ERROR \_ INVALID \_ PARAMETER,** questo valore indica il numero massimo di byte che il server consentirà di scrivere in un singolo blocco, ovvero 1 MB. In caso contrario, questo valore indica il numero di byte scritti correttamente nell'ultimo blocco che non è stato elaborato correttamente (se si è verificata una scrittura parziale).<br/> |
| <span id="TotalBytesWritten"></span><span id="totalbyteswritten"></span><span id="TOTALBYTESWRITTEN"></span>**TotalBytesWritten**<br/> | Se l'operazione non è riuscita con **ERROR \_ INVALID \_ PARAMETER**, questo valore indica il numero massimo di byte che il server copierà in una singola richiesta, ovvero 16 MB. In caso contrario, questo valore indica il numero di byte scritti correttamente.<br/>                                                                                                 |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Deviceiocontrol**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**CHIAVE DI RIPRESA DELLA \_ RICHIESTA FSCTL SRV \_ \_ \_**](fsctl-srv-request-resume-key.md)
</dt> </dl>

 

 
