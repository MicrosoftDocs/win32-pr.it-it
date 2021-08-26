---
description: Il sistema trasmette l'evento del dispositivo DBT DEVICEARRIVAL quando un dispositivo o un elemento multimediale è stato inserito \_ e diventa disponibile.
ms.assetid: 8e44cb02-cf79-4b19-807e-20cea07362af
title: DBT_DEVICEARRIVAL evento (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 826d0b510ca76b829eb683396c99579c14a512a6773b76a2049ae7963ede54a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088151"
---
# <a name="dbt_devicearrival-event"></a>EVENTO DBT \_ DEVICEARRIVAL

Il sistema trasmette l'evento del dispositivo DBT DEVICEARRIVAL quando un dispositivo o un elemento multimediale è stato inserito \_ e diventa disponibile.

Per trasmettere questo evento del dispositivo, il sistema usa il messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) con *wParam* impostato su DBT \_ DEVICEARRIVAL e *lParam* impostato come descritto di seguito.


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

Impostare su DBT \_ DEVICEARRIVAL.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura che identifica il dispositivo inserito. La struttura è costituita da un'intestazione indipendente dagli eventi, seguita da membri dipendenti dall'evento che descrivono il dispositivo. Per usare questa struttura, considerare la struttura come una struttura [**DEV \_ BROADCAST \_ HDR,**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) quindi controllare il relativo membro **dbch \_ devicetype** per determinare il tipo di dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE.**

## <a name="remarks"></a>Commenti

Se vengono inseriti supporti, il tipo di dispositivo in arrivo è un volume (il membro **\_ dbch devicetype** è DBT DEVTYP VOLUME) e la modifica ha effetto sul supporto (il membro dei flag \_ \_ **dbcv \_** è DBTF \_ MEDIA).

## <a name="examples"></a>Esempio

Per un esempio, vedere [Rilevamento dell'inserimento o della rimozione di supporti.](detecting-media-insertion-or-removal.md)

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

 

 




