---
title: Codice di notifica CBEN_ENDEDIT (COMmctrl. h)
description: Inviato quando l'utente ha concluso un'operazione all'interno della casella di modifica o ha selezionato un elemento dall'elenco a discesa del controllo. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: b6b50951-7304-4499-b57b-a5b592de2190
keywords:
- Controlli di Windows per il codice di notifica CBEN_ENDEDIT
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
ms.openlocfilehash: 679b9f878dbd8f7f374b461ee548f9ce2c62e281
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400262"
---
# <a name="cben_endedit-notification-code"></a>Codice di notifica di CBEN \_ ENDEDIT

Inviato quando l'utente ha concluso un'operazione all'interno della casella di modifica o ha selezionato un elemento dall'elenco a discesa del controllo. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
CBEN_ENDEDIT

    pnmEditInfo = (PNMCBEENDEDIT) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMCBEENDEDIT**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbeendedita) che contiene informazioni sul modo in cui l'utente ha concluso l'operazione di modifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**False** per accettare il codice di notifica e consentire al controllo di visualizzare l'elemento selezionato; in caso contrario, **true**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **CBEN \_ ENDEDITW** (Unicode) e **CBEN \_ ENDEDITA** (ANSI)<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni sui controlli ComboBoxEx](comboboxex-controls.md)
</dt> </dl>

 

 





