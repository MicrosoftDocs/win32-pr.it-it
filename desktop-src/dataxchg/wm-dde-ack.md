---
title: WM_DDE_ACK messaggio (Dde.h)
description: Il messaggio WM DDE ACK notifica a un'applicazione Dynamic Data Exchange (DDE) la ricezione e l'elaborazione dei messaggi \_ \_ SEGUENTI WM \_ \_ DDE POKE, WM \_ DDE \_ EXECUTE, WM \_ DDE \_ DATA, WM \_ DDE \_ ADVISE, WM \_ DDE \_ UNADVISE, WM \_ DDE \_ INITIATE o WM \_ DDE \_ REQUEST (in alcuni casi). Per pubblicare questo messaggio, chiamare la funzione PostMessage con i parametri seguenti.
ms.assetid: aca47dbf-e1f2-4725-8364-0aa7fcd98bd9
keywords:
- WM_DDE_ACK messaggio Dati Exchange
topic_type:
- apiref
api_name:
- WM_DDE_ACK
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1aad39115e1bdb68208a9ccbb0d83eea934ef2ff8c6521a0602e081c7ed811
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636241"
---
# <a name="wm_dde_ack-message"></a>Messaggio WM \_ DDE \_ ACK

Il messaggio **WM \_ DDE \_ ACK** notifica a un'applicazione Dynamic Data Exchange (DDE) la ricezione e l'elaborazione dei messaggi seguenti: [**WM \_ DDE \_ POKE,**](wm-dde-poke.md) [**WM \_ DDE \_ EXECUTE,**](wm-dde-execute.md) [**WM \_ DDE \_ DATA,**](wm-dde-data.md) [**WM \_ DDE \_ ADVISE,**](wm-dde-advise.md) [**WM \_ DDE \_ UNADVISE,**](wm-dde-unadvise.md) [**WM \_ DDE \_ INITIATE**](wm-dde-initiate.md)o [**WM \_ DDE \_ REQUEST**](wm-dde-request.md) (in alcuni casi).

Per pubblicare questo messaggio, chiamare la [**funzione PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con i parametri seguenti.


```C++
#define WM_DDE_ACK     0x03E4
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Quando si risponde a [**WM \_ DDE \_ INITIATE,**](wm-dde-initiate.md)questo parametro è un handle alla finestra del server che invia il messaggio.

Quando si risponde a [**WM \_ DDE \_ EXECUTE,**](wm-dde-execute.md)questo parametro è un handle per la finestra del server che pubblica il messaggio.

Quando si risponde a tutti gli altri messaggi, questo parametro è un handle per la finestra del client o del server che pubblica il messaggio.

</dd> <dt>

*lParam* 
</dt> <dd>

Quando si risponde a [**WM \_ DDE \_ INITIATE,**](wm-dde-initiate.md)la parola di ordine basso contiene un atom che identifica l'applicazione di risposta. La parola di ordine elevato contiene un atomo che identifica l'argomento per cui viene stabilita una conversazione.

Quando si risponde a [**WM \_ DDE \_ EXECUTE,**](wm-dde-execute.md)la parola di ordine basso specifica una struttura [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) contenente una serie di flag che indicano lo stato della risposta. La parola di ordine elevato è un handle per un oggetto di memoria globale che contiene la stringa di comando ricevuta nel messaggio **WM \_ DDE \_ EXECUTE.**

Quando si risponde a tutti gli altri messaggi, la parola di ordine basso specifica una struttura [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) contenente una serie di flag che indicano lo stato della risposta. La parola di ordine superiore contiene un atom globale che identifica il nome dell'elemento di dati per cui viene inviata la risposta.

</dd> </dl>

## <a name="remarks"></a>Commenti

### <a name="posting"></a>Distacco

Tranne in risposta al messaggio [**WM \_ DDE \_ INITIATE,**](wm-dde-initiate.md) l'applicazione invia il messaggio **WM \_ DDE \_ ACK** chiamando la funzione [**PostMessage,**](/windows/desktop/api/winuser/nf-winuser-postmessagea) non chiamando la [**funzione SendMessage.**](/windows/desktop/api/winuser/nf-winuser-sendmessage) Quando si risponde a **WM \_ DDE \_ INITIATE,** l'applicazione invia il **messaggio WM \_ DDE \_ ACK** chiamando **SendMessage**. In questo caso, né l'atom del nome dell'applicazione né l'atom del nome dell'argomento devono essere **NULL** (anche se il messaggio **WM \_ DDE \_ INITIATE** ha specificato **atomi NULL).**

Quando si riconosce un messaggio con un atom associato, l'applicazione che pubblica **WM \_ DDE \_ ACK** può riutilizzare l'atomo che accompagna il messaggio originale oppure può eliminarlo e crearne uno nuovo.

Quando si riconosce [**WM \_ DDE \_ EXECUTE,**](wm-dde-execute.md)l'applicazione che invia **WM \_ DDE \_ ACK** deve riutilizzare l'oggetto memoria globale identificato nel messaggio **EXECUTE WM \_ DDE \_** originale.

Tutti i **messaggi WM \_ DDE \_ ACK** inviati devono creare o riutilizzare il parametro *lParam* chiamando la funzione [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o [**la funzione ReuseDDElParam.**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)

Se un'applicazione ha avviato la terminazione di una conversazione pubblicando [**WM \_ DDE \_ TERMINATE**](wm-dde-terminate.md) ed è in attesa di conferma, l'applicazione in attesa non deve riconoscere (in modo positivo o negativo) eventuali messaggi successivi inviati dall'altra applicazione. L'applicazione in attesa deve eliminare tutti gli atomi o gli oggetti di memoria condivisa ricevuti in questi messaggi interviene. Gli oggetti di memoria non devono essere liberati se il flag **fRelease** è impostato su **FALSE** nei messaggi [**WM \_ DDE \_ POKE**](wm-dde-poke.md) e [**WM \_ DDE \_ DATA.**](wm-dde-data.md)

### <a name="receiving"></a>Ricezione

L'applicazione che riceve un **messaggio WM \_ DDE \_ ACK** deve eliminare tutti gli atomi che accompagnano il messaggio. Se l'applicazione riceve un **\_ \_ ACK WM DDE** in risposta a un messaggio con un oggetto di memoria globale associato e l'oggetto è stato inviato con i flag **fRelease** impostati su **FALSE,** l'applicazione è responsabile dell'eliminazione dell'oggetto.

Se l'applicazione riceve un messaggio **WM \_ DDE \_ ACK** negativo inviato in risposta a un messaggio [**WM \_ DDE \_ ADVISE,**](wm-dde-advise.md) l'applicazione deve eliminare l'oggetto di memoria globale pubblicato con il messaggio **WM \_ DDE \_ ADVISE** originale. Se l'applicazione riceve un messaggio **WM \_ DDE \_ ACK** negativo inviato in risposta a un messaggio [**WM \_ DDE \_ DATA,**](wm-dde-data.md) [**WM \_ DDE \_ POKE**](wm-dde-poke.md)o [**WM \_ DDE \_ EXECUTE,**](wm-dde-execute.md) l'applicazione deve eliminare l'oggetto di memoria globale inviato con il messaggio **WM \_ DDE \_ DATA**, **WM \_ DDE \_ POKE** o **WM \_ DDE \_ EXECUTE** originale.

L'applicazione che riceve un messaggio **WM \_ DDE \_ ACK** inviato deve liberare il *parametro lParam* usando la [**funzione FreeDDElParam.**](/windows/desktop/api/Dde/nf-dde-freeddelparam)

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

[**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack)
</dt> <dt>

[**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam)
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

[**WM \_ DDE \_ ADVISE**](wm-dde-advise.md)
</dt> <dt>

[**DATI \_ WM DDE \_**](wm-dde-data.md)
</dt> <dt>

[**ESECUZIONE DI WM \_ DDE \_**](wm-dde-execute.md)
</dt> <dt>

[**AVVIO DI WM \_ DDE \_**](wm-dde-initiate.md)
</dt> <dt>

[**WM \_ DDE \_ POKE**](wm-dde-poke.md)
</dt> <dt>

[**RICHIESTA \_ WM DDE \_**](wm-dde-request.md)
</dt> <dt>

[**TERMINAZIONE DI WM \_ DDE \_**](wm-dde-terminate.md)
</dt> <dt>

[**WM \_ DDE \_ UNADE UNADVISE**](wm-dde-unadvise.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni Dynamic Data Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

