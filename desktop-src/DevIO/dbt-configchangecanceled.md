---
description: Il sistema trasmette l'evento DBT \_ CONFIGCHANGECANCELED Device quando una richiesta di modifica della configurazione corrente (dock o Undock) è stata annullata.
ms.assetid: b4b1455c-9a04-4fa0-a3fa-ed991f278c0c
title: Evento DBT_CONFIGCHANGECANCELED (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97944daa698808c55f88bc377c9bf1c59c1217fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877758"
---
# <a name="dbt_configchangecanceled-event"></a>\_Evento CONFIGCHANGECANCELED DBT

Il sistema trasmette l'evento DBT \_ CONFIGCHANGECANCELED Device quando una richiesta di modifica della configurazione corrente (dock o Undock) è stata annullata.

Per trasmettere questo evento del dispositivo, il sistema usa il messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) con *wParam* impostato su DBT \_ CONFIGCHANGECANCELED e *lParam* impostati su zero.


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

Impostare su DBT \_ CONFIGCHANGECANCELED.

</dd> <dt>

*lParam* 
</dt> <dd>

Imposta su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true**.

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

 

 




