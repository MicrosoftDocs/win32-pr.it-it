---
description: Notifica alle applicazioni che il sistema sta riprendendo dalla sospensione o dall'ibernazione. Questo evento viene recapitato ogni volta che il sistema riprende e non indica se un utente è presente.
ms.assetid: cd331f79-b64d-479e-aea8-5118ccc87224
title: PBT_APMRESUMEAUTOMATIC evento (WinUser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43e66fcd2201e9fb3c4feeb135843e92a350303b89a5c5045836428b9a326a30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143344"
---
# <a name="pbt_apmresumeautomatic-event"></a>Evento PBT \_ APMRESUMEAUTOMATIC

Notifica alle applicazioni che il sistema sta riprendendo dalla sospensione o dall'ibernazione. Questo evento viene recapitato ogni volta che il sistema riprende e non indica se un utente è presente.

Una finestra riceve questo evento tramite il [**messaggio WM \_ POWERBROADCAST.**](wm-powerbroadcast.md) I *parametri wParam* *e lParam* vengono impostati come descritto di seguito.

> [!Note]  
> In Windows 10 versione 1507 o successiva, se il sistema riprende dalla sospensione solo per entrare immediatamente in ibernazione, questo evento non viene recapitato. In questo caso, non viene inviato un messaggio [**WM \_ POWERBROADCAST.**](wm-powerbroadcast.md)

 


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

*Hwnd* 
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

Riservato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Se il sistema rileva un'attività utente dopo la trasmissione di PBT \_ APMRESUMEAUTOMATIC, trasmetterà un evento [ \_ PBT APMRESUMESUSPEND](pbt-apmresumesuspend.md) per invii alle applicazioni la possibilità di riprendere l'interazione completa con l'utente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                              |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>WinUser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi di riattivazione del sistema](system-wake-up-events.md)
</dt> <dt>

[Eventi di risparmio energia](power-management-events.md)
</dt> <dt>

[PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md)
</dt> <dt>

[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)
</dt> </dl>

 

 




