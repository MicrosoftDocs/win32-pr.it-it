---
title: Messaggio di WM_CAP_SET_PREVIEWRATE (VFW. h)
description: Il \_ messaggio WM Cap \_ set \_ PREVIEWRATE imposta la frequenza di visualizzazione dei frame in modalità anteprima. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capPreviewRate.
ms.assetid: 1189ad4a-1f32-4684-920b-ee3c26ef97f8
keywords:
- WM_CAP_SET_PREVIEWRATE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_SET_PREVIEWRATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1134255b73e579841800af6cd5f6900965217106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964886"
---
# <a name="wm_cap_set_previewrate-message"></a>\_ \_ Messaggio PREVIEWRATE set di estremità WM \_

Il messaggio **WM \_ Cap \_ set \_ PREVIEWRATE** imposta la frequenza di visualizzazione dei frame in modalità anteprima. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) .


```C++
WM_CAP_SET_PREVIEWRATE 
wParam = (WPARAM) (wMS); 
lParam = 0L; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wMS"></span><span id="wms"></span><span id="WMS"></span>*wMS*
</dt> <dd>

Frequenza, in millisecondi, in base alla quale vengono acquisiti e visualizzati nuovi frame.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** se la finestra di acquisizione non è connessa a un driver di acquisizione.

## <a name="remarks"></a>Commenti

La modalità di anteprima usa risorse di CPU sostanziali. Le applicazioni possono disabilitare l'anteprima o abbassare la frequenza di anteprima quando un'altra applicazione ha lo stato attivo. Durante lo streaming di acquisizione video, l'attività di anteprima è più bassa rispetto alla scrittura di frame su disco e i frame di anteprima vengono visualizzati solo se non sono disponibili altri buffer per la scrittura.

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

 

 





