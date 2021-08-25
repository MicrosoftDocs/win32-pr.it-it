---
description: Imposta i livelli di retroilluminazione ca e controller di dominio correnti.
ms.assetid: baa77811-046d-4a07-b3df-2a31fba2d9a7
title: IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS codice di controllo (Ntddvdeo.h)
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
ms.openlocfilehash: ec4bb5200378f9f530913f26d33bfbd485d81ae184c7b478a51c90bca18d95da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961851"
---
# <a name="ioctl_video_set_display_brightness-control-code"></a>Codice di controllo DISPLAY BRIGHTNESS DI IOCTL \_ VIDEO \_ SET \_ \_

Imposta i livelli di retroilluminazione ca e controller di dominio correnti.

Per eseguire questa operazione, chiamare la [**funzione DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.


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

Handle per \\ \\ l'oggetto . \\ Dispositivo LCD. Per recuperare un handle di dispositivo, chiamare [**la funzione CreateFile.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Codice di controllo per l'operazione. Questo valore identifica l'operazione specifica da eseguire e il tipo di dispositivo in cui eseguirla. Usare **IOCTL \_ VIDEO SET DISPLAY BRIGHTNESS \_ \_ \_ per** questa operazione.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Puntatore a una [**struttura DISPLAY \_ BRIGHTNESS.**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Dimensioni del buffer a cui punta *lpOutBuffer,* in byte.

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

Puntatore a una variabile che riceve il conteggio effettivo dei byte restituiti dalla funzione nel buffer di output.

Se *lpOverlapped* è **NULL** (I/O non sovrapposto), *lpBytesReturned* viene usato internamente e non può essere **NULL.**

Se *lpOverlapped* non è **NULL** (I/O sovrapposto), *lpBytesReturned* può essere **NULL.**

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

I valori specificati nei membri **ucACBrightness** e **ucDCBrightness** della struttura [**DISPLAY \_ BRIGHTNESS**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) devono essere stati restituiti in precedenza da [**IOCTL \_ VIDEO QUERY SUPPORTED \_ \_ \_ BRIGHTNESS.**](ioctl-video-query-supported-brightness.md) Ad esempio, se i valori supportati sono 10, 20, 30, 40, 50, 60, 70, 80, 90 e 100, l'uso di un valore pari a 33 sarebbe un errore.

Il file di intestazione usato per compilare applicazioni che includono questa funzionalità, Ntddvdeo.h, è incluso in Microsoft Windows Driver Development Kit (DDK). Per informazioni su come ottenere il DDK, vedere [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .

In alternativa, è possibile definire questo codice di controllo come segue:

``` syntax
#define IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x127, METHOD_BUFFERED, FILE_ANY_ACCESS)
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
</dt> <dt>

[**LUMINOSITÀ \_ DELLO SCHERMO**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))
</dt> <dt>

[**LUMINOSITÀ DELLA \_ VISUALIZZAZIONE DELLA QUERY VIDEO IOCTL \_ \_ \_**](ioctl-video-query-display-brightness.md)
</dt> <dt>

[**LUMINOSITÀ SUPPORTATA \_ PER LE QUERY VIDEO IOCTL \_ \_ \_**](ioctl-video-query-supported-brightness.md)
</dt> </dl>

 

