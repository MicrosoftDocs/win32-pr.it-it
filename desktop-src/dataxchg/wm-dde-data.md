---
title: Messaggio di WM_DDE_DATA (DDE. h)
description: Un'applicazione server Dynamic Data Exchange (DDE) Invia un \_ messaggio di \_ dati DDE WM a un'applicazione client DDE per passare un elemento dati al client o per notificare al client la disponibilità di un elemento di dati.
ms.assetid: ed6a65d3-b2a3-45f2-9600-291ce2ec8c0a
keywords:
- Scambio di dati del messaggio WM_DDE_DATA
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
ms.openlocfilehash: 9f045ff07e01023e6535eb00dcb78400e4c9519a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301493"
---
# <a name="wm_dde_data-message"></a>\_ \_ Messaggio dati DDE WM

Un'applicazione server Dynamic Data Exchange (DDE) Invia un messaggio di **\_ \_ dati DDE WM** a un'applicazione client DDE per passare un elemento dati al client o per notificare al client la disponibilità di un elemento di dati.

Per pubblicare questo messaggio, chiamare la funzione [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con i parametri seguenti.


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

La parola di ordine inferiore è un handle per un oggetto memoria globale contenente una struttura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) con i dati e informazioni aggiuntive. L'handle deve essere impostato su **null** se il server invia una notifica al client che il valore dell'elemento di dati è stato modificato durante un collegamento dati caldo. Un collegamento a caldo viene stabilito dal client che invia un messaggio di [**\_ \_ notifica DDE di WM**](wm-dde-advise.md) con il set di bit **FDeferUpd** .

La parola più significativa contiene un atomo che identifica l'elemento di dati per il quale vengono inviati i dati o la notifica.

</dd> </dl>

## <a name="remarks"></a>Commenti

### <a name="posting"></a>Distacco

L'applicazione server alloca l'oggetto memoria globale mediante la funzione [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) . Alloca il Atom usando la funzione [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .

Il server deve creare o riutilizzare il parametro *lParam* **\_ \_ dei dati DDE di WM** chiamando la funzione [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .

Se l'applicazione ricevente (client) risponde con un messaggio [**\_ \_ ACK DDE**](wm-dde-ack.md) negativo, l'applicazione di invio (Server) deve eliminare l'oggetto memoria globale. in caso contrario, il client deve eliminare l'oggetto dopo aver estratto il contenuto chiamando la funzione [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) .

Se l'applicazione server imposta il membro **fRelease** della struttura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) su **false**, il server è responsabile dell'eliminazione dell'oggetto in caso di ricezione di un riconoscimento positivo o negativo.

L'applicazione server non deve impostare i membri **fAckReq** e **FRelease** della struttura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) su **false**. Se entrambi i membri sono impostati su **false**, è impossibile per il server determinare quando eliminare l'oggetto.

### <a name="receiving"></a>Ricezione

Se **fAckReq** è **true**, l'applicazione client deve pubblicare il [**messaggio \_ \_ ACK DDE di WM**](wm-dde-ack.md) per rispondere in modo positivo o negativo. Quando si invia un **\_ \_ ACK DDE di WM**, il client può riutilizzare il formato Atom oppure può eliminarlo e crearne uno nuovo.

Il client deve creare o riutilizzare il parametro *lParam* del [**\_ \_ ACK DDE WM**](wm-dde-ack.md) chiamando la funzione [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .

Se **fAckReq** è **false**, l'applicazione client deve eliminare il formato Atom.

Se l'applicazione di invio ha specificato l'oggetto memoria globale come **null**, l'applicazione ricevente può richiedere al server di inviare i dati pubblicando un messaggio di [**\_ \_ richiesta DDE di WM**](wm-dde-request.md) .

Dopo l'elaborazione di un messaggio di **\_ \_ dati DDE di WM** in cui l'oggetto memoria globale non è **null**, il client deve liberare l'oggetto, a meno che non si verifica una delle condizioni seguenti:

-   Il membro **fRelease** è **false**.
-   Il membro **fRelease** è **true**, ma l'applicazione client risponde con un messaggio [**\_ \_ ACK DDE di WM**](wm-dde-ack.md) negativo.

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

[**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[**\_ACK DDE \_ WM**](wm-dde-ack.md)
</dt> <dt>

[**\_avviso DDE di WM \_**](wm-dde-advise.md)
</dt> <dt>

[**\_poke DDE \_ WM**](wm-dde-poke.md)
</dt> <dt>

[**\_richiesta DDE \_ WM**](wm-dde-request.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni su Dynamic Data Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

