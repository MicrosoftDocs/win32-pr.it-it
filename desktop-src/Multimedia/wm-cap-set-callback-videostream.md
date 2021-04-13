---
title: Messaggio di WM_CAP_SET_CALLBACK_VIDEOSTREAM (VFW. h)
description: Il \_ messaggio WM Cap \_ set \_ callback \_ VIDEOSTREAM imposta una funzione di callback nell'applicazione.
ms.assetid: 590089b8-7a8d-476b-9b81-f96bf73b0369
keywords:
- WM_CAP_SET_CALLBACK_VIDEOSTREAM messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_VIDEOSTREAM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cde1d2b44ba3786f2d17934e6e92e0894d8d3bba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400256"
---
# <a name="wm_cap_set_callback_videostream-message"></a>\_ \_ \_ Messaggio VIDEOSTREAM di richiamata di WM Cap Set \_

Il messaggio **WM \_ Cap \_ set \_ callback \_ VIDEOSTREAM** imposta una funzione di callback nell'applicazione. AVICap chiama questa procedura durante l'acquisizione del flusso quando un buffer video viene riempito. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) .


```C++
WM_CAP_SET_CALLBACK_VIDEOSTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Puntatore alla funzione di callback del flusso video, di tipo [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback). Specificare **null** per questo parametro per disabilitare una funzione di callback video-stream installata in precedenza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito **positivo o negativo** se è in corso l'acquisizione di flussi o una sessione di acquisizione a singolo frame.

## <a name="remarks"></a>Commenti

La finestra di acquisizione chiama la funzione di callback prima di scrivere il frame acquisito su disco. Questo consente alle applicazioni di modificare il frame se lo si desidera.

Se per l'acquisizione di flussi viene usata una funzione di callback del flusso video, la procedura deve essere installata prima di avviare la sessione di acquisizione e deve rimanere abilitata per la durata della sessione. Può essere disabilitato al termine dell'acquisizione di streaming.

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

 

 





