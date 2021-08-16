---
description: Il codice di controllo \_ IOCTL LMR DISABLE LOCAL BUFFERING disabilita la memorizzazione nella cache locale in memoria sul lato client dei dati durante la lettura o la scrittura di dati \_ in un file \_ \_ remoto. Si tratta di un codice di controllo definito internamente non disponibile in un'intestazione pubblica.
ms.assetid: a464671b-253c-4f35-84a2-2619cb15b009
title: IOCTL_LMR_DISABLE_LOCAL_BUFFERING di controllo
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
ms.openlocfilehash: 88a6fff0955fb9e0c57c7ea5fae99f532c7c6d4dcc3578a75e07da3f35867f9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827197"
---
# <a name="ioctl_lmr_disable_local_buffering-control-code"></a>Codice di controllo IOCTL \_ LMR \_ DISABLE \_ LOCAL \_ BUFFERING

Il codice di controllo **\_ IOCTL LMR \_ DISABLE LOCAL \_ \_ BUFFERING** disabilita la memorizzazione nella cache locale in memoria sul lato client dei dati durante la lettura o la scrittura di dati in un file remoto. Si tratta di un codice di controllo definito internamente non disponibile in un'intestazione pubblica.

Per eseguire questa operazione, chiamare la [**funzione DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_LMR_DISABLE_LOCAL_BUFFERING, // dwIoControlCode
  (LPVOID) NULL,                // lpInBuffer
  (DWORD) 0,                    // nInBufferSize
  (LPVOID) NULL,                // lpOutBuffer
  (DWORD) 0,                    // nOutBufferSize
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* \[ Pollici\]
</dt> <dd>

Handle per il file remoto. Per ottenere questo handle, chiamare [**la funzione CreateFile.**](/windows/win32/api/fileapi/nf-fileapi-createfilea)

</dd> <dt>

*dwIoControlCode* \[ Pollici\]
</dt> <dd>

Codice di controllo per l'operazione. Usare il valore 0x140390 per questa operazione.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Non usato, deve essere **NULL.**

</dd> <dt>

*nInBufferSize* \[ Pollici\]
</dt> <dd>

Dimensioni del buffer di input, in byte. Deve essere zero.

</dd> <dt>

*lpOutBuffer* \[ Cambio\]
</dt> <dd>

Non usato, deve essere **NULL.**

</dd> <dt>

*nOutBufferSize* \[ Pollici\]
</dt> <dd>

Dimensioni in byte del buffer di output. Deve essere zero.

</dd> <dt>

*lpBytesReturned* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve le dimensioni dei dati archiviati nel buffer di output, in byte.

Se il buffer di output è troppo piccolo, la chiamata ha esito negativo, la [**funzione GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce **ERROR INSUFFICIENT \_ \_ BUFFER** e *lpBytesReturned* è zero.

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

Il codice di controllo **IOCTL \_ LMR \_ DISABLE LOCAL \_ \_ BUFFERING** viene definito internamente dal sistema come 0x140390 e non in un file di intestazione pubblico. Viene usato dalle applicazioni per scopi speciali per disabilitare la memorizzazione dei dati nella cache in memoria sul lato client locale durante la lettura o la scrittura di dati in un file remoto. Dopo la disabilitazione del buffer locale, l'impostazione rimane attiva fino a quando tutti gli handle aperti per il file non vengono chiusi e il redirector pulisce le strutture di dati interne.

Le applicazioni per utilizzo generico non devono usare **IOCTL \_ LMR \_ DISABLE LOCAL \_ \_ BUFFERING,** perché possono comportare un traffico di rete eccessivo e una perdita di prestazioni associata. Il codice di controllo **\_ IOCTL LMR \_ DISABLE LOCAL \_ \_ BUFFERING** deve essere usato solo in applicazioni specializzate che spostano grandi quantità di dati in rete durante il tentativo di ottimizzare l'uso della larghezza di banda di rete. Ad esempio, le funzioni [**CopyFile**](/windows/win32/api/winbase/nf-winbase-copyfile) e [**CopyFileEx**](/windows/win32/api/winbase/nf-winbase-copyfileexa) usano **IOCTL \_ LMR \_ DISABLE LOCAL \_ \_ BUFFERING** per migliorare le prestazioni di copia di file di grandi dimensioni.

**IOCTL \_ LMR \_ DISABLE \_ LOCAL \_ BUFFERING non** è implementato dai file system locali e avrà esito negativo con errore INVALID **\_ \_ FUNCTION**. L'emissione del codice di controllo **IOCTL \_ LMR \_ DISABLE LOCAL \_ \_ BUFFERING** sugli handle di directory remota avrà esito negativo con l'errore **ERROR NOT \_ \_ SUPPORTED**.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Deviceiocontrol**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

 
