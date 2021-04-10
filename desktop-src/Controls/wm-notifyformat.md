---
title: Messaggio WM_NOTIFYFORMAT (winuser. h)
description: Determina se una finestra accetta strutture ANSI o Unicode nel messaggio di \_ notifica di WM Notify. I \_ messaggi WM NOTIFYFORMAT vengono inviati da un controllo comune alla relativa finestra padre e dalla finestra padre al controllo comune.
ms.assetid: 45ddef45-3300-448d-b609-5fe931b08336
keywords:
- Controlli di Windows Message WM_NOTIFYFORMAT
topic_type:
- apiref
api_name:
- WM_NOTIFYFORMAT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57e9c7d74b21d0f5785273d1b60d612a346f2d85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964462"
---
# <a name="wm_notifyformat-message"></a>\_Messaggio NOTIFYFORMAT WM

Determina se una finestra accetta strutture ANSI o Unicode nel messaggio di notifica di [**WM \_ Notify**](wm-notify.md) . **WM \_** I messaggi NOTIFYFORMAT vengono inviati da un controllo comune alla relativa finestra padre e dalla finestra padre al controllo comune.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra che invia il messaggio **WM \_ NOTIFYFORMAT** . Se *lParam* è \_ una query NF, questo parametro è l'handle di un controllo. Se *lParam* è NF \_ Requery, questo parametro è l'handle per la finestra padre di un controllo.

</dd> <dt>

*lParam* 
</dt> <dd>

Valore del comando che specifica la natura del messaggio **WM \_ NOTIFYFORMAT** . Si otterrà uno dei valori seguenti:



| Valore                                                                                                                                                | Significato                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NF_QUERY"></span><span id="nf_query"></span><dl> <dt>**\_query NF**</dt> </dl>       | Il messaggio è una query per determinare se le strutture ANSI o Unicode devono essere utilizzate nei messaggi di [**\_ notifica WM**](wm-notify.md) . Questo comando viene inviato da un controllo alla relativa finestra padre durante la creazione di un controllo e in risposta a un \_ comando NF Requery.<br/>                                                                                                         |
| <span id="NF_REQUERY"></span><span id="nf_requery"></span><dl> <dt>**Requery NF \_**</dt> </dl> | Il messaggio è una richiesta di invio di un \_ modulo di query NF di questo messaggio alla finestra padre di un controllo. Questo comando viene inviato dalla finestra padre. La finestra padre chiede al controllo di eseguire di nuovo la query sul tipo di strutture da usare nei messaggi di [**\_ notifica WM**](wm-notify.md) . Se *lParam* è NF \_ Requery, il valore restituito è il risultato dell'operazione di riesecuzione della query.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori seguenti.



| Codice restituito                                                                                 | Descrizione                                                                                                    |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NFR \_ ANSI**</dt> </dl>    | È consigliabile usare le strutture ANSI nei messaggi [**WM \_ Notify**](wm-notify.md) inviati dal controllo.<br/>     |
| <dl> <dt>**NFR \_ Unicode**</dt> </dl> | Le strutture Unicode devono essere usate nei messaggi [**WM \_ Notify**](wm-notify.md) inviati dal controllo. <br/> |
| <dl> <dt>**0**</dt> </dl>            | Si è verificato un errore.<br/>                                                                                  |



 

## <a name="remarks"></a>Commenti

Quando viene creato un controllo comune, il controllo Invia un messaggio **WM \_ NOTIFYFORMAT** alla finestra padre per determinare il tipo di strutture da usare nei messaggi [**di \_ notifica WM**](wm-notify.md) . Se la finestra padre non gestisce questo messaggio, la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) risponde in base al tipo della finestra padre. Ovvero, se la finestra padre è una finestra Unicode, **DefWindowProc** restituisce NFR \_ Unicode e se la finestra padre è una finestra ANSI, **DefWindowProc** restituisce NFR \_ ANSI. Se la finestra padre è una finestra di dialogo e non gestisce questo messaggio, la funzione [**DefDlgProc**](/windows/desktop/api/winuser/nf-winuser-defdlgprocw) risponde in modo analogo a seconda del tipo di finestra di dialogo (Unicode o ANSI).

Una finestra padre può modificare il tipo di strutture usate da un controllo comune nei messaggi di [**\_ notifica WM**](wm-notify.md) impostando *lParam* su NF per \_ ripetere la query e inviando un messaggio **WM \_ NOTIFYFORMAT** al controllo. Questo fa in modo che il controllo invii un \_ modulo di query NF del messaggio **WM \_ NOTIFYFORMAT** alla finestra padre.

Tutti i controlli comuni invieranno messaggi **WM \_ NOTIFYFORMAT** . Tuttavia, i controlli Windows standard (modifica controlli, caselle combinate, caselle di riepilogo, pulsanti, barre di scorrimento e controlli statici) non lo sono.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



 

