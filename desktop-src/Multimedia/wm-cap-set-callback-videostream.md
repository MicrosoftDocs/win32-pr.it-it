---
title: WM_CAP_SET_CALLBACK_VIDEOSTREAM messaggio (Vfw.h)
description: Il messaggio WM \_ CAP \_ SET CALLBACK \_ \_ VIDEOSTREAM imposta una funzione di callback nell'applicazione.
ms.assetid: 590089b8-7a8d-476b-9b81-f96bf73b0369
keywords:
- WM_CAP_SET_CALLBACK_VIDEOSTREAM messaggio Windows Multimediali
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
ms.openlocfilehash: f2cdb4d7d18997fe437609b43a266242f04bd0bc2bb25429191d944240706244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940719"
---
# <a name="wm_cap_set_callback_videostream-message"></a>Messaggio \_ \_ VIDEOSTREAM DI CALLBACK WM CAP SET \_ \_

Il **messaggio WM CAP SET CALLBACK \_ \_ \_ \_ VIDEOSTREAM** imposta una funzione di callback nell'applicazione. AVICap chiama questa procedura durante l'acquisizione in streaming quando viene riempito un buffer video. È possibile inviare questo messaggio in modo esplicito o usando la macro [**capSetCallbackOnVideoStream.**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream)


```C++
WM_CAP_SET_CALLBACK_VIDEOSTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Puntatore alla funzione di callback del flusso video di tipo [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback). Specificare **NULL per** questo parametro per disabilitare una funzione di callback del flusso video installata in precedenza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'operazione ha esito positivo o **FALSE** se è in corso un'acquisizione di streaming o una sessione di acquisizione a frame singolo.

## <a name="remarks"></a>Commenti

La finestra di acquisizione chiama la funzione di callback prima di scrivere il frame acquisito su disco. In questo modo le applicazioni possono modificare il frame, se necessario.

Se per l'acquisizione in streaming viene usata una funzione di callback del flusso video, la procedura deve essere installata prima di avviare la sessione di acquisizione e deve rimanere abilitata per la durata della sessione. Può essere disabilitato al termine dell'acquisizione dello streaming.

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

 

 





