---
title: Messaggio di WM_DDE_TERMINATE (DDE. h)
description: Un'applicazione Dynamic Data Exchange (DDE) (client o server) Invia un \_ \_ messaggio di terminazione DDE WM per terminare una conversazione. Per pubblicare questo messaggio, chiamare la funzione PostMessage con i parametri seguenti.
ms.assetid: 4fc162c0-ccc2-44e3-9c07-d49d7426af8b
keywords:
- Scambio di dati del messaggio WM_DDE_TERMINATE
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
ms.openlocfilehash: 105b4a7daab87b1311a58a7b5e5805bbd81e73ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119519"
---
# <a name="wm_dde_terminate-message"></a>\_Messaggio di \_ terminazione DDE WM

Un'applicazione Dynamic Data Exchange (DDE) (client o server) Invia un messaggio di **\_ \_ terminazione DDE WM** per terminare una conversazione.

Per pubblicare questo messaggio, chiamare la funzione [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con i parametri seguenti.


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

Durante l'attesa della conferma della chiusura, l'applicazione di pubblicazione non deve inviare altri messaggi all'applicazione ricevente. Se l'applicazione mittente riceve messaggi (diversi da **WM \_ DDE \_ Terminate**) dall'applicazione ricevente, deve eliminare tutti gli oggetti di memoria condivisa o gli atomi che accompagnano i messaggi, ad eccezione degli oggetti memoria globale associati ai messaggi di [**\_ \_ dati DDE**](wm-dde-data.md) di [**WM o WM DDE per \_ \_**](wm-dde-poke.md) i quali non è impostato il membro **fRelease** .

### <a name="receiving"></a>Ricezione

È necessario che l'applicazione client o server risponda inviando un messaggio di **\_ \_ terminazione DDE WM** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                 |
| Intestazione<br/>                   | <dl> <dt>DDE. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**\_dati DDE di WM \_**](wm-dde-data.md)
</dt> <dt>

[**\_poke DDE \_ WM**](wm-dde-poke.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni su Dynamic Data Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

