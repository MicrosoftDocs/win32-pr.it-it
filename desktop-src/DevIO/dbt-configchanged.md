---
description: Il sistema trasmette l'evento DBT \_ CONFIGCHANGED Device per indicare che la configurazione corrente è cambiata a causa di un ancoraggio o di Undock. Un'applicazione o un driver che archivia i dati nel registro di sistema sotto la \_ chiave di configurazione HKEY corrente \_ dovrebbe aggiornare i dati.
ms.assetid: e5e33970-b17e-4723-98aa-e242f90fe4e7
title: Evento DBT_CONFIGCHANGED (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d242832378ba9ca3d3006965719942aa41ecff93
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225646"
---
# <a name="dbt_configchanged-event"></a>\_Evento CONFIGCHANGED DBT

Il sistema trasmette l'evento DBT \_ CONFIGCHANGED Device per indicare che la configurazione corrente è cambiata a causa di un ancoraggio o di Undock. Un'applicazione o un driver che archivia i dati nel registro di sistema sotto la \_ chiave di configurazione HKEY corrente \_ dovrebbe aggiornare i dati.

Per trasmettere questo evento del dispositivo, il sistema usa il messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) con *wParam* impostato su DBT \_ CONFIGCHANGED e *lParam* impostati su zero.


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

Impostare su DBT \_ CONFIGCHANGED.

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

 

 




