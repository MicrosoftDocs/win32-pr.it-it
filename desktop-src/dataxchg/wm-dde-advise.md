---
title: WM_DDE_ADVISE messaggio (Dde.h)
description: Un'applicazione client Dynamic Data Exchange (DDE) invia il messaggio WM DDE ADVISE a un'applicazione server DDE per richiedere al server di fornire un aggiornamento per un elemento di dati ogni volta che l'elemento \_ \_ viene modificato.
ms.assetid: b00db740-36a7-4487-abbf-d74b12f5212a
keywords:
- WM_DDE_ADVISE messaggio Data Exchange
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
ms.openlocfilehash: c651144b4f09cf53f07c0f1860625cab8277e5c8a9532ee864b9ec1b1c927323
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636221"
---
# <a name="wm_dde_advise-message"></a>Messaggio WM \_ DDE \_ ADVISE

Un'applicazione client Dynamic Data Exchange (DDE) invia il messaggio **WM \_ DDE \_ ADVISE** a un'applicazione server DDE per richiedere al server di fornire un aggiornamento per un elemento di dati ogni volta che l'elemento viene modificato.

Per pubblicare questo messaggio, chiamare [**la funzione PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con i parametri seguenti.


```C++
#define WM_DDE_ADVISE      0x03E2
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra client che pubblica il messaggio.

</dd> <dt>

*lParam* 
</dt> <dd>

La parola di ordine più basso è un handle per un oggetto memoria globale contenente una [**struttura DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise) che specifica come devono essere inviati i dati.

La parola di ordine elevato contiene un atom che identifica l'elemento di dati richiesto.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se un'applicazione client supporta più di un formato degli Appunti per un singolo argomento ed elemento, può pubblicare più messaggi **WM \_ DDE \_ ADVISE** per l'argomento e l'elemento, specificando un formato diverso per gli Appunti con ogni messaggio. Si noti che un server può supportare più formati solo per i collegamenti dati ad accesso remoto, non per i collegamenti dati ad accesso più caldo.

### <a name="posting"></a>Distacco

L'applicazione client pubblica **il messaggio ADVISE di WM \_ DDE \_** chiamando la funzione [**PostMessage,**](/windows/desktop/api/winuser/nf-winuser-postmessagea) non la [**funzione SendMessage.**](/windows/desktop/api/winuser/nf-winuser-sendmessage)

L'applicazione client alloca l'oggetto memoria globale usando la [**funzione GlobalAlloc.**](/windows/desktop/api/winbase/nf-winbase-globalalloc) Alloca l'atom usando [**la funzione GlobalAddAtom.**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)

L'applicazione client deve creare o riutilizzare il parametro *lParam* **WM \_ DDE \_ ADVISE** chiamando la funzione [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o [**la funzione ReuseDDElParam.**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)

Se l'applicazione ricevente (server) risponde con un messaggio [**\_ \_ ACK WM DDE**](wm-dde-ack.md) negativo, l'applicazione di pubblicazione deve eliminare l'oggetto.

Il flag **fRelease** non viene usato nei messaggi **WM \_ DDE \_ ADVISE,** ma il relativo comportamento di liberamento dei dati è simile a quello dei messaggi [**WM \_ DDE \_ DATA**](wm-dde-data.md) e [**\_ \_ POKE WM DDE**](wm-dde-poke.md) in cui **fRelease** è **TRUE.**

### <a name="receiving"></a>Ricezione

L'applicazione server pubblica [**il messaggio \_ WM DDE \_ ACK**](wm-dde-ack.md) per rispondere in modo positivo o negativo. Quando si pubblica **WM \_ DDE \_ ACK,** l'applicazione può riutilizzare l'atom o eliminarlo e crearne uno nuovo. Se il **messaggio WM \_ DDE \_ ACK** è positivo, l'applicazione deve eliminare l'oggetto memoria globale. In caso contrario, l'applicazione non deve eliminare l'oggetto.

Il server deve creare o riutilizzare il parametro *lParam* ACK di [**WM \_ DDE \_**](wm-dde-ack.md) chiamando la funzione [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o [**la funzione ReuseDDElParam.**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)

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

[**DisimballareDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[**WM \_ DDE \_ ACK**](wm-dde-ack.md)
</dt> <dt>

[**DATI \_ WM DDE \_**](wm-dde-data.md)
</dt> <dt>

[**WM \_ DDE \_ POKE**](wm-dde-poke.md)
</dt> <dt>

[**RICHIESTA \_ WM DDE \_**](wm-dde-request.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni Dynamic Data Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

