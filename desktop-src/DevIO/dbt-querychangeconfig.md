---
description: Il sistema trasmette l'evento DBT \_ QUERYCHANGECONFIG Device per richiedere l'autorizzazione per modificare la configurazione corrente (dock o Undock). Qualsiasi applicazione può negare questa richiesta e annullare la modifica.
ms.assetid: 2e452ea7-e2bf-4500-952a-ee7d891533a0
title: Evento DBT_QUERYCHANGECONFIG (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48367da1788ae2985b21fad6e960153008e9ffd2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523650"
---
# <a name="dbt_querychangeconfig-event"></a>\_Evento QUERYCHANGECONFIG DBT

Il sistema trasmette l'evento DBT \_ QUERYCHANGECONFIG Device per richiedere l'autorizzazione per modificare la configurazione corrente (dock o Undock). Qualsiasi applicazione può negare questa richiesta e annullare la modifica.

Per trasmettere questo evento del dispositivo, il sistema usa il messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) con *wParam* impostato su DBT \_ QUERYCHANGECONFIG e *lParam* impostati su zero.


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* 
</dt> <dd>

Handle di una finestra.

</dd> <dt>

*uMsg* 
</dt> <dd>

Identificatore del messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) .

</dd> <dt>

*wParam* 
</dt> <dd>

Impostare su DBT \_ QUERYCHANGECONFIG.

</dd> <dt>

*lParam* 
</dt> <dd>

Imposta su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** per concedere l'autorizzazione per modificare la configurazione.

Return BROADCAST \_ query \_ Deny per negare l'autorizzazione per modificare la configurazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP<br/>                                                            |
| Server minimo supportato<br/> | Windows Server 2003<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>DBT. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi dispositivo](device-events.md)
</dt> <dt>

[Eventi di gestione dei dispositivi](device-management-events.md)
</dt> <dt>

[**\_DEVICECHANGE WM**](wm-devicechange.md)
</dt> </dl>

 

 




