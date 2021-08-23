---
description: Il sistema trasmette l'evento del dispositivo DBT DEVICEQUERYREMOVEFAILED quando una richiesta di rimozione di un dispositivo o di un elemento multimediale \_ è stata annullata.
ms.assetid: a24916a9-b67a-4622-b9f3-4b4f26bf4d6b
title: DBT_DEVICEQUERYREMOVEFAILED evento (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 605c2689d7d986b4e85fda6d8ce5f24fa6483641de46a6a84f3e4e96ba473897
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076305"
---
# <a name="dbt_devicequeryremovefailed-event"></a>EVENTO DBT \_ DEVICEQUERYREMOVEFAILED

Il sistema trasmette l'evento del dispositivo DBT DEVICEQUERYREMOVEFAILED quando una richiesta di rimozione di un dispositivo o di un elemento multimediale \_ è stata annullata.

Per trasmettere questo evento del dispositivo, il sistema usa il messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) con *wParam* impostato su DBT \_ DEVICEQUERYREMOVEFAILED e *lParam* impostato come descritto di seguito.


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

Impostare su DBT \_ DEVICEQUERYREMOVEFAILED.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura che identifica il dispositivo. La struttura è costituita da un'intestazione indipendente dagli eventi, seguita da membri dipendenti dall'evento che descrivono il dispositivo. Per usare questa struttura, considerare la struttura come una struttura [**DEV \_ BROADCAST \_ HDR,**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) quindi controllare il relativo membro **dbch \_ devicetype** per determinare il tipo di dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE.**

## <a name="examples"></a>Esempio

Per un esempio, vedere [Elaborazione di una richiesta di rimozione di un dispositivo.](processing-a-request-to-remove-a-device.md)

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

 

 




