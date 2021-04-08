---
title: Codice di notifica EN_SELCHANGE (RichEdit. h)
description: Notifica alla finestra padre di un controllo Rich Edit che la selezione corrente è stata modificata. Un controllo Rich Edit invia questo codice di notifica sotto forma di un \_ messaggio di notifica WM.
ms.assetid: 53d47b53-a73c-4652-889c-2374f8e99382
keywords:
- Controlli di Windows per il codice di notifica EN_SELCHANGE
topic_type:
- apiref
api_name:
- EN_SELCHANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79dfcf951f88fa1e10f4723bd9843421f0e20ae5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743031"
---
# <a name="en_selchange-notification-code"></a>\_Codice di notifica en SelChange

Notifica alla finestra padre di un controllo Rich Edit che la selezione corrente è stata modificata. Un controllo Rich Edit invia questo codice di notifica sotto forma di un messaggio di [**\_ notifica WM**](wm-notify.md) .


```C++
EN_SELCHANGE

    pSelChange = (SELCHANGE *) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Struttura [**selChange**](/windows/desktop/api/Richedit/ns-richedit-selchange) che riceve informazioni sulla selezione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo codice di notifica non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Per ricevere \_ i codici di notifica en SelChange, specificare [**ENM \_ selChange**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il messaggio [**\_ SETEVENTMASK em**](em-seteventmask.md) .

Questo codice di notifica viene inviato quando viene modificata la posizione del punto di inserimento e non è selezionato alcun testo (la selezione è vuota). La posizione del punto di inserimento può variare quando l'utente fa clic con il mouse, digita o preme un tasto di direzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange)
</dt> <dt>

[**\_notifica WM**](wm-notify.md)
</dt> </dl>

 

 





