---
description: Il sistema invia l'evento del dispositivo DBT CUSTOMEVENT quando si verifica un evento \_ personalizzato definito dal driver.
ms.assetid: 6e66fa93-0cd7-4202-83eb-cddc668525ae
title: DBT_CUSTOMEVENT evento (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75ec02262e4cf49a7b929f738acce94822aaf67a397a37d6237f4faa57ef7f1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109041"
---
# <a name="dbt_customevent-event"></a>Evento DBT \_ CUSTOMEVENT

Il sistema invia l'evento del dispositivo DBT CUSTOMEVENT quando si verifica un evento \_ personalizzato definito dal driver.

Per trasmettere questo evento del dispositivo, il sistema usa il messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) con *wParam* impostato su DBT CUSTOMEVENT e \_ *lParam* impostato come descritto di seguito.


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

Impostare su DBT \_ CUSTOMEVENT.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura che identifica il dispositivo. La struttura è costituita da un'intestazione indipendente dagli eventi, seguita da membri dipendenti dall'evento che descrivono il dispositivo. Per usare questa struttura, considerare la struttura come una struttura [**DEV \_ BROADCAST \_ HDR,**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) quindi controllare il relativo membro **dbch \_ devicetype** per determinare il tipo di dispositivo.

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

[**DEV \_ BROADCAST \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[**WM \_ DEVICECHANGE**](wm-devicechange.md)
</dt> </dl>

 

 




