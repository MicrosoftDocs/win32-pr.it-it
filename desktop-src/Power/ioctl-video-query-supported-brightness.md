---
description: Recupera i livelli di retroilluminazione supportati.
ms.assetid: b4c1ee3f-af75-477e-b7ed-53be905374d7
title: IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS di controllo (Ntddvdeo.h)
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
ms.openlocfilehash: 0c41b6773b0ed64160e2ad8850b6092dd5ec987c3e6726ba1cd668909c266311
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143394"
---
# <a name="ioctl_video_query_supported_brightness-control-code"></a>IOCTL VIDEO QUERY SUPPORTED BRIGHTNESS control code (CODICE DI CONTROLLO LUMINOSITÀ SUPPORTATO PER LE \_ QUERY VIDEO IOCTL) \_ \_ \_

Recupera i livelli di retroilluminazione supportati.

Per eseguire questa operazione, chiamare la [**funzione DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.


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

Handle per \\ \\ l'oggetto . \\ Dispositivo LCD. Per recuperare un handle di dispositivo, chiamare [**la funzione CreateFile.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Codice di controllo per l'operazione. Questo valore identifica l'operazione specifica da eseguire e il tipo di dispositivo in cui eseguirla. Usare **IOCTL \_ VIDEO QUERY SUPPORTED BRIGHTNESS \_ \_ \_ per** questa operazione.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Non utilizzato con questa operazione. impostato su **NULL.**

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Non utilizzato con questa operazione. impostato su zero.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Puntatore a un buffer che riceve una matrice dei livelli di alimentazione disponibili. Questo buffer deve avere una lunghezza di 256 byte.

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Dimensioni in byte del buffer di output.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Puntatore a una variabile che riceve le dimensioni, in byte, dei dati di output restituiti.

Se il buffer di output è troppo piccolo per restituire dati, la chiamata non riesce, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce il codice di errore ERROR INSUFFICIENT BUFFER e il numero di byte restituiti \_ \_ è zero.

Se il buffer di output è troppo piccolo per contenere tutti i dati, ma può contenere alcune voci, il sistema operativo restituisce quanto più adatto, la chiamata non riesce, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce il codice di errore ERROR MORE DATA e \_ \_ *lpBytesReturned* indica la quantità di dati restituiti. L'applicazione deve [**chiamare di nuovo DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con la stessa operazione, specificando un nuovo punto di partenza.

Se *lpOverlapped* è **NULL** (I/O non sovrapposto), *lpBytesReturned* non può essere **NULL.**

Se *lpOverlapped* non è **NULL** (I/O sovrapposto), *lpBytesReturned* può essere **NULL.** Se si tratta di un'operazione sovrapposta, è possibile recuperare il numero di byte restituiti chiamando la [**funzione GetOverlappedResult.**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) Se *hDevice è* associato a una porta di completamento I/O, è possibile ottenere il numero di byte restituiti chiamando la [**funzione GetQueuedCompletionStatus.**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

Puntatore a una [**struttura OVERLAPPED.**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)

Se *hDevice è* stato aperto con il flag FILE \_ FLAG \_ OVERLAPPED, *lpOverlapped* deve puntare a una struttura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valida. In questo caso, l'operazione viene eseguita come operazione sovrapposta (asincrona). Se il dispositivo è stato aperto con il flag FILE FLAG OVERLAPPED e \_ \_ *lpOverlapped* è **NULL,** la funzione ha esito negativo in modi imprevedibili.

Se *hDevice* è stato aperto senza specificare il flag FILE \_ FLAG \_ OVERLAPPED, *lpOverlapped* viene ignorato e [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) non restituisce alcun valore fino al completamento dell'operazione o fino a quando non si verifica un errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione viene completata correttamente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce un valore diverso da zero.

Se l'operazione non riesce o è in sospeso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce zero. Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Osservazioni

Ogni elemento nella matrice *lpOutBuffer* ha una lunghezza di un byte. Pertanto, al momento della restituzione, *il parametro lpBytesReturned* indica il numero di livelli supportati. Ogni livello è un valore compreso tra 0 e 100. Maggiore è il valore, più chiaro è la retroilluminazione. Tutti i livelli sono supportati indipendentemente dal fatto che la fonte di alimentazione sia CA o DC.

Il file di intestazione usato per compilare applicazioni che includono questa funzionalità, Ntddvdeo.h, è incluso in Microsoft Windows Driver Development Kit (DDK). Per informazioni su come ottenere il DDK, vedere [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .

In alternativa, è possibile definire questo codice di controllo come segue:

``` syntax
#define IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x125, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows XP solo con app desktop SP1 \[\]<br/>                   |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Ntddvdeo.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfaccia di controllo retroilluminazione](backlight-control-interface.md)
</dt> <dt>

[**Deviceiocontrol**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

