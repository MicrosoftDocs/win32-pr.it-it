---
description: Recupera il tag corrente delle batteria.
ms.assetid: 0bbe59ba-e037-47ce-a54a-6500ea7c9bc5
title: IOCTL_BATTERY_QUERY_TAG di controllo (Poclass.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_TAG
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: c68c9dc2385803155a6c0f8fd2a5b7c84cedaa8e78c98ae2baca6909104e7315
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143514"
---
# <a name="ioctl_battery_query_tag-control-code"></a>Codice di controllo \_ \_ TAG QUERY IOCTL BATTERY \_

Recupera il tag corrente della batteria.

Per eseguire questa operazione, chiamare la [**funzione DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to battery
  IOCTL_BATTERY_QUERY_TAG,     // dwIoControlCode
  (LPVOID) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of input buffer
  (LPVOID) lpOutBuffer,        // output buffer
  (DWORD) nOutBufferSize,      // size of output buffer
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped);// OVERLAPPED structure
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle della batteria da cui recuperare il tag. Per recuperare un handle di dispositivo, chiamare [**la funzione CreateFile.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Codice di controllo per l'operazione. Questo valore identifica l'operazione specifica da eseguire e il tipo di dispositivo in cui eseguirla. Usare **IOCTL \_ BATTERY QUERY TAG \_ \_ per** questa operazione.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Puntatore a un buffer di input **ULONG.** Il valore indica il numero di millisecondi di attesa in assenza di batteria. Il valore -1 indica che la richiesta attenderà per un periodo illimitato (o fino a quando non verrà annullata da un altro evento).

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Dimensioni del buffer di input, in byte.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Puntatore a un buffer di output **ULONG.** In caso di esito positivo, questo buffer contiene il tag della batteria corrente, che può essere qualsiasi valore ad eccezione di BATTERY \_ TAG \_ INVALID. In caso di errore, se [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce il codice di errore **ERROR FILE NOT \_ \_ \_ FOUND**, questo buffer contiene il **valore BATTERY TAG \_ \_ INVALID**.

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Dimensioni in byte del buffer di output.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Puntatore a una variabile che riceve le dimensioni dei dati archiviati nel buffer *lpOutBuffer,* in byte.

Se il buffer di output è troppo piccolo per restituire dati, la chiamata ha esito negativo, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce il codice di errore **ERROR INSUFFICIENT \_ \_ BUFFER** e il numero di byte restituiti è zero.

Se *lpOverlapped* è **NULL** (I/O non sovrapposto), *lpBytesReturned* non può essere **NULL.**

Se *lpOverlapped* non è **NULL** (I/O sovrapposto), *lpBytesReturned* può essere **NULL.** Se si tratta di un'operazione sovrapposta, è possibile recuperare il numero di byte restituiti chiamando la [**funzione GetOverlappedResult.**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) Se *hDevice è* associato a una porta di completamento I/O, è possibile ottenere il numero di byte restituiti chiamando la [**funzione GetQueuedCompletionStatus.**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

Puntatore a una [**struttura OVERLAPPED.**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)

Se *hDevice è* stato aperto con il flag **FILE FLAG \_ \_ OVERLAPPED,** *lpOverlapped* deve puntare a una struttura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valida. In questo caso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) viene eseguito come operazione sovrapposta (asincrona). Se il dispositivo è stato aperto con il flag **FILE \_ FLAG \_ OVERLAPPED** e *lpOverlapped* è **NULL,** la funzione ha esito negativo in modi imprevedibili.

Se *hDevice* è stato aperto senza specificare il flag **FILE FLAG \_ \_ OVERLAPPED,** *lpOverlapped* viene ignorato e la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) non restituisce alcun valore fino al completamento dell'operazione o fino a quando non si verifica un errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione viene completata correttamente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce un valore diverso da zero.

Se l'operazione non riesce o è in sospeso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce zero. Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Osservazioni

Questa batteria IOCTL recupera il tag corrente della batteria. Il tag della batteria è un valore univoco diverso da zero che cambia quando la batteria fisica viene reinserita, sostituita o sottoposta a modifiche delle caratteristiche. Vedere la sezione Battery Tags (Tag batteria) nell'argomento [Battery Information](battery-information.md) overview (Panoramica delle informazioni sulla batteria) per altri dettagli su quando viene modificato un tag della batteria, su come rilevare la modifica e su come un'applicazione deve procedere dopo la modifica di un tag della batteria. Quando non è presente una batteria, questa richiesta attenderà l'ora indicata e, se non è ancora presente alcuna batteria, restituirà **ERROR \_ FILE NOT \_ \_ FOUND** e imposta il tag battery su **BATTERY TAG \_ \_ INVALID**. Per altre informazioni, vedere Informazioni sulla batteria.

Tutte le richieste di altre informazioni sulla batteria richiedono al chiamante di fornire il tag della batteria corrispondente. Ciò garantisce che il chiamante riceva informazioni per la stessa batteria per ogni richiesta e garantisce che il chiamante sia a conoscenza delle variazioni della batteria senza polling costante.

Per informazioni sulle implicazioni dell'I/O sovrapposto su questa operazione, vedere la sezione Osservazioni [**dell'argomento DeviceIoControl.**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)

## <a name="examples"></a>Esempio

Per un esempio, vedere [Enumerazione dei dispositivi a batteria.](enumerating-battery-devices.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                                                                                                                                                                                         |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                                                                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>Poclass.h;</dt> <dt>BatClass.h in Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni sulla batteria](battery-information.md)
</dt> <dt>

[Codici di controllo del risparmio energia](power-management-control-codes.md)
</dt> <dt>

[**Deviceiocontrol**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**INFORMAZIONI SULLA \_ QUERY DELLA \_ BATTERIA IOCTL \_**](ioctl-battery-query-information.md)
</dt> <dt>

[**STATO QUERY BATTERIA IOCTL \_ \_ \_**](ioctl-battery-query-status.md)
</dt> <dt>

[**INFORMAZIONI SUL \_ SET DI \_ BATTERIA IOCTL \_**](ioctl-battery-set-information.md)
</dt> </dl>

 

