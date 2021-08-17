---
title: CBEN_ENDEDIT codice di notifica (Commctrl.h)
description: Inviato quando l'utente ha terminato un'operazione all'interno della casella di modifica o ha selezionato un elemento dall'elenco a discesa del controllo. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: b6b50951-7304-4499-b57b-a5b592de2190
keywords:
- CBEN_ENDEDIT codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- CBEN_ENDEDIT
- CBEN_ENDEDITA
- CBEN_ENDEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22ae9205e84e4f1c0b10e516b1f406f2d167f1bc5cc38417a31379d20e16fcac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413951"
---
# <a name="cben_endedit-notification-code"></a>Codice di notifica \_ CBEN ENDEDIT

Inviato quando l'utente ha terminato un'operazione all'interno della casella di modifica o ha selezionato un elemento dall'elenco a discesa del controllo. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
CBEN_ENDEDIT

    pnmEditInfo = (PNMCBEENDEDIT) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMCBEENDEDIT**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbeendedita) che contiene informazioni sul modo in cui l'utente ha terminato l'operazione di modifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**FALSE** per accettare il codice di notifica e consentire al controllo di visualizzare l'elemento selezionato. in caso contrario, **TRUE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **CBEN \_ ENDEDITW** (Unicode) e **CBEN \_ ENDEDITA** (ANSI)<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni sui controlli ComboBoxEx](comboboxex-controls.md)
</dt> </dl>

 

 





