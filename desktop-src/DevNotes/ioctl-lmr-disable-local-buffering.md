---
description: Il \_ LMR IOCTL \_ Disabilita \_ il \_ codice di controllo del buffer locale Disabilita la memorizzazione nella cache locale dei dati in memoria durante la lettura o la scrittura di dati in un file remoto. Si tratta di un codice di controllo definito internamente non disponibile in un'intestazione pubblica.
ms.assetid: a464671b-253c-4f35-84a2-2619cb15b009
title: Codice di controllo IOCTL_LMR_DISABLE_LOCAL_BUFFERING
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
ms.openlocfilehash: 0d596402c489caee972e1305f2a32881312fd3e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304408"
---
# <a name="ioctl_lmr_disable_local_buffering-control-code"></a>IOCTL \_ LMR \_ disabilitare \_ il \_ codice di controllo del buffer locale

Il LMR IOCTL Disabilita il codice di controllo del **\_ \_ \_ \_ buffer locale Disabilita** la memorizzazione nella cache locale dei dati in memoria durante la lettura o la scrittura di dati in un file remoto. Si tratta di un codice di controllo definito internamente non disponibile in un'intestazione pubblica.

Per eseguire questa operazione, chiamare la funzione [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.


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

*hDevice* \[ in\]
</dt> <dd>

Handle per il file remoto. Per ottenere questo handle, chiamare la funzione [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* \[ in\]
</dt> <dd>

Codice di controllo per l'operazione. Usare il valore 0x140390 per questa operazione.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Non utilizzato, deve essere **null**.

</dd> <dt>

*nInBufferSize* \[ in\]
</dt> <dd>

Dimensioni in byte del buffer di input. Deve essere zero.

</dd> <dt>

*lpOutBuffer* \[ out\]
</dt> <dd>

Non utilizzato, deve essere **null**.

</dd> <dt>

*nOutBufferSize* \[ in\]
</dt> <dd>

Dimensioni in byte del buffer di output. Deve essere zero.

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

Il LMR IOCTL Disabilita il codice di controllo del **\_ \_ \_ \_ buffer locale** viene definito internamente dal sistema come 0x140390 e non in un file di intestazione pubblico. Viene usato da applicazioni per scopi specifici per disabilitare la memorizzazione nella cache locale dei dati in memoria sul lato client durante la lettura o la scrittura di dati in un file remoto. Quando il buffering locale è disabilitato, l'impostazione rimane attiva fino a quando tutti gli handle aperti del file non vengono chiusi e il redirector pulisce le relative strutture di dati interne.

Le applicazioni generiche non devono utilizzare **IOCTL \_ LMR \_ disabilitare \_ il \_ buffering locale**, perché può comportare un eccessivo traffico di rete e una perdita di prestazioni associata. Il LMR IOCTL disabilitare il codice di controllo del **\_ \_ \_ \_ buffer locale** deve essere usato solo in applicazioni specializzate che trasferiscono grandi quantità di dati in rete, tentando di ottimizzare l'uso della larghezza di banda di rete. Le funzioni [**CopyFile**](/windows/win32/api/winbase/nf-winbase-copyfile) e [**CopyFileEx**](/windows/win32/api/winbase/nf-winbase-copyfileexa) , ad esempio, utilizzano **IOCTL \_ LMR disabilitare il \_ \_ \_ buffering locale** per migliorare le prestazioni di copia dei file di grandi dimensioni.

**IOCTL \_ LMR \_ Disabilita \_ la \_ memorizzazione nel buffer locale** non è implementata dai file system locali e avrà esito negativo e verrà restituita una funzione di errore **\_ non valida \_**. Il rilascio del LMR IOCTL Disabilita il codice di controllo del **\_ \_ \_ \_ buffer locale** negli handle di directory remota avrà esito negativo e l'errore di errore **non è \_ \_ supportato**.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

 
