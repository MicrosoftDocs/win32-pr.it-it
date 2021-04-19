---
description: Recupera il tag corrente delle batterie.
ms.assetid: 0bbe59ba-e037-47ce-a54a-6500ea7c9bc5
title: Codice di controllo IOCTL_BATTERY_QUERY_TAG (Poclass. h)
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
ms.openlocfilehash: 1d8435e62c4f061ac13b3e18e5bcd64afcb399c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312047"
---
# <a name="ioctl_battery_query_tag-control-code"></a>\_Codice di \_ \_ controllo tag di query della batteria IOCTL

Recupera il tag corrente della batteria.

Per eseguire questa operazione, chiamare la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.


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

Handle per la batteria da cui deve essere recuperato il tag. Per recuperare un handle di dispositivo, chiamare la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Codice di controllo per l'operazione. Questo valore identifica l'operazione specifica da eseguire e il tipo di dispositivo su cui eseguirla. Usare **il \_ \_ \_ tag di query della batteria IOCTL** per questa operazione.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Puntatore a un buffer di input **ULONG** . Il valore indica il numero di millisecondi di attesa in assenza di batteria. Il valore-1 indica che la richiesta attenderà per un tempo illimitato (o fino a quando non viene annullata da un altro evento).

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Dimensioni in byte del buffer di input.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Puntatore a un buffer di output **ULONG** . In caso di esito positivo, questo buffer contiene il tag corrente della batteria, che può essere qualsiasi valore eccetto \_ tag batteria \_ non valido. In caso di esito negativo, se [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce il file di errore del codice di errore **\_ \_ non \_ trovato**, questo buffer contiene il valore **tag della batteria non \_ \_ valido**.

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Dimensioni in byte del buffer di output.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Puntatore a una variabile che riceve la dimensione dei dati archiviati nel buffer *lpOutBuffer* , in byte.

Se il buffer di output è troppo piccolo per restituire i dati, la chiamata ha esito negativo, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce il **\_ \_ buffer insufficiente** nell'errore del codice di errore e il numero di byte restituito è zero.

Se *lpOverlapped* è **null** (I/O non sovrapposti), *lpBytesReturned* non può essere **null**.

Se *lpOverlapped* non è **null** (I/O sovrapposto), *lpBytesReturned* può essere **null**. Se si tratta di un'operazione sovrapposta, è possibile recuperare il numero di byte restituiti chiamando la funzione [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) . Se *hDevice* è associato a una porta di completamento di I/O, è possibile ottenere il numero di byte restituiti chiamando la funzione [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

Puntatore a una struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .

Se *hDevice* è stato aperto con il flag **\_ \_ OVERLAPPED del flag file** , *lpOverlapped* deve puntare a una struttura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valida. In questo caso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) viene eseguito come operazione sovrapposta (asincrona). Se il dispositivo è stato aperto con il flag **file \_ \_ sovrapposto** e *lpOverlapped* è **null**, la funzione avrà esito negativo in modi imprevedibili.

Se *hDevice* è stato aperto senza specificare il flag **\_ \_ OVERLAPPED del flag file** , *lpOverlapped* viene ignorato e la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) non viene restituita fino al completamento dell'operazione o fino a quando non si verifica un errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione viene completata correttamente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce un valore diverso da zero.

Se l'operazione ha esito negativo o è in sospeso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce zero. Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Osservazioni

Questa batteria IOCTL recupera il tag corrente della batteria. Il tag della batteria è un valore univoco diverso da zero che cambia quando la batteria fisica viene reinserita, sostituita o sottoposta a qualsiasi modifica delle caratteristiche. Vedere la sezione relativa ai tag della batteria nell'argomento Panoramica [delle informazioni](battery-information.md) sulla batteria per maggiori dettagli su quando viene modificato un tag della batteria, su come rilevare la modifica e su come un'applicazione deve continuare dopo la modifica di un tag della batteria. Quando non è presente una batteria, la richiesta attende l'ora indicata e, se non è ancora presente una batteria, restituirà il file di **errore \_ \_ non \_ trovato** e imposterà il tag della batteria su **tag della batteria non \_ \_ valido**. (Per altre informazioni, vedere informazioni sulla batteria).

Per tutte le richieste di altre informazioni sulla batteria è necessario che il chiamante fornisca il tag della batteria corrispondente. In questo modo il chiamante riceve informazioni per la stessa batteria per ogni richiesta e garantisce che il chiamante sia a conoscenza delle modifiche della batteria senza il polling costante.

Per le implicazioni dell'I/O sovrapposto in questa operazione, vedere la sezione Osservazioni dell'argomento [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .

## <a name="examples"></a>Esempio

Per un esempio, vedere [enumerazione dei dispositivi a batteria](enumerating-battery-devices.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                                                                                                                                                                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                                                                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>Poclass. h; </dt> <dt>BatClass. h in Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni sulla batteria](battery-information.md)
</dt> <dt>

[Codici di controllo del risparmio energia](power-management-control-codes.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**\_ \_ informazioni sulle query della batteria IOCTL \_**](ioctl-battery-query-information.md)
</dt> <dt>

[**\_stato della \_ query della batteria IOCTL \_**](ioctl-battery-query-status.md)
</dt> <dt>

[**\_ \_ informazioni sui set di batterie IOCTL \_**](ioctl-battery-set-information.md)
</dt> </dl>

 

