---
title: WM_DDE_REQUEST messaggio (Dde.h)
description: Un'applicazione client DDE (Dynamic Data Exchange) invia un messaggio WM DDE REQUEST a un'applicazione server DDE per richiedere il valore \_ di un elemento di \_ dati. Per pubblicare questo messaggio, chiamare la funzione PostMessage con i parametri seguenti.
ms.assetid: 922452d2-455c-43e1-a8a8-e3c52b0fab51
keywords:
- WM_DDE_REQUEST messaggio Data Exchange
topic_type:
- apiref
api_name:
- WM_DDE_REQUEST
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05c58877b15f39d2de907688972905e98007658981bcc57df62655634bafe8be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118811351"
---
# <a name="wm_dde_request-message"></a>Messaggio WM \_ DDE \_ REQUEST

Un'applicazione client DDE (Dynamic Data Exchange) invia un messaggio **WM \_ DDE \_ REQUEST** a un'applicazione server DDE per richiedere il valore di un elemento di dati.

Per pubblicare questo messaggio, chiamare [**la funzione PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con i parametri seguenti.


```C++
#define WM_DDE_REQUEST     0x03E6
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle alla finestra client che invia il messaggio.

</dd> <dt>

*lParam* 
</dt> <dd>

La parola meno ordinata specifica un formato degli Appunti standard o registrato.

La parola di ordine elevato contiene un atom che identifica l'elemento di dati richiesto dal server.

</dd> </dl>

## <a name="remarks"></a>Commenti

### <a name="posting"></a>Distacco

L'applicazione client alloca l'atom chiamando la [**funzione GlobalAddAtom.**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)

### <a name="receiving"></a>Ricezione

Se l'applicazione ricevente (server) può soddisfare la richiesta, risponde con un messaggio [**WM \_ DDE \_ DATA**](wm-dde-data.md) contenente i dati richiesti. In caso contrario, risponde con un messaggio [**\_ \_ ACK WM DDE**](wm-dde-ack.md) negativo.

Quando si risponde con un messaggio [**WM \_ DDE \_ DATA**](wm-dde-data.md) o [**WM \_ DDE \_ ACK,**](wm-dde-ack.md) l'applicazione server può riutilizzare l'atom o eliminare l'atom e crearne uno nuovo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                 |
| Intestazione<br/>                   | <dl> <dt>Dde.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**DisimballareDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[**WM \_ DDE \_ ACK**](wm-dde-ack.md)
</dt> <dt>

[**DATI \_ WM DDE \_**](wm-dde-data.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni Dynamic Data Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

