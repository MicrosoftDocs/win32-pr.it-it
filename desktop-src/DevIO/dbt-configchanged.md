---
description: Il sistema trasmette l'evento del dispositivo DBT CONFIGCHANGED per indicare che la configurazione corrente è stata modificata a causa di \_ un'ancoraggio o un disanco. Un'applicazione o un driver che archivia i dati nel Registro di sistema nella chiave HKEY \_ CURRENT CONFIG deve aggiornare i \_ dati.
ms.assetid: e5e33970-b17e-4723-98aa-e242f90fe4e7
title: DBT_CONFIGCHANGED evento (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba7e0d93b2a89793bb572a5c7563e54fa3114101443b43b8d6beac7955bdd6ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874517"
---
# <a name="dbt_configchanged-event"></a>Evento DBT \_ CONFIGCHANGED

Il sistema trasmette l'evento del dispositivo DBT CONFIGCHANGED per indicare che la configurazione corrente è stata modificata a causa di \_ un'ancoraggio o un disanco. Un'applicazione o un driver che archivia i dati nel Registro di sistema nella chiave HKEY \_ CURRENT CONFIG deve aggiornare i \_ dati.

Per trasmettere questo evento del dispositivo, il sistema usa il messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) con *wParam* impostato su DBT \_ CONFIGCHANGED e *lParam* impostato su zero.


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

Identificatore [**del messaggio WM \_ DEVICECHANGE.**](wm-devicechange.md)

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

Restituisce **TRUE.**

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

[**WM \_ DEVICECHANGE**](wm-devicechange.md)
</dt> </dl>

 

 




