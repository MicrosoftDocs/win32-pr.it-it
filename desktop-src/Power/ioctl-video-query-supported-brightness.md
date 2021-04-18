---
description: Recupera i livelli di retroilluminazione supportati.
ms.assetid: b4c1ee3f-af75-477e-b7ed-53be905374d7
title: Codice di controllo IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS (Ntddvdeo. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: a5618ec29fd47ba690106b5f826e6fb145eac208
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312044"
---
# <a name="ioctl_video_query_supported_brightness-control-code"></a>\_Codice di \_ controllo della \_ luminosità supportato dalla query video IOCTL \_

Recupera i livelli di retroilluminazione supportati.

Per eseguire questa operazione, chiamare la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to device
  IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS,  // dwIoControlCode
  NULL,                            // lpInBuffer
  0,                               // nInBufferSize
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle per l'oggetto \\ \\ . \\ Dispositivo LCD. Per recuperare un handle di dispositivo, chiamare la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Codice di controllo per l'operazione. Questo valore identifica l'operazione specifica da eseguire e il tipo di dispositivo su cui eseguirla. Usare **la \_ \_ \_ \_ luminosità supportata da query video IOCTL** per questa operazione.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Non utilizzato con questa operazione. impostare su **null**.

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Non utilizzato con questa operazione. impostare su zero.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Puntatore a un buffer che riceve una matrice dei livelli di alimentazione disponibili. Il buffer deve avere una lunghezza di 256 byte.

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Dimensioni in byte del buffer di output.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Puntatore a una variabile che riceve le dimensioni, in byte, dei dati di output restituiti.

Se il buffer di output è troppo piccolo per restituire i dati, la chiamata ha esito negativo, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce il buffer insufficiente per l'errore del codice di errore \_ \_ e il numero di byte restituito è zero.

Se il buffer di output è troppo piccolo per conservare tutti i dati, ma può inserire alcune voci, il sistema operativo viene restituito per quanto riguarda, la chiamata ha esito negativo, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l'errore del codice \_ di errore più \_ dati e *lpBytesReturned* indica la quantità di dati restituiti. L'applicazione deve chiamare nuovamente [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con la stessa operazione, specificando un nuovo punto di partenza.

Se *lpOverlapped* è **null** (I/O non sovrapposti), *lpBytesReturned* non può essere **null**.

Se *lpOverlapped* non è **null** (I/O sovrapposto), *lpBytesReturned* può essere **null**. Se si tratta di un'operazione sovrapposta, è possibile recuperare il numero di byte restituiti chiamando la funzione [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) . Se *hDevice* è associato a una porta di completamento di I/O, è possibile ottenere il numero di byte restituiti chiamando la funzione [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

Puntatore a una struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .

Se *hDevice* è stato aperto con il flag \_ OVERLAPPED del flag file \_ , *lpOverlapped* deve puntare a una struttura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valida. In questo caso, l'operazione viene eseguita come operazione sovrapposta (asincrona). Se il dispositivo è stato aperto con il flag FILE \_ \_ sovrapposto e *lpOverlapped* è **null**, la funzione avrà esito negativo in modi imprevedibili.

Se *hDevice* è stato aperto senza specificare il \_ flag Overlapped del flag file \_ , *lpOverlapped* viene ignorato e [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) non restituisce fino a quando l'operazione non viene completata o fino a quando non si verifica un errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione viene completata correttamente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce un valore diverso da zero.

Se l'operazione ha esito negativo o è in sospeso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce zero. Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Osservazioni

Ogni elemento nella matrice *lpOutBuffer* è di lunghezza pari a un byte. Pertanto, al momento della restituzione, il parametro *lpBytesReturned* indica il numero di livelli supportati. Ogni livello è un valore compreso tra 0 e 100. Maggiore è il valore, più luminoso è la retroilluminazione. Tutti i livelli sono supportati se la fonte di alimentazione è AC o DC.

Il file di intestazione utilizzato per compilare applicazioni che includono questa funzionalità, Ntddvdeo. h, è incluso in Microsoft Windows Driver Development Kit (DDK). Per informazioni su come ottenere il DDK, vedere [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .

In alternativa, è possibile definire questo codice di controllo come segue:

``` syntax
#define IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x125, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, \[ solo app desktop Windows XP con SP1\]<br/>                   |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Ntddvdeo. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfaccia di controllo retroilluminazione](backlight-control-interface.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

