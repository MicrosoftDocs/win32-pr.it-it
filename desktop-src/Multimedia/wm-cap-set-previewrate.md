---
title: WM_CAP_SET_PREVIEWRATE messaggio (Vfw.h)
description: Il messaggio WM \_ CAP \_ SET \_ PREVIEWRATE imposta la frequenza di visualizzazione dei fotogrammi in modalità di anteprima. È possibile inviare questo messaggio in modo esplicito o usando la macro capPreviewRate.
ms.assetid: 1189ad4a-1f32-4684-920b-ee3c26ef97f8
keywords:
- WM_CAP_SET_PREVIEWRATE messaggio Windows Multimediali
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
ms.openlocfilehash: fa9b9a24614a40c5efb545b91a80069bf915c77c4b7d8fb289ed581f750ac0cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135083"
---
# <a name="wm_cap_set_previewrate-message"></a>MESSAGGIO \_ WM CAP SET \_ \_ PREVIEWRATE

Il **messaggio WM CAP SET \_ \_ \_ PREVIEWRATE** imposta la frequenza di visualizzazione dei fotogrammi in modalità di anteprima. È possibile inviare questo messaggio in modo esplicito o usando la macro [**capPreviewRate.**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate)


```C++
WM_CAP_SET_PREVIEWRATE 
wParam = (WPARAM) (wMS); 
lParam = 0L; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wMS"></span><span id="wms"></span><span id="WMS"></span>*Wms*
</dt> <dd>

Frequenza, in millisecondi, con cui vengono acquisiti e visualizzati nuovi fotogrammi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** se ha esito positivo **o FALSE** se la finestra di acquisizione non è connessa a un driver di acquisizione.

## <a name="remarks"></a>Commenti

La modalità di anteprima usa notevoli risorse della CPU. Le applicazioni possono disabilitare l'anteprima o ridurre la frequenza di anteprima quando un'altra applicazione ha lo stato attivo. Durante l'acquisizione di video in streaming, l'attività di anteprima ha una priorità inferiore rispetto alla scrittura di fotogrammi su disco e i fotogrammi di anteprima vengono visualizzati solo se non sono disponibili altri buffer per la scrittura.

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

 

 





