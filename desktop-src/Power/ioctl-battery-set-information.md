---
description: Imposta varie informazioni sulla batteria.
ms.assetid: b827983d-5fb8-43f2-b732-541d16b3eb7b
title: IOCTL_BATTERY_SET_INFORMATION di controllo (Poclass.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_SET_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: be6fca1042c4ba381996ccca1740d1662f9795269aaaa8b3e429576d96011dbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143494"
---
# <a name="ioctl_battery_set_information-control-code"></a>CODICE DI CONTROLLO INFORMAZIONI \_ \_ SET \_ BATTERIA IOCTL

Imposta varie informazioni sulla batteria. La struttura del parametro di input [**BATTERY \_ SET \_ INFORMATION**](battery-set-information-str.md)indica le informazioni sullo stato della batteria da impostare.

Per eseguire questa operazione, chiamare la [**funzione DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,              // handle to battery
  IOCTL_BATTERY_SET_INFORMATION, // dwIoControlCode
  (LPVOID) lpInBuffer,           // input buffer
  (DWORD) nInBufferSize,         // size of input buffer
  NULL,                          // lpOutBuffer
  0,                             // nOutBufferSize
  (LPDWORD) lpBytesReturned,     // number of bytes returned
  (LPOVERLAPPED) lpOverlapped    // OVERLAPPED structure
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle della batteria su cui devono essere impostate le informazioni. Per recuperare un handle di dispositivo, chiamare [**la funzione CreateFile.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Codice di controllo per l'operazione. Questo valore identifica l'operazione specifica da eseguire e il tipo di dispositivo in cui eseguirla. Usare **IOCTL \_ BATTERY SET INFORMATION \_ \_ per** questa operazione.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Puntatore a una [**struttura BATTERY \_ SET \_ INFORMATION.**](battery-set-information-str.md)

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Dimensioni del buffer di input, in byte.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Non utilizzato con questa operazione. impostato su **NULL.**

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Non utilizzato con questa operazione. impostato su zero.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Puntatore a una variabile che riceve le dimensioni dei dati restituiti nel buffer *lpOutBuffer,* in byte.

Se il buffer di output è troppo piccolo per restituire dati, la chiamata non riesce, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce il codice di errore ERROR INSUFFICIENT BUFFER e il numero di byte restituiti \_ \_ è zero.

Se *lpOverlapped* è **NULL** (I/O non sovrapposto), *lpBytesReturned* non può essere **NULL,** anche se *lpOutBuffer* è **NULL.**

Se *lpOverlapped* non è **NULL** (I/O sovrapposto), *lpBytesReturned* può essere **NULL.** Se si tratta di un'operazione sovrapposta, è possibile recuperare il numero di byte restituiti chiamando la [**funzione GetOverlappedResult.**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) Se *hDevice è* associato a una porta di completamento I/O, è possibile ottenere il numero di byte restituiti chiamando la [**funzione GetQueuedCompletionStatus.**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

Puntatore a una [**struttura OVERLAPPED.**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)

Se *hDevice è* stato aperto con il flag FILE \_ FLAG \_ OVERLAPPED, *lpOverlapped* deve puntare a una struttura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valida. In questo caso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) viene eseguito come operazione sovrapposta (asincrona). Se il dispositivo è stato aperto con il flag FILE FLAG OVERLAPPED e \_ \_ *lpOverlapped* è **NULL,** la funzione ha esito negativo in modi imprevedibili.

Se *hDevice* è stato aperto senza specificare il flag FILE \_ FLAG \_ OVERLAPPED, *lpOverlapped* viene ignorato e la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) non restituisce alcun valore fino al completamento dell'operazione o fino a quando non si verifica un errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione viene completata correttamente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce un valore diverso da zero.

Se l'operazione non riesce o è in sospeso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce zero. Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Osservazioni

Tutte le richieste di impostazione delle informazioni sulla batteria verranno completate con lo stato FILE DI ERRORE NON TROVATO se il tag della batteria della richiesta non corrisponde a \_ quello del tag della batteria \_ \_ corrente.

Per informazioni sulle implicazioni dell'I/O sovrapposto su questa operazione, vedere la sezione Osservazioni [**dell'argomento DeviceIoControl.**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                                                                                                                                                                                         |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                                                                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>Poclass.h;</dt> <dt>Batclass.h in Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni sulla batteria](battery-information.md)
</dt> <dt>

[Codici di controllo del risparmio energia](power-management-control-codes.md)
</dt> <dt>

[**Deviceiocontrol**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**INFORMAZIONI SUL \_ SET DI \_ BATTERIA**](battery-set-information-str.md)
</dt> <dt>

[**INFORMAZIONI SULLA \_ QUERY DELLA \_ BATTERIA IOCTL \_**](ioctl-battery-query-information.md)
</dt> <dt>

[**STATO QUERY BATTERIA IOCTL \_ \_ \_**](ioctl-battery-query-status.md)
</dt> <dt>

[**TAG DI \_ QUERY DELLA \_ BATTERIA IOCTL \_**](ioctl-battery-query-tag.md)
</dt> </dl>

 

