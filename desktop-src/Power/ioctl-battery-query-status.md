---
description: Recupera lo stato corrente della batteria.
ms.assetid: 7a7bf429-9b2c-4faf-9f27-fb5fd8dd18df
title: Codice di controllo IOCTL_BATTERY_QUERY_STATUS (Poclass. h)
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
ms.openlocfilehash: e2de9d3ab48aec13a9a5c1957a5f98aefbe6a09f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312048"
---
# <a name="ioctl_battery_query_status-control-code"></a>\_Codice di \_ \_ controllo stato query IOCTL Battery

Recupera lo stato corrente della batteria.

Per eseguire questa operazione, chiamare la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.


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

Handle per la batteria da cui devono essere restituite le informazioni. Per recuperare un handle di dispositivo, chiamare la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Codice di controllo per l'operazione. Questo valore identifica l'operazione specifica da eseguire e il tipo di dispositivo su cui eseguirla. Usare **\_ \_ \_ lo stato di query della batteria IOCTL** per questa operazione.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Puntatore a una struttura [**di \_ \_ stato di attesa della batteria**](battery-wait-status-str.md) .

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Dimensioni in byte del buffer di input.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Puntatore a una struttura [**di \_ stato della batteria**](battery-status-str.md) .

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Dimensioni in byte del buffer di output.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Puntatore a una variabile che riceve la dimensione dei dati restituiti nel buffer *lpOutBuffer* , in byte.

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

Questa batteria IOCTL recupera lo stato della batteria al momento della restituzione dell'operazione. La struttura del parametro di input, [**\_ \_ stato di attesa della**](battery-wait-status-str.md)batteria, indica quando lo stato della batteria deve essere elaborato e restituito.

Le richieste di stato della batteria possono essere per la restituzione immediata oppure possono essere impostate per attendere una determinata condizione prima del completamento. Ad esempio, è possibile effettuare una richiesta di informazioni sulla batteria per attendere che la capacità della batteria raggiunga un punto specificato o che lo stato della batteria venga modificato.

Tutte le richieste di informazioni sulla batteria vengono completate con lo stato del **file di errore \_ \_ non \_ trovato** ogni volta che l'elemento **BatteryTag** della richiesta non corrisponde a quello del tag della batteria corrente. Per ulteriori informazioni, vedere la pagina relativa ai [tag della batteria](battery-information.md) . Viene usato per garantire che le informazioni della batteria restituita corrispondano a quelle della batteria richiesta.

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

[**stato della batteria \_**](battery-status-str.md)
</dt> <dt>

[**\_stato di attesa della batteria \_**](battery-wait-status-str.md)
</dt> <dt>

[**\_ \_ informazioni sulle query della batteria IOCTL \_**](ioctl-battery-query-information.md)
</dt> <dt>

[**\_tag di \_ query della batteria IOCTL \_**](ioctl-battery-query-tag.md)
</dt> <dt>

[**\_ \_ informazioni sui set di batterie IOCTL \_**](ioctl-battery-set-information.md)
</dt> </dl>

 

