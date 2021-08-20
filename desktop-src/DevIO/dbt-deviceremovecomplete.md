---
description: Il sistema trasmette l'evento del dispositivo DBT DEVICEREMOVECOMPLETE quando un dispositivo o un elemento \_ multimediale è stato rimosso fisicamente.
ms.assetid: e25d35b9-f8f1-4850-996c-e1cb393cca66
title: DBT_DEVICEREMOVECOMPLETE evento (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5998742d823d710bfb91cd10579a3fb1ec65bec42b615fc7fdac3ac35545b24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539191"
---
# <a name="dbt_deviceremovecomplete-event"></a>EVENTO DBT \_ DEVICEREMOVECOMPLETE

Il sistema trasmette l'evento del dispositivo DBT DEVICEREMOVECOMPLETE quando un dispositivo o un elemento \_ multimediale è stato rimosso fisicamente.

Per trasmettere questo evento del dispositivo, il sistema usa il messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) con *wParam* impostato su DBT \_ DEVICEREMOVECOMPLETE e *lParam* impostato come descritto di seguito.


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

Impostare su DBT \_ DEVICEREMOVECOMPLETE

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura che identifica il dispositivo rimosso. La struttura è costituita da un'intestazione indipendente dagli eventi, seguita da membri dipendenti dall'evento che descrivono il dispositivo. Per usare questa struttura, considerare la struttura come una struttura [**DEV \_ BROADCAST \_ HDR,**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) quindi controllare il relativo membro **dbch \_ devicetype** per determinare il tipo di dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE.**

## <a name="remarks"></a>Commenti

Il sistema può trasmettere un messaggio DBT DEVICEREMOVECOMPLETE senza inviare i messaggi \_ [ \_ DBT DEVICEQUERYREMOVE](dbt-devicequeryremove.md) e [ \_ DBT DEVICEREMOVEPENDING](dbt-deviceremovepending.md) corrispondenti. In questi casi, le applicazioni e i driver devono eseguire il ripristino dalla perdita del dispositivo nel modo migliore possibile.

Se il supporto viene rimosso, il tipo di dispositivo in arrivo è un volume (il membro **\_ dbch devicetype** è DBT DEVTYP VOLUME) e la modifica ha effetto sul supporto (il membro dei flag \_ \_ **dbcv \_** è DBTF \_ MEDIA).

## <a name="examples"></a>Esempio

Per un esempio, vedere [Detecting Media Insertion or Removal](detecting-media-insertion-or-removal.md) or Processing a Request to Remove a [Device](processing-a-request-to-remove-a-device.md).

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

 

 




