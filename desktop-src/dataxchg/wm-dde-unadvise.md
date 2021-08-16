---
title: WM_DDE_UNADVISE messaggio (Dde.h)
description: Un'applicazione client Dynamic Data Exchange (DDE) invia un messaggio WM \_ DDE UNADVISE per informare un'applicazione server DDE che l'elemento specificato o un particolare formato degli Appunti per l'elemento non deve più \_ essere aggiornato.
ms.assetid: 9a5f9a86-e6fa-450e-b8bf-f20042c7e6d1
keywords:
- WM_DDE_UNADVISE messaggio Data Exchange
topic_type:
- apiref
api_name:
- WM_DDE_UNADVISE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bbd0ac8e056cc43be764e745f824b50fc90b3cb2f0c50c9061d111fb3bc178d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117915105"
---
# <a name="wm_dde_unadvise-message"></a>Messaggio WM \_ DDE \_ UNADVISE

Un'applicazione client Dynamic Data Exchange (DDE) invia un messaggio **WM \_ DDE \_ UNADVISE** per informare un'applicazione server DDE che l'elemento specificato o un particolare formato degli Appunti per l'elemento non deve più essere aggiornato. In questo modo viene terminato il collegamento dati ad accesso più caldo per l'elemento specificato.

Per pubblicare questo messaggio, chiamare [**la funzione PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con i parametri seguenti.


```C++
#define WM_DDE_UNADVISE        0x03E3
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle alla finestra client che invia il messaggio.

</dd> <dt>

*lParam* 
</dt> <dd>

La parola di ordine più basso specifica il formato degli Appunti dell'elemento per il quale viene ritirata la richiesta di aggiornamento. Se è **NULL,** tutte le conversazioni [**WM \_ DDE \_ ADVISE**](wm-dde-advise.md) attive per l'elemento devono essere terminate.

La parola più importante contiene un atom globale che identifica l'elemento per il quale viene ritirata la richiesta di aggiornamento. Se è **NULL,** tutti i collegamenti [**WM \_ DDE \_ ADVISE**](wm-dde-advise.md) attivi associati alla conversazione devono essere terminati.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'applicazione client alloca la parola più alta *di lParam* chiamando la [**funzione GlobalAddAtom.**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)

L'applicazione server pubblica [**il messaggio \_ WM DDE \_ ACK**](wm-dde-ack.md) per rispondere in modo positivo o negativo. Quando si **pubblica WM \_ DDE \_ ACK,** il server può riutilizzare l'atom oppure può eliminare l'atom e crearne uno nuovo.

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

[**WM \_ DDE \_ ADVISE**](wm-dde-advise.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni Dynamic Data Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

