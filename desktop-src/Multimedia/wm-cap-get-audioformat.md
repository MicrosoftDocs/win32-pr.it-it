---
title: WM_CAP_GET_AUDIOFORMAT messaggio (Vfw.h)
description: Il messaggio WM \_ CAP \_ GET \_ AUDIOFORMAT ottiene il formato audio o le dimensioni del formato audio. È possibile inviare questo messaggio in modo esplicito o usando le macro capGetAudioFormat e capGetAudioFormatSize.
ms.assetid: 25e58863-2b1e-4ed8-9f34-c39617a15bc1
keywords:
- WM_CAP_GET_AUDIOFORMAT di Windows multimediali
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
ms.openlocfilehash: d247c035f251b387537f8e6c360adf79e6ed479d8d40e4f8fe8180e059dab3cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940739"
---
# <a name="wm_cap_get_audioformat-message"></a>Messaggio WM \_ CAP \_ GET \_ AUDIOFORMAT

Il **messaggio WM CAP GET \_ \_ \_ AUDIOFORMAT** ottiene il formato audio o le dimensioni del formato audio. È possibile inviare questo messaggio in modo esplicito o usando le macro [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) e [**capGetAudioFormatSize.**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize)


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

Puntatore a [**una struttura WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) o **NULL.** Se il valore è **NULL,** vengono restituite le dimensioni, in byte, necessarie per contenere la struttura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce le dimensioni, in byte, del formato audio.

## <a name="remarks"></a>Commenti

Poiché i formati audio compressi variano in base ai requisiti di dimensione, le applicazioni devono prima recuperare le dimensioni, quindi allocare memoria e infine richiedere i dati del formato audio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Acquisizione video](video-capture.md)
</dt> <dt>

[Messaggi di acquisizione video](video-capture-messages.md)
</dt> </dl>

 

