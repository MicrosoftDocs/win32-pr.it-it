---
description: Il sistema trasmette l'evento del dispositivo DBT CONFIGCHANGECANCELED quando una richiesta di modifica della configurazione corrente \_ (ancoramento o annullamento) è stata annullata.
ms.assetid: b4b1455c-9a04-4fa0-a3fa-ed991f278c0c
title: DBT_CONFIGCHANGECANCELED evento (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 624144ccd5a87d983d453c8d6a3c0667376c2a1b9340bba83f229a29882bffe4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874541"
---
# <a name="dbt_configchangecanceled-event"></a>Evento DBT \_ CONFIGCHANGECANCELED

Il sistema trasmette l'evento del dispositivo DBT CONFIGCHANGECANCELED quando una richiesta di modifica della configurazione corrente \_ (ancoramento o annullamento) è stata annullata.

Per trasmettere questo evento del dispositivo, il sistema usa il messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) con *wParam* impostato su DBT \_ CONFIGCHANGECANCELED e *lParam* impostato su zero.


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

Impostare su DBT \_ CONFIGCHANGECANCELED.

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

 

 




