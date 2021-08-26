---
description: L'evento del dispositivo DBT \_ USERDEFINED identifica un evento definito dall'utente.
ms.assetid: b42feda9-5fe7-4e54-aad9-28c61d2f29b6
title: DBT_USERDEFINED evento (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49eca726ea9c4336a36f30872ad068e45062a67189192154374d5d5b21e578ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103871"
---
# <a name="dbt_userdefined-event"></a>Evento DBT \_ USERDEFINED

L'evento del dispositivo DBT \_ USERDEFINED identifica un evento definito dall'utente.

Per trasmettere questo evento del dispositivo, chiamare la [**funzione BroadcastSystemMessage**](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage) con il [**messaggio WM \_ DEVICECHANGE.**](wm-devicechange.md) Impostare *wParam su* DBT \_ USERDEFINED e *lParam* come descritto di seguito.


```C++
LRESULT CALLBACK WindowProc( HWND   hwnd,     // handle to window
                             UINT   uMsg,     // WM_DEVICECHANGE
                             WPARAM wParam,   // DBT_USERDEFINED
                             LPARAM lParam ); // event-specific data
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

Impostare su DBT \_ USERDEFINED.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**\_ struttura DEV BROADCAST \_ \_ USERDEFINED**](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined) che descrive la trasmissione definita dall'utente in corso. Il **membro dbud \_ szName** contiene il nome del messaggio definito dall'utente, seguito da tutti i dati definiti dall'utente.

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

[**\_DEV \_ BROADCAST \_ DEFINITO DALL'UTENTE**](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined)
</dt> <dt>

[**WM \_ DEVICECHANGE**](wm-devicechange.md)
</dt> <dt>

[**BroadcastSystemMessage**](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage)
</dt> </dl>

 

