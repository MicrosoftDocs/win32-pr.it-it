---
description: Notifica alle applicazioni che il BIOS APM ha segnalato un evento OEM APM.
ms.assetid: 3251ac00-41f1-44e9-a579-fa31e7c7d2ff
title: PBT_APMOEMEVENT evento (WinUser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b92feb840e69c3a7e560d7bc71a0a5e4746ae5677920010f0251a1b951ddb8d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961658"
---
# <a name="pbt_apmoemevent-event"></a>Evento \_ APMOEMEVENT PBT

\[PBT \_ APMOEMEVENT è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Il supporto per questo evento è stato rimosso in Windows Vista.\]

Notifica alle applicazioni che il BIOS APM ha segnalato un evento OEM APM.

Una finestra riceve questo evento tramite il [**messaggio WM \_ POWERBROADCAST.**](wm-powerbroadcast.md) I *parametri wParam* *e lParam* vengono impostati come descritto di seguito.


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMOEMEVENT
            LPARAM lParam); // OEM event code
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

| Valore                                                                                                                                                                                                                             | Significato                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMOEMEVENT"></span><span id="pbt_apmoemevent"></span><dl> <dt>**PBT \_ APMOEMEVENT**</dt> <dt>11 (0xB)</dt> </dl> | Identificatore dell'evento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Codice evento definito dall'OEM segnalato dal BIOS APM del sistema. I codici evento OEM sono nell'intervallo 0200h - 02FFh.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Poiché non tutte le implementazioni del BIOS APM forniscono notifiche di eventi OEM, è possibile che questo evento non venga mai trasmesso in alcuni computer.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                                    |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                                           |
| Intestazione<br/>                   | <dl> <dt>WinUser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi di risparmio energia](power-management-events.md)
</dt> <dt>

[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)
</dt> </dl>

 

 




