---
description: Notifica alle applicazioni che il computer sta per entrare in uno stato sospeso.
ms.assetid: 61b177a0-4cff-4740-bed8-a46c06c43be8
title: PBT_APMSUSPEND evento (WinUser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb3634765e6c0f863beb0c7a1c16af29cadae18ef14796e9ef01a0c8edec36a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961671"
---
# <a name="pbt_apmsuspend-event"></a>Evento PBT \_ APMSUSPEND

Notifica alle applicazioni che il computer sta per entrare in uno stato sospeso. Questo evento viene in genere trasmesso quando tutte le applicazioni e i driver installabili hanno restituito **TRUE** a un evento [ \_ APMQUERYSUSPEND PBT](pbt-apmquerysuspend.md) precedente.

Una finestra riceve questo evento tramite il [**messaggio WM \_ POWERBROADCAST.**](wm-powerbroadcast.md) I *parametri wParam* *e lParam* vengono impostati come descritto di seguito.


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMSUSPEND
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

| Valore                                                                                                                                                                                                                         | Significato                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMSUSPEND"></span><span id="pbt_apmsuspend"></span><dl> <dt>**PBT \_ APMSUSPEND**</dt> <dt>4 (0x4)</dt> </dl> | Identificatore dell'evento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Riservato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Un'applicazione deve elaborare questo evento completando tutte le attività necessarie per salvare i dati.

Il sistema consente circa due secondi a un'applicazione di gestire questa notifica. Se un'applicazione sta ancora eseguendo operazioni dopo la scadenza dell'acconto temporale, il sistema potrebbe interrompere l'applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                              |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>WinUser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Criteri di sospensione del sistema](system-sleep-criteria.md)
</dt> <dt>

[Eventi di riattivazione del sistema](system-wake-up-events.md)
</dt> <dt>

[Eventi di risparmio energia](power-management-events.md)
</dt> <dt>

[PBT \_ APMQUERYSUSPEND](pbt-apmquerysuspend.md)
</dt> <dt>

[**SetSystemPowerState**](/windows/desktop/api/WinBase/nf-winbase-setsystempowerstate)
</dt> <dt>

[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)
</dt> </dl>

 

 




