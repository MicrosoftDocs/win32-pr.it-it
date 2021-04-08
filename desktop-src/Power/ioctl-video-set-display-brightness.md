---
description: Imposta i livelli di retroilluminazione AC e DC correnti.
ms.assetid: baa77811-046d-4a07-b3df-2a31fba2d9a7
title: Codice di controllo IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS (Ntddvdeo. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: a0c679f352012eea66b80335bc3ad1547501dd92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967494"
---
# <a name="ioctl_video_set_display_brightness-control-code"></a>\_Codice di \_ controllo \_ della \_ luminosità del set di video IOCTL

Imposta i livelli di retroilluminazione AC e DC correnti.

Per eseguire questa operazione, chiamare la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to device
  IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS, // dwIoControlCode
  (LPVOID) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of the input buffer
  NULL,                        // lpOutBuffer
  0,                           // nOutBufferSize 
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped  // OVERLAPPED structure
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

Codice di controllo per l'operazione. Questo valore identifica l'operazione specifica da eseguire e il tipo di dispositivo su cui eseguirla. Usare **la \_ \_ luminosità di \_ visualizzazione \_ del set di video IOCTL** per questa operazione.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Puntatore a una struttura [**di \_ luminosità della visualizzazione**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) .

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Dimensioni del buffer a cui punta *lpOutBuffer* in byte.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Non utilizzato con questa operazione. impostare su **null**.

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Non utilizzato con questa operazione. impostare su zero.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Puntatore a una variabile che riceve il numero effettivo di byte restituiti dalla funzione nel buffer di output.

Se *lpOverlapped* è **null** (I/O non sovrapposti), *lpBytesReturned* viene utilizzato internamente e non può essere **null**.

Se *lpOverlapped* non è **null** (I/O sovrapposto), *lpBytesReturned* può essere **null**.

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

I valori specificati nei membri **ucACBrightness** e **ucDCBrightness** della struttura di [**\_ luminosità dello schermo**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) devono essere stati restituiti in precedenza [**dalla \_ \_ \_ \_ luminosità supportata dalla query IOCTL video**](ioctl-video-query-supported-brightness.md). Se, ad esempio, i valori supportati sono 10, 20, 30, 40, 50, 60, 70, 80, 90 e 100, l'utilizzo di un valore di 33 è un errore.

Il file di intestazione utilizzato per compilare applicazioni che includono questa funzionalità, Ntddvdeo. h, è incluso in Microsoft Windows Driver Development Kit (DDK). Per informazioni su come ottenere il DDK, vedere [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .

In alternativa, è possibile definire questo codice di controllo come segue:

``` syntax
#define IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x127, METHOD_BUFFERED, FILE_ANY_ACCESS)
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
</dt> <dt>

[**\_luminosità visualizzazione**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))
</dt> <dt>

[**\_ \_ \_ luminosità visualizzazione query video \_ IOCTL**](ioctl-video-query-display-brightness.md)
</dt> <dt>

[**\_ \_ luminosità supportata dalla query video \_ IOCTL \_**](ioctl-video-query-supported-brightness.md)
</dt> </dl>

 

