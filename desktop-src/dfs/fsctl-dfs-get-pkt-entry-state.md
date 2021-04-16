---
title: Codice di controllo FSCTL_DFS_GET_PKT_ENTRY_STATE (LmDfs.h)
description: Il codice di controllo FSCTL_DFS_GET_PKT_ENTRY_STATE può ottenere le stesse informazioni della funzione NetDfsGetClientInfo, ma può fornire prestazioni migliori in alcune configurazioni con latenze elevate per i server DFS.
ms.assetid: d4eec104-128b-43b5-9fae-08ab0b977dec
topic_type:
- apiref
api_name:
- FSCTL_DFS_GET_PKT_ENTRY_STATE
api_location:
- LmDfs.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a57fb448934908ebc1530e95a298715324aaee6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524033"
---
# <a name="fsctl_dfs_get_pkt_entry_state-control-code"></a>Codice di controllo FSCTL_DFS_GET_PKT_ENTRY_STATE

Il codice di controllo **FSCTL_DFS_GET_PKT_ENTRY_STATE** può ottenere le stesse informazioni della funzione [**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) , ma può fornire prestazioni migliori in alcune configurazioni con latenze elevate per i server DFS. Non è consigliabile usare il codice di controllo **FSCTL_DFS_GET_PKT_ENTRY_STATE** , a meno che non si verifichino problemi di prestazioni.

Per eseguire questa operazione, chiamare la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.

```C++
BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,            // handle to device
                    (DWORD)        FSCTL_DFS_GET_PKT_ENTRY_STATE, // dwIoControlCode(LPDWORD)      lpInBuffer,         // input buffer
                    (DWORD)        nInBufferSize,      // size of input buffer
                    (LPDWORD)      lpOutBuffer,        // output buffer
                    (DWORD)        nOutBufferSize,     // size of output buffer
                    (LPDWORD)      lpBytesReturned,    // number of bytes returned
                    (LPOVERLAPPED) lpOverlapped );     // OVERLAPPED structure
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* [in]
</dt> <dd>

Handle per il dispositivo. Per ottenere un handle di dispositivo, chiamare la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* [in]
</dt> <dd>

Codice di controllo per l'operazione. Usare **FSCTL_DFS_GET_PKT_ENTRY_STATE** per questa operazione.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Indirizzo di una struttura [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) e delle stringhe Unicode 1-3 che seguono.

</dd> <dt>

*nInBufferSize* [in]
</dt> <dd>

Dimensione, in byte, del buffer a cui punta il parametro *lpInBuffer* .

</dd> <dt>

*lpOutBuffer* [out]
</dt> <dd>

Indirizzo di una struttura di **DFS_INFO_ \#** e di eventuali stringhe e strutture a cui punta la struttura di **DFS_INFO_ \#** . La struttura specifica restituita dipende dal membro del **livello** nella struttura [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) passata nel buffer di input.

</dd> <dt>

*nOutBufferSize* [in]
</dt> <dd>

Dimensione, in byte, del buffer a cui punta il parametro *lpOutBuffer* . A causa delle stringhe e delle strutture a cui fa riferimento la struttura di **DFS_INFO_ \#** restituita anch ' essa nel buffer di output, il buffer deve essere maggiore della struttura **DFS_INFO_ \#** specificata.

</dd> <dt>

*lpBytesReturned* [out]
</dt> <dd>

Puntatore a una variabile che riceve le dimensioni in byte dei dati archiviati nel buffer di output.

Se il buffer di output è troppo piccolo, ma almeno sufficientemente grande da contenere un **valore DWORD**, la chiamata ha esito negativo, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce **ERROR_MORE_DATA** e il primo **valore DWORD** del buffer di output contiene le dimensioni necessarie. Se il buffer di output non può mantenere un **valore DWORD** , la chiamata ha esito negativo con **ERROR_INSUFFICIENT_BUFFER** e *lpBytesReturned* è zero.

Se *lpOverlapped* è **null**, *lpBytesReturned* non può essere **null**. Anche quando un'operazione non restituisce dati di output e *lpOutBuffer* è **null**, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) USA *lpBytesReturned*. Dopo tale operazione, il valore di *lpBytesReturned* non è significativo.

Se *lpOverlapped* non è **null**, *lpBytesReturned* può essere **null**. Se questo parametro non è **null** e l'operazione restituisce dati, *lpBytesReturned* non ha significato fino al completamento dell'operazione di sovrapposizione. Per recuperare il numero di byte restituiti, chiamare [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult). Se il parametro *hDevice* è associato a una porta di completamento di I/O, è possibile recuperare il numero di byte restituiti chiamando [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).

</dd> <dt>

*lpOverlapped* [in]
</dt> <dd>

Puntatore a una struttura [**sovrapposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .

Se *hDevice* è stato aperto senza specificare **FILE_FLAG_OVERLAPPED**, *lpOverlapped* viene ignorato.

Se *hDevice* è stato aperto con il FLAG di **FILE_FLAG_OVERLAPPED** , l'operazione viene eseguita come operazione sovrapposta (asincrona). In questo caso, *lpOverlapped* deve puntare a una struttura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valida che contiene un handle per un oggetto evento. In caso contrario, la funzione avrà esito negativo in modi imprevedibili.

Per le operazioni sovrapposte, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce immediatamente un risultato e l'oggetto evento viene segnalato al completamento dell'operazione. In caso contrario, la funzione non restituisce alcun risultato fino a quando l'operazione non viene completata o si verifica un errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione viene completata correttamente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce un valore diverso da zero.

Se l'operazione ha esito negativo o è in sospeso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce zero. Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                             |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                       |
| Intestazione<br/>                   | <dl> <dt>LmDfs. h (include LmDfs. h)</dt> </dl> |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo)
</dt> </dl>
