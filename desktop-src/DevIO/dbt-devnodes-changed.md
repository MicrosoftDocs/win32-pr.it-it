---
description: Il sistema trasmette l'evento del dispositivo DBT DEVNODES CHANGED quando un dispositivo è stato aggiunto \_ \_ o rimosso dal sistema. Le applicazioni che gestiscono elenchi di dispositivi nel sistema devono aggiornare i propri elenchi.
ms.assetid: 62acc633-7dad-4792-a5a2-1f95356479d1
title: DBT_DEVNODES_CHANGED evento (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00d43873241c3f72336dd996fb9fa3486229d9ffcf522923d68ab606313afb7e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539161"
---
# <a name="dbt_devnodes_changed-event"></a>DBT \_ DEVNODES \_ CHANGED - evento

Il sistema trasmette l'evento del dispositivo DBT DEVNODES CHANGED quando un dispositivo è stato aggiunto \_ \_ o rimosso dal sistema. Le applicazioni che gestiscono elenchi di dispositivi nel sistema devono aggiornare i propri elenchi.

Per trasmettere questo evento del dispositivo, il sistema usa il messaggio [**\_ DEVICECHANGE WM**](wm-devicechange.md) con *wParam* impostato su DBT \_ DEVNODES \_ CHANGED e *lParam* impostato su zero.


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

*Hwnd* 
</dt> <dd>

Handle di una finestra.

</dd> <dt>

*Umsg* 
</dt> <dd>

Identificatore [**del \_ messaggio DEVICECHANGE WM.**](wm-devicechange.md)

</dd> <dt>

*wParam* 
</dt> <dd>

Impostare su DBT \_ DEVNODES \_ CHANGED.

</dd> <dt>

*lParam* 
</dt> <dd>

Imposta su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE.**

## <a name="remarks"></a>Commenti

Non sono disponibili informazioni aggiuntive sul dispositivo aggiunto o rimosso dal sistema. Le applicazioni che richiedono altre informazioni devono registrarsi per la notifica del dispositivo usando [**la funzione RegisterDeviceNotification.**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP<br/>                                                            |
| Server minimo supportato<br/> | Windows Server 2003<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>Dbt.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi del dispositivo](device-events.md)
</dt> <dt>

[Eventi di gestione dei dispositivi](device-management-events.md)
</dt> <dt>

[**DEV \_ BROADCAST \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[**WM \_ DEVICECHANGE**](wm-devicechange.md)
</dt> </dl>

 

 




