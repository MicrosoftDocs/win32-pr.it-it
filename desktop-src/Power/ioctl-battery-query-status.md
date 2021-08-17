---
description: Recupera lo stato corrente della batteria.
ms.assetid: 7a7bf429-9b2c-4faf-9f27-fb5fd8dd18df
title: IOCTL_BATTERY_QUERY_STATUS codice di controllo (Poclass.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: 29d8b33238fa8daa463c007fa9d65cba9c6fb72ef13f0f68587a1452f3dabb0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143536"
---
# <a name="ioctl_battery_query_status-control-code"></a>Codice di controllo STATO \_ \_ QUERY IOCTL BATTERY \_

Recupera lo stato corrente della batteria.

Per eseguire questa operazione, chiamare la [**funzione DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,           // handle to battery
  IOCTL_BATTERY_QUERY_STATUS, // dwIoControlCode
  (LPVOID) lpInBuffer,        // input buffer
  (DWORD) nInBufferSize,      // size of input buffer
  (LPVOID) lpOutBuffer,       // output buffer
  (DWORD) nOutBufferSize,     // size of output buffer
  (LPDWORD) lpBytesReturned,  // number of bytes returned
  (LPOVERLAPPED) lpOverlapped // OVERLAPPED structure
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle della batteria da cui devono essere restituite le informazioni. Per recuperare un handle di dispositivo, chiamare la [**funzione CreateFile.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Codice di controllo per l'operazione. Questo valore identifica l'operazione specifica da eseguire e il tipo di dispositivo in cui eseguirla. Usare **IOCTL \_ BATTERY QUERY STATUS \_ \_ per** questa operazione.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Puntatore a una [**struttura BATTERY \_ WAIT \_ STATUS.**](battery-wait-status-str.md)

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Dimensioni del buffer di input, in byte.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Puntatore a una [**struttura BATTERY \_ STATUS.**](battery-status-str.md)

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Dimensioni in byte del buffer di output.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Puntatore a una variabile che riceve le dimensioni dei dati restituiti nel buffer *lpOutBuffer,* in byte.

Se il buffer di output è troppo piccolo per restituire dati, la chiamata ha esito negativo, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce il codice di errore **ERROR INSUFFICIENT \_ \_ BUFFER** e il numero di byte restituiti è zero.

Se *lpOverlapped* è **NULL** (I/O non sovrapposto), *lpBytesReturned* non può essere **NULL.**

Se *lpOverlapped* non è **NULL** (I/O sovrapposto), *lpBytesReturned* può essere **NULL.** Se si tratta di un'operazione sovrapposta, è possibile recuperare il numero di byte restituiti chiamando la [**funzione GetOverlappedResult.**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) Se *hDevice è* associato a una porta di completamento I/O, è possibile ottenere il numero di byte restituiti chiamando la [**funzione GetQueuedCompletionStatus.**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

Puntatore a una [**struttura OVERLAPPED.**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)

Se *hDevice è* stato aperto con il flag **FILE FLAG \_ \_ OVERLAPPED,** *lpOverlapped* deve puntare a una struttura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valida. In questo caso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) viene eseguito come operazione sovrapposta (asincrona). Se il dispositivo è stato aperto con il flag **FILE \_ FLAG \_ OVERLAPPED** e *lpOverlapped* è **NULL,** la funzione ha esito negativo in modi imprevedibili.

Se *hDevice* è stato aperto senza specificare il flag **FILE FLAG \_ \_ OVERLAPPED,** *lpOverlapped* viene ignorato e la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) non viene restituita fino al completamento dell'operazione o fino a quando non si verifica un errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione viene completata correttamente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce un valore diverso da zero.

Se l'operazione ha esito negativo o è in sospeso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce zero. Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Osservazioni

Questa batteria IOCTL recupera lo stato della batteria al momento del ritorno dell'operazione. La struttura del parametro di input [**BATTERY \_ WAIT \_ STATUS**](battery-wait-status-str.md)indica quando lo stato della batteria deve essere elaborato e restituito.

Le richieste di stato della batteria possono essere restituite immediatamente o possono essere impostate in modo da attendere una determinata condizione prima del completamento. Ad esempio, è possibile eseguire una richiesta di informazioni sulla batteria che attende che la capacità della batteria raggiunga un punto specificato o che lo stato della batteria cambi.

Tutte le richieste di informazioni sulla batteria verranno completate con lo stato **\_ ERROR FILE NOT \_ \_ FOUND** ogni volta che l'elemento **BatteryTag** della richiesta non corrisponde a quello del tag della batteria corrente. Per altre [informazioni, vedere Tag](battery-information.md) della batteria. Viene usato per garantire che le informazioni sulla batteria restituite corrispondano a quella della batteria richiesta.

Per informazioni sulle implicazioni dell'I/O sovrapposto su questa operazione, vedere la sezione Osservazioni [**dell'argomento DeviceIoControl.**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)

## <a name="examples"></a>Esempio

Per un esempio, vedere [Enumerazione dei dispositivi a batteria](enumerating-battery-devices.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                                                                                                                                                                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                                                                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>Poclass.h;</dt> <dt>BatClass.h in Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni sulla batteria](battery-information.md)
</dt> <dt>

[Codici di controllo per il risparmio energia](power-management-control-codes.md)
</dt> <dt>

[**Deviceiocontrol**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**STATO \_ DELLA BATTERIA**](battery-status-str.md)
</dt> <dt>

[**STATO \_ DI ATTESA DELLA \_ BATTERIA**](battery-wait-status-str.md)
</dt> <dt>

[**INFORMAZIONI SULLE \_ QUERY SULLA \_ BATTERIA IOCTL \_**](ioctl-battery-query-information.md)
</dt> <dt>

[**TAG DI QUERY DELLA BATTERIA IOCTL \_ \_ \_**](ioctl-battery-query-tag.md)
</dt> <dt>

[**INFORMAZIONI SUL \_ SET DI \_ BATTERIA IOCTL \_**](ioctl-battery-set-information.md)
</dt> </dl>

 

