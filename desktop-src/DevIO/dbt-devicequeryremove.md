---
description: Il sistema trasmette l'evento del \_ dispositivo DEVICEQUERYREMOVE di DBT per richiedere l'autorizzazione per rimuovere un dispositivo o un elemento multimediale.
ms.assetid: a0e9aa57-da0e-4e9c-99d0-5502040d2664
title: Evento DBT_DEVICEQUERYREMOVE (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8c9dbdee13318f9a664582fdba8f9e3f9bfc5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304853"
---
# <a name="dbt_devicequeryremove-event"></a>\_Evento DEVICEQUERYREMOVE DBT

Il sistema trasmette l'evento del \_ dispositivo DEVICEQUERYREMOVE di DBT per richiedere l'autorizzazione per rimuovere un dispositivo o un elemento multimediale. Questo messaggio è l'ultima possibilità per le applicazioni e i driver di prepararsi per la rimozione. Tuttavia, qualsiasi applicazione può negare questa richiesta e annullare l'operazione.

Per trasmettere questo evento del dispositivo, il sistema usa il messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) con *wParam* impostato su DBT \_ DEVICEQUERYREMOVE e *lParam* impostati come descritto di seguito.


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

Impostare su DBT \_ DEVICEQUERYREMOVE.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura che identifica il dispositivo da rimuovere. La struttura è costituita da un'intestazione indipendente dall'evento, seguita da membri dipendenti dall'evento che descrivono il dispositivo. Per usare questa struttura, considerare la struttura come una [**struttura \_ \_ HDR di sviluppo broadcast**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) , quindi controllare il membro **dbch \_ DeviceType** per determinare il tipo di dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** per concedere l'autorizzazione per la rimozione di un dispositivo.

Return BROADCAST \_ query \_ Nega per negare l'autorizzazione per rimuovere un dispositivo.

## <a name="remarks"></a>Commenti

È necessario chiudere tutti gli handle del dispositivo o la rimozione del dispositivo non riuscirà.

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

 

 




