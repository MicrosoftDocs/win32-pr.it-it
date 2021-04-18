---
description: Il \_ codice di controllo IOCTL copychunk esegue avvia una copia sul lato server di un intervallo di dati, detto anche blocco.
ms.assetid: 36f68840-bd5c-4cfc-a8ad-0cfbbdc5a2a9
title: Codice di controllo IOCTL_COPYCHUNK
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
ms.openlocfilehash: c425fc53563e6dfc16d2040fb575f47f0f8fdf35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304409"
---
# <a name="ioctl_copychunk-control-code"></a>\_Codice di controllo IOCTL copychunk esegue

Il codice di controllo **IOCTL \_ copychunk esegue** avvia una copia sul lato server di un intervallo di dati, detto anche blocco.

Per eseguire questa operazione, chiamare la funzione [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.


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

*hDevice* \[ in\]
</dt> <dd>

Handle per il file che è la destinazione dell'operazione di copia sul lato server. Per ottenere questo handle, chiamare la funzione [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* \[ in\]
</dt> <dd>

Codice di controllo per l'operazione. Utilizzare **IOCTL \_ copychunk esegue** per questa operazione.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Puntatore al buffer di input, una struttura **di \_ \_ copia SRV copychunk esegue** . Per altre informazioni, vedere la sezione Osservazioni.

</dd> <dt>

*nInBufferSize* \[ in\]
</dt> <dd>

Dimensioni in byte del buffer di input.

</dd> <dt>

*lpOutBuffer* \[ out\]
</dt> <dd>

Puntatore al buffer di output, una struttura **di \_ \_ risposta SRV copychunk esegue** . Per altre informazioni, vedere la sezione Osservazioni.

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
| <span id="DestinationOffset"></span><span id="destinationoffset"></span><span id="DESTINATIONOFFSET"></span>**DestinationOffset**<br/> | Offset, in byte, dall'inizio del file di destinazione fino alla posizione in cui deve essere copiato il blocco.<br/>                                                                                                                                                                                                                                               |
| <span id="Length"></span><span id="length"></span><span id="LENGTH"></span>**Lunghezza**<br/>                                             | Numero di byte di dati nel blocco da copiare. Deve essere maggiore di zero e minore o uguale a 1 MB. **Lunghezza** \* **ChunkCount** deve essere minore o uguale a 16 MB.<br/>                                                                                                                                                                         |
| <span id="SourceFile"></span><span id="sourcefile"></span><span id="SOURCEFILE"></span>**SourceFile**<br/>                             | Chiave che rappresenta il file di origine con i dati da copiare. Questa chiave viene ottenuta tramite la [**\_ chiave di \_ \_ ripresa \_ della richiesta SRV FSCTL**](fsctl-srv-request-resume-key.md).<br/>                                                                                                                                                                                   |
| <span id="ChunkCount"></span><span id="chunkcount"></span><span id="CHUNKCOUNT"></span>**ChunkCount**<br/>                             | Numero di blocchi da copiare. Deve essere maggiore di zero e minore o uguale a 256.<br/>                                                                                                                                                                                                                                                                |
| <span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Riservati**<br/>                                     | Questo membro è riservato per l'utilizzo del sistema; Non usare.<br/>                                                                                                                                                                                                                                                                                                        |
| <span id="Chunk"></span><span id="chunk"></span><span id="CHUNK"></span>**Pezzo**<br/>                                                 | Matrice di strutture **ChunkCount** **SRV \_ copychunk esegue** , una per ogni blocco da copiare. La lunghezza, in byte, di questa matrice deve essere **ChunkCount** \* sizeof (**SRV \_ copychunk esegue**).<br/>                                                                                                                                                                       |
| <span id="ChunksWritten"></span><span id="chunkswritten"></span><span id="CHUNKSWRITTEN"></span>**ChunksWritten**<br/>                 | Se l'operazione non è riuscita con un **parametro di errore \_ non valido \_**, questo valore indica il numero massimo di blocchi accettati dal server in una singola richiesta, ovvero 256. In caso contrario, questo valore indica il numero di blocchi scritti correttamente.<br/>                                                                                               |
| <span id="ChunkBytesWritten"></span><span id="chunkbyteswritten"></span><span id="CHUNKBYTESWRITTEN"></span>**ChunkBytesWritten**<br/> | Se l'operazione non è riuscita con un **parametro di errore \_ non valido \_**, questo valore indica il numero massimo di byte che il server consentirà di scrivere in un singolo blocco, ovvero 1 MB. In caso contrario, questo valore indica il numero di byte scritti correttamente nell'ultimo blocco non elaborato correttamente (se si è verificata una scrittura parziale).<br/> |
| <span id="TotalBytesWritten"></span><span id="totalbyteswritten"></span><span id="TOTALBYTESWRITTEN"></span>**TotalBytesWritten**<br/> | Se l'operazione non è riuscita con un **parametro di errore \_ non valido \_**, questo valore indica il numero massimo di byte copiati dal server in una singola richiesta, ovvero 16 MB. In caso contrario, questo valore indica il numero di byte scritti correttamente.<br/>                                                                                                 |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**FSCTL \_ la \_ \_ chiave di ripresa della richiesta SRV \_**](fsctl-srv-request-resume-key.md)
</dt> </dl>

 

 
