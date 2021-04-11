---
title: Messaggio di WM_DDE_ADVISE (DDE. h)
description: Un'applicazione client di Dynamic Data Exchange (DDE) Invia il \_ \_ messaggio di notifica DDE di WM a un'applicazione server DDE per richiedere al server di fornire un aggiornamento per un elemento di dati ogni volta che l'elemento viene modificato.
ms.assetid: b00db740-36a7-4487-abbf-d74b12f5212a
keywords:
- Scambio di dati del messaggio WM_DDE_ADVISE
topic_type:
- apiref
api_name:
- WM_DDE_ADVISE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 832c6991169b71955c0ab21b59d2b55b0b54fc9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119623"
---
# <a name="wm_dde_advise-message"></a>\_Messaggio di avviso DDE di WM \_

Un'applicazione client di Dynamic Data Exchange (DDE) Invia il messaggio di **\_ \_ notifica DDE di WM** a un'applicazione server DDE per richiedere al server di fornire un aggiornamento per un elemento di dati ogni volta che l'elemento viene modificato.

Per pubblicare questo messaggio, chiamare la funzione [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con i parametri seguenti.


```C++
#define WM_DDE_ADVISE      0x03E2
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra client che invia il messaggio.

</dd> <dt>

*lParam* 
</dt> <dd>

La parola di ordine inferiore è un handle per un oggetto memoria globale contenente una struttura [**DDEAdvise**](/windows/desktop/api/Dde/ns-dde-ddeadvise) che specifica la modalità di invio dei dati.

La parola più ordinata contiene un Atom che identifica l'elemento di dati richiesto.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se un'applicazione client supporta più di un formato degli Appunti per un singolo argomento ed elemento, può inserire più messaggi di **\_ \_ notifica DDE di WM** per l'argomento e l'elemento, specificando un formato degli Appunti diverso a ogni messaggio. Si noti che un server può supportare più formati solo per i collegamenti dati ad accesso frequente, non per i collegamenti dati caldi.

### <a name="posting"></a>Distacco

L'applicazione client invia il messaggio di **\_ \_ notifica DDE di WM** chiamando la funzione [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) , non la funzione [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) .

L'applicazione client alloca l'oggetto memoria globale usando la funzione [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) . Alloca il Atom usando la funzione [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .

L'applicazione client deve creare o riutilizzare il parametro *lParam* del **\_ \_ Consiglio DDE di WM** chiamando la funzione [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .

Se l'applicazione ricevente (Server) risponde con un messaggio [**di \_ \_ ACK DDE di WM**](wm-dde-ack.md) negativo, l'applicazione di pubblicazione deve eliminare l'oggetto.

Il flag **fRelease** non viene usato nei messaggi di **\_ \_ notifica DDE di WM** , ma il comportamento di liberazione dei dati è simile a quello dei [**\_ \_ dati DDE**](wm-dde-data.md) di WM e dei messaggi [**\_ \_ poke DDE di WM**](wm-dde-poke.md) in cui **fRelease** è **true**.

### <a name="receiving"></a>Ricezione

L'applicazione server inserisce il [**messaggio \_ \_ ACK DDE di WM**](wm-dde-ack.md) per rispondere in modo positivo o negativo. Quando si invia un **\_ \_ ACK DDE di WM**, l'applicazione può riutilizzare l'Atom o eliminarlo e crearne uno nuovo. Se il **messaggio \_ \_ ACK DDE WM** è positivo, l'applicazione deve eliminare l'oggetto memoria globale; in caso contrario, l'applicazione non deve eliminare l'oggetto.

Il server deve creare o riutilizzare il parametro *lParam* del [**\_ \_ ACK DDE WM**](wm-dde-ack.md) chiamando la funzione [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .

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

[**DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise)
</dt> <dt>

[**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam)
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

[**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[**\_ACK DDE \_ WM**](wm-dde-ack.md)
</dt> <dt>

[**\_dati DDE di WM \_**](wm-dde-data.md)
</dt> <dt>

[**\_poke DDE \_ WM**](wm-dde-poke.md)
</dt> <dt>

[**\_richiesta DDE \_ WM**](wm-dde-request.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni su Dynamic Data Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

