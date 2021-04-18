---
description: Notifica alle applicazioni che il sistema ha ripreso l'operazione dopo essere stata sospesa.
ms.assetid: 9058a2ff-9b8e-48e5-accb-4810c8598294
title: Evento PBT_APMRESUMESUSPEND (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d26357215853e0989851b6a9e731340a8dc2e6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312033"
---
# <a name="pbt_apmresumesuspend-event"></a>\_Evento APMRESUMESUSPEND PBT

Notifica alle applicazioni che il sistema ha ripreso l'operazione dopo essere stata sospesa.

Una finestra riceve questo evento tramite il messaggio [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) . I parametri *wParam* e *lParam* sono impostati come descritto di seguito.


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMESUSPEND
            LPARAM lParam); // zero
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* 
</dt> <dd>

Handle per la finestra.

</dd> <dt>*uMsg*</dt> <dd> 

| Valore                                                                                                                                                                                                                                                                   | Significato                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt> </dl> | Identificatore del messaggio.<br/> |



 

</dd> <dt>*wParam*</dt> <dd> 

| Valore                                                                                                                                                                                                                                           | Significato                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMESUSPEND"></span><span id="pbt_apmresumesuspend"></span><dl> <dt>**PBT \_ APMRESUMESUSPEND**</dt> <dt>7 (0x7)</dt> </dl> | Identificatore dell'evento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Riservati deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Un'applicazione può ricevere questo evento solo se ha ricevuto l' [evento \_ APMSUSPEND PBT](pbt-apmsuspend.md) prima della sospensione del computer. In caso contrario, l'applicazione riceverà un evento [PBT \_ APMRESUMECRITICAL](pbt-apmresumecritical.md) .

Se il sistema viene riattivato a causa dell'attività dell'utente, ad esempio premendo il pulsante di alimentazione, o se il sistema rileva l'interazione dell'utente sulla console fisica (ad esempio, l'input del mouse o della tastiera) dopo la riattivazione automatica, il sistema trasmette prima di tutto l'evento [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) , quindi trasmette l' \_ evento PBT APMRESUMESUSPEND. Inoltre, il sistema attiva la visualizzazione. L'applicazione deve riaprire i file chiusi quando il sistema entra in sospensione e prepara l'input dell'utente.

Se il sistema viene riattivato a causa di un segnale di riattivazione esterno (riattivazione remota), il sistema trasmette solo l'evento [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) . L' \_ evento APMRESUMESUSPEND PBT non viene inviato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>WinUser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi di riattivazione del sistema](system-wake-up-events.md)
</dt> <dt>

[Eventi di risparmio energia](power-management-events.md)
</dt> <dt>

[\_APMSUSPEND PBT](pbt-apmsuspend.md)
</dt> <dt>

[\_APMRESUMECRITICAL PBT](pbt-apmresumecritical.md)
</dt> <dt>

[**\_POWERBROADCAST WM**](wm-powerbroadcast.md)
</dt> </dl>

 

 




