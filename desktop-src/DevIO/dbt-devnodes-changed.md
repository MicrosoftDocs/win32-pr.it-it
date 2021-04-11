---
description: Il sistema trasmette l'evento DBT \_ devnode \_ Changed Device quando un dispositivo è stato aggiunto o rimosso dal sistema. Le applicazioni che gestiscono elenchi di dispositivi nel sistema devono aggiornare gli elenchi.
ms.assetid: 62acc633-7dad-4792-a5a2-1f95356479d1
title: Evento DBT_DEVNODES_CHANGED (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1450e9a87d541e5df3d9a9286e48601697e6aaae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126789"
---
# <a name="dbt_devnodes_changed-event"></a>\_Evento di modifica devnode di DBT \_

Il sistema trasmette l'evento DBT \_ devnode \_ Changed Device quando un dispositivo è stato aggiunto o rimosso dal sistema. Le applicazioni che gestiscono elenchi di dispositivi nel sistema devono aggiornare gli elenchi.

Per trasmettere questo evento del dispositivo, il sistema usa il messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) con *wParam* impostato su DBT \_ devnode \_ modificato e *lParam* impostato su zero.


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

Impostare su DBT \_ devnode \_ modificato.

</dd> <dt>

*lParam* 
</dt> <dd>

Imposta su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true**.

## <a name="remarks"></a>Commenti

Non sono disponibili informazioni aggiuntive sul dispositivo che è stato aggiunto o rimosso dal sistema. Le applicazioni che richiedono altre informazioni devono registrarsi per la notifica del dispositivo tramite la funzione [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) .

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

[**SVILUPPO \_ broadcast \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[**\_DEVICECHANGE WM**](wm-devicechange.md)
</dt> </dl>

 

 




