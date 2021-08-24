---
description: Il sistema trasmette l'evento del dispositivo DBT QUERYCHANGECONFIG per richiedere l'autorizzazione per modificare la \_ configurazione corrente (ancoramento o disanco). Qualsiasi applicazione può negare questa richiesta e annullare la modifica.
ms.assetid: 2e452ea7-e2bf-4500-952a-ee7d891533a0
title: DBT_QUERYCHANGECONFIG evento (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e9c222fdc29f635263b45b5fd7e54ee229a33d7dee1ff31cd1e3072bfe6e84f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318421"
---
# <a name="dbt_querychangeconfig-event"></a>Evento DBT \_ QUERYCHANGECONFIG

Il sistema trasmette l'evento del dispositivo DBT QUERYCHANGECONFIG per richiedere l'autorizzazione per modificare la \_ configurazione corrente (ancoramento o disanco). Qualsiasi applicazione può negare questa richiesta e annullare la modifica.

Per trasmettere questo evento del dispositivo, il sistema usa il messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) con *wParam* impostato su DBT \_ QUERYCHANGECONFIG e *lParam* impostato su zero.


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

Impostare su DBT \_ QUERYCHANGECONFIG.

</dd> <dt>

*lParam* 
</dt> <dd>

Imposta su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituire **TRUE per** concedere l'autorizzazione per modificare la configurazione.

Restituisce BROADCAST \_ QUERY DENY per negare \_ l'autorizzazione per modificare la configurazione.

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

 

 




