---
description: Notifica alle applicazioni che il sistema riprende la sospensione o l'ibernazione. Questo evento viene recapitato ogni volta che il sistema riprende e non indica se un utente è presente.
ms.assetid: cd331f79-b64d-479e-aea8-5118ccc87224
title: Evento PBT_APMRESUMEAUTOMATIC (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a7a481dee356c85b3831fcace0c1ff127b0b276
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881714"
---
# <a name="pbt_apmresumeautomatic-event"></a>\_Evento APMRESUMEAUTOMATIC PBT

Notifica alle applicazioni che il sistema riprende la sospensione o l'ibernazione. Questo evento viene recapitato ogni volta che il sistema riprende e non indica se un utente è presente.

Una finestra riceve questo evento tramite il messaggio [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) . I parametri *wParam* e *lParam* sono impostati come descritto di seguito.

> [!Note]  
> Nei sistemi Windows 10, versione 1507 o versioni successive, se il sistema riprende dalla modalità di sospensione solo per entrare immediatamente in ibernazione, questo evento non viene recapitato. In questo caso non viene inviato un messaggio [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) .

 


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMEAUTOMATIC
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

| Valore                                                                                                                                                                                                                                                   | Significato                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMEAUTOMATIC"></span><span id="pbt_apmresumeautomatic"></span><dl> <dt>**PBT \_ APMRESUMEAUTOMATIC**</dt> <dt>18 (0x12)</dt> </dl> | Identificatore dell'evento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Riservati deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Se il sistema rileva qualsiasi attività utente dopo la trasmissione \_ di PBT APMRESUMEAUTOMATIC, trasmette un evento [PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md) per consentire alle applicazioni di essere in grado di riprendere l'interazione completa con l'utente.

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

[\_APMRESUMESUSPEND PBT](pbt-apmresumesuspend.md)
</dt> <dt>

[**\_POWERBROADCAST WM**](wm-powerbroadcast.md)
</dt> </dl>

 

 




