---
description: Il sistema trasmette l'evento del dispositivo DBT \_ DEVICETYPESPECIFIC quando si verifica un evento specifico del dispositivo.
ms.assetid: 5d68e29d-b4d7-46f4-a35e-1db286e944ca
title: DBT_DEVICETYPESPECIFIC evento (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd8fb403568cef55741a8c206929d9105284f5191c547500fd79ff39f6b01f1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109031"
---
# <a name="dbt_devicetypespecific-event"></a>EVENTO DBT \_ DEVICETYPESPECIFIC

Il sistema trasmette l'evento del dispositivo DBT \_ DEVICETYPESPECIFIC quando si verifica un evento specifico del dispositivo.

Per trasmettere questo evento del dispositivo, il sistema usa il messaggio [**\_ DEVICECHANGE WM**](wm-devicechange.md) con *wParam* impostato su DBT \_ DEVICETYPESPECIFIC e *lParam* impostato come descritto di seguito.


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

Impostare su DBT \_ DEVICETYPESPECIFIC.

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

 

 




