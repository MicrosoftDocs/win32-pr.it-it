---
title: WM_DDE_TERMINATE messaggio (Dde.h)
description: Un'Dynamic Data Exchange (DDE) (client o server) invia un messaggio WM \_ DDE \_ TERMINATE per terminare una conversazione. Per pubblicare questo messaggio, chiamare la funzione PostMessage con i parametri seguenti.
ms.assetid: 4fc162c0-ccc2-44e3-9c07-d49d7426af8b
keywords:
- WM_DDE_TERMINATE messaggio Data Exchange
topic_type:
- apiref
api_name:
- WM_DDE_TERMINATE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a98d9b4bf2120cb6daa08b6088a8dd39f8a17b8e28c37a3917936a9c49230487
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736268"
---
# <a name="wm_dde_terminate-message"></a>Messaggio WM \_ DDE \_ TERMINATE

Un'Dynamic Data Exchange (DDE) (client o server) invia un messaggio **WM \_ DDE \_ TERMINATE** per terminare una conversazione.

Per pubblicare questo messaggio, chiamare [**la funzione PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con i parametri seguenti.


```C++
#define WM_DDE_TERMINATE       0x03E1
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra client o server che pubblica il messaggio.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="remarks"></a>Commenti

### <a name="posting"></a>Distacco

In attesa di conferma della chiusura, l'applicazione di pubblicazione non deve inviare altri messaggi all'applicazione ricevente. Se l'applicazione mittente riceve messaggi (diversi da **WM \_ DDE \_ TERMINATE)** dall'applicazione ricevente, deve eliminare tutti gli atom o gli oggetti di memoria condivisa associati ai messaggi, ad eccezione degli oggetti di memoria globale associati ai messaggi [**WM \_ DDE \_ POKE**](wm-dde-poke.md) o [**WM \_ DDE \_ DATA**](wm-dde-data.md) per cui non è impostato il membro **fRelease.**

### <a name="receiving"></a>Ricezione

L'applicazione client o server deve rispondere pubblicando un **messaggio WM \_ DDE \_ TERMINATE.**

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

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**DATI \_ WM DDE \_**](wm-dde-data.md)
</dt> <dt>

[**WM \_ DDE \_ POKE**](wm-dde-poke.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni Dynamic Data Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

