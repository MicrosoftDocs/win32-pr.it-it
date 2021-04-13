---
title: Messaggio di WM_CAP_GET_AUDIOFORMAT (VFW. h)
description: Il \_ messaggio WM Cap \_ get \_ AUDIOFORMAT ottiene il formato audio o le dimensioni del formato audio. È possibile inviare questo messaggio in modo esplicito o usando le macro capGetAudioFormat e capGetAudioFormatSize.
ms.assetid: 25e58863-2b1e-4ed8-9f34-c39617a15bc1
keywords:
- WM_CAP_GET_AUDIOFORMAT messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_GET_AUDIOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9508972c173c9e189bdc092a63d849adf3be739
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400218"
---
# <a name="wm_cap_get_audioformat-message"></a>\_ \_ \_ Messaggio AUDIOFORMAT di WM Cap

Il messaggio **WM \_ Cap \_ get \_ AUDIOFORMAT** ottiene il formato audio o le dimensioni del formato audio. È possibile inviare questo messaggio in modo esplicito o usando le macro [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) e [**capGetAudioFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) .


```C++
WM_CAP_GET_AUDIOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPWAVEFORMATEX) (psAudioFormat); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Dimensione, in byte, della struttura a cui fa riferimento **s**.

</dd> <dt>

<span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*psAudioFormat*
</dt> <dd>

Puntatore a una struttura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) o **null**. Se il valore è **null**, viene restituita la dimensione, in byte, necessaria per mantenere la struttura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la dimensione, in byte, del formato audio.

## <a name="remarks"></a>Commenti

Poiché i formati audio compressi variano in requisiti di dimensioni, le applicazioni devono prima recuperare le dimensioni, quindi allocare memoria e infine richiedere i dati in formato audio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Acquisizione video](video-capture.md)
</dt> <dt>

[Messaggi di acquisizione video](video-capture-messages.md)
</dt> </dl>

 

