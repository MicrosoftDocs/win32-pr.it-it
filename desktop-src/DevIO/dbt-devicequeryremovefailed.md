---
description: Il sistema trasmette l'evento DBT \_ DEVICEQUERYREMOVEFAILED Device quando una richiesta di rimozione di un dispositivo o di un elemento multimediale è stata annullata.
ms.assetid: a24916a9-b67a-4622-b9f3-4b4f26bf4d6b
title: Evento DBT_DEVICEQUERYREMOVEFAILED (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 848c7378cdbac95729eee70c70a1e323373b8e85
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877754"
---
# <a name="dbt_devicequeryremovefailed-event"></a>\_Evento DEVICEQUERYREMOVEFAILED DBT

Il sistema trasmette l'evento DBT \_ DEVICEQUERYREMOVEFAILED Device quando una richiesta di rimozione di un dispositivo o di un elemento multimediale è stata annullata.

Per trasmettere questo evento del dispositivo, il sistema usa il messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) con *wParam* impostato su DBT \_ DEVICEQUERYREMOVEFAILED e *lParam* impostati come descritto di seguito.


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

Impostare su DBT \_ DEVICEQUERYREMOVEFAILED.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura che identifica il dispositivo. La struttura è costituita da un'intestazione indipendente dall'evento, seguita da membri dipendenti dall'evento che descrivono il dispositivo. Per usare questa struttura, considerare la struttura come una [**struttura \_ \_ HDR di sviluppo broadcast**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) , quindi controllare il membro **dbch \_ DeviceType** per determinare il tipo di dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true**.

## <a name="examples"></a>Esempio

Per un esempio, vedere [elaborazione di una richiesta di rimozione di un dispositivo](processing-a-request-to-remove-a-device.md).

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

 

 




