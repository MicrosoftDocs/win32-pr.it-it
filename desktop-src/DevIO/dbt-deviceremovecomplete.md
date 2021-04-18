---
description: Il sistema trasmette l'evento DBT \_ DEVICEREMOVECOMPLETE Device quando un dispositivo o un elemento multimediale è stato rimosso fisicamente.
ms.assetid: e25d35b9-f8f1-4850-996c-e1cb393cca66
title: Evento DBT_DEVICEREMOVECOMPLETE (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16c899d8cee4a0be34829ba0a8edbaf27be71f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304852"
---
# <a name="dbt_deviceremovecomplete-event"></a>\_Evento DEVICEREMOVECOMPLETE DBT

Il sistema trasmette l'evento DBT \_ DEVICEREMOVECOMPLETE Device quando un dispositivo o un elemento multimediale è stato rimosso fisicamente.

Per trasmettere questo evento del dispositivo, il sistema usa il messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) con *wParam* impostato su DBT \_ DEVICEREMOVECOMPLETE e *lParam* impostati come descritto di seguito.


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

Imposta su DBT \_ DEVICEREMOVECOMPLETE

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura che identifica la periferica rimossa. La struttura è costituita da un'intestazione indipendente dall'evento, seguita da membri dipendenti dall'evento che descrivono il dispositivo. Per usare questa struttura, considerare la struttura come una [**struttura \_ \_ HDR di sviluppo broadcast**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) , quindi controllare il membro **dbch \_ DeviceType** per determinare il tipo di dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true**.

## <a name="remarks"></a>Commenti

Il sistema può trasmettere un \_ messaggio DBT DEVICEREMOVECOMPLETE senza inviare i messaggi [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) e [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) corrispondenti. In questi casi, le applicazioni e i driver devono essere ripristinati dalla perdita del dispositivo nel modo migliore possibile.

Se è in corso la rimozione del supporto, il tipo di dispositivo in arrivo è un volume (il membro **dbch \_ DeviceType** è DBT \_ DEVTYP \_ volume) e la modifica ha effetto sui supporti (il membro dei **\_ flag dbcv** è DBTF \_ ).

## <a name="examples"></a>Esempio

Per un esempio, vedere [rilevamento dell'inserimento o della rimozione di supporti](detecting-media-insertion-or-removal.md) o [elaborazione di una richiesta di rimozione di un dispositivo](processing-a-request-to-remove-a-device.md).

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

 

 




