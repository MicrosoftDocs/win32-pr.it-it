---
title: WM_DDE_DATA messaggio (Dde.h)
description: Un'applicazione server Dynamic Data Exchange (DDE) invia un messaggio WM DDE DATA a un'applicazione \_ client DDE per passare un elemento di dati al client o per notificare al client la disponibilità di un elemento \_ dati.
ms.assetid: ed6a65d3-b2a3-45f2-9600-291ce2ec8c0a
keywords:
- WM_DDE_DATA messaggio Dati Exchange
topic_type:
- apiref
api_name:
- WM_DDE_DATA
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0200737a9b25a123954498941ad117e5465f58f5313daa8caf90674751355ed6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736278"
---
# <a name="wm_dde_data-message"></a>Messaggio WM \_ DDE \_ DATA

Un'applicazione server Dynamic Data Exchange (DDE) invia un messaggio **WM \_ DDE \_ DATA** a un'applicazione client DDE per passare un elemento di dati al client o per notificare al client la disponibilità di un elemento dati.

Per pubblicare questo messaggio, chiamare la [**funzione PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con i parametri seguenti.


```C++
#define WM_DDE_DATA        0x03E05
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra del server che pubblica il messaggio.

</dd> <dt>

*lParam* 
</dt> <dd>

La parola di ordine basso è un handle per un oggetto di memoria globale contenente una [**struttura DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) con i dati e informazioni aggiuntive. L'handle deve essere impostato su **NULL** se il server invia una notifica al client che il valore dell'elemento di dati è stato modificato durante un collegamento dati a caldo. Un collegamento a caldo viene stabilito dal client che invia un [**messaggio WM \_ DDE \_ ADVISE**](wm-dde-advise.md) con il bit **fDeferUpd** impostato.

La parola di ordine elevato contiene un atom che identifica l'elemento di dati per cui vengono inviati i dati o la notifica.

</dd> </dl>

## <a name="remarks"></a>Commenti

### <a name="posting"></a>Distacco

L'applicazione server alloca l'oggetto di memoria globale usando la [**funzione GlobalAlloc.**](/windows/desktop/api/winbase/nf-winbase-globalalloc) Alloca l'atom usando [**la funzione GlobalAddAtom.**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)

Il server deve creare o riutilizzare il parametro **WM \_ DDE \_ DATA** *lParam* chiamando la [**funzione PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o [**la funzione ReuseDDElParam.**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)

Se l'applicazione ricevente (client) risponde con un messaggio [**WM \_ DDE \_ ACK**](wm-dde-ack.md) negativo, l'applicazione di pubblicazione (server) deve eliminare l'oggetto memoria globale. In caso contrario, il client deve eliminare l'oggetto dopo averne estratto il contenuto chiamando la funzione [**UnpackDDElParam.**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)

Se l'applicazione server imposta il membro **fRelease** della struttura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) su **FALSE,** il server è responsabile dell'eliminazione dell'oggetto alla ricezione di un riconoscimento positivo o negativo.

L'applicazione server non deve impostare entrambi i **membri fAckReq** e **fRelease** della struttura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) su **FALSE.** Se entrambi i membri sono impostati su **FALSE,** non è possibile per il server determinare quando eliminare l'oggetto.

### <a name="receiving"></a>Ricezione

Se **fAckReq** è **TRUE,** l'applicazione client deve inviare il messaggio [**WM \_ DDE \_ ACK**](wm-dde-ack.md) per rispondere in modo positivo o negativo. Quando si **pubblica WM \_ DDE \_ ACK,** il client può riutilizzare l'atomo oppure eliminarlo e crearne uno nuovo.

Il client deve creare o riutilizzare il parametro [**\_ WM DDE \_ ACK**](wm-dde-ack.md) *lParam* chiamando la [**funzione PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o [**la funzione ReuseDDElParam.**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)

Se **fAckReq** è **FALSE,** l'applicazione client deve eliminare l'atom.

Se l'applicazione di pubblicazione ha specificato l'oggetto di memoria globale **come NULL,** l'applicazione ricevente può richiedere al server di inviare i dati inviando un messaggio [**WM \_ DDE \_ REQUEST.**](wm-dde-request.md)

Dopo l'elaborazione di un messaggio **WM \_ DDE \_ DATA** in cui l'oggetto di memoria globale non è **NULL,** il client deve liberare l'oggetto, a meno che non si verifica una delle condizioni seguenti:

-   Il **membro fRelease** è **FALSE.**
-   Il **membro fRelease** è **TRUE,** ma l'applicazione client risponde con un messaggio [**\_ \_ ACK WM DDE**](wm-dde-ack.md) negativo.

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

[**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata)
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

[**Decomprimere UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[**WM \_ DDE \_ ACK**](wm-dde-ack.md)
</dt> <dt>

[**WM \_ DDE \_ ADVISE**](wm-dde-advise.md)
</dt> <dt>

[**WM \_ DDE \_ POKE**](wm-dde-poke.md)
</dt> <dt>

[**RICHIESTA \_ WM DDE \_**](wm-dde-request.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni Dynamic Data Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

