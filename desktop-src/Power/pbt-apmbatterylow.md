---
description: Notifica alle applicazioni che l'energia elettrica della batteria è insufficiente.
ms.assetid: ef24b8cf-d801-4452-a03c-3f2bdbdd7e5d
title: Evento PBT_APMBATTERYLOW (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64884f9bb01e37883e1be61b2de88862e8b119fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312040"
---
# <a name="pbt_apmbatterylow-event"></a>\_Evento APMBATTERYLOW PBT

\[PBT \_ APMBATTERYLOW è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Il supporto per questo evento è stato rimosso in Windows Vista. In alternativa, usare [PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) .\]

Notifica alle applicazioni che l'energia elettrica della batteria è insufficiente.

Una finestra riceve questo evento tramite il messaggio [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) . I parametri *wParam* e *lParam* sono impostati come descritto di seguito.


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMBATTERYLOW
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

| Valore                                                                                                                                                                                                                                  | Significato                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMBATTERYLOW"></span><span id="pbt_apmbatterylow"></span><dl> <dt>**PBT \_ APMBATTERYLOW**</dt> <dt>9 (0x9)</dt> </dl> | Identificatore dell'evento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Riservato, deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Questo evento viene trasmesso quando un BIOS APM del sistema segnala una notifica di batteria insufficiente per APM. Poiché alcune implementazioni del BIOS APM non forniscono notifiche quando le batterie sono insufficienti, questo evento potrebbe non essere mai trasmesso in alcuni computer.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                                    |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                                           |
| Intestazione<br/>                   | <dl> <dt>WinUser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi di risparmio energia](power-management-events.md)
</dt> <dt>

[**\_POWERBROADCAST WM**](wm-powerbroadcast.md)
</dt> </dl>

 

 




