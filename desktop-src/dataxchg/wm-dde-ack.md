---
title: Messaggio di WM_DDE_ACK (DDE. h)
description: Il \_ \_ messaggio ACK DDE di WM notifica a un'applicazione Dynamic Data Exchange (DDE) la ricezione e l'elaborazione dei seguenti messaggi WM \_ DDE \_ poke, WM \_ DDE \_ Execute, WM \_ DDE \_ data, WM \_ DDE \_ Advise, WM \_ DDE \_ Unadvise, WM \_ DDE \_ Initiation o WM DDE \_ \_ Request (in alcuni casi). Per pubblicare questo messaggio, chiamare la funzione PostMessage con i parametri seguenti.
ms.assetid: aca47dbf-e1f2-4725-8364-0aa7fcd98bd9
keywords:
- Scambio di dati del messaggio WM_DDE_ACK
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
ms.openlocfilehash: a407fc6cad7077586539f119dd65be59a507cacd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048284"
---
# <a name="wm_dde_ack-message"></a>\_ \_ Messaggio ACK DDE WM

Il **messaggio \_ \_ ACK DDE WM** notifica a un'applicazione Dynamic Data Exchange (DDE) la ricezione e l'elaborazione dei messaggi seguenti: [**WM \_ DDE \_ poke**](wm-dde-poke.md), [**WM \_ DDE \_ Execute**](wm-dde-execute.md), [**WM \_ DDE \_ Data**](wm-dde-data.md), [**WM \_ DDE \_ Advise**](wm-dde-advise.md), [**WM \_ DDE \_ Unadvise**](wm-dde-unadvise.md), [**WM \_ DDE \_ Initiation**](wm-dde-initiate.md)o WM DDE [**\_ \_ Request**](wm-dde-request.md) (in alcuni casi).

Per pubblicare questo messaggio, chiamare la funzione [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con i parametri seguenti.


```C++
#define WM_DDE_ACK     0x03E4
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Quando si risponde [**all' \_ \_ avvio di WM DDE**](wm-dde-initiate.md), questo parametro è un handle per la finestra del server che invia il messaggio.

Quando si risponde [**all' \_ \_ esecuzione di WM DDE**](wm-dde-execute.md), questo parametro è un handle per la finestra del server che pubblica il messaggio.

Quando si risponde a tutti gli altri messaggi, questo parametro è un handle per la finestra client o server che pubblica il messaggio.

</dd> <dt>

*lParam* 
</dt> <dd>

Quando si risponde [**all' \_ \_ avvio di WM DDE**](wm-dde-initiate.md), la parola più bassa contiene un atomo che identifica l'applicazione di risposta. La parola più ordinata contiene un atomo che identifica l'argomento per cui viene stabilita una conversazione.

Quando si risponde [**all' \_ \_ esecuzione di WM DDE**](wm-dde-execute.md), la parola più bassa indica una struttura [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) contenente una serie di flag che indicano lo stato della risposta. La parola più ordinata è un handle per un oggetto memoria globale che contiene la stringa di comando ricevuta nel messaggio di **\_ \_ esecuzione DDE di WM** .

Quando si risponde a tutti gli altri messaggi, la parola di ordine inferiore specifica una struttura [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) contenente una serie di flag che indicano lo stato della risposta. La parola più ordinata contiene un Atom globale che identifica il nome dell'elemento di dati per cui viene inviata la risposta.

</dd> </dl>

## <a name="remarks"></a>Commenti

### <a name="posting"></a>Distacco

Tranne che in risposta al messaggio di [**\_ \_ inizializzazione di WM DDE**](wm-dde-initiate.md) , l'applicazione invia il messaggio **\_ \_ ACK DDE di WM** chiamando la funzione [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) , non chiamando la funzione [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) . Quando si risponde **all' \_ \_ avvio di WM DDE**, l'applicazione invia il messaggio **\_ \_ ACK DDE di WM** chiamando **SendMessage**. In questo caso, né il nome dell'applicazione Atom né il nome dell'argomento Atom devono essere **null** (anche se il messaggio di **\_ \_ inizializzazione del DDE di WM** ha specificato atomi **null** ).

Quando si riconosce un messaggio con un Atom associato, l'applicazione che invia **l' \_ \_ ACK DDE WM** può riutilizzare il Atom che ha accompagnato il messaggio originale oppure può eliminarlo e crearne uno nuovo.

Quando si riconosce [**l' \_ \_ esecuzione di WM DDE**](wm-dde-execute.md), l'applicazione che invia **ACK di WM \_ DDE \_** deve riutilizzare l'oggetto memoria globale identificato nel messaggio **\_ \_ Execute DDE** originale di WM.

Tutti i messaggi di **\_ \_ ACK con DDE WM** inviati devono creare o riutilizzare il parametro *lParam* chiamando la funzione [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .

Se un'applicazione ha avviato la chiusura di una conversazione pubblicando la terminazione di [**WM \_ DDE \_**](wm-dde-terminate.md) ed è in attesa di conferma, l'applicazione in attesa non deve riconoscere (in modo positivo o negativo) i messaggi successivi inviati dall'altra applicazione. L'applicazione in attesa deve eliminare tutti gli atomi o gli oggetti di memoria condivisa ricevuti in questi messaggi. Gli oggetti memoria non devono essere liberati se il flag **fRelease** è impostato su **false** nei messaggi di [**\_ \_ dati DDE**](wm-dde-data.md) del DDE [**WM \_ \_**](wm-dde-poke.md) e WM.

### <a name="receiving"></a>Ricezione

L'applicazione che riceve un **messaggio \_ \_ ACK DDE WM** deve eliminare tutti gli atomi che accompagnano il messaggio. Se l'applicazione riceve un **\_ \_ ACK DDE di WM** in risposta a un messaggio con un oggetto di memoria globale associato e l'oggetto è stato inviato con i flag **fRelease** impostati su **false**, l'applicazione è responsabile dell'eliminazione dell'oggetto.

Se l'applicazione riceve un messaggio **\_ \_ ACK DDE di WM** negativo inviato in risposta a un messaggio di [**\_ \_ avviso DDE di WM**](wm-dde-advise.md) , l'applicazione deve eliminare l'oggetto memoria globale inviato con il messaggio di **\_ \_ notifica DDE** di WM originale. Se l'applicazione riceve un messaggio **\_ \_ ACK DDE di WM** negativo pubblicato in risposta a [**\_ \_ dati DDE WM**](wm-dde-data.md), [**WM \_ DDE \_ poke**](wm-dde-poke.md)o [**WM \_ DDE \_ Execute**](wm-dde-execute.md) Message, l'applicazione deve eliminare l'oggetto memoria globale inviato con i **\_ \_ dati DDE di WM** originali, **WM \_ DDE \_ poke** o WM DDE **\_ \_ Execute** Message.

L'applicazione che riceve un messaggio **di \_ \_ ACK DDE WM** inviato deve liberare il parametro *lParam* usando la funzione [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) .

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

[**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[**\_avviso DDE di WM \_**](wm-dde-advise.md)
</dt> <dt>

[**\_dati DDE di WM \_**](wm-dde-data.md)
</dt> <dt>

[**esecuzione di WM \_ DDE \_**](wm-dde-execute.md)
</dt> <dt>

[**\_avvio DDE \_ WM**](wm-dde-initiate.md)
</dt> <dt>

[**\_poke DDE \_ WM**](wm-dde-poke.md)
</dt> <dt>

[**\_richiesta DDE \_ WM**](wm-dde-request.md)
</dt> <dt>

[**\_ \_ terminazione DDE WM**](wm-dde-terminate.md)
</dt> <dt>

[**\_Unadvise DDE WM \_**](wm-dde-unadvise.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni su Dynamic Data Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

