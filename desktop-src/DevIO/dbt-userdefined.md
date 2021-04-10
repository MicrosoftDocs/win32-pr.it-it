---
description: L' \_ evento DBT USERDEFINED Device identifica un evento definito dall'utente.
ms.assetid: b42feda9-5fe7-4e54-aad9-28c61d2f29b6
title: Evento DBT_USERDEFINED (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d57ed3ebb801da4ae1ed7a7964cb7aac4f411a35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049187"
---
# <a name="dbt_userdefined-event"></a>\_Evento USERDEFINED DBT

L' \_ evento DBT USERDEFINED Device identifica un evento definito dall'utente.

Per trasmettere questo evento del dispositivo, chiamare la funzione [**BroadcastSystemMessage**](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage) con il messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) . Impostare *wParam* su DBT \_ USERDEFINED e impostare *lParam* come descritto di seguito.


```C++
LRESULT CALLBACK WindowProc( HWND   hwnd,     // handle to window
                             UINT   uMsg,     // WM_DEVICECHANGE
                             WPARAM wParam,   // DBT_USERDEFINED
                             LPARAM lParam ); // event-specific data
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

Impostare su DBT \_ USERDEFINED.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**\_ \_ \_ USERDEFINED di sviluppo broadcast**](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined) che descrive la trasmissione definita dall'utente in corso. Il membro **dbud \_ szName** contiene il nome del messaggio definito dall'utente, seguito da tutti i dati definiti dall'utente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true**.

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

[**\_\_USERDEFINED broadcast \_ dev**](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined)
</dt> <dt>

[**\_DEVICECHANGE WM**](wm-devicechange.md)
</dt> <dt>

[**BroadcastSystemMessage**](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage)
</dt> </dl>

 

